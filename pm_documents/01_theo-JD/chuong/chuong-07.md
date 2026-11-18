# Chương 7 · Giao tiếp, văn hóa & quản trị kỳ vọng khách Nhật (Q601–Q700)

## 7.1 報連相 & 確認

**Q601. 報連相 là gì và vì sao khách Nhật coi trọng nó đến vậy trong dự án outsourcing?**
報連相 (hou-ren-sou) gồm 報告 (houkoku – báo cáo kết quả/tiến độ cho người giao việc), 連絡 (renraku – chia sẻ fact cho người liên quan) và 相談 (soudan – xin ý kiến trước khi tự quyết). Khách Nhật chịu trách nhiệm trước nội bộ nên cần biết sớm để không bị bất ngờ; 報連相 chính là công cụ kiểm soát rủi ro của họ. Với vendor offshore khác ngôn ngữ, lệch 2 giờ, 報連相 tốt là bằng chứng hằng ngày rằng dự án "đang trong tầm kiểm soát".
> 💡 Phân biệt được 報告–連絡–相談 bằng ví dụ dự án thật sẽ ghi điểm hơn đọc định nghĩa.

**Q602. Tần suất và độ chi tiết của 報連相 với khách nên thiết lập thế nào?**
Em chốt từ kickoff một communication plan: daily report 3–5 dòng (đã xong, đang làm, vướng gì) gửi trước 17:00 giờ Nhật; báo cáo tiến độ tuần trong buổi họp định kỳ; báo ngay trong ngày khi có sự cố, lệch > 1 ngày ở milestone hoặc rủi ro mới mức cao (ngưỡng tham khảo). Độ chi tiết theo người nhận: người phụ trách cần chi tiết task, cấp quản lý chỉ cần kết luận, tín hiệu màu và quyết định cần xin. Sau 2–3 tuần, em hỏi lại khách để chỉnh.

**Q603. "Không có tin tức là tin xấu" — vì sao với khách Nhật, vendor im lặng lại nguy hiểm?**
Với khách Nhật, im lặng nghĩa là vendor "không nắm được" hoặc "đang giấu vấn đề", nên họ bắt đầu hỏi dồn, micro-manage và mất niềm tin dù dự án thực ra ổn. Vì vậy em báo cả khi không có gì mới: 「予定通り進んでおります」 (yotei doori susunde orimasu – đang tiến triển đúng kế hoạch) kèm % hoàn thành. Quy tắc team: mọi câu hỏi của khách có phản hồi trong ngày, ít nhất là 一次回答 (ichiji kaitou – trả lời sơ bộ) "đã nhận, sẽ trả lời trước 15:00 ngày mai".
> 💡 一次回答 gần như không tốn công nhưng giữ niềm tin cực hiệu quả — nên nêu như một quy tắc của team.

**Q604. 中間報告 (chuukan houkoku – báo cáo giữa chừng) là gì, nên làm vào thời điểm nào?**
Là báo cáo trước khi việc hoàn thành để khách kiểm tra hướng đi sớm, tránh làm xong mới phát hiện sai. Em đặt mốc ở khoảng 30–50% khối lượng, hoặc ngay khi có output đầu tiên xem được: màn hình mẫu, bản nháp thiết kế, 10–20% test case. Nội dung gồm đã làm gì, hướng đang đi, điểm cần khách xác nhận, dự báo ngày xong. Với task từ 2 tuần trở lên (tham khảo), bỏ qua 中間報告 thì rủi ro làm lại rất cao.

**Q605. 先手 (sente – đi trước một bước) trong giao tiếp với khách nghĩa là gì? Cho ví dụ.**
Là chủ động đưa thông tin, cảnh báo rủi ro và đề xuất trước khi khách phải hỏi. Ví dụ: thấy spec màn hình B mâu thuẫn với batch C, em gửi câu hỏi kèm 2 phương án ngay khi phát hiện thay vì đợi đến lúc code; hoặc 2 tuần trước UAT, em gửi checklist khách cần chuẩn bị (data test, account, người tham gia). Ngược lại là 後手 (gote – bị động chạy theo), khiến khách thấy vendor chỉ "làm theo bảo".

**Q606. Khi báo cáo cho người Nhật, cấu trúc nội dung nên thế nào để họ nắm nhanh?**
Em theo 結論から (ketsuron kara – nói kết luận trước): ① trạng thái/kết luận một câu → ② lý do, số liệu → ③ việc cần khách làm hoặc quyết, kèm hạn. Tách rõ 事実 (jijitsu – sự thật) và 意見 (iken – nhận định), dùng con số thay cho "sắp xong", "hơi trễ". Ví dụ: "Chức năng X trễ 2 ngày do API phía khách cấp chậm; đề xuất dời mốc test sang 20/11, cần khách duyệt trước 15/11."
> 💡 "Sắp xong" là bẫy kinh điển — người Nhật sẽ hỏi lại ngay "bao nhiêu %, ngày nào?".

**Q607. Tiến độ đang lệch nhưng PM nghĩ có thể đuổi kịp bằng OT — có nên báo khách ngay không?**
Có, nhưng báo theo kiểu 相談 chứ không phải báo động. Khi dự báo lệch ở mốc cam kết (tham khảo: > 1 ngày ở milestone hoặc buffer đã dùng > 50%), em báo kèm kế hoạch phục hồi: OT có giới hạn, bổ sung người, đổi thứ tự việc, và ngày kiểm tra lại. Âm thầm OT rồi vẫn trễ là lỗi kép: vừa trễ vừa giấu. Khách Nhật đánh giá vendor báo sớm cao hơn vendor chỉ "cố gắng".

**Q608. Làm sao 確認 (kakunin – xác nhận) để tránh hiểu lầm yêu cầu khi giao tiếp bằng ngôn ngữ thứ hai?**
Em dùng 3 lớp: ① 復唱 (fukushou – nhắc lại bằng lời của mình) ngay trong họp: 「念のため確認させてください。〜という理解でよろしいでしょうか」 (cho phép xác nhận lại: hiểu là… có đúng không ạ); ② ghi thành văn bản (biên bản, bảng Q&A) và xin khách confirm; ③ minh họa bằng ví dụ, mockup, bảng input/output thay vì chỉ mô tả chữ. Điểm nào ảnh hưởng scope, chi phí, lịch thì bắt buộc chốt bằng văn bản.

**Q609. 認識合わせ (ninshiki awase – thống nhất cách hiểu) khác gì với việc gửi tài liệu cho khách đọc?**
Gửi tài liệu là một chiều, khách có thể đọc lướt rồi nói "OK"; 認識合わせ là hai bên cùng đi qua từng điểm dễ hiểu khác nhau và chốt lại. Em làm ở các điểm chuyển giai đoạn: sau 要件定義 (youken teigi – định nghĩa yêu cầu), trước test, trước release, với danh sách chuẩn bị sẵn 5–10 điểm "dễ hiểu sai" kèm ví dụ. Kết quả ghi biên bản; điểm còn khác biệt thành mục Q&A có hạn trả lời.

**Q610. 報連相 quá dày có phản tác dụng không? PM cân bằng thế nào?**
Có: khách nhận 10 email/ngày từ nhiều member sẽ bỏ sót tin quan trọng và thấy vendor thiếu tự chủ. Em cân bằng: ① một đầu mối gửi, gom theo lịch cố định; ② việc trong quyền của team thì tự quyết rồi 報告, chỉ 相談 khi ảnh hưởng scope/lịch/chất lượng; ③ tiêu đề có nhãn 【至急】(shikyuu – gấp), 【ご確認依頼】(go-kakunin irai – nhờ xác nhận), 【共有】(kyouyuu – để biết). Định kỳ hỏi khách lượng thông tin đã vừa chưa.
> 💡 Senior PM thể hiện 報連相 "đúng liều", không phải "càng nhiều càng tốt".

**Q611. Khi nào dùng email, chat, điện thoại hay họp để 報連相 với khách Nhật?**
Em chia kênh theo mức độ và nhu cầu lưu vết: email cho nội dung cần bằng chứng (quyết định, thay đổi, báo cáo chính thức); chat (Teams, Slack, Chatwork… theo khách) cho trao đổi nhanh, nhưng kết luận quan trọng phải tóm vào email hoặc bảng quản lý; điện thoại/họp cho tin xấu, sự cố nghiêm trọng và việc cần bàn nhiều chiều. Nguyên tắc: tin xấu không gửi chỉ bằng chat — gọi trước, email xác nhận sau.

## 7.2 Ra quyết định kiểu Nhật

**Q612. 根回し (nemawashi – vận động, thống nhất trước) là gì và PM vendor làm 根回し thế nào?**
Là trao đổi riêng với từng người liên quan trước cuộc họp chính thức, để cuộc họp chỉ còn là nơi xác nhận. Trước buổi họp xin đổi scope hay lịch, em gửi tài liệu trước và gọi 15–30 phút với 担当 (tantou – người phụ trách) phía khách để nghe phản ứng, chỉnh phương án, hỏi cấp trên họ đang lo điều gì. Đưa đề xuất "bất ngờ" vào họp có quản lý khách thường chỉ nhận về 「持ち帰ります」 (mochikaerimasu – xin mang về xem xét).
> 💡 Nói rõ 根回し không phải "chính trị ngầm" mà là tôn trọng cách ra quyết định của khách.

