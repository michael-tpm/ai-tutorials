# Chương 6 · Theo dõi và báo cáo tình trạng dự án (Q626–Q750)

## 6.1 Thiết kế hệ thống báo cáo

**Q626. Dự án migration hệ thống quản lý hợp đồng cho khách bảo hiểm nhân thọ B (team 25 người, hợp đồng trọn gói, 10 tháng) kick-off tuần sau, khách chưa nêu yêu cầu báo cáo nào. Việc đầu tiên khi thiết kế hệ thống báo cáo là gì?**
Việc đầu tiên là **phân tích nhu cầu thông tin của từng stakeholder**, chưa phải làm template. ① Liệt kê người nhận: đầu mối liên lạc và trưởng phòng phía khách, PMO khách, lãnh đạo nội bộ, team. ② Hỏi mỗi người cần biết gì để ra quyết định gì, vào lúc nào. ③ Lập ma trận "ai nhận gì · tần suất · kênh · định dạng · người soạn": ví dụ báo cáo tuần qua họp định kỳ, báo cáo tháng cho trưởng phòng, dashboard nội bộ hằng tuần. ④ Chốt giờ cut-off số liệu, nguồn số, người duyệt; ghi vào kế hoạch và cho khách xác nhận trong biên bản họp. Bẫy: copy nguyên template dự án cũ.
> 📘 PMP: Plan Communications Management: communication requirements analysis → communications management plan (ai, nhận gì, khi nào, kênh nào, ai chịu trách nhiệm).
> 💡 Nhật: Nhiều khách Nhật đã có mẫu báo cáo tiến độ riêng; hỏi xin trước để dùng đúng mẫu, tránh phải làm hai bản.

**Q627. Dự án trọn gói với ngân hàng A, team 30 người: lãnh đạo nội bộ và khách đều muốn nhận báo cáo tuần. Nội dung hai báo cáo nên giống và khác nhau ở điểm nào?**
Nguyên tắc: **cùng một bộ số tiến độ, chất lượng, rủi ro; khác ở lớp thông tin bổ sung**. Báo cáo khách: kế hoạch – thực tế tiến độ, mốc, chất lượng, rủi ro/issue ảnh hưởng khách, việc khách cần làm hoặc quyết định. Báo cáo nội bộ: toàn bộ phần trên + effort thực tế so ngân sách, dự báo lợi nhuận gộp, nhân sự, CR chưa ký, lịch nghiệm thu và thu tiền. Với hợp đồng trọn gói, chi phí và lãi lỗ là thông tin nội bộ, không cần đưa khách; nhưng tình trạng tiến độ gửi hai bên phải giống hệt. Bẫy: hai bản RAG khác màu cho cùng một tuần.
> 📘 PMP: Plan Communications Management + phân tích stakeholder (power/interest grid): điều chỉnh nội dung theo người nhận nhưng dùng chung một nguồn work performance information.
> 💡 Nhật: Với hợp đồng theo công sức, công số lại là căn cứ thanh toán nên phải báo khách; đừng áp nguyên cách làm của hợp đồng trọn gói.

**Q628. Khách phi nhân thọ C yêu cầu thêm báo cáo ngày trong giai đoạn kiểm thử tích hợp, PM và BrSE mất khoảng 1,5 giờ mỗi ngày để tổng hợp. Anh/chị xử lý thế nào?**
① Xác nhận mục đích: khách lo điều gì (bug tăng? sợ trễ?) — yêu cầu tăng tần suất thường là dấu hiệu khách thiếu tin tưởng. ② Đề xuất phương án nhẹ hơn mà vẫn đáp ứng: dashboard cập nhật tự động hằng ngày từ tool test/bug của IT gồm case thực hiện/đạt, bug mở/đóng, cộng báo cáo ngày 5 dòng cấp PM (vấn đề mới, việc cần khách). ③ Nêu chi phí: 1,5 giờ × 20 ngày = 30 giờ/tháng; với hợp đồng theo công sức là giờ tính tiền, với hợp đồng trọn gói là chi phí nội bộ. ④ Thử 2 tuần rồi cùng khách đánh giá; khi khách chưa đồng ý thì vẫn gửi báo cáo ngày như yêu cầu.
> 📘 PMP: Monitor Communications: đánh giá hiệu quả truyền thông; muốn đổi thì cập nhật communications management plan theo quy trình đã thống nhất.

**Q629. Báo cáo tuần của team 18 người hay bị khách hỏi "số này lấy ở đâu" vì cùng một chỉ số mà slide và file Excel đính kèm lệch nhau. Thiết lập nguồn số liệu thế nào?**
Áp dụng **một nguồn sự thật cho mỗi loại số**: tiến độ từ WBS/schedule tool, effort từ timesheet đã duyệt, bug/test từ bug tracker, vấn đề từ bảng quản lý vấn đề. Quy định giờ cut-off (ví dụ thứ Sáu 12:00), chủ sở hữu từng nguồn, định nghĩa cách tính (tiến độ đo theo gì, bug tính từ trạng thái nào). Xuất số tự động hoặc qua một file tổng hợp có công thức khóa; slide chỉ lấy từ file đó và ghi "số liệu tính đến ngày…". Lưu bản báo cáo đã gửi để đối chiếu khi bị hỏi. Bẫy: copy tay từ nhiều file sang PowerPoint, mỗi lần sửa một chỗ.
> 📘 PMP: Work performance data → work performance information → work performance reports (Monitor and Control Project Work); định nghĩa số đo ghi trong kế hoạch.

**Q630. Team 15 người ở Hà Nội và 2 BrSE onsite Tokyo; báo cáo tuần do BrSE onsite tự viết bằng tiếng Nhật từ tin nhắn chat rời rạc nên hay sai số. Thiết kế lại luồng báo cáo thế nào?**
Tách rõ **nội dung** và **ngôn ngữ**. Luồng: thứ Năm leader từng nhóm cập nhật WBS/bug tool → sáng thứ Sáu PM tại VN tổng hợp, kiểm tra chéo số liệu → BrSE dịch, chuẩn hóa thuật ngữ, không đổi số và mức độ → PM duyệt bản cuối → gửi đầu mối liên lạc trước họp định kỳ. Lập RACI cho từng bước: PM chịu trách nhiệm nội dung, BrSE chịu trách nhiệm ngôn ngữ. Template song ngữ, phần số lấy tự động. Bẫy: BrSE "làm mềm" tin xấu khi dịch, ví dụ "trễ 5 ngày" thành "hơi trễ"; PM phải đọc lại các câu về trễ và lỗi.
> 📘 PMP: RACI chart + Manage Communications: quy định rõ người soạn, người duyệt, người gửi.
> 💡 Nhật: Gửi tài liệu trước họp định kỳ ít nhất 1 ngày làm việc (tham khảo) để khách đọc trước; giờ họp dành cho điểm cần thảo luận và quyết định.

**Q631. Giám đốc khối phụ trách 12 dự án phàn nàn báo cáo tuần của PM dài 20 slide, đọc không ra vấn đề. Anh/chị thiết kế lại thế nào?**
Làm **1 trang tóm tắt** theo mẫu chung cả khối để so sánh được các dự án: ① RAG tổng + 4 trục (tiến độ, effort/chi phí, chất lượng, rủi ro), mỗi trục 1 số chính và mũi tên xu hướng so tuần trước. ② Top 3 vấn đề/rủi ro. ③ Mục "cần lãnh đạo quyết định/hỗ trợ gì, trước ngày nào". ④ Dự báo mốc kế tiếp và lợi nhuận. Chi tiết chuyển sang phụ lục. Viết theo nói kết luận trước. Bẫy: rút gọn nhưng cắt mất tin xấu; bản tóm tắt phải giữ nguyên vấn đề lớn nhất của tuần.
> 📘 PMP: Manage Communications – tailoring theo người nhận; dashboard/information radiator (Measurement performance domain, PMBOK 7).

**Q632. Dự án ngân hàng A làm trong mạng đóng của khách, bug tracker nằm trong môi trường khách và không được xuất dữ liệu ra ngoài; lãnh đạo nội bộ muốn dashboard chất lượng hằng tuần. Xử lý thế nào?**
① Xác nhận quy định bảo mật của mạng đóng: được mang gì ra, qua kênh nào, ai duyệt. ② Đề xuất bằng văn bản với khách: chỉ xuất **số tổng hợp** (đếm bug theo mức, module, trạng thái), không có nội dung ticket, dữ liệu khách hay ảnh màn hình, qua kênh đã phê duyệt. ③ Khách đồng ý thì lập mẫu cố định để mỗi lần xuất giống nhau; khách không đồng ý thì lãnh đạo nhận báo cáo miệng hoặc bản tóm tắt PM soạn từ số đã được phép. ④ Ghi ràng buộc vào communication plan. Tuyệt đối không tự chụp màn hình gửi ra ngoài.
> 📘 PMP: Plan Communications Management: ràng buộc bảo mật là đầu vào khi thiết kế kênh; stewardship (PMBOK 7).
> 💡 Nhật: Ngành tài chính Nhật áp dụng các chuẩn an toàn như FISC; xin phép bằng văn bản cho mọi luồng dữ liệu ra ngoài, kể cả số tổng hợp.

**Q633. Thành viên mới hỏi: trong dự án khách Nhật, khi nào dùng báo cáo định kỳ, khi nào phải liên lạc ngay? Anh/chị giải thích và thiết kế kênh theo nguyên tắc báo cáo – liên lạc – thảo luận thế nào?**
Báo cáo – liên lạc – trao đổi gồm báo cáo – báo kết quả/tình trạng (định kỳ hoặc khi xong việc), liên lạc – báo ngay sự kiện cho người liên quan (môi trường down, người nghỉ, đổi lịch), trao đổi – xin ý kiến khi chưa tự quyết được. Thiết kế 3 kênh: định kỳ (báo cáo tuần + họp định kỳ), ad-hoc trong ngày (email/chat cho liên lạc), escalation (gọi điện/họp khẩn cho trao đổi vấn đề lớn). Ghi **ngưỡng kích hoạt**: ví dụ ảnh hưởng mốc > 2 ngày hoặc bug mức cao thì báo trong ngày (tham khảo). Bẫy: giữ việc gấp chờ đến họp định kỳ mới nói.
> 📘 PMP: Phương pháp truyền thông push/pull/interactive và escalation path trong communications management plan.

**Q634. Khách sản xuất D chỉ muốn nhận báo cáo qua email, không họp; sau 2 tháng PM phát hiện khách không đọc kỹ, 6 câu hỏi cần khách quyết định bị treo hơn 3 tuần. Làm gì?**
Push communication không bảo đảm người nhận hiểu và hành động. ① Xác nhận fact: liệt kê 6 câu, ngày gửi, việc nào đang bị chặn. ② Gọi trực tiếp đầu mối liên lạc để xử lý ngay các câu chặn critical path. ③ Đề xuất thêm kênh tương tác ngắn: họp 30 phút hai tuần một lần chỉ cho phần cần quyết định; email tách riêng mục "cần trả lời" với hạn cụ thể. ④ Thêm chỉ số "số câu chờ khách quá 5 ngày" vào báo cáo để khách thấy ảnh hưởng. Bẫy: coi "đã gửi email" là đã thông báo xong trách nhiệm.
> 📘 PMP: Monitor Communications: kiểm tra truyền thông có đạt hiệu quả không, chuyển từ push sang interactive khi cần.
> 💡 Nhật: Tiêu đề email có [Cần trả lời] [Nhờ xác nhận] và hạn trả lời giúp khách Nhật xếp ưu tiên giữa rất nhiều mail mỗi ngày.

**Q635. Dự án theo công sức với khách bảo hiểm B, team 12 người; hợp đồng quy định báo cáo công số hằng tháng làm căn cứ thanh toán. Thiết kế báo cáo effort thế nào?**
Báo cáo effort thực tế tháng gồm: giờ theo từng người/vai trò, so với khoảng giờ quyết toán, giờ làm thêm, tóm tắt công việc đã làm. Nguồn: timesheet leader duyệt hằng tuần, đối chiếu chấm công vào ra. Gửi dự báo giữa tháng nếu có người sắp vượt hoặc thiếu khoảng giờ. Khách xác nhận trước ngày nghiệm thu. Bẫy: giờ báo cáo không khớp chấm công; tính giờ làm thêm khách chưa đồng ý; ghi cả giờ đào tạo nội bộ vào giờ tính tiền.
> 📘 PMP: Control Costs + Manage Communications: báo cáo phải đáp ứng điều khoản hợp đồng (agreements) về căn cứ thanh toán.

**Q636. Khách bảo hiểm B đề nghị được cấp quyền xem trực tiếp Redmine nội bộ của team (task, bug, comment) để tự theo dõi, đỡ phải chờ báo cáo. Anh/chị trả lời thế nào?**
Minh bạch là tốt nhưng dữ liệu thô dễ bị hiểu sai. ① Xác nhận mục đích của khách: muốn thấy gì, ai xem. ② Có thể đồng ý với điều kiện: quyền read-only đúng phạm vi dự án, giải thích định nghĩa từng trạng thái, ghi rõ "số liệu chính thức là báo cáo tuần". ③ Dọn trước: không để trên tool comment nội bộ, đánh giá cá nhân, chi phí, dữ liệu dự án khác. ④ Thống nhất: thắc mắc từ tool gửi qua đầu mối liên lạc, không chỉ đạo trực tiếp từng dev. Xin ý kiến lãnh đạo nội bộ trước khi cấp quyền.
> 📘 PMP: Pull communication trong Manage Communications + Manage Stakeholder Engagement: cân bằng minh bạch và rủi ro hiểu sai dữ liệu.
> 💡 Nhật: Với cả hợp đồng trọn gói và hợp đồng theo công sức, khách chỉ đạo trực tiếp từng dev có thể bị coi là trọn gói trá hình; giữ kênh qua PM/BrSE.

**Q637. Chương trình migration 60 người gồm 3 sub-team (BE, FE, chuyển đổi dữ liệu) và một vendor hạ tầng do khách thuê trực tiếp. Anh/chị tổng hợp báo cáo tình trạng chung thế nào?**
① Một template và một giờ cut-off cho mọi bên; vendor hạ tầng gửi số qua PMO khách. ② Lịch tổng (integrated master schedule) có các **điểm giao** (môi trường, API, dữ liệu mẫu) với ngày cần và người chịu trách nhiệm. ③ RAG theo từng thành phần, RAG tổng theo nguyên tắc "hạng mục critical xấu nhất", không lấy trung bình. ④ Họp phụ thuộc định kỳ giữa các bên; điểm giao trễ được báo như rủi ro của toàn chương trình. Bẫy: từng bên báo xanh riêng nhưng điểm giao giữa họ đỏ, đến lúc tích hợp mới lộ.
> 📘 PMP: Monitor and Control Project Work ở cấp tích hợp; systems thinking (PMBOK 7) – nhìn tương tác giữa các thành phần.
> 💡 Nhật: PM phía VN không có quyền chỉ đạo vendor do khách thuê; mọi yêu cầu với họ phải qua PMO khách và ghi vào biên bản họp.

**Q638. Sau 4 tháng, dự án chuyển từ thiết kế cơ bản sang lập trình và test, nhưng báo cáo vẫn dùng chỉ số của giai đoạn thiết kế. Anh/chị điều chỉnh thế nào?**
Báo cáo phải đổi theo **giai đoạn**. Basic Design: tài liệu hoàn thành/review, câu hỏi tồn, góp ý review. Lập trình: số chương trình theo trạng thái code, review, UT xong. Test: case thực hiện/đạt, bug mở/đóng, case bị chặn. Migration: số lần rehearsal, thời gian so cửa sổ cutover, kết quả đối chiếu. Cutover: trạng thái theo bước và theo giờ. Cập nhật communication plan, báo khách mẫu mới áp dụng từ tuần nào, ghi biên bản họp. Bẫy: đổi mẫu đột ngột không giải thích, khách tưởng số liệu bị giấu.
> 📘 PMP: Tailoring (PMBOK 7) và cập nhật lặp lại communications management plan khi dự án đổi giai đoạn.

## 6.2 Báo cáo tiến độ

**Q639. Khách ngân hàng A yêu cầu báo cáo tiến độ theo dạng kế hoạch/thực tế mỗi tuần. Một báo cáo tiến độ đủ cần những thành phần nào?**
① Baseline và thực tế tại ngày cut-off theo dạng kế hoạch/thực tế (yotei/jisseki – kế hoạch/thực tế): % kế hoạch và % thực tế theo từng giai đoạn và deliverable. ② Số ngày trễ ở các mốc chính, đánh dấu mốc trên critical path. ③ Bảng mốc: ngày kế hoạch, ngày dự báo, trạng thái. ④ Nguyên nhân chênh lệch, đối sách có người phụ trách và hạn, ngày dự báo hoàn thành. % tính theo quy tắc đo đã thống nhất (0/100, 50/50, weighted milestone), không theo cảm giác. Bẫy: có % mà không có ngày dự báo, khách không biết "trễ" nghĩa là gì với kế hoạch của họ.
> 📘 PMP: Control Schedule: variance analysis + forecast; milestone chart.
> 💡 Nhật: Câu "không có chậm trễ" phải chứng minh bằng bảng kế hoạch – thực tế; khách Nhật nhìn số trước, đọc giải thích sau.

