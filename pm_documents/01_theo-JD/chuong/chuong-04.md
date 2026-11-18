# Chương 4 · Base kỹ thuật cho PM (Q301–Q400)

## 4.1 Kiến trúc & thiết kế hệ thống

**Q301. Là PM, anh/chị cần hiểu kiến trúc hệ thống đến mức nào?**
Đủ để ra quyết định trade-off và hỏi đúng câu, không cần tự thiết kế. Tôi phải đọc được tài liệu 方式設計 (houshiki sekkei – thiết kế kiến trúc), biết mỗi thành phần kéo theo chi phí, tiến độ, rủi ro gì, và nhận ra khi công nghệ được chọn vì "team thích" chứ không vì yêu cầu. Thước đo của tôi: giải thích lại được cho khách bằng ngôn ngữ nghiệp vụ và nêu được 3 rủi ro kỹ thuật lớn nhất của dự án.
> 💡 Đừng nói "kỹ thuật để tech lead lo" — interviewer muốn thấy PM chủ động phản biện kỹ thuật bằng câu hỏi về rủi ro và chi phí.

**Q302. Khi nào nên chọn monolith, khi nào chọn microservices?**
Mặc định tôi nghiêng về **modular monolith** khi team nhỏ (vd dưới 15 người), domain chưa ổn định, deadline gấp: deploy một lần, debug dễ, hạ tầng rẻ. Microservices chỉ đáng khi có lý do thật: các module cần scale rất khác nhau, nhiều team phải release độc lập, hoặc vòng đời công nghệ khác nhau. Cái giá là distributed transaction, monitoring, CI/CD cho từng service và kỹ năng DevOps — effort hạ tầng tăng rõ, nên tôi yêu cầu tech lead ghi lý do vào ADR.

**Q303. Kiến trúc phân tầng (layered) giúp gì cho PM khi quản lý dự án offshore?**
Tách presentation – business logic – data access giúp chia việc theo tầng, estimate theo đơn vị rõ, và khoanh vùng 影響調査 (eikyou chousa – phân tích ảnh hưởng) khi có 仕様変更 (shiyou henkou – thay đổi đặc tả). Ví dụ đổi công thức tính phí chỉ chạm tầng business, tôi báo khách mức ảnh hưởng nhỏ và test hồi quy tập trung. Rủi ro là dev "xuyên tầng" (controller gọi thẳng DB) làm vỡ ranh giới — tôi đưa quy tắc này vào checklist review.

**Q304. Event-driven architecture là gì và kéo theo rủi ro dự án nào?**
Các thành phần giao tiếp qua sự kiện (vd "đơn hàng đã tạo") thay vì gọi trực tiếp, nên tách rời và mở rộng dễ. Rủi ro với PM: ① khó trace luồng khi lỗi; ② dữ liệu chỉ nhất quán sau một khoảng trễ (eventual consistency) — người dùng phía khách dễ coi là bug; ③ test E2E phức tạp hơn. Tôi chốt sớm với khách độ trễ chấp nhận được (vd ≤ 5 giây, tham khảo) và yêu cầu correlation ID trong log ngay từ sprint đầu.

**Q305. Batch và online khác nhau thế nào, vì sao khách Nhật vẫn rất chuộng 夜間バッチ?**
Online xử lý từng giao dịch tức thời; batch gom xử lý theo lô, thường chạy đêm — 夜間バッチ (yakan bacchi – batch ban đêm) — để tính lãi, đối soát, tạo file gửi đối tác mà không ảnh hưởng giờ nghiệp vụ. Khách tài chính, sản xuất Nhật chuộng vì quy trình nghiệp vụ đã xây quanh chu kỳ ngày/tháng và dễ kiểm soát. PM phải quản lý **batch window**: mọi job phải xong trước giờ mở online, kèm phương án rerun khi job lỗi lúc 3 giờ sáng.
> 💡 Hỏi ngay "batch window mấy giờ, dữ liệu tăng bao nhiêu mỗi năm" là dấu hiệu PM từng làm batch thật.

**Q306. Hệ thống có hàng trăm job batch phụ thuộc nhau, PM cần kiểm soát gì?**
Ba thứ: ① ジョブネット (jobu netto – chuỗi job có phụ thuộc) được vẽ thành sơ đồ, biết job nào nằm trên đường găng của batch window; ② thiết kế restart/rerun để chạy lại không sinh dữ liệu trùng; ③ công cụ scheduler phía khách (ở Nhật hay gặp JP1 của Hitachi) và ai được thao tác trên 本番 (honban – môi trường production). Trước go-live, tôi yêu cầu đo thời gian chạy với khối lượng dữ liệu gần thực tế và chừa dư ≥ 30% batch window (tham khảo).

**Q307. Scale up và scale out khác nhau thế nào, PM quan tâm điểm nào?**
Scale up là tăng cấu hình một máy — đơn giản nhưng có trần và thường phải dừng hệ thống; scale out là thêm máy — linh hoạt nhưng đòi ứng dụng stateless, session/cache dùng chung. PM quan tâm: chi phí theo tải, phản hồi khi tải tăng đột biến (vd cao điểm cuối tháng), và kiến trúc có cho phép scale out không — sửa sau rất đắt. Tôi xin khách con số tải dự kiến 3–5 năm để thiết kế vừa đủ, không over-engineer.

**Q308. ADR là gì, vì sao PM nên đòi tech lead viết?**
ADR (Architecture Decision Record) ghi mỗi quyết định kiến trúc: bối cảnh, các phương án, lựa chọn, hệ quả. Dự án offshore hay xoay vòng nhân sự, và khách Nhật thường hỏi lại "vì sao chọn thế này" sau vài tháng — ADR trả lời trong một phút thay vì tranh luận lại. Tôi yêu cầu mỗi ADR một trang, có mục chi phí và rủi ro, link từ tài liệu 基本設計 (kihon sekkei – thiết kế cơ bản), và gửi khách xác nhận những ADR ảnh hưởng phạm vi hoặc chi phí.

**Q309. 非機能要件 gồm những gì, vì sao hay thành nguồn tranh chấp?**
非機能要件 (hikinou youken – yêu cầu phi chức năng) gồm hiệu năng, availability, bảo mật, vận hành, khả năng mở rộng, di chuyển dữ liệu. Tranh chấp xảy ra vì khách hiếm khi nói ra ("đương nhiên phải nhanh") nhưng lúc nghiệm thu lại đòi, trong khi effort giữa các mức chênh rất lớn. Tôi dùng 非機能要求グレード (hikinou youkyuu gureedo – bộ phân cấp yêu cầu phi chức năng) của IPA làm checklist để khách chọn mức cụ thể từng hạng mục ngay giai đoạn 要件定義 (youken teigi – định nghĩa yêu cầu).
> 💡 Nhắc 非機能要求グレード của IPA là điểm cộng lớn — cho thấy bạn quen cách khách Nhật chốt NFR.

**Q310. Làm sao chốt NFR với khách bằng con số đo được?**
① Đổi câu mơ hồ thành chỉ số: "nhanh" → 95% request màn tra cứu ≤ 2 giây với 500 user đồng thời; "luôn chạy" → 稼働率 (kadouritsu – tỉ lệ hoạt động) 99.9% trong giờ nghiệp vụ. ② Ghi điều kiện đo: khối lượng dữ liệu, môi trường, công cụ. ③ Báo chi phí của từng mức để khách tự chọn. ④ Đưa vào tài liệu yêu cầu và kịch bản 性能試験 (seinou shiken – kiểm thử hiệu năng) để nghiệm thu không phải tranh cãi.

**Q311. Khách yêu cầu availability 99.99% cho một hệ thống nội bộ, anh/chị phản hồi thế nào?**
Tôi không từ chối mà quy ra hệ quả: 99.99% nghĩa là chỉ được dừng khoảng 52 phút/năm kể cả bảo trì, cần 冗長化 (jouchouka – dự phòng) mọi tầng, multi-AZ, deploy không downtime, trực 24/7 — chi phí cao hơn nhiều so với 99.9% (khoảng 8,8 giờ/năm). Sau đó hỏi ngược: nghiệp vụ mất gì nếu dừng 1 giờ? Thường khách chọn 99.9% trong giờ hành chính kèm thời gian khôi phục rõ ràng. Kết luận ghi vào biên bản và ADR.
> 💡 Biến tranh luận kỹ thuật thành lựa chọn chi phí – rủi ro để khách tự quyết; PM không đứng ra "từ chối".

**Q312. Tech lead bên mình và kỹ sư phía khách bất đồng về giải pháp kỹ thuật, PM làm gì?**
① Tách cảm xúc khỏi dữ kiện: yêu cầu mỗi bên trình bày phương án theo cùng một khung — mục tiêu, trade-off, chi phí, rủi ro, ảnh hưởng NFR và tiến độ. ② Nếu còn tranh cãi, làm PoC nhỏ với tiêu chí đo chốt trước (vd 2–3 ngày công). ③ Trình bày như lựa chọn có căn cứ, không phải "bên tôi đúng"; quyết định cuối thuộc chủ hệ thống. ④ Ghi ADR để không mở lại. Tôi không để tech lead một mình tranh luận với khách — PM đứng giữa giữ quan hệ.

## 4.2 API & tích hợp hệ thống