**Q613. 稟議 (ringi – trình ký tập thể) ảnh hưởng thế nào đến lịch dự án?**
稟議 là đề xuất bằng văn bản (稟議書 – ringisho) đi qua nhiều cấp đóng dấu phê duyệt, nên mọi việc cần ngân sách hay thay đổi lớn (CR, gia hạn, thêm người) đều có lead time từ vài ngày đến vài tuần tùy cấp. PM phải hỏi 担当 "quy trình duyệt mất bao lâu, qua những ai" và đưa thời gian đó vào kế hoạch, gửi đề xuất sớm tương ứng. Quên tính 稟議 là lý do phổ biến khiến CR duyệt xong thì đã trễ.

**Q614. Hierarchy phía khách Nhật (部長/課長/担当) — PM giao tiếp với từng cấp ra sao?**
担当 làm việc hằng ngày, cần chi tiết và trả lời nhanh; 課長 (kachou – trưởng phòng/nhóm) quản lý tiến độ, cần tóm tắt rủi ro và việc cần quyết; 部長 (buchou – trưởng bộ phận) quan tâm kết quả kinh doanh, ngân sách, rủi ro lớn, chỉ cần báo cáo 1 trang ở mốc quan trọng. Em giữ kênh chính qua 担当 và luôn để 担当 có mặt khi trao đổi với cấp trên của họ. Gặp 部長 định kỳ (mỗi phase hoặc mỗi quý) cùng lãnh đạo phía mình.

**Q615. 窓口 (madoguchi – đầu mối liên lạc) là gì? Vì sao phải thống nhất 窓口 hai bên?**
窓口 là người được giao nhận thông tin chính thức giữa hai bên. Thiếu 窓口 rõ ràng thì mỗi member trả lời khách một kiểu, yêu cầu đi thẳng xuống dev mà không qua kiểm soát scope, quyết định mâu thuẫn nhau. Em chốt trong kickoff: 窓口 chính và dự phòng mỗi bên, kênh nào cho loại việc nào, ai được cam kết lịch/chi phí (chỉ PM). Member vẫn trao đổi kỹ thuật được, nhưng kết luận phải về 窓口 và vào bảng quản lý.

**Q616. Vì sao khách Nhật thường ra quyết định chậm? PM nên phản ứng thế nào?**
Thường do cần 合意形成 (goui keisei – tạo đồng thuận) giữa nhiều bộ phận, văn hóa tránh rủi ro và 稟議 nhiều cấp. PM không nên ép "phải quyết ngay", mà: ① cung cấp đủ thông tin để quyết (phương án, ưu nhược, chi phí, rủi ro); ② nói rõ 期限 (kigen – hạn) và tác động nếu quá hạn; ③ đề xuất phương án mặc định; ④ đưa việc chờ quyết định vào kế hoạch như một dependency có owner và ngày.

**Q617. Làm sao để tài liệu của PM giúp 担当 khách dễ trình 稟議 nội bộ?**
Em coi 担当 là người phải "bán" đề xuất cho cấp trên của họ, nên viết theo dạng họ dùng lại được: 1 trang tiếng Nhật nêu 背景 (haikei – bối cảnh), 目的 (mokuteki – mục đích), 2–3 phương án so sánh, chi phí, rủi ro nếu không làm, khuyến nghị và lịch. Em hỏi trước mẫu 稟議書 hoặc những điểm sếp họ hay hỏi. Tài liệu tốt giúp 担当 ghi điểm trong nội bộ, và họ trở thành đồng minh của dự án.
> 💡 Ý "giúp 担当 thắng trong nội bộ của họ" thể hiện tư duy senior rõ nhất ở nhóm câu này.

**Q618. 部長 khách yêu cầu trực tiếp PM một việc mà 担当 không biết — xử lý sao?**
Em tiếp nhận lịch sự, không từ chối tại chỗ nhưng cũng không cam kết ngay: 「承知いたしました。担当の〇〇様とも認識を合わせた上で、ご回答いたします」 (shouchi itashimashita… – tôi đã rõ, sẽ thống nhất với anh/chị 〇〇 phụ trách rồi trả lời). Sau đó báo ngay cho 担当 để họ không bị gạt ra ngoài, cùng đánh giá tác động rồi trả lời 部長 qua đúng kênh, có 担当 trong CC. Đi vòng qua 担当 làm họ mất mặt và mất luôn người hỗ trợ hằng ngày quan trọng nhất.

**Q619. Trong họp khách gật đầu đồng ý nhưng sau đó lại đổi ý — vì sao, và phòng ngừa thế nào?**
Thường vì người dự họp không phải người quyết, hoặc bộ phận khác (vận hành, kiểm toán, business) chưa được hỏi; cái gật đầu có thể chỉ là "tôi đã nghe". Phòng ngừa: ① xác định 決裁者 (kessaisha – người có quyền phê duyệt) cho từng loại quyết định từ đầu; ② hỏi rõ 「この内容で確定としてよろしいでしょうか」 (chốt nội dung này được chưa ạ) và ghi vào 決定事項 (kettei jikou – điều đã quyết) trong biên bản; ③ hỏi "còn bộ phận nào cần xác nhận không" trước khi chốt.

**Q620. Có phải lúc nào cũng nên chờ khách đồng thuận? Khi nào PM nên đẩy khách quyết nhanh hơn?**
Không. Khi chi phí chờ vượt rủi ro quyết sai — ví dụ team 10 người chờ spec, mỗi tuần chờ là 50 man-day bị treo — em làm rõ chi phí đó bằng con số, đưa 暫定案 (zanteian – phương án tạm) để team chạy tiếp phần không phụ thuộc, và xin khách "quyết định có điều kiện" có thể đảo ngược. Đẩy nhanh bằng dữ liệu và lựa chọn, không bằng áp lực; nếu vẫn tắc thì escalate qua lãnh đạo hai bên, có 根回し trước.
> 💡 "Biến chi phí chờ thành con số" là điểm phân biệt senior với mid-level.

**Q621. Các stakeholder phía khách (IT, business, vận hành) có ý kiến mâu thuẫn — PM xử lý ra sao?**
Em không tự chọn bên, vì quyết định nội bộ khách không thuộc quyền vendor. Em: ① gom các yêu cầu mâu thuẫn vào bảng so sánh, nêu tác động của từng phương án; ② đưa về 窓口 hoặc 決裁者 để họ tự 合意形成 nội bộ; ③ ghi thành vấn đề có hạn trong bảng quản lý. Trong lúc chờ, team làm phần không bị ảnh hưởng. Tránh trả lời riêng từng bên kiểu "vâng ạ", vì sẽ thành các cam kết chồng chéo.

## 7.3 Họp & tài liệu giao tiếp

**Q622. Một buổi 定例会議 (teirei kaigi – họp định kỳ) với khách Nhật nên chuẩn bị và vận hành thế nào?**
Trước 1 ngày làm việc, em gửi agenda và tài liệu (báo cáo tiến độ, Q&A còn mở, vấn đề cần quyết) để khách đọc trước. Họp đúng giờ, thường 30–60 phút, theo thứ tự: tiến độ (tín hiệu màu) → vấn đề, rủi ro → Q&A → quyết định cần xin → việc tuần tới. Cuối họp đọc lại 決定事項 và 宿題 (shukudai – việc mang về, có người phụ trách và hạn). Biên bản gửi trong 24 giờ.

**Q623. 議事録 (gijiroku – biên bản họp) chuẩn gồm những gì và vì sao phải xin khách confirm?**
Gồm thời gian, người tham dự, mục tiêu, nội dung chính, 決定事項, 宿題 (việc – người – hạn), vấn đề còn mở, lịch họp tiếp. Em gửi trong 24 giờ, kèm câu 「内容に相違がございましたら、〇日までにご指摘いただけますと幸いです」 (nếu có điểm sai khác, mong anh/chị chỉ ra trước ngày…). Biên bản đã confirm là bằng chứng khi sau này có tranh cãi về scope hay cam kết, nên các điểm liên quan scope, chi phí phải viết rõ, không mơ hồ.
> 💡 Biên bản gửi trễ 3 ngày gần như mất giá trị — người Nhật đánh giá vendor qua chính những việc nhỏ này.

**Q624. Biên bản nên do vendor hay khách viết? Nếu khách sửa biên bản theo hướng có lợi cho họ thì sao?**
Em chủ động nhận viết, vì người viết kiểm soát cách ghi nhận. Nếu khách sửa, em đối chiếu với ghi chép hoặc recording (nếu đã xin phép ghi); điểm sửa không đúng thực tế thì không phản bác bằng email lạnh lùng mà gọi 担当 để 認識合わせ, rồi gửi bản thống nhất. Nếu khác biệt về scope/chi phí chưa giải quyết được, ghi thành vấn đề mở và đưa vào họp định kỳ — không để "im lặng là đồng ý".

**Q625. QA管理表 (QA kanrihyou – bảng quản lý hỏi đáp) dùng để làm gì và nên có những cột nào?**
Là nơi duy nhất ghi mọi câu hỏi về spec giữa hai bên, tránh hỏi qua chat rồi thất lạc. Cột tối thiểu: số thứ tự, ngày tạo, người hỏi, chức năng/màn hình, câu hỏi kèm phương án đề xuất, người trả lời, câu trả lời, hạn, trạng thái, ảnh hưởng (spec/lịch/chi phí), cần cập nhật tài liệu không. Em review bảng trong mỗi buổi 定例; câu quá hạn thì nêu đích danh tác động lên lịch.
> 💡 Mỗi câu hỏi kèm "phương án em đề xuất" để khách chỉ cần chọn — tốc độ trả lời nhanh hơn hẳn.

