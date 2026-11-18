# Chương 6 · Quản lý chất lượng & quy trình kiểu Nhật (Q501–Q600)

## 6.1 Tư duy chất lượng của khách Nhật

**Q501. Với khách Nhật, 品質 (hinshitsu – chất lượng) có nghĩa gì rộng hơn "phần mềm ít bug"?**
Với khách Nhật, chất lượng gắn với **niềm tin (信頼 – shinrai)**: sản phẩm chạy đúng, tài liệu khớp code, mọi thay đổi có lý do, và khi có lỗi thì giải thích được vì sao xảy ra, đã chặn tái phát thế nào. Một bug nhỏ kèm báo cáo rõ ràng vẫn giữ được niềm tin; một bug nhỏ bị giấu hoặc giải thích mơ hồ có thể làm mất hợp đồng tiếp theo. Vì vậy PM quản lý đồng thời **chất lượng sản phẩm**, **chất lượng quy trình** và **chất lượng giải trình**.
> 💡 Trả lời bằng ba lớp "sản phẩm – quy trình – giải trình" cho interviewer thấy bạn hiểu khách Nhật chứ không chỉ thuộc định nghĩa.

**Q502. Vì sao khách Nhật kỳ vọng gần "zero defect", và PM nên hiểu kỳ vọng đó thế nào cho thực tế?**
"Zero defect" thực chất là **không để lỗi lọt sang phía khách** (流出 – ryuushutsu – lỗi lọt ra ngoài), không phải dự án không có bug. Bug tìm và sửa trong nội bộ là bằng chứng quy trình hoạt động; bug khách tìm thấy ở 受入テスト (ukeire tesuto – kiểm thử nghiệm thu) hay production mới bị coi là thất bại. PM cần thỏa thuận từ đầu mục tiêu bug lọt theo mức độ, ví dụ 0 lỗi nghiêm trọng, lỗi nhẹ dưới ngưỡng đã thống nhất (tham khảo), và cách đo.
> 💡 Đừng hứa "zero bug" tuyệt đối; nói "zero bug nghiêm trọng lọt ra" kèm cơ chế đo vừa đúng tinh thần vừa khả thi.

**Q503. 品質計画書 (hinshitsu keikakusho – kế hoạch chất lượng) của một dự án offshore gồm những nội dung chính nào?**
Gồm: ① mục tiêu chất lượng định lượng (mật độ review, mật độ test, mật độ bug, số bug lọt ra khách); ② quality gate cho từng 工程 (koutei – công đoạn) với tiêu chí vào/ra; ③ loại review và người review cho từng 成果物 (seikabutsu – sản phẩm bàn giao); ④ chiến lược test và mức evidence; ⑤ quy trình quản lý bug, thay đổi, cấu hình; ⑥ báo cáo chất lượng gửi khách và tần suất. Kế hoạch được khách duyệt trước khi vào thiết kế, làm "luật chơi" chung cho hai bên.

**Q504. Quality gate theo 工程 vận hành thế nào trong một dự án waterfall cho khách Nhật?**
Cuối mỗi công đoạn (yêu cầu, thiết kế, lập trình, từng mức test) có một buổi 工程完了判定 (koutei kanryou hantei – đánh giá hoàn thành công đoạn): deliverable đủ, review xong, chỉ số trong ngưỡng, các 指摘 (shiteki – điểm bị chỉ ra) đã đóng. Không đạt thì không sang công đoạn sau, hoặc sang có điều kiện kèm danh sách tồn đọng và hạn đóng. PM chủ trì, có người QA độc lập tham gia, biên bản gửi khách khi hợp đồng yêu cầu.

**Q505. 手戻り (temodori – làm lại) được đo thế nào để trở thành một chỉ số chất lượng nội bộ?**
Em đo **tỉ lệ effort 手戻り** = giờ công sửa lại sản phẩm của công đoạn trước / tổng giờ công, ghi bằng mã task riêng trong timesheet hoặc ticket. Tách theo công đoạn gây ra và nguyên nhân (hiểu sai spec, lỗi thiết kế, khách đổi yêu cầu) để biết chi phí đang "rò" ở đâu. Tỉ lệ này tăng ở một module là cảnh báo sớm hơn cả mật độ bug, và cũng là dữ liệu khi đàm phán phần 手戻り do khách đổi yêu cầu.
> 💡 Tách được "手戻り do mình" và "手戻り do khách đổi yêu cầu" cho thấy bạn vừa quản chất lượng vừa giữ được chi phí.

**Q506. Câu "品質は工程で作り込む" (hinshitsu wa koutei de tsukurikomu – chất lượng được tạo ra trong từng công đoạn) áp dụng vào phần mềm thế nào?**
Nghĩa là chất lượng không đến từ việc test thật nhiều ở cuối, mà được "xây" ở từng bước: yêu cầu rõ, thiết kế được review, code theo chuẩn có self-check, unit test đủ quan điểm. Cụ thể em gắn mỗi công đoạn với checklist, review bắt buộc và tiêu chí ra; test cuối để xác nhận chứ không phải để "vớt" lỗi. Khi test hệ thống phát hiện nhiều lỗi thiết kế, đó là tín hiệu quy trình thượng nguồn hỏng, phải sửa quy trình chứ không chỉ sửa bug.

**Q507. Khách Nhật khác khách Âu/Mỹ thế nào trong cách nhìn chất lượng, và PM điều chỉnh ra sao?**
Khái quát (không phải khách nào cũng vậy): khách Nhật thường coi trọng **hoàn chỉnh trước khi giao**, tài liệu chi tiết, quy trình giải trình được; khách Âu/Mỹ thường chấp nhận giao sớm rồi sửa nhanh qua nhiều vòng, ưu tiên tốc độ và giá trị kinh doanh. Với khách Nhật, em tăng review nội bộ, evidence và báo cáo định kỳ; với khách Âu/Mỹ, em tập trung demo, test tự động và thời gian phản hồi lỗi. Quan trọng nhất là hỏi rõ tiêu chí nghiệm thu của từng khách thay vì áp khuôn.
> 💡 Luôn thêm ý "tùy từng khách" để không bị đánh giá là định kiến văn hóa.

**Q508. 安心感 (anshinkan – cảm giác an tâm) của khách liên quan gì đến quản lý chất lượng?**
Khách Nhật đánh giá vendor không chỉ qua sản phẩm mà qua việc họ có **an tâm** khi giao việc không: biết trước rủi ro, nhận báo cáo đúng hạn, không bị bất ngờ. PM tạo an tâm bằng chỉ số chất lượng minh bạch hằng tuần, báo tin xấu sớm (ví dụ mật độ bug vượt ngưỡng là báo ngay kèm phân tích), và giữ đúng cả những lời hứa nhỏ. Vendor ít lỗi nhưng hay im lặng thường bị đánh giá thấp hơn vendor có lỗi nhưng chủ động minh bạch.

**Q509. QCD (Quality – Cost – Delivery) là gì và chữ Q thường đứng ở đâu trong ưu tiên của khách Nhật?**
QCD là ba trục khách Nhật dùng để đánh giá vendor. Ở nhiều dự án tài chính, bảo hiểm, Q thường được đặt ngang hoặc trên D: trễ vài ngày còn đàm phán được, nhưng lỗi lọt ra production làm khách mất uy tín với khách hàng cuối thì rất khó cứu. Tuy vậy PM không mặc định "Q luôn thắng"; em hỏi khách thứ tự ưu tiên cho từng giai đoạn, ghi vào kế hoạch, và khi phải đánh đổi thì trình phương án có số liệu để khách quyết.

**Q510. Khi mới nhận một dự án đang chạy, làm sao đánh giá nhanh "sức khỏe chất lượng" trong một tuần?**
Em xem năm thứ: ① 品質計画書 có tồn tại và còn được theo dõi không; ② xu hướng 指摘 review và bug theo tuần so với mục tiêu; ③ số bug mở, tuổi bug, tỉ lệ reopen; ④ các bug khách phát hiện gần đây và báo cáo nguyên nhân; ⑤ trao đổi ngắn với BrSE (Bridge SE – kỹ sư cầu nối), tester, onsite về điều khách phàn nàn. Kết quả gom thành một trang đỏ–vàng–xanh kèm 3 hành động ưu tiên để báo cấp trên và onsite.
> 💡 Luôn hỏi "khách đã phàn nàn gì trong 3 tháng qua" — đó là chỉ số chất lượng thật nhất và không nằm trong dashboard.

## 6.2 成果物 theo V-model & quản lý tài liệu

**Q511. Liệt kê các 成果物 chính theo công đoạn V-model và ai thường tạo, ai duyệt trong mô hình offshore.**
Yêu cầu: 要件定義書 (youken teigisho – tài liệu định nghĩa yêu cầu), khách hoặc onsite tạo. Thiết kế: 基本設計書 (kihon sekkeisho – thiết kế cơ bản) thường onsite/BrSE tạo, khách duyệt; 詳細設計書 (shousai sekkeisho – thiết kế chi tiết) team offshore tạo, leader/BrSE duyệt. Lập trình: ソースコード kèm kết quả review code. Mỗi mức test: テスト仕様書 (tesuto shiyousho – test spec) và テスト結果報告書 (tesuto kekka houkokusho – báo cáo kết quả test) kèm evidence. Bàn giao: 運用手順書 (unyou tejunsho – hướng dẫn vận hành), release note. Phân vai cụ thể ghi trong 品質計画書.