**Q640. Module "tính phí bảo hiểm" ở giai đoạn thiết kế chi tiết đã báo 90% suốt 3 tuần liền, người phụ trách nói "sắp xong". Anh/chị làm gì?**
Đây là dấu hiệu "hội chứng 90%". ① Xác nhận fact: liệt kê từng tài liệu Detail Design còn lại, trạng thái review, số góp ý chưa sửa, câu hỏi chờ khách. ② Đổi cách đo sang tiêu chí khách quan: 0/100 theo tài liệu hoặc weighted milestone (viết xong 50%, review xong 80%, sửa xong và được duyệt 100%). ③ Ước lượng lại phần còn lại từ dưới lên, ra ngày dự báo mới. ④ Báo cáo theo cách đo mới, giải thích chênh lệch; áp dụng cùng tiêu chí cho mọi module theo rà soát và áp dụng sang chỗ tương tự.
> 📘 PMP: Phương pháp đo tiến độ khách quan của EVM (0/100, 50/50, weighted milestones) trong Control Schedule.
> 💡 Nhật: Khách Nhật thường hỏi "Còn bao nhiêu hạng mục?" — trả lời bằng số đếm, không bằng %.

**Q641. Tuần 10 của giai đoạn thiết kế cơ bản: PV = 400 man-day, EV = 340 man-day. Tính SPI, SV và diễn giải cho khách thế nào?**
SPI = EV/PV = 340/400 = **0,85**; SV = EV − PV = **−60 man-day**: team mới hoàn thành 85% khối lượng lẽ ra phải xong. Khi báo khách, không dừng ở con số: ① Kiểm tra phần thiếu có nằm trên critical path không; nếu có thì mốc sẽ trễ, quy ra số ngày; nếu không thì float có thể hấp thụ. ② Cho xu hướng SPI 3–4 tuần gần nhất (đang xấu đi hay hồi phục). ③ Kèm đối sách và ngày dự báo. Bẫy: SV tính bằng man-day hoặc tiền, không phải ngày lịch; và về cuối dự án SPI luôn tiến về 1,0 nên mất tác dụng cảnh báo.
> 📘 PMP: EVM: SPI = EV/PV, SV = EV − PV; kết hợp critical path để quy ra ngày trễ.

**Q642. SPI tổng của dự án là 0,97 (trong ngưỡng xanh), nhưng mốc giao thiết kế cơ bản phần "thanh toán quyền lợi" nằm trên critical path đang trễ 6 ngày. Báo cáo màu gì, vì sao?**
Báo **vàng hoặc đỏ theo ngưỡng của mốc**, không xanh. SPI tổng bị kéo đẹp vì các việc không quan trọng đi trước kế hoạch, che mất việc critical đang trễ. ① Xác nhận float của mốc bằng 0, trễ 6 ngày sẽ đẩy các mốc sau. ② Báo song song: SPI tổng và trạng thái từng mốc critical. ③ Đưa đối sách: chuyển người từ việc đang vượt sang việc critical, review song song (fast-tracking) có kiểm soát rủi ro làm lại. ④ Từ kỳ này RAG tiến độ xét cả mốc critical, không chỉ chỉ số tổng.
> 📘 PMP: Critical path method + Control Schedule: chỉ số tổng hợp không thay được phân tích float.

**Q643. Khách hỏi "bao giờ xong lập trình?"; team đưa ngày theo kế hoạch gốc dù 4 tuần qua tốc độ thực tế chỉ 40 so với 50 chương trình/tuần kế hoạch, còn 200 chương trình. Dự báo thế nào?**
Dự báo phải dựa trên **hiệu suất thực tế**. 200 chương trình ÷ 40/tuần = 5 tuần, không phải 4 tuần như kế hoạch. ① Kiểm tra tốc độ 40 có ổn định không, có yếu tố một lần (nghỉ lễ, môi trường hỏng) không. ② Đưa khoảng dự báo: tốt nhất 4,5 tuần nếu đối sách hiệu quả, khả năng cao 5 tuần, kèm giả định. ③ Nêu đối sách để kéo lại và điều kiện để đạt. ④ Cập nhật dự báo mỗi tuần. Bẫy: báo ngày kế hoạch khi đã biết gần như chắc không đạt.
> 📘 PMP: Forecasting bằng trend analysis trong Control Schedule.
> 💡 Nhật: Khách Nhật hay hỏi dự báo điểm về đích; luôn ghi kèm điều kiện tiền đề.

**Q644. Khách sản xuất D phàn nàn tiến độ lập trình "chỉ thấy %, không biết thật hay không" (team 20 người, 180 chương trình). Anh/chị trình bày tiến độ thế nào cho khách quan?**
Đếm theo **đơn vị WBS và trạng thái có bằng chứng**: mỗi chương trình đi qua code xong → review xong → UT xong; chỉ tính "hoàn thành" khi UT đạt và có biên bản review. Báo cáo: số chương trình kế hoạch/thực tế theo từng trạng thái mỗi tuần, đường S-curve tích lũy kế hoạch vs thực tế, danh sách chương trình trễ. ① Thống nhất định nghĩa "xong" với khách trước. ② Cho khách xem mẫu bằng chứng (biên bản review, kết quả UT) khi được yêu cầu. Bẫy: đếm "code xong" là xong, sau đó UT phát sinh rework lớn và % tụt.
> 📘 PMP: Definition of done + S-curve trong Control Schedule.

**Q645. Dự án chuyển hệ thống hợp đồng bảo hiểm nhân thọ đang chạy diễn tập chuyển đổi lần 2 trên 3 lần. Báo cáo tiến độ diễn tập cho khách gồm gì?**
Bám theo kịch bản cutover của diễn tập chuyển đổi: ① Số bước trong quy trình chuyển đổi từng bước đã chạy/tổng, bước lỗi hoặc phải làm lại. ② Thời gian thực tế từng khối việc so kế hoạch và so **cửa sổ** cutover, ví dụ 19 giờ so cửa sổ 24 giờ. ③ Issue phát sinh, trạng thái xử lý, ảnh hưởng tới lần sau. ④ Xu hướng qua các lần diễn tập so tiêu chí go/no-go đã thống nhất. Kết quả đối chiếu dữ liệu báo trong báo cáo chất lượng đi kèm. Bẫy: ghi "diễn tập hoàn tất" mà không có thời gian và số bước.
> 📘 PMP: Control Schedule cho chuỗi hoạt động cutover; tiêu chí go/no-go như milestone có điều kiện.
> 💡 Nhật: Khách tài chính Nhật duyệt quy trình chuyển đổi từng bước rất kỹ; báo cáo theo đúng số bước trong tài liệu đó để họ đối chiếu.

**Q646. Báo cáo tuần trước ghi tiến độ thiết kế cơ bản 65%; tuần này rà lại phát hiện 30 màn hình chưa có trong WBS, tiến độ tính lại chỉ còn 58%. Báo cáo thế nào?**
Báo **minh bạch việc mẫu số thay đổi**. ① Xác nhận 30 màn hình là gì: thiếu do WBS sót (lỗi ước lượng nội bộ) hay yêu cầu mới của khách (xử lý theo CR). ② Báo % cũ, % mới, lý do đổi mẫu số, ảnh hưởng tới ngày hoàn thành và effort. ③ Nếu cần đổi baseline thì đi qua change control; chưa duyệt thì vẫn báo so baseline cũ kèm dự báo. ④ Gốc rễ: WBS chưa đối chiếu đủ danh sách định nghĩa yêu cầu; phòng ngừa bằng checklist đối chiếu khi lập WBS. Bẫy: giữ mẫu số cũ để % không đi lùi.
> 📘 PMP: Control Schedule; mọi thay đổi baseline đi qua Perform Integrated Change Control.
> 💡 Nhật: % "đi lùi" mà không giải thích khiến khách Nhật nghi cả báo cáo; ghi rõ mẫu số thay đổi và vì sao.

**Q647. Steering committee hằng tháng của khách bảo hiểm B chỉ xem ngày dự báo hiện tại của từng mốc nên không nhận ra mốc nào đang trôi dần. Anh/chị dùng công cụ gì?**
Dùng **biểu đồ xu hướng mốc** (milestone trend): trục ngang là kỳ báo cáo, trục dọc là ngày dự báo của từng mốc. Đường nằm ngang là ổn định; đường đi lên là mốc trôi dần dù mỗi tuần chỉ trễ 1–2 ngày. ① Lấy dữ liệu dự báo các kỳ trước từ báo cáo đã lưu. ② Vẽ 5–6 mốc chính (xong thiết kế cơ bản, xong IT, xong ST, UAT, cutover). ③ Mốc nào trôi từ 2 kỳ liên tiếp trở lên phải được giải thích và có đối sách. Bẫy: mỗi kỳ ghi đè dự báo cũ nên mất lịch sử, không ai thấy xu hướng.
> 📘 PMP: Trend analysis trong Control Schedule; báo cáo xu hướng để cảnh báo sớm.

**Q648. Team đang trễ 8 ngày so kế hoạch lập trình; trưởng nhóm đề nghị báo khách "đúng tiến độ" vì sẽ làm thêm giờ 2 tuần để bắt kịp. Anh/chị quyết định thế nào?**
Không báo "đúng tiến độ". ① Kiểm tra tính khả thi: 8 ngày trễ quy ra bao nhiêu giờ, OT 2 tuần có đủ không, ảnh hưởng chất lượng và sức khỏe. ② Báo khách trạng thái thật (trễ 8 ngày, vàng) kèm kế hoạch lấy lại, ngày dự kiến bắt kịp, điểm kiểm tra hằng tuần. ③ OT cần lãnh đạo nội bộ duyệt chi phí; với hợp đồng theo công sức, giờ vượt phải được khách đồng ý trước. ④ Phân tích gốc rễ trễ để kế hoạch không chỉ dựa vào OT. Bẫy: OT thất bại thì tuần sau báo trễ đột ngột, mất tin tưởng gấp đôi.
> 📘 PMP: PMI Code of Ethics – honesty; crashing phải phân tích chi phí và rủi ro trước khi áp dụng (Control Schedule).
> 💡 Nhật: Kế hoạch đuổi kịp có số giờ, số người, ngày kiểm tra — khách Nhật chấp nhận trễ có kế hoạch hơn là bị bất ngờ.

**Q649. Giai đoạn kiểm thử tích hợp của khách phi nhân thọ C có 2.400 test case trong 6 tuần. Báo cáo tiến độ test hằng tuần dùng chỉ số nào?**
① Số case kế hoạch / đã thực hiện / đạt theo ngày, vẽ đường tích lũy so kế hoạch (2.400 ÷ 6 tuần ≈ 400 case/tuần). ② Case bị chặn và lý do (bug chưa sửa, môi trường, dữ liệu test). ③ Bug mở/đóng ở mức tổng quan; chi tiết thuộc báo cáo chất lượng. ④ Số ngày còn lại và ngày dự báo xong theo tốc độ thực tế. Tách rõ "đã thực hiện" và "đạt": case fail chưa retest thì chưa tính xong. Bẫy: báo "thực hiện 100%" trong khi 20% case fail chưa test lại.
> 📘 PMP: Control Schedule kết hợp Control Quality: work performance information của hoạt động test.

**Q650. Giai đoạn thiết kế cơ bản có 25 câu hỏi trong bảng Q&A quá hạn trả lời trung bình 7 ngày, làm trễ 2 tài liệu. Báo cáo cho khách thế nào để công bằng mà không đổ lỗi?**
Báo **bằng số và ảnh hưởng**, không bằng lời trách. ① Thống kê từ bảng quản lý Q&A : số câu mở, quá hạn, tuổi trung bình, câu nào chặn tài liệu nào. ② Quy ra ảnh hưởng: ví dụ 2 tài liệu trễ 4 ngày vì chờ 6 câu cụ thể. ③ Đề xuất: danh sách 5 câu ưu tiên cao nhất, buổi họp 30 phút giải đáp trực tiếp, hoặc tiến hành theo giả định có ghi rủi ro. ④ Ghi vào biên bản họp; phần trễ do chờ khách là căn cứ thảo luận điều chỉnh lịch theo quy trình CR. Bẫy: chỉ nói "khách trả lời chậm" chung chung.
> 📘 PMP: Issue log + assumption log; Manage Stakeholder Engagement.
> 💡 Nhật: Cách nói "Nếu anh/chị trả lời giúp thì chúng tôi rất biết ơn" (nói bằng tiếng Nhật) kèm danh sách ưu tiên giúp đầu mối liên lạc dễ đi hỏi nội bộ phía họ.

**Q651. Team VN nghỉ Tết 7 ngày trong khi khách Nhật vẫn làm việc; tuần đó khách thấy tiến độ đứng yên và hỏi có vấn đề gì. Báo cáo tiến độ quanh giai đoạn nghỉ lễ thế nào?**
Lịch dự án phải gồm **cả hai lịch nghỉ** ngay từ baseline. ① Kiểm tra baseline: nếu đã tính Tết thì kế hoạch tuần đó cũng phẳng, không có chênh lệch — chỉ cần giải thích bằng biểu đồ kế hoạch – thực tế. ② Nếu baseline bỏ sót Tết: đây là lỗi lập lịch, báo rõ ảnh hưởng và xử lý thay đổi baseline theo quy trình. ③ Từ nay mỗi báo cáo nêu trước các giai đoạn nghỉ trong 4–6 tuần tới, kèm phương án trực hỗ trợ (ai trực, xử lý sự cố gì, kênh liên lạc). Bẫy: khách chỉ phát hiện team nghỉ khi gửi câu hỏi mà không ai trả lời.
> 📘 PMP: Project calendar và resource calendars trong Develop Schedule và Control Schedule.
> 💡 Nhật: Báo lịch Tết VN trước 1–2 tháng (tham khảo), nhất là khi gần cuối năm tài chính (tháng 3): khách Nhật lên lịch UAT và nhân sự theo năm tài chính.

## 6.3 Báo cáo effort và ngân sách

**Q652. Dự án có BAC 1.200 man-day; cuối tháng 4: PV 500, EV 450, AC 540. Tính CPI, SPI, EAC và diễn giải cho lãnh đạo nội bộ thế nào?**
CPI = 450/540 ≈ **0,83**; SPI = 450/500 = **0,90**. Nếu hiệu suất hiện tại tiếp diễn: EAC = BAC/CPI ≈ **1.440 man-day**, VAC ≈ −240 (vượt khoảng 20%). Nếu phần vượt do sự kiện một lần (ví dụ môi trường hỏng 2 tuần) và đã qua: EAC = AC + (BAC − EV) = 540 + 750 = **1.290**. ① Kiểm tra AC đúng (timesheet đã duyệt). ② Phân tích nguyên nhân để chọn công thức, ghi rõ giả định. ③ Báo khoảng 1.290–1.440 kèm đối sách và người phụ trách. Bẫy: mặc định một công thức cho mọi trường hợp.
> 📘 PMP: Control Costs: CPI = EV/AC; EAC = BAC/CPI khi sai lệch điển hình, EAC = AC + (BAC − EV) khi sai lệch không lặp lại.

**Q653. Effort tổng team 20 người tháng này chỉ vượt 3% kế hoạch, nhưng xem theo module thì batch tính phí vượt 55%, màn hình tra cứu thấp hơn 30%. Anh/chị báo cáo thế nào?**
Con số tổng đang che vấn đề. ① Drill-down theo module/work package, liệt kê các chênh lệch vượt ngưỡng (ví dụ ±10%, tham khảo). ② Phân tích: batch tính phí vượt vì logic phức tạp hơn ước lượng? Nếu đúng, các batch tương tự còn lại cũng sẽ vượt và ETC phải tăng. Tra cứu thấp vì làm chưa hết hay ước lượng dư? ③ Báo top 3 chênh lệch kèm nguyên nhân và ảnh hưởng tới EAC. ④ Điều chỉnh ước lượng phần còn lại cùng loại theo rà soát và áp dụng sang chỗ tương tự. Bẫy: thấy tổng đẹp nên không nhìn chi tiết.
> 📘 PMP: Variance analysis ở mức control account/work package trong Control Costs.
> 💡 Nhật: Nhiều nơi chỉ so effort kế hoạch với thực tế trong effort kế hoạch – thực tế; thêm khối lượng đạt được (tương đương EV) để tránh kết luận "đúng ngân sách" khi việc chưa xong.

**Q654. Dự án trọn gói giá cố định với khách bảo hiểm B, kế hoạch lợi nhuận gộp 25%; tại 40% tiến độ CPI = 0,85. Báo lãnh đạo nội bộ những gì?**
① Quy ra tiền: ngân sách chi phí = 75% doanh thu; EAC ≈ 75%/0,85 ≈ 88% doanh thu, lợi nhuận gộp dự báo còn khoảng **12%** thay vì 25%. ② Nguyên nhân có số: ước lượng thiếu, rework, đặc tả chưa rõ, việc ngoài phạm vi. ③ Phương án và hiệu quả từng phương án: tăng năng suất (review sớm, tái sử dụng), tách việc ngoài phạm vi làm CR, dùng contingency. ④ Quyết định cần lãnh đạo: duyệt dùng reserve, bổ sung người hay đàm phán với khách. Báo ngay ở 40%; chờ đến 70% thì gần như hết cơ hội cứu.
> 📘 PMP: Control Costs: forecasting EAC, reserve analysis; escalate khi vượt ngưỡng ủy quyền của PM.

**Q655. Dự án 30 người có contingency reserve 8% ngân sách, đã dùng 6% khi mới đạt 35% tiến độ. Báo cáo reserve cho lãnh đạo thế nào?**
Phân biệt rõ: **contingency reserve** nằm trong cost baseline, dành cho rủi ro đã nhận diện, PM dùng theo risk response plan; **management reserve** ngoài baseline, cho rủi ro chưa biết, cần lãnh đạo duyệt. ① Tính tốc độ tiêu: 6/8 = 75% reserve đã dùng khi mới 35% tiến độ — cảnh báo. ② So reserve còn lại (2%) với mức phơi nhiễm rủi ro còn lại (EMV). ③ Báo rủi ro nào đã xảy ra làm tiêu reserve và đề xuất: giảm phơi nhiễm hoặc xin thêm từ management reserve. Bẫy: gộp reserve vào effort chung nên không ai biết đã gần hết.
> 📘 PMP: Reserve analysis trong Determine Budget và Control Costs.

