# Chương 5 · Estimation, proposal & hợp đồng với khách Nhật (Q401–Q500)

## 5.1 Đơn vị effort & năng suất

**Q401. 人月 và 人日 là gì, quy đổi sang giờ thế nào khi làm việc với khách Nhật?**
`人月` (ningetsu – người-tháng) là effort 1 người làm 1 tháng, `人日` (ninnichi – người-ngày) là 1 người làm 1 ngày. Quy ước phổ biến (tham khảo): 1人日 = 8h, 1人月 = 20人日 = 160h; nhưng có khách tính 7.5h/ngày hoặc 1人月 = 21 ngày. Em luôn ghi quy ước quy đổi vào phần điều kiện của báo giá để lúc quyết toán hai bên không hiểu khác nhau.
> 💡 Hỏi ngay từ đầu "1人月は何時間換算でしょうか" (1 người-tháng quy đổi bao nhiêu giờ) — lệch quy đổi 5–10% là có thể mất gần hết margin.

**Q402. Vì sao "người × tháng" là ảo tưởng? Giải thích Brooks's law.**
Effort và thời gian không hoán đổi tuyến tính: thêm người thì kênh giao tiếp tăng theo n(n−1)/2, cần thời gian onboarding, và nhiều việc phụ thuộc tuần tự không chia nhỏ được. **Brooks's law** (Fred Brooks, *The Mythical Man-Month*): thêm người vào dự án đang trễ làm nó trễ thêm. Vì vậy 12人月 không có nghĩa 12 người × 1 tháng; em estimate effort trước, rồi tính lịch theo critical path và số người tối đa hợp lý cho từng 工程 (koutei – công đoạn).
> 💡 Bẫy: "khách muốn rút từ 6 tháng còn 3 tháng, nhân đôi người được không?" — trả lời bằng kênh giao tiếp và ramp-up, đừng nói "được".

**Q403. Khi khách hỏi "dự án này bao nhiêu 人月", câu trả lời của bạn gồm những thành phần nào?**
Em tách ① effort phát triển theo công đoạn, ② overhead quản lý và cầu nối: PM, QA, BrSE, comtor, ③ effort tài liệu và dịch tiếng Nhật, ④ contingency cho rủi ro đã nhận diện. Mỗi phần có `根拠` (konkyo – căn cứ) riêng, và nếu yêu cầu còn mơ hồ thì đưa range (vd 40–55人月) chứ không đưa 1 con số trơn. Kèm theo là phạm vi tính và những gì không bao gồm, để con số không bị hiểu là "trọn gói mọi thứ".

**Q404. Năng suất offshore khác onsite thế nào, đưa vào estimate ra sao?**
Offshore có chi phí đơn vị thấp hơn nhưng phát sinh overhead: truyền đạt qua BrSE, độ trễ hỏi–đáp do lệch ngôn ngữ, dịch tài liệu, review chéo. Em không nhân "năng suất thô" mà cộng riêng dòng overhead cầu nối, và dùng dữ liệu lịch sử của chính team cho loại dự án tương tự. Việc cần ngồi cùng khách như `要件定義` (youken teigi – định nghĩa yêu cầu), UAT, go-live thì để onsite; build và test để offshore — chia theo tính chất việc, không theo cảm tính.

**Q405. Đo quy mô bằng ステップ数, Function Point hay "giờ/màn hình"? Ưu nhược điểm?**
Ở Nhật, quy mô truyền thống hay đo bằng `ステップ数` (suteppu-suu – số dòng lệnh): dễ đếm sau khi có code, nhưng phụ thuộc ngôn ngữ và không đo được lúc báo giá. FP đo theo chức năng người dùng thấy, độc lập ngôn ngữ, dùng được từ giai đoạn thiết kế, nhưng cần người đếm có kỹ năng. "Giờ/màn hình", "giờ/batch" thực dụng khi team đã có dữ liệu cùng loại hệ thống. Em estimate bằng FP hoặc đơn vị chức năng, LOC chỉ dùng để đối chiếu sau dự án.

**Q406. Lịch nghỉ lễ VN và Nhật khác nhau ảnh hưởng estimate thế nào?**
Effort không đổi nhưng lịch thì đổi: VN nghỉ Tết Nguyên đán dài ngày vào khoảng tháng 1–2, Nhật nghỉ ゴールデンウィーク (Golden Week, cuối tháng 4–đầu tháng 5), お盆 (obon, giữa tháng 8) và 年末年始 (nenmatsu nenshi – nghỉ cuối năm, đầu năm). Em lập lịch chung hai nước, không đặt mốc giao hay `検収` (kenshuu – nghiệm thu) sát Tết, và tính thêm việc nhiều công ty Nhật kết thúc năm tài chính vào tháng 3 nên hay dồn release/検収 vào thời điểm này.
> 💡 Ghi lịch nghỉ hai nước ngay trong slide スケジュール của proposal — khách Nhật đánh giá cao vendor tính trước điều này.

**Q407. Thành viên mới vào dự án giữa chừng thì tính năng suất và chi phí onboarding thế nào?**
Em không dùng năng suất trung bình của người đã quen hệ thống cho người mới. Thực tế em tính hiệu suất tháng đầu thấp hơn (vd 50–70%, tham khảo) nếu domain hoặc hệ thống lạ, cộng thời gian mentor của senior (thường mất 10–20% quỹ thời gian, tham khảo) và effort đọc tài liệu tiếng Nhật. Sau 2–4 tuần em đo output thật để hiệu chỉnh kế hoạch; nếu lệch ảnh hưởng mốc thì báo khách sớm, không đợi đến hạn.

**Q408. Phân biệt effort, duration và cost trong một bản estimate?**
Effort (`工数` kousuu – công số) là lượng công sức tính bằng 人時 (ninji – người-giờ), 人日 hoặc 人月; duration là thời gian lịch từ lúc bắt đầu đến lúc xong, phụ thuộc số người, phụ thuộc giữa các task và lịch nghỉ; cost = effort × đơn giá theo vai trò + chi phí khác (license, môi trường, đi lại onsite). Một estimate tốt trình bày cả ba và nêu giả định nối chúng, ví dụ "8 người chạy song song từ giai đoạn thiết kế chi tiết".

**Q409. Vì sao estimate nên tách theo vai trò (PM, BrSE, dev, QA, comtor) thay vì gộp một đơn giá?**
Vì đơn giá từng vai trò khác nhau, và khách Nhật thường muốn thấy `体制` (taisei – cơ cấu nhân sự dự án) để đánh giá tính hợp lý. Tách vai trò giúp ① khách thấy ai làm gì, ② khi đàm phán có thể chỉnh tỷ lệ (vd giảm comtor nếu khách đọc được tiếng Anh) thay vì cắt đều mọi thứ, ③ nội bộ kiểm soát margin theo vai trò. Dự án nhỏ có thể báo blended rate, nhưng bảng tách vẫn giữ ở nội bộ.

**Q410. "The Mythical Man-Month" còn đúng với team dùng AI coding assistant không?**
Công cụ AI có thể giảm effort ở phần code và test lặp lại, nhưng không xóa chi phí giao tiếp, làm rõ yêu cầu, review và tích hợp — chính là phần Brooks nói tới. Em chỉ đưa mức giảm vào estimate khi có số đo nội bộ trên loại task tương tự (trước/sau khi dùng), và ghi nó thành giả định có thể hiệu chỉnh. Với khách tài chính/bảo hiểm, còn phải nêu rõ chính sách dùng AI, quy trình review code sinh ra và việc có được phép đưa tài liệu khách vào công cụ hay không.
> 💡 Đừng hứa "AI giảm 30–50% chi phí" khi chưa có số đo của chính team — khách sẽ đòi giảm giá ngay trong hợp đồng.

## 5.2 Phương pháp estimate

**Q411. Bạn dùng những phương pháp estimate nào và khi nào dùng cái nào?**
① Analogous khi giai đoạn sớm, chỉ có mô tả cấp cao và có dự án cũ tương tự; ② parametric (FP, use case point, đơn vị màn hình × năng suất) khi đã có danh sách chức năng; ③ WBS bottom-up khi yêu cầu đủ rõ để lập kế hoạch chi tiết; ④ 3-point/PERT cho task bất định cao; ⑤ expert judgment hoặc Wideband Delphi cho phần mới lạ. Thực tế em dùng ít nhất 2 cách độc lập; lệch nhau > 20% (tham khảo) thì tìm nguyên nhân trước khi nộp.
> 💡 Câu "em triangulate bằng 2 phương pháp độc lập rồi giải thích chênh lệch" cho thấy độ senior hơn nhiều so với kể tên phương pháp.

**Q412. Làm WBS bottom-up estimate thế nào cho đúng?**
Chia việc đến work package khoảng 8–80 giờ (quy tắc tham khảo), mỗi gói có đầu ra rõ: tài liệu, màn hình, batch, test spec. Người sẽ làm hoặc người có kinh nghiệm estimate từng gói, sau đó em cộng các việc hay bị quên: review và sửa sau review, họp, Q&A, dựng môi trường, chuẩn bị dữ liệu test, tài liệu bàn giao. Cuối cùng đối chiếu tổng với kết quả top-down — bottom-up thường thiếu vì bỏ sót các việc "keo dán" giữa các gói.

**Q413. Analogous estimate có rủi ro gì, giảm thế nào?**
Rủi ro là "giống bề ngoài, khác bản chất": cùng là hệ thống bảo hiểm nhưng khác số tích hợp, khác yêu cầu phi chức năng, khác độ chín của team. Em giảm bằng cách so theo yếu tố định lượng (số màn hình, batch, interface, bảng dữ liệu), điều chỉnh hệ số cho phần khác biệt và ghi rõ dự án tham chiếu. Analogous chỉ dùng cho `概算` (gaisan – ước tính sơ bộ), không dùng làm con số cam kết của hợp đồng `請負` (ukeoi – hợp đồng trọn gói theo kết quả).