**Q512. 基本設計書 và 詳細設計書 khác nhau thế nào về người đọc và mức chi tiết?**
基本設計書 (còn gọi 外部設計 – gaibu sekkei – thiết kế ngoài) mô tả hệ thống nhìn từ phía người dùng: màn hình, item, chức năng, báo cáo, interface ngoài, data model logic; khách đọc và duyệt. 詳細設計書 (内部設計 – naibu sekkei – thiết kế trong) mô tả bên trong: module, class, xử lý từng bước, SQL, xử lý lỗi; chủ yếu cho dev, đủ chi tiết để người khác code ra cùng kết quả. Ở offshore, phần chi tiết thường do team Việt Nam viết và được review chéo trước khi code.

**Q513. Khách Nhật mong đợi tài liệu chi tiết đến mức nào, và làm sao biết đã "đủ"?**
Thường rất cao: 詳細設計書 có thể mô tả đến từng item màn hình, điều kiện validate, message ID, nhánh xử lý. Cách biết "đủ": ① lấy tài liệu khách đã chấp nhận ở dự án trước làm chuẩn; ② làm mẫu cho 1 chức năng đầu, gửi khách review sớm để chốt mức chi tiết; ③ dùng tiêu chí "người khác đọc có code và test được mà không phải hỏi". Sau khi chốt, đưa mẫu vào template và checklist cho cả team.
> 💡 "Làm mẫu 1 chức năng cho khách duyệt trước khi nhân rộng" là điểm cộng lớn vì nó chặn 手戻り hàng loạt.

**Q514. テスト仕様書 chuẩn kiểu Nhật cần có những cột thông tin nào?**
Thường gồm: ID case, chức năng/màn hình, テスト観点 (tesuto kanten – quan điểm test), điều kiện tiền đề, dữ liệu test, thao tác, kết quả mong đợi, kết quả thực tế, ngày test, người test, người xác nhận, link evidence, ID bug nếu fail. Phần đầu file có phạm vi, môi trường, danh sách quan điểm và thống kê số case. Kết quả mong đợi phải cụ thể đến giá trị hoặc message, không viết chung chung.
> 💡 Kết quả mong đợi kiểu "正常に表示される" (seijou ni hyouji sareru – hiển thị bình thường) là lỗi bị khách Nhật chỉ ra nhiều nhất.

**Q515. テスト仕様書 và テスト結果報告書 khác nhau ở điểm nào?**
テスト仕様書 trả lời "sẽ test gì, thế nào, kỳ vọng gì" và được review **trước** khi test. テスト結果報告書 trả lời "đã test được gì, kết quả ra sao, đủ để sang bước sau chưa" và được viết **sau** mỗi mức test: số case đạt/không đạt, bug phát hiện, phần chưa test được và lý do, kèm kết luận của người phụ trách test. Báo cáo kết quả là đầu vào cho quyết định chuyển công đoạn và cho báo cáo chất lượng gửi khách.

**Q516. 運用手順書 cần được chuẩn bị và kiểm tra thế nào trước bàn giao?**
運用手順書 mô tả cách khởi động/dừng hệ thống, chạy batch, backup/restore, xử lý khi lỗi, đầu mối liên hệ khi sự cố, kèm lệnh và màn hình cụ thể. Em yêu cầu viết sớm, song song với test hệ thống, và **chạy thử đúng theo tài liệu** bởi người không viết ra nó, có evidence từng bước. Lỗi tài liệu vận hành thường chỉ lộ ra khi đã đi vào vận hành, nên đây là deliverable hay bị xem nhẹ nhưng rủi ro cao.

**Q517. Quản lý version tài liệu cho khách Nhật thế nào cho đúng chuẩn?**
Mỗi tài liệu có bìa ghi số phiên bản, ngày, người tạo, người duyệt và bảng 改訂履歴 (kaitei rireki – lịch sử sửa đổi) gồm version, ngày, nội dung sửa, vị trí sửa, người sửa. Phần thay đổi được đánh dấu (chữ đỏ hoặc gạch chân) để người review chỉ cần xem phần khác biệt. File lưu trên repo hoặc kho tài liệu chung với quy tắc đặt tên thống nhất, chỉ một bản chính thức, bản cũ được lưu trữ chứ không ghi đè.
> 💡 Khách để ý 改訂履歴 trống hoặc chỉ ghi "修正" (shuusei – sửa); ghi rõ "sửa mục 3.2 theo Q&A số 15" tạo ấn tượng chuyên nghiệp.

**Q518. Tài liệu thiết kế dạng Excel 方眼紙 (hougan-shi – Excel kẻ ô vuông) có ưu nhược điểm gì và PM xử lý ra sao?**
Ưu: khách Nhật quen dùng, dễ trình bày layout màn hình, dễ in và đóng dấu. Nhược: khó so sánh phiên bản, khó merge khi nhiều người sửa, khó tìm kiếm, dễ lệch giữa các sheet. Em xử lý bằng cách phân owner theo file, khóa sheet template, dùng công cụ so sánh Excel trước mỗi lần gửi và ghi đủ 改訂履歴. Nếu khách cởi mở, có thể dùng wiki/Markdown cho tài liệu nội bộ, còn deliverable chính thức vẫn giữ đúng định dạng khách yêu cầu.

**Q519. Làm sao giữ tài liệu và code luôn nhất quán, nhất là khi có thay đổi giữa chừng?**
Em áp quy tắc **"tài liệu trước, code sau"**: mọi thay đổi phải cập nhật thiết kế và 改訂履歴 rồi mới sửa code, trong cùng một ticket. Có ma trận truy vết yêu cầu ↔ thiết kế ↔ code ↔ test case, checklist review code có mục "đã khớp thiết kế chưa", và trước mỗi lần bàn giao lấy mẫu đối chiếu tài liệu với code. Lệch tài liệu–code được ghi nhận như một bug, có phân loại, để team không coi nhẹ.

**Q520. Luồng 作成 → 確認 → 承認 (sakusei – kakunin – shounin: tạo, kiểm tra, phê duyệt) trên tài liệu có ý nghĩa gì với PM?**
Đó là chuỗi trách nhiệm: người tạo chịu trách nhiệm nội dung, người kiểm tra (thường leader/BrSE) xác nhận đã review theo checklist, người phê duyệt (PM hoặc khách) chịu trách nhiệm cho phép phát hành. Ô ký duyệt không phải hình thức: khi có lỗi, khách sẽ hỏi "ai đã 確認, theo tiêu chí nào". Vì vậy PM chỉ 承認 khi có レビュー記録票 (rebyuu kirokuhyou – biên bản review) đi kèm.
> 💡 Không bao giờ ký duyệt "cho kịp" khi chưa có biên bản review — đó là bẫy trách nhiệm kinh điển.

## 6.3 Review & 指摘

**Q521. Các loại review thường gặp trong dự án cho khách Nhật là gì, mỗi loại dùng khi nào?**
① セルフレビュー (self review) theo checklist trước khi giao; ② ピアレビュー (peer review) giữa đồng nghiệp cùng cấp, bắt lỗi logic và vi phạm chuẩn; ③ review của 有識者 (yuushikisha – người có chuyên môn) cho phần khó hoặc rủi ro cao; ④ 顧客レビュー (kokyaku rebyuu – review của khách) cho deliverable chính thức. Về hình thức có ウォークスルー (walkthrough – tác giả dẫn dắt giải thích) và インスペクション (inspection – review chính thức có vai trò, checklist, số đo). Nguyên tắc: lỗi phải bị bắt ở tầng thấp nhất trước khi đến tay khách.

**Q522. 設計レビュー (sekkei rebyuu – review thiết kế) nên tập trung vào những điểm nào?**
Tập trung vào: ① đúng và đủ so với yêu cầu, truy vết được; ② nhất quán giữa các màn hình/module, với data model và interface; ③ xử lý ngoại lệ, lỗi, giá trị biên; ④ yêu cầu phi chức năng như hiệu năng, bảo mật, log; ⑤ khả năng test được. Lỗi chính tả, format là phụ, nên để self-check xử lý trước. Mỗi buổi review giới hạn phạm vi (ví dụ khoảng 30–40 trang – tham khảo) để giữ độ sâu.

**Q523. コードレビュー (koodo rebyuu – review code) trong dự án offshore cho khách Nhật nên tổ chức thế nào?**
Ba tầng: công cụ tự động (lint, static analysis, coding convention) chặn lỗi hình thức trước; peer review qua pull request theo checklist (logic, xử lý lỗi, bảo mật, hiệu năng, khớp thiết kế); leader review phần rủi ro cao. Mỗi 指摘 được ghi lại có phân loại chứ không chỉ comment rồi quên, để cuối giai đoạn tính được mật độ và xu hướng. Pull request quá lớn (ví dụ trên 400 dòng – tham khảo) bị yêu cầu tách để review có chất lượng.

**Q524. レビュー記録票 cần ghi những gì?**
Gồm: tên tài liệu/module và version, ngày, thời lượng review, người tham gia, phạm vi (số trang hoặc LOC), danh sách 指摘 (vị trí, nội dung, phân loại, mức độ, người sửa, ngày sửa, người xác nhận đã sửa) và kết luận (đạt hoặc review lại). Từ đó tính được 指摘密度 (shiteki mitsudo – mật độ chỉ ra) và レビュー工数密度 (rebyuu kousuu mitsudo – giờ review trên quy mô). Biên bản này là evidence chất lượng thượng nguồn khi khách audit hoặc khi phân tích lỗi về sau.