**Q656. Dự án theo công sức với ngân hàng A: giữa tháng PM thấy 3 người dự kiến vượt trần khoảng giờ thanh toán khoảng 20 giờ. Báo cáo thế nào?**
① Xác nhận: ai, vượt bao nhiêu, vì sao (khách giao thêm việc hay vấn đề nội bộ như rework). ② Báo khách **ngay khi dự báo vượt**, không đợi cuối tháng. ③ Vượt do yêu cầu khách: xác nhận cách tính giờ vượt theo hợp đồng và xin đồng ý trước khi làm tiếp; vượt do nội bộ: không tính tiền, xử lý năng suất, điều chỉnh phân công để không vượt. ④ Phòng ngừa: dự báo giờ hằng tuần, cảnh báo khi đạt 80% trần (tham khảo). Bẫy: để khách thấy số vượt lần đầu trên hóa đơn.
> 📘 PMP: Control Costs + điều khoản hợp đồng (agreements); Manage Communications.
> 💡 Nhật: Ngân sách phía khách Nhật được duyệt theo năm; vượt mà không báo trước có thể khiến đầu mối liên lạc không có tiền trả và bị cấp trên trách.

**Q657. Báo cáo chi phí nội bộ của dự án chỉ có effort, trong khi có 2 BrSE onsite Tokyo, license công cụ test và phí thuê môi trường. Tổ chức báo cáo ngân sách đầy đủ thế nào?**
Cấu trúc ngân sách theo nhóm: ① Nhân công = effort × đơn giá theo cấp bậc; ② Onsite (vé, lưu trú, phụ cấp); ③ Chi phí trực tiếp khác (license, thiết bị, môi trường); ④ Reserve. Mỗi nhóm có kế hoạch, thực tế, dự báo; ghi nhận cả chi phí đã phát sinh chưa có hóa đơn. Lợi nhuận dự báo = doanh thu theo lịch nghiệm thu − EAC toàn bộ. Bẫy: chỉ báo effort nên lợi nhuận ảo; onsite kéo dài thêm 1 tháng có thể ăn mất vài điểm % lợi nhuận.
> 📘 PMP: Cost aggregation trong Determine Budget; Control Costs cho mọi loại chi phí, không chỉ nhân công.
> 💡 Nhật: Thời điểm nghiệm thu quyết định ghi nhận doanh thu; nghiệm thu trượt qua cuối năm tài chính (tháng 3) có thể làm lệch kết quả năm của cả công ty — báo lãnh đạo sớm.

**Q658. Ở 60% tiến độ: BAC 1.000 man-day, EV 600, AC 680. Lãnh đạo hỏi "còn giữ được ngân sách không?". Trả lời thế nào?**
Tính TCPI = (BAC − EV)/(BAC − AC) = 400/320 = **1,25**: phần việc còn lại phải đạt hiệu suất cao hơn kế hoạch 25%, trong khi CPI hiện tại chỉ 600/680 ≈ 0,88. Khoảng cách 0,37 gần như không thể bù (chênh trên 0,1 đã rất khó, tham khảo). ① Báo thẳng: BAC không giữ được. ② Đưa EAC thực tế (≈ 1.130 man-day nếu CPI giữ nguyên). ③ Đề xuất: xin duyệt ngân sách mới, hoặc giảm phạm vi/đàm phán CR cho phần ngoài hợp đồng. ④ Lấy TCPI theo EAC mới làm mục tiêu theo dõi. Bẫy: trả lời "team sẽ cố gắng".
> 📘 PMP: TCPI trong Control Costs, so với CPI hiện tại để đánh giá tính khả thi của mục tiêu.

**Q659. Dự án migration trọn gói: phần effort vượt 40% là rework do dữ liệu cũ bẩn hơn dự kiến (dữ liệu mẫu khách đưa không đại diện). Báo cho khách và cho lãnh đạo khác nhau thế nào?**
**Cùng fact, khác lớp thông tin**. Nội bộ: effort vượt, CPI, nguyên nhân, ảnh hưởng lợi nhuận, phương án phục hồi, khả năng đề xuất CR. Khách: không nói chi phí nội bộ hay "chúng tôi lỗ", mà nêu fact về dữ liệu, ví dụ 12.000 bản ghi lỗi thuộc 8 loại so với giả định ban đầu; ảnh hưởng tới lịch/phạm vi; đề xuất thảo luận trách nhiệm làm sạch dữ liệu theo quy trình CR. ① Tập hợp bằng chứng (thống kê lỗi, ví dụ đã che dữ liệu cá nhân). ② Báo lãnh đạo trước, thống nhất thông điệp. ③ Trình khách. ④ Ghi giả định bị phá vỡ vào log.
> 📘 PMP: Truyền thông theo stakeholder; assumption log → change request.
> 💡 Nhật: Hợp đồng trọn gói với khách Nhật thường có điều kiện tiền đề; báo cáo bám vào điều kiện tiền đề bị phá vỡ giúp khách dễ chấp nhận thảo luận hơn là nói "khó quá".

**Q660. Team 25 người ghi timesheet dồn vào cuối tháng, nhiều người điền đều 8 giờ/ngày cho cùng 1 task, CPI tính ra luôn xấp xỉ 1,0. Anh/chị xử lý thế nào?**
AC sai thì EVM vô nghĩa. ① Kiểm tra: đối chiếu timesheet với chấm công, lịch sử task, commit; đo tỷ lệ timesheet nộp đúng hạn. ② Quy định ghi hằng ngày hoặc chậm nhất cuối tuần, theo task WBS, leader duyệt sáng thứ Hai. ③ Đưa "tỷ lệ timesheet duyệt đúng hạn" vào báo cáo nội bộ như chỉ số vệ sinh dữ liệu. ④ Giải thích cho team: số liệu dùng để dự báo và xin nguồn lực, không dùng để phạt — nếu không, mọi người sẽ tiếp tục điền "cho đẹp". Bẫy: CPI đẹp nhờ dữ liệu, che vượt effort thật.
> 📘 PMP: Chất lượng work performance data là nền của Control Costs; Measurement performance domain (PMBOK 7) – số đo phải tin cậy.

**Q661. Sau re-estimate giữa dự án, EAC cao hơn BAC 15%. Một PM đề nghị cập nhật luôn baseline chi phí để báo cáo trở lại màu xanh. Anh/chị nghĩ sao?**
Không đổi baseline tự ý. ① Baseline chỉ thay khi được duyệt qua change control: nội bộ cần lãnh đạo duyệt tăng ngân sách; nếu kéo theo giá hợp đồng thì cần khách đồng ý qua CR. ② Trước khi duyệt, báo cáo vẫn so baseline gốc + EAC mới, màu theo ngưỡng. ③ Sau khi duyệt, re-baseline nhưng **giữ lịch sử**: baseline gốc, baseline hiện hành, lý do, ngày duyệt, để xu hướng không bị xóa. Bẫy: re-baseline liên tục khiến dự án lúc nào cũng xanh, lãnh đạo mất khả năng nhìn thấy vấn đề.
> 📘 PMP: Perform Integrated Change Control: thay đổi cost baseline phải được duyệt và lưu vết.
> 💡 Nhật: Tăng ngân sách nội bộ ở công ty làm với Nhật thường đi qua thủ tục trình ký nội bộ; chuẩn bị số EAC và phương án sớm vì vòng duyệt có thể mất 1–2 tuần (tham khảo).

**Q662. Giám đốc khối hỏi "3 tháng tới dự án cần bao nhiêu người, kỹ năng gì?" khi dự án chuẩn bị vào kiểm thử tổng hợp. Anh/chị báo cáo thế nào?**
Lập **resource histogram** theo vai trò và theo tháng từ WBS còn lại và ETC, so với nhân sự đang có. ① Chỉ ra thiếu/thừa và thời điểm: ví dụ ST cần thêm 2 tester biết nghiệp vụ bảo hiểm từ tuần 3 tháng 6; thừa 4 dev sau khi xong IT. ② Nêu lead time cần để tuyển hoặc điều chuyển. ③ Rủi ro nếu không có người đúng kỹ năng. ④ Đề xuất giải phóng người thừa sớm để giảm chi phí và hỗ trợ dự án khác. Bẫy: chỉ báo số đầu người, không nói kỹ năng (tiếng Nhật, nghiệp vụ).
> 📘 PMP: Resource histogram; Control Resources.

**Q663. Dự án theo công sức giữa kỳ có CPI = 1,10 và SPI = 0,80; lãnh đạo khen dự án "tiết kiệm". Anh/chị phản hồi thế nào?**
Đọc CPI cùng SPI: CPI > 1 kèm SPI < 1 thường là **thiếu người** — chi ít vì ít người, nhưng việc chậm. ① Kiểm tra số người thực tế so kế hoạch, ngày onboard trễ. ② Với hợp đồng theo công sức, doanh thu tính theo công số: thiếu người nghĩa là giảm doanh thu và khách nhận kết quả trễ, không phải tiết kiệm. ③ Báo lãnh đạo vấn đề thật là thiếu nguồn lực; đề xuất bổ sung người và ngày dự báo. ④ Báo khách trễ kèm kế hoạch bổ sung. Bẫy: nhìn từng chỉ số riêng lẻ rồi kết luận.
> 📘 PMP: Đọc EVM theo cặp CPI–SPI để chẩn đoán nguyên nhân (Control Costs, Control Schedule).

**Q664. Dự án kéo dài 2 năm; đầu năm thứ hai đơn giá nội bộ tăng 6% do tăng lương, CPI tính theo tiền giảm từ 1,0 xuống 0,94 dù năng suất không đổi. Báo cáo thế nào?**
Tách hai loại chênh lệch: ① **Chênh lệch hiệu suất** – CPI tính theo man-hour vẫn 1,0, team không làm kém đi; ② **Chênh lệch đơn giá** – chi phí mỗi giờ tăng 6%. Báo lãnh đạo tác động lên lợi nhuận năm thứ hai và nói rõ nguyên nhân không nằm ở năng suất. ③ Tăng lương là việc dự đoán được, lẽ ra phải có hệ số tăng giá trong ngân sách nhiều năm; đề xuất cập nhật baseline qua phê duyệt. ④ Bài học cho estimate dự án sau: thêm hệ số tăng đơn giá theo năm. Bẫy: để PM bị đánh giá "kém hiệu quả" vì yếu tố ngoài kiểm soát.
> 📘 PMP: Variance analysis tách theo nguyên nhân; thay đổi cost baseline qua Perform Integrated Change Control.

## 6.4 Báo cáo rủi ro và vấn đề

**Q665. Khách ngân hàng A yêu cầu đưa phần rủi ro vào họp định kỳ hằng tuần; register hiện có 42 rủi ro. Phần rủi ro trong báo cáo cho khách nên trình bày gì?**
Chỉ đưa **top 5 rủi ro** theo điểm xác suất × ảnh hưởng; register đầy đủ để phụ lục. Mỗi rủi ro: mô tả dạng nguyên nhân → sự kiện → ảnh hưởng, điểm P×I và xu hướng (tăng/giảm), owner, biện pháp ứng phó, trigger, hạn. Thêm: rủi ro mới, rủi ro đóng kỳ này, và **việc khách cần làm** để giảm rủi ro. Bẫy: liệt kê 42 dòng không ưu tiên; rủi ro nào cũng "đang theo dõi" mãi mà không có hành động.
> 📘 PMP: Monitor Risks: risk register, probability and impact matrix, risk report.
> 💡 Nhật: Khách Nhật phân biệt rõ risk (chưa xảy ra) và issue (đã xảy ra, cần xử lý); trộn hai loại vào một bảng gây hiểu sai mức khẩn cấp.

**Q666. Bảng quản lý vấn đề của dự án bảo hiểm B có 18 issue mở quá 30 ngày, phần lớn không có hạn xử lý. Anh/chị báo cáo và xử lý thế nào?**
① Phân tích tuổi issue trong bảng quản lý vấn đề: nhóm 0–7, 8–30, trên 30 ngày; phân loại theo owner (khách, nội bộ, vendor) và mức ảnh hưởng (có chặn critical path không). ② Dọn: gộp trùng, đóng issue đã hết hiệu lực có xác nhận; mỗi issue còn lại phải có owner tên cụ thể và hạn. ③ Issue chặn critical path: escalate theo thang đã thống nhất, ví dụ không tiến triển sau 2 kỳ họp định kỳ thì đưa lên trưởng phòng (tham khảo). ④ Thêm biểu đồ tuổi issue vào báo cáo tuần để thấy xu hướng. Bẫy: issue không có hạn và người chịu trách nhiệm.
> 📘 PMP: Issue log trong Monitor and Control Project Work; escalation path theo communications management plan.

**Q667. Rủi ro "thiếu tester đọc được spec tiếng Nhật" đã có trong register; hôm nay 1 trong 3 tester như vậy nghỉ việc giữa giai đoạn kiểm thử tích hợp. Báo cáo thế nào?**
Rủi ro đã xảy ra thì **chuyển thành issue**. ① Xác nhận: ngày nghỉ, việc đang dở, case nào bị ảnh hưởng. ② Kích hoạt contingency plan đã ghi (tester dự phòng, BrSE hỗ trợ đọc spec, đổi thứ tự test). ③ Báo cáo: "rủi ro số 7 đã xảy ra ngày…, đã kích hoạt phương án…, ảnh hưởng còn lại…", đưa sang issue log có owner và hạn. ④ Đánh giá rủi ro thứ phát (người thay chưa quen nghiệp vụ bảo hiểm), cập nhật register. Bẫy: rủi ro đã xảy ra mà báo cáo vẫn ghi "đang theo dõi".
> 📘 PMP: Implement Risk Responses: kích hoạt contingency plan; chuyển sang issue log; nhận diện secondary risk.

**Q668. Migration phụ thuộc hệ thống mainframe cũ của khách bảo hiểm nhân thọ B mà chỉ còn 1 nhân viên phía khách hiểu logic, người này nghỉ hưu tháng 9. Báo cáo rủi ro này thế nào khi đó là chuyện nội bộ của khách?**
Đây là rủi ro của dự án dù owner là khách. ① Ghi fact: ai, ngày nghỉ, hạng mục migration nào phụ thuộc kiến thức đó. ② Đưa vào register với owner phía khách, ảnh hưởng tới lịch chuyển đổi dữ liệu, biện pháp đề xuất: buổi chuyển giao kiến thức có ghi hình, team ghi lại spec ngầm, ưu tiên phân tích phần đó trước tháng 9. ③ Trao đổi riêng với đầu mối liên lạc trước khi đưa vào báo cáo chính thức. ④ Theo dõi trigger: đến tháng 7 chưa xong 50% chuyển giao (tham khảo) thì escalate.
> 📘 PMP: Plan Risk Responses: risk owner có thể là stakeholder bên ngoài; Manage Stakeholder Engagement.
> 💡 Nhật: Nêu rủi ro thuộc phía khách trước mặt trưởng phòng khi chưa trao đổi riêng trước với từng người liên quan sẽ làm đầu mối liên lạc mất mặt; luôn nói riêng trước.

**Q669. Dự án cần khách chọn giữ nguyên hay đổi cách tính lãi chậm nộp phí, quyết định đã treo 2 tuần. Anh/chị viết mục "cần quyết định" trong báo cáo thế nào để khách quyết nhanh?**
Viết theo khung 1 trang: ① Vấn đề trong 2–3 câu. ② 2–3 phương án, mỗi phương án có ảnh hưởng tới phạm vi, lịch, chi phí, chất lượng. ③ Khuyến nghị của PM kèm lý do. ④ **Hạn quyết định** và hậu quả nếu không quyết: ví dụ sau ngày 15, mỗi tuần chậm làm trễ mốc Basic Design thêm 1 tuần. Nêu rõ ai là người quyết. Bẫy: chỉ nêu vấn đề, không có phương án; hoặc đưa 5 phương án khiến khách càng khó chọn.
> 📘 PMP: Decision-making với phân tích phương án; Manage Stakeholder Engagement; escalation khi quá hạn.
> 💡 Nhật: Khách Nhật cần thời gian thống nhất nội bộ; đặt hạn quyết định sớm hơn hạn thật 1–2 tuần (tham khảo).

**Q670. Rủi ro "chậm cấp quyền truy cập môi trường mạng đóng cho team VN" tăng điểm 3 tuần liền, nhưng báo cáo vẫn ghi biện pháp là "theo dõi". Anh/chị làm gì?**
"Theo dõi" không phải biện pháp ứng phó. ① Xác định trigger cụ thể: ví dụ đến ngày 10 chưa có quyền thì kích hoạt phương án B. ② Lập phương án B: làm trên môi trường giả lập ngoài mạng đóng với dữ liệu giả, hoặc tăng người onsite tạm thời, kèm chi phí. ③ Xu hướng tăng 3 tuần là tín hiệu escalate: báo khách bằng yêu cầu cụ thể (ai phía khách cần duyệt gì, trước ngày nào) và ảnh hưởng nếu không có. ④ Rà lại các rủi ro khác đang chỉ ghi "theo dõi".
> 📘 PMP: Monitor Risks: risk reassessment, trigger condition, escalate khi xu hướng xấu đi.