**Q626. 課題管理表 (kadai kanrihyou – bảng quản lý vấn đề) khác gì QA管理表?**
QA管理表 xử lý câu hỏi cần làm rõ (thông tin còn thiếu), còn 課題管理表 quản lý vấn đề cần hành động để gỡ: chậm cấp môi trường, mâu thuẫn spec giữa hai hệ thống, thiếu người tham gia UAT… Mỗi 課題 có owner, hạn, ưu tiên, tác động, hành động tiếp theo và trạng thái. Câu Q&A quá hạn mà ảnh hưởng lịch thì em nâng thành 課題 để có owner và được theo dõi ở cấp cao hơn.

**Q627. 進捗報告書 (shinchoku houkokusho – báo cáo tiến độ) gửi khách nên trình bày ra sao?**
Trang đầu là tóm tắt cho cấp quản lý: trạng thái tổng thể theo tín hiệu 青/黄/赤 (ao/ki/aka – xanh/vàng/đỏ), kế hoạch so với thực tế ở các mốc, top 3 rủi ro/vấn đề và quyết định cần khách. Phần sau mới là chi tiết: tiến độ theo chức năng, việc tuần này/tuần tới, Q&A và 課題 tồn. Mọi mục 黄/赤 phải kèm nguyên nhân, 対策 (taisaku – biện pháp xử lý) và ngày dự kiến về xanh.
> 💡 Người Nhật gọi đèn xanh là 青 (ao) — dùng đúng từ này trong báo cáo cho tự nhiên.

**Q628. 見える化 (mieruka – minh bạch hóa, trực quan hóa) trong dự án offshore nghĩa là gì?**
Là làm cho tình trạng thật của dự án hiển thị để ai cũng thấy mà không cần hỏi: tiến độ, backlog, bug, Q&A, rủi ro. Cách làm: dashboard chung trên công cụ khách quen (Backlog, Redmine, Jira…), biểu đồ kế hoạch–thực tế hoặc burn-down, bảng Q&A và 課題 khách xem được bất cứ lúc nào. Với khách Nhật, 見える化 giảm báo cáo thủ công và giảm lo lắng, vì "không nhìn thấy" chính là gốc của mất niềm tin.

**Q629. Có nên cho khách xem toàn bộ dashboard nội bộ, kể cả số bug và task trễ?**
Em cho khách xem dữ liệu thật nhưng thiết kế theo lớp: tiến độ, bug theo mức độ, Q&A, 課題 là chung; năng suất từng người, đánh giá nội bộ, chi phí nội bộ thì không. Che số xấu rủi ro hơn nhiều, vì khách phát hiện là mất niềm tin vào toàn bộ báo cáo. Điều quan trọng là số liệu luôn đi kèm diễn giải và 対策, để khách thấy vấn đề "đang được kiểm soát" chứ không chỉ thấy số đỏ.
> 💡 "Minh bạch nhưng có thiết kế lớp thông tin" là câu trả lời cân bằng mà interviewer chờ ở senior.

**Q630. Họp online với khách Nhật cần lưu ý gì để chuyên nghiệp?**
Gửi lời mời qua calendar kèm link và agenda; vào trước 3–5 phút kiểm tra âm thanh, màn hình chia sẻ; tên hiển thị theo quy ước (công ty + họ tên). Khi có BrSE hoặc phiên dịch, nói câu ngắn, chờ dịch xong mới nói tiếp, chia sẻ màn hình tài liệu để giảm hiểu lầm. Chỉ ghi âm khi đã xin phép. Cuối họp tóm tắt quyết định và kết thúc đúng giờ, vì người Nhật thường có lịch họp nối tiếp.

**Q631. Khách hỏi một câu trong họp mà PM chưa chắc câu trả lời — nên xử lý thế nào?**
Không đoán, vì câu trả lời trong họp được coi là cam kết. Em nói 「確認の上、明日中にご回答いたします」 (kakunin no ue, ashita-juu ni go-kaitou itashimasu – xác nhận xong sẽ trả lời trong ngày mai), ghi ngay thành 宿題 có hạn trong biên bản, rồi trả lời đúng hoặc sớm hơn hạn. Nếu đến hạn chưa có kết luận, gửi 中間報告 cho biết đang ở đâu và hạn mới. Trả lời sai rồi đính chính tốn niềm tin hơn nhiều so với hẹn lại.

**Q632. Tài liệu giao tiếp viết bằng tiếng Nhật hay tiếng Anh, và ai chịu trách nhiệm chất lượng nội dung?**
Theo thỏa thuận với khách; phần lớn khách Nhật cần tiếng Nhật cho tài liệu chính thức (báo cáo, biên bản, Q&A). Team viết nội dung, BrSE hoặc comtor dịch và rà soát, nhưng PM chịu trách nhiệm nội dung cam kết: con số, ngày, phạm vi phải được PM đối chiếu bản gốc trước khi gửi. Em duy trì 用語集 (yougoshuu – bảng thuật ngữ) để thống nhất cách dịch, tránh một khái niệm có ba cách gọi.

**Q633. Khách liên tục gửi yêu cầu qua chat, không ghi vào bảng Q&A — PM chuẩn hóa thế nào mà không làm khách khó chịu?**
Em không từ chối kênh chat mà "chuyển kênh" thay khách: nhận yêu cầu, trả lời 「承知いたしました。QA管理表No.〇〇として登録いたしました」 (đã rõ, đã ghi thành mục số… trong bảng Q&A) kèm link, cuối ngày gom các mục mới vào email tóm tắt. Trong 定例, em cho khách thấy lợi ích: mục nào cũng có số, hạn, trạng thái, không thất lạc. Sau vài tuần, phần lớn khách tự ghi vào bảng vì thấy tiện hơn.
> 💡 Đổi thói quen khách bằng cách làm thay họ trước, đừng bằng quy định.

## 7.4 Vai trò cầu nối BrSE, comtor, onsite

**Q634. BrSE (Bridge SE) khác comtor (コミュニケーター – phiên dịch IT) và onsite coordinator thế nào?**
BrSE là kỹ sư hiểu cả kỹ thuật lẫn tiếng Nhật: phân tích yêu cầu, làm rõ spec, viết/dịch tài liệu thiết kế, chịu trách nhiệm phần "hiểu đúng" giữa khách và team. Comtor chủ yếu phiên dịch họp và biên dịch tài liệu, không chịu trách nhiệm quyết định kỹ thuật. Onsite coordinator (hoặc BrSE onsite) làm tại văn phòng khách, nắm thông tin nhanh và xử lý vấn đề tại chỗ. PM phải phân vai rõ để không ai "tưởng người kia làm".

**Q635. PM không giỏi tiếng Nhật thì làm việc với khách và BrSE thế nào để vẫn là người chịu trách nhiệm cao nhất?**
Em tách vai: BrSE lo ngôn ngữ và làm rõ yêu cầu, PM lo quyết định và cam kết (lịch, chi phí, scope, chất lượng). Cụ thể: PM dự mọi buổi họp quan trọng và chuẩn bị nội dung trước với BrSE; email có cam kết phải có bản tóm tắt tiếng Việt/Anh để PM duyệt; phần 決定事項 của biên bản viết song ngữ. Song song, PM học tiếng Nhật đủ đọc tiêu đề, thuật ngữ, nghe được ý chính để không bị "mù" thông tin.
> 💡 Thành thật về trình độ tiếng Nhật, nhưng nêu kế hoạch học có mục tiêu và mốc thời gian — JD có hỗ trợ đào tạo tiếng Nhật.

**Q636. Rủi ro "BrSE thành nút cổ chai" biểu hiện ra sao và phòng ngừa thế nào?**
Biểu hiện: Q&A tồn vì chờ BrSE dịch, BrSE kín lịch họp không còn thời gian review, team không dám hỏi khách trực tiếp, BrSE nghỉ là dự án đứng. Phòng ngừa: ① lập kế hoạch capacity cho BrSE (tham khảo: không để quá 70–80% thời gian cho dịch); ② có BrSE/comtor dự phòng và member chủ chốt đọc được spec tiếng Nhật; ③ Q&A đi qua bảng, không qua tin nhắn riêng với BrSE; ④ công cụ dịch được công ty duyệt cùng 用語集 để member tự đọc tài liệu.

**Q637. BrSE tự ý hứa với khách một deadline mà team không kịp — PM xử lý thế nào?**
① Xác nhận fact: BrSE đã nói gì, khách hiểu thế nào, đã có văn bản chưa. ② Đánh giá nhanh: ưu tiên lại thì có kịp không, kịp được phần nào. ③ Nếu không kịp, PM báo khách ngay trong ngày: xin lỗi, đưa ngày thực tế và phương án giao phần quan trọng trước. ④ Phòng ngừa: quy định chỉ PM xác nhận lịch/chi phí, BrSE trả lời 「確認して回答します」 (sẽ xác nhận rồi trả lời), và chia sẻ bài học cho các dự án khác.