**Q313. REST và GraphQL khác nhau ra sao, khi nào PM đồng ý dùng GraphQL?**
REST tổ chức theo resource với endpoint cố định, dễ cache, dễ hiểu với kỹ sư phía khách; GraphQL cho client tự chọn trường cần lấy qua một endpoint, hợp với app mobile/web có nhiều màn hiển thị dữ liệu đa dạng. Tôi đồng ý GraphQL khi có nhiều loại client và team đã có kinh nghiệm; ngược lại REST an toàn hơn vì với GraphQL, phân quyền theo trường, giới hạn độ phức tạp query và giám sát hiệu năng đều khó hơn. Quyết định ghi vào ADR.

**Q314. Contract API (OpenAPI) giúp gì cho quản lý dự án nhiều bên?**
OpenAPI là "hợp đồng" giữa front-end, back-end và hệ thống của khách: chốt sớm thì các bên làm song song bằng mock server, không chờ nhau. Tôi coi file contract là baseline — đổi field là thay đổi có kiểm soát, có version, báo bên phụ thuộc trước. Ví dụ với khách bảo hiểm B, chốt contract trước sprint 1 làm lộ ra chuyện hai bên hiểu khác định dạng ngày ngay từ đầu, thay vì đến 結合テスト (ketsugou tesuto – kiểm thử tích hợp) mới phát hiện.

**Q315. OAuth2, OIDC và SSO — PM cần hiểu ở mức nào?**
OAuth2 là chuẩn **ủy quyền** (cấp token để ứng dụng gọi API thay user); OIDC thêm lớp **xác thực** trên OAuth2 (biết user là ai qua ID token); SSO là trải nghiệm đăng nhập một lần cho nhiều hệ thống, thường dựng bằng OIDC hoặc SAML. PM cần hiểu để hỏi đúng: IdP của khách là gì (Entra ID, Okta…), ai cấp tài khoản test, quy trình đăng ký redirect URL và client secret — những việc phụ thuộc phía khách rất hay làm trễ tiến độ.
> 💡 Bẫy: gọi OAuth2 là chuẩn xác thực — phân biệt rõ authorization và authentication là ghi điểm ngay.

**Q316. Tích hợp với hệ thống cũ của khách thường gặp rủi ro gì, kiểm soát thế nào?**
Rủi ro lớn nhất: tài liệu interface không khớp thực tế, không có môi trường test của hệ thống đối tác, người nắm hệ thống đã nghỉ. Tôi kiểm soát bằng: ① xin dữ liệu mẫu thật (đã mask) ngay tuần đầu; ② lập danh sách interface có owner, định dạng, tần suất, ngày có môi trường kết nối; ③ đưa ngày "có môi trường đối tác" vào kế hoạch như mốc phụ thuộc, lệch là báo ngay theo 報連相 (hou-ren-sou – báo cáo, liên lạc, thảo luận).

**Q317. File interface CSV và 固定長 có những bẫy gì với hệ thống Nhật?**
Với 固定長 (koteichou – bản ghi độ dài cố định), field tính theo byte nên bảng mã quyết định tất cả: ký tự 全角 (zenkaku – toàn độ rộng) chiếm 2 byte trong Shift_JIS nhưng thường 3 byte trong UTF-8, mainframe có thể dùng EBCDIC. Bẫy khác: 半角カナ (hankaku kana – katakana nửa độ rộng), 外字 (gaiji – ký tự ngoài bảng mã chuẩn) trong tên người, CRLF/LF, ngày 和暦 (wareki – lịch niên hiệu), padding bằng 0 hay space. Tôi yêu cầu bảng định nghĩa layout file và test bằng file thật từ sớm.
> 💡 Kể một lỗi encoding cụ thể (vd tên khách hàng bị cắt mất nửa ký tự 全角) cho thấy bạn đã làm thật.

**Q318. Message queue dùng để làm gì, ảnh hưởng gì đến thiết kế và test?**
Queue (SQS, RabbitMQ, Kafka…) tách bên gửi và bên nhận: hấp thụ tải đột biến, xử lý bất đồng bộ, bên nhận chết thì message vẫn chờ. Đổi lại phải thiết kế cho message trùng, sai thứ tự, message lỗi lặp vô hạn (cần dead-letter queue) và giám sát độ dài hàng đợi. Với PM, điều này nghĩa là thêm test case cho tình huống lỗi và thêm việc vận hành — tôi yêu cầu tech lead liệt kê các phần này trước khi estimate, tránh chỉ tính happy path.

**Q319. Idempotency là gì, vì sao PM phải quan tâm?**
Idempotent nghĩa là gọi một thao tác nhiều lần cho cùng kết quả như gọi một lần. Retry do timeout mạng là chuyện thường; nếu API chuyển tiền hay tạo đơn không idempotent, khách hàng cuối có thể bị trừ tiền hai lần — sự cố nghiêm trọng với khách tài chính. Tôi yêu cầu API ghi dữ liệu nhận idempotency key, batch rerun không tạo bản ghi trùng, và có test case "gửi hai lần" trong kịch bản nghiệm thu.
> 💡 Ví dụ "trừ tiền hai lần" là cách giải thích idempotency dễ hiểu nhất cho interviewer không thuần kỹ thuật.

**Q320. Đối tác của khách đổi định dạng API không báo trước làm production lỗi. Anh/chị xử lý thế nào?**
① Xác nhận fact: log cho thấy field nào đổi, từ lúc nào, bao nhiêu giao dịch bị ảnh hưởng. ② Khoanh vùng: tạm dừng nhận hoặc đưa vào hàng chờ để dữ liệu sai không lan, chuẩn bị xử lý lại. ③ Báo khách theo 報連相 càng sớm càng tốt kèm phạm vi ảnh hưởng — đầu mối với đối tác là khách. ④ 再発防止 (saihatsu boushi – phòng tái phát): validate schema đầu vào, contract test, thỏa thuận báo trước khi đổi; 横展開 (yokotenkai – áp dụng ngang) rà các interface còn lại.

**Q321. Dự án có nhiều interface với hệ thống ngoài, PM lập kế hoạch kiểm thử tích hợp thế nào?**
Tôi lập ma trận interface: hệ thống đối tác, chiều dữ liệu, giao thức, môi trường test đã có hay chưa, owner phía khách. Interface chưa có môi trường thì dùng stub/mock để dev không chờ, nhưng vẫn giữ một đợt test với hệ thống thật trước 総合テスト (sougou tesuto – kiểm thử hệ thống tổng thể). Lịch test liên kết phải chốt sớm vì các bên có lịch riêng; mỗi interface có tiêu chí hoàn thành rõ, vd 100% case bình thường và các case lỗi timeout, sai định dạng.

**Q322. Timeout, retry, rate limit — PM có cần quan tâm không?**
Có, vì đây là nguồn sự cố production và chi phí. Gọi API bên ngoài phải có timeout rõ, retry có giới hạn và backoff; nếu không, một đối tác chậm có thể kéo sập cả hệ thống (cascading failure). Rate limit của API bên thứ ba ảnh hưởng thiết kế batch và có thể buộc mua gói cao hơn. Tôi yêu cầu bảng **external dependency** ghi giới hạn, SLA, chi phí, đầu mối hỗ trợ của từng dịch vụ và rà lại trước go-live.

**Q323. Dev estimate tích hợp API thanh toán của đối tác chỉ 3 ngày. Anh/chị kiểm tra con số đó thế nào?**
Tôi không bác con số mà đặt câu hỏi để lộ phần bị bỏ sót: ① đã có tài liệu API, sandbox, tài khoản test chưa; ② xác thực, ký request, lưu key ở đâu; ③ xử lý timeout, retry, idempotency, đối soát giao dịch lệch; ④ test case lỗi và test chung với đối tác mất bao lâu; ⑤ log và mask dữ liệu thẻ. Thường 3 ngày chỉ là happy path. Tôi để dev tự estimate lại theo danh sách này — vừa sát hơn vừa để dev giữ quyền sở hữu con số.
> 💡 Challenge estimate bằng checklist câu hỏi kỹ thuật, không bằng câu "anh thấy lâu/nhanh quá".

## 4.3 Database & dữ liệu

**Q324. RDBMS và NoSQL — khi nào chọn loại nào?**
RDBMS (Oracle, PostgreSQL, MySQL, SQL Server) mạnh ở transaction ACID, ràng buộc toàn vẹn, truy vấn phức tạp — gần như mặc định cho dữ liệu tiền, hợp đồng, kế toán. NoSQL (DynamoDB, MongoDB, Redis…) hợp với dữ liệu lớn, schema linh hoạt, truy cập theo key độ trễ thấp như session, log, catalog. Nhiều hệ thống dùng cả hai. Câu hỏi PM đặt ra: team đã vận hành công nghệ này chưa, khách có chuẩn DB nội bộ hay license sẵn không — khách lớn thường đã chuẩn hóa.

**Q325. Index giúp gì và có cái giá gì?**
Index như mục lục, giúp truy vấn tìm nhanh thay vì quét toàn bảng — có thể giảm từ vài giây xuống mili giây. Cái giá: tốn dung lượng, làm chậm insert/update, và index đặt sai thì vô ích. Khi màn hình chậm, tôi hỏi tech lead đã xem execution plan chưa trước khi đồng ý nâng cấp server — nguyên nhân thường là thiếu index hoặc truy vấn N+1 chứ không phải phần cứng.