**Q671. Đầu mối khách bảo hiểm B yêu cầu bỏ rủi ro "dữ liệu thật của người được bảo hiểm đang dùng trong môi trường test chưa che" khỏi báo cáo gửi trưởng phòng của họ, vì "nhạy cảm". Xử lý thế nào?**
Không xóa rủi ro trọng yếu, nhưng có thể điều chỉnh cách trình bày. ① Hỏi lý do đầu mối liên lạc lo ngại. ② Đề xuất ghi trung tính kèm kế hoạch: "dữ liệu test cần che trước ngày X; công cụ che đã sẵn sàng; cần khách duyệt quy trình". ③ Nếu đầu mối liên lạc vẫn từ chối: giữ nguyên trong register, ghi biên bản họp rằng khách quyết định không đưa vào báo cáo cấp trên, báo lãnh đạo nội bộ xin chỉ đạo. ④ Song song đẩy nhanh việc che dữ liệu vì đây còn là rủi ro tuân thủ bảo mật.
> 📘 PMP: PMI Code of Ethics – honesty, responsibility; Manage Stakeholder Engagement; giữ toàn vẹn risk register.
> 💡 Nhật: Đầu mối liên lạc thường sợ bị cấp trên trách; đưa rủi ro kèm câu "phía khách đã có biện pháp" giúp họ đồng ý báo lên.

**Q672. Lãnh đạo nội bộ hỏi contingency 25 man-day hiện có có đủ không. Top 3 rủi ro: 30% gây thêm 40 man-day, 20% gây thêm 100 man-day, 50% gây thêm 10 man-day. Trả lời thế nào?**
Tính EMV: 0,3 × 40 = 12; 0,2 × 100 = 20; 0,5 × 10 = 5; tổng **37 man-day**, lớn hơn contingency 25 nên thiếu 12. ① Kiểm tra lại xác suất và ảnh hưởng với team, tránh số cảm tính. ② Báo lãnh đạo mức thiếu và rủi ro đóng góp lớn nhất (rủi ro 2). ③ Đề xuất giảm xác suất rủi ro 2 trước (thường rẻ hơn xin thêm reserve), phần còn lại xin bổ sung contingency. ④ Cập nhật hằng tháng. Lưu ý: nếu riêng rủi ro 2 xảy ra (100 man-day) thì contingency vẫn không đủ — phải nêu riêng.
> 📘 PMP: Expected monetary value (EMV) trong Perform Quantitative Risk Analysis; reserve analysis.

**Q673. Steering committee của chương trình 60 người chỉ dành 15 phút cho phần rủi ro, trong khi có 45 rủi ro đang mở. Trình bày thế nào?**
Steering chỉ cần những gì **thuộc thẩm quyền của họ**. ① Một biểu đồ xu hướng tổng mức phơi nhiễm rủi ro (tổng EMV) qua các tháng. ② Heat map vị trí 45 rủi ro, không đọc từng dòng. ③ 3 rủi ro cần cấp steering quyết định hoặc hỗ trợ (ngân sách, ưu tiên giữa các dự án, chấp nhận rủi ro kinh doanh), mỗi rủi ro có phương án và hạn. ④ Ghi rõ các rủi ro còn lại đang được xử lý ở cấp dự án. Bẫy: dùng 15 phút đọc register, không còn thời gian cho quyết định.
> 📘 PMP: Monitor Risks: risk report theo cấp; governance và escalation theo thẩm quyền.

**Q674. Rủi ro "hiệu năng batch cuối tháng" PM đánh giá xác suất thấp, nay đã xảy ra trong kiểm thử tổng hợp làm trễ mốc 2 tuần; khách hỏi "sao không báo trước?". Trả lời và xử lý?**
Không biện hộ. ① Thừa nhận: rủi ro có trong register (cho khách xem bản ghi) nhưng bị đánh giá thấp, xin lỗi về ảnh hưởng. ② Trình bày ảnh hưởng hiện tại và kế hoạch phục hồi có mốc kiểm tra. ③ Phân tích vì sao đánh giá sai: không đo hiệu năng sớm, một người tự chấm điểm, không có trigger. ④ Phòng ngừa: đánh giá lại rủi ro hằng tháng có team tham gia, gắn chỉ số cảnh báo sớm, rà với khách mỗi tháng; áp dụng rà soát và áp dụng cho các rủi ro hiệu năng khác.
> 📘 PMP: Monitor Risks: risk audit, risk reassessment; cập nhật lessons learned register.
> 💡 Nhật: Khách Nhật mong khung lời xin lỗi → nguyên nhân → đối sách → phòng ngừa tái diễn; thiếu phần nào họ sẽ hỏi lại phần đó.

**Q675. Một senior dev hiệu suất thấp liên tục làm module thanh toán trễ 1 tuần. Báo cáo issue này cho khách thế nào?**
Báo cáo khách ở **mức dự án**, không nêu tên hay đánh giá cá nhân: module trễ bao nhiêu, nguyên nhân dạng "phân bổ năng lực chưa phù hợp độ phức tạp", biện pháp (chia lại task, thêm reviewer, bổ sung người) và ngày dự báo. Báo cáo nội bộ mới có chi tiết nhân sự và kế hoạch xử lý với người đó. Với hợp đồng trọn gói, bố trí người là trách nhiệm bên nhận; với hợp đồng theo công sức có chỉ định người, thay người phải báo khách theo hợp đồng. Bẫy: nói "lỗi do bạn A" trong họp định kỳ.
> 📘 PMP: Manage Team + Manage Communications: tôn trọng (respect) và mức chi tiết phù hợp người nhận.
> 💡 Nhật: Khách Nhật không muốn nghe lỗi của cá nhân; họ muốn biết tổ chức dự án đã được tăng cường thế nào.

**Q676. Kế hoạch kiểm thử tích hợp dựa trên giả định "khách cung cấp dữ liệu test đã che trước ngày 1/6". Theo dõi và báo cáo giả định này thế nào, khác gì so với rủi ro?**
Giả định là điều tạm coi là đúng để lập kế hoạch; rủi ro là sự kiện không chắc chắn có ảnh hưởng. ① Ghi giả định vào assumption log với người xác nhận và **ngày phải xác nhận** (ví dụ 15/5). ② Mỗi báo cáo liệt kê các giả định sắp đến hạn xác nhận. ③ Quá hạn chưa xác nhận thì chuyển thành rủi ro (có xác suất, ảnh hưởng: IT trễ bao nhiêu ngày); đã sai thì thành issue hoặc CR. ④ Giả định quan trọng nên nằm trong hợp đồng dưới dạng điều kiện tiền đề. Bẫy: giả định chỉ nằm trong file estimate, không ai theo dõi.
> 📘 PMP: Assumption log (Develop Project Charter), được rà và cập nhật trong Monitor Risks.

**Q677. Khách phi nhân thọ C dự kiến có thay đổi quy định ngành ảnh hưởng cách tính phí, sẽ công bố khoảng 2 tháng trước go-live nhưng chưa rõ nội dung. Báo cáo rủi ro này thế nào?**
Rủi ro bên ngoài có độ bất định cao nên trình bày theo **kịch bản**. ① Xác định kịch bản: thay đổi nhỏ (chỉ tham số) ảnh hưởng vài ngày; thay đổi logic ảnh hưởng vài tuần (ước lượng khoảng). ② Biện pháp chủ động: thiết kế tham số hóa qua parameter sheet, giữ buffer lịch, xác định điểm quyết định (ngày công bố + 1 tuần phân tích). ③ Báo steering: kịch bản, chi phí phòng bị, điểm quyết định giữ ngày go-live hay phát hành theo giai đoạn. ④ Theo dõi thông tin qua khách. Không phỏng đoán nội dung quy định khi chưa có nguồn chính thức.
> 📘 PMP: Uncertainty performance domain (PMBOK 7): phân tích kịch bản, tăng khả năng thích ứng; contingency reserve.

## 6.5 Báo cáo KPI chất lượng

**Q678. Khách ngân hàng A yêu cầu báo cáo chất lượng hằng tuần trong giai đoạn kiểm thử tích hợp. Báo cáo nên gồm những gì?**
① Chỉ số định lượng: mật độ test, mật độ bug, bug tích lũy phát hiện vs đóng (đường hội tụ), bug mở theo mức độ và tuổi, tỷ lệ retest đạt. ② So với **ngưỡng mục tiêu** trong kế hoạch chất lượng; giá trị ngoài ngưỡng có phân tích. ③ Phân loại nguyên nhân bug (thiết kế, code, spec) bằng Pareto. ④ **Đánh giá** của PM/QA: chất lượng đang đạt hay chưa, vì sao, cần làm gì tiếp. Cách tính chi tiết từng chỉ số theo chuẩn chất lượng của dự án. Bẫy: bảng số không có kết luận, khách phải tự diễn giải.
> 📘 PMP: Control Quality: work performance information; Pareto chart, control chart.
> 💡 Nhật: Báo cáo chất lượng của khách Nhật cần cả đánh giá định lượng và đánh giá định tính, kết luận rõ "chất lượng đã được bảo đảm" hay chưa.

**Q679. Mật độ bug module "thanh toán quyền lợi" chỉ 0,5 bug/KLOC trong khi ngưỡng dự án là 2–4 bug/KLOC (tham khảo); leader muốn báo xanh. Anh/chị xử lý thế nào?**
Thấp bất thường cũng là tín hiệu cần phân tích. ① Kiểm tra mật độ test của module: đủ case chưa, có bao quát nhánh lỗi, giá trị biên, trường hợp hợp đồng đặc biệt không. ② Kiểm tra chất lượng test: tester có hiểu nghiệp vụ, case đã được review chưa. ③ Kiểm tra lý do hợp lý: code tái sử dụng từ module đã ổn định? ④ Báo "cần phân tích" (vàng), bổ sung test theo quan điểm còn thiếu, có kết quả mới kết luận. Bẫy: coi ít bug là chất lượng tốt.
> 📘 PMP: Control Quality: giá trị ngoài control limit ở cả hai phía đều cần điều tra nguyên nhân.
> 💡 Nhật: Khách Nhật yêu cầu phân tích nguyên nhân cho mọi giá trị ngoài giá trị chuẩn, kể cả khi trông "tốt hơn".

**Q680. Đường hội tụ bug vẫn dốc lên ở tuần cuối kiểm thử tích hợp, chỉ còn 2 tuần trước khi vào kiểm thử tổng hợp. Báo cáo và đề xuất gì?**
① Xác nhận: số bug mới mỗi ngày tuần qua, tập trung ở module nào, nguyên nhân (Pareto). ② Báo thẳng: chất lượng **chưa hội tụ**, chưa đạt tiêu chí kết thúc IT. ③ Đưa phương án cho khách quyết: kéo dài IT N ngày; test bổ sung tập trung vào module nóng; hoặc vào ST có điều kiện (danh sách hạng mục loại trừ, ngưỡng dừng). ④ Phân tích gốc rễ module nóng (thiết kế chưa rõ? dev mới?), áp dụng rà soát và áp dụng sang chỗ tương tự. Bẫy: vào ST đúng hạn rồi ST biến thành IT lần hai.
> 📘 PMP: Control Quality: trend analysis; exit criteria của giai đoạn.
> 💡 Nhật: Đường cong hội tụ bug là căn cứ khách Nhật dùng để quyết định giai đoạn có được kết thúc hay không.

**Q681. Trong kiểm thử chấp nhận, khách bảo hiểm B phát hiện 12 bug, trong đó 7 bug lẽ ra phải bắt được ở kiểm thử tích hợp. Báo cáo thế nào?**
① Xác nhận từng bug: mức độ, giai đoạn lẽ ra phải phát hiện, trạng thái sửa. ② Báo ngay số liệu và kế hoạch sửa, ưu tiên bug chặn tiến độ UAT. ③ Phân tích gốc rễ 7 bug lọt lỗi: thiếu quan điểm test, dữ liệu test không đại diện, hiểu sai spec. ④ Phòng ngừa: bổ sung quan điểm vào checklist, rà soát và áp dụng sang các module tương tự, thêm chỉ số "tỷ lệ lọt lỗi theo giai đoạn" vào báo cáo từ nay. Bẫy: chỉ sửa 12 bug mà không giải thích vì sao lọt.
> 📘 PMP: Root cause analysis; Control Quality; cập nhật lessons learned register.
> 💡 Nhật: Khách Nhật thường yêu cầu báo cáo sự cố cho bug nghiêm trọng và hỏi "đã rà soát và áp dụng sang chỗ tương tự chưa?"; chuẩn bị sẵn kết quả rà soát.

**Q682. Giai đoạn thiết kế cơ bản chưa có bug để đo; khách sản xuất D vẫn muốn báo cáo chất lượng. Anh/chị dùng chỉ số gì?**
Dùng số liệu **review**. ① Độ phủ review: số tài liệu/trang đã review trên tổng. ② Effort review và số góp ý trên mỗi trang (mật độ góp ý review), so ngưỡng chuẩn công ty (tham khảo). ③ Phân loại góp ý: thiếu yêu cầu, sai logic nghiệp vụ, trình bày — tỷ lệ lỗi nghiệp vụ cao là tín hiệu xấu hơn lỗi trình bày. ④ Chỉ trích còn mở và hạn đóng. Kèm đánh giá: tài liệu nào cần review lại hoặc thêm reviewer nghiệp vụ. Bẫy: chỉ đếm số buổi review mà không đo kết quả.
> 📘 PMP: Manage Quality/Control Quality: inspection (review) và dữ liệu kiểm tra.

**Q683. Giám đốc chất lượng nội bộ muốn một dashboard so sánh chất lượng 10 dự án (từ 5 đến 60 người). Chọn KPI nào?**
Chọn chỉ số **chuẩn hóa** để so được: mật độ bug theo quy mô, tỷ lệ lọt lỗi (bug UAT và production trên tổng bug), tỷ lệ lỗi phát hiện ở review so với ở test, % effort rework, số sự cố khách báo. ① Thống nhất định nghĩa giữa các dự án. ② Hiển thị xu hướng, không chỉ giá trị tuần này. ③ Ngưỡng cảnh báo chung, dự án được điều chỉnh khi có lý do ghi rõ. ④ Mỗi dự án đỏ có một dòng giải thích và hành động. Bẫy: so số bug tuyệt đối giữa dự án 5 người và 60 người.
> 📘 PMP: Measurement performance domain (PMBOK 7): chỉ số phải có ý nghĩa và so sánh được; organizational process assets.

**Q684. Team bị chấm KPI "càng ít bug càng tốt"; PM phát hiện tester gộp nhiều lỗi vào 1 ticket, dev chuyển bug thành "câu hỏi Q&A". Xử lý thế nào?**
Đây là số đo bị thao túng do cách đánh giá. ① Xác nhận: lấy mẫu 30–50 ticket, đếm lỗi bị gộp và ghi sai loại. ② Sửa dữ liệu (tách, phân loại lại), báo số đã điều chỉnh cho lãnh đạo và khách kèm giải thích. ③ Đổi cách đánh giá: không phạt việc tìm ra bug; đánh giá dev bằng tỷ lệ lọt lỗi và rework, tester bằng độ phủ và lọt lỗi. ④ Quy định rõ: 1 hiện tượng = 1 ticket, tiêu chí phân biệt bug và Q&A. Bẫy: chỉ nhắc nhở mà giữ nguyên KPI cũ.
> 📘 PMP: Measurement performance domain (PMBOK 7): cạm bẫy đo lường (misusing metrics); build quality into processes and deliverables.

**Q685. Dự án migration hệ thống hợp đồng bảo hiểm nhân thọ: khách muốn báo cáo chất lượng dữ liệu sau mỗi lần diễn tập. Báo cáo gồm gì?**
① Đối chiếu số bản ghi nguồn và đích theo từng bảng (đối soát số bản ghi). ② Đối chiếu tổng tiền các trường trọng yếu như phí, số tiền bảo hiểm (đối soát số tiền). ③ Kiểm tra mẫu theo trường cho các loại hợp đồng đặc biệt (đã hủy, đang tạm dừng, nhiều điều khoản bổ sung). ④ Danh sách chênh lệch theo nguyên nhân, ngoại lệ đã được khách duyệt, xu hướng giữa các lần diễn tập. Tiêu chí go thường là 0 chênh lệch không giải thích được. Bằng chứng phải che dữ liệu cá nhân. Bẫy: chỉ đếm số dòng, không đối chiếu tiền.
> 📘 PMP: Control Quality cho deliverable dữ liệu; acceptance criteria đo được.
> 💡 Nhật: Khách tài chính Nhật coi một hợp đồng lệch số tiền là sự cố; chuẩn bị script đối chiếu và mẫu báo cáo từ lần diễn tập đầu.

**Q686. Sau go-live, hệ thống mới chạy song song với hệ thống cũ 1 tháng trước khi bàn giao vận hành. Báo cáo chất lượng cho khách thế nào?**
① Hằng ngày: kết quả so sánh đầu ra hai hệ thống (số giao dịch, số tiền, file xuất), chênh lệch và nguyên nhân. ② Sự cố theo mức độ, thời gian khôi phục, có tái diễn không. ③ Hiệu năng batch so với thời hạn vận hành. ④ Xu hướng ổn định so với tiêu chí kết thúc chạy song song đã thống nhất. Phân biệt lỗi do dự án với lỗi do vận hành hoặc dữ liệu. Bẫy: chỉ báo "không có sự cố" mà không chứng minh đầu ra hai bên khớp.
> 📘 PMP: Control Quality + Close Project or Phase: chuyển giao (transition) có tiêu chí.
> 💡 Nhật: Bàn giao vận hành thường kèm tiêu chí ổn định, ví dụ không có sự cố mức cao trong N tuần (tham khảo); thống nhất N từ trước.