**Q525. 指摘 thường được phân loại thế nào và vì sao phải phân loại?**
Theo nội dung: 誤り (ayamari – sai), 漏れ (more – thiếu), 曖昧 (aimai – mơ hồ), 不整合 (fuseigou – không nhất quán), 表記 (hyouki – cách viết, chính tả), 改善提案 (kaizen teian – đề xuất cải tiến); theo mức độ: lớn, vừa, nhỏ. Phân loại để biết **lỗi bản chất nằm ở đâu**: nhiều 漏れ → hiểu yêu cầu chưa đủ; nhiều 不整合 → thiếu thiết kế chung; toàn 表記 → review chưa đủ sâu. Không phân loại thì chỉ có con số đếm, không rút ra hành động.
> 💡 Khi kể "review ra 200 指摘", hãy nói ngay tỉ lệ 指摘 bản chất (logic, thiếu sót) — interviewer đánh giá cao tư duy phân tích đó.

**Q526. 指摘密度 được tính thế nào và dùng để làm gì?**
指摘密度 = số 指摘 / quy mô được review, ví dụ 指摘 trên mỗi trang thiết kế hoặc trên mỗi KLOC code. Khi so với baseline của tổ chức hoặc dự án tương tự, nó cho biết review đã "đào" đủ sâu chưa và tài liệu có ổn không. Phải đọc kèm レビュー工数密度: mật độ chỉ ra thấp và giờ review cũng thấp thì nghi review hời hợt; giờ review đủ mà mật độ thấp thì nhiều khả năng tài liệu tốt.

**Q527. Ngưỡng tham khảo cho 指摘密度 lấy từ đâu, và xử lý thế nào khi lệch trên hoặc dưới?**
Ngưỡng nên lấy từ **baseline nội bộ** của công ty hoặc dự án tương tự; nếu chưa có, em đặt tạm một khoảng (ví dụ thiết kế khoảng 0,5–1,5 指摘/trang – tham khảo) rồi hiệu chỉnh sau 1–2 module. Lệch trên: tài liệu còn non, có thể 差し戻し (sashimodoshi – trả lại) cho tác giả làm lại trước khi review tiếp. Lệch dưới: kiểm tra giờ review, năng lực người review, cân nhắc cho người khác review bổ sung. Điều quan trọng là **giải thích** được mọi điểm lệch.
> 💡 Đừng đọc một con số "chuẩn ngành"; nói rõ là baseline nội bộ và cách hiệu chỉnh sẽ an toàn và thuyết phục hơn.

**Q528. Một buổi review kết thúc với 0 指摘. PM nên vui hay lo?**
Nên nghi ngờ trước. 0 指摘 có thể vì tài liệu thật sự tốt, nhưng thường gặp hơn là review hời hợt, người review thiếu kiến thức nghiệp vụ, thời gian quá ngắn hoặc ngại "chê" đồng nghiệp. Em kiểm tra giờ review và checklist đã dùng, rồi cho một người khác review lấy mẫu một phần; nếu mẫu đó tìm ra lỗi bản chất thì cả buổi review phải làm lại. Với khách Nhật, báo cáo "0 指摘" không kèm giải thích thường bị hỏi ngược.

**Q529. Làm sao để review không thành buổi "bắt lỗi người" khiến dev ngại đưa tài liệu ra review?**
Nguyên tắc: **review sản phẩm, không review người**. 指摘 viết theo sự kiện ("mục 3.2 thiếu xử lý khi số tiền âm"), không viết nhận xét ("viết ẩu"); số 指摘 không dùng trực tiếp để chấm điểm cá nhân. Em khuyến khích review sớm từng phần nhỏ thay vì một lần cuối, ghi nhận người tìm ra lỗi quan trọng, và leader, PM cũng đưa tài liệu của chính mình ra review. Khi mật độ 指摘 của ai đó cao, ta bàn cách hỗ trợ chứ không phạt.

**Q530. Khách trả về tài liệu với rất nhiều 指摘 từ 顧客レビュー. PM xử lý thế nào?**
① Xác nhận fact: tổng số, phân loại, bao nhiêu lỗi bản chất, bao nhiêu do yêu cầu đổi. ② Lập kế hoạch sửa có ngày và báo khách theo 報連相 (hou-ren-sou – báo cáo, liên lạc, bàn bạc). ③ Tìm vì sao review nội bộ để lọt: so 指摘 của khách với biên bản review nội bộ, xác định quan điểm còn thiếu. ④ Bổ sung quan điểm đó vào checklist, 横展開 (yokotenkai – nhân rộng kiểm tra) sang tài liệu chưa gửi, và gửi khách phân tích cùng bản sửa.
> 💡 Khách đánh giá cao việc bạn tự phân tích "vì sao nội bộ để lọt" hơn là chỉ sửa đúng những điểm khách chỉ ra.

## 6.4 Test, chỉ số & evidence

**Q531. Mỗi mức 単体/結合/総合/受入テスト nhằm bắt loại lỗi nào, và PM theo dõi chỉ số gì ở từng mức?**
単体テスト (tantai tesuto – unit test) bắt lỗi logic trong module: theo dõi coverage C0/C1 (statement/branch). 結合テスト (ketsugou tesuto – integration test) bắt lỗi giao tiếp giữa module, dữ liệu, hệ thống ngoài: theo dõi mật độ test và bug theo interface. 総合テスト (sougou tesuto – system test) bắt lỗi so với yêu cầu và phi chức năng: theo dõi độ phủ yêu cầu, đường cong hội tụ. 受入テスト do khách làm: chỉ số chính là số bug khách tìm thấy. Mức sau toàn lỗi lẽ ra mức trước phải bắt là dấu hiệu mức trước yếu.

**Q532. テスト観点 là gì và vì sao khách Nhật hay hỏi "観点は網羅されていますか"?**
テスト観点 là các góc nhìn cần kiểm tra cho một chức năng: giá trị biên, giá trị bất thường, quyền hạn, xử lý đồng thời, ngày đặc biệt (cuối tháng, năm nhuận), message lỗi. Câu 観点は網羅されていますか (kanten wa moura sarete imasu ka – quan điểm đã bao phủ hết chưa) cho thấy khách đánh giá test qua **độ phủ quan điểm** chứ không chỉ số case. Em duy trì danh sách quan điểm chuẩn theo loại chức năng, review nó trước khi viết case, và bổ sung mỗi khi có bug lọt do thiếu quan điểm.
> 💡 Nêu được 1–2 quan điểm đặc thù nghiệp vụ (làm tròn số tiền, ngày nghỉ lễ Nhật) cho thấy bạn hiểu domain tài chính, bảo hiểm.

**Q533. テスト密度 (tesuto mitsudo – mật độ test) là gì và tính thế nào?**
テスト密度 = số test case / quy mô, thường là case/KLOC (theo dòng code) hoặc case/FP (theo function point). Nó cho biết test đã đủ "dày" so với độ lớn sản phẩm chưa, khi so với baseline cùng loại hệ thống và cùng mức test. Lưu ý KLOC phụ thuộc ngôn ngữ và cách đếm (có tính comment, code tự sinh hay không), nên phải thống nhất cách đếm trong 品質計画書 trước khi so sánh giữa các module hay dự án.

**Q534. バグ密度 (bagu mitsudo – mật độ bug) đọc thế nào cho đúng?**
バグ密度 = số bug phát hiện / quy mô (bug/KLOC hoặc bug/FP), tính riêng cho từng mức test. Phải đọc **cùng** テスト密度: bug thấp có thể do sản phẩm tốt hoặc do test chưa đủ; bug cao có thể do code kém hoặc do test rất kỹ. Em đặt khoảng mục tiêu trên–dưới theo baseline, và module nào nằm ngoài khoảng đều phải có phân tích định tính, không chỉ báo con số.

**Q535. Phân tích hai trục テスト密度 × バグ密度 giúp gì khi đánh giá chất lượng từng module?**
Đặt mỗi module lên ma trận 2×2: ① test đủ, bug trong ngưỡng → tương đối ổn; ② test đủ, bug cao → chất lượng build kém, cần review lại thiết kế/code và test bổ sung; ③ test thiếu, bug thấp → chưa đủ căn cứ đánh giá, phải bổ sung test; ④ test thiếu, bug cao → rủi ro cao nhất, ưu tiên xử lý. Ma trận giúp PM phân bổ effort test và giải thích cho khách vì sao module nào cần thêm thời gian.
> 💡 Vẽ ma trận 2×2 này lên bảng trong buổi phỏng vấn là cách nhanh nhất chứng minh bạn quản chất lượng bằng dữ liệu.

**Q536. 信頼度成長曲線 (shinraido seichou kyokusen – đường cong tăng trưởng độ tin cậy) đọc thế nào?**
Trục ngang là thời gian hoặc số case đã chạy, trục dọc là số bug tích lũy. Đường lý tưởng có dạng chữ S (thường mô hình hóa bằng đường Gompertz hoặc logistic): đầu tăng nhanh, sau chậm dần và **đi ngang** (収束 – shuusoku – hội tụ) khi gần hết test. Nếu đến cuối vẫn dốc lên gần như tuyến tính, sản phẩm chưa ổn định, chưa nên release. Em cập nhật theo ngày và so với đường dự báo để thấy lệch sớm thay vì đợi cuối kỳ.

**Q537. Đường cong đi ngang rất sớm khi mới chạy khoảng 40% số case. Đó là tín hiệu tốt hay xấu?**
Phải nghi ngờ trước. Có thể chất lượng tốt, nhưng thường gặp hơn: đang chạy các case dễ trước, tester bị chặn môi trường nên ít case thực chất, bug đã thấy nhưng chưa ghi phiếu, hoặc case thiếu quan điểm. Em kiểm tra tốc độ chạy case, phân bổ case theo quan điểm và module, hỏi tester về bug "chưa kịp ghi". Chỉ khi các yếu tố này bình thường mới kết luận chất lượng tốt.