**Q638. Làm sao biết BrSE truyền đạt đúng ý, không "lọc" tin xấu hay làm mềm quá mức?**
Em kiểm bằng nhiều nguồn: đọc email gửi đi qua công cụ dịch được phép để đối chiếu ý chính; quan sát phản ứng của khách trong họp; định kỳ hỏi trực tiếp khách 「何かご懸念はございますか」 (nani ka go-kenen wa gozaimasu ka – anh/chị có lo ngại gì không ạ). Tin xấu phải theo mẫu cố định (sự việc, tác động, 対策, ngày) để không còn chỗ làm mềm. Không phải vì nghi ngờ BrSE, mà vì PM chịu trách nhiệm cuối cùng.

**Q639. Khi nào nên đưa BrSE sang onsite, khi nào nên giữ offshore?**
Onsite hợp lý khi giai đoạn 要件定義 và 設計 (sekkei – thiết kế) cần trao đổi nhiều; khách mới cần xây quan hệ; hệ thống khách không truy cập được từ xa (thường gặp ở khách tài chính do quy định bảo mật); hoặc giai đoạn UAT, go-live cần xử lý tại chỗ. Offshore hợp lý khi spec đã ổn định và kênh từ xa vận hành tốt. Em cân chi phí onsite với chi phí hiểu lầm, và luôn có người đối ứng ở offshore để onsite không thành ốc đảo thông tin.

**Q640. Onsite coordinator và PM offshore phối hợp thế nào để khách không nhận hai thông điệp khác nhau?**
Nguyên tắc "một giọng nói": sync 15 phút mỗi ngày giữa onsite và PM trước giờ làm của khách; cùng dùng một bảng Q&A/課題; phân quyền rõ onsite được trả lời gì tại chỗ, việc gì phải mang về PM. Tin quan trọng (trễ, sự cố, thay đổi) thì PM và onsite thống nhất nội dung trước rồi mới báo khách. Onsite còn là "tai" của PM: ghi nhận không khí và những lo ngại khách chưa nói ra, báo về hằng ngày.

**Q641. Member offshore có nên giao tiếp trực tiếp với khách Nhật, hay mọi thứ qua BrSE?**
Em cho phép có kiểm soát: member chủ chốt được trao đổi kỹ thuật trực tiếp (tiếng Nhật, hoặc tiếng Anh nếu khách đồng ý) để bớt tầng truyền đạt, với điều kiện kết luận ghi vào bảng Q&A, không cam kết lịch/scope, có BrSE hoặc PM trong kênh. Lợi ích là phản hồi nhanh và member trưởng thành; rủi ro là sai ngôn ngữ, cam kết lẻ tẻ. Với khách mới, em giữ qua BrSE 1–2 tháng đầu rồi mở dần khi đã có tin cậy.

**Q642. Dùng dịch máy cho tài liệu của khách Nhật có rủi ro gì?**
Hai rủi ro chính: ① bảo mật — đưa spec, dữ liệu khách lên công cụ dịch công cộng có thể vi phạm NDA, nhất là với khách tài chính, bảo hiểm; chỉ dùng công cụ công ty đã cho phép và đúng quy định của khách; ② sai nghĩa — tiếng Nhật hay lược chủ ngữ, phủ định nằm cuối câu, thuật ngữ nghiệp vụ dễ dịch sai. Em dùng dịch máy để đọc hiểu nội bộ; tài liệu gửi khách phải qua người rà soát và đối chiếu 用語集.
> 💡 Nhắc đến NDA và bảo mật khi nói về dịch máy cho thấy hiểu đặc thù khách tài chính Nhật.

**Q643. Đã có BrSE giỏi, vì sao PM vẫn cần học tiếng Nhật?**
Vì nếu mọi thông tin đi qua một người, PM bị phụ thuộc và bỏ lỡ sắc thái: một câu 「ちょっと厳しいですね」 (chotto kibishii desu ne – hơi căng đấy) có thể là cảnh báo nghiêm trọng. Biết tiếng Nhật giúp PM tự kiểm chứng thông tin, nói trực tiếp lời chào, cảm ơn, xin lỗi trong tình huống quan trọng và xây quan hệ với cấp quản lý khách. Mục tiêu thực tế không phải thay BrSE, mà là đủ để kiểm chứng và tạo niềm tin.

## 7.5 Ngôn ngữ & ngầm ý

**Q644. Keigo gồm những loại nào? PM cần dùng thế nào với khách?**
敬語 (keigo – kính ngữ) gồm 尊敬語 (sonkeigo – tôn kính, nâng hành động của người khác: いらっしゃる, ご覧になる), 謙譲語 (kenjougo – khiêm nhường, hạ hành động của mình: 伺う, 拝見する) và 丁寧語 (teineigo – lịch sự, です/ます). Với khách, dùng 尊敬語 cho khách và 謙譲語 cho phía mình, kể cả khi nhắc đến sếp mình (không thêm さん, xưng 弊社 – heisha – công ty chúng tôi). Người Nhật thường bỏ qua lỗi keigo nhỏ của người nước ngoài; quan trọng là lịch sự nhất quán.

**Q645. Mở đầu và kết thúc email business với khách Nhật thế nào cho chuẩn?**
Mở: tên công ty, bộ phận, họ + 様 (sama – kính ngữ gọi người), rồi 「お世話になっております。〇〇社の〇〇です。」 (osewa ni natte orimasu – cảm ơn sự quan tâm thường ngày). Thân: kết luận trước, đoạn ngắn, đánh số các điểm cần xác nhận, nêu hạn. Kết: 「ご確認のほど、よろしくお願いいたします。」 (go-kakunin no hodo… – kính nhờ anh/chị xác nhận) và chữ ký đầy đủ. Tiêu đề rõ, có nhãn và hạn, ví dụ 【ご確認依頼】要件定義書v1.2(11/20まで).
> 💡 Một email một chủ đề — khách Nhật thường chuyển tiếp email cho người khác xử lý theo từng chủ đề.

**Q646. 御社, 貴社 và 弊社 khác nhau thế nào?**
御社 (onsha) và 貴社 (kisha) đều là "quý công ty": 御社 dùng khi nói, 貴社 dùng khi viết (email, văn bản). 弊社 là "công ty chúng tôi" dạng khiêm nhường, dùng cả nói lẫn viết. Trong văn bản, gọi người bên khách bằng họ + 様; với chức danh thì viết 〇〇部長 hoặc 部長の〇〇様, tránh 部長様 vì thường bị coi là thừa kính ngữ. Đây là lỗi nhỏ nhưng lộ ra ngay từ email đầu tiên.

**Q647. Người Nhật thường nói "không" bằng những cách nào?**
Họ hiếm khi nói thẳng 「できません」 với đối tác. Tín hiệu hay gặp: 「それはちょっと…」 (sore wa chotto – cái đó thì hơi…), 「難しいですね」 (muzukashii desu ne – khó đấy), 「検討します」 (kentou shimasu – sẽ xem xét), 「考えておきます」 (kangaete okimasu – để tôi suy nghĩ), im lặng lâu hoặc chuyển chủ đề. Trong kinh doanh, 「難しい」 thường gần với "không" hơn là "khó nhưng làm được". PM nên coi đó là từ chối mềm và hỏi lại điều kiện, thay vì cố thuyết phục ngay.
> 💡 Bẫy: hiểu 「難しいです」 là "khó nhưng vẫn làm" rồi báo team chuẩn bị triển khai.

**Q648. 「検討します」 và 「前向きに検討します」 khác gì nhau, PM nên phản ứng thế nào?**
「検討します」 có thể là xem xét thật hoặc từ chối lịch sự; 「前向きに検討します」 (maemuki ni kentou shimasu – xem xét theo hướng tích cực) cho thấy thiện chí nhưng vẫn chưa phải cam kết. Em hỏi tiếp 「いつ頃ご判断いただけそうでしょうか」 (khoảng khi nào có thể quyết ạ) và 「追加で必要な情報はございますか」 (có cần thêm thông tin gì không ạ). Sau đó ghi vào 課題管理表 với ngày dự kiến, và không lập kế hoạch dựa trên giả định "khách đã đồng ý".

**Q649. 曖昧 (aimai – mơ hồ) trong yêu cầu của khách Nhật xử lý thế nào?**
Em coi làm rõ là việc của mình, không phải lỗi của khách. Cách làm: ① hỏi câu đóng hoặc đưa lựa chọn A/B thay vì hỏi mở; ② đưa ví dụ, mockup, dữ liệu mẫu để khách "chỉ vào" cái đúng; ③ hỏi giới hạn: số lượng, trường hợp ngoại lệ, ai dùng; ④ ghi phần đã chốt vào tài liệu và xin confirm. Những từ như 「いい感じに」 (ii kanji ni – làm sao cho hay), 「よしなに」 (yoshinani – tùy bên anh liệu) là tín hiệu phải hỏi lại ngay.

**Q650. 空気を読む (kuuki wo yomu – đọc bầu không khí) có ý nghĩa gì với PM vendor, có nên dựa vào nó?**
Là nhận ra điều không được nói ra: khách bỗng trả lời ngắn, cấp trên khách dự họp bất thường, một rủi ro bị hỏi đi hỏi lại — đều là tín hiệu lo ngại cần hành động sớm. Nhưng không nên chỉ dựa vào nó, vì khác biệt ngôn ngữ và văn hóa khiến đoán sai rất dễ. Em dùng "đọc không khí" để phát hiện, rồi xác nhận bằng câu hỏi trực tiếp, lịch sự và chốt bằng văn bản.
> 💡 Công thức dễ nhớ: "đọc để phát hiện, hỏi để xác nhận, viết để chốt".