**Q414. Function Point là gì? Các thành phần chính theo IFPUG?**
FP đo quy mô phần mềm theo chức năng người dùng nhìn thấy, không phụ thuộc ngôn ngữ lập trình. Theo IFPUG có 5 loại: data function gồm ILF (dữ liệu hệ thống tự quản lý) và EIF (dữ liệu tham chiếu từ hệ thống khác); transaction function gồm EI (nhập), EO (xuất có xử lý/tính toán), EQ (truy vấn). Mỗi loại xếp độ phức tạp thấp/trung bình/cao theo số DET, RET, FTR rồi nhân trọng số ra unadjusted FP; effort = FP × năng suất (giờ/FP) lấy từ dữ liệu lịch sử.

**Q415. Ở Nhật FP được dùng thế nào? Đếm nhanh ra sao khi chưa có thiết kế?**
Nhiều khách Nhật, nhất là khối tài chính và khu vực công, dùng FP để đánh giá quy mô và kiểm tra tính hợp lý của báo giá vendor; IPA cũng công bố dữ liệu thống kê năng suất theo FP để ngành tham khảo. Khi chưa có thiết kế, có thể đếm ước lượng kiểu NESMA (chủ yếu dựa vào số data function), sai số lớn hơn nhưng nhanh. Em dùng FP ước lượng cho báo giá sơ bộ, rồi đếm lại chi tiết sau khi có thiết kế cơ bản để ra số cam kết.
> 💡 Với khách tài chính/bảo hiểm, chủ động hỏi "御社では FP で規模を評価されていますか" (quý công ty có đánh giá quy mô bằng FP không) và chuẩn bị sẵn bảng đếm FP.

**Q416. 3-point estimate và PERT tính thế nào? Cho ví dụ.**
Lấy 3 giá trị: lạc quan O, khả dĩ nhất M, bi quan P; PERT: E = (O + 4M + P)/6, độ lệch chuẩn σ ≈ (P − O)/6. Ví dụ task tích hợp API ngân hàng: O = 5, M = 8, P = 17 ngày → E = 9 ngày, σ = 2 ngày; muốn độ tin cậy khoảng 84% thì lấy E + 1σ = 11 ngày. Giá trị lớn nhất của 3-point là lộ ra độ bất định: task nào P/O lớn là ứng viên cho POC hoặc cần ghi giả định.

**Q417. Expert judgment khác Wideband Delphi thế nào? Khi nào dùng Delphi?**
Expert judgment là 1 hoặc vài chuyên gia đưa số — nhanh nhưng dễ dính bias của người nói to nhất. Wideband Delphi: nhiều người estimate độc lập, ẩn danh, thảo luận các giả định khác nhau rồi estimate lại 2–3 vòng đến khi hội tụ. Em dùng Delphi cho phần mới lạ, rủi ro cao hoặc bid lớn; giá trị chính là lộ ra giả định ngầm khác nhau, ví dụ người A hiểu có migration dữ liệu còn người B thì không.

**Q418. Use Case Point là gì, có hợp với dự án outsourcing Nhật không?**
UCP tính quy mô từ số actor và use case theo độ phức tạp (UUCP), nhân hệ số kỹ thuật TCF và hệ số môi trường ECF; Karner gợi ý khoảng 20 giờ/UCP (tham khảo, phải hiệu chỉnh). Hợp khi yêu cầu viết dạng use case; nhưng tài liệu khách Nhật thường mô tả theo màn hình, `帳票` (chouhyou – biểu mẫu/báo cáo in), batch, interface, nên em hay quy về đơn vị đó hoặc FP thay vì UCP.

**Q419. Parametric estimate theo "đơn vị chức năng × năng suất" làm thế nào?**
Phân loại từng đơn vị theo độ khó (vd màn hình S/M/L theo số item, độ phức tạp logic, số bảng truy cập), gán effort chuẩn mỗi loại từ dữ liệu lịch sử, đếm số lượng rồi nhân. Ví dụ phần thiết kế chi tiết đến unit test: 20 màn hình M × 6人日 + 10 batch L × 8人日. Ưu điểm: nhanh, minh bạch, khách dễ kiểm và dễ tính `追加見積` (tsuika mitsumori – báo giá bổ sung) khi thêm màn hình. Điều kiện: định nghĩa S/M/L phải viết ra và thống nhất với khách.

**Q420. COCOMO II có dùng được trong thực tế không?**
COCOMO II (Boehm) tính effort = A × Size^E × các hệ số điều chỉnh; điểm hay là thể hiện tính phi tuyến: quy mô gấp đôi thì effort hơn gấp đôi do chi phí phối hợp. Nhưng hệ số mặc định phải hiệu chỉnh bằng dữ liệu nội bộ, nếu không sai số rất lớn. Em dùng nó để kiểm chéo cho dự án lớn và để giải thích với khách vì sao gộp hai hệ thống thành một dự án không thể báo giá bằng tổng hai báo giá lẻ, chứ không dùng làm số chính.

**Q421. Làm sao xây dữ liệu lịch sử để estimate ngày càng chính xác?**
Sau mỗi dự án hoặc milestone, em ghi actual effort theo đúng cấu trúc của estimate: công đoạn, đơn vị chức năng (màn hình/batch/FP), độ khó, công nghệ, domain, thành phần team, kèm % lệch và nguyên nhân. Dữ liệu chỉ có giá trị khi cùng định nghĩa đơn vị và timesheet ghi đúng mã task. Sau 3–5 dự án đã có năng suất chuẩn theo loại để làm parametric và bảo vệ estimate bằng số thật thay vì cảm tính.
> 💡 Nói được "em lưu cả % lệch và nguyên nhân" cho thấy bạn có vòng học, không estimate xong là quên.

**Q422. Yêu cầu phi chức năng estimate thế nào để không bị bỏ sót?**
`非機能要件` (hi-kinou youken – yêu cầu phi chức năng) hay bị quên vì không hiện thành màn hình. Em dùng checklist — có thể tham khảo `非機能要求グレード` (hi-kinou youkyuu gureedo – bộ phân cấp yêu cầu phi chức năng) của IPA — gồm hiệu năng, availability, bảo mật, backup, vận hành; mỗi mục ghi mức yêu cầu và việc phải làm (tuning, load test, monitoring). Mục nào khách chưa chốt thì ghi vào `前提条件` (zentei jouken – điều kiện tiền đề) với giả định cụ thể, vd "phản hồi ≤ 3 giây với 100 user đồng thời".

## 5.3 Phân bổ effort theo 工程 & overhead

**Q423. Tỷ lệ effort tham khảo giữa các 工程 trong dự án waterfall kiểu Nhật là bao nhiêu?**
Tỷ lệ em dùng để kiểm tra tính hợp lý (tham khảo, tùy dự án): 要件定義 ~10–15%, `基本設計` (kihon sekkei – thiết kế cơ bản) ~15%, `詳細設計` (shousai sekkei – thiết kế chi tiết) ~10–15%, `製造・単体テスト` (seizou/tantai tesuto – lập trình và unit test) ~25–35%, `結合テスト` (ketsugou tesuto – test tích hợp) ~15%, `総合テスト` (sougou tesuto – test hệ thống) ~10–15%. Đây là bộ lọc: nếu bottom-up ra phần test chỉ 10% tổng thì gần như chắc đang thiếu. Dự án migration, package hay AI có tỷ lệ khác hẳn.
> 💡 Luôn nói kèm "tham khảo, tùy loại dự án" — đọc tỷ lệ như chân lý là bẫy interviewer hay giăng.

**Q424. Offshore thường nhận những 工程 nào, và estimate phần ranh giới với khách ra sao?**
Mô hình phổ biến: khách hoặc onsite làm 要件定義 và 基本設計, offshore nhận 詳細設計 đến 結合テスト, còn 総合テスト và `受入テスト` (ukeire tesuto – test nghiệm thu của khách) có khi khách làm hoặc làm chung. Ranh giới là nơi estimate hay hụt: đọc hiểu 基本設計 tiếng Nhật, Q&A, sửa theo thay đổi thiết kế, hỗ trợ khách test. Em ghi rõ vendor làm từ công đoạn nào đến công đoạn nào, đầu vào bắt buộc là gì, và effort hỗ trợ công đoạn khách làm tính thành dòng riêng.

**Q425. Overhead PM, QA, BrSE, comtor thường chiếm bao nhiêu và bạn tính thế nào?**
Tham khảo, tùy quy mô: PM khoảng 10–15% effort phát triển, QA độc lập 10–20%, BrSE 10–20% với dự án nhiều tài liệu tiếng Nhật, comtor tính theo khối lượng dịch thực tế. Em không cộng % máy móc: dự án nhỏ vẫn cần tối thiểu khoảng 0.5 PM, dự án lớn thì tỷ lệ giảm dần. Em tính bottom-up từ số cuộc họp, số trang tài liệu phải dịch, số Q&A dự kiến mỗi tuần, rồi so với % tham khảo để kiểm.