**Q326. Transaction và lock ảnh hưởng thế nào đến hệ thống?**
Transaction đảm bảo một nhóm thao tác hoặc thành công hết hoặc không gì cả (ACID) — vd chuyển khoản trừ bên A thì phải cộng bên B. Lock ngăn dữ liệu bị sửa đồng thời; lock giữ lâu hoặc sai thứ tự sinh chờ đợi và deadlock, thường lộ ra khi batch đêm chạy chồng giờ online. PM cần đảm bảo kế hoạch 性能試験 có kịch bản chạy đồng thời online + batch, và chốt với khách quy tắc khi hai người cùng sửa một bản ghi (khóa lạc quan hay bi quan).

**Q327. データ移行 thường thất bại vì đâu?**
データ移行 (deeta ikou – di chuyển dữ liệu) hay thất bại vì: ① dữ liệu cũ kém chất lượng (trùng, thiếu, giá trị ngoài quy ước) mà không ai biết đến lúc chạy thật; ② mapping thiếu trường hợp đặc biệt; ③ thời gian chạy vượt cửa sổ chuyển đổi; ④ không có tiêu chí đối soát rõ. Tôi coi migration là một dự án con có WBS, owner, test riêng — không phải "việc của tuần cuối" — và bắt đầu profiling dữ liệu ngay từ giai đoạn thiết kế.
> 💡 Câu ăn điểm: "migration là dự án con, bắt đầu từ ngày đầu, không phải tuần cuối".

**Q328. 移行リハーサル nên tổ chức thế nào?**
移行リハーサル (ikou rihaasaru – diễn tập di chuyển) chạy toàn bộ quy trình như ngày thật: cùng khối lượng dữ liệu, cùng 手順書 (tejunsho – tài liệu thủ tục), cùng người, đo thời gian từng bước. Tôi làm tối thiểu 2–3 lần (tham khảo): lần đầu tìm lỗi, lần sau tối ưu thời gian, lần cuối "y như thật" kèm diễn tập rollback. Tiêu chí qua: đối soát khớp 100%, tổng thời gian ≤ 70–80% cửa sổ chuyển đổi, không có thao tác ngoài thủ tục.

**Q329. Đối soát số liệu sau migration thế nào để khách tin?**
Đối soát nhiều tầng: ① số bản ghi từng bảng trước/sau; ② tổng kiểm (tổng số dư, tổng số tiền theo kỳ, checksum); ③ so từng bản ghi với mẫu dữ liệu đặc biệt; ④ chạy cùng báo cáo nghiệp vụ trên hệ thống cũ và mới rồi so kết quả. Tiêu chí và script đối soát được khách duyệt trước, kết quả có log làm bằng chứng — với khách tài chính, lệch một yên cũng phải giải thích được.
> 💡 Mời khách tự chọn mẫu bản ghi để đối soát — tạo niềm tin hơn mọi báo cáo do vendor tự làm.

**Q330. Kế hoạch rollback cho migration gồm những gì?**
Gồm: ① điểm Go/No-Go có giờ cố định (vd 4:00 sáng) và người có quyền quyết; ② điều kiện kích hoạt rollback đo được (đối soát lệch, vượt giờ); ③ backup đầy đủ hệ thống cũ và thủ tục 切り戻し (kirimodoshi – quay về trạng thái cũ) đã diễn tập; ④ cách xử lý dữ liệu phát sinh sau thời điểm chuyển. Rollback chưa diễn tập thì coi như không có — tôi luôn đưa nó vào ít nhất một lần rehearsal.

**Q331. Schema thay đổi giữa dự án, làm sao không phá dữ liệu và tiến độ?**
Dùng migration script có version (Flyway, Liquibase…) chạy giống nhau ở mọi môi trường, không sửa tay DB. Với hệ thống đang chạy, áp dụng expand–contract: thêm cột mới song song, chuyển dữ liệu, chuyển code, cuối cùng mới xóa cột cũ — lúc nào cũng rollback được. Về PM, mỗi thay đổi schema phải qua 影響調査: màn hình, batch, file interface, báo cáo nào bị chạm, và cập nhật tài liệu thiết kế DB — thứ khách Nhật thường kiểm rất kỹ.

**Q332. Khách muốn đưa dữ liệu production thật cho team offshore test, anh/chị xử lý thế nào?**
Tôi không nhận dữ liệu thật về offshore khi chưa có thỏa thuận và biện pháp bảo vệ. Đề xuất theo thứ tự: ① dữ liệu giả lập theo quy tắc nghiệp vụ; ② dữ liệu thật đã mask/ẩn danh (tên, điện thoại, số tài khoản) do phía khách làm; ③ bắt buộc dùng dữ liệu thật thì test trên môi trường của khách, truy cập remote có log. Lý do: trách nhiệm bảo vệ 個人情報 (kojin jouhou – thông tin cá nhân) và rủi ro uy tín cho cả hai bên.
> 💡 Từ chối bằng phương án thay thế chứ không bằng chữ "không" — cách khách Nhật dễ chấp nhận nhất.

**Q333. Dữ liệu tăng nhanh làm hệ thống chậm dần, PM xử lý ra sao?**
① Đo trước: tốc độ tăng dữ liệu mỗi tháng, truy vấn nào chậm nhất. ② Chọn giải pháp theo chi phí tăng dần: tối ưu index/truy vấn, partition bảng theo tháng, archive dữ liệu cũ sang lưu trữ rẻ, cuối cùng mới nâng phần cứng. ③ Đưa vào backlog có ưu tiên kèm dự báo, vd "không làm thì 6 tháng nữa màn tra cứu vượt NFR". Chính sách lưu giữ và xóa dữ liệu phải do khách quyết vì có thể liên quan quy định pháp lý và kiểm toán.

## 4.4 Cloud

**Q334. Phân biệt IaaS, PaaS, SaaS theo góc nhìn trách nhiệm và chi phí.**
IaaS (vd EC2) cho thuê máy ảo — mình lo OS, patch, middleware; PaaS (vd RDS, Elastic Beanstalk) nhà cung cấp lo nền tảng, mình lo ứng dụng và dữ liệu; SaaS (vd Microsoft 365, Salesforce) dùng sẵn, chỉ cấu hình. Càng lên cao càng ít việc vận hành nhưng càng phụ thuộc nhà cung cấp, ít tùy biến. Với PM, lựa chọn này quyết định phạm vi 運用保守 (unyou hoshu – vận hành bảo trì) và phải ghi rõ trong hợp đồng ai chịu phần nào.

**Q335. Mô hình trách nhiệm chung (shared responsibility) của AWS ảnh hưởng gì đến dự án?**
AWS chịu trách nhiệm bảo mật "của" cloud (data center, phần cứng, hạ tầng ảo hóa); khách hàng chịu trách nhiệm bảo mật "trong" cloud (IAM, network, mã hóa dữ liệu, patch OS nếu dùng EC2). Nhiều sự cố lộ dữ liệu trên cloud đến từ cấu hình sai như bucket S3 để public. PM phải chốt trong hợp đồng phần nào do vendor, khách hay đơn vị vận hành chịu, và đưa review cấu hình bảo mật vào checklist trước go-live.

**Q336. Giải thích nhanh EC2, S3, RDS, Lambda, VPC, IAM và khi nào dùng.**
Máy ảo **EC2** dùng khi cần kiểm soát OS hoặc chuyển nguyên trạng ứng dụng cũ; **S3** lưu trữ object (file, ảnh, backup, file interface); **RDS** là database được quản lý sẵn, có backup tự động và Multi-AZ; **Lambda** chạy code theo sự kiện, trả tiền theo lần chạy, giới hạn 15 phút/lần nên không hợp batch dài; **VPC** là mạng riêng ảo chia subnet public/private; **IAM** quản lý user, role, quyền. PM cần nắm để đọc sơ đồ hạ tầng và biết dòng chi phí nào từ đâu ra.

**Q337. Kiểm soát chi phí cloud (FinOps) trong dự án thế nào?**
① Ước tính bằng AWS Pricing Calculator ngay từ proposal, tách theo môi trường. ② Gắn tag (dự án, môi trường, owner) cho mọi resource để báo cáo được. ③ Đặt budget alert, vd cảnh báo ở 80% ngân sách tháng (tham khảo). ④ Tắt dev/staging ngoài giờ, chọn đúng size, dùng Savings Plans/Reserved Instances cho tải ổn định. ⑤ Review chi phí hằng tháng với tech lead, báo khách khi có xu hướng vượt. Thủ phạm hay gặp: NAT Gateway, data transfer, log lưu vô thời hạn.
> 💡 Nêu được "thủ phạm chi phí ẩn" như NAT Gateway hay log không đặt thời hạn lưu cho thấy kinh nghiệm thật.