**Q651. 本音 (honne – ý thật) và 建前 (tatemae – lời xã giao) ảnh hưởng gì đến việc thu thập phản hồi của khách?**
Trong họp chính thức, khách thường nói 建前: "không có vấn đề gì", "cảm ơn các bạn đã cố gắng". 本音 hay xuất hiện ở trao đổi 1-1, sau giờ họp hoặc qua người trung gian thân thiết. PM nên tạo kênh nghe 本音: gọi riêng 担当 sau mỗi mốc quan trọng, hỏi cụ thể "điểm nào cải thiện thì anh/chị làm việc dễ hơn", khảo sát định kỳ nếu khách đồng ý. Điểm đánh giá thấp bất ngờ cuối phase thường do đã bỏ qua 本音.

**Q652. Khách nói 「はい」 hoặc 「なるほど」 liên tục trong họp — có nghĩa là họ đồng ý?**
Không nhất thiết. 相槌 (aizuchi – tiếng đệm phản hồi) như はい, ええ, なるほど thường chỉ có nghĩa "tôi đang nghe", không phải "tôi đồng ý". Ngược lại, người Việt im lặng nghe có thể bị khách hiểu là chưa theo kịp. PM nên chốt bằng câu hỏi xác nhận rõ ràng như 「この方針で進めてよろしいでしょうか」 (tiến hành theo hướng này được không ạ), và khi nghe khách nói thì cũng đáp 相槌 để khách thấy được lắng nghe.

**Q653. Nhắc khách trả lời Q&A quá hạn thế nào để không gây áp lực?**
Dùng クッション言葉 (kusshon kotoba – từ đệm làm mềm) và nói tác động thay vì trách: 「お忙しいところ恐れ入りますが、QA管理表No.12について、11/20までにご回答いただけますと幸いです。ご回答が遅れる場合、結合テストの開始が遅れる可能性がございます。」 Nghĩa: xin lỗi làm phiền lúc bận, mong nhận trả lời trước 20/11; nếu chậm, 結合テスト (ketsugou tesuto – test tích hợp) có thể bắt đầu muộn. Kèm phương án đề xuất để khách chỉ cần trả lời "OK".

**Q654. 「承知しました」, 「了解しました」, 「かしこまりました」 dùng thế nào với khách?**
Với khách và cấp trên, an toàn nhất là 「承知いたしました」 hoặc 「かしこまりました」 (kashikomarimashita – xin vâng, tôi đã rõ; rất trang trọng). 「了解しました」 (ryoukai shimashita – đã hiểu) về nghĩa không sai, nhưng nhiều người Nhật coi là kém trang trọng khi nói với người trên, nên tránh dùng với khách. Trong chat ngắn với khách vẫn ưu tiên 「承知しました」. Những câu đáp nhỏ như vậy tạo ấn tượng chuyên nghiệp rất nhanh.

**Q655. Khi khách Nhật chọn giao tiếp bằng tiếng Anh, PM cần lưu ý gì?**
Dùng câu ngắn, từ đơn giản, tránh idiom, tiếng lóng; tránh câu hỏi phủ định ("Isn't it ready?") vì người Nhật trả lời Yes/No theo logic khác. Sau mỗi cuộc gọi, viết lại kết luận bằng văn bản, dùng số và ngày thay vì "soon", "ASAP". Nhiều người Nhật đọc tiếng Anh tốt hơn nghe, nên gửi tài liệu trước và chia sẻ màn hình khi họp.
> 💡 Với "Isn't it ready?", câu trả lời "Yes" của người Nhật có thể nghĩa là "đúng vậy, chưa xong".

## 7.6 Báo tin xấu & xin lỗi