**Q538. Đường cong có các "bậc thang" tăng vọt giữa chừng nói lên điều gì?**
Bậc thang thường xuất hiện khi một module mới được đưa vào test, môi trường hoặc dữ liệu thay đổi, hoặc có bản build chứa thay đổi lớn hay bản sửa gây デグレ (degure – lỗi hồi quy). Em đối chiếu thời điểm bậc thang với lịch build và nhật ký thay đổi để xác định nguyên nhân. Nếu do デグレ, phải mở rộng phạm vi test hồi quy hoặc tự động hóa cho vùng đó; nếu do module mới, nên vẽ đường riêng theo module để đọc đúng.

**Q539. エビデンス (ebidensu – bằng chứng test) gồm những gì và vì sao khách Nhật coi trọng?**
Evidence là chứng cứ cho thấy case đã chạy và cho kết quả như đã ghi: screenshot, log, kết quả SQL trước/sau, file output, kết quả so sánh. Với khách Nhật, "đã test" mà không có evidence coi như chưa test; evidence còn dùng khi có sự cố sau release để chứng minh phạm vi đã kiểm tra. Mỗi evidence gắn ID case, ngày, người test và được lưu theo cấu trúc thư mục, quy tắc đặt tên thống nhất.

**Q540. Làm sao cân bằng chi phí làm evidence với tiến độ?**
Thỏa thuận **mức evidence** với khách ngay trong 品質計画書: ví dụ màn hình chỉ cần screenshot kết quả cuối, batch cần log và dữ liệu trước/sau, case hồi quy tự động dùng report của tool thay screenshot. Dùng công cụ chụp/ghi tự động, template đặt tên file, và tính effort evidence vào ước lượng test dựa trên số đo thực tế của dự án trước. Tránh để cuối kỳ mới "bổ sung evidence", vì vừa tốn công vừa dễ thành làm giả.
> 💡 Nói rõ "evidence tạo bù sau khi test xong là rủi ro về tính trung thực" cho thấy bạn hiểu điểm khách Nhật nhạy cảm nhất.

**Q541. Làm evidence cho khách tài chính, bảo hiểm cần lưu ý gì về dữ liệu?**
Evidence thường chứa dữ liệu màn hình, nên phải dùng dữ liệu test giả lập, không dùng dữ liệu khách hàng thật; nếu bắt buộc dùng dữ liệu thật và được khách cho phép thì phải che (masking) thông tin cá nhân như tên, số tài khoản, số hợp đồng. Evidence lưu ở vùng có phân quyền, không gửi qua kênh cá nhân, và xóa theo quy định khi kết thúc dự án. Vi phạm ở điểm này là sự cố bảo mật, không còn là chuyện chất lượng.

**Q542. Tiêu chí bắt đầu (開始基準 – kaishi kijun) và kết thúc (完了基準 – kanryou kijun) của một mức test nên đặt thế nào?**
Bắt đầu: mức test trước đã đạt, test spec đã review và duyệt, môi trường và dữ liệu sẵn sàng, bản build qua smoke test; thiếu điều kiện thì không bắt đầu để tránh test "nửa vời" rồi phải chạy lại. Kết thúc: 消化率 (shoukaritsu – tỉ lệ case đã thực hiện) 100% có evidence, mật độ test/bug trong khoảng hoặc có giải thích, không còn bug nghiêm trọng mở, các bug đã sửa đã test hồi quy. Cả hai được thống nhất với khách trước khi test, không đặt lại lúc cuối.

## 6.5 Quản lý bug

**Q543. 不具合管理票 (fuguai kanrihyou – bảng quản lý lỗi) cần có những trường nào?**
Tối thiểu: ID, ngày 起票 (kihyou – tạo phiếu), người tạo, chức năng, môi trường, hiện tượng, bước tái hiện, kết quả mong đợi, mức nghiêm trọng, độ ưu tiên, 摘出工程 (tekishutsu koutei – công đoạn phát hiện), 作り込み工程 (tsukurikomi koutei – công đoạn gây ra lỗi), phân loại nguyên nhân, nội dung sửa, phạm vi ảnh hưởng, người sửa, người xác nhận, trạng thái, ngày đóng. Các trường phân tích phải bắt buộc khi đóng phiếu, nếu không cuối kỳ sẽ không làm được báo cáo chất lượng.

**Q544. Phân biệt severity và priority bằng ví dụ.**
Severity (重要度 – juuyoudo) là mức ảnh hưởng của lỗi đến hệ thống và nghiệp vụ; priority (優先度 – yuusendo) là thứ tự cần sửa. Ví dụ: sai logo trên màn hình đăng nhập có severity thấp nhưng priority cao nếu ngày mai demo cho ban lãnh đạo khách; lỗi tính sai ở một sản phẩm chưa mở bán có severity cao nhưng có thể xếp sau lỗi đang chặn cả nhóm test. Severity do người phát hiện đề xuất theo định nghĩa chung; priority do PM/leader cùng khách quyết.

**Q545. Nên định nghĩa các mức severity thế nào để tránh tranh cãi với khách?**
Viết định nghĩa có ví dụ cụ thể và thống nhất trong 品質計画書, ví dụ: S1 – dừng hệ thống, mất hoặc sai dữ liệu, tính sai tiền, lỗ hổng bảo mật; S2 – chức năng chính không dùng được nhưng có cách làm thay; S3 – lỗi chức năng phụ, hiển thị sai nhưng không sai dữ liệu; S4 – chính tả, layout nhỏ. Kèm thời hạn phản hồi và sửa cho từng mức. Khi bất đồng, đối chiếu định nghĩa và ví dụ chứ không thương lượng theo cảm giác.

**Q546. Phân loại nguyên nhân bug theo 仕様漏れ, 設計ミス, 実装ミス, テスト漏れ có ý nghĩa gì?**
仕様漏れ (shiyou more – thiếu sót spec): yêu cầu chưa được định nghĩa; 設計ミス (sekkei misu – lỗi thiết kế); 実装ミス (jissou misu – lỗi code); テスト漏れ (tesuto more – test bỏ sót). Phân loại cho biết **phải sửa quy trình ở đâu**: 仕様漏れ nhiều → cải thiện Q&A và review yêu cầu; 実装ミス nhiều → coding checklist, unit test; テスト漏れ nhiều → bổ sung quan điểm test. Nên thêm loại "nguyên nhân phía khách" (spec khách đổi hoặc sai) để phân định minh bạch.
> 💡 Luôn tách loại "nguyên nhân phía khách" — vừa công bằng vừa là dữ liệu quan trọng khi đàm phán phát sinh.

**Q547. 摘出工程 và 作り込み工程 khác nhau thế nào, phân tích chúng để làm gì?**
作り込み工程 là công đoạn tạo ra lỗi (ví dụ thiết kế chi tiết), 摘出工程 là công đoạn phát hiện lỗi (ví dụ test hệ thống). Lập ma trận hai chiều này cho thấy lỗi đã "trôi" qua bao nhiêu công đoạn: lỗi thiết kế đến test hệ thống mới thấy nghĩa là review thiết kế, unit test và test tích hợp đều 見逃し (minogashi – bỏ sót). Mục tiêu là tăng tỉ lệ phát hiện ngay tại công đoạn gây ra lỗi, và biết cần tăng cường kiểm tra ở công đoạn nào.

**Q548. 工程内摘出率 (kouteinai tekishutsuritsu – tỉ lệ phát hiện trong công đoạn) là gì và PM dùng nó thế nào?**
工程内摘出率 = số lỗi phát hiện ngay trong công đoạn gây ra / tổng số lỗi do công đoạn đó gây ra (tính đến thời điểm phân tích). Tỉ lệ thấp ở thiết kế nghĩa là review thiết kế yếu và chi phí 手戻り sẽ dồn về sau. Em theo dõi chỉ số này theo từng công đoạn, đặt mục tiêu tăng dần qua các release, và dùng nó làm căn cứ khi xin thêm effort review thượng nguồn.

**Q549. Tỉ lệ reopen bug cao (ví dụ trên 10% – tham khảo) cho thấy gì và xử lý thế nào?**
Reopen cao cho thấy sửa chưa triệt để: dev sửa triệu chứng chứ không sửa nguyên nhân, thiếu 影響調査 (eikyou chousa – điều tra phạm vi ảnh hưởng), không tự test lại trước khi chuyển trạng thái, hoặc phiếu bug mô tả không rõ. Em yêu cầu mỗi bản sửa ghi nguyên nhân, phạm vi ảnh hưởng, case đã tự test lại; leader review bản sửa của bug nghiêm trọng; và phân tích các phiếu reopen theo module, theo loại lỗi để tìm điểm yếu cụ thể.

**Q550. Vòng đời một bug từ lúc phát hiện đến khi đóng nên thế nào?**
起票 → phân loại và gán (PM/leader đặt priority, chỉ định người) → phân tích nguyên nhân và 影響調査 → sửa kèm unit test → review bản sửa → tester 再テスト (sai tesuto – test lại) và test hồi quy vùng ảnh hưởng → đóng, điền đủ trường phân tích. Bug liên quan cách hiểu spec phải qua Q&A với khách trước khi sửa. Mỗi trạng thái có thời hạn theo severity; bug quá hạn hiện đỏ trong báo cáo tuần.