**Q338. Multi-AZ, multi-region và DR khác nhau thế nào? RPO, RTO là gì?**
Multi-AZ chạy dự phòng ở nhiều data center trong cùng region (vd Tokyo) — chống sự cố một trung tâm; multi-region (vd Tokyo + Osaka) chống thảm họa cả vùng — khách Nhật rất quan tâm vì rủi ro động đất. RPO là lượng dữ liệu tối đa chấp nhận mất (vd 15 phút), RTO là thời gian tối đa để khôi phục (vd 4 giờ). RPO/RTO càng nhỏ chi phí càng tăng mạnh, nên tôi để khách chọn mức theo độ quan trọng của từng hệ thống và yêu cầu diễn tập DR thật.

**Q339. Vì sao khách tài chính Nhật vẫn chuộng on-premise hoặc private cloud?**
Lý do thường gặp: ① quy định, chuẩn ngành, kiểm toán nội bộ và cơ quan giám sát đòi hỏi giải trình kỹ; ② lo dữ liệu khách hàng ra ngoài tầm kiểm soát hoặc ra nước ngoài; ③ hệ thống lõi gắn với mainframe và 閉域網 (heiikimou – mạng khép kín) sẵn có; ④ văn hóa ưu tiên ổn định, quy trình phê duyệt dài; ⑤ đã đầu tư lớn vào data center và đội vận hành. Hiểu đúng lý do giúp tôi không "bán cloud" mà giải quyết đúng mối lo của khách.

**Q340. Làm sao thuyết phục khách tài chính Nhật đưa một phần hệ thống lên cloud?**
Không thuyết phục bằng "cloud rẻ hơn" mà bằng lộ trình giảm rủi ro: ① bắt đầu từ hệ thống không lõi (dev/test, công cụ nội bộ) để chứng minh; ② trả lời từng mối lo bằng bằng chứng — dữ liệu nằm ở region Tokyo/Osaka, kết nối riêng (Direct Connect), mã hóa bằng key do khách quản lý, tài liệu đối chiếu chuẩn ngành của nhà cung cấp; ③ so TCO 5 năm kể cả chi phí thay phần cứng. Quyết định thuộc về khách, tôi cung cấp dữ liệu để họ quyết.
> 💡 Nhắc "dữ liệu nằm tại region Tokyo/Osaka" đánh trúng mối lo chủ quyền dữ liệu của khách Nhật.

**Q341. Hybrid cloud mang thêm rủi ro gì cho dự án?**
Hybrid giữ dữ liệu lõi tại chỗ và đưa phần linh hoạt lên cloud, nhưng thêm rủi ro: kết nối mạng giữa hai bên (độ trễ, băng thông, đường dự phòng), hai bộ quy trình vận hành và bảo mật, đồng bộ dữ liệu, và sự cố nằm ở "khe giữa" không ai nhận. Tôi lập sơ đồ ranh giới trách nhiệm, đo độ trễ thật sớm, và đưa thời gian xin mở firewall/đường truyền phía khách vào kế hoạch — ở tổ chức lớn việc này có thể mất vài tuần (tham khảo).

**Q342. Vendor lock-in với cloud có đáng lo không?**
Có, nhưng ở mức hợp lý. Né lock-in hoàn toàn thì tốn chi phí và bỏ mất lợi ích của dịch vụ managed. Tôi phân loại: dữ liệu và logic nghiệp vụ lõi giữ ở dạng dễ chuyển (SQL chuẩn, container, Terraform); tiện ích phụ trợ (queue, notification, serverless) chấp nhận dùng dịch vụ riêng của nhà cung cấp. Quan trọng là ADR ghi rõ chi phí ước tính nếu phải chuyển đi, để khách quyết định có ý thức chứ không bị khóa mà không biết.

**Q343. Hóa đơn cloud tháng này vượt 40% so với dự toán, anh/chị xử lý thế nào?**
① Xác nhận fact bằng Cost Explorer: dịch vụ, môi trường, tag nào tăng, từ ngày nào. ② Hành động ngay: tắt resource thừa, giới hạn log, chặn nguyên nhân rõ (môi trường test quên tắt, vòng lặp gọi API). ③ Báo khách theo 報連相: nguyên nhân, số tiền, phần nào do thay đổi yêu cầu, phần nào do lỗi bên mình. ④ 再発防止: budget alert theo ngày, bắt buộc tag, review chi phí trong họp tuần; 横展開 sang các dự án cloud khác của công ty.

## 4.5 DevOps & release

**Q344. Chiến lược branching Git nào hợp với dự án outsourcing?**
GitFlow (develop, feature, release, hotfix) hợp dự án release theo đợt, có UAT dài như nhiều dự án Nhật; trunk-based (nhánh ngắn, merge vào main hằng ngày, dùng feature flag) hợp CI/CD liên tục. Tôi chọn theo nhịp release của khách, nhưng quy tắc quan trọng hơn mô hình: không push thẳng main, mọi merge qua pull request có review, nhánh release đóng băng, hotfix phải merge ngược về các nhánh để tránh デグレ (degure – lỗi hồi quy, tính năng cũ hỏng lại).
> 💡 デグレ do quên merge hotfix ngược là bẫy kinh điển — và khách Nhật đặc biệt khó chịu với デグレ.

**Q345. CI/CD mang lại gì cho PM, khi nào đáng đầu tư?**
CI tự build, chạy test, phân tích tĩnh ở mỗi commit — lỗi lộ ra sau vài phút thay vì vài ngày; CD tự đóng gói và deploy lên môi trường, giảm lỗi thao tác tay. Lợi ích đo được: thời gian từ commit đến môi trường test giảm, lỗi do deploy sai giảm, mọi bản build tái lập và truy vết được. Dự án dài hơn vài tháng gần như luôn đáng; chi phí dựng ban đầu thường vài ngày công (tham khảo) và tôi đưa vào WBS ngay sprint 0.

**Q346. Infrastructure as Code (IaC) là gì, lợi ích gì khi làm với khách Nhật?**
IaC (Terraform, CloudFormation…) mô tả hạ tầng bằng code, được review và quản lý version như code ứng dụng. Lợi ích: dựng môi trường giống hệt nhau nhanh, biết ai đổi gì lúc nào, giảm sai sót thao tác tay. Với khách Nhật, IaC là "tài liệu sống" phục vụ 構成管理 (kousei kanri – quản lý cấu hình) và kiểm toán. Tôi quy định mọi thay đổi hạ tầng production đi qua IaC + review; sửa tay chỉ khi khẩn cấp, phải ghi lại và đồng bộ về code.

**Q347. Container và Kubernetes — PM cần hiểu gì để quyết định?**
Container (Docker) đóng gói ứng dụng cùng môi trường chạy, hết cảnh "máy tôi chạy được"; Kubernetes điều phối nhiều container: tự khởi động lại, scale, rolling update. Kubernetes mạnh nhưng phức tạp và tốn người vận hành — hệ thống vài service thì dịch vụ managed đơn giản hơn (vd ECS) thường đủ. Tôi hỏi: ai vận hành sau go-live, khách có đội platform không, chi phí vận hành mỗi tháng bao nhiêu — chưa trả lời được thì chưa nên chọn Kubernetes.
> 💡 Bẫy: chọn Kubernetes vì "đẹp CV" của team — PM phải hỏi "ai trực nó lúc 2 giờ sáng".

**Q348. Dự án nên có những môi trường nào, quản lý ra sao?**
Tối thiểu: dev cho team phát triển; staging/検証環境 (kenshou kankyou – môi trường kiểm chứng) giống production nhất có thể cho UAT và test hiệu năng; và 本番. Dự án lớn thêm môi trường test liên kết với hệ thống đối tác. Nguyên tắc: các môi trường chỉ khác nhau ở biến cấu hình, quyền vào 本番 tối thiểu và có log, dữ liệu 本番 không chảy ngược xuống dev. Lịch dùng staging phải lên kế hoạch vì nhiều team, nhiều đợt test tranh nhau.

**Q349. Blue-green và canary deployment khác nhau thế nào, chọn khi nào?**
Blue-green dựng song song môi trường mới (green) giống hệt môi trường cũ (blue) rồi chuyển toàn bộ traffic một lần — rollback nhanh bằng cách chuyển lại, nhưng tốn gấp đôi hạ tầng trong lúc chuyển. Canary đẩy phiên bản mới cho một phần nhỏ người dùng (vd 5%), theo dõi chỉ số rồi tăng dần — lỗi chỉ ảnh hưởng nhóm nhỏ nhưng đòi monitoring tốt. Cả hai vướng khi thay đổi schema DB không tương thích ngược, nên tôi luôn hỏi "DB có quay lại được không" trước khi chọn.

**Q350. 本番リリース手順書 cần có những gì?**
本番リリース手順書 (honban ririisu tejunsho – tài liệu thủ tục release production) gồm: điều kiện tiên quyết và checklist trước release; từng bước có người làm, người xác nhận, lệnh cụ thể, thời gian dự kiến, kết quả mong đợi; điểm Go/No-Go; bước kiểm tra sau release (smoke test); thủ tục 切り戻し và điều kiện kích hoạt; danh sách liên lạc khẩn cấp. Khách Nhật thường review từng dòng và yêu cầu diễn tập trên staging — tôi tính effort riêng cho việc này trong kế hoạch.
> 💡 Nhắc cách làm "một người thao tác, một người đọc và tick từng bước" — chuẩn mực mà khách Nhật rất coi trọng.