**Q687. Mọi KPI chất lượng đều đạt ngưỡng nhưng khách vẫn nói "chất lượng kém" vì lỗi chính tả và thuật ngữ tiếng Nhật trên màn hình. Xử lý trong báo cáo thế nào?**
Bộ KPI đang bỏ sót **chất lượng cảm nhận**. ① Thu thập và phân loại phàn nàn: bao nhiêu điểm, loại gì (chính tả, thuật ngữ không thống nhất, bố cục). ② Thừa nhận với khách, không dùng KPI để phản bác. ③ Bổ sung biện pháp: checklist tiếng Nhật, BrSE kiểm tra màn hình và thông báo lỗi, bảng thuật ngữ thống nhất; thêm chỉ số "góp ý của khách theo loại" vào báo cáo. ④ Theo dõi đến khi giảm rõ. Bẫy: trả lời "theo số liệu thì chất lượng đã đạt".
> 📘 PMP: Focus on value (PMBOK 7): chất lượng là mức đáp ứng kỳ vọng của khách; Manage Stakeholder Engagement.
> 💡 Nhật: Cách viết không thống nhất là lỗi khách Nhật rất để ý dù không ảnh hưởng chức năng.

**Q688. Khách bảo hiểm B yêu cầu bằng chứng cho từng test case kiểm thử đơn vị (khoảng 3.000 case). Chuẩn bị và báo cáo thế nào?**
① Thống nhất trước với khách mẫu evidence: dạng (ảnh màn hình, log, dump DB), mức chi tiết, cách đặt tên, nơi lưu. ② Quy tắc che dữ liệu cá nhân trong bằng chứng. ③ Báo cáo: số case, case đạt, số bằng chứng tương ứng, độ phủ, bug phát hiện; QA nội bộ lấy mẫu kiểm tra bằng chứng trước khi gửi. ④ Lưu theo cấu trúc để khách tra được từ mã case. Bẫy: làm xong mới hỏi mẫu, phải chụp lại hàng nghìn ảnh; bằng chứng chứa dữ liệu thật.
> 📘 PMP: Plan Quality Management + Control Quality: verified deliverables có bằng chứng.
> 💡 Nhật: Khách Nhật coi evidence là một phần sản phẩm bàn giao; thiếu bằng chứng thì coi như chưa test.

**Q689. Khách ngân hàng A yêu cầu "0 bug trước go-live" và muốn báo cáo chất lượng chứng minh điều đó. Anh/chị phản hồi thế nào?**
Quản lý kỳ vọng bằng định nghĩa đo được. ① Làm rõ ý khách: 0 bug đã biết ở mức cao/trung, hay 0 bug tuyệt đối (không thể chứng minh)? ② Đề xuất tiêu chí: 0 bug mức cao và trung còn mở; bug mức thấp còn lại có danh sách, cách tránh và lịch sửa, được khách duyệt. ③ Báo cáo chất lượng theo đúng tiêu chí đó, kèm đánh giá rủi ro còn lại. ④ Ghi tiêu chí vào biên bản họp và kế hoạch. Bẫy: đồng ý "0 bug" rồi trước go-live phải giấu bug mức thấp.
> 📘 PMP: Plan Quality Management: tiêu chí chấp nhận đo được; Manage Stakeholder Engagement – quản lý kỳ vọng.
> 💡 Nhật: Danh sách lỗi đã biết kèm cách tránh là thông lệ được khách Nhật chấp nhận khi go-live.

## 6.6 Trạng thái RAG, ngưỡng dung sai và báo cáo "dưa hấu"

**Q690. Dự án mới chưa có định nghĩa màu trạng thái, mỗi PM tự chọn xanh/vàng/đỏ theo cảm giác. Anh/chị định nghĩa RAG và ngưỡng dung sai thế nào?**
RAG phải dựa trên **ngưỡng ghi trước** trong kế hoạch. Ví dụ tham khảo: xanh khi chênh lệch trong ±5% (SPI/CPI ≥ 0,95) và mốc chính đúng hạn; vàng khi chênh 5–10% hoặc mốc trễ nhưng có kế hoạch phục hồi khả thi trong quyền PM; đỏ khi chênh > 10% hoặc mốc chính chắc chắn trễ, cần cấp trên hoặc khách hỗ trợ. ① Thống nhất ngưỡng với khách và lãnh đạo từ đầu. ② Ghi định nghĩa màu ngay trên báo cáo. ③ Màu thể hiện **mức cần hành động**, không phải điểm của PM. Bẫy: không có ngưỡng nên kỳ nào cũng tranh cãi màu.
> 📘 PMP: Variance thresholds trong schedule management plan và cost management plan; Control Schedule, Control Costs.

**Q691. Lãnh đạo hỏi "báo cáo dưa hấu" là gì và làm sao nhận ra trong 12 dự án của khối. Anh/chị trả lời thế nào?**
"Dưa hấu" là báo cáo xanh bên ngoài, đỏ bên trong. Dấu hiệu: RAG tổng xanh nhiều tuần nhưng ngày dự báo mốc trôi dần; % tiến độ đứng ở 80–90%; issue tồn lâu tăng; case test bị chặn nhiều; OT cao; team né câu hỏi chi tiết. Nguyên nhân: màu do PM tự chấm, sợ bị phạt khi báo đỏ, chỉ dùng chỉ số trễ. Phòng ngừa: ngưỡng khách quan, thêm leading indicator, PMO kiểm tra chéo ngẫu nhiên một module, khen thưởng việc báo xấu sớm. Bẫy: chỉ đọc trang tóm tắt.
> 📘 PMP: Measurement performance domain (PMBOK 7): leading vs lagging indicators; minh bạch thông tin.

**Q692. PM một sub-team báo xanh 6 tuần liền, nhưng dữ liệu cho thấy OT trung bình 50 giờ/tháng/người. Anh/chị làm gì?**
Xanh mua bằng OT là **đỏ ẩn**. ① Kiểm tra dữ liệu OT theo người, theo tuần, xu hướng. ② Tính lại tiến độ nếu làm giờ chuẩn: SPI thật là bao nhiêu. ③ Đổi trạng thái sang vàng với ghi chú "đang duy trì bằng OT", nêu rủi ro kiệt sức, lỗi tăng, nghỉ việc. ④ Lập kế hoạch bền vững: ưu tiên lại việc, bổ sung người, giảm phạm vi qua CR nếu cần; tuân thủ giới hạn giờ làm theo quy định lao động. Từ nay OT là chỉ số chuẩn trong báo cáo. Bẫy: khen team "chịu khó" và giữ màu xanh.
> 📘 PMP: Leading indicators; Manage Team; Monitor and Control Project Work.

**Q693. Lãnh đạo nội bộ ban hành quy định "dự án đỏ thì PM bị xem xét đánh giá hiệu suất". Anh/chị góp ý thế nào?**
Quy định này **khuyến khích báo cáo dưa hấu**. ① Nêu hệ quả: PM giấu màu đỏ đến khi không giấu được, mất thời gian cứu dự án. ② Đề xuất tách: màu RAG phản ánh trạng thái dự án; đánh giá PM dựa vào phát hiện sớm, chất lượng phương án, mức độ phục hồi. ③ Màu tính tự động theo ngưỡng, PM không tự chọn. ④ Ghi nhận PM báo đỏ sớm có kế hoạch tốt. Nếu công ty có dữ liệu, so chi phí cứu dự án "đột ngột đỏ" với dự án báo vàng sớm để thuyết phục. Bẫy: góp ý bằng cảm tính.
> 📘 PMP: Measurement performance domain: cạm bẫy đo lường làm sai lệch hành vi; demonstrate leadership behaviors – tạo môi trường an toàn để báo vấn đề.

**Q694. Khách bảo hiểm B hỏi vì sao báo cáo tuần này chuyển từ xanh thẳng sang đỏ mà không qua vàng. Trả lời và xử lý thế nào?**
Đây là dấu hiệu **phát hiện muộn**. ① Trả lời thật: nguyên nhân là sự kiện đột xuất (khách đổi yêu cầu lớn, server hỏng) hay vấn đề tích tụ mà chỉ số không bắt được. ② Nếu là tích tụ: thừa nhận, chỉ ra tín hiệu đã bỏ lỡ (Q&A tồn tăng, case bị chặn). ③ Bổ sung leading indicator vào báo cáo và quy tắc "2 tuần liên tiếp xấu đi thì chuyển vàng". ④ Báo kế hoạch phục hồi có mốc kiểm tra. Bẫy: giải thích dài để bảo vệ màu xanh cũ.
> 📘 PMP: Monitor Communications; cập nhật lessons learned về hệ thống chỉ số.
> 💡 Nhật: Khách Nhật đánh giá rất thấp chuyện "đột nhiên đỏ"; báo vàng sớm kèm điểm đáng lo là cách được tin tưởng.

**Q695. Báo cáo tháng có tiến độ đỏ, chi phí xanh, chất lượng xanh; một PM đề xuất RAG tổng là vàng vì "trung bình". Đúng không?**
Không. RAG tổng theo **quy tắc**, không lấy trung bình. Ví dụ: tổng đỏ nếu có trục đỏ ảnh hưởng mốc hợp đồng; tổng vàng nếu có trục vàng; còn lại xanh. Trục chất lượng cũng cần quy tắc riêng: đỏ nếu còn bug mức cao mở tại mốc hoặc lọt lỗi vượt ngưỡng; vàng nếu chỉ số lệch ngưỡng một phía hoặc chưa hội tụ. ① Ghi quy tắc vào kế hoạch. ② Báo cáo hiển thị từng trục và màu tổng. Bẫy: "vàng trung bình" khiến lãnh đạo không thấy mốc hợp đồng sắp trễ.
> 📘 PMP: Định nghĩa quy tắc tổng hợp trạng thái trong kế hoạch; Monitor and Control Project Work.

**Q696. Ngưỡng ±5%/±10% đang áp dụng cho cả dự án; sắp tới là ngày chuyển đổi thật với cửa sổ 30 giờ. Có dùng tiếp ngưỡng này không?**
Ngưỡng phải **tailoring theo bối cảnh**. Trong ngày cutover, đơn vị là phút/giờ: mỗi bước trong quy trình chuyển đổi từng bước có thời gian kế hoạch và buffer; vượt buffer của bước critical là đỏ ngay và kích hoạt quyết định tại các điểm go/no-go. Với dự án nhỏ 5 người, ngưỡng tuyệt đối (trễ từ 3 ngày) dễ dùng hơn % (tham khảo). ① Xác định đơn vị đo theo hoạt động. ② Ghi ngưỡng riêng cho từng giai đoạn. ③ Thông báo khách trước. Bẫy: báo "chậm 4%" trong cutover khi đã mất 1 giờ ở bước không có buffer.
> 📘 PMP: Tailoring (PMBOK 7): điều chỉnh ngưỡng và cách đo theo bối cảnh.
> 💡 Nhật: Ngày cutover, khách Nhật thường yêu cầu báo theo mốc giờ cố định (ví dụ 1–2 giờ một lần, tham khảo) theo đúng bước trong quy trình chuyển đổi từng bước.

**Q697. Lãnh đạo nội bộ dùng ngưỡng ±5%, nhưng khách ngân hàng A yêu cầu ngưỡng ±3% cho báo cáo gửi họ. Xử lý thế nào?**
① Ghi nhận yêu cầu khách vào communications plan; báo cáo cho khách dùng ngưỡng của khách. ② Tránh cùng một tuần có hai màu: đề xuất dùng ngưỡng chặt hơn cho cả báo cáo nội bộ của dự án này, hoặc ghi rõ màu theo chuẩn nào. ③ Báo lãnh đạo: dự án này sẽ vàng thường xuyên hơn, không có nghĩa xấu hơn dự án khác. ④ Đánh giá lại ngưỡng sau 1 tháng cùng khách. Bẫy: báo khách vàng nhưng nội bộ xanh, lãnh đạo không chuẩn bị khi khách phàn nàn.
> 📘 PMP: Plan Communications Management theo yêu cầu stakeholder; tailoring.

**Q698. Anh/chị nhận dự án giữa chừng khi PM cũ chuyển đi; báo cáo luôn xanh, nhưng sau 1 tuần rà soát anh/chị đánh giá thực tế trễ khoảng 3 tuần. Làm gì?**
① Đánh giá lại nhanh có bằng chứng (1–2 tuần): đếm việc còn lại, tốc độ thực tế, issue, chất lượng; ra dự báo. ② Báo lãnh đạo nội bộ trước, thống nhất thông điệp và nguồn lực cần. ③ Báo khách kết quả đánh giá, ngày dự báo, kế hoạch phục hồi; không đổ lỗi PM cũ, trình bày là "kết quả rà soát theo cách đo mới". ④ Thiết lập cách đo khách quan để không tái diễn. Bẫy: tiếp tục báo xanh vài tuần để "ổn định" rồi mới nói, khi đó trách nhiệm thành của mình.
> 📘 PMP: Monitor and Control Project Work; PMI Code of Ethics – honesty; Manage Stakeholder Engagement.
> 💡 Nhật: Đổi PM là thời điểm khách Nhật dễ chấp nhận đánh giá lại; trình bày như đánh giá lại dưới cơ cấu mới kèm số liệu cụ thể.

**Q699. Dự án đang ở thiết kế cơ bản; SPI và mốc chỉ báo khi đã trễ. Anh/chị dùng chỉ số dẫn báo (leading indicator) nào để phát hiện vàng sớm?**
Leading indicator cho giai đoạn thiết kế: ① Số câu Q&A mở và tuổi trung bình; ② Tốc độ hoàn thành tài liệu mỗi tuần so kế hoạch; ③ Số góp ý review trên mỗi trang đang tăng; ④ Thời gian khách duyệt tài liệu; ⑤ mức tham gia của người chủ chốt phía khách. Đặt ngưỡng cảnh báo, ví dụ Q&A quá hạn hơn 10 câu hoặc tuổi trung bình trên 5 ngày thì vàng (tham khảo). Đưa vào báo cáo tuần cùng chỉ số trễ. Bẫy: chỉ dùng SPI, đến khi SPI xấu thì đã mất vài tuần.
> 📘 PMP: Measurement performance domain (PMBOK 7): leading vs lagging indicators.

**Q700. PMO muốn RAG được tính tự động từ tool, còn các PM muốn tự đánh giá vì "số không nói hết". Anh/chị đề xuất cách nào?**
Kết hợp cả hai. ① Màu gốc tính tự động từ ngưỡng (SPI, CPI, mốc, bug). ② PM được điều chỉnh màu nhưng phải ghi lý do có bằng chứng: ví dụ đã có kế hoạch phục hồi được khách duyệt, hoặc ngược lại thấy rủi ro mà chỉ số chưa phản ánh. ③ Hiển thị cả màu tự động và màu PM khi khác nhau. ④ PMO rà định kỳ các lần điều chỉnh; PM nào luôn nâng màu là tín hiệu cần kiểm tra. Bẫy: hoàn toàn tự động thì bỏ qua phán đoán; hoàn toàn chủ quan dễ thành dưa hấu.
> 📘 PMP: Data analysis kết hợp expert judgment trong Monitor and Control Project Work.

**Q701. Mọi chỉ số của dự án đều xanh, nhưng PM lo vì trưởng phòng mới phía khách ít tham gia và chưa duyệt bản yêu cầu cuối. Báo màu gì và trình bày thế nào?**
Không đổi chỉ số, nhưng nêu rõ nhận định. ① Tách trong báo cáo: phần **fact** (chỉ số xanh) và phần **nhận định** của PM (rủi ro stakeholder). ② Đưa rủi ro vào top rủi ro mức vàng kèm bằng chứng: trưởng phòng vắng 3/4 buổi họp, 5 tài liệu chờ duyệt quá 2 tuần. ③ Đề xuất hành động: buổi giới thiệu dự án riêng cho trưởng phòng mới, xác nhận lại ai có quyền duyệt. ④ Theo dõi đến khi trưởng phòng tham gia đều. Bẫy: giữ xanh vì "chỉ là linh cảm", hoặc báo đỏ khi không có số.
> 📘 PMP: Stakeholder engagement assessment matrix; Monitor Stakeholder Engagement.
> 💡 Nhật: Tách rõ sự thật và nhận định cá nhân trong báo cáo; khách Nhật đánh giá cao sự rõ ràng này.

## 6.7 Báo tin xấu cho khách Nhật và lãnh đạo

**Q702. Phỏng vấn viên hỏi: nguyên tắc báo tin xấu cho khách Nhật là gì? Anh/chị trả lời thế nào?**
① **Sớm**: báo ngay khi fact chính được xác nhận, không chờ có đủ giải pháp. ② **Kết luận trước**: chuyện gì, ảnh hưởng gì, mức độ. ③ **Fact có số**, tách rõ điều đã biết và chưa biết. ④ **Kèm đối sách**: biện pháp tạm thời đã làm, kế hoạch điều tra, giờ báo tiếp. Trình tự thường gặp: báo cáo nhanh đầu tiên → báo cáo tiếp theo → báo cáo cuối có nguyên nhân và phòng ngừa tái phát. Bẫy: chờ tìm ra nguyên nhân mới báo, để khách biết từ nguồn khác.
> 📘 PMP: Manage Communications: truyền thông kịp thời, minh bạch; escalation path.
> 💡 Nhật: "Tin xấu càng phải báo sớm" gần như là luật ngầm; khách Nhật tha thứ việc trễ, khó tha thứ việc giấu.

**Q703. Chiều thứ Năm PM phát hiện mốc giao tài liệu vào thứ Hai tới sẽ trễ 5 ngày; họp định kỳ với khách là thứ Ba tuần sau. Khi nào và báo thế nào?**
Không chờ họp định kỳ. ① Trong vài giờ: xác nhận phần còn lại, nguyên nhân sơ bộ, ngày dự báo mới. ② Báo quản lý trực tiếp nội bộ ngay. ③ Ngay thứ Năm hoặc sáng thứ Sáu: gọi điện đầu mối liên lạc, sau đó email tóm tắt: mốc trễ 5 ngày, ngày mới dự kiến, phần nào có thể giao trước, ảnh hưởng tới việc phía khách (review, UAT). ④ Kế hoạch phục hồi chi tiết trình bày tại họp định kỳ. Bẫy: sáng thứ Hai mới báo "chưa giao được", khách không kịp điều chỉnh người review.
> 📘 PMP: Escalation theo communications management plan; Control Schedule.