**Q551. Bug do khách phát hiện trong 受入テスト cần xử lý khác bug nội bộ thế nào?**
Đây là **lỗi lọt ra**, nên xử lý ưu tiên và minh bạch hơn: ① xác nhận hiện tượng, tái hiện, kiểm tra có phải khác biệt cách hiểu spec không; ② phản hồi khách sớm (ví dụ trong ngày – tham khảo) kèm kế hoạch sửa; ③ báo tiến độ theo 報連相 đến khi đóng; ④ với lỗi nghiêm trọng, phân tích cả nguyên nhân phát sinh lẫn nguyên nhân lọt và 横展開. Thống kê riêng số bug khách tìm thấy, vì đó là chỉ số khách dùng để chấm vendor.
> 💡 Trả lời khách "chúng tôi đang xác nhận, sẽ báo lại trước X giờ" luôn tốt hơn im lặng hoặc vội phủ nhận.

**Q552. Khi số bug mở tăng nhanh hơn tốc độ sửa, PM xử lý thế nào?**
① Xem dữ liệu: bug mới tập trung ở module hay nguyên nhân nào, bao nhiêu là trùng hoặc không phải bug. ② Ưu tiên sửa theo severity và theo bug chặn test; tạm dừng test vùng quá nhiều lỗi, trả về dev kiểm tra lại nội bộ thay vì tiếp tục ghi phiếu; tăng người sửa có thời hạn. ③ Báo khách xu hướng kèm dự báo ngày hội tụ. ④ Nếu gốc là chất lượng build kém, làm lại review và unit test cho module đó trước khi test tiếp.

## 6.6 Phân tích nguyên nhân gốc & phòng ngừa

**Q553. なぜなぜ分析 (naze naze bunseki – phân tích "vì sao" lặp lại, 5 Whys) làm đúng cách như thế nào?**
Bắt đầu từ **hiện tượng cụ thể** đã xác nhận; mỗi tầng hỏi "vì sao" dựa trên sự kiện kiểm chứng được, không dựa trên phỏng đoán. Dừng khi chạm tới nguyên nhân thuộc **cơ chế, quy trình** mà ta kiểm soát và sửa được, không nhất thiết đúng 5 lần; mỗi tầng có thể rẽ nhiều nhánh. Kiểm tra lại bằng cách đọc ngược từ dưới lên với "vì vậy…" xem chuỗi có logic không. Nên làm theo nhóm, có người trong cuộc và người ngoài để tránh tự bào chữa.
> 💡 Bước "đọc ngược bằng 'vì vậy' để kiểm logic" ít ứng viên nhắc tới, rất ghi điểm với interviewer người Nhật.

**Q554. Vì sao "do dev không cẩn thận" không được chấp nhận làm nguyên nhân gốc?**
Vì nguyên nhân kiểu 注意不足 (chuui busoku – thiếu chú ý) hay 確認不足 (kakunin busoku – kiểm tra chưa đủ) chỉ dẫn đến biện pháp "sẽ chú ý hơn", không đo được, không nhân rộng được. Cần hỏi tiếp: vì sao quy trình cho phép một người sơ suất mà lỗi vẫn lọt — checklist thiếu mục, review thiếu quan điểm đó, không có test tự động? Báo cáo có biện pháp kiểu 気をつけます (ki wo tsukemasu – sẽ cẩn thận) gần như chắc chắn bị khách trả lại.

**Q555. 発生原因 (hassei gen'in – nguyên nhân phát sinh) và 流出原因 (ryuushutsu gen'in – nguyên nhân lọt) khác nhau thế nào?**
発生原因 trả lời "vì sao lỗi được tạo ra", ví dụ thiết kế không xét tháng 2 năm nhuận. 流出原因 trả lời "vì sao lỗi không bị chặn mà lọt ra", ví dụ test spec thiếu quan điểm ngày đặc biệt, checklist review thiết kế không có mục về ngày. Báo cáo cho khách Nhật phải phân tích **cả hai nhánh**, mỗi nhánh có biện pháp phòng ngừa riêng. Thiếu nhánh 流出 là lỗi phổ biến nhất trong báo cáo của vendor offshore.
> 💡 Câu này gần như chắc chắn được hỏi khi phỏng vấn PM thị trường Nhật — nhớ cặp 発生/流出.

**Q556. 再発防止策 (saihatsu boushisaku – biện pháp chống tái phát) thế nào thì được coi là tốt?**
Tốt khi: ① trỏ thẳng tới nguyên nhân gốc đã xác định; ② là **cơ chế** (仕組み – shikumi) chứ không phải lời hứa: thêm mục checklist, quan điểm review, test tự động, ràng buộc trong công cụ, ポカヨケ (poka-yoke – cơ chế chống thao tác sai); ③ có người chịu trách nhiệm và ngày áp dụng; ④ có cách kiểm chứng hiệu quả, ví dụ 1–2 sprint không tái phát lỗi cùng loại. Biện pháp quá nặng như thêm ba tầng duyệt cũng là biện pháp xấu, vì team sẽ tìm cách bỏ qua.

**Q557. 横展開 là gì và làm thế nào cho thực chất?**
横展開 là sau khi tìm ra một lỗi và nguyên nhân, **kiểm tra những chỗ tương tự xem có cùng vấn đề không** và áp biện pháp sang đó: module khác dùng cùng logic, màn hình cùng pattern, dự án khác cùng team hoặc cùng framework. Thực chất nghĩa là có danh sách đối tượng cụ thể, cách tìm (tìm theo pattern code, rà thiết kế), kết quả từng đối tượng và evidence. Báo cáo cho khách nêu rõ "đã kiểm tra N chỗ, phát hiện M chỗ, đã sửa xong".

**Q558. 暫定対応 (zantei taiou – xử lý tạm thời) và 恒久対応 (koukyuu taiou – xử lý triệt để) khác nhau thế nào?**
暫定対応 là chặn thiệt hại ngay, ví dụ batch tính phí sai thì tạm dừng batch, chạy tay có kiểm tra chéo và sửa dữ liệu sai. 恒久対応 là xử lý tận gốc: sửa logic, test hồi quy, release bản vá, kèm 再発防止策. Hai bước có lịch riêng và đều báo khách; không để 暫定対応 kéo dài thành "vĩnh viễn", vì nó thường dựa vào thao tác tay và dễ sai ở lần sau.
> 💡 Khi kể tình huống, nói rõ "暫定 trong X giờ, 恒久 trong Y ngày" — khách Nhật đánh giá tốc độ chặn thiệt hại trước, độ triệt để sau.

**Q559. 三現主義 (sangen shugi – nguyên tắc "ba thực") áp dụng khi phân tích lỗi phần mềm thế nào?**
Ba thực gồm 現場 (genba – hiện trường), 現物 (genbutsu – hiện vật), 現実 (genjitsu – thực tế). Trong phần mềm: xem trực tiếp log, dữ liệu, môi trường nơi lỗi xảy ra; tái hiện lỗi trên đúng phiên bản build; kết luận dựa trên sự kiện đã xác minh chứ không dựa trên báo cáo gián tiếp hay trí nhớ. Em yêu cầu dev tái hiện được lỗi và đưa log trước khi đề xuất nguyên nhân; điều chưa tái hiện được ghi rõ là giả thuyết trong báo cáo.

**Q560. Tổ chức buổi phân tích nguyên nhân thế nào để không biến thành truy tìm người có lỗi?**
Thống nhất ngay đầu buổi: mục tiêu là sửa **cơ chế**, không ai bị phạt vì lỗi được báo trung thực. Dựng timeline sự kiện theo bước và vai trò ("bước review ngày X không có quan điểm Y") thay vì tên người. PM điều phối bằng câu hỏi "quy trình nào đã cho phép điều này" và tự nhận phần trách nhiệm quản lý nếu có. Báo cáo gửi khách nói về vai trò và quy trình, không nêu tên cá nhân.

**Q561. Sau khi đưa ra 再発防止策, PM theo dõi hiệu quả thế nào?**
Đưa từng biện pháp vào danh sách theo dõi có owner, ngày áp dụng và chỉ số kiểm chứng, ví dụ "0 bug loại làm tròn tiền ở test tích hợp các module sau", "100% pull request có mục checklist X". Review danh sách trong họp chất lượng hằng tuần hoặc mỗi sprint; sau 1–2 chu kỳ, biện pháp không hiệu quả thì sửa, biện pháp tốn công mà không bắt được lỗi thì đề xuất bỏ. Báo kết quả cho khách để khép vòng.

**Q562. Khách yêu cầu làm なぜなぜ分析 cho cả một bug hiển thị nhỏ. Có nên làm đầy đủ không?**
Em tôn trọng yêu cầu nhưng điều chỉnh độ sâu theo mức độ: bug nhỏ làm bản ngắn một trang gồm hiện tượng, 発生/流出 tóm tắt, biện pháp, 横展開. Nếu có nhiều bug nhỏ cùng loại, em gộp phân tích theo **nhóm nguyên nhân** (ví dụ 15 lỗi hiển thị cùng do thiếu checklist UI) thay vì từng phiếu, vừa đỡ công vừa ra biện pháp có tác dụng hơn. Đồng thời thỏa thuận với khách từ mức severity nào thì bắt buộc phân tích đầy đủ.

## 6.7 Báo cáo chất lượng & quyết định release

**Q563. 品質報告書 (hinshitsu houkokusho – báo cáo chất lượng) gửi khách thường có cấu trúc thế nào?**
Thường gồm: ① tóm tắt và kết luận đánh giá ở đầu; ② phạm vi và quy mô (KLOC/FP, số chức năng); ③ phần **định lượng** (定量 – teiryou): mật độ review, test, bug so với mục tiêu, đường cong hội tụ; ④ phần **định tính** (定性 – teisei): bug theo nguyên nhân, module, công đoạn gây lỗi; ⑤ bug còn mở và cách xử lý; ⑥ rủi ro và hành động tiếp theo. Định lượng chỉ ra "lệch ở đâu", định tính giải thích "vì sao và đã xử lý chưa".