**Q426. Effort cho tài liệu tiếng Nhật và dịch thuật tính thế nào?**
Em tách 3 loại: ① đọc hiểu tài liệu khách (spec, biên bản) — dịch sang tiếng Việt hoặc BrSE giải thích; ② viết deliverable bằng tiếng Nhật như `設計書` (sekkeisho – tài liệu thiết kế), `テスト仕様書` (tesuto shiyousho – đặc tả test), báo cáo; ③ dịch qua lại hằng ngày: mail, `QA表` (QA-hyou – bảng hỏi đáp), biên bản họp. Mỗi loại estimate theo số trang × năng suất của team, cộng vòng review ngôn ngữ. Dịch máy cho nháp nhanh nhưng vẫn phải tính effort hiệu đính, vì thuật ngữ tài chính/bảo hiểm dễ sai nghĩa.

**Q427. Có nên tính effort cho Q&A với khách không? Tính thế nào?**
Có, vì Q&A là khoản tiêu tốn lớn ở offshore: viết câu hỏi tiếng Nhật, chờ trả lời, xử lý những câu trả lời làm đổi thiết kế. Em estimate theo số câu hỏi dự kiến (dựa trên độ chín của spec và tỷ lệ câu hỏi/màn hình ở dự án cũ) × thời gian xử lý mỗi câu, và ghi giả định thời hạn trả lời của khách (vd ≤ 2 ngày làm việc) vào 前提条件. Khách trả lời chậm hơn thì đó là căn cứ để điều chỉnh lịch.

**Q428. Những chi phí ngoài nhân công nào hay bị quên khi estimate?**
License phần mềm và công cụ, môi trường cloud cho dev/test/staging, thiết bị test thật, đường truyền hoặc VPN riêng theo yêu cầu bảo mật của khách tài chính, chi phí onsite (vé máy bay, visa, khách sạn, phụ cấp), đánh giá bảo mật bởi bên thứ ba, dịch thuật thuê ngoài. Em có checklist chi phí ngoài nhân công và ghi rõ khoản nào vendor chịu, khoản nào là `支給` (shikyuu – khách cung cấp) để tránh tranh cãi khi chạy dự án.