**Q351. Release lỗi giữa chừng lúc nửa đêm, anh/chị quyết định rollback hay fix-forward thế nào?**
① Xác nhận fact: lỗi ở bước nào, ảnh hưởng người dùng và dữ liệu ra sao. ② Áp tiêu chí đã chốt sẵn trong 手順書: không sửa được trong khung quy định (vd 30 phút) hoặc có nguy cơ hỏng dữ liệu thì rollback, không "cố thêm chút nữa". ③ Báo khách theo 報連相 ngay khi kích hoạt rollback. ④ Sau đó RCA, sửa 手順書, diễn tập lại trước lần release sau. Fix-forward chỉ chọn khi lỗi nhỏ, rõ nguyên nhân và rollback còn rủi ro hơn.
> 💡 Mấu chốt: tiêu chí rollback được chốt TRƯỚC release, không quyết bằng cảm xúc lúc 2 giờ sáng.

**Q352. Feature flag giúp gì cho quản lý release?**
Feature flag cho phép deploy code nhưng chưa bật tính năng — tách "deploy" khỏi "release". Lợi ích: merge sớm tránh nhánh sống dài, bật dần cho từng nhóm user, tắt ngay khi lỗi mà không phải deploy lại, và vẫn giữ lịch deploy khi khách chưa duyệt xong UAT một tính năng. Cái giá: code thêm nhánh điều kiện, phải test cả hai trạng thái bật/tắt, và phải dọn flag cũ định kỳ để không thành nợ kỹ thuật.

**Q353. Đo hiệu quả DevOps của team bằng chỉ số nào?**
Tôi dùng 4 chỉ số DORA: tần suất deploy, lead time từ commit đến production, tỉ lệ thay đổi gây sự cố, thời gian khôi phục. Với dự án Nhật release theo đợt, tần suất deploy production thấp là bình thường, nên tôi đo thêm ở staging để thấy sức khỏe pipeline. Chỉ số dùng để cải tiến quy trình theo xu hướng, không dùng để so sánh hay chấm điểm cá nhân — dùng sai sẽ khiến team "làm đẹp số".

## 4.6 Testing kỹ thuật & automation

**Q354. Test pyramid là gì, tương ứng thế nào với các mức test trong dự án Nhật?**
Test pyramid: đáy là nhiều unit test (nhanh, rẻ), giữa là integration test, đỉnh là ít E2E test (chậm, dễ vỡ). Dự án Nhật thường chia 単体テスト (tantai tesuto – unit test, UT), 結合テスト (IT), 総合テスト (ST), 受入テスト (ukeire tesuto – kiểm thử nghiệm thu, UAT) — gần tương ứng các tầng nhưng nặng tài liệu và test tay. Tôi đề xuất tự động hóa phần đáy (UT, API test) để giảm effort hồi quy, giữ test tay cho nghiệp vụ và trải nghiệm ở ST/UAT.

**Q355. Vì sao test pyramid bị đảo ngược là dấu hiệu rủi ro?**
Khi phần lớn test là test tay/E2E qua giao diện còn unit test rất ít ("ice-cream cone"), mỗi đợt hồi quy tốn nhiều ngày, test chậm và vỡ mỗi khi UI đổi, lỗi lộ muộn nên sửa đắt. Dấu hiệu: mỗi release phải test tay lại toàn bộ, dev ngại refactor vì sợ デグレ. Tôi đảo dần: code mới bắt buộc có unit test, ưu tiên tự động hóa API test cho luồng chính, E2E chỉ giữ cho golden path quan trọng nhất.

**Q356. Code coverage 80% có nghĩa là chất lượng tốt không?**
Chưa chắc. Coverage chỉ cho biết bao nhiêu dòng/nhánh được chạy qua khi test, không cho biết test có kiểm tra đúng kết quả — có thể đạt 100% mà không có assertion nào. Khách Nhật hay đặt mục tiêu C0 (statement coverage) hoặc C1 (branch coverage). Tôi dùng coverage như cờ báo vùng chưa test, kết hợp review chất lượng test case, và ưu tiên coverage cao ở logic quan trọng (tính tiền, phân quyền) thay vì ép đều mọi nơi.
> 💡 Bẫy: biến coverage thành KPI của dev — sẽ sinh ra test "cho có", chạy qua code mà không kiểm gì.

**Q357. Performance test, load test, stress test khác nhau thế nào, lập kế hoạch ra sao?**
Performance test đo thời gian phản hồi, throughput ở tải mục tiêu; load test đẩy đến tải cao nhất dự kiến; stress test vượt ngưỡng để tìm điểm gãy và xem hệ thống phục hồi thế nào. Kế hoạch gồm: kịch bản theo nghiệp vụ thật (vd cao điểm cuối tháng), khối lượng dữ liệu gần production, môi trường gần giống 本番, công cụ (JMeter, k6, Gatling), tiêu chí pass theo NFR đã chốt. Tôi xếp test hiệu năng sớm, không để tuần cuối vì sửa kiến trúc rất tốn.

**Q358. Kết quả load test không đạt NFR khi chỉ còn 2 tuần đến go-live, anh/chị làm gì?**
① Xác nhận fact: điều kiện test có đúng thỏa thuận không (dữ liệu, cấu hình, kịch bản), nút cổ chai nằm ở DB, ứng dụng hay mạng. ② Khoanh vùng: tách phần sửa nhanh được (index, cache, connection pool, cấu hình) với phần phải sửa thiết kế. ③ Báo khách theo 報連相 ngay, kèm phương án: tạm nâng hạ tầng để go-live đúng hạn rồi tối ưu sau, hoặc dời ngày — khách chọn. ④ 再発防止: đưa performance test vào từ giữa dự án; 横展開 sang các dự án đang chạy.
> 💡 Luôn đưa khách ít nhất hai phương án có chi phí và rủi ro rõ ràng, đừng chỉ báo "không đạt".

**Q359. Test automation có đáng đầu tư không, tính ROI thế nào?**
ROI ≈ (effort test tay tiết kiệm qua các lần chạy − chi phí viết và bảo trì script) / chi phí đầu tư. Minh họa: hồi quy tay 10 ngày công/lần, 12 lần/năm = 120 ngày; tự động hóa tốn 30 ngày + bảo trì 1 ngày/lần = 42 ngày → tiết kiệm khoảng 78 ngày công/năm. Đáng làm khi hệ thống sống lâu, release thường xuyên, UI/API ổn định; không đáng khi dự án ngắn hoặc giao diện còn đổi liên tục. Chi phí bảo trì script thường bị đánh giá thấp.
> 💡 Đưa ra phép tính cụ thể thay vì nói "automation giúp tiết kiệm" — interviewer chấm điểm đúng chỗ này.

**Q360. Có thay đổi nhỏ trong một hệ thống lớn, phạm vi regression test xác định thế nào?**
Dựa trên 影響調査: xác định module, màn hình, batch, interface bị chạm, rồi chọn phạm vi hồi quy theo rủi ro thay vì test lại toàn bộ. Bộ test tự động cốt lõi (smoke + luồng chính) luôn chạy; vùng bị ảnh hưởng thì test sâu; vùng không liên quan test mẫu. Với khách Nhật, tôi ghi rõ phạm vi hồi quy và căn cứ chọn trong tài liệu để khách duyệt — họ cần thấy lý do, không chỉ kết quả "đã test OK".

**Q361. Test data và môi trường test hay làm trễ tiến độ thế nào, phòng ra sao?**
Hay gặp: dữ liệu test không đủ đa dạng nên sót case biên, môi trường dùng chung bị team khác ghi đè, hệ thống đối tác chưa sẵn sàng, dữ liệu phải chờ khách cung cấp. Tôi biến "chuẩn bị test data" thành task có owner trong WBS, dùng script sinh dữ liệu chạy lại được, lập lịch dùng môi trường, và theo dõi ngày khách giao dữ liệu như một dependency — trễ một ngày là báo khách kèm ảnh hưởng đến lịch test.

**Q362. Có nên giao test cho chính dev, hay cần QA độc lập?**
Cả hai, ở các tầng khác nhau. Dev chịu trách nhiệm unit test và test tích hợp phần mình làm — hiểu code nhất, sửa nhanh nhất. QA độc lập cần cho test hệ thống, nghiệp vụ, hồi quy vì người viết code có "điểm mù" với giả định của chính mình. Với tài chính, bảo hiểm, tôi nghiêng về đội QA mạnh hơn và cho QA tham gia từ lúc đọc yêu cầu, vì chi phí lỗi lọt ra production cao hơn nhiều so với chi phí test.

## 4.7 Bảo mật

**Q363. OWASP Top 10 — PM cần nắm ở mức nào?**
Đủ để biết các nhóm lỗ hổng phổ biến và đưa vào quy trình: Broken Access Control (đứng đầu bản 2021 — user xem được dữ liệu người khác), Injection như SQL injection, Cryptographic Failures, Security Misconfiguration, thành phần lỗi thời, lỗi xác thực… PM không cần tự khai thác lỗ hổng, nhưng phải đảm bảo có checklist secure coding trong review, công cụ quét (SAST, dependency scan) trong CI, và pentest trước go-live với hệ thống quan trọng.
> 💡 Cho ví dụ "đổi ID trên URL là xem được hợp đồng người khác" — interviewer hiểu ngay bạn nắm Broken Access Control.