**Q564. Vì sao báo cáo chất lượng chỉ có số liệu mà thiếu phân tích định tính thường bị khách Nhật trả lại?**
Vì con số tự nó không nói chất lượng tốt hay xấu: cùng một mật độ bug có thể là tốt ở module này, xấu ở module khác. Khách cần nghe vendor **đánh giá** (評価 – hyouka), ví dụ: "module X vượt ngưỡng do 実装ミス tập trung ở xử lý ngày, đã bổ sung 30 case, đường cong đã hội tụ, nên đánh giá đạt". Thiếu phần này, khách phải tự phân tích, và họ sẽ coi như vendor chưa làm xong việc.

**Q565. 障害報告書 (shougai houkokusho – báo cáo sự cố) cần những mục gì?**
Chuẩn thường gặp: tiêu đề và mức độ; 発生日時 (hassei nichiji – thời điểm phát sinh) và thời điểm phát hiện; 影響範囲 (eikyou han'i – phạm vi ảnh hưởng: người dùng, dữ liệu, giao dịch, thời gian); hiện tượng; 原因 (gen'in – nguyên nhân, gồm phát sinh và lọt); 暫定対応; 恒久対応 và lịch; 再発防止策; 横展開; timeline chi tiết. Mở đầu bằng lời xin lỗi ngắn và hiện trạng (đã khôi phục hay chưa) để lãnh đạo khách nắm ngay.

**Q566. Khi có sự cố production, báo cáo nên chia thành mấy lần và tốc độ ra sao?**
Thường chia ba: 第一報 (dai-ippou – báo cáo đầu tiên) gửi rất sớm, kể cả khi chưa rõ nguyên nhân, nêu hiện tượng, ảnh hưởng đã biết, việc đang làm và giờ báo tiếp; 続報 (zokuhou – báo cáo tiếp theo) cập nhật đúng mốc đã hẹn; 最終報 (saishuuhou – báo cáo cuối) là 障害報告書 hoàn chỉnh. Mốc cụ thể (ví dụ 第一報 trong 30–60 phút – tham khảo) theo thỏa thuận với khách. Tốc độ của 第一報 quan trọng hơn độ hoàn chỉnh.
> 💡 Nói "em không chờ có nguyên nhân mới báo" — đó đúng là điều khách Nhật muốn nghe nhất ở PM.

**Q567. Mô tả 影響範囲 trong báo cáo sự cố thế nào để khách tin?**
Phải **định lượng và có căn cứ**: bao nhiêu bản ghi, giao dịch, người dùng bị ảnh hưởng, trong khoảng thời gian nào, chức năng nào; xác định bằng cách nào (câu truy vấn, log đã kiểm tra). Tách rõ ba nhóm "đã xác nhận có ảnh hưởng", "đã xác nhận không ảnh hưởng", "đang điều tra". Tránh viết "ảnh hưởng nhỏ" hay "có lẽ không ảnh hưởng" khi chưa kiểm tra; khách tài chính cần con số để báo tiếp cho cấp trên hoặc cơ quan quản lý của họ.

**Q568. 出荷判定 (shukka hantei – đánh giá cho phép xuất xưởng) hay リリース判定 (ririisu hantei – quyết định release) dựa trên tiêu chí nào?**
Tiêu chí thống nhất trước và nhìn **toàn bộ mức sẵn sàng**, không chỉ test: ① các mức test đạt tiêu chí kết thúc, đường cong hội tụ; ② bug còn mở đều có workaround và được khách đồng ý; ③ deliverable, release note, 運用手順書 đã review; ④ kế hoạch triển khai, rollback, giám sát, người trực sẵn sàng; ⑤ rủi ro còn lại được nêu rõ. Buổi 出荷判定会議 (shukka hantei kaigi – họp quyết định) có PM, QA, onsite/khách; biên bản ghi kết luận: release, release có điều kiện, hoặc chưa release.

**Q569. 条件付き出荷 (jouken tsuki shukka – release có điều kiện) là gì và khi nào nên dùng?**
Là release dù còn một số điểm chưa đạt tiêu chí, kèm **điều kiện** được khách đồng ý bằng văn bản: danh sách bug còn mở và workaround, hạn sửa, giới hạn phạm vi sử dụng, giám sát tăng cường sau release. Chỉ nên dùng khi các điểm chưa đạt không ảnh hưởng dữ liệu, tiền, bảo mật, và lợi ích của việc release đúng hạn rõ ràng lớn hơn rủi ro. PM không tự quyết điều kiện thay khách và phải theo dõi đến khi mọi điều kiện được đóng.
> 💡 Nhấn mạnh "khách đồng ý bằng văn bản" — release có điều kiện chỉ thỏa thuận miệng là rủi ro trách nhiệm.

**Q570. Báo cáo chất lượng hằng tuần khác báo cáo cuối công đoạn thế nào?**
Báo cáo tuần ngắn (1–2 trang), tập trung **xu hướng và cảnh báo sớm**: tiến độ chạy case, bug mới/đóng/còn mở, đường cong, các điểm vượt ngưỡng và hành động. Báo cáo cuối công đoạn đầy đủ phân tích định lượng, định tính, kết luận đánh giá chất lượng và là căn cứ để chuyển công đoạn hoặc release. Báo cáo tuần làm tốt thì báo cáo cuối không có "bất ngờ": khách không nên đọc thấy một vấn đề lần đầu ở báo cáo cuối.

**Q571. Trình bày chỉ số xấu trong báo cáo thế nào để không làm khách mất niềm tin?**
Theo nhịp **sự thật → nguyên nhân → hành động → dự báo**. Ví dụ: "Mật độ bug module thanh toán vượt mục tiêu 40%; nguyên nhân tập trung ở 実装ミス khi làm tròn số tiền; đã review lại toàn bộ hàm tính tiền và bổ sung 25 case; dự kiến hội tụ ngày X, sẽ báo lại." Không giấu, không làm đẹp số, không dùng từ mơ hồ. Khách Nhật mất niềm tin vì bị bất ngờ, không phải vì một chỉ số xấu được báo sớm kèm kế hoạch.

**Q572. Ai viết và ai duyệt báo cáo chất lượng trước khi gửi khách?**
Số liệu do QA hoặc test lead tổng hợp trực tiếp từ công cụ quản lý bug và test (không nhập tay để tránh sai lệch); phân tích định tính do leader từng module viết; PM viết phần đánh giá, kết luận và chịu trách nhiệm cuối cùng. Bản tiếng Nhật được BrSE kiểm tra thuật ngữ trước khi PM duyệt; dự án lớn có thể qua bộ phận QA độc lập của công ty nếu có. Gửi onsite xem trước để họ không bị bất ngờ khi khách hỏi.

## 6.8 Chuẩn & cải tiến liên tục

**Q573. ISO 9001 giúp gì cho một công ty outsourcing làm với khách Nhật?**
ISO 9001 là chuẩn về hệ thống quản lý chất lượng (QMS): quy trình được định nghĩa, có hồ sơ, có 内部監査 (naibu kansa – đánh giá nội bộ), 是正処置 (zesei shochi – hành động khắc phục) và cải tiến liên tục. Với khách Nhật, nó là tín hiệu ban đầu rằng vendor có quy trình, thường được hỏi khi đánh giá nhà cung cấp. Nhưng chứng chỉ không thay được chất lượng thực tế; PM cần biết quy trình dự án đáp ứng QMS ở điểm nào để trả lời khi khách audit.
> 💡 Đừng khẳng định công ty đang có chứng chỉ nào khi chưa xác minh; nói "nếu công ty áp dụng ISO 9001 thì em sẽ…" là an toàn.

**Q574. ISO 27001 (ISMS) ảnh hưởng thế nào đến cách vận hành dự án cho khách tài chính, bảo hiểm?**
ISO 27001 là chuẩn hệ thống quản lý an toàn thông tin (ISMS – Information Security Management System). Trong dự án, nó thể hiện qua: phân quyền truy cập theo nhu cầu, cấp và thu hồi tài khoản khi người vào/ra dự án, kiểm soát thiết bị và USB, không đưa dữ liệu khách ra ngoài vùng cho phép, đào tạo bảo mật định kỳ, quy trình báo sự cố bảo mật. Khách tài chính thường có checklist bảo mật riêng hoặc audit; PM phải có hồ sơ chứng minh từng mục.

**Q575. CMMI là gì và các mức trưởng thành nói lên điều gì với PM?**
CMMI là mô hình đánh giá mức trưởng thành quy trình, gồm 5 mức: 1 Initial (phụ thuộc cá nhân), 2 Managed (dự án có kế hoạch, theo dõi), 3 Defined (quy trình chuẩn cấp tổ chức), 4 Quantitatively Managed (quản lý bằng số liệu thống kê), 5 Optimizing (cải tiến liên tục dựa trên dữ liệu). Với PM, câu hỏi thực tế là dự án có dùng quy trình chuẩn của tổ chức và có baseline để so sánh không; bộ chỉ số mật độ kiểu Nhật là nền tảng để tiến tới quản lý định lượng.