**Q704. Anh/chị cần gửi email báo trễ mốc cho đầu mối khách ngân hàng A. Cấu trúc email thế nào?**
Tiêu đề có [Báo cáo] và tên mốc. Thân email theo thứ tự: ① Kết luận (mốc nào, trễ bao nhiêu, ngày mới dự kiến); ② Nguyên nhân dạng fact; ③ Ảnh hưởng tới mốc sau và việc khách cần làm; ④ Đối sách tạm thời và lâu dài; ⑤ lời xin lỗi nếu lỗi thuộc phía mình; ⑥ thời điểm báo cáo tiếp theo. BrSE kiểm tra tiếng Nhật, PM kiểm tra số liệu trước khi gửi. Bẫy: mở đầu bằng giải thích dài, kết luận nằm cuối email.
> 📘 PMP: Manage Communications: chọn phương thức và cấu trúc thông điệp để giảm nhiễu (communication model).
> 💡 Nhật: Gọi điện báo trước rồi gửi email để lưu vết thường được khách Nhật đánh giá là có thành ý; chỉ gửi email cho tin xấu lớn dễ bị coi là thiếu lịch sự.

**Q705. Một sự cố làm trễ mốc giao: PM nên báo lãnh đạo nội bộ trước hay báo khách trước?**
Thường báo **lãnh đạo nội bộ trước, rất nhanh** (cùng ngày, trong vài giờ) để công ty thống nhất thông điệp và hỗ trợ. Nhưng không để việc chờ ý kiến nội bộ làm chậm báo khách khi sự việc ảnh hưởng trực tiếp vận hành của khách (sự cố production, rò rỉ dữ liệu) hoặc hợp đồng quy định thời hạn báo. ① Xác định loại sự việc và nghĩa vụ hợp đồng. ② Báo nội bộ ngắn gọn ngay. ③ Đặt giới hạn thời gian; quá hạn vẫn gửi khách báo cáo nhanh đầu tiên với fact đã xác nhận. ④ Ghi quy tắc này vào communication plan để lần sau không phải hỏi.
> 📘 PMP: Escalation path trong communications management plan; Manage Stakeholder Engagement.
> 💡 Nhật: Lãnh đạo nội bộ nghe tin xấu từ khách trước khi nghe từ PM là lỗi báo cáo – liên lạc – trao đổi nghiêm trọng, ảnh hưởng uy tín cả công ty với khách.

**Q706. Dự án trọn gói 20 người với khách sản xuất D: EAC mới cho thấy lợi nhuận gộp từ +18% thành −5%. Anh/chị báo lãnh đạo nội bộ thế nào?**
① Xác nhận số: EAC tính từ dưới lên, kiểm tra lại với các leader, không chỉ ngoại suy CPI. ② Báo trong ngày bằng 1 trang: kết luận (dự báo lỗ 5%, quy ra man-day), nguyên nhân có số (ước lượng thiếu ở module nào, rework bao nhiêu), các phương án và hiệu quả (tăng năng suất, CR phần ngoài phạm vi, điều chỉnh nhân sự), quyết định cần lãnh đạo. ③ Đề xuất điểm kiểm tra 2 tuần một lần. ④ Phân tích gốc rễ estimate để áp dụng cho dự án sau. Bẫy: chờ thêm số liệu "cho chắc" đến khi hết đường xoay xở.
> 📘 PMP: Control Costs: forecasting; escalate khi vượt ngưỡng ủy quyền; PMI Code of Ethics – responsibility.

**Q707. Dự án dự báo trễ 10 ngày; lãnh đạo nội bộ muốn "chờ thêm 1 tuần xem có cứu được không" rồi mới báo khách. Anh/chị xử lý thế nào?**
① Đánh giá: xác suất cứu được trong 1 tuần là bao nhiêu (có số), trễ ảnh hưởng gì tới kế hoạch của khách (nhân sự UAT, cuối năm tài chính (tháng 3)). ② Trình lãnh đạo hệ quả của việc chờ: khách mất 1 tuần chuẩn bị; nếu không cứu được thì vừa trễ vừa mất tin tưởng. ③ Đề xuất cách trung thực mà không bi quan: báo ngay dạng dự báo "có khả năng trễ tối đa 10 ngày; đang thực hiện biện pháp X; kết luận vào ngày Y". ④ Ghi lại quyết định cuối cùng. Bẫy: im lặng theo lãnh đạo dù biết khách sẽ bị ảnh hưởng.
> 📘 PMP: Manage Stakeholder Engagement; PMI Code of Ethics – honesty; cảnh báo sớm.

**Q708. Anh/chị định báo một tin xấu lớn ngay tại steering committee có lãnh đạo cấp cao của khách, trong khi đầu mối khách chưa được biết trước. Có nên không?**
Không nên. ① Trước họp, trao đổi riêng trước với từng người liên quan với đầu mối liên lạc và trưởng phòng: chia sẻ fact, ảnh hưởng, đối sách; thống nhất thông điệp và ai trình bày phần nào. ② Chuẩn bị Q&A cho các câu hỏi có thể đến từ ban giám đốc. ③ Tại họp, trình bày đúng thông điệp đã thống nhất; nếu tin xấu phát sinh sát giờ, gặp đầu mối liên lạc trước họp dù chỉ 10 phút. ④ Sau họp, xác nhận lại với đầu mối liên lạc các việc tiếp theo. Bẫy: lần đầu tiên đầu mối liên lạc nghe tin xấu là trước mặt cấp trên của họ.
> 📘 PMP: Manage Stakeholder Engagement: chuẩn bị trước với từng stakeholder chủ chốt.
> 💡 Nhật: Ở Nhật, họp cấp cao là nơi xác nhận điều đã thống nhất, không phải nơi gây bất ngờ; làm đầu mối liên lạc mất mặt thì hợp tác về sau rất khó.

**Q709. PM không nói tiếng Nhật, phải báo trễ cho khách qua cuộc gọi có phiên dịch. Làm sao để thông điệp không bị truyền đạt sai mức độ?**
① Chuẩn bị trước thông điệp chính bằng tiếng Nhật dạng viết (kết luận, số, đối sách), BrSE kiểm tra. ② Brief phiên dịch trước cuộc gọi: mức độ nghiêm trọng, các từ không được làm mềm (ví dụ "sẽ trễ" khác "có khả năng trễ"). ③ Trong cuộc gọi chia sẻ màn hình tài liệu để số liệu không phụ thuộc lời dịch. ④ Ngay sau cuộc gọi gửi email tóm tắt bằng tiếng Nhật, đề nghị khách xác nhận đã hiểu đúng. Bẫy: "sẽ trễ" bị dịch thành "có khả năng trễ", khách hiểu là chưa chắc trễ.
> 📘 PMP: Manage Communications: giảm nhiễu trong mô hình truyền thông; xác nhận phản hồi (feedback).
> 💡 Nhật: Comtor (communicator – phiên dịch dự án) thường có xu hướng nói mềm để giữ hòa khí; với tin xấu, sự chính xác quan trọng hơn sự êm tai.

**Q710. Một tuần sau go-live, team phát hiện batch migration đã bỏ sót 230 hợp đồng bảo hiểm nhân thọ, chưa chuyển sang hệ thống mới. Báo cáo thế nào?**
① Xác nhận nhanh phạm vi: hợp đồng nào, có ảnh hưởng thu phí, chi trả quyền lợi, thư gửi người được bảo hiểm không. ② Báo ngay nội bộ và gửi khách báo cáo nhanh đầu tiên trong vài giờ: fact đã biết, chưa biết, biện pháp tạm thời đề xuất, giờ báo cáo tiếp theo. ③ Thực hiện biện pháp tạm thời như xử lý thủ công khi khách duyệt; lập kế hoạch chuyển bổ sung có đối chiếu. ④ Báo cáo sự cố: nguyên nhân gốc (vì sao đối chiếu không bắt được), biện pháp lâu dài, rà soát và áp dụng sang các batch khác. Bẫy: tự chạy lại batch trên production khi chưa được duyệt.
> 📘 PMP: Issue log + root cause analysis; mọi thao tác trên production đi qua Perform Integrated Change Control.
> 💡 Nhật: Sai sót ảnh hưởng người được bảo hiểm có thể kéo theo nghĩa vụ báo cáo của khách với cơ quan quản lý; khách cần thông tin sớm để tự quyết.

**Q711. Đây là lần thứ 3 trong 2 tháng PM phải báo khách bảo hiểm B dời ngày giao; khách bắt đầu không tin dự báo. Lần này làm gì khác?**
Vấn đề giờ là **uy tín dự báo**. ① Phân tích vì sao 3 lần dự báo sai: lạc quan, không tính rủi ro, đo tiến độ chủ quan. ② Lập lại kế hoạch từ dưới lên dựa trên tốc độ thực tế, có buffer rõ ràng; nếu cần thì re-baseline qua change control. ③ Chia mốc nhỏ hằng tuần mà khách tự kiểm được (số tài liệu giao, số case xong). ④ Mời lãnh đạo nội bộ cùng trình bày để thể hiện cam kết. Bẫy: đưa ngày mới lạc quan lần thứ tư.
> 📘 PMP: Control Schedule; re-baseline qua Perform Integrated Change Control; xây lại niềm tin stakeholder.
> 💡 Nhật: Khách Nhật có thể yêu cầu cấp trên của vendor giải trình; chủ động đề nghị lãnh đạo tham dự thể hiện thành ý.

**Q712. Khi báo sự cố cho khách Nhật, PM nên phân biệt "xin lỗi" với "nhận trách nhiệm hợp đồng" thế nào?**
Lời xin lỗi vì gây phiền cho khách là phép lịch sự được mong đợi; nhưng nhận định về **trách nhiệm hợp đồng, bồi thường** (bồi thường thiệt hại) cần lãnh đạo và pháp lý nội bộ thống nhất. ① Xin lỗi về ảnh hưởng và cam kết hành động. ② Trình bày fact, chưa kết luận lỗi thuộc bên nào khi chưa phân tích xong. ③ Khi khách hỏi về bồi thường: ghi nhận, hẹn trả lời sau khi nội bộ xem xét. ④ Ghi chép cẩn thận những gì đã nói. Bẫy: viết trong email "lỗi hoàn toàn của chúng tôi, chúng tôi chịu mọi chi phí".
> 📘 PMP: Manage Communications + Control Procurements: hiểu điều khoản hợp đồng trước khi cam kết.
> 💡 Nhật: "xin lỗi vì đã gây phiền hà" (nói bằng tiếng Nhật) là xin lỗi vì gây phiền, không đồng nghĩa thừa nhận toàn bộ trách nhiệm hợp đồng.

**Q713. Sau khi đã báo tin xấu và trình kế hoạch phục hồi, PM cần theo dõi và báo cáo gì tiếp?**
① Thực hiện đúng các mốc báo cáo tiếp theo đã hứa, kể cả khi chưa có tiến triển (báo "chưa có tiến triển, lý do, giờ báo tiếp"). ② Theo dõi kế hoạch phục hồi bằng điểm kiểm tra có số, đưa vào bảng quản lý vấn đề và báo cáo tuần. ③ Đóng vấn đề bằng báo cáo kết thúc: kết quả, nguyên nhân, phòng ngừa. ④ Hỏi đầu mối liên lạc cảm nhận về cách xử lý, ghi lessons learned. Bẫy: báo xong rồi im lặng, để khách phải hỏi lại "tình hình thế nào rồi".
> 📘 PMP: Monitor Communications; Monitor Stakeholder Engagement.

**Q714. Trong cuộc họp báo trễ, trưởng phòng khách yêu cầu PM cam kết ngay "không trễ thêm ngày nào nữa". Trả lời thế nào?**
Không hứa khi chưa phân tích. ① Thừa nhận mối lo của khách và nhắc lại những gì đã chắc chắn. ② Cam kết điều mình kiểm soát được: nộp kế hoạch lại có căn cứ vào ngày cụ thể (ví dụ trong 2 ngày làm việc), kèm mức độ tin cậy và giả định. ③ Nếu khách vẫn ép, nêu điều kiện: "giữ được ngày này nếu A, B được bảo đảm". ④ Sau họp, phân tích thật và trả lời đúng hạn. Bẫy: hứa ngay để kết thúc cuộc họp căng thẳng, tuần sau lại báo trễ.
> 📘 PMP: Ước lượng có độ tin cậy và giả định (Estimate Activity Durations); PMI Code of Ethics – honesty.
> 💡 Nhật: "xin mang về xem xét" (nói bằng tiếng Nhật) là câu trả lời hợp lệ, nhưng phải hẹn ngày trả lời cụ thể và giữ đúng hẹn.

## 6.8 Khi số liệu lệch nhau và áp lực "làm đẹp" số

**Q715. Trong kiểm thử chấp nhận, khách báo đã phát hiện 85 bug, còn số trên tool nội bộ là 52. Xử lý thế nào?**
① Đối chiếu từng mục theo ID hoặc mô tả, lập bảng ghép hai danh sách. ② Phân loại phần chênh: trùng lặp, câu hỏi spec, yêu cầu mới, lỗi môi trường/dữ liệu, ngoài phạm vi, bug thật bị sót. ③ Họp phân loại chung với khách theo tiêu chí đã thống nhất, không tranh luận trong họp định kỳ. ④ Báo một con số đã thống nhất kèm bảng phân loại; bug thật bị sót thì nhận và sửa. Phòng ngừa: một danh sách chung, một quy trình ghi nhận. Bẫy: mỗi bên giữ số của mình.
> 📘 PMP: Control Quality + Manage Stakeholder Engagement: thống nhất định nghĩa số đo.
> 💡 Nhật: Khách Nhật hay ghi mọi góp ý review là "bug"; thống nhất phân loại sự cố/xác nhận spec/yêu cầu bổ sung/môi trường từ đầu UAT.

**Q716. Khách tính tiến độ thiết kế theo số màn hình hoàn thành được 40%, trong khi báo cáo nội bộ theo EV là 55%. Anh/chị giải thích và báo cáo thế nào?**
Hai cách đo đều đúng nhưng đo khác thứ. ① Giải thích: EV tính cả phần việc đang dở; khách chỉ đếm màn hình đã xong trọn vẹn. ② Khoảng chênh 15 điểm là tín hiệu: nhiều màn hình đang làm dở cùng lúc — rủi ro dồn việc cuối kỳ. ③ Thống nhất một cách đo chính thức trong kế hoạch (thường là cách khách hiểu được), cách còn lại làm thông tin bổ sung. ④ Hành động: giảm số việc dở dang song song, đóng từng màn hình. Bẫy: mỗi kỳ chọn cách đo nào cho số đẹp hơn.
> 📘 PMP: Measurement performance domain (PMBOK 7): thống nhất số đo với stakeholder; kiểm soát work in progress.

**Q717. Trước báo cáo chất lượng tháng, lãnh đạo nội bộ yêu cầu chuyển 15 bug khách phát hiện thành "thay đổi đặc tả" để chỉ số lọt lỗi đẹp hơn. Anh/chị xử lý thế nào?**
① Xem lại 15 mục theo tiêu chí phân loại đã thống nhất: mục nào thực sự khác tài liệu đã duyệt thì có bằng chứng và đưa khách xác nhận theo quy trình CR. ② Mục nào là bug thì giữ là bug; nói rõ với lãnh đạo không thể đổi nhãn. ③ Đề xuất cách bảo vệ uy tín đúng: báo số thật kèm phân tích nguyên nhân và đối sách — khách đánh giá cao điều này hơn số đẹp. ④ Nếu tiếp tục bị ép, escalate theo kênh tuân thủ của công ty và lưu lại trao đổi.
> 📘 PMP: PMI Code of Ethics – honesty; Control Quality dựa trên dữ liệu trung thực.

**Q718. Lãnh đạo bảo PM ghi bớt 300 giờ của dự án X (đang lỗ) sang dự án Y (theo công sức, đang lãi) để "cân" báo cáo quý. Anh/chị làm gì?**
Từ chối: đây là làm sai số liệu nội bộ, và với hợp đồng theo công sức là **tính tiền khách Y cho việc không làm cho họ**. ① Làm rõ yêu cầu (đôi khi lãnh đạo nói vội) và nêu thẳng hệ quả: vi phạm hợp đồng, rủi ro pháp lý, kiểm toán. ② Đề xuất cách đúng: báo lỗ thật của X kèm kế hoạch phục hồi, xin management reserve, xem lại phạm vi để đàm phán CR nếu có việc ngoài hợp đồng. ③ Nếu bị ép, báo qua kênh PMO hoặc tuân thủ. ④ Lưu email trao đổi. Bẫy: làm theo một lần "vì lãnh đạo bảo".
> 📘 PMP: PMI Code of Ethics – honesty, responsibility; stewardship (PMBOK 7).

**Q719. Dự án theo công sức: báo cáo nội bộ ghi 1.650 giờ trong tháng, hóa đơn gửi khách là 1.600 giờ; lãnh đạo hỏi vì sao lệch. Anh/chị xử lý thế nào?**
Chênh lệch có thể hợp lệ nhưng phải **giải thích được**. ① Đối chiếu: giờ không tính tiền theo hợp đồng (đào tạo nội bộ, họp nội bộ, rework do lỗi phía mình, giờ vượt trần chưa được duyệt), khác biệt ngày cut-off giữa timesheet và kỳ hóa đơn. ② Lập bảng đối chiếu từ 1.650 về 1.600 theo từng loại. ③ Nếu phát hiện hóa đơn tính thiếu hoặc thừa, báo khách và sửa. ④ Chuẩn hóa: mỗi task trong timesheet có cờ "tính tiền/không tính tiền". Bẫy: lãnh đạo tưởng thất thoát doanh thu, còn khách nếu thấy thì tưởng bị tính thừa.
> 📘 PMP: Control Costs: đối chiếu dữ liệu; tuân thủ điều khoản hợp đồng (Control Procurements).