**Q656. Nguyên tắc "bad news first" với khách Nhật là gì? Báo tin xấu theo cấu trúc nào?**
Tin xấu báo trước, báo sớm, kèm 対策 — không đợi có giải pháp hoàn hảo mới báo. Cấu trúc em dùng: ① sự việc (事象 – jishou) và thời điểm; ② phạm vi ảnh hưởng (影響範囲 – eikyou han'i); ③ nguyên nhân (đã xác định hay đang điều tra); ④ 暫定対策 (zantei taisaku – biện pháp tạm thời) đã/đang làm; ⑤ 恒久対策 (koukyuu taisaku – biện pháp lâu dài) dự kiến; ⑥ thời điểm báo cáo tiếp theo.
> 💡 Chưa rõ nguyên nhân thì nói "đang điều tra, sẽ báo lại lúc X giờ", tuyệt đối không phỏng đoán.

**Q657. Sự cố production xảy ra ngoài giờ — 第一報 (daiippou – báo cáo đầu tiên) gửi trong bao lâu và gồm gì?**
Theo SLA trong hợp đồng; nếu chưa quy định, em đặt chuẩn nội bộ khoảng 30–60 phút (tham khảo) từ lúc xác nhận sự cố mức cao, gọi điện cho đầu mối khẩn cấp rồi gửi email. Nội dung ngắn: hiện tượng, thời điểm phát hiện, phạm vi ảnh hưởng đã biết, việc đang làm, giờ báo tiếp (ví dụ mỗi 1–2 giờ). 第一報 cần nhanh hơn cần đầy đủ; 障害報告書 (shougai houkokusho – báo cáo sự cố) chi tiết làm sau.

**Q658. Cấu trúc một lời xin lỗi (お詫び – owabi) chuẩn với khách Nhật gồm những phần nào?**
① Xin lỗi rõ ràng ngay đầu: 「この度は多大なるご迷惑をおかけし、誠に申し訳ございません」 (lần này đã gây phiền hà lớn, thành thật xin lỗi); ② trình bày sự việc khách quan; ③ nguyên nhân, nhận trách nhiệm phía vendor; ④ 対策 đã làm và sẽ làm; ⑤ 再発防止策 (saihatsu boushi saku – biện pháp ngăn tái diễn) cụ thể, có người và ngày; ⑥ xin lỗi lại và mong tiếp tục được hợp tác. Thiếu ④⑤ thì lời xin lỗi bị xem là nói suông.

**Q659. Lỗi thực chất do một member bất cẩn — khi xin lỗi khách có nên nói rõ điều đó?**
Không. Với khách, đó là lỗi của công ty và của PM quản lý: em nói 「弊社の確認不足により」 (do phía chúng tôi kiểm tra chưa đủ), không nêu tên hay đổ cho cá nhân, càng không đổ cho khách. Đổ lỗi member khiến khách nghĩ vendor không kiểm soát được team và thiếu quy trình. Nguyên nhân gốc và bài học xử lý nội bộ; với khách chỉ trình bày lỗ hổng quy trình và 再発防止.
> 💡 Nói "tôi chịu trách nhiệm" trước, phân tích nguyên nhân sau — đó là điều interviewer muốn nghe.

**Q660. Lỗi một phần do khách (spec sai, duyệt chậm) — khi báo sự cố, PM nói thế nào để không đổ lỗi mà vẫn bảo vệ team?**
Em trình bày theo timeline fact, không phán xét: "ngày X nhận spec bản Y, ngày Z có thay đổi…", để sự thật tự nói. Phần lỗi của vendor (ví dụ không phát hiện mâu thuẫn sớm) thì nhận rõ. 再発防止 đề xuất cho cả hai bên dưới dạng "cùng cải thiện": chốt spec bằng văn bản, thêm bước 認識合わせ. Tác động chi phí/lịch nếu có thì xử lý qua kênh CR riêng sau khi sự cố ổn định, không trộn vào lời xin lỗi.

**Q661. Khi nào cần xin lỗi trực tiếp (gặp mặt, gọi điện), khi nào chỉ cần email?**
Lỗi nhỏ, không ảnh hưởng nghiệp vụ (sai sót tài liệu, trễ vài giờ có báo trước): email hoặc nói trong 定例. Lỗi ảnh hưởng nghiệp vụ, lịch release, hoặc lặp lại lần hai: gọi điện trước, email xác nhận sau, giải thích trong họp riêng. Sự cố nghiêm trọng (production dừng, dữ liệu sai, rò rỉ thông tin): xin lỗi trực tiếp, có thể đến văn phòng khách, kèm báo cáo bằng văn bản. Nguyên tắc: kênh xin lỗi phải "nặng" tương xứng với tác động.

**Q662. Khi nào lãnh đạo công ty vendor cần cùng xin lỗi khách?**
Khi tác động vượt quyền hạn của PM: sự cố gây thiệt hại kinh doanh hoặc ảnh hưởng người dùng cuối của khách, rò rỉ dữ liệu, cùng loại lỗi lặp lại, hoặc khách đã escalate lên 部長/役員 (yakuin – ban điều hành). Lãnh đạo tham gia thể hiện cam kết của tổ chức và bảo đảm nguồn lực cho 再発防止. PM chuẩn bị đủ fact, báo cáo, 対策 để lãnh đạo không phải xin lỗi suông, và chủ động đề xuất việc này thay vì đợi khách yêu cầu.

**Q663. 横展開 (yokotenkai – nhân rộng biện pháp sang chỗ tương tự) là gì, vì sao khách Nhật luôn hỏi?**
Sau khi sửa lỗi, khách sẽ hỏi: "chỗ khác có lỗi tương tự không?". 横展開 là rà các module, dự án có cùng nguyên nhân hoặc cùng pattern để sửa và áp dụng biện pháp phòng ngừa. Ví dụ: lỗi format ngày ở màn A thì kiểm mọi màn có xử lý ngày và bổ sung vào checklist review. Báo cáo sự cố thiếu 横展開 gần như chắc chắn bị khách trả lại yêu cầu bổ sung.
> 💡 Chủ động nêu 横展開 trước khi khách hỏi là cách nhanh nhất lấy lại niềm tin sau sự cố.

**Q664. Xin lỗi quá nhiều có phản tác dụng không? Có lúc nào không nên xin lỗi ngay?**
Có. Xin lỗi liên tục mà không có 対策 làm khách thấy vendor yếu; xin lỗi về nguyên nhân khi chưa rõ fact có thể bị hiểu là nhận trách nhiệm hợp đồng, trong khi lỗi có thể đến từ hệ thống bên thứ ba. Em tách hai việc: xin lỗi vì đã để khách lo lắng (「ご心配をおかけし申し訳ございません」) thì nói ngay; nhận trách nhiệm nguyên nhân thì sau khi xác nhận fact. Vấn đề có rủi ro bồi thường thì trao đổi với lãnh đạo và bộ phận pháp chế trước.

**Q665. Báo cáo "xanh" suốt 2 tháng rồi đột ngột chuyển "đỏ" — khách Nhật phản ứng thế nào, và tránh ra sao?**
Khách sẽ nghi ngờ toàn bộ báo cáo trước đó (「今まで何を報告していたのか」 – vậy trước giờ đã báo cáo cái gì), thường yêu cầu báo cáo hằng ngày và họp với lãnh đạo vendor. Tránh bằng cách định nghĩa tiêu chí màu đo được ngay từ đầu (tham khảo: 黄 khi lệch > 3 ngày hoặc dùng > 50% buffer) và dám chuyển 黄 sớm. 黄 sớm kèm 対策 là bình thường; nhảy thẳng 青 sang 赤 là dấu hiệu PM che giấu hoặc không đo.
> 💡 "Dự án dưa hấu" (ngoài xanh trong đỏ) là cụm hay gặp — gọi tên và nói cách phòng sẽ ghi điểm.

## 7.7 Nói "không" & đàm phán mềm

**Q666. Khách yêu cầu chức năng ngoài phạm vi ngay trong họp — PM từ chối thế nào mà vẫn giữ quan hệ?**
Không từ chối thẳng tại chỗ; em ghi nhận nhu cầu và nói 「貴重なご要望ありがとうございます。影響を確認の上、対応案をご提示させてください」 (cảm ơn đề xuất, xin phép đánh giá tác động rồi đưa phương án). Trong 1–2 ngày, em gửi lại: căn cứ phạm vi (tài liệu yêu cầu đã chốt), tác động nếu làm, và 2–3 代替案 (daitaian – phương án thay thế). Khách Nhật dễ chấp nhận "chưa làm được theo cách này nhưng có cách khác" hơn một chữ "không".

**Q667. 代替案 nên gồm những loại nào khi từ chối yêu cầu?**
Em thường đưa 3 loại: ① làm như yêu cầu nhưng dưới dạng thay đổi có báo giá và lịch riêng (CR); ② đổi chỗ — làm cái mới, lùi hoặc bỏ một hạng mục ưu tiên thấp hơn có quy mô tương đương; ③ chia giai đoạn — bản đơn giản trước, đầy đủ ở phase sau, hoặc workaround vận hành tạm. Mỗi phương án nêu rõ đánh đổi về lịch, chi phí, chất lượng, rủi ro; em nói khuyến nghị nhưng để khách chọn.
> 💡 Để khách "chọn" giữa các phương án giữ thể diện cho họ hơn là để họ "bị từ chối".

**Q668. Những mẫu câu tiếng Nhật lịch sự để báo không thể đáp ứng?**
「大変恐縮ですが、今回のスケジュールでは対応いたしかねます」 (rất ngại nhưng với lịch hiện tại chúng tôi khó đáp ứng); đuôi 「〜いたしかねます」 (itashikanemasu – khó có thể làm) là cách từ chối trang trọng; 「あいにく〜」 (ainiku – thật không may) để mở câu. Luôn nối bằng 「その代わりに、〜という方法はいかがでしょうか」 (thay vào đó, cách… thì sao ạ). Tránh 「できません」 trơn và 「無理です」 (muri desu – không thể) với khách vì quá thẳng.

**Q669. Khách đề nghị "làm thêm chút thôi, coi như サービス (saabisu – làm miễn phí)" — PM xử lý thế nào?**
Em đánh giá quy mô thật trước khi trả lời. Nếu rất nhỏ và có lợi cho quan hệ thì có thể nhận, nhưng phải 見える化: ghi vào danh sách hỗ trợ miễn phí kèm công sức và nói rõ đây là ngoại lệ. Nếu không nhỏ hoặc lặp lại, đưa về quy trình CR. Bẫy là nhận im lặng nhiều lần: khách coi đó là chuẩn, team quá tải, và đến lúc từ chối thì khách thấy vendor "đổi thái độ".
> 💡 "Miễn phí nhưng hiển thị giá trị" tạo cơ sở cho các lần đàm phán sau.

**Q670. 部長 khách đưa ra yêu cầu vô lý trước mặt nhiều người trong họp — PM nên phản ứng thế nào?**
Không phản bác công khai, vì làm 部長 mất mặt trước cấp dưới là sai lầm khó sửa. Em ghi nhận, hỏi làm rõ mục tiêu thật (「〜という目的でよろしいでしょうか」 – mục đích là… có đúng không ạ) và hẹn trả lời sau. Sau họp, em hỏi 担当 để hiểu bối cảnh, chuẩn bị phương án kèm dữ liệu tác động, 根回し với 担当 trước khi trình lại. Nhiều khi mục tiêu thật đạt được bằng cách đơn giản hơn yêu cầu ban đầu.

**Q671. Đàm phán với khách Nhật khác gì đàm phán "thắng–thua"? Tìm 落とし所 (otoshidokoro – điểm thỏa hiệp) thế nào?**
Khách Nhật coi trọng quan hệ dài hạn hơn thắng một ván, nên mục tiêu là 落とし所 mà hai bên đều giữ thể diện và giải thích được với nội bộ. Em chuẩn bị trước: mục tiêu, giới hạn tối thiểu, các "biến" có thể nhượng (thứ tự giao, phạm vi phase, mức hỗ trợ) và biến không nhượng (chất lượng, an toàn dữ liệu). Nhượng phải có đổi lại, không nhượng một chiều, và mọi thỏa thuận được ghi bằng văn bản.

**Q672. Khách yêu cầu rút ngắn deadline 2 tuần mà không thay đổi gì khác — PM trả lời ra sao?**
Em không nói "được" hay "không" ngay, mà xin thời gian đánh giá rồi đưa trade-off rõ: ① giữ phạm vi, thêm người — chi phí tăng, rủi ro onboarding; ② giữ đội, giảm phạm vi — liệt kê chức năng lùi sang đợt sau; ③ release từng phần, chức năng quan trọng nhất trước. Đồng thời hỏi lý do thật của việc rút ngắn (sự kiện kinh doanh, 年度末 – nendomatsu – cuối năm tài chính…), vì đó thường là chìa khóa tìm phương án.

**Q673. Khi nào PM phải nói "không" dứt khoát với khách Nhật, kể cả có thể làm khách phật ý?**
Khi yêu cầu vi phạm pháp luật, hợp đồng, bảo mật (ví dụ đưa dữ liệu thật của khách tài chính ra môi trường test không được phép), an toàn hệ thống, hoặc buộc team cam kết điều chắc chắn không làm được. Lúc đó em vẫn nói lịch sự nhưng rõ ràng, tránh cách nói mập mờ dễ bị hiểu là "sẽ xem xét", nêu lý do và đề xuất cách hợp lệ thay thế. Một lần "không" rõ ràng tốt hơn nhiều so với "vâng" rồi thất hứa.
> 💡 Ví dụ về dữ liệu thật và bảo mật rất thuyết phục với khách tài chính, bảo hiểm.

**Q674. Sau khi từ chối một yêu cầu, làm sao biết quan hệ với khách không bị ảnh hưởng?**
Em theo dõi tín hiệu: tốc độ trả lời email, giọng điệu trong họp, khách có còn chia sẻ kế hoạch sắp tới không. Chủ động gọi 担当 sau 1–2 ngày, hỏi phương án thay thế có phù hợp với nội bộ họ không, cần hỗ trợ gì để giải thích với cấp trên. Đồng thời làm thật tốt phần đã cam kết, để khách thấy việc từ chối là vì chất lượng, không phải vì thiếu thiện chí.

## 7.8 Lịch & nhịp kinh doanh Nhật

**Q675. 年度 (nendo – năm tài chính) của doanh nghiệp Nhật thường bắt đầu khi nào và ảnh hưởng gì đến dự án?**
Cơ quan nhà nước và nhiều doanh nghiệp Nhật dùng năm tài chính từ 1/4 đến 31/3 năm sau, chia thành 上期 (kamiki – nửa đầu, tháng 4–9) và 下期 (shimoki – nửa sau, tháng 10–3). Ngân sách IT thường được lên trong năm tài chính trước, nên dự án mới hay bắt đầu tháng 4 hoặc tháng 10, đề xuất phải đến trước khi khách chốt ngân sách, và cuối năm dồn việc nghiệm thu. Một số công ty dùng năm tài chính khác, nên em luôn hỏi lại từng khách.

**Q676. Vì sao tháng 3 (年度末) thường là giai đoạn căng nhất với khách Nhật?**
Vì khách cần hoàn tất nghiệm thu, dùng ngân sách năm, và nhiều hệ thống, quy định, nghiệp vụ mới áp dụng từ 1/4. Hệ quả: release dồn, thay đổi phút chót, khách bận nên trả lời chậm. Em lập kế hoạch ngược từ tháng 3: chốt spec sớm, đặt code freeze trước vài tuần, chuẩn bị người hỗ trợ UAT, và đẩy các việc không bắt buộc ra khỏi cuối tháng 3.
> 💡 Hỏi khách ngay từ kickoff "có mốc 年度末 nào cố định không?" — đó thường là deadline thật.

**Q677. Tháng 4 có rủi ro giao tiếp nào PM cần chuẩn bị?**
Tháng 4 là mùa 人事異動 (jinji idou – điều chuyển nhân sự) và nhân viên mới vào ở nhiều công ty Nhật, nên 担当 hoặc quản lý phía khách có thể đổi người. Người mới không biết bối cảnh và các thỏa thuận cũ. Em chuẩn bị: tài liệu tóm tắt cho người mới (lịch sử quyết định, thỏa thuận về scope, Q&A quan trọng), đề xuất buổi chào hỏi và giới thiệu dự án, xác nhận lại 窓口 và 決裁者.

**Q678. Golden Week, お盆 (obon) và 年末年始 (nenmatsu nenshi) ảnh hưởng thế nào đến kế hoạch dự án offshore?**
Golden Week rơi khoảng cuối tháng 4 đầu tháng 5, お盆 (dịp lễ về quê) khoảng giữa tháng 8, 年末年始 (nghỉ cuối năm–đầu năm) khoảng cuối tháng 12 đến đầu tháng 1; ngày nghỉ cụ thể tùy công ty. Trong các dịp này khách gần như không duyệt, không trả lời Q&A, không làm UAT. Em đưa lịch nghỉ của khách vào kế hoạch từ đầu, tránh đặt release hay mốc cần khách duyệt sát kỳ nghỉ, và thống nhất ai trực khi có sự cố.

**Q679. Lịch nghỉ Việt Nam và lịch Nhật lệch nhau — PM xử lý thế nào?**
Tết Nguyên Đán thường rơi vào tháng 1–2, lúc khách Nhật làm việc bình thường và đang chuẩn bị cho 年度末, nên đây là rủi ro lớn nhất. Em gửi lịch nghỉ cho khách từ đầu năm, hoàn thành các mốc quan trọng trước Tết, bố trí trực luân phiên cho bảo trì/sự cố, và xác nhận bằng văn bản phạm vi hỗ trợ trong dịp nghỉ. Nghỉ 30/4–1/5 và 2/9 của Việt Nam không trùng hẳn với ngày nghỉ của khách, cần đối chiếu từng năm.
> 💡 Báo lịch nghỉ Tết sớm 2–3 tháng (tham khảo) kèm kế hoạch trực cho thấy PM hiểu rủi ro của khách.

**Q680. Lệch múi giờ VN–JP 2 tiếng ảnh hưởng thế nào đến nhịp làm việc?**
Giờ Nhật nhanh hơn Việt Nam 2 tiếng (Nhật không dùng giờ mùa hè): 9:00 Nhật là 7:00 Việt Nam, và khi team VN làm đến 17:00 thì bên Nhật đã 19:00. Em đặt họp ở khung chung, ví dụ 10:00–12:00 hoặc 15:00–17:00 giờ Nhật (8:00–10:00 hoặc 13:00–15:00 giờ VN); báo cáo ngày gửi trước 15:00 giờ VN để khách đọc trong giờ làm; câu hỏi cần trả lời trong ngày gửi từ buổi sáng.
> 💡 Giờ nghỉ trưa Nhật 12:00–13:00 là 10:00–11:00 giờ VN — tránh hẹn họp vào khung đó.

**Q681. Kế hoạch nguồn lực của PM nên điều chỉnh theo nhịp năm của khách Nhật thế nào?**
Em vẽ "bản đồ nhịp năm" của khách: tháng 1–3 cao điểm (年度末, nghiệm thu, Tết VN chen giữa), tháng 4 đổi người và dự án mới khởi động, Golden Week, お盆, 年末年始 là các khoảng khách vắng. Từ đó: giữ buffer người cho quý 1 dương lịch, xếp đào tạo và nghỉ phép của team vào lúc khách nghỉ, chuẩn bị nhân sự cho dự án mới từ tháng 2–3 để khởi động được ngay tháng 4.

**Q682. 年末年始 có nghi thức giao tiếp nào PM nên biết?**
Cuối năm, email chào 「本年も大変お世話になりました。来年もどうぞよろしくお願いいたします」 (cảm ơn sự giúp đỡ năm nay, mong năm sau tiếp tục hợp tác), kèm lịch nghỉ và đầu mối khẩn cấp. Ngày làm việc đầu năm, gửi lời chúc 「新年あけましておめでとうございます。本年もよろしくお願いいたします」 (chúc mừng năm mới, năm nay mong tiếp tục được giúp đỡ). Một số công ty còn gửi 年賀状 (nengajou – thiệp chúc năm mới), tùy mức độ quan hệ với khách.

**Q683. Có nên release ngay trước kỳ nghỉ dài của Nhật để "kịp" deadline?**
Em hạn chế tối đa. Nếu có sự cố sau release, người duyệt và người vận hành phía khách vắng mặt, xử lý chậm, rủi ro bị đẩy lên rất cao. Nếu buộc phải release, em thống nhất trước bằng văn bản: danh sách người trực hai bên, kênh liên lạc khẩn, tiêu chí rollback, thời gian theo dõi; tốt nhất để ít nhất 2–3 ngày làm việc giữa release và kỳ nghỉ (tham khảo).

## 7.9 Xây niềm tin & quản trị kỳ vọng

**Q684. 信頼関係 (shinrai kankei – quan hệ tin cậy) với khách Nhật được xây dựng như thế nào?**
Bằng tích lũy nhất quán những lời hứa nhỏ được giữ: biên bản gửi đúng 24 giờ, câu trả lời đúng hạn hẹn, con số trong mọi báo cáo khớp nhau, vấn đề báo sớm. Người Nhật đánh giá đối tác qua thời gian dài và không dễ cho "cơ hội thứ hai". Em coi 約束を守る (yakusoku wo mamoru – giữ lời hứa) là KPI: theo dõi tỉ lệ cam kết đúng hạn (trả lời Q&A, giao hàng) và không để trễ nào xảy ra mà không báo trước.
> 💡 "Niềm tin = số lời hứa nhỏ được giữ" ngắn gọn, dễ nhớ với interviewer.

**Q685. Under-promise, over-deliver áp dụng với khách Nhật thế nào? Có rủi ro gì?**
Cam kết ở mức team chắc chắn đạt (buffer hợp lý, ví dụ 10–15% — tham khảo), rồi giao đúng hoặc sớm hơn, chất lượng tốt hơn kỳ vọng. Rủi ro: buffer quá dày, khách thấy "lúc nào cũng xong sớm" thì mất tin vào estimate hoặc cho rằng vendor thiếu tham vọng. Em giữ buffer minh bạch ở mức dự án, không giấu trong từng task; xong sớm thì dùng thời gian dư cho chất lượng hoặc đề xuất cải tiến.

**Q686. Biết chắc không giữ được lời hứa, PM nên báo khách khi nào?**
Ngay khi biết, trước hạn — không bao giờ đợi đến đúng ngày hạn mới báo. Em báo kèm ngày mới chắc chắn hơn, lý do, và phần nào có thể giao trước. Với người Nhật, 期限前の相談 (kigen mae no soudan – bàn trước khi đến hạn) thể hiện trách nhiệm, còn trễ hạn không báo là vi phạm 約束. Ngày mới phải là ngày giữ được chắc chắn, vì trễ hai lần liên tiếp gây mất niềm tin nặng hơn nhiều so với một lần.

**Q687. Khách mới và khách lâu năm — quản trị kỳ vọng khác nhau thế nào?**
Khách mới chưa có niềm tin: em tăng tần suất báo cáo, giao từng phần nhỏ sớm (prototype, pilot), giải thích quy trình và tiêu chuẩn của vendor, chốt định nghĩa "xong" từ đầu. Khách lâu năm có sẵn niềm tin, nhưng rủi ro là 慣れ (nare – quen nên lơ là): chất lượng giảm dần, báo cáo sơ sài, kỳ vọng ngầm tăng lên. Với họ, em giữ tiêu chuẩn như ngày đầu và chủ động đưa 改善提案 (kaizen teian – đề xuất cải tiến) định kỳ.

**Q688. Khách là bộ phận IT và khách là business user — giao tiếp khác nhau thế nào?**
情報システム部 (jouhou shisutemu bu – phòng hệ thống thông tin) quan tâm kiến trúc, chuẩn kỹ thuật, bảo mật, tài liệu và vận hành sau go-live; có thể nói bằng thuật ngữ kỹ thuật. Business user quan tâm nghiệp vụ, thao tác, ngày áp dụng, ảnh hưởng đến công việc hằng ngày; cần ngôn ngữ nghiệp vụ, demo trực quan, tránh jargon. Khi cả hai cùng dự họp, em chia phần báo cáo theo người nghe và kiểm tra kỳ vọng của từng nhóm riêng.

**Q689. Kỳ vọng "chất lượng không lỗi" của khách Nhật — PM quản trị thế nào cho thực tế?**
Em không hứa "zero bug" chung chung mà thống nhất từ đầu tiêu chí đo được: mức lỗi nào chấp nhận ở từng giai đoạn, tiêu chí nghiệm thu, phạm vi test. Đồng thời cho khách thấy quy trình đảm bảo chất lượng qua 見える化, vì với người Nhật, quy trình đáng tin quan trọng không kém kết quả. Khi có lỗi, cách xử lý nhanh, minh bạch và có 再発防止 chính là thứ giữ được kỳ vọng.

**Q690. Làm sao phát hiện sớm khoảng cách kỳ vọng trước khi thành bất mãn?**
Em dùng 3 nguồn: ① demo sớm và định kỳ (ví dụ cuối mỗi sprint hoặc 2 tuần/lần) để khách thấy sản phẩm thật, không chỉ đọc báo cáo; ② sau mỗi mốc hỏi thẳng 「ご期待と違う点はございますか」 (có điểm nào khác với mong đợi không ạ); ③ khảo sát hài lòng ngắn mỗi phase (3–5 câu, có điểm số) nếu khách đồng ý. Khoảng cách nào lộ ra thì ghi thành 課題 có hành động cụ thể, không "chờ xem".

**Q691. Khách mất niềm tin sau một chuỗi sự cố — PM khôi phục thế nào?**
① Thừa nhận thẳng thắn, không biện hộ, có lãnh đạo vendor tham gia; ② đưa kế hoạch khôi phục có mốc (ví dụ 4–8 tuần): tăng cường review, bổ sung người chủ chốt, báo cáo dày hơn; ③ 見える化 toàn bộ để khách tự kiểm chứng thay vì yêu cầu khách "tin lại"; ④ giao liên tục các kết quả nhỏ đúng hẹn. Khi chỉ số ổn định, chủ động đề xuất giảm dần tần suất báo cáo. Niềm tin quay lại bằng hành vi lặp lại, không bằng lời hứa.

**Q692. Khách Nhật khen 「よくやってくれています」 — PM có nên yên tâm?**
Không hẳn. Lời khen (các bạn làm tốt lắm) trong họp có thể là 建前; khách Nhật hiếm khi phàn nàn trực tiếp mà thể hiện bằng hành động như không gia hạn hợp đồng hoặc giao việc mới cho vendor khác. Em kiểm chứng bằng tín hiệu khách quan: khách có giao thêm việc, chia sẻ kế hoạch năm sau, mời tham gia sớm dự án mới không; và hỏi riêng 担当 điểm cần cải thiện. Không có góp ý không có nghĩa là không có vấn đề.
> 💡 Bẫy: coi lời khen xã giao là đánh giá thật rồi ngừng cải tiến.

## 7.10 Business etiquette & khác biệt thị trường

**Q693. 名刺交換 (meishi koukan – trao danh thiếp) đúng cách gồm những bước nào?**
Đứng dậy, đưa danh thiếp bằng hai tay, mặt chữ hướng về người nhận, vừa đưa vừa nói tên công ty và họ tên; bên đến thăm hoặc người vị trí thấp hơn đưa trước. Nhận bằng hai tay, đọc tên và nói 「頂戴いたします」 (choudai itashimasu – xin nhận ạ). Trong họp, đặt danh thiếp trên bàn theo thứ tự chỗ ngồi, danh thiếp người cấp cao nhất đặt trên hộp danh thiếp. Không viết lên, không nhét túi quần, không để quên trên bàn.

**Q694. Khi đến thăm văn phòng khách Nhật, cần lưu ý gì về giờ giấc và chỗ ngồi?**
Có mặt ở tòa nhà sớm khoảng 10 phút nhưng chỉ báo lễ tân khoảng 5 phút trước giờ hẹn, vì đến quá sớm cũng làm khách bận. Mùa lạnh, cởi áo khoác trước khi vào tòa nhà. Trong phòng họp, chờ được mời mới ngồi; nếu không được chỉ chỗ, ngồi phía gần cửa (下座 – shimoza) và để 上座 (kamiza – chỗ danh dự, xa cửa) cho người cấp cao. Đồ uống được mời thì chờ chủ nhà mời mới dùng. Sau buổi gặp, gửi email cảm ơn trong ngày.

**Q695. Dress code khi làm việc với khách Nhật cần lưu ý gì?**
Mặc định là trang phục công sở chỉnh tề, màu trung tính (vest tối màu, sơ mi trắng hoặc sáng, giày sạch), đặc biệt với khách tài chính, bảo hiểm vốn bảo thủ. Mùa hè nhiều công ty áp dụng クールビズ (kuuru bizu – không cà vạt, trang phục mát), em hỏi trước hoặc theo cách khách mặc. Buổi gặp đầu tiên, buổi xin lỗi hay buổi có lãnh đạo thì luôn chọn trang trọng hơn. Họp online cũng giữ chuẩn tối thiểu: áo sơ mi, nền gọn gàng.

**Q696. 飲み会 (nomikai – tiệc rượu) và 接待 (settai – tiếp khách) với khách Nhật cần biết gì?**
Chờ 乾杯 (kanpai – nâng ly chung) rồi mới uống; để ý ly của người khác, rót cho khách và cấp trên. Dù không khí thoải mái, không nói xấu ai, không cam kết công việc khi đã uống. Không uống được thì từ chối lịch sự, dùng đồ uống không cồn. Với khách tài chính, bảo hiểm, nhiều nơi có quy định compliance về tiếp khách và quà tặng — em hỏi trước để không đặt khách vào thế khó.
> 💡 Bẫy 無礼講 (bureikou – "hôm nay bỏ qua lễ nghi"): câu này không có nghĩa được thất lễ thật.

**Q697. お土産 (omiyage – quà mang theo) khi sang Nhật thăm khách nên chọn thế nào?**
Chọn đặc sản Việt Nam hoặc Đà Nẵng (cà phê, bánh kẹo đặc sản…), đóng gói từng phần nhỏ (個包装 – kohousou) để khách chia cho cả phòng, giá trị vừa phải để không gây áp lực. Đưa sau phần chào hỏi, kèm câu 「ささやかなものですが、皆様で召し上がってください」 (chút quà nhỏ, mời mọi người cùng dùng). Kiểm tra trước khách có quy định từ chối quà không, nhất là ngành tài chính.

**Q698. Đúng giờ với khách Nhật quan trọng thế nào? Nếu sắp trễ phải làm gì?**
Rất quan trọng: đúng giờ được xem là thước đo đầu tiên của sự tin cậy, kể cả với họp online. Nếu biết có thể trễ, em liên lạc trước giờ hẹn (gọi điện hoặc nhắn), xin lỗi, báo thời gian đến dự kiến và đề nghị khách bắt đầu trước nếu phù hợp. Đến nơi thì xin lỗi ngắn gọn rồi vào việc ngay, không giải thích dài dòng. Hạn gửi tài liệu cũng vậy: nếu sẽ trễ dù chỉ 1 giờ, phải báo trước khi đến hạn.

**Q699. Khách Nhật, Hàn, Singapore khác nhau thế nào trong giao tiếp dự án (nói ngắn)?**
Đây là xu hướng thường gặp, không đúng với mọi khách. Nhật: quyết định qua đồng thuận, coi trọng quy trình, tài liệu, chất lượng và báo cáo sớm, nói gián tiếp. Hàn: ưu tiên tốc độ, quyết định thường từ cấp trên và nhanh hơn, yêu cầu thay đổi nhiều, phản hồi thẳng. Singapore: giao tiếp bằng tiếng Anh, thẳng và thực dụng, tập trung hợp đồng, KPI, chi phí, ít nặng thứ bậc. PM giữ một bộ quy trình lõi, chỉnh tần suất, kênh và cách nói theo từng khách.
> 💡 Nói "xu hướng" và kết bằng "em quan sát từng khách cụ thể" để tránh bị đánh giá là rập khuôn.

**Q700. Khách Nhật sang thăm văn phòng Đà Nẵng — PM chuẩn bị đón tiếp thế nào?**
Em chuẩn bị như một mốc dự án: agenda gửi trước (giới thiệu công ty, demo, gặp team, họp các vấn đề chính), slide tiếng Nhật, đưa đón nếu phù hợp, phòng họp có bảng tên, đủ danh thiếp, sắp chỗ theo 上座. Cho khách gặp trực tiếp member chủ chốt, xem môi trường làm việc và biện pháp bảo mật — mối quan tâm lớn của khách tài chính. Sau chuyến thăm, gửi email cảm ơn, biên bản và danh sách việc tiếp theo trong 1–2 ngày.
> 💡 Chuyến thăm là cơ hội tốt để 根回し trực tiếp các quyết định lớn với cấp quản lý khách.