**Q576. Áp dụng PDCA vào quản lý chất lượng dự án cụ thể ra sao?**
Plan: đặt mục tiêu chất lượng và kế hoạch review/test trong 品質計画書. Do: thực hiện, ghi nhận 指摘, bug, số liệu. Check: so số liệu với mục tiêu theo tuần hoặc công đoạn, phân tích nguyên nhân các điểm lệch. Act: điều chỉnh checklist, quan điểm test, phân công, và đưa bài học vào kế hoạch giai đoạn sau. Chữ "A" hay bị bỏ nhất: nhiều dự án đo rất nhiều nhưng không thay đổi gì, nên em luôn kết thúc họp chất lượng bằng danh sách hành động có owner.

**Q577. 改善 (kaizen – cải tiến liên tục) khác gì một dự án cải tiến lớn?**
Kaizen là cải tiến **nhỏ, liên tục, do chính người làm đề xuất**: rút ngắn một bước build, thêm một mục checklist, tự động hóa một bước tạo evidence. Nó không cần ngân sách lớn và hiệu quả tích lũy theo thời gian. Em duy trì bằng cách mỗi retrospective chọn 1–2 cải tiến cụ thể, đo trước/sau, chia sẻ kết quả và ghi nhận người đề xuất. Khách Nhật thường trông đợi 改善提案 từ vendor, nên đây cũng là điểm cộng trong quan hệ khách hàng.

**Q578. 5S áp dụng vào môi trường phát triển phần mềm như thế nào?**
5S gồm 整理 (seiri – sàng lọc), 整頓 (seiton – sắp xếp), 清掃 (seisou – sạch sẽ), 清潔 (seiketsu – săn sóc, duy trì), 躾 (shitsuke – kỷ luật, sẵn sàng). Trong phần mềm: xóa branch, file, code chết không dùng; cấu trúc thư mục tài liệu và evidence thống nhất; dọn warning và TODO quá hạn; chuẩn hóa thành quy tắc, template; duy trì bằng kiểm tra định kỳ cho thành thói quen. Lợi ích thực tế là tìm tài liệu nhanh và giảm nhầm phiên bản khi bàn giao.

**Q579. Kể tên QC七つ道具 và công cụ nào hữu ích nhất cho PM phần mềm?**
QC七つ道具 (QC nanatsu dougu – 7 công cụ QC): Pareto (パレート図 – pareeto zu), biểu đồ xương cá (特性要因図 – tokusei youin zu), check sheet, histogram, biểu đồ phân tán (散布図 – sanpu zu), biểu đồ kiểm soát (管理図 – kanri zu) và phân tầng (層別 – soubetsu; có tài liệu thay bằng graph). Với PM phần mềm, hữu ích nhất là **Pareto** để chọn vài nguyên nhân gây phần lớn bug, **xương cá** để phân tích nguyên nhân theo nhóm, và **phân tầng** để chia bug theo module, công đoạn, nguyên nhân.
> 💡 Kể một lần thật đã dùng Pareto để chọn 2–3 nguyên nhân ưu tiên sẽ hơn hẳn việc liệt kê đủ 7 công cụ.

**Q580. Làm sao áp dụng quy trình chuẩn (ISO, CMMI) mà không biến dự án thành "làm giấy tờ"?**
Nguyên tắc **tailoring**: điều chỉnh quy trình theo quy mô và rủi ro của dự án, có ghi lại và được duyệt, thay vì áp nguyên khối. Mỗi biểu mẫu phải trả lời được "ai dùng nó để ra quyết định gì"; không trả lời được thì gộp hoặc bỏ. Số liệu sinh tự động từ công cụ (hệ thống ticket, Git, CI) thay vì nhập tay. Định kỳ hỏi team bước nào tốn công mà không bắt được lỗi để đề xuất bỏ qua kênh cải tiến chính thức.

## 6.9 Chất lượng đặc thù offshore

**Q581. Những nguồn lỗi đặc thù của mô hình offshore Việt Nam – Nhật Bản là gì?**
Phổ biến nhất: ① hiểu sai spec do khác ngôn ngữ, do dịch, hoặc do bối cảnh nghiệp vụ Nhật (thuế, lịch, cách ghi tên và địa chỉ); ② thông tin rơi rớt qua nhiều tầng khách – onsite – BrSE – dev; ③ giả định ngầm khi spec không ghi mà dev ngại hỏi; ④ khác biệt giữa môi trường offshore và môi trường khách; ⑤ tài liệu tiếng Nhật diễn đạt chưa chuẩn. Vì vậy quản lý chất lượng offshore phải đầu tư nhiều vào **xác nhận hiểu đúng** trước khi code.

**Q582. Q&A管理表 (Q&A kanrihyou – bảng quản lý hỏi đáp) giúp kiểm soát chất lượng thế nào?**
Mọi câu hỏi về spec được ghi một nơi: ID, ngày hỏi, tài liệu và mục liên quan, câu hỏi kèm **phương án đề xuất** của team, người trả lời, câu trả lời, ngày, trạng thái, và đã cập nhật vào tài liệu chưa. Nó ngăn dev tự giả định, giữ bằng chứng khi có tranh cãi trách nhiệm, và là nguồn để cập nhật spec. Em theo dõi số câu còn mở và tuổi câu hỏi; câu chặn tiến độ quá hạn (ví dụ quá 2 ngày – tham khảo) được escalate qua onsite.
> 💡 Câu hỏi gửi khách luôn kèm phương án ("A hay B, chúng tôi đề xuất A vì…") — khách Nhật trả lời nhanh hơn hẳn.

**Q583. Làm sao kiểm tra team offshore đã hiểu đúng spec trước khi code?**
Dùng kỹ thuật **giải thích ngược**: dev trình bày lại spec bằng lời của mình, hoặc viết tóm tắt luồng và các test case chính, cho BrSE/onsite nghe; sai lệch lộ ra ngay. Kết hợp viết test case song song với thiết kế chi tiết để buộc phải hiểu điều kiện biên; điểm mơ hồ đẩy vào Q&A. Với chức năng phức tạp, tổ chức 認識合わせ (ninshiki awase – buổi thống nhất cách hiểu) với khách trên một bộ dữ liệu ví dụ cụ thể.

**Q584. Văn hóa checklist trong offshore nên xây thế nào để không thành "tick cho có"?**
Checklist phải **ngắn, cụ thể, sinh ra từ lỗi thật**: mỗi mục trỏ được tới một loại bug đã từng lọt; mục lâu không bắt được gì thì xem xét bỏ. Tách checklist theo loại sản phẩm (màn hình, batch, API, tài liệu) thay vì một danh sách chung dài. Leader kiểm tra lấy mẫu vài mục đã tick; tick mà không làm thì xử lý như lỗi quy trình. Mục nào kiểm được bằng máy thì đưa vào công cụ thay vì để người tick.
> 💡 Câu "checklist là trí nhớ của dự án về các lỗi đã gặp" giúp bạn giải thích giá trị của nó rất gọn.

**Q585. Self-check trước 納品 (nouhin – bàn giao) gồm những bước gì?**
① Dev self-check theo checklist và chạy lại unit test; ② build từ source sạch theo đúng hướng dẫn, bảo đảm không phụ thuộc máy cá nhân; ③ chạy smoke test và bộ test hồi quy chính; ④ kiểm tra tài liệu khớp code, 改訂履歴 đã cập nhật; ⑤ đối chiếu danh sách deliverable; ⑥ người không trực tiếp làm (QA nội bộ hoặc leader) kiểm tra chéo. Kết quả self-check được ghi lại và gửi kèm khi khách yêu cầu.

**Q586. Vai trò của BrSE trong kiểm soát chất lượng là gì, ngoài việc dịch?**
BrSE là "cổng chất lượng" về hiểu biết: kiểm tra spec đã được hiểu đúng, review thiết kế chi tiết và test spec từ góc nhìn của khách, kiểm tra deliverable tiếng Nhật trước khi gửi, phát hiện sớm khác biệt về nghiệp vụ và cách làm. BrSE cũng là người nhận phản hồi của khách, nên cần biến 指摘 của khách thành mục checklist cho team. PM phải chừa effort review cho BrSE trong kế hoạch, không để BrSE chỉ làm phiên dịch.

**Q587. Tài liệu tiếng Nhật hay mắc lỗi gì và kiểm soát thế nào?**
Lỗi thường gặp: 誤字脱字 (goji datsuji – sai chữ, thiếu chữ), 表記ゆれ (hyouki yure – một khái niệm viết nhiều kiểu, ví dụ lẫn katakana/kanji hoặc ký tự full-width/half-width), câu dịch máy cứng hoặc sai nghĩa, kính ngữ không phù hợp. Kiểm soát bằng glossary thuật ngữ thống nhất, quy tắc trình bày (dấu câu, số, ngày), công cụ kiểm tra chính tả và 表記ゆれ, rồi BrSE review trước khi gửi. Dịch máy chỉ dùng làm bản nháp, luôn có người đọc lại.
> 💡 Khách dễ suy từ lỗi chính tả ra "làm ẩu" ở cả code — sửa lỗi chính tả là việc rẻ nhất mà giữ ấn tượng tốt nhất.

**Q588. Một bộ 納品 package chuẩn gồm những gì?**
Thường gồm: 納品物一覧 (nouhinbutsu ichiran – danh sách sản phẩm bàn giao) có version; source code (tag hoặc commit cụ thể) và hướng dẫn build, deploy; tài liệu thiết kế đã cập nhật; test spec, kết quả test và evidence; báo cáo chất lượng; release note gồm thay đổi, bug đã sửa, lỗi còn tồn đọng kèm workaround; 運用手順書 nếu có. Người thứ hai kiểm tra đủ danh mục trước khi gửi qua kênh truyền file được khách chấp thuận.