**Q720. Giữa họp định kỳ, PMO khách nói họ tự tính từ tool chung ra SPI 0,82, trong khi báo cáo của PM ghi 0,93. Anh/chị phản ứng thế nào?**
Không tranh luận trong họp. ① Ghi nhận, đề nghị cùng rà phép tính ngay sau họp hoặc trong ngày. ② Kiểm tra các nguồn chênh thường gặp: thời điểm cut-off, task chưa cập nhật trạng thái trên tool, trọng số, task bị tính hai lần. ③ Nếu số của PM sai: đính chính công khai trong biên bản họp và báo cáo kỳ sau. Nếu số khách lệch do tool chưa cập nhật: đó vẫn là lỗi vệ sinh dữ liệu của team, phải sửa. ④ Thống nhất một cách tính chung. Bẫy: bảo vệ số của mình trước mặt trưởng phòng khách.
> 📘 PMP: Monitor Communications; minh bạch phương pháp tính (Measurement performance domain).

**Q721. Lãnh đạo muốn báo khách "lập trình hoàn thành 100%" trước steering committee cho khách yên tâm, trong khi còn 8/180 chương trình chưa xong kiểm thử đơn vị. Anh/chị xử lý thế nào?**
Không báo 100%. ① Lấy fact: 8 chương trình nào, còn thiếu gì, ngày xong dự kiến, có ảnh hưởng IT không. ② Đề xuất cách báo vẫn tích cực mà đúng: "lập trình hoàn thành 172/180 chương trình (96%); 8 chương trình còn lại xong UT trước ngày X, không ảnh hưởng mốc IT". ③ Giải thích với lãnh đạo: báo 100% rồi IT phát hiện thiếu thì mất tin tưởng ở cấp steering — rất khó lấy lại. ④ Lưu lại quyết định. Bẫy: báo 100% rồi lặng lẽ làm nốt.
> 📘 PMP: PMI Code of Ethics – honesty; Validate Scope: chỉ tuyên bố hoàn thành khi deliverable đã được kiểm.
> 💡 Nhật: Khách Nhật hiểu hoàn thành là xong hẳn kể cả UT và review; dùng sai từ này có thể bị coi là báo cáo sai sự thật.

**Q722. Anh/chị làm báo cáo tổng hợp cho chương trình 4 dự án và nghi một PM khác đang "làm đẹp" tiến độ (báo 85% trong khi tool chỉ ra 70%). Xử lý thế nào?**
① Kiểm tra fact trước: so số báo cáo với dữ liệu gốc (tool, bằng chứng), tránh kết luận vội. ② Trao đổi trực tiếp với PM đó, hỏi nguyên nhân chênh, đề nghị sửa. ③ Nếu không sửa, báo program manager hoặc PMO bằng dữ liệu, không bằng suy đoán động cơ. ④ Trong báo cáo tổng hợp của mình, không đưa số chưa xác minh: ghi "đang đối chiếu" thay vì dùng số đáng ngờ. Bẫy: im lặng vì "không phải việc của mình" — báo cáo tổng hợp sai thì người chịu trách nhiệm là mình.
> 📘 PMP: PMI Code of Ethics – responsibility (báo cáo hành vi thiếu trung thực qua kênh phù hợp); giải quyết ở cấp thấp nhất trước khi escalate.

**Q723. Đầu mối khách tự tổng hợp lại số liệu của dự án để báo cáo lên cấp trên của họ, nhưng dùng nhầm số cũ, làm dự án trông trễ hơn thực tế. Anh/chị làm gì?**
① Xác nhận chênh lệch cụ thể giữa tài liệu của đầu mối liên lạc và báo cáo của mình. ② Trao đổi riêng với đầu mối liên lạc, nhẹ nhàng: "số này có lẽ lấy từ bản tuần trước", đưa số đúng kèm nguồn. ③ Đề xuất hỗ trợ: từ nay PM cung cấp sẵn 1 trang số liệu theo đúng mẫu báo cáo nội bộ của khách để đầu mối liên lạc dùng trực tiếp. ④ Nếu số sai đã lên cấp trên và ảnh hưởng quyết định, cùng đầu mối liên lạc tìm cách đính chính. Bẫy: sửa công khai trong cuộc họp có cấp trên của đầu mối liên lạc.
> 📘 PMP: Manage Stakeholder Engagement: hỗ trợ stakeholder truyền đạt đúng thông tin trong tổ chức của họ.
> 💡 Nhật: Đầu mối liên lạc phải báo cáo lên trưởng phòng, ban giám đốc bằng tài liệu của họ; cung cấp sẵn tài liệu dùng được ngay là cách tạo tin tưởng rất hiệu quả.

**Q724. Tech lead chủ chốt đang có ý định nghỉ việc; lãnh đạo nội bộ yêu cầu không đưa rủi ro này vào báo cáo cho khách. Anh/chị xử lý thế nào?**
Cân bằng giữa bảo mật nhân sự và minh bạch. ① Thông tin cá nhân (ai, lý do, thương lượng lương) là nội bộ, không đưa khách. ② Nhưng nếu ảnh hưởng giao hàng là đáng kể, báo khách ở mức "rủi ro biến động nhân sự ở vai trò chủ chốt" kèm biện pháp: người dự phòng, chuyển giao kiến thức, tài liệu hóa. ③ Thống nhất cách diễn đạt với lãnh đạo, cho thấy cách này bảo vệ cả nhân viên lẫn quan hệ với khách. ④ Thực hiện biện pháp ngay. Bẫy: không báo gì, người đó nghỉ, khách biết dấu hiệu đã có từ trước.
> 📘 PMP: Monitor Risks + Manage Communications: mức chi tiết phù hợp, vừa tôn trọng vừa trung thực.

**Q725. Vendor hạ tầng do khách thuê báo "API xác thực đã xong", nhưng team không gọi được trên môi trường kiểm thử tích hợp. Báo cáo tổng hợp ghi thế nào?**
① Thu bằng chứng: log gọi API, mã lỗi, thời điểm, môi trường. ② Gửi PMO khách fact và ảnh hưởng (bao nhiêu case IT bị chặn, mấy ngày), đề nghị kiểm tra chung. ③ Đề xuất định nghĩa "xong" chung cho mọi điểm giao: đã triển khai lên môi trường IT và qua smoke test của bên sử dụng. ④ Trong báo cáo tổng, ghi điểm giao này là "chưa xác nhận" kèm rủi ro lịch, không ghi xanh theo báo cáo của vendor. Bẫy: tranh cãi trực tiếp với vendor mà không qua khách.
> 📘 PMP: Monitor and Control Project Work: quản lý điểm giao (interface); định nghĩa hoàn thành rõ ràng.

**Q726. Một PM trẻ hỏi: "Trình bày báo cáo cho đẹp khác gì làm đẹp số liệu?" Anh/chị trả lời thế nào?**
Được phép: chọn chỉ số liên quan **đã thống nhất từ trước**, đưa bối cảnh và xu hướng, nhấn mạnh điểm tích cực có số, trình bày kế hoạch phục hồi rõ ràng, dùng biểu đồ dễ đọc. Không được: đổi định nghĩa giữa chừng mà không nói, chọn khoảng thời gian có lợi, giấu mẫu số, đổi baseline chưa duyệt, bỏ tin xấu trọng yếu, đổi nhãn dữ liệu. Phép thử: nếu khách hoặc lãnh đạo xem dữ liệu gốc, họ có cảm thấy bị dẫn dắt sai không? Nếu có, đó là làm đẹp số. Bẫy: nghĩ rằng "không nói dối từng con số" là đủ trung thực.
> 📘 PMP: PMI Code of Ethics – honesty (không đưa thông tin gây hiểu lầm); cạm bẫy đo lường trong Measurement performance domain.

## 6.9 Họp định kỳ, báo cáo tháng, steering committee, review mốc

**Q727. Anh/chị chuẩn bị agenda cho họp định kỳ hằng tuần đầu tiên với khách bảo hiểm B. Agenda chuẩn gồm gì?**
Agenda 60 phút (tham khảo): ① Xác nhận biên bản họp kỳ trước và action item; ② Tiến độ (kế hoạch – thực tế, mốc, dự báo); ③ Chất lượng; ④ Vấn đề và rủi ro; ⑤ câu hỏi Q&A cần khách trả lời; ⑥ việc cần khách quyết định; ⑦ lịch sắp tới (giao hàng, review, nghỉ lễ). Tài liệu gửi trước 1 ngày; trong họp chỉ đi vào điểm cần thảo luận. Biên bản họp gửi trong 24 giờ để khách xác nhận. Bẫy: dùng 60 phút đọc lại báo cáo khách đã có trong tay.
> 📘 PMP: Manage Communications (meetings); Monitor Communications.
> 💡 Nhật: Biên bản họp là bằng chứng của các thỏa thuận; gửi trong ngày hoặc sáng hôm sau và đề nghị khách xác nhận bằng văn bản.

**Q728. Họp định kỳ với khách ngân hàng A thường kéo dài 2,5 giờ vì sa vào thảo luận kỹ thuật chi tiết, trưởng phòng khách bắt đầu vắng mặt. Cải thiện thế nào?**
① Timebox từng mục agenda, có người điều phối giữ giờ. ② Chủ đề kỹ thuật sâu đưa vào "parking lot", tách thành buổi riêng họp nhóm chuyên đề chỉ có người liên quan. ③ Gửi tài liệu trước để khách đọc, câu hỏi gửi trước bằng văn bản. ④ Họp định kỳ tập trung: tình trạng, vấn đề cần quyết, việc cần khách; kết luận của họp nhóm chuyên đề ghi vào biên bản họp chung. Bẫy: trưởng phòng khách ngồi 2 tiếng nghe thảo luận chi tiết rồi bỏ hẳn, các quyết định cấp trưởng phòng bị treo.
> 📘 PMP: Manage Communications: thiết kế cuộc họp hiệu quả, ground rules.

**Q729. Khách yêu cầu thêm báo cáo tháng ngoài báo cáo tuần. Báo cáo tháng khác báo cáo tuần ở điểm nào?**
Báo cáo tháng dành cho người nhận cấp cao hơn (trưởng phòng, steering), tập trung **xu hướng và quyết định**: ① Xu hướng tiến độ và dự báo các mốc 2–3 tháng tới; ② Tóm tắt EVM hoặc kế hoạch – thực tế effort (phần phù hợp với hợp đồng); ③ Xu hướng chất lượng; ④ Xu hướng mức rủi ro và top rủi ro; ⑤ quyết định cần cấp trưởng phòng; ⑥ tình trạng hợp đồng, nghiệm thu, thay đổi tổ chức dự án. Báo cáo tuần thì chi tiết vận hành. Bẫy: ghép 4 báo cáo tuần thành báo cáo tháng.
> 📘 PMP: Work performance reports theo cấp người nhận (Monitor and Control Project Work).

**Q730. Anh/chị chuẩn bị steering committee hằng quý cho chương trình migration của ngân hàng A. Chuẩn bị thế nào?**
Steering để **ra quyết định và định hướng**, không để nghe chi tiết. ① Xác định trước 2–3 quyết định cần steering (ưu tiên phạm vi, phương án go-live, nguồn lực phía khách). ② Tài liệu: tình trạng tổng, mốc chính và dự báo, ngân sách phần khách quan tâm, top rủi ro, từng quyết định có phương án và khuyến nghị. ③ Trao đổi riêng trước với từng thành viên quan trọng trước họp. ④ Biên bản ghi quyết định, người chịu trách nhiệm, hạn; theo dõi tiếp ở họp định kỳ. Bẫy: 40 slide tình trạng, hết giờ chưa ra quyết định nào.
> 📘 PMP: Governance (steering committee); Manage Stakeholder Engagement; escalation theo thẩm quyền.

**Q731. Cuối giai đoạn kiểm thử tích hợp có buổi review mốc với khách để quyết định có chuyển sang kiểm thử tổng hợp không. Báo cáo gì?**
Báo cáo theo **tiêu chí kết thúc giai đoạn** đã thống nhất từ đầu: ① Thực hiện 100% case, tỷ lệ đạt; ② Bug mở theo mức độ (0 mức cao), đường hội tụ; ③ Đánh giá chất lượng định lượng và định tính; ④ Deliverable đầy đủ (báo cáo test, bằng chứng); ⑤ danh sách lỗi đã biết kèm cách tránh; ⑥ điều kiện vào ST sẵn sàng (môi trường, dữ liệu, người). Kết luận đề xuất: đạt, đạt có điều kiện (ghi điều kiện và hạn), hoặc chưa đạt. Bẫy: chỉ trình "đã test xong" mà không đối chiếu tiêu chí.
> 📘 PMP: Phase gate review với exit criteria; Close Project or Phase, Validate Scope.
> 💡 Nhật: Họp đánh giá kết thúc giai đoạn với khách Nhật khá trang trọng; chuẩn bị tiêu chí đánh giá từ đầu giai đoạn.

**Q732. Trưởng phòng khách lần đầu dự họp định kỳ và hỏi một câu PM chưa chuẩn bị: "dữ liệu khách hàng có bao giờ rời khỏi mạng đóng không?". Trả lời thế nào?**
① Trả lời phần đã biết chắc bằng fact, không đoán. ② Phần chưa chắc: nói rõ sẽ xác nhận và trả lời trước ngày cụ thể (ví dụ trong 2 ngày làm việc), ghi vào action item. ③ Sau họp, trả lời bằng văn bản qua đầu mối liên lạc, kèm bằng chứng (quy trình, cấu hình, log truy cập nếu được phép). ④ Rút kinh nghiệm: trước buổi có lãnh đạo khách mới, hỏi đầu mối liên lạc mối quan tâm của họ, chuẩn bị bộ Q&A (bảo mật, rủi ro, nhân sự). Bẫy: trả lời "chắc chắn không" rồi sau phải đính chính.
> 📘 PMP: Manage Stakeholder Engagement; cập nhật stakeholder register khi có stakeholder mới.
> 💡 Nhật: Câu "Chúng tôi xác nhận rồi trả lời trước ngày…" được khách Nhật đánh giá cao hơn câu trả lời nhanh nhưng sai.

**Q733. Khách gửi lại biên bản họp đã sửa phần quyết định, nội dung khác với điều hai bên đã nói trong họp. Xử lý thế nào?**
① So với ghi chép của mình (và bản ghi âm nếu đã được đồng ý ghi). ② Liên hệ riêng đầu mối liên lạc, hỏi lý do: có thể hiểu khác nhau, hoặc khách điều chỉnh sau khi bàn nội bộ. ③ Thống nhất nội dung đúng; nếu khách thật sự đổi quyết định thì ghi là quyết định mới có ngày và đánh giá ảnh hưởng (có thể là CR). ④ Phòng ngừa: cuối mỗi họp đọc lại các quyết định để xác nhận, gửi biên bản họp trong 24 giờ, quản lý phiên bản. Bẫy: chấp nhận bản sửa trong im lặng, sau đó phạm vi đổi mà không có căn cứ.
> 📘 PMP: Manage Communications; decision log; Perform Integrated Change Control khi quyết định thay đổi.
> 💡 Nhật: Đọc soát cùng nhau các quyết định cuối buổi họp là thói quen tốt với khách Nhật.

**Q734. Họp online với khách có 12 người phía VN tham dự nhưng gần như chỉ PM và BrSE nói, khách nhận xét "không biết ai phụ trách gì". Thiết kế lại cuộc họp thế nào?**
① Thành phần theo vai trò: PM, BrSE, leader của phần được thảo luận; người khác đọc biên bản. ② Mỗi mục agenda có người trình bày được phân công và chuẩn bị trước; BrSE hỗ trợ ngôn ngữ. ③ Câu hỏi phức tạp gửi trước bằng văn bản tiếng Nhật. ④ Chia sẻ màn hình tài liệu, nói theo slide. Lợi ích: khách thấy đúng người phụ trách, leader phát triển kỹ năng làm việc với khách. Bẫy: 12 người im lặng, khách thấy lãng phí và nghi ngờ năng lực team.
> 📘 PMP: Plan Communications Management và Manage Communications: chọn đúng người tham gia và phương thức.

**Q735. Action item từ họp định kỳ hay bị quên, cả phía khách lẫn phía team. Quản lý thế nào?**
① Danh sách action item có mã, nội dung, owner là một người cụ thể (cả hai phía), hạn, trạng thái. ② Rà ở đầu mỗi họp định kỳ; mục quá hạn được đánh dấu, owner cập nhật lý do và hạn mới. ③ Mục kéo dài hoặc ảnh hưởng lịch thì chuyển vào bảng quản lý vấn đề. ④ Gửi danh sách kèm biên bản họp sau mỗi buổi. Owner không được là "team" hay "khách". Bẫy: action item chỉ nằm trong biên bản dạng văn xuôi, không ai theo dõi.
> 📘 PMP: Action item log/issue log; Monitor Communications.