**Q364. Đưa secure coding vào dự án thế nào để không chỉ là khẩu hiệu?**
① コーディング規約 (koodingu kiyaku – quy ước code) có mục bảo mật cụ thể: dùng prepared statement, escape output, validate input phía server, không log thông tin nhạy cảm. ② Công cụ tự động: SAST và quét thư viện có lỗ hổng trong CI, chặn merge khi có lỗi mức cao. ③ Checklist review có mục bảo mật. ④ Đào tạo ngắn đầu dự án bằng ví dụ lỗi thật. Chỉ số theo dõi: lỗi bảo mật mức cao không được mở quá 7 ngày (tham khảo).

**Q365. Quản lý secret (password, API key) trong dự án thế nào?**
Nguyên tắc: secret không bao giờ nằm trong source code, Excel, chat hay email. Dùng secret manager (AWS Secrets Manager, Parameter Store, Vault), phân quyền theo môi trường, xoay vòng định kỳ, quét secret ở pre-commit hook và CI. Nếu lỡ commit key lên Git, xóa commit là chưa đủ — phải thu hồi và cấp key mới ngay vì lịch sử có thể đã bị sao chép. Tôi đưa các mục này vào checklist onboarding và review.
> 💡 Bẫy: trả lời "xóa commit là xong" — câu đúng là "revoke key ngay, coi như đã lộ".

**Q366. Phân quyền truy cập cho team offshore vào hệ thống của khách thế nào?**
Áp dụng least privilege: mỗi người chỉ có quyền đúng việc, đúng thời hạn. Dev không có quyền thường trực vào 本番; ai cần thao tác production thì xin quyền tạm thời có phê duyệt, đi qua bastion/VPN, mọi thao tác được log. Tài khoản cá nhân, không dùng chung; thành viên rời dự án bị thu hồi quyền trong ngày. Tôi giữ bảng quản lý quyền (ai, hệ thống nào, quyền gì, đến ngày nào) và rà soát hằng tháng cùng khách.

**Q367. 個人情報保護法 (APPI) ảnh hưởng gì đến dự án offshore?**
個人情報保護法 (kojin jouhou hogo hou – luật bảo vệ thông tin cá nhân, APPI) yêu cầu doanh nghiệp quản lý an toàn dữ liệu cá nhân và giám sát bên nhận ủy thác — tức vendor offshore nằm trong phạm vi khách phải kiểm soát. Bản sửa đổi hiệu lực từ 2022 siết nghĩa vụ báo cáo rò rỉ và việc chuyển dữ liệu ra nước ngoài. Hệ quả cho PM: hạn chế dữ liệu cá nhân thật về Việt Nam, có thỏa thuận xử lý dữ liệu, log truy cập, quy trình báo rò rỉ rõ ràng.
> 💡 Không cần thuộc điều luật — nói được "vendor là bên nhận ủy thác, khách có nghĩa vụ giám sát mình" là đủ ghi điểm.

**Q368. Khách tài chính thường có yêu cầu bảo mật gì cao hơn, FISC liên quan thế nào?**
Khách tài chính Nhật thường tham chiếu 安全対策基準 (anzen taisaku kijun – chuẩn biện pháp an toàn) do FISC (Trung tâm Hệ thống Thông tin Tài chính) ban hành, cùng chính sách nội bộ và yêu cầu kiểm toán. Thực tế dự án hay gặp: checklist bảo mật dài phải trả lời từng mục, audit nơi phát triển, log truy cập lưu dài hạn, phân tách nhiệm vụ, kiểm soát chặt việc giao lại cho bên thứ ba. Tôi chuẩn bị sẵn bằng chứng (chính sách, log, chứng nhận ISMS) để không làm chậm onboarding.

**Q369. ISMS/ISO 27001 ở môi trường offshore thể hiện cụ thể thế nào?**
Thể hiện ở mặt bằng và thao tác hằng ngày: phòng dev riêng cho dự án có thẻ ra vào, camera; cấm USB, điện thoại có camera hoặc thiết bị cá nhân vào khu vực tùy mức khách yêu cầu; máy dự án khóa cổng USB, chặn upload lên dịch vụ cá nhân, khóa màn hình tự động; tài liệu in phải hủy theo quy trình. Đi kèm là cam kết bảo mật từng thành viên, đào tạo định kỳ, audit nội bộ — và khách Nhật có thể đến kiểm tra trực tiếp.

**Q370. Một thành viên lỡ đẩy source code của khách lên repo public. Anh/chị xử lý thế nào?**
① Xác nhận fact: repo nào, nội dung gì (có secret, dữ liệu cá nhân không), public từ lúc nào. ② Hành động ngay: chuyển private/xóa repo, thu hồi mọi key/password trong code, kiểm tra log truy cập nếu có. ③ Báo khách theo 報連相 trong ngày, trung thực về phạm vi — chưa đủ thông tin vẫn báo trước, cập nhật sau. ④ 再発防止: chặn tài khoản Git cá nhân trên máy dự án, quét secret, đào tạo lại; 横展開 rà tất cả dự án khác trong công ty.
> 💡 Khách Nhật có thể bỏ qua một lỗi, nhưng rất khó bỏ qua việc báo chậm hay che giấu.

**Q371. Pentest nên làm khi nào, ai làm, ảnh hưởng kế hoạch ra sao?**
Với hệ thống public hoặc dữ liệu nhạy cảm: quét tự động liên tục trong CI, và pentest bởi bên thứ ba độc lập trước go-live, sau thay đổi lớn hoặc định kỳ (vd hằng năm, tham khảo). Cần chốt sớm với khách ai thuê bên pentest, phạm vi, môi trường, thời gian. Kết quả gần như luôn có lỗi phải sửa, nên tôi chừa 1–2 tuần sửa và test lại trước go-live, không đặt pentest sát ngày release.

**Q372. Audit trail với khách tài chính cần đáp ứng những gì?**
Audit trail ghi ai, làm gì, lúc nào, trên dữ liệu nào, từ đâu, kết quả ra sao — nhất là thao tác đổi dữ liệu quan trọng, đăng nhập, cấp quyền, xuất dữ liệu. Yêu cầu thường gặp: không ai sửa/xóa được log kể cả admin, lưu theo thời hạn khách quy định, đồng bộ giờ giữa các server, tra cứu được khi kiểm toán, đồng thời mask dữ liệu cá nhân. Đây là NFR phải chốt từ 要件定義 — bổ sung sau rất tốn vì chạm hầu hết chức năng.

**Q373. Cân bằng giữa bảo mật và tốc độ phát triển thế nào?**
Siết quá thì team chậm (chờ quyền, môi trường bị khóa), lỏng quá thì rủi ro mất khách. Tôi phân mức theo độ nhạy cảm: dữ liệu cá nhân và 本番 kiểm soát chặt nhất; môi trường dev chỉ chứa dữ liệu giả lập thì nới để team làm nhanh. Tự động hóa kiểm tra (quét secret, SAST) thay cho kiểm tay để không thêm bước chờ. Yêu cầu bảo mật làm tăng effort được estimate thành dòng riêng cho khách duyệt — không để team âm thầm gánh.

## 4.8 Legacy modernization

**Q374. 2025年の崖 là gì, liên quan gì đến cơ hội của vendor offshore?**
2025年の崖 (nisen nijuugo nen no gake – "vách đá 2025") là cảnh báo trong DX Report của METI năm 2018: nếu doanh nghiệp Nhật không thay các hệ thống cũ phức tạp, phụ thuộc vài người, thì từ 2025 có thể chịu thiệt hại kinh tế rất lớn (thường được trích tới 12 nghìn tỷ yên/năm) và tụt lại trong DX. Đến nay đó vẫn là động lực của nhiều dự án modernization, migration và nhu cầu bù thiếu kỹ sư — cơ hội lớn cho vendor offshore.
> 💡 Trích đúng nguồn (DX Report của METI, 2018) cho thấy bạn hiểu bối cảnh thị trường Nhật, không chỉ kỹ thuật.

**Q375. Nhận dự án liên quan ホスト系 / COBOL, PM offshore cần lưu ý gì?**
ホスト系 (hosuto-kei – hệ thống chạy trên mainframe) thường là hệ thống lõi tài chính, bảo hiểm chạy hàng chục năm bằng COBOL, PL/I, JCL, với batch lớn và dữ liệu EBCDIC. Rủi ro chính: tài liệu thiết kế lệch so với code thật, logic nghiệp vụ ẩn trong code, người hiểu hệ thống đã nghỉ, kỹ sư COBOL tại Việt Nam rất ít. Tôi yêu cầu giai đoạn phân tích hiện trạng có effort riêng, dùng công cụ phân tích source, và có người phía khách xác nhận nghiệp vụ.

**Q376. Rehost, replatform, refactor, rebuild — chọn chiến lược modernization thế nào?**
Bốn mức: **rehost** (lift-and-shift) chuyển nguyên trạng sang hạ tầng mới — nhanh, rủi ro thấp, ít lợi ích dài hạn; **replatform** đổi nền tảng, sửa code ít (vd DB sang managed service); **refactor** tái cấu trúc code để tận dụng kiến trúc mới — tốn hơn nhưng giảm nợ kỹ thuật; **rebuild** viết lại từ đầu — linh hoạt nhất, rủi ro và chi phí cao nhất. Tôi chọn theo từng hệ thống (giá trị nghiệp vụ, tần suất thay đổi, hạn hết hỗ trợ, ngân sách) — một chương trình thường kết hợp nhiều chiến lược.