**Q589. Làm sao giảm khác biệt giữa môi trường test offshore và môi trường của khách?**
Thống nhất từ đầu danh sách phiên bản (OS, middleware, DB, browser, framework) và ghi vào 品質計画書; dùng container hoặc hạ tầng dạng code để tái tạo môi trường; dùng dữ liệu test có cấu trúc giống thật nhưng đã ẩn danh. Phần không tái tạo được (hệ thống ngoài, mạng nội bộ khách) liệt kê rõ là ngoài phạm vi test offshore và lập kế hoạch test tại môi trường khách cùng onsite. Bug do môi trường được phân loại riêng để cải thiện.

**Q590. Onsite liên tục phàn nàn chất lượng bàn giao của offshore. PM xử lý thế nào?**
① Lấy fact: danh sách lỗi onsite tìm thấy, phân loại theo nguyên nhân và công đoạn. ② Ngắn hạn: thêm một vòng kiểm tra chéo trước bàn giao cho vùng hay lỗi, thống nhất lại định nghĩa "xong" với onsite. ③ Báo onsite và khách kế hoạch theo 報連相, không đổ lỗi qua lại. ④ Xử lý gốc: thường là thiếu hiểu spec hoặc thiếu quan điểm test, nên cập nhật checklist, Q&A và 横展開 sang các module đang làm; theo dõi số lỗi onsite tìm thấy theo tuần để chứng minh cải thiện.

## 6.10 Câu hỏi senior: trade-off & tình huống xám

**Q591. Mọi chỉ số chất lượng đều trong ngưỡng, nhưng khách vẫn chê chất lượng. Anh/chị xử lý thế nào?**
Chỉ số đo **cái ta chọn đo**, còn khách cảm nhận qua trải nghiệm: lỗi lặp lại, giao diện không như kỳ vọng, phản hồi chậm, tài liệu sai chính tả, sửa lỗi này sinh lỗi khác. Em cùng onsite gặp khách để lấy ví dụ cụ thể, phân loại xem khoảng cách nằm ở kỳ vọng chưa được viết thành yêu cầu hay ở khía cạnh chưa đo. Sau đó bổ sung chỉ số theo góc nhìn khách (bug khách tìm thấy, thời gian phản hồi, 指摘 trong 顧客レビュー) và thống nhất lại tiêu chí.
> 💡 Chốt bằng ý "chất lượng là cái khách cảm nhận, chỉ số chỉ là công cụ" — đừng bảo vệ con số trước mặt khách.

**Q592. Mật độ bug của dự án thấp bất thường so với baseline. Anh/chị có tự hào không?**
Chưa. Trước tiên kiểm tra các giả thuyết: test thiếu (mật độ test thấp, thiếu quan điểm), tester không ghi phiếu các bug dev sửa ngay, nhiều lỗi bị gộp vào một phiếu, quy mô KLOC bị đội lên do code tự sinh, hoặc chức năng đơn giản hơn dự án baseline. Em lấy mẫu: cho người ngoài team test thăm dò một module, đối chiếu commit "fix" với phiếu bug. Chỉ khi loại trừ được các khả năng này mới báo khách "chất lượng tốt", kèm giải thích vì sao.
> 💡 Câu này kiểm tra bạn có hoài nghi con số đẹp hay không — "tốt bất thường thì phải kiểm tra" là hướng trả lời đúng.

**Q593. Khi phải chọn giữa giữ chất lượng và giữ deadline, anh/chị quyết định thế nào?**
Em không tự chọn ngầm. Em lượng hóa các phương án: ① giữ ngày, thu hẹp phạm vi release (tách chức năng chưa đạt sang bản sau); ② giữ ngày, release có điều kiện với các bug không ảnh hưởng dữ liệu, tiền; ③ lùi ngày, giữ đủ phạm vi và chất lượng; ④ tăng nguồn lực, nêu rõ chi phí và rủi ro. Mỗi phương án kèm rủi ro chất lượng cụ thể, rồi trình khách và cấp trên quyết. Điểm không thương lượng là lỗi liên quan tiền, dữ liệu, bảo mật.

**Q594. Giảm effort review/test để cắt chi phí có bao giờ là quyết định đúng không?**
Có, nếu dựa trên dữ liệu và rủi ro: module đơn giản, tái sử dụng với lịch sử ít lỗi, có test tự động tốt thì có thể hạ từ inspection xuống peer review hoặc giảm mức evidence. Nhưng quyết định phải được ghi lại, có đánh giá rủi ro, được khách đồng ý nếu đã cam kết trong 品質計画書, và có chỉ số theo dõi để quay lại khi lỗi tăng. Cắt đồng loạt mọi module chỉ vì thiếu ngân sách thực chất là đẩy chi phí sang 手戻り về sau.

**Q595. Khách đòi "chất lượng kiểu Nhật" nhưng muốn làm Agile, ít tài liệu, release hai tuần một lần. Anh/chị dung hòa thế nào?**
Giữ **tinh thần**, đổi **hình thức**: Definition of Done chặt (review, test, evidence tự động), test hồi quy tự động thay cho phần lớn evidence screenshot, tài liệu "vừa đủ" nhưng luôn đồng bộ với code, mỗi sprint có báo cáo chất lượng ngắn với chỉ số xu hướng. Thống nhất từ đầu tài liệu nào bắt buộc (interface, vận hành) và tài liệu nào thay bằng code, test. Lỗi nhỏ xử lý qua retrospective; lỗi lọt ra khách vẫn làm 再発防止 đầy đủ.

**Q596. Xây văn hóa chất lượng cho một team mới thành lập, ví dụ ở chi nhánh mới, bắt đầu từ đâu?**
Bắt đầu từ ít mà chắc: ① 3–5 quy tắc không thương lượng (bàn giao phải qua self-check, sửa code phải cập nhật tài liệu, bug phải có phiếu, test phải có evidence); ② template và checklist lấy từ dự án đã thành công; ③ người có kinh nghiệm thị trường Nhật review, kèm cặp các deliverable đầu tiên; ④ chia sẻ 指摘 của khách như bài học chung; ⑤ đo vài chỉ số cốt lõi từ tuần đầu để có baseline. Mục tiêu đầu tiên là **sự nhất quán**.
> 💡 Liên hệ kinh nghiệm build-up team mới của chính bạn (nếu có) — JD coi kinh nghiệm setup chi nhánh Đà Nẵng là lợi thế lớn.

**Q597. Team "làm đẹp" chỉ số (tách nhỏ phiếu bug, không ghi bug tự sửa, chia nhỏ review) để đạt target. Anh/chị xử lý thế nào?**
Đây là dấu hiệu chỉ số đang bị dùng sai mục đích: khi con số thành target để đánh giá người, người ta sẽ tối ưu con số thay vì chất lượng. Em tách chỉ số chất lượng khỏi đánh giá cá nhân trực tiếp và nói rõ mục đích là tìm điểm yếu của quy trình. Kết hợp kiểm tra chéo (đối chiếu commit "fix" với phiếu bug, lấy mẫu review) và đọc nhiều chỉ số cùng lúc để khó "lách". Công khai ghi nhận người báo lỗi trung thực, kể cả lỗi của chính mình.

**Q598. Bug nghiêm trọng bắt nguồn từ spec sai của khách, nhưng team cũng không phát hiện khi review. Anh/chị phân định trách nhiệm trong báo cáo thế nào?**
Trình bày theo fact, không né cũng không đổ: nguyên nhân phát sinh là spec (dẫn tài liệu, lịch sử Q&A); nguyên nhân lọt là review và test của team chưa có quan điểm kiểm tra tính hợp lý của spec. Báo cáo nêu cả hai, mỗi bên có biện pháp: team bổ sung quan điểm "nghi ngờ spec" vào checklist; đề xuất với khách bước xác nhận spec cho các vùng tương tự. Chi phí sửa do ai chịu thì thảo luận riêng theo hợp đồng, không trộn vào báo cáo kỹ thuật.
> 💡 Tách "phân tích nguyên nhân" khỏi "đàm phán chi phí" là dấu hiệu senior — trộn hai việc làm khách thấy vendor đang tự bào chữa.

**Q599. Làm sao chứng minh với khách rằng đầu tư thêm vào chất lượng (review, test tự động) là đáng tiền?**
Dùng số liệu của chính dự án: chi phí trung bình sửa một bug theo công đoạn phát hiện (giờ công), số bug lọt ra khách trước và sau khi áp dụng, thời gian test hồi quy tiết kiệm mỗi release, số sự cố production. Trình bày dạng "đầu tư X giờ mỗi tháng, giảm Y giờ 手戻り và Z sự cố" thay vì nói chung "chất lượng tốt hơn". Đề xuất thử có thời hạn trên một module, đo kết quả, rồi mới mở rộng.

**Q600. Nếu chịu trách nhiệm chất lượng cao nhất cho nhiều dự án cùng lúc, anh/chị đo và duy trì chất lượng thế nào?**
Em xây ba lớp: ① **chuẩn chung** — template 品質計画書, định nghĩa chỉ số và severity, checklist dùng chung, mỗi dự án tailoring có duyệt; ② **dữ liệu chung** — dashboard tổng hợp chỉ số từ công cụ, baseline theo loại dự án, cảnh báo khi dự án lệch ngưỡng; ③ **học chung** — lỗi lọt ra khách ở dự án này được 横展開 sang dự án khác, họp chất lượng định kỳ giữa các PM. Chỉ số cuối cùng em bám là số lỗi khách phát hiện và mức hài lòng của khách sau mỗi release.