**Q736. Steering committee họp quyết định go/no-go cho chuyển đổi thật; 2/10 tiêu chí chưa đạt (diễn tập vượt cửa sổ 2 giờ, 3 bug mức trung chưa sửa). Anh/chị trình bày khuyến nghị thế nào?**
① Trình từng tiêu chí đạt/chưa đạt với bằng chứng. ② Với 2 tiêu chí chưa đạt: rủi ro cụ thể (vượt cửa sổ 2 giờ có thể không kịp mở nghiệp vụ sáng thứ Hai; 3 bug ảnh hưởng nghiệp vụ nào), biện pháp giảm (rút ngắn bước nào, đã thử chưa; cách tránh bug). ③ Phương án: go có điều kiện (thêm điểm dừng, rollback đã diễn tập) hoặc hoãn N tuần, kèm chi phí hoãn. ④ Khuyến nghị của PM có lý do; quyết định thuộc steering vì khách chịu rủi ro kinh doanh; ghi biên bản.
> 📘 PMP: Decision-making dựa trên rủi ro; Monitor Risks; tiêu chí go/no-go.
> 💡 Nhật: Quyết định go/no-go của khách Nhật thường cần thủ tục trình ký nội bộ của họ; gửi tài liệu đánh giá trước vài ngày (tham khảo).

**Q737. Khách sản xuất D đề nghị hủy họp định kỳ vì "dự án đang ổn, chỉ cần email". Anh/chị phản hồi thế nào?**
① Đồng ý giảm nhưng không bỏ hẳn: đề xuất 30 phút hai tuần một lần cho rủi ro và quyết định; báo cáo tuần vẫn gửi bằng văn bản. ② Đặt quy tắc kích hoạt họp đột xuất khi có vấn đề vượt ngưỡng. ③ Ghi thay đổi vào communication plan và biên bản họp. ④ Xem lại sau 1 tháng. Lý do giữ nhịp tối thiểu: quyết định nhỏ không bị dồn, quan hệ được duy trì. Bẫy: hủy hẳn, đến khi có vấn đề thì không có kênh và khách đã mất bối cảnh.
> 📘 PMP: Monitor Communications: điều chỉnh tần suất theo nhu cầu; tailoring.

**Q738. Kết thúc giai đoạn thiết kế, khách và lãnh đạo nội bộ đều muốn có báo cáo nhìn lại giai đoạn. Báo cáo gồm gì?**
① Kế hoạch vs thực tế của giai đoạn: lịch, effort, chất lượng (có số). ② Điều làm tốt, điều chưa tốt, nguyên nhân gốc có bằng chứng. ③ Hành động cho giai đoạn sau, có owner và cách đo hiệu quả, áp dụng rà soát và áp dụng sang chỗ tương tự. ④ Hai phiên bản: bản cho khách (không có chi phí, lợi nhuận nội bộ) và bản nội bộ đầy đủ; cập nhật vào lessons learned register của công ty. Bẫy: chỉ ghi "cần cố gắng hơn", không có hành động đo được.
> 📘 PMP: Close Project or Phase; lessons learned register; Manage Project Knowledge.
> 💡 Nhật: Nhìn lại (retrospective) với khách Nhật hay dùng khung KPT (Keep – Problem – Try); khách thường đánh giá cao khi vendor tự nêu Problem trước.

## 6.10 Tình huống khó

**Q739. Dự án đã đỏ 8 tuần liền, tuần nào báo cáo cũng ghi "đang phục hồi"; khách và lãnh đạo bắt đầu không còn phản ứng với màu đỏ. Anh/chị làm gì?**
Đây là "mệt mỏi với màu đỏ". ① Đánh giá lại bằng số: khoảng cách so baseline 8 tuần qua thu hẹp hay nới rộng? Nếu nới rộng, kế hoạch phục hồi đã thất bại. ② Lập lại kế hoạch căn bản: re-baseline qua change control, cắt phạm vi theo MoSCoW, phát hành theo giai đoạn, hoặc bổ sung nguồn lực có số. ③ Escalate lên steering dưới dạng **yêu cầu quyết định**, không phải báo cáo tình trạng. ④ Đặt tiêu chí thoát đỏ có ngày. Bẫy: tiếp tục báo "đang phục hồi" tuần thứ 9.
> 📘 PMP: Perform Integrated Change Control (re-baseline); escalation; Monitor and Control Project Work.
> 💡 Nhật: Khách Nhật có thể yêu cầu kế hoạch cải thiện chính thức; chủ động nộp trước khi bị yêu cầu thể hiện tinh thần trách nhiệm.

**Q740. Dự án trễ 20 ngày; lãnh đạo nội bộ muốn báo khách nguyên nhân là "đặc tả thay đổi", trong khi phân tích cho thấy 12 ngày do năng suất nội bộ, 8 ngày do đặc tả thay đổi. Xử lý thế nào?**
① Chuẩn bị phân tích có bằng chứng: 12 ngày do ước lượng thiếu và rework; 8 ngày do đặc tả thay đổi (danh sách thay đổi, ngày, effort). ② Trình lãnh đạo rủi ro của việc quy hết cho khách: khách có dữ liệu riêng, phát hiện ra thì mất tin tưởng và mất luôn cơ sở đàm phán phần thật sự do khách. ③ Báo khách đúng tỷ lệ: phần do đặc tả xử lý theo quy trình CR; phần nội bộ nhận và trình đối sách. ④ Thống nhất thông điệp với lãnh đạo trước khi gửi. Bẫy: nhượng bộ để tránh va chạm với lãnh đạo.
> 📘 PMP: Root cause analysis; PMI Code of Ethics – honesty, fairness.

**Q741. Dự án theo công sức: khách yêu cầu hồ sơ kinh nghiệm từng thành viên, còn lãnh đạo nội bộ không muốn gửi vì team có nhiều junior hơn mức đơn giá đang tính. Anh/chị xử lý thế nào?**
Với hợp đồng theo công sức tính đơn giá theo cấp kỹ năng, khách có lý do chính đáng để biết năng lực có khớp hợp đồng không. ① Kiểm tra hợp đồng: có cam kết kinh nghiệm, kỹ năng theo vai trò không. ② Cung cấp hồ sơ kỹ năng **trung thực** theo mẫu thống nhất, chỉ thông tin cần thiết. ③ Nếu thực tế lệch cam kết: xử lý bằng điều chỉnh đơn giá, thay người hoặc kế hoạch kèm cặp có khách đồng ý — không phải bằng giấu. ④ Trình lãnh đạo rủi ro khi khai sai. Bẫy: nâng số năm kinh nghiệm trên hồ sơ.
> 📘 PMP: PMI Code of Ethics – honesty; tuân thủ hợp đồng; Manage Stakeholder Engagement.
> 💡 Nhật: Khai sai hồ sơ kỹ năng là vi phạm nghiêm trọng ở thị trường Nhật, có thể dẫn tới chấm dứt hợp đồng và ảnh hưởng mọi đơn hàng sau.

**Q742. PM tự phát hiện file tổng hợp tiến độ 3 tuần qua có công thức cộng trùng một sheet: đã báo khách 61%, thực tế chỉ 52%. Xử lý thế nào?**
① Xác minh: tính lại tiến độ 3 tuần bằng dữ liệu gốc, chốt số đúng. ② Báo lãnh đạo nội bộ ngay. ③ Chủ động gửi khách báo cáo đính chính: sai ở đâu, số đúng của 3 tuần, ảnh hưởng tới dự báo và kế hoạch, nguyên nhân, phòng ngừa. ④ Phòng ngừa: khóa công thức, kiểm tra chéo 2 người, đối chiếu tổng với tool; rà các báo cáo khác dùng cùng mẫu theo rà soát và áp dụng sang chỗ tương tự. Bẫy: âm thầm sửa từ tuần này, để số "tụt" 9 điểm không giải thích.
> 📘 PMP: PMI Code of Ethics – honesty; áp dụng kiểm soát chất lượng cho chính báo cáo; lessons learned.

**Q743. Trưởng phòng khách chỉ ra báo cáo ghi 1.200 test case "đã thực hiện" nhưng thư mục bằng chứng chỉ có 950. Anh/chị phản ứng và xử lý thế nào?**
Không bào chữa tại chỗ. ① Ghi nhận, hẹn kết quả điều tra trong thời hạn cụ thể (ví dụ 24 giờ). ② Điều tra 250 case chênh: bằng chứng chưa upload, hay case chưa thực sự chạy? ③ Nếu chưa chạy: thực hiện lại, sửa báo cáo, xin lỗi và giải thích; nếu chỉ thiếu upload: bổ sung và mời khách kiểm tra mẫu. ④ Gốc rễ: trạng thái "xong" được cập nhật trước khi có bằng chứng; phòng ngừa: chỉ cho chuyển "xong" khi có link bằng chứng, QA lấy mẫu hằng tuần. Bẫy: nói ngay "chắc do chưa upload" khi chưa kiểm.
> 📘 PMP: Control Quality: toàn vẹn của work performance data; root cause analysis.

**Q744. Dự án đang đỏ; đầu mối khách bảo hiểm B dặn PM "đừng báo đỏ lên trưởng phòng, để tôi tự xử lý", trong khi trưởng phòng yêu cầu báo cáo đúng tình trạng. Anh/chị làm gì?**
Tôn trọng kênh đầu mối liên lạc nhưng không báo sai. ① Hiểu lý do: đầu mối liên lạc muốn tự xử lý hay sợ bị đánh giá. ② Đề xuất thỏa thuận: cho đầu mối liên lạc thời hạn (ví dụ 1 tuần) và tiêu chí rõ để xử lý; báo cáo chính thức vẫn ghi đúng trạng thái, kèm câu "phía khách đang có biện pháp". ③ Giúp đầu mối liên lạc chuẩn bị giải thích cho trưởng phòng. ④ Nếu đầu mối liên lạc yêu cầu ghi sai màu: từ chối lịch sự, báo lãnh đạo nội bộ xin chỉ đạo, ghi chép lại. Bẫy: đồng ý giấu, khi trưởng phòng phát hiện thì cả PM và đầu mối liên lạc đều mất uy tín.
> 📘 PMP: Manage Stakeholder Engagement; PMI Code of Ethics – honesty; escalate theo quy trình.

**Q745. Lãnh đạo nội bộ muốn báo cáo tháng thể hiện dự án "rất tốt" để chào giai đoạn 2, trong khi khách đang phàn nàn về chất lượng. Anh/chị viết báo cáo tháng thế nào?**
① Báo cáo tháng phải đúng trước: nêu các phàn nàn chất lượng với số liệu, nguyên nhân, đối sách và tiến độ khắc phục. ② Giải thích với lãnh đạo: báo "rất tốt" khi khách đang phàn nàn sẽ khiến khách nghi cả đề xuất giai đoạn 2. ③ Đề xuất trình tự: khắc phục và chứng minh bằng số trong 1–2 tháng, sau đó mới chào giai đoạn 2. ④ Nếu giai đoạn 2 thật sự giải quyết gốc rễ (ví dụ tự động hóa test hồi quy), có thể nêu như một phương án kèm lợi ích rõ ràng. Bẫy: dùng báo cáo tình trạng làm tài liệu bán hàng.
> 📘 PMP: Focus on value (PMBOK 7); Manage Stakeholder Engagement; PMI Code of Ethics – honesty.
> 💡 Nhật: Khách Nhật chỉ mở rộng hợp tác khi tin vào chất lượng và cách xử lý của vendor; giai đoạn 2 thường được quyết từ cách xử lý phàn nàn hôm nay.

**Q746. Khi đàm phán một CR trong dự án trọn gói, khách yêu cầu công khai chi phí và lợi nhuận nội bộ để "kiểm tra giá có hợp lý không". Lãnh đạo không muốn. Anh/chị xử lý thế nào?**
① Xác nhận khách thật sự cần gì: thường là muốn biết giá CR có căn cứ. ② Với hợp đồng trọn gói, chi phí và lợi nhuận nội bộ không thuộc nghĩa vụ công khai; nhưng có thể minh bạch **căn cứ ước lượng**: phân rã công việc, effort từng hạng mục, đơn giá theo hợp đồng hoặc bảng giá đã thỏa thuận, giả định. ③ Xin lãnh đạo duyệt mức thông tin chia sẻ trước khi gửi. ④ Không đưa số giả để "trông hợp lý". Bẫy: từ chối thẳng khiến khách nghi ngờ, hoặc đưa hết chi phí nội bộ làm mất vị thế đàm phán.
> 📘 PMP: Manage Stakeholder Engagement + Control Procurements; minh bạch basis of estimates.
> 💡 Nhật: Khách Nhật thường hỏi căn cứ báo giá; bảng phân rã effort rõ ràng thường đủ thuyết phục mà không cần lộ lợi nhuận.

**Q747. Báo cáo chất lượng tuần có ảnh chụp bug chứa tên và số hợp đồng của người được bảo hiểm, đã gửi email cho 15 người, gồm cả người nội bộ ngoài phạm vi được phép. Xử lý thế nào?**
Đây là sự cố bảo mật: xử lý trước, báo cáo song song. ① Ngăn lan rộng: yêu cầu người nhận xóa và xác nhận đã xóa; thu hồi email nếu hệ thống cho phép. ② Báo ngay bộ phận bảo mật nội bộ và khách theo quy trình sự cố đã thỏa thuận, không chờ điều tra xong. ③ Xác định phạm vi: bao nhiêu bản ghi, loại dữ liệu, ai đã nhận, có chuyển tiếp không. ④ Gốc rễ: mẫu báo cáo cho phép chèn ảnh thô; phòng ngừa: quy tắc che dữ liệu, kiểm tra trước khi gửi, rà các báo cáo khác. Bẫy: tự đánh giá "ít người thấy" rồi không báo.
> 📘 PMP: Stewardship (PMBOK 7); issue log; Manage Communications với ràng buộc bảo mật.
> 💡 Nhật: Với ngành tài chính Nhật (tham chiếu các chuẩn như FISC), báo sự cố thông tin cá nhân trễ thường bị đánh giá nặng hơn bản thân sự cố.

**Q748. Cả lãnh đạo nội bộ và khách đều muốn giữ ngày go-live, nhưng dữ liệu tốc độ sửa bug và rủi ro cho thấy xác suất đạt chỉ khoảng 30%. Anh/chị trình bày thế nào?**
① Trình dữ liệu dự báo: phân tích kịch bản hoặc mô phỏng Monte Carlo từ tốc độ thực tế và rủi ro, ra xác suất đạt ngày khoảng 30%. ② Nêu "điều gì phải đúng" để đạt ngày: mỗi ngày phải đóng bao nhiêu bug, cần thêm bao nhiêu người. ③ Đưa phương án: giảm phạm vi go-live, go-live theo giai đoạn, dời ngày N tuần, hoặc giữ ngày với rủi ro chất lượng cụ thể ảnh hưởng người được bảo hiểm. ④ Khuyến nghị có lý do; quyết định thuộc sponsor/steering; ghi biên bản. Bẫy: im lặng theo mong muốn chung, không trình xác suất.
> 📘 PMP: Perform Quantitative Risk Analysis (Monte Carlo simulation); decision-making có phân tích phương án.
> 💡 Nhật: Go-live gắn với cuối năm tài chính (tháng 3) hoặc ngày áp dụng chế độ mới thường là ràng buộc cứng của khách Nhật; khi đó cắt phạm vi hoặc phát hành theo giai đoạn khả thi hơn dời ngày.

**Q749. PM mới nhận dự án phát hiện PM cũ đã báo khách "hoàn tất định nghĩa yêu cầu", nhưng 30% yêu cầu vẫn ghi TBD; hợp đồng trọn gói giai đoạn thiết kế đã ký dựa trên đó. Xử lý thế nào?**
① Xác minh: lập danh sách yêu cầu TBD, cái nào ảnh hưởng thiết kế, effort ước tính. ② Báo lãnh đạo nội bộ ngay vì liên quan hợp đồng đã ký (phạm vi, giá). ③ Với khách: trình bày như "danh sách hạng mục cần xác nhận để vào thiết kế", có hạn trả lời và ảnh hưởng nếu trễ; không đổ lỗi PM cũ. ④ Hạng mục xác nhận xong mà vượt phạm vi hợp đồng thì đi theo quy trình CR; ghi vào risk register và assumption log. Bẫy: tự điền giả định cho 30% TBD rồi vào thiết kế.
> 📘 PMP: Monitor and Control Project Work; Validate Scope; Perform Integrated Change Control.
> 💡 Nhật: Khách Nhật coi tài liệu định nghĩa yêu cầu đã duyệt là ranh giới trách nhiệm; phần chưa đủ mà đã báo "hoàn tất" phải được làm rõ bằng văn bản càng sớm càng tốt.

**Q750. Khách cần nghiệm thu trước cuối năm tài chính để dùng ngân sách, lãnh đạo nội bộ cần doanh thu; cả hai muốn PM ký báo cáo chất lượng ghi "đạt" dù còn 4 bug mức cao chưa sửa. Anh/chị làm gì?**
Không ký báo cáo sai, nhưng tìm con đường hợp lệ. ① Lấy fact: 4 bug ảnh hưởng nghiệp vụ nào, cách tránh tạm thời, ngày sửa. ② Báo cáo chất lượng ghi trung thực: đạt các tiêu chí trừ 4 bug, kèm đánh giá rủi ro và kế hoạch sửa. ③ Đề xuất hình thức nghiệm thu có điều kiện nếu hợp đồng và quy định của khách cho phép: nghiệm thu kèm danh sách tồn đọng và hạn hoàn thành. ④ Ghi rõ bằng văn bản, pháp lý hai bên kiểm tra. Bẫy: ký "đạt" vì hai phía đều muốn — bug xảy ra trên production thì người ký chịu trách nhiệm.
> 📘 PMP: PMI Code of Ethics – honesty; Validate Scope với điều kiện chấp nhận rõ ràng.
> 💡 Nhật: Khách Nhật cũng chịu áp lực ngân sách cuối năm tài chính (tháng 3); giúp họ có cách nghiệm thu hợp lệ là giải quyết đúng nhu cầu thật mà không phải làm sai báo cáo.