**Q377. Khách yêu cầu 現行踏襲 khi chuyển đổi hệ thống — rủi ro là gì?**
現行踏襲 (genkou toushuu – giữ nguyên hành vi hệ thống hiện tại) nghe đơn giản nhưng là bẫy: "hiện tại" thường không có tài liệu đầy đủ, nên phạm vi thật là toàn bộ hành vi ẩn của hệ thống cũ, kể cả lỗi người dùng đã quen. Tôi xử lý: ① chốt cách xác định "giống" — cùng đầu vào thì so đầu ra; ② lập danh sách khác biệt chấp nhận được để khách duyệt; ③ estimate có phần phân tích hiện trạng riêng, không coi 現行踏襲 là "không cần yêu cầu".
> 💡 Nhận "現行踏襲" mà không chốt tiêu chí so sánh là con đường ngắn nhất dẫn đến phát sinh không giới hạn.

**Q378. 並行稼働 nên tổ chức thế nào?**
並行稼働 (heikou kadou – vận hành song song) là chạy hệ thống cũ và mới cùng lúc với cùng đầu vào, so đầu ra trước khi dừng hẳn hệ thống cũ. Cần chốt: thời gian song song (vd 1–3 chu kỳ nghiệp vụ như kỳ chốt tháng, tham khảo), cách so sánh tự động, quy trình khi lệch, và hệ thống nào là "chính thức" trong giai đoạn đó. Cái giá là người dùng nhập liệu hai lần hoặc cần cơ chế đồng bộ, nên phải thống nhất nguồn lực phía khách từ sớm.

**Q379. Big-bang và chuyển dần (strangler) khác nhau ra sao?**
Big-bang cắt toàn bộ sang hệ thống mới trong một lần — quản lý dữ liệu đơn giản nhưng rủi ro dồn vào một ngày. Strangler fig thay từng phần: đặt lớp định tuyến phía trước, chuyển dần chức năng sang hệ thống mới đến khi hệ thống cũ hết vai trò — rủi ro chia nhỏ, có giá trị sớm, nhưng phải duy trì đồng bộ hai hệ thống lâu hơn. Với hệ thống lõi lớn, tôi nghiêng về chuyển dần theo nhóm nghiệp vụ, trừ khi dữ liệu dùng chung quá chặt để tách.

**Q380. Làm sao giảm rủi ro "không ai còn hiểu hệ thống cũ"?**
① Reverse engineering có hệ thống: công cụ phân tích source vẽ call graph và CRUD matrix (chương trình nào đọc/ghi bảng nào). ② Phỏng vấn người dùng, người vận hành; lấy kết quả batch thật làm "chân lý". ③ Viết lại tài liệu thiết kế từ code và nhờ khách xác nhận từng phần. ④ Dùng GenAI hỗ trợ giải thích code cũ nếu khách cho phép, luôn có người kiểm chứng. Effort phân tích này tôi tách riêng, báo giá theo giai đoạn thay vì gộp vào phát triển.

**Q381. Khách muốn rebuild toàn bộ hệ thống lõi 20 năm tuổi trong 18 tháng. Anh/chị phản hồi thế nào?**
Tôi không nói "được" ngay. ① Xin một giai đoạn assessment ngắn (vd 4–8 tuần, tham khảo) để đo quy mô thật: số chương trình, job batch, interface, bảng dữ liệu. ② Trình bày phương án: rebuild toàn bộ, chuyển dần theo nhóm nghiệp vụ, hoặc rehost trước rồi refactor dần — mỗi phương án có chi phí, thời gian, rủi ro. ③ Nêu rõ rủi ro đã biết của rebuild lớn: phạm vi ẩn, 現行踏襲, データ移行. Mục tiêu là khách chọn với đủ thông tin, không phải vendor hứa để có hợp đồng.
> 💡 "Assessment trước, cam kết sau" thể hiện tư duy chiến lược và bảo vệ cả công ty lẫn khách.

**Q382. Làm sao chứng minh hệ thống mới tương đương hệ thống cũ trước cutover?**
Bằng bằng chứng so sánh định lượng: ① bộ test so đầu ra (cùng input → so output) cho batch và báo cáo, tự động hóa để chạy lặp; ② kết quả 並行稼働 với tỉ lệ khớp và danh sách khác biệt đã được khách phân loại "chấp nhận/phải sửa"; ③ kết quả 移行リハーサル và đối soát dữ liệu; ④ hiệu năng so với hệ thống cũ. Tiêu chí Go cutover được khách ký trước, vd khớp 100% ở nghiệp vụ tiền tệ, mọi khác biệt còn lại đều đã có quyết định.

## 4.9 Code quality & nợ kỹ thuật

**Q383. Tổ chức code review trong dự án offshore thế nào để hiệu quả?**
① Mọi thay đổi qua pull request, tối thiểu một reviewer có kinh nghiệm, PR nhỏ (vd dưới 400 dòng, tham khảo) để review được kỹ. ② Checklist: đúng yêu cầu, xử lý lỗi, bảo mật, hiệu năng, có test. ③ Linter/formatter lo phần hình thức để người review tập trung vào logic. ④ Đo thời gian chờ review — PR treo quá 1 ngày là nút thắt. Một số khách muốn tham gia ソースレビュー (soosu rebyuu – review mã nguồn); tôi thống nhất phạm vi, công cụ và cách phản hồi ngay từ đầu.

**Q384. Static analysis (SonarQube) giúp PM ra quyết định thế nào?**
SonarQube phân tích tĩnh mã nguồn: bug tiềm ẩn, lỗ hổng bảo mật, code smell, trùng lặp, coverage, và ước lượng nợ kỹ thuật theo thời gian cần sửa. Với PM, đó là dữ liệu khách quan thay cảm tính: đặt Quality Gate (vd code mới không có bug/lỗ hổng mức cao, coverage code mới ≥ ngưỡng đã thỏa thuận) để chặn merge, theo dõi xu hướng qua từng sprint, và dùng số liệu khi đàm phán với khách về thời gian dọn nợ.
> 💡 Nhấn mạnh "Quality Gate áp cho code mới" — cách thực tế để không bị nhấn chìm bởi nợ cũ.

**Q385. Coding convention quan trọng thế nào, ai quyết định?**
Rất quan trọng với dự án đông người, nhiều đợt nhân sự: code đồng nhất thì review nhanh, người mới hiểu nhanh, bảo trì rẻ. Khách Nhật thường có コーディング規約 riêng và yêu cầu tuân thủ nghiêm — tôi cho team đọc kỹ từ đầu, chuyển thành cấu hình linter/formatter để máy kiểm thay người nhớ. Nếu khách không có, tech lead đề xuất dựa trên chuẩn phổ biến của ngôn ngữ và gửi khách xác nhận trước khi bắt đầu code.

**Q386. Technical debt là gì, đo bằng cách nào?**
Nợ kỹ thuật — 技術的負債 (gijutsuteki fusai) — là các "đường tắt" trong thiết kế/code giúp nhanh hôm nay nhưng khiến mỗi thay đổi sau này chậm và rủi ro hơn, như trả lãi. Đo bằng: ① chỉ số công cụ (nợ ước lượng của SonarQube, độ phức tạp, trùng lặp); ② chỉ số dự án (thời gian làm một thay đổi nhỏ tăng dần, số lần デグレ, thời gian onboard người mới); ③ danh sách nợ trong backlog có mô tả tác động. Không đo được thì không thể xin khách thời gian trả.

**Q387. Làm sao xin khách thời gian và ngân sách để trả nợ kỹ thuật?**
Nói bằng ngôn ngữ chi phí – rủi ro của khách, không bằng "code xấu". ① Dữ liệu: "mỗi thay đổi ở module tính phí mất 5 ngày thay vì 2, có 3 lần デグレ trong 6 tháng". ② Phương án: dành 10–20% capacity mỗi sprint (tham khảo), hoặc gói refactor gắn với tính năng sắp làm ở cùng module. ③ Cam kết kết quả đo được sau khi trả: thời gian thay đổi, số lỗi. Phần nợ do vendor làm ẩu thì vendor tự chịu — minh bạch điều này giúp khách tin phần còn lại.
> 💡 Tách bạch nợ "do vendor làm ẩu" (mình chịu) và nợ "do quyết định chung" (thương lượng) — rất được đánh giá cao.

**Q388. Dev muốn refactor lớn giữa dự án, anh/chị quyết định thế nào?**
Tôi hỏi bốn câu: ① vấn đề cụ thể là gì, có số đo không; ② không refactor thì rủi ro gì cho tiến độ/chất lượng trong 3 tháng tới; ③ phạm vi và effort, chia nhỏ được không; ④ test hiện có đủ bảo vệ khỏi デグレ không. Lợi ích rõ và rủi ro kiểm soát được thì đưa vào kế hoạch theo từng bước nhỏ gắn với tính năng; nếu ảnh hưởng mốc giao hàng thì phải báo và được khách đồng ý — không refactor "lén".