**Q429. Giai đoạn bảo trì vận hành được estimate thế nào?**
`保守運用` (hoshu un'you – bảo trì vận hành) không estimate theo chức năng mà theo khối lượng dịch vụ: số ticket/tháng dự kiến, khung giờ phản hồi (giờ hành chính JST hay 24/7), SLA, số người trực tối thiểu để phủ ca. Em dùng dữ liệu sự cố quá khứ nếu khách có, đặt mức nền (vd X人月/tháng cho tối đa Y ticket) và đơn giá cho phần vượt. Phải ghi rõ bảo trì có bao gồm cải tiến nhỏ hay không, để không biến thành phát triển miễn phí.

**Q430. Effort 結合テスト và 総合テスト hay bị underestimate — làm sao estimate sát hơn?**
Em estimate test theo số test case dự kiến chứ không chỉ theo %: số case/đơn vị chức năng × thời gian thiết kế case, thực thi, lấy `エビデンス` (ebidensu – bằng chứng test, thường là screenshot từng bước), cộng 1–2 vòng retest sau khi sửa bug. Khách Nhật thường yêu cầu evidence chi tiết nên effort lấy evidence có thể rất đáng kể — phải hỏi format trước khi báo giá. Thêm effort chuẩn bị dữ liệu test và môi trường tích hợp với hệ thống ngoài.
> 💡 Hỏi sớm "エビデンスの粒度はどの程度必要でしょうか" (cần evidence chi tiết đến mức nào) — chụp từng bước hay chỉ log kết quả có thể làm effort test chênh nhau rất xa.

**Q431. Dự án có nhiều interface với hệ thống cũ của khách thì phân bổ effort khác gì?**
Tích hợp kéo effort về phía phân tích và 結合テスト: phải đọc tài liệu interface cũ (thường thiếu hoặc lỗi thời), làm stub/mock, xin lịch dùng môi trường test của hệ thống đối tác, và xử lý dữ liệu không đúng như spec. Em tăng tỷ trọng phân tích và test tích hợp, đếm interface theo độ khó (định dạng file, online hay batch, số hệ thống liên quan) và ghi 前提条件 về môi trường kết nối do khách chuẩn bị và lịch đối tác hỗ trợ.

## 5.4 Buffer, rủi ro & 前提条件

**Q432. Contingency reserve và management reserve khác nhau thế nào? Nên đặt bao nhiêu?**
Contingency reserve dành cho rủi ro đã nhận diện (known unknowns), nằm trong baseline do PM quản lý; management reserve cho rủi ro chưa biết (unknown unknowns), cấp trên giữ, không nằm trong baseline. Mức tham khảo: 10–15% khi yêu cầu tương đối rõ, 20–30% khi yêu cầu mơ hồ hoặc công nghệ mới. Nhưng em ưu tiên tính contingency từ danh sách rủi ro (xác suất × tác động) hơn là cộng một % chung cho cả dự án.

**Q433. Có nên để buffer lộ ra trong báo giá gửi khách Nhật không?**
Em không ghi dòng "buffer 15%" vì khách rất dễ yêu cầu cắt ngay. Thay vào đó, em gắn contingency vào từng hạng mục có rủi ro cụ thể (vd thêm effort cho interface chưa có tài liệu) và giải thích bằng chính rủi ro đó; rủi ro ngoài kiểm soát của vendor thì chuyển thành 前提条件. Tức là minh bạch về rủi ro, nhưng không trình bày như một khoản "dự phòng" vô danh có thể bị gạch.
> 💡 Bẫy: giấu buffer bằng cách thổi phồng đều mọi task — khách so effort/màn hình hay effort/FP sẽ thấy bất thường ngay; hãy gắn buffer vào rủi ro có tên.

**Q434. 前提条件 là gì và vì sao nó là công cụ quan trọng nhất để bảo vệ estimate?**
前提条件 là các giả định mà con số estimate dựa vào: phạm vi, đầu vào khách cung cấp, thời hạn phản hồi, môi trường, công nghệ, số vòng review, ngôn ngữ tài liệu. Khi giả định thay đổi, estimate được phép thay đổi theo — đây là căn cứ hợp đồng để đưa ra 追加見積. Estimate không có 前提条件 rõ thì mọi rủi ro mặc định thuộc về vendor, đặc biệt với hợp đồng 請負.

**Q435. Cho ví dụ các 前提条件 điển hình bạn ghi trong báo giá dự án web cho ngân hàng.**
① Phạm vi theo danh sách chức năng đính kèm (bản ngày X); ② 基本設計書 do khách cung cấp và đã chốt trước khi bắt đầu 詳細設計; ③ Q&A được trả lời trong ≤ 2 ngày làm việc; ④ môi trường test và dữ liệu test khách cung cấp trước ngày Y; ⑤ trình duyệt/thiết bị hỗ trợ theo danh sách cụ thể; ⑥ deliverable tiếng Nhật theo template khách, review tối đa 2 vòng; ⑦ không bao gồm migration dữ liệu và load test quy mô production.
> 💡 Mỗi 前提条件 phải kiểm chứng được (có ngày, số, phiên bản tài liệu) — "khách hợp tác tích cực" là giả định vô dụng.

**Q436. 対象外 nên ghi những gì?**
`対象外` (taishougai – ngoài phạm vi) liệt kê rõ những việc khách dễ mặc định là "có trong giá": migration dữ liệu, test hiệu năng/bảo mật bởi bên thứ ba, 総合テスト hoặc UAT, đào tạo người dùng, vận hành sau go-live, sửa lỗi của hệ thống hiện có, hỗ trợ ngoài giờ, mua license/hạ tầng. Em viết thành danh sách cụ thể, không chỉ "ngoài những gì ghi trên"; mục quan trọng thì thêm câu "nếu cần sẽ báo giá riêng" để mở sẵn đường cho 追加見積.

**Q437. 概算見積 và 詳細見積 khác nhau thế nào? Trình bày 概算 ra sao để khách không coi là con số cam kết?**
`概算見積` (gaisan mitsumori – báo giá sơ bộ) làm khi yêu cầu còn ở mức ý tưởng hoặc RFI, sai số lớn, khách dùng để xin ngân sách; `詳細見積` (shousai mitsumori – báo giá chi tiết) làm khi đã có 要件定義/基本設計, dùng để ký hợp đồng. Với 概算, em ghi range (vd 40–60人月), độ chính xác, căn cứ, hạn hiệu lực và câu "本見積は概算であり、要件確定後に再見積いたします" (đây là báo giá sơ bộ, sẽ báo giá lại sau khi chốt yêu cầu).
> 💡 Khách Nhật thường dùng 概算 để xin `予算` (yosan – ngân sách) nội bộ; đưa số quá thấp để "lấy lòng" sẽ tự khóa mình vào ngân sách đó.

**Q438. 多段階見積 là gì và vì sao nên đề xuất cho khách?**
`多段階見積` (tadankai mitsumori – báo giá nhiều giai đoạn) là chia dự án thành các giai đoạn, mỗi giai đoạn báo giá và ký riêng khi đã đủ thông tin, thay vì báo một giá cho toàn bộ từ lúc yêu cầu còn mơ hồ. Mẫu hợp đồng tham khảo do METI/IPA công bố cũng khuyến nghị cách tiếp cận theo giai đoạn. Lợi ích: estimate từng bước chính xác hơn, rủi ro chia công bằng hơn, khách có điểm quyết định dừng hay đi tiếp, và vendor không phải độn buffer lớn.

**Q439. Rủi ro nào nên chuyển thành điều khoản thay vì cộng buffer?**
Rủi ro nằm ngoài kiểm soát của vendor: khách chậm cung cấp đầu vào, thay đổi spec, hệ thống ngoài chưa sẵn sàng, thay đổi luật/quy định, biến động tỷ giá với hợp đồng dài. Cộng buffer cho những thứ này vừa làm giá kém cạnh tranh, vừa không đủ nếu rủi ro xảy ra lớn. Em đưa chúng vào 前提条件 kèm cơ chế `変更管理` (henkou kanri – quản lý thay đổi): khi xảy ra thì phân tích ảnh hưởng và báo giá bổ sung. Buffer chỉ dành cho rủi ro nội bộ như năng suất, kỹ thuật, nhân sự.

**Q440. Estimate ra range 80–110人月 — khi nộp giá thì chọn điểm nào?**
Tùy loại hợp đồng và mức rủi ro chấp nhận: với 請負, em đề xuất mức có xác suất hoàn thành cao (vd P80, tham khảo) vì vendor gánh phần vượt; với `準委任` (jun-inin – hợp đồng theo công sức) có thể trình bày range, lập kế hoạch theo điểm giữa và cập nhật định kỳ. Giá cuối cùng là quyết định kinh doanh của sales/BOD (khách chiến lược có thể chấp nhận margin thấp), nhưng PM phải ghi rõ xác suất và rủi ro của điểm đã chọn vào hồ sơ duyệt giá nội bộ.
> 💡 Tách bạch "estimate" (PM nói sự thật) và "price" (quyết định kinh doanh) — trộn hai thứ này là dấu hiệu thiếu độ chín.

**Q441. Hạn hiệu lực của báo giá có ý nghĩa gì với dự án Nhật?**
`有効期限` (yuukou kigen – thời hạn hiệu lực), thường 30–90 ngày (tham khảo), bảo vệ vendor khỏi việc khách ký sau nhiều tháng khi đơn giá, tỷ giá, nhân sự đã đổi. Khách Nhật có quy trình `稟議` (ringi – trình duyệt nội bộ nhiều cấp) khá dài, nên em hỏi lịch duyệt dự kiến để đặt hạn hợp lý và ghi thêm "nếu bắt đầu sau ngày X thì cần xác nhận lại nhân sự và lịch". Hết hạn thì báo giá lại hoặc xác nhận bằng văn bản là giá vẫn giữ.

**Q442. Rủi ro key person và rủi ro nhân sự phản ánh vào estimate thế nào?**
Em xác định các vị trí khó thay: BrSE giỏi tiếng Nhật và hiểu domain, tech lead công nghệ hiếm. Với các vị trí này, em tính effort chồng lấn để bàn giao (shadow) và chi phí đào tạo người dự phòng vào contingency; dự án dài thì cộng thêm giả định tỷ lệ nghỉ việc và thời gian tuyển thay thế. Đồng thời proposal phải thể hiện cơ chế backup (vị trí phó cho PM/BrSE) — đây là câu khách Nhật rất hay hỏi khi review đề xuất.

## 5.5 Bảo vệ estimate

**Q443. Sales hoặc khách yêu cầu giảm estimate 30% để kịp chào giá. Bạn làm gì?**
Em không cắt effort trên giấy mà đưa ra các phương án đổi lấy: ① giảm phạm vi (bỏ hoặc hoãn chức năng ưu tiên thấp), ② đổi điều kiện (khách tự làm 総合テスト, dùng template có sẵn, giảm số vòng review tài liệu), ③ đổi loại hợp đồng cho phần bất định sang 準委任, ④ giãn lịch để dùng team nhỏ hơn. Mỗi phương án có con số mới và rủi ro kèm theo. Nếu công ty vẫn quyết giảm giá vì chiến lược, em đề nghị ghi nhận đó là chiết khấu kinh doanh, không phải estimate sai.
> 💡 Câu chốt: "Giảm giá thì được, giảm effort thì phải giảm việc" — và lưu lại bằng văn bản ai duyệt khoản giảm.

**Q444. Cone of uncertainty là gì, bạn dùng nó để nói chuyện với khách thế nào?**
Mô hình (Boehm, được McConnell phổ biến) cho thấy sai số estimate ở giai đoạn ý tưởng rất lớn — khoảng 0.25x–4x — và thu hẹp dần khi yêu cầu, thiết kế được chốt (khoảng 0.67x–1.5x khi yêu cầu hoàn tất, theo McConnell). Em dùng nó để giải thích vì sao 概算 phải là range và vì sao nên đi 多段階見積: muốn con số chắc thì phải đầu tư làm rõ yêu cầu trước. Lưu ý: cone chỉ thu hẹp khi dự án thật sự ra quyết định, không tự thu hẹp theo thời gian.

**Q445. Dev estimate quá thấp (lạc quan) hoặc quá cao (độn) — làm sao phát hiện và xử lý?**
Phát hiện bằng cách so với dữ liệu lịch sử cùng loại, so hai người estimate độc lập, và hỏi "số này đã gồm review, unit test, sửa bug, tài liệu chưa?" — estimate thấp thường thiếu đúng các việc này. Estimate cao thì hỏi rủi ro nào khiến cao, tách rủi ro đó ra xử lý riêng (spike, POC, giả định) thay vì giữ nguyên phần độn. Em không ép dev giảm số; em làm rõ phạm vi và giả định rồi để họ estimate lại.

**Q446. Estimate, target và commitment khác nhau thế nào?**
Theo cách phân biệt của McConnell: estimate là dự đoán dựa trên dữ liệu và có xác suất; target là mong muốn kinh doanh (khách muốn go-live tháng 4); commitment là lời hứa giao một phạm vi vào một ngày với chất lượng xác định. Lỗi phổ biến là coi target như estimate. Khi khách đưa deadline cứng, em estimate độc lập trước, rồi trình bày khoảng cách và cách đóng khoảng cách (phạm vi, nguồn lực, release theo đợt) để hai bên cùng chọn commitment.

**Q447. Khách nói "vendor khác báo thấp hơn bạn 25%". Bạn phản hồi thế nào?**
Em không vội giảm mà đề nghị so trên cùng phạm vi: vendor kia có cùng 対象外, cùng 前提条件, cùng công đoạn, cùng mức test và tài liệu không — chênh lệch thường nằm ở đây. Em chuẩn bị bảng "chúng tôi đã bao gồm X, Y, Z" và rủi ro nếu bỏ những mục đó. Nếu so xong vẫn chênh thật, em đề xuất phương án tối ưu (giảm phạm vi, đổi cơ cấu nhân sự) thay vì giảm đơn phương.
> 💡 Khách Nhật tin vendor giải thích được 根拠 hơn vendor giảm giá ngay — giảm ngay khiến họ nghi estimate ban đầu bị độn.

**Q448. Dùng dữ liệu lịch sử để bảo vệ estimate thế nào cho thuyết phục?**
Em trình bày ngắn và so sánh được: "dự án tương tự cho khách bảo hiểm B (35 màn hình, 12 batch) có actual 48人月; dự án này 40 màn hình và thêm 2 interface nên estimate 52–58人月". Dữ liệu phải cùng định nghĩa đơn vị và nêu rõ các điểm khác biệt đã điều chỉnh. Nếu chưa có dữ liệu nội bộ, có thể dẫn số liệu thống kê ngành công khai (vd của IPA) làm đối chiếu, nhưng nói rõ chỉ là tham khảo.

**Q449. Bị yêu cầu estimate gấp trong 1 ngày — làm sao vẫn an toàn?**
Em trả lời bằng 概算 có range và ghi rõ độ chính xác, dùng analogous + parametric nhanh, kèm danh sách giả định và câu hỏi mở. Trong mail nộp em ghi "estimate trong 1 ngày, độ tin cậy thấp, sẽ cập nhật sau khi có thông tin A, B, C vào ngày X". Không đưa một con số tròn không kèm điều kiện, vì con số đầu tiên sẽ thành "mỏ neo" trong đầu khách suốt dự án.

**Q450. Những bias nào hay làm estimate sai và bạn chống thế nào?**
① Anchoring — bị neo bởi con số sales hoặc khách nói trước; chống bằng cách estimate trước khi nghe ngân sách. ② Planning fallacy — lạc quan, quên rủi ro; chống bằng 3-point và dữ liệu lịch sử. ③ Bias người có thâm niên — người nói to nhất quyết định; chống bằng Delphi ẩn danh. ④ Bỏ sót việc phụ (họp, review, môi trường); chống bằng checklist. Em biến các điểm này thành checklist estimate cố định cho cả team.

**Q451. Estimate của bạn bị cấp trên sửa giảm trước khi gửi khách mà không hỏi bạn. Xử lý?**
Em gặp riêng cấp trên, trình bày phần bị cắt tương ứng với việc gì và rủi ro cụ thể (vd thiếu effort 結合テスト → bug sau go-live). Đề xuất hai hướng: giữ giá đã giảm nhưng chỉnh phạm vi/前提条件 trong báo giá cho khớp, hoặc ghi nhận khoản giảm là chiết khấu và lập kế hoạch xử lý rủi ro. Quyết định cuối cùng được ghi lại bằng mail. Mục tiêu là cấp trên quyết định khi có đủ thông tin, không phải thắng tranh luận.

**Q452. Khách Nhật yêu cầu giải thích căn cứ báo giá đến từng 人日. Bạn chuẩn bị gì?**
Em chuẩn bị bảng `見積根拠` (mitsumori konkyo – căn cứ báo giá): danh sách chức năng với phân loại độ khó, effort chuẩn mỗi loại, phân bổ theo công đoạn, overhead theo vai trò, cùng 前提条件 và 対象外. Bảng viết bằng tiếng Nhật, thuật ngữ khớp tài liệu của khách. Mức chi tiết đủ để khách kiểm tra tính hợp lý nhưng không lộ cơ cấu lương nội bộ; câu nào chưa trả lời được thì ghi lại và hồi đáp bằng văn bản sau.
> 💡 Khách hỏi chi tiết là tín hiệu tốt — họ đang cần tài liệu để thuyết phục nội bộ qua 稟議; hãy giúp họ, đừng phòng thủ.

## 5.6 Proposal 提案書 & 見積書 tiếng Nhật

**Q453. Cấu trúc một 提案書 chuẩn cho khách Nhật gồm những phần nào?**
`提案書` (teiansho – hồ sơ đề xuất) em dùng khung: `背景・課題` (haikei/kadai – bối cảnh, vấn đề) → `提案概要` (teian gaiyou – tóm tắt đề xuất) → `対応範囲` (taiou han'i – phạm vi) → `実現方式` (jitsugen houshiki – cách thực hiện, kiến trúc) → `体制図` (taisei-zu – sơ đồ tổ chức) → スケジュール → `品質管理` (hinshitsu kanri – quản lý chất lượng) → 見積 và 前提条件 → `実績` (jisseki – dự án đã làm). Thứ tự đi từ vấn đề của khách đến giải pháp, không mở đầu bằng phần giới thiệu công ty dài.
> 💡 Mở bằng 背景・課題 viết đúng ngôn ngữ của khách chứng minh bạn đã hiểu họ — nhiều vendor mở bằng 10 slide giới thiệu công ty.

**Q454. Viết phần 背景・課題 thế nào cho thuyết phục?**
Em lấy nội dung từ RFP và buổi `ヒアリング` (hiaringu – buổi phỏng vấn lấy thông tin khách), diễn đạt lại theo 3 lớp: hiện trạng (hệ thống cũ, quy trình), vấn đề cụ thể có số nếu khách đã cung cấp (thời gian xử lý hồ sơ, chi phí vận hành), và mục tiêu khách muốn đạt. Dùng đúng thuật ngữ khách dùng, không suy diễn quá mức. Mỗi 課題 phải nối được tới một phần giải pháp phía sau — nếu không, hoặc 課題 đó thừa, hoặc đề xuất đang thiếu.

**Q455. Nguyên tắc "1 slide 1 message" áp dụng thế nào trong 提案書 tiếng Nhật?**
Mỗi slide có một câu thông điệp (メッセージライン – message line) ở đầu trang nói kết luận, phần thân là bằng chứng hoặc hình minh họa cho câu đó. Câu thông điệp ngắn 1–2 dòng, thống nhất văn phong, thường dùng `体言止め` (taigen-dome – kết câu bằng danh từ) cho gọn. Em kiểm tra bằng cách chỉ đọc liên tiếp các メッセージライン: nếu đọc xong đã hiểu toàn bộ đề xuất như một câu chuyện thì cấu trúc đạt.

**Q456. Lỗi ngôn ngữ nào hay gặp khi team VN làm proposal tiếng Nhật?**
① `表記ゆれ` (hyouki yure – cách viết không thống nhất) như サーバー/サーバ, ログイン/サインイン; ② dịch máy sai nghĩa thuật ngữ nghiệp vụ tài chính/bảo hiểm; ③ dùng font chữ Hán kiểu Trung Quốc thay vì font tiếng Nhật; ④ kính ngữ lẫn lộn, câu quá dài; ⑤ trộn thể です・ます và である trong cùng tài liệu. Em dùng `用語集` (yougoshuu – bảng thuật ngữ) chung, template font chuẩn, và bắt buộc người tiếng Nhật trình độ cao review trước khi gửi.
> 💡 Font chữ Hán kiểu Trung Quốc là lỗi người Nhật nhận ra ngay và bị coi là "thiếu chuyên nghiệp" — kiểm tra font trước mọi lần gửi.

**Q457. 体制図 trong proposal cần thể hiện những gì?**
Sơ đồ các bên (khách, onsite, offshore), vai trò, người chịu trách nhiệm từng phần, kênh liên lạc và mức phân bổ (vd PM 1.0, BrSE 1.0 onsite + 1.0 offshore). Khách Nhật cần thấy rõ `窓口` (madoguchi – đầu mối liên lạc), người có quyền quyết định phía vendor, đường escalation và người backup cho vị trí chủ chốt. Nếu khách yêu cầu, kèm tóm tắt kinh nghiệm của các vị trí chủ chốt (số năm, domain, trình độ tiếng Nhật).

**Q458. Phần スケジュール trong proposal nên trình bày thế nào?**
Em vẽ tổng quan theo 工程 và các mốc chính (マイルストーン – milestone): bắt đầu, chốt 基本設計, các đợt giao, 受入テスト, go-live, kèm các điểm khách phải tham gia như review, cung cấp dữ liệu, 検収. Mức chi tiết theo tuần hoặc tháng, không xuống task. Ghi rõ lịch nghỉ lễ đã tính và giả định lịch (ngày bắt đầu phụ thuộc ngày ký). Đánh dấu mốc phụ thuộc khách để sau này có căn cứ khi đầu vào bị trễ.

**Q459. Phần 品質管理 trong proposal viết gì để khách Nhật tin?**
Không viết chung chung "chúng tôi coi trọng chất lượng", mà nêu cách kiểm soát cụ thể: review cho từng loại deliverable, tiêu chí kết thúc mỗi công đoạn, chỉ số sẽ theo dõi và báo cáo định kỳ, chứng nhận liên quan nếu công ty có. Kèm mẫu báo cáo chất lượng hoặc mẫu evidence test để khách hình dung. Proposal chỉ cần cho thấy cơ chế kiểm soát; ngưỡng chi tiết sẽ nằm trong kế hoạch chất lượng sau khi ký hợp đồng.

**Q460. Trình bày 実績 thế nào khi bị ràng buộc NDA?**
Em ẩn danh khách theo dạng "大手保険会社様" (công ty bảo hiểm lớn) hoặc theo ngành và quy mô, chỉ nêu thông tin đã được phép: lĩnh vực, loại hệ thống, công nghệ, quy mô (人月, thời gian), vai trò của vendor, kết quả. Chọn 3–5 実績 gần nhất với bài toán của khách, không liệt kê tất cả. Nếu NDA cấm cả việc nêu ngành, em hỏi bộ phận pháp chế trước khi đưa vào.

**Q461. 見積書 tiếng Nhật có format thế nào?**
`見積書` (mitsumorisho – bảng báo giá chính thức) thường gồm: tên khách kèm 御中 (onchuu – kính gửi tổ chức), tiêu đề, số báo giá, ngày phát hành, 有効期限, bảng hạng mục – số lượng – đơn vị (人月) – `単価` (tanka – đơn giá) – thành tiền, tổng phụ, thuế, tổng cộng, `納期` (nouki – hạn giao), `支払条件` (shiharai jouken – điều kiện thanh toán), `備考` (bikou – ghi chú, dẫn tới 前提条件). Cách tính thuế phụ thuộc pháp nhân ký hợp đồng — hỏi kế toán/pháp chế, không tự đặt.
> 💡 Số tiền trên 見積書 và trong 提案書 phải khớp từng yên — lệch một dòng là mất uy tín ngay tại buổi review.

**Q462. Nếu PM chưa giỏi tiếng Nhật thì tổ chức làm proposal tiếng Nhật thế nào?**
Em viết khung và nội dung lõi (giải pháp, estimate, rủi ro) bằng tiếng Việt/Anh trên template slide tiếng Nhật đã chuẩn hóa, BrSE chuyển sang tiếng Nhật, sau đó người có tiếng Nhật tốt nhất (đồng nghiệp người Nhật hoặc onsite) review văn phong. Lịch làm proposal phải chừa 1–2 ngày cho vòng dịch và review. Em tự kiểm bản cuối về số liệu, tên chức năng và câu thông điệp — PM chịu trách nhiệm nội dung dù không tự dịch.

**Q463. Proposal tốt khác proposal trung bình ở điểm nào?**
Proposal trung bình nói "chúng tôi làm được"; proposal tốt chứng minh "chúng tôi hiểu vấn đề của anh và đã nghĩ trước rủi ro". Cụ thể: ① phản ánh đúng 課題 riêng của khách, ② có phương án lựa chọn (tối thiểu / khuyến nghị / mở rộng) để khách dễ quyết, ③ nêu rủi ro và cách xử lý thay vì giấu, ④ con số có căn cứ, ⑤ thân ngắn, chi tiết dồn sang phụ lục. Khách Nhật đánh giá sự cẩn thận và nhất quán cao hơn sự hào nhoáng.
> 💡 Đưa 3 phương án kiểu `松竹梅` (shou-chiku-bai – 3 mức cao/vừa/thấp) giúp người phụ trách bên khách trình 稟議 dễ hơn và tránh bị so giá trần trụi.

## 5.7 RFP/RFI, コンペ & プレゼン

**Q464. RFI và RFP khác nhau thế nào, vendor nên phản hồi ra sao?**
RFI (`情報提供依頼書` jouhou teikyou iraisho – yêu cầu cung cấp thông tin) khách dùng để tìm hiểu vendor, giải pháp và khoảng giá sơ bộ; RFP (`提案依頼書` teian iraisho – yêu cầu đề xuất) là yêu cầu chính thức có phạm vi, tiêu chí đánh giá, hạn nộp. Với RFI, em trả lời đủ để vào vòng sau, gợi ý cách tiếp cận (vd chia giai đoạn) và đưa giá dạng range. Với RFP, trả lời đúng từng mục, đúng format, đúng hạn — thiếu mục là bị trừ điểm hoặc loại.

**Q465. Đọc RFP xong, bạn phân tích gì để quyết định Go/No-Go?**
Em chấm nhanh 6 điểm: ① độ khớp năng lực (domain, công nghệ, ngôn ngữ), ② độ rõ yêu cầu so với loại hợp đồng (請負 mà spec mơ hồ là cờ đỏ), ③ ngân sách và lịch có khả thi, ④ khả năng thắng (quan hệ, số đối thủ, vendor đương nhiệm), ⑤ giá trị chiến lược (khách mới, ngành mới), ⑥ nguồn lực làm proposal. Kết quả trình sales/BOD bằng 1 trang có khuyến nghị. No-Go đúng lúc tiết kiệm hơn thắng một dự án lỗ.
> 💡 Interviewer rất thích ứng viên dám nói "có những RFP nên từ chối" và nêu được tiêu chí cụ thể.

**Q466. Giai đoạn Q&A trước khi nộp proposal nên tận dụng thế nào?**
Đây là cơ hội chính để giảm bất định và cho khách thấy mình hiểu sâu. Em gom câu hỏi theo nhóm (phạm vi, phi chức năng, môi trường, hợp đồng, lịch), viết tiếng Nhật ngắn, mỗi câu kèm giả định đề xuất: "〜と想定していますが、よろしいでしょうか" (chúng tôi giả định là…, như vậy có được không). Câu nào khách chưa trả lời kịp thì đưa giả định đó vào 前提条件. Lưu ý trả lời Q&A thường được chia sẻ cho mọi vendor, nên không hỏi câu làm lộ chiến lược của mình.
> 💡 Câu hỏi kèm giả định giúp khách trả lời nhanh "はい", và câu trả lời đó trở thành căn cứ hợp đồng.

**Q467. Trong コンペ nhiều vendor, làm sao proposal nổi bật mà không phá giá?**
`コンペ` (konpe – đấu thầu cạnh tranh) thường chấm nhiều tiêu chí, giá chỉ là một phần. Em tập trung ① hiểu 課題 sâu hơn đối thủ nhờ hearing, ② giảm rủi ro cho khách: POC, kế hoạch chuyển giao, backup nhân sự, ③ 実績 cùng ngành, ④ phương án giá linh hoạt (chia giai đoạn, nhiều mức). Nếu được, em hỏi trước `評価基準` (hyouka kijun – tiêu chí đánh giá) và phân bổ dung lượng proposal theo trọng số của từng tiêu chí.

**Q468. Chuẩn bị buổi プレゼン proposal với khách Nhật thế nào?**
`プレゼン` (purezen – buổi thuyết trình) em chuẩn bị: ① kịch bản theo đúng thời lượng khách cho, chừa ít nhất 1/3 cho Q&A; ② phân vai trước: người trình bày tiếng Nhật chính, PM trả lời phần kế hoạch và kỹ thuật; ③ tập dượt ít nhất 2 lần, có người đóng vai khách hỏi khó; ④ danh sách câu hỏi dự đoán kèm câu trả lời ngắn; ⑤ gửi tài liệu trước nếu khách yêu cầu. Đúng giờ và đúng thời lượng — vượt giờ là điểm trừ lớn.

**Q469. Trong プレゼン, khách hỏi một câu bạn chưa thể trả lời chắc (vd "giảm 20% được không?"). Bạn phản hồi thế nào?**
Em không cam kết tại chỗ. Em ghi nhận câu hỏi, nêu hướng sẽ xem xét và hẹn thời hạn: "持ち帰って検討し、◯日までにご回答いたします" (xin mang về xem xét và trả lời trước ngày ◯). Sau buổi, em cùng sales phân tích phương án (giảm phạm vi, đổi điều kiện) rồi trả lời bằng văn bản đúng hạn. Cam kết miệng trong プレゼン thường được khách ghi vào biên bản và trở thành điều kiện.
> 💡 "持ち帰って検討" rất tự nhiên với người Nhật — nhưng trễ hạn trả lời đã hẹn còn mất điểm hơn cả việc từ chối.

**Q470. Khi nào nên đề xuất POC trước khi báo giá phát triển, và POC nên miễn phí hay tính phí?**
Đề xuất POC (`概念実証` gainen jisshou – kiểm chứng khái niệm) khi có rủi ro kỹ thuật lớn chưa kiểm chứng: công nghệ mới, AI/OCR trên dữ liệu thật của khách, hiệu năng với khối lượng lớn, tích hợp hệ thống cũ khó. POC phải có mục tiêu đo được, thời hạn ngắn, tiêu chí thành công/thất bại ghi trước. Chỉ miễn phí khi phạm vi rất nhỏ và là khoản đầu tư bán hàng đã duyệt; còn lại em đề xuất POC tính phí theo 準委任 — nghiêm túc hơn và tránh "POC không hồi kết".

**Q471. Thua コンペ — bạn làm gì tiếp theo?**
Em xin khách phản hồi `失注理由` (shicchuu riyuu – lý do không trúng thầu) một cách lịch sự: giá, giải pháp, 体制 hay 実績. Sau đó tổ chức review nội bộ ngắn: estimate có cao bất thường không, proposal thiếu gì, Q&A đã hỏi đủ chưa, rồi cập nhật template và dữ liệu estimate. Em vẫn giữ liên lạc với khách, vì dự án của vendor khác có thể gặp vấn đề và khách quay lại ở giai đoạn sau hoặc dự án khác.

## 5.8 Hợp đồng kiểu Nhật

**Q472. 請負契約 và 準委任契約 khác nhau thế nào?**
請負 cam kết hoàn thành `成果物` (seikabutsu – sản phẩm bàn giao): vendor có nghĩa vụ hoàn thành theo spec, chi phí vượt do vendor gánh, thanh toán sau 検収. 準委任 cam kết thực hiện công việc với `善管注意義務` (zenkan chuui gimu – nghĩa vụ chú ý của người quản lý cẩn trọng), không bắt buộc hoàn thành kết quả, thanh toán theo công sức/thời gian. 請負 hợp với phạm vi đã rõ; 準委任 hợp với 要件定義, hỗ trợ test, bảo trì và việc bất định cao.
> 💡 Trả lời bằng "bên nào chịu rủi ro gì" (rủi ro hoàn thành, rủi ro vượt chi phí) thay vì đọc định nghĩa.

**Q473. 準委任 có hai loại 履行割合型 và 成果完成型 — khác nhau thế nào?**
Luật Dân sự Nhật sửa đổi (hiệu lực từ 1/4/2020) phân biệt rõ hai cách trả thù lao trong 準委任: `履行割合型` (rikou wariai-gata – trả theo phần công việc đã thực hiện) và `成果完成型` (seika kansei-gata – trả khi có kết quả). Ở loại thứ hai, tiền gắn với kết quả nhưng vendor vẫn không mang nghĩa vụ hoàn thành như 請負. Vì loại này dễ bị nhầm với 請負, em đọc kỹ điều khoản thanh toán và nghĩa vụ để biết chính xác mình đang gánh rủi ro nào.

**Q474. 派遣 là gì và vì sao phát triển offshore không phải là 派遣?**
`派遣` (haken – phái cử lao động) là cho khách "mượn" người, khách trực tiếp `指揮命令` (shiki meirei – chỉ huy, ra lệnh) người lao động; ở Nhật, kinh doanh phái cử phải có giấy phép theo luật phái cử lao động. Offshore development ký 請負 hoặc 準委任: vendor tự phân công, chỉ đạo và quản lý nhân sự của mình tại VN, khách chỉ giao yêu cầu và nhận kết quả qua đầu mối (PM/BrSE). Vì vậy quyền chỉ huy phải luôn nằm ở vendor — trong vận hành thực tế, không chỉ trên giấy.

**Q475. 偽装請負 là gì? Dấu hiệu nguy cơ trong dự án offshore/onsite?**
`偽装請負` (gisou ukeoi – hợp đồng ukeoi trá hình) là hợp đồng ghi 請負/準委任 nhưng thực tế khách chỉ huy trực tiếp từng nhân sự như 派遣 — vi phạm quy định lao động của Nhật. Dấu hiệu: khách giao task thẳng cho từng dev, quản lý giờ vào/ra, đánh giá cá nhân, chỉ định đổi người cụ thể, BrSE onsite làm theo lệnh trưởng nhóm của khách. Em phòng bằng cách: mọi yêu cầu đi qua 窓口 của vendor, vendor tự phân task và quản lý giờ, vai trò ghi rõ trong 体制図.
> 💡 Nêu được "quyền 指揮命令 phải nằm ở vendor" là ghi điểm phần hiểu biết pháp lý — nhiều PM kỹ thuật bỏ qua điểm này.

**Q476. ラボ型開発 là gì, phù hợp khi nào và có rủi ro gì?**
`ラボ型開発` (rabo-gata kaihatsu – mô hình lab/ODC) là khách đặt một team cố định trong thời gian dài (thường ≥ 6 tháng, tham khảo), trả theo 人月, thường ký 準委任. Hợp khi khách có lượng việc liên tục, yêu cầu thay đổi thường xuyên và muốn giữ tri thức trong team. Rủi ro: thiếu việc gây lãng phí cho khách, khách chỉ đạo trực tiếp dễ thành 偽装請負, thành viên chán nếu việc lặp lại. PM cần backlog rõ, báo cáo output định kỳ và lộ trình phát triển cho từng thành viên.

**Q477. SES là gì, khác ラボ型 thế nào?**
SES (System Engineering Service) là dạng 準委任 phổ biến ở Nhật: cung cấp kỹ sư (thường làm tại site khách) theo đơn giá 人月 kèm `精算幅` (seisan haba – khoảng giờ quyết toán, vd 140–180h/tháng, tham khảo): làm dưới mức thì trừ tiền, vượt mức thì tính thêm. ラボ型 là một team offshore do vendor quản lý và chịu trách nhiệm tổ chức; SES thường là từng kỹ sư riêng lẻ. Cả hai đều phải tránh để khách chỉ huy trực tiếp.

**Q478. 検収 là gì? Bạn quản lý rủi ro 検収 thế nào?**
検収 là bước khách kiểm tra deliverable và xác nhận chính thức bằng `検収書` (kenshuusho – biên bản nghiệm thu), thường là điều kiện xuất hóa đơn với 請負. Rủi ro: khách kéo dài, tiêu chí không rõ, đòi sửa ngoài spec rồi mới ký. Em ghi vào hợp đồng: tiêu chí 検収 cụ thể (kết quả 受入テスト theo test spec đã duyệt), thời hạn 検収 (vd 10–14 ngày làm việc, tham khảo), và điều khoản `みなし検収` (minashi kenshuu – nghiệm thu mặc nhiên) nếu khách không phản hồi trong hạn.
> 💡 Bẫy: bắt đầu giai đoạn sau khi giai đoạn trước chưa 検収 — yêu cầu sửa của khách sẽ dồn sang và không ai trả tiền cho phần đó.

**Q479. 契約不適合責任 khác 瑕疵担保責任 trước đây thế nào?**
Luật Dân sự Nhật sửa đổi (hiệu lực 1/4/2020) thay `瑕疵担保責任` (kashi tanpo sekinin – trách nhiệm bảo hành khuyết tật) bằng `契約不適合責任` (keiyaku futekigou sekinin – trách nhiệm khi không phù hợp hợp đồng). Bên đặt hàng có thể yêu cầu `追完` (tsuikan – sửa/bổ sung cho đúng), giảm giá, bồi thường, hủy hợp đồng. Với 請負, hạn thông báo 1 năm tính từ khi bên đặt hàng *biết* lỗi thay vì từ lúc giao, nên trách nhiệm có thể kéo dài — vendor cần thỏa thuận thời hạn cụ thể, vd 1 năm từ 検収.

**Q480. Khi review điều khoản 契約不適合責任 trong hợp đồng 請負, PM cần chú ý gì?**
① Thời hạn chịu trách nhiệm tính từ mốc nào (từ 検収 là rõ nhất) và kéo dài bao lâu; ② "không phù hợp" phải được đối chiếu với spec đã duyệt, không phải mong muốn mới của khách; ③ giới hạn mức bồi thường (thường đề xuất không vượt giá trị hợp đồng cá biệt, tham khảo) và loại trừ thiệt hại gián tiếp; ④ effort sửa lỗi trong thời gian bảo hành đã có trong estimate chưa. PM không thay pháp chế, nhưng phải đưa ra rủi ro vận hành để pháp chế đàm phán.

**Q481. Mô hình 基本契約 + 個別契約 hoạt động thế nào?**
`基本契約` (kihon keiyaku – hợp đồng khung) quy định điều khoản chung dài hạn: bảo mật, sở hữu trí tuệ, trách nhiệm, thanh toán, giải quyết tranh chấp. Mỗi dự án hoặc giai đoạn ký `個別契約` (kobetsu keiyaku – hợp đồng cá biệt) hoặc cặp `注文書・注文請書` (chuumonsho/chuumon ukesho – đơn đặt hàng và xác nhận nhận đặt hàng) ghi phạm vi, giá, thời hạn, loại hợp đồng. Lợi ích là không phải đàm phán lại từ đầu mỗi lần; PM cần nắm điều khoản nào của 個別契約 được ưu tiên hơn 基本契約.

**Q482. Quyền sở hữu trí tuệ trong hợp đồng phát triển với khách Nhật — PM cần lưu ý gì?**
Khách thường yêu cầu chuyển `著作権` (chosakuken – quyền tác giả) của deliverable khi 検収 hoặc thanh toán. Lưu ý: ① vendor nên giữ quyền với thư viện, framework, công cụ đã có từ trước (`汎用部分` han'you bubun – phần dùng chung) để tái sử dụng; ② kiểm license OSS và code do công cụ AI sinh ra, có danh sách OSS đính kèm; ③ điều khoản không thực thi quyền nhân thân tác giả thường có trong hợp đồng. PM đảm bảo team không mang code của khách này sang dự án khách khác.

**Q483. NDA với khách Nhật ảnh hưởng tới cách vận hành team thế nào?**
NDA (`秘密保持契約` himitsu hoji keiyaku – hợp đồng bảo mật) quy định thông tin mật, ai được tiếp cận, cách lưu giữ, hủy khi kết thúc và thời hạn bảo mật kéo dài sau hợp đồng. Khách tài chính/bảo hiểm có thể thêm: khu làm việc riêng, cấm thiết bị cá nhân, quy định xử lý dữ liệu cá nhân thật, hạn chế dùng dịch vụ dịch máy/AI công cộng với tài liệu khách. PM chuyển NDA thành quy định vận hành cụ thể, cho thành viên ký cam kết và kiểm tra định kỳ.
> 💡 Hỏi rõ trước khi dùng dịch máy/AI cho tài liệu khách — dán spec vào dịch vụ công cộng có thể là vi phạm NDA.

**Q484. Điều kiện thanh toán của 請負 và 準委任 khác nhau thế nào, PM cần quan tâm gì?**
準委任 thường thanh toán hằng tháng theo 人月 hoặc giờ thực tế trong 精算幅, căn cứ `作業報告書` (sagyou houkokusho – báo cáo công việc). 請負 thanh toán sau 検収, có thể chia đợt theo milestone (`分割検収` bunkatsu kenshuu – nghiệm thu từng phần) hoặc có tạm ứng. Ở Nhật hay gặp điều kiện "月末締め翌月末払い" (chốt cuối tháng, trả cuối tháng sau). PM phải bảo đảm mốc giao/検収 khớp kế hoạch dòng tiền của công ty và báo sớm khi mốc có nguy cơ trễ.

## 5.9 Đơn giá, đàm phán & 追加見積

**Q485. Bạn xây đơn giá 人月 như thế nào (không cần số cụ thể)?**
Đơn giá = chi phí thực của 1人月 chia cho tỷ lệ billable, cộng rủi ro và margin. Chi phí gồm lương, bảo hiểm, phúc lợi, thưởng; văn phòng, thiết bị, license; chi phí gián tiếp (HR, admin, sales); đào tạo (vd tiếng Nhật); và thời gian bench. Chia cho utilization dự kiến, cộng dự phòng tỷ giá và margin mục tiêu do công ty đặt. Đơn giá khác nhau theo vai trò và cấp bậc; BrSE, PM cao hơn dev.
> 💡 Nhắc tới "utilization" và "bench cost" cho thấy bạn hiểu kinh tế của outsourcing, không chỉ quản lý task.

**Q486. Khách đề nghị discount vì cam kết khối lượng lớn hoặc dài hạn. Bạn đánh giá thế nào?**
Discount theo volume hợp lý khi nó thật sự giảm chi phí cho vendor: ít bench, nhân sự ổn định, giảm chi phí bán hàng. Em đề xuất discount theo bậc, gắn điều kiện cụ thể (vd ≥ X人月/tháng trong ≥ 12 tháng, tham khảo) và có điều khoản xem lại nếu khối lượng thực tế thấp hơn cam kết. Tránh discount vô điều kiện đổi lấy lời hứa miệng kiểu "sau này sẽ có nhiều dự án".

**Q487. Khách ép giảm đơn giá vì đồng yên yếu. Bạn đàm phán thế nào?**
Em thừa nhận áp lực của khách nhưng không chỉ có lựa chọn giảm giá: ① đổi cơ cấu nhân sự (tăng tỷ lệ offshore, giao việc đúng cấp độ), ② tăng năng suất bằng tự động hóa, tái sử dụng và chia sẻ lợi ích với khách, ③ cam kết dài hạn đổi lấy giá tốt hơn, ④ với hợp đồng dài, thêm điều khoản điều chỉnh giá theo tỷ giá trong biên độ thỏa thuận. Mọi phương án đều được tính lại margin trước khi đưa ra và không xuống dưới margin sàn của công ty.
> 💡 Cho thấy bạn hiểu yên yếu là áp lực của cả hai bên (doanh thu quy đổi của vendor cũng giảm) — đề xuất chia sẻ rủi ro thay vì đối đầu.

**Q488. 仕様変更 phát sinh trong dự án 請負 — quy trình 追加見積 bạn làm thế nào?**
① Xác nhận đây là `仕様変更` (shiyou henkou – thay đổi đặc tả) bằng cách so với baseline tài liệu đã chốt; ② phân tích ảnh hưởng: effort, lịch, chất lượng, chức năng liên quan; ③ gửi phân tích ảnh hưởng kèm 追加見積 bằng tiếng Nhật; ④ chỉ bắt tay làm khi khách đồng ý bằng văn bản hoặc biên bản họp có xác nhận. Thay đổi nhỏ có thể gom theo đợt hoặc trừ vào quỹ thay đổi thỏa thuận trước trong hợp đồng.

**Q489. Khách nói "đây là bug, không phải 仕様変更". Làm sao phân định?**
Căn cứ là tài liệu thiết kế đã duyệt và biên bản Q&A: hành vi lệch so với tài liệu là bug, vendor sửa miễn phí; hành vi đúng tài liệu nhưng khách muốn khác là 仕様変更. Vùng xám là chỗ tài liệu không nói rõ — em xem hợp đồng quy định bên nào chịu trách nhiệm làm rõ, rồi xử lý theo hướng chia sẻ: nếu nhỏ thì sửa trước để giữ quan hệ, nhưng ghi lại. Bài học là chốt phạm vi càng rõ ở thiết kế thì càng ít tranh cãi.
> 💡 Đừng tranh cãi từng ticket nhỏ — ghi lại các phần đã làm thêm và dùng nó làm căn cứ khi đàm phán thay đổi lớn hơn.

**Q490. Khách muốn chuyển sang 準委任 "để rẻ hơn" nhưng vẫn yêu cầu vendor cam kết deadline. Bạn trả lời thế nào?**
Em nói rõ bản chất: 準委任 không có nghĩa vụ hoàn thành, nên không thể vừa trả theo công sức vừa để vendor gánh rủi ro hoàn thành như 請負. Em đề xuất: 準委任 với mục tiêu và kế hoạch rõ, báo cáo tiến độ minh bạch, cơ chế điều chỉnh phạm vi khi chậm; hoặc giữ 請負 cho phần đã rõ, 準委任 cho phần bất định. Nếu khách vẫn cần cam kết cứng, giá phải phản ánh rủi ro đó. Quan trọng nhất là văn bản hợp đồng khớp với cách vận hành thật.

**Q491. Margin dự kiến và margin thực tế của dự án — PM kiểm soát thế nào?**
Em theo dõi margin từ lúc báo giá đến khi chạy: mỗi tháng dự báo margin cuối dự án = doanh thu dự kiến − (chi phí đã phát sinh + chi phí còn lại). Đòn bẩy chính của PM: giữ đúng phạm vi (không làm miễn phí), cơ cấu nhân sự đúng cấp, giảm làm lại, đưa 追加見積 kịp thời. Khi dự báo margin xuống dưới ngưỡng cảnh báo công ty đặt, em báo cấp trên ngay kèm phương án, không đợi đến cuối dự án mới lộ.

**Q492. Báo giá trọn gói và báo giá theo đơn giá × số lượng — khi nào dùng cách nào?**
`一括請負` (ikkatsu ukeoi – trọn gói một giá) hợp khi phạm vi rõ và khách muốn chắc ngân sách; vendor có thể đạt margin tốt nếu làm hiệu quả nhưng gánh rủi ro vượt. Đơn giá × số lượng (theo 人月 hoặc theo màn hình/chức năng) hợp khi phạm vi còn thay đổi; khách dễ thêm bớt, vendor ít rủi ro hơn nhưng margin không vượt kỳ vọng. Mô hình lai hay dùng: trọn gói cho phần lõi + bảng đơn giá theo đơn vị cho phần phát sinh, ghi sẵn trong hợp đồng.

## 5.10 Tình huống senior & trade-off

**Q493. Estimate dự án migration hệ thống cũ (vd COBOL hoặc VB sang web) thế nào?**
Bắt đầu bằng `棚卸し` (tanaoroshi – kiểm kê tài sản): số chương trình, LOC, màn hình, 帳票, batch, bảng/file dữ liệu, interface, và tỷ lệ tài liệu còn đúng thực tế. Chia theo cách xử lý: chuyển bằng tool, viết lại, loại bỏ. Test thường chiếm tỷ trọng lớn vì phải `現新比較` (genshin hikaku – so sánh kết quả hệ thống cũ và mới) trên dữ liệu thật. Em đề xuất giai đoạn đánh giá hiện trạng theo 準委任 trước, vì hệ thống cũ luôn có "chức năng ẩn" không ai còn nhớ.
> 💡 Bẫy: báo giá migration chỉ theo LOC × tỷ lệ chuyển đổi — chi phí thật nằm ở test so sánh và dữ liệu.

**Q494. Estimate dự án AI (vd OCR hồ sơ, chatbot cho khách bảo hiểm) khác dự án truyền thống ở đâu?**
Kết quả phụ thuộc dữ liệu và độ chính xác không biết trước, nên không thể cam kết "độ chính xác 95%" như một chức năng 請負. Em chia: ① PoC đánh giá dữ liệu theo 準委任, có timebox; ② phần hệ thống bao quanh mô hình (màn hình, workflow, tích hợp) estimate như phần mềm thường; ③ cải thiện độ chính xác lặp lại theo 準委任. Chỉ số độ chính xác ghi là `努力目標` (doryoku mokuhyou – mục tiêu nỗ lực), không phải điều kiện 検収; estimate cả chi phí API/hạ tầng và đánh giá định kỳ.
> 💡 Câu chốt: "phần phần mềm có thể 請負, độ chính xác của mô hình thì không".

**Q495. Khách muốn báo giá 請負 nhưng chưa có spec, chỉ có vài trang ý tưởng. Bạn xử lý thế nào?**
Em không từ chối thẳng mà đưa hai lựa chọn: ① làm 要件定義 trước theo 準委任 (vài tuần, phí rõ), sau đó báo giá 請負 chính xác; ② nếu khách cần con số ngay, đưa 概算 range kèm 前提条件 rất chi tiết và danh sách chức năng do vendor định nghĩa làm baseline, ghi điều kiện "báo giá lại sau 要件定義 nếu phạm vi thay đổi quá X%". Tuyệt đối không ký 請負 trọn gói chỉ dựa trên ý tưởng khi danh sách chức năng chưa được khách xác nhận.

**Q496. Dự án đang chạy 準委任 ổn, khách muốn chuyển giai đoạn tiếp sang 請負. Bạn đánh giá gì trước khi đồng ý?**
Em kiểm tra: ① spec giai đoạn tới đã ổn định chưa (tỷ lệ thay đổi gần đây), ② đã có năng suất thực đo được trên chính hệ thống này chưa, ③ trách nhiệm phía khách (review, quyết định, môi trường) đã rõ chưa, ④ ranh giới bảo hành với phần code làm theo 準委任 trước đó. Đủ điều kiện thì estimate từ năng suất thực + contingency cho phần rủi ro chuyển sang vendor, đồng thời đổi cách vận hành: baseline phạm vi, change control chặt hơn.
> 💡 Bẫy: đã ký 請負 mà vẫn làm việc "kiểu 準委任" (khách đổi gì làm nấy) — đó là con đường ngắn nhất tới dự án lỗ.

**Q497. Dự án 請負 đang lỗ vì chính bạn estimate sai (không phải do khách thay đổi). Bạn xử lý thế nào?**
① Xác nhận fact: lỗ bao nhiêu, sai ở hạng mục nào, dự báo chi phí đến hết; ② báo cấp trên ngay theo `報連相` (hou-ren-sou – báo cáo, liên lạc, bàn bạc), không giấu; ③ khoanh vùng: tối ưu nguồn lực, ưu tiên mốc quan trọng, rà lại phần nào thật ra là 仕様変更 chưa được 追加見積; ④ không giảm chất lượng cam kết với khách vì lỗi estimate thuộc về vendor; sau dự án làm `再発防止` (saihatsu boushi – phòng ngừa tái diễn) cho quy trình estimate và `横展開` (yokotenkai – nhân rộng bài học) sang team khác.
> 💡 Interviewer muốn nghe: bạn nhận trách nhiệm, không đổ cho khách, và sửa quy trình estimate chứ không chỉ "tăng ca bù".

**Q498. Sales đã báo giá cho khách trước khi PM estimate, con số thấp hơn nhiều so với effort thật. Bạn làm gì?**
Em estimate độc lập, trình bày khoảng chênh cho sales và cấp trên kèm rủi ro cụ thể, rồi cùng tìm cách chỉnh trước khi ký: thu hẹp phạm vi trong báo giá cho khớp số, bổ sung 前提条件 và 対象外, đề xuất chia giai đoạn. Nếu hợp đồng đã ký, tập trung kiểm soát phạm vi thật chặt và chuẩn bị 追加見積 cho mọi thay đổi. Sau đó em đề xuất quy tắc: không phát hành báo giá chính thức khi chưa có PM hoặc tech lead review estimate.

**Q499. Chi nhánh/team mới ở Đà Nẵng nhận dự án đầu tiên — estimate có rủi ro gì và bạn làm thế nào?**
Rủi ro: chưa có dữ liệu năng suất của chính team, thiếu người nắm domain và tiếng Nhật, quy trình chưa ổn định. Em ① dùng dữ liệu của team đã chín ở nơi khác nhưng áp hệ số ramp-up, ② đặt senior/BrSE có kinh nghiệm làm nòng cốt giai đoạn đầu, ③ ưu tiên dự án đầu có phạm vi vừa phải, ký 準委任 hoặc chạy pilot, ④ đo năng suất thực sau 1–2 tháng để hiệu chỉnh các estimate sau. Chi phí ramp-up ghi rõ là đầu tư nội bộ hay tính vào giá.
> 💡 Với vị trí có lợi thế "build-up chi nhánh Đà Nẵng", nêu được cách biến dự án đầu thành nguồn dữ liệu estimate cho cả chi nhánh sẽ rất ghi điểm.

**Q500. Nếu chỉ chọn một nguyên tắc quan trọng nhất về estimate và hợp đồng với khách Nhật, bạn chọn gì?**
Em chọn: "mọi con số phải đi kèm căn cứ và điều kiện". Estimate không có 前提条件 thì rủi ro mặc định về vendor; hợp đồng không khớp vận hành thực tế (請負 mà làm như 準委任, 準委任 mà khách chỉ huy như 派遣) thì sớm muộn thành tranh chấp. Với khách Nhật, căn cứ minh bạch còn giúp họ duyệt nội bộ nhanh hơn — nên đây vừa là cách vendor tự bảo vệ, vừa là cách phục vụ khách.
> 💡 Câu tổng kết nên nối được ba mảng: estimate có căn cứ – proposal rõ ràng – hợp đồng khớp cách vận hành.