**Q389. Tiếp nhận dự án maintenance từ vendor khác với code chất lượng kém, 30 ngày đầu làm gì?**
① Đánh giá hiện trạng: chạy static analysis, đo coverage, đối chiếu tài liệu với code, kiểm tra build được từ source và dựng lại được môi trường không. ② Lập báo cáo rủi ro có số liệu, gửi khách sớm — để "nợ cũ" không bị tính lên đầu mình sau này. ③ Ổn định trước: dựng CI, bổ sung test cho vùng hay phải sửa nhất. ④ Đề xuất lộ trình cải thiện theo ưu tiên. Không chỉ trích vendor cũ trước mặt khách — chỉ trình bày fact.
> 💡 Báo cáo hiện trạng có số liệu trong tháng đầu là "bảo hiểm" quan trọng nhất khi tiếp quản dự án.

**Q390. Framework, thư viện, OS sắp hết hỗ trợ (EOL) — PM quản lý thế nào?**
EOL nghĩa là hết bản vá bảo mật — với khách tài chính thường là vi phạm chính sách. Tôi giữ danh sách thành phần (ngôn ngữ, framework, DB, OS, thư viện chính) kèm ngày EOL, rà mỗi quý, và đề xuất nâng cấp trước hạn ít nhất 6–12 tháng (tham khảo) vì khách cần thời gian xin ngân sách — nhiều công ty Nhật lập ngân sách theo năm tài chính bắt đầu tháng 4. Nâng cấp lớn được lập kế hoạch như dự án nhỏ: 影響調査, test hồi quy, release có rollback.

**Q391. Cân bằng "làm nhanh cho kịp deadline" và chất lượng code thế nào?**
Tôi chấp nhận nợ kỹ thuật có chủ đích, không chấp nhận nợ vô ý. Khi buộc phải đi tắt để kịp mốc: ghi rõ vào backlog đi tắt chỗ nào, rủi ro gì, khi nào trả, và báo khách nếu ảnh hưởng vận hành. Những thứ không đánh đổi: bảo mật, tính đúng của dữ liệu, test cho logic tiền tệ. Sau mốc, sprint kế tiếp phải có slot trả nợ đã hứa — nếu không, lần sau team sẽ không còn tin vào "đi tắt tạm thời".

## 4.10 Vận hành, sự cố & công cụ

**Q392. Trước go-live cần tối thiểu những gì về logging và monitoring?**
① Log tập trung, có cấu trúc, có correlation ID để trace một giao dịch qua nhiều thành phần, đã mask dữ liệu cá nhân. ② Monitoring hạ tầng (CPU, bộ nhớ, đĩa) và ứng dụng (tỉ lệ lỗi, thời gian phản hồi, độ dài queue, batch đã xong chưa). ③ Alert có ngưỡng, có người nhận và quy trình xử lý — alert không ai xem còn tệ hơn không có. ④ Dashboard chung cho team và khách. Tất cả nằm trong checklist go-live, không đợi sau sự cố mới bổ sung.

**Q393. SLA, SLO, SLI khác nhau thế nào?**
SLI là chỉ số đo thực tế (vd tỉ lệ request thành công, thời gian phản hồi p95); SLO là mục tiêu nội bộ cho SLI (vd 99.9% request thành công mỗi tháng); SLA là cam kết hợp đồng với khách, thường kèm chế tài, nên đặt lỏng hơn SLO để có vùng an toàn. Phần chênh giữa 100% và SLO là error budget: còn nhiều thì được release mạnh tay, sắp cạn thì ưu tiên ổn định. PM dùng nó để quyết định release hay hoãn bằng số.

**Q394. Thực hiện RCA kỹ thuật sau sự cố thế nào?**
① Dựng timeline chính xác từ log, alert, thao tác: lỗi bắt đầu, được phát hiện, được khôi phục lúc nào. ② Tìm nguyên nhân trực tiếp (vd deploy sai cấu hình) rồi hỏi "tại sao" nhiều lần đến nguyên nhân gốc trong quy trình (không review cấu hình, không có môi trường test tương đương). ③ Tách 暫定対応 (zantei taiou – xử lý tạm thời) và 恒久対応 (koukyuu taiou – xử lý triệt để), mỗi việc có owner và hạn. ④ Không đổ lỗi cá nhân — sửa hệ thống để người khác không lặp lại.
> 💡 Bẫy: kết luận RCA là "dev bất cẩn" — khách Nhật sẽ hỏi tiếp "vì sao quy trình để lọt".

**Q395. Hệ thống chậm bất thường sau release, anh/chị điều phối điều tra thế nào?**
① Xác nhận fact: chậm ở chức năng nào, từ lúc nào, bao nhiêu người dùng bị ảnh hưởng, có trùng thời điểm release, batch hay tải tăng không. ② Khoanh vùng: nếu trùng release và ảnh hưởng nghiệp vụ thì cân nhắc rollback theo tiêu chí đã chốt; song song dùng APM/log tìm điểm nghẽn (DB, API ngoài, bộ nhớ). ③ Báo khách theo 報連相 kèm giờ cập nhật tiếp theo (vd mỗi 30 phút). ④ Sau khi ổn: RCA, bổ sung performance test cho chức năng liên quan vào pipeline.

**Q396. Làm với khách Nhật hay gặp công cụ quản lý nào, PM dùng ra sao?**
Ticket: Jira, Redmine (rất phổ biến ở Nhật), Backlog (của Nulab, công ty Nhật); tài liệu: Confluence, nhưng Excel vẫn là "ngôn ngữ chung" cho WBS, 課題管理表 (kadai kanrihyou – bảng quản lý vấn đề), bảng Q&A; giao tiếp: Teams, Slack, Chatwork; source: Git (GitHub, GitLab, Bitbucket). Nguyên tắc: dùng công cụ khách chọn, mỗi loại thông tin chỉ có một nguồn sự thật; nội bộ dùng Jira còn khách dùng Redmine thì đồng bộ bằng API hoặc theo nhịp cố định, không để khách phải đọc hai nơi.
> 💡 Đừng chê Excel — làm tốt Excel WBS và bảng Q&A chuẩn là kỹ năng khách Nhật đánh giá cao.

**Q397. GenAI (Copilot, LLM) giúp tăng năng suất phát triển thế nào, đo ra sao?**
GenAI hỗ trợ tốt ở sinh code lặp lại, viết unit test, giải thích code cũ, tạo dữ liệu test, dịch và rà tài liệu Nhật–Việt. Tôi không dựa vào con số quảng cáo mà đo trong dự án: so lead time, số lỗi phát hiện ở review và デグレ trước và sau khi dùng qua vài sprint. Rủi ro chất lượng: code "trông đúng" nhưng sai nghiệp vụ, gợi ý thư viện không tồn tại, vấn đề license — nên review và test không giảm, effort chỉ dịch từ viết sang kiểm chứng.

**Q398. Dùng GenAI có rủi ro lộ code, dữ liệu khách thế nào, xin phép khách Nhật ra sao?**
Rủi ro: code, đặc tả, dữ liệu khách bị gửi ra dịch vụ ngoài, có thể bị lưu hoặc dùng huấn luyện — vi phạm hợp đồng bảo mật dù không cố ý. Cách làm: ① chưa có đồng ý bằng văn bản thì không dùng; ② đề xuất cụ thể: công cụ nào, gói doanh nghiệp cam kết không dùng dữ liệu để huấn luyện (kiểm điều khoản hiện hành), dữ liệu nào được nhập; ③ guideline nội bộ, chặn công cụ chưa được phép, log sử dụng; ④ thử phạm vi nhỏ, báo kết quả.
> 💡 Khách Nhật cần thời gian xin phép nội bộ — gửi đề xuất bằng văn bản sớm, đừng hỏi miệng trong họp.

**Q399. Phát hiện dev dán đặc tả của khách vào chatbot AI bằng tài khoản cá nhân. Anh/chị xử lý thế nào?**
① Xác nhận fact: nội dung gì, có dữ liệu cá nhân hay bí mật không, công cụ, loại tài khoản, thời điểm. ② Hành động ngay: dừng sử dụng, xóa lịch sử hội thoại nếu được, báo bộ phận bảo mật công ty. ③ Báo khách theo 報連相 và quy trình sự cố trong hợp đồng — dù nhỏ, che giấu mới là nghiêm trọng. ④ 再発防止: guideline GenAI rõ ràng, chặn công cụ chưa được phép, cung cấp công cụ được phép thay thế; 横展開 rà các dự án khác.

**Q400. Làm PM nhiều năm, anh/chị giữ "base kỹ thuật" bằng cách nào?**
Bằng thói quen có lịch: ① mỗi tuần đọc các PR và ADR quan trọng, hỏi tech lead điều mình chưa hiểu; ② tự làm lab nhỏ với công nghệ dự án dùng (vd dựng thử hạ tầng trên AWS); ③ học chứng chỉ có cấu trúc như AWS hoặc PMP để kiến thức không rời rạc; ④ dự buổi tech sharing của team mỗi tháng. Mục tiêu không phải code thay dev, mà đủ hiểu để đặt câu hỏi đúng và nhận ra estimate bất hợp lý.
> 💡 Nhắc việc tận dụng chính sách hỗ trợ thi Cloud/AWS/PMP của VTI cho thấy bạn đã đọc kỹ JD.
