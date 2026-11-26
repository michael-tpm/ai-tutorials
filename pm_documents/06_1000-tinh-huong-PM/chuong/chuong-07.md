# Chương 7 · Quy trình Waterfall kiểu Nhật, quản lý Q&A, báo cáo định kỳ và quản lý chất lượng bằng số liệu (Q751–Q875)

## 7.1 Tiêu chí vào/ra từng giai đoạn

**Q751. Khách bảo hiểm nhân thọ B, dự án migration hệ thống quản lý hợp đồng, kế hoạch bắt đầu Basic Design ngày 1/6 nhưng tài liệu định nghĩa yêu cầu còn 12 mục TBD và khách chưa ký phê duyệt. Tiêu chí vào giai đoạn Basic Design gồm gì, việc đầu tiên anh/chị làm là gì?**
Tiêu chí vào của Basic Design thường gồm: tài liệu định nghĩa yêu cầu đã được khách phê duyệt, TBD có người chịu trách nhiệm và hạn chốt, phạm vi đã baseline, nhân sự và môi trường sẵn sàng. Việc đầu tiên em làm là phân loại 12 TBD theo mức ảnh hưởng tới màn hình/batch. Nếu phần bị chặn khoảng ≤ 15% phạm vi (tham khảo), em đề xuất **bắt đầu có điều kiện**: thiết kế phần đã chốt trước, TBD đưa vào bảng quản lý Q&A có hạn trả lời, ghi rủi ro vào risk register và xin khách xác nhận điều kiện này trong biên bản họp.
> 📘 PMP: Phase gate thuộc Control Quality và Perform Integrated Change Control: đánh giá tiêu chí vào trước khi cho phép bắt đầu công việc, ngoại lệ phải được ghi nhận và chấp thuận.
> 💡 Nhật: Khách Nhật hay nói "cứ làm đi" (nói bằng tiếng Nhật) nhưng về sau vẫn tính phần làm lại do TBD là lỗi vendor; điều kiện bắt đầu phải nằm trên giấy.

**Q752. Ngân hàng A, team 20 người vừa viết xong tài liệu Basic Design gồm 180 trang cho 25 màn hình và 8 batch. Leader hỏi: "Khi nào được coi là xong Basic Design để chuyển sang Detail Design?". Anh/chị trả lời thế nào?**
Basic Design chỉ xong khi đạt **tiêu chí ra** đã ghi trong kế hoạch chất lượng: 100% tài liệu qua tự review, review chéo và review khách; góp ý review mức cao đã sửa và người review xác nhận đóng; mật độ góp ý review và tỷ lệ effort review nằm trong ngưỡng hoặc có giải thích; QA còn mở bằng 0 hoặc đều có hướng xử lý; traceability yêu cầu → thiết kế đủ 100%; khách phê duyệt bằng văn bản. Bằng chứng là phiếu ghi kết quả review, bảng truy vết và email/chữ ký duyệt. Bẫy hay gặp là coi "viết xong" là "xong giai đoạn": tài liệu chưa được khách duyệt thì Detail Design xây trên nền chưa chắc.
> 📘 PMP: Validate Scope và Control Quality: deliverable chỉ được chấp nhận khi thỏa tiêu chí chấp nhận đã thống nhất, có bằng chứng.
> 💡 Nhật: Ở nhiều khách Nhật, kết thúc giai đoạn được chốt trong họp đánh giá kết thúc giai đoạn; chuẩn bị sẵn check sheet tiêu chí ra để khách xác nhận từng dòng.

**Q753. Khách bảo hiểm phi nhân thọ C, Detail Design đã xong 95%, còn 5% (3 module tính phí) chưa review vì reviewer nghỉ ốm. Khách giục chuyển sang lập trình đúng hạn thứ Hai tuần sau. Anh/chị quyết định thế nào?**
Em xác nhận fact trước: 3 module tính phí chiếm bao nhiêu % quy mô code, có phụ thuộc module khác không. Sau đó em cho **chuyển lập trình từng phần**: 95% đã đạt tiêu chí ra thì bắt đầu đúng hạn; 3 module tính phí giữ lại, sắp xếp reviewer thay thế có kinh nghiệm nghiệp vụ phí trong 2–3 ngày, xong review mới cho code. Em báo khách ngay theo báo cáo – liên lạc – trao đổi: phần nào bắt đầu, phần nào chờ, ảnh hưởng tiến độ nếu có, và ghi ngoại lệ vào biên bản. Về phòng ngừa, em bố trí reviewer dự phòng (backup) cho các module rủi ro cao ngay từ kế hoạch.
> 📘 PMP: Manage Quality kết hợp rolling wave và fast-tracking có kiểm soát: chỉ chồng lấn phần đã đủ điều kiện, phần rủi ro cao giữ ở gate.
> 💡 Nhật: Module tính phí, tính lãi là "trái tim" của hệ thống với khách bảo hiểm; bỏ review ở đây để kịp ngày là thứ khách không tha thứ khi có lỗi.

**Q754. Dự án ngân hàng A, lập trình xong 40 KLOC. Leader báo "code xong rồi, chuyển UT được". Tiêu chí ra của lập trình nên kiểm những gì?**
Tiêu chí ra của lập trình thường gồm: build/compile thành công, warning ở mức đã thống nhất (vd 0 warning mức cao); chạy công cụ phân tích tĩnh và xử lý hết vi phạm mức cao; 100% source qua code review có phiếu ghi kết quả review; tuân thủ chuẩn coding; đặc tả UT đã viết và review; source đã lên kho quản lý cấu hình với tag rõ ràng. Em kiểm bằng số: tỷ lệ file đã review, số vi phạm tĩnh còn lại, mật độ góp ý review code review so ngưỡng. Bẫy là "xong code" theo lời leader nhưng thực ra chưa review, rồi bug dồn sang UT, IT và chi phí sửa tăng theo từng giai đoạn.
> 📘 PMP: Control Quality: dùng checklist và inspection để xác nhận deliverable đạt chuẩn trước khi chuyển sang hoạt động sau.

**Q755. Khách bảo hiểm B yêu cầu tiêu chí ra UT là C1 coverage 100%. Team 15 người báo C1 đạt 92%, phần còn lại là nhánh xử lý lỗi khó tạo điều kiện. Anh/chị xử lý ra sao?**
Em xem chi tiết 8% nhánh chưa phủ: thuộc module nào, là nhánh lỗi gì (timeout DB, file hỏng…). Với nhánh tạo được bằng stub/mock thì bổ sung test. Với nhánh thật sự không tạo được, em lập danh sách từng nhánh kèm lý do và **phương án thay thế**: review code bắt buộc cho nhánh đó, hoặc kiểm ở IT bằng cách giả lập lỗi. Em gửi khách danh sách này để xin chấp thuận ngoại lệ trước khi kết thúc UT, không tự ý coi 92% là đạt. Bài học cho dự án sau: thống nhất ngay từ kế hoạch chất lượng cách xử lý nhánh không phủ được.
> 📘 PMP: Plan Quality Management: tiêu chí chất lượng phải đo được và khả thi; ngoại lệ được xử lý qua quyết định có ghi nhận, không âm thầm hạ chuẩn.
> 💡 Nhật: Khách Nhật chấp nhận ngoại lệ có lý do rõ ràng và danh sách đầy đủ; điều họ không chấp nhận là phát hiện ra sau rằng vendor tự bỏ qua.

**Q756. Dự án migration cho ngân hàng A, kế hoạch bắt đầu IT ngày 15/9. Đến 13/9 còn 3 trong 20 module chưa xong UT, môi trường IT đã sẵn sàng. Tiêu chí vào IT là gì và anh/chị làm gì?**
Tiêu chí vào IT thường gồm: UT hoàn tất và có báo cáo kết thúc, bug UT mức cao đã đóng, đặc tả interface đã cố định, test spec IT đã review, môi trường và dữ liệu test sẵn sàng. Em lập ma trận: kịch bản IT nào chỉ dùng 17 module đã xong thì chạy trước từ 15/9; kịch bản đụng 3 module còn lại xếp sau, kèm ngày hoàn tất UT cam kết. Em báo khách đây là **bắt đầu có điều kiện**, nêu rủi ro (phải chạy lại một số case khi 3 module vào) và theo dõi hằng ngày. Gốc rễ cần tìm: vì sao 3 module trễ (ước lượng sai, phụ thuộc, nhân sự) để chỉnh kế hoạch còn lại.
> 📘 PMP: Control Schedule kết hợp phân tích phụ thuộc trong network diagram: sắp lại thứ tự hoạt động thay vì bỏ tiêu chí vào.
> 💡 Nhật: Khách Nhật thường hỏi "giai đoạn trước đã xong chưa" (nói bằng tiếng Nhật); bắt đầu có điều kiện phải kèm danh sách module chưa xong và ngày cam kết, không nói chung chung.

**Q757. Khách bảo hiểm phi nhân thọ C chuẩn bị ST. Môi trường ST chỉ bằng 1/4 cấu hình production, trong khi phạm vi ST có test hiệu năng batch đêm. Anh/chị đánh giá tiêu chí vào ST thế nào?**
Tiêu chí vào ST gồm: IT đã đạt tiêu chí ra và khách nhận báo cáo chất lượng, kịch bản ST theo nghiệp vụ đã duyệt, dữ liệu test gần thật (đã che thông tin cá nhân), môi trường tương đương production cho phần phi chức năng. Với môi trường 1/4, em tách phạm vi: chức năng chạy ngay; hiệu năng batch thì đề xuất (a) mượn môi trường production trước cutover, hoặc (b) đo trên môi trường nhỏ rồi ngoại suy, ghi rõ giới hạn. Em trình khách 2 phương án với chi phí, rủi ro để khách quyết, không tự nhận "đạt" trên môi trường không tương đương.
> 📘 PMP: Identify Risks và Plan Quality Management: điều kiện môi trường là giả định cần kiểm, khác biệt môi trường là rủi ro phải được xử lý có chủ đích.
> 💡 Nhật: Khách ngành tài chính thường hỏi thẳng "có tương đương production không" (hỏi bằng tiếng Nhật); câu trả lời mập mờ sẽ bị yêu cầu làm lại test.

**Q758. Khách bảo hiểm nhân thọ B lên lịch UAT trong 4 tuần. ST đã xong, nhưng tài liệu hướng dẫn vận hành chưa có và dữ liệu UAT chưa được che thông tin cá nhân. Anh/chị có cho bắt đầu UAT không?**
Em chưa cho bắt đầu toàn bộ. Tiêu chí vào UAT thường gồm: báo cáo chất lượng ST đã được khách chấp thuận, bug còn mở chỉ ở mức thấp và có workaround, môi trường UAT ổn định, tài liệu thao tác/vận hành cho người dùng khách, dữ liệu test hợp lệ về bảo mật. Dữ liệu chưa che thông tin cá nhân là điều kiện chặn tuyệt đối với ngành bảo hiểm, nên em ưu tiên hoàn tất masking và kiểm tra lại trước. Tài liệu vận hành có thể bổ sung song song trong tuần đầu nếu khách đồng ý. Em báo khách ngày bắt đầu mới, lý do, kế hoạch bù để không vượt mốc nghiệm thu.
> 📘 PMP: Plan Risk Responses: rủi ro tuân thủ (bảo mật dữ liệu) được xử lý bằng avoid trước khi bắt đầu, không chấp nhận tạm.

**Q759. Ngân hàng A muốn bắt đầu IT sớm 1 tuần để kịp cuối năm tài chính. UT mới đạt tỷ lệ đã chạy test 85%, bug mở 30 cái. Khách nói "rủi ro chúng tôi chịu". Anh/chị làm gì trước tiên?**
Việc đầu tiên là phân tích ảnh hưởng bằng số trước khi trả lời: 15% UT còn lại thuộc module nào, 30 bug mở có bao nhiêu bug mức cao, nếu IT bắt đầu sớm thì xác suất chạy lại case IT và công sức làm lại ước bao nhiêu MD. Sau đó em trình khách 2–3 phương án: bắt đầu sớm toàn bộ, bắt đầu sớm phần module sạch, hoặc giữ lịch cũ và tăng người để bù. Nếu khách chọn bắt đầu sớm, rủi ro và trách nhiệm phải ghi trong biên bản họp và có người có thẩm quyền xác nhận. "Rủi ro chúng tôi chịu" nói miệng chưa phải là chấp nhận rủi ro.
> 📘 PMP: Perform Integrated Change Control: đánh giá ảnh hưởng tới tiến độ, chi phí, chất lượng trước, sau đó người có thẩm quyền quyết định và ghi nhận.
> 💡 Nhật: Người nói "tôi chịu trách nhiệm" (nói bằng tiếng Nhật) có thể là người phụ trách không có quyền; cần xác nhận cấp trưởng bộ phận trở lên hoặc người ký hợp đồng.

**Q760. Dự án migration hệ thống tính phí của khách bảo hiểm B có giai đoạn kiểm chứng dữ liệu chuyển đổi trước ST. Tiêu chí ra cho phần kiểm chứng dữ liệu migration nên định nghĩa thế nào?**
Em định nghĩa tiêu chí ra bằng con số kiểm được: khớp 100% số bản ghi giữa hệ thống cũ và mới theo từng bảng; khớp tổng kiểm (sum check) cho các cột tiền như phí, số tiền bảo hiểm; kiểm mẫu chi tiết theo danh sách hợp đồng đại diện cho từng loại sản phẩm và trạng thái; 0 lỗi chuyển đổi ký tự (đặc biệt ký tự ngoài bảng mã chuẩn); thời gian chạy chuyển đổi nằm trong cửa sổ cutover. Bằng chứng là log đối chiếu tự động và bảng kết quả kiểm mẫu được khách xác nhận. Bẫy là chỉ đếm số bản ghi khớp mà không đối chiếu giá trị.
> 📘 PMP: Plan Quality Management: tiêu chí chấp nhận phải đo được; Control Quality dùng inspection và statistical sampling để kiểm chứng.
> 💡 Nhật: Khách bảo hiểm thường muốn tự chọn mẫu kiểm (hợp đồng có điều khoản đặc biệt, hợp đồng nhiều lần sửa đổi); nên mời khách chọn mẫu từ sớm để tiêu chí ra được khách tin.

**Q761. Dự án mới với khách sản xuất D, hợp đồng trọn gói, team 12 người. Ai xác định tiêu chí vào/ra từng giai đoạn, xác định khi nào, và ghi vào đâu?**
PM chủ trì xác định ngay từ lúc lập kế hoạch, trước khi bắt đầu định nghĩa yêu cầu, cùng bộ phận QA nội bộ dựa trên chuẩn công ty, rồi thống nhất với khách. Nội dung ghi trong kế hoạch chất lượng hoặc kế hoạch dự án: từng giai đoạn có tiêu chí vào, tiêu chí ra, chỉ số và ngưỡng (tham khảo baseline công ty), tài liệu đầu ra, người duyệt, hình thức họp kết thúc giai đoạn. Với hợp đồng trọn gói, tiêu chí ra của UAT gắn trực tiếp với điều kiện nghiệm thu nên phải khớp với hợp đồng. Bẫy là để đến lúc gần kết thúc giai đoạn mới bàn tiêu chí, khi đó hai bên sẽ tranh luận theo lợi ích chứ không theo chuẩn.
> 📘 PMP: Plan Quality Management tạo ra quality management plan và quality metrics; nguyên tắc tailoring của PMBOK 7 cho phép điều chỉnh chuẩn công ty theo dự án.
> 💡 Nhật: Khách Nhật lớn thường có chuẩn riêng; nên xin trước chuẩn của khách để đối chiếu với chuẩn công ty ngay từ đầu.

**Q762. ST của khách bảo hiểm phi nhân thọ C đạt tỷ lệ pass 98%, mọi chỉ số đều trong ngưỡng. Nhưng 2 bug còn mở đều nằm ở logic tính phí tái tục, mức "Medium". Họp kết thúc giai đoạn vào ngày mai. Anh/chị kết luận thế nào?**
Em không kết luận "đạt" chỉ dựa trên tỷ lệ. Trước họp em kiểm lại: 2 bug ảnh hưởng bao nhiêu hợp đồng, có làm sai số tiền không, đánh giá mức "Medium" có đúng không, có workaround không. Nếu sai số tiền thì theo em mức độ thực chất phải là cao, và nghiệp vụ tính phí là vùng không được để lỗi sang UAT. Trong họp em trình bày: chỉ số đạt, nhưng có 2 bug ở vùng trọng yếu, đề xuất **kết thúc có điều kiện**: sửa và retest trong 3 ngày trước ngày vào UAT, kèm rà soát và áp dụng cho logic tính phí khác. Quyết định cuối cùng do khách, có ghi biên bản.
> 📘 PMP: Control Quality: dữ liệu đo được phải kèm phán đoán theo mức độ ảnh hưởng tới giá trị nghiệp vụ, không chỉ theo tỷ lệ tổng.

**Q763. Hợp đồng theo công sức (T&M) với ngân hàng A, khách tự làm UAT. Đến cuối UAT, khách hỏi PM vendor "có thể kết thúc UAT chưa?". Vai trò của PM ở đây là gì?**
Với hợp đồng theo công sức (T&M), trách nhiệm phán đoán kết thúc UAT thuộc về khách; vai trò của em là **cung cấp dữ liệu để khách quyết**. Em tổng hợp: tỷ lệ case UAT đã chạy và đạt, bug còn mở theo mức độ và tình trạng sửa, đường cong hội tụ bug UAT, các rủi ro còn lại cho cutover. Em đối chiếu với tiêu chí ra UAT trong kế hoạch, nêu rõ mục nào đạt, mục nào chưa, và khuyến nghị của vendor kèm lý do. Em không nói thay khách "kết thúc được", nhưng cũng không im lặng nếu thấy rủi ro. Biên bản họp ghi rõ ai quyết định và dựa trên dữ liệu nào.
> 📘 PMP: Manage Stakeholder Engagement và Validate Scope: khách là người chấp nhận deliverable; PM cung cấp thông tin minh bạch và khuyến nghị.
> 💡 Nhật: Với hợp đồng theo công sức (T&M), vendor vẫn có nghĩa vụ cẩn trọng của người quản lý tốt; không cảnh báo rủi ro đã thấy vẫn có thể bị quy trách nhiệm.

## 7.2 Quy trình review (tự review, review chéo, review khách; phiếu ghi kết quả review; góp ý review được phân loại)

**Q764. Phỏng vấn tại công ty outsource cho khách Nhật: "Quy trình review tài liệu thiết kế 3 tầng ở dự án trước của anh/chị chạy thế nào?". Anh/chị trả lời ra sao?**
Em trình bày theo thứ tự: ① Tự review – người viết tự kiểm theo checklist, nộp checklist đã tick cùng tài liệu; ② Review chéo – đồng nghiệp hoặc leader kiểm nội dung, tính nhất quán với tài liệu định nghĩa yêu cầu và tài liệu liên quan; ③ Review khách – khách xác nhận nghiệp vụ và phê duyệt. Mỗi tầng có phiếu ghi kết quả review ghi góp ý review, người sửa, người xác nhận đóng. Tầng sau chỉ bắt đầu khi tầng trước đã đóng góp ý review mức cao. Bằng chứng: số góp ý review mỗi tầng giảm dần; nếu khách vẫn bắt nhiều lỗi cơ bản thì review nội bộ đang không hiệu quả.
> 📘 PMP: Manage Quality: quality assurance thông qua quy trình review nhiều lớp, dùng checklist và quality audit để bảo đảm quy trình được tuân thủ.
> 💡 Nhật: Khách Nhật rất khó chịu khi phải bắt lỗi chính tả, sai số trang; họ coi đó là dấu hiệu vendor không tự review.

**Q765. PMO yêu cầu chuẩn hóa phiếu ghi kết quả review cho toàn dự án migration của khách bảo hiểm B. Phiếu này cần những trường thông tin nào để dùng được cho phân tích chất lượng?**
Phần đầu phiếu ghi: tên và phiên bản tài liệu/source, quy mô (số trang hoặc KLOC), loại review, người review, ngày và **thời gian review thực tế** (giờ công). Phần chi tiết mỗi góp ý review ghi: vị trí, nội dung, phân loại (thiếu, sai, mơ hồ, trình bày, đề xuất), mức độ, giai đoạn gây ra lỗi, người sửa, nội dung sửa, người xác nhận và ngày đóng. Thiếu quy mô và thời gian review thì không tính được mật độ góp ý review và tỷ lệ effort review; thiếu phân loại thì không làm được Pareto. Bẫy là phiếu quá nhiều cột khiến team điền qua loa; em giữ trường bắt buộc tối thiểu và dùng danh sách chọn sẵn.
> 📘 PMP: Manage Quality và Control Quality: thiết kế data gathering (check sheet) ngay từ đầu để có dữ liệu phân tích nguyên nhân về sau.

**Q766. Tổng hợp góp ý review của Basic Design tại ngân hàng A cho thấy 60% thuộc loại "trình bày, chính tả", chỉ 8% thuộc "thiếu sót". Anh/chị đọc kết quả này thế nào?**
Em không coi đây là tín hiệu tốt ngay. Tỷ lệ trình bày cao thường có hai khả năng: tài liệu chưa qua tự review tử tế nên lỗi vặt nhiều, hoặc reviewer chỉ đọc bề mặt mà không kiểm nghiệp vụ. Em kiểm thêm: thời gian review trên mỗi trang, reviewer có kiến thức nghiệp vụ không, góp ý review loại bỏ sót ở các tài liệu khác của cùng người viết. Hành động: dùng công cụ/checklist để tự loại bỏ lỗi trình bày trước khi review, và yêu cầu review chéo tập trung vào đối chiếu với yêu cầu. Nếu sau đó bỏ sót tăng lên thì trước đây review đã bỏ sót, không phải tài liệu tốt.
> 📘 PMP: Control Quality: dùng Pareto và phân loại dữ liệu để thấy vấn đề thật, không chỉ nhìn tổng số.

**Q767. Dev junior trong team 25 người thường bỏ qua tự review, nộp thẳng cho leader. Leader mất 30% thời gian bắt lỗi cơ bản. Anh/chị xử lý thế nào?**
Em xác nhận bằng số trước: trong phiếu ghi kết quả review, tỷ lệ góp ý review loại lỗi cơ bản (đặt tên, định dạng, thiếu mục) của từng người là bao nhiêu. Sau đó em đặt **cổng tự động**: tài liệu/code chỉ được nộp review khi kèm checklist tự kiểm đã tick, code phải qua phân tích tĩnh không lỗi mức cao; leader được quyền trả lại ngay nếu thiếu, không review. Em nói chuyện riêng với các bạn junior, giải thích chi phí sửa lỗi muộn và hướng dẫn cách tự review. Sau 2 tuần em so lại tỷ lệ lỗi cơ bản để xem biện pháp có hiệu quả không.
> 📘 PMP: Manage Quality: áp dụng checklist và "quality built in" (nguyên tắc PMBOK 7 về chất lượng), phòng ngừa thay vì kiểm tra cuối.

**Q768. Tài liệu Detail Design được viết tiếng Việt rồi comtor dịch sang tiếng Nhật để giao khách bảo hiểm phi nhân thọ C. Quy trình review nên sắp xếp thế nào để không lọt lỗi dịch?**
Em tách hai lớp review: ① Review nội dung kỹ thuật trên bản tiếng Việt (review chéo trong team) và chỉ dịch khi nội dung đã đóng góp ý review; ② Review bản tiếng Nhật do BrSE đối chiếu song ngữ, tập trung vào thuật ngữ nghiệp vụ theo bảng thuật ngữ đã thống nhất với khách. Góp ý review lỗi dịch được phân loại riêng để đo chất lượng dịch, tránh lẫn với lỗi thiết kế. Em cũng quy định sửa nội dung thì sửa cả hai bản trong cùng lần. Bẫy là dịch song song khi bản gốc còn thay đổi, dẫn tới hai bản lệch nhau và khách review bản sai.
> 📘 PMP: Plan Quality Management và Manage Communications: xác định chuẩn ngôn ngữ, thuật ngữ và kiểm soát phiên bản tài liệu giao tiếp.
> 💡 Nhật: Một từ nghiệp vụ bảo hiểm dịch sai (vd nhầm "hủy hợp đồng" với "mất hiệu lực") có thể làm khách nghi ngờ toàn bộ tài liệu.

**Q769. Khách bảo hiểm nhân thọ B review tài liệu Basic Design và trả về 80 góp ý review trong 1 tuần. BrSE thấy khoảng 30 cái thực chất là yêu cầu mới. Anh/chị xử lý thế nào?**
Em cùng BrSE phân loại lại 80 góp ý review thành ba nhóm: lỗi thiết kế của vendor (sửa trong phạm vi), làm rõ yêu cầu (làm rõ spec, sửa và ghi bảng quản lý Q&A), và thay đổi yêu cầu. Với nhóm thay đổi, em không từ chối ngay mà phân tích ảnh hưởng: công sức, tiến độ, tài liệu liên quan, rồi đưa vào quy trình change request. Em gửi khách bảng phân loại kèm lý do từng mục, xin xác nhận trong họp định kỳ. Điểm mấu chốt là thái độ: không tranh cãi "đây không phải lỗi", mà trình bày dựa trên tài liệu định nghĩa yêu cầu đã duyệt.
> 📘 PMP: Perform Integrated Change Control: thay đổi phải qua phân tích ảnh hưởng và phê duyệt; tránh scope creep khi trộn thay đổi vào góp ý review.
> 💡 Nhật: Nhiều khách Nhật không phân biệt "góp ý review" và "mong muốn của khách"; việc phân loại phải làm khéo, có căn cứ tài liệu, tránh làm khách mất mặt.

**Q770. Buổi review Detail Design với 6 người kéo dài 4 tiếng nhưng chỉ đi được 20/60 trang, chủ yếu tranh luận cách sửa. Anh/chị cải tiến buổi review thế nào?**
Em đổi cách tổ chức: tài liệu gửi trước ít nhất 1 ngày, reviewer đọc trước và ghi góp ý review vào phiếu; buổi họp chỉ xác nhận góp ý review và làm rõ ý, **không thảo luận cách sửa** (để người viết tự xử lý sau). Mỗi buổi tối đa 1–2 tiếng (tham khảo), có moderator giữ thời gian và người ghi chép. Chỉ mời người cần thiết cho phần tài liệu đó. Vấn đề cần bàn sâu được chuyển thành item riêng có người phụ trách. Em đo hiệu quả bằng số trang review được mỗi giờ và số góp ý review phát hiện mỗi giờ trước và sau khi đổi.
> 📘 PMP: Manage Quality: inspection có cấu trúc (vai trò moderator, chuẩn bị trước) hiệu quả hơn họp tự do.
> 💡 Nhật: Khách Nhật quen với buổi review dài; đề xuất đổi cách họp nên trình bày như cải tiến chung kèm số đo, tránh để khách hiểu là vendor chê họp mất thời gian.

**Q771. Kiểm tra cuối Basic Design tại ngân hàng A thấy 45 góp ý review có trạng thái "đã sửa" nhưng không có ai xác nhận đóng. Leader nói "dev sửa rồi mà". Anh/chị xử lý thế nào?**
Em không cho kết thúc giai đoạn khi 45 góp ý review chưa được xác nhận. Quy tắc là: người sửa đổi trạng thái sang "đã sửa", **người đưa ra hoặc người được chỉ định mới xác nhận và đóng**. Em lấy mẫu 10 góp ý review để kiểm thử: nếu có cái sửa sai hoặc sửa thiếu thì phải xác nhận lại toàn bộ 45. Em sắp xếp reviewer xác nhận trong 1–2 ngày, cập nhật vào tiến độ. Phòng ngừa: tiêu chí ra giai đoạn ghi rõ "góp ý review chưa xác nhận đóng = 0", và báo cáo tuần có số góp ý review chờ xác nhận để không dồn cuối.
> 📘 PMP: Control Quality: verified deliverables chỉ có được sau khi kiểm tra xác nhận; tự khai "đã sửa" chưa phải là bằng chứng.

**Q772. Dự án ngân hàng A có 60 KLOC Java mới. Leader đề xuất bỏ code review thủ công, chỉ dùng công cụ phân tích tĩnh để tiết kiệm thời gian. Anh/chị phản hồi thế nào?**
Em đồng ý dùng công cụ cho phần máy làm tốt (vi phạm chuẩn coding, null, độ phức tạp), nhưng không bỏ hẳn review của người. Công cụ không phát hiện được logic nghiệp vụ sai như cách làm tròn tiền lãi, điều kiện ngày hiệu lực. Em đề xuất: chạy phân tích tĩnh bắt buộc trước khi review; review thủ công tập trung vào module rủi ro cao (tính toán tiền, xử lý giao dịch, phân quyền) và lấy mẫu với module đơn giản. Em đo bằng số: so sánh tỷ lệ bug IT xuất phát từ lỗi logic giữa module có review đầy đủ và module lấy mẫu để điều chỉnh tiếp.
> 📘 PMP: Tailoring (PMBOK 7): chọn mức độ kiểm tra theo rủi ro; Plan Quality Management cân bằng cost of quality.
> 💡 Nhật: Khách ngân hàng thường yêu cầu bằng chứng review cho source; bỏ review thủ công mà không thỏa thuận có thể vi phạm chuẩn của khách.

**Q773. Khách bảo hiểm phi nhân thọ C yêu cầu mọi góp ý review nội bộ, kể cả lỗi chính tả, đều phải ghi vào phiếu ghi kết quả review và gửi khách. Team 10 người than tốn thêm khoảng 15% công. Anh/chị làm gì?**
Em hỏi khách mục đích: họ cần bằng chứng review đã làm thật, hay cần dữ liệu để đánh giá chất lượng. Từ đó em đề xuất phương án vừa đủ: lỗi trình bày được ghi dạng tổng hợp (số lượng theo tài liệu) thay vì từng dòng; góp ý review nội dung vẫn ghi chi tiết. Em ước lượng công tiết kiệm được và trình khách để quyết. Nếu khách vẫn yêu cầu đủ chi tiết, em coi đây là yêu cầu hợp đồng, đưa vào ước lượng và nếu là phát sinh thì xử lý qua change request, không để team âm thầm gánh. Bằng chứng giao khách phải nhất quán với dữ liệu nội bộ.
> 📘 PMP: Tailoring và Plan Quality Management: điều chỉnh quy trình theo nhu cầu khách; chi phí thêm là một phần cost of quality cần được nhận diện.

**Q774. Ở dự án migration của khách bảo hiểm B, chỉ có 1 leader đủ kiến thức nghiệp vụ để review. Hiện 30 tài liệu đang chờ, thời gian chờ trung bình 6 ngày. Anh/chị tháo nút thắt thế nào?**
Em phân tầng review theo rủi ro: tài liệu rủi ro cao (tính phí, thanh toán, chuyển đổi dữ liệu) leader review; tài liệu rủi ro thấp giao cho thành viên khác review chéo với checklist chi tiết, leader chỉ duyệt lấy mẫu. Em xếp 30 tài liệu theo thứ tự đường găng để leader làm trước những cái chặn giai đoạn sau. Song song, em đào tạo 1–2 người làm reviewer phụ bằng cách cho họ review cùng leader. Em báo khách nếu tiến độ bị ảnh hưởng. Về lâu dài, phụ thuộc vào một người là rủi ro phải có trong risk register.
> 📘 PMP: Resource Management và Control Schedule: xử lý ràng buộc nguồn lực (resource leveling), ưu tiên việc trên critical path.

**Q775. Khách sản xuất D review Basic Design trong buổi họp, nói "về cơ bản là OK" (nói bằng tiếng Nhật) nhưng không ký, không email. Ba tháng sau ở IT, khách nói thiết kế sai và họ chưa từng duyệt. Lúc review lẽ ra anh/chị phải làm gì?**
"về cơ bản là OK" không phải phê duyệt. Sau buổi review, em phải gửi trong 24 giờ biên bản họp ghi rõ: tài liệu, phiên bản, góp ý review khách đưa ra, kết luận "chấp thuận với điều kiện sửa các góp ý review số…", và xin khách xác nhận bằng email hoặc dấu duyệt theo quy định của họ. Khi sửa xong góp ý review, gửi lại bản cuối và xin phê duyệt chính thức. Trong tiêu chí ra giai đoạn ghi rõ "có bằng chứng phê duyệt của khách". Hiện tại, em vẫn xử lý lỗi thiết kế theo hướng hợp tác, rồi thống nhất quy trình phê duyệt để không lặp lại.
> 📘 PMP: Validate Scope: chấp nhận chính thức phải được ghi nhận; Manage Communications bảo đảm thông tin quyết định được lưu.
> 💡 Nhật: Nhiều khách Nhật ngại ký sớm vì sợ mất quyền sửa; có thể đề xuất phê duyệt theo phiên bản ("v1.0 đã duyệt, thay đổi sau đi theo quản lý thay đổi") để khách yên tâm.

**Q776. Dự án ngân hàng A, review chéo code giữa hai sub-team VN. Sub-team X luôn có góp ý review rất ít, sub-team Y rất nhiều. Hai bên bắt đầu căng thẳng. Anh/chị xử lý thế nào?**
Em xác nhận dữ liệu: cùng quy mô code thì mật độ góp ý review hai bên khác nhau bao nhiêu, loại góp ý review là gì, thời gian review mỗi bên bỏ ra. Ít góp ý review có thể do code tốt hoặc do review lỏng; nhiều góp ý review có thể do code kém hoặc reviewer khắt khe về chuyện vặt. Em lấy mẫu 2 file mỗi bên, nhờ một reviewer trung lập review lại để so. Sau đó em thống nhất **checklist và tiêu chí mức độ chung** cho cả hai, tách lỗi phong cách khỏi lỗi logic. Em nói rõ với team: số góp ý review dùng để cải tiến sản phẩm, không dùng để đánh giá ai giỏi hơn.
> 📘 PMP: Manage Team và Manage Quality: giải quyết xung đột bằng dữ liệu khách quan và chuẩn chung (collaborate/problem solve).

## 7.3 Chỉ số review: mật độ góp ý review, tỷ lệ effort review, đọc bất thường

**Q777. Interviewer hỏi: "Mật độ góp ý review tính thế nào, đơn vị gì, ngưỡng lấy ở đâu?". Ví dụ tài liệu Basic Design 120 trang có 150 góp ý review. Anh/chị trả lời thế nào?**
Mật độ góp ý review = số góp ý review ÷ quy mô đối tượng review. Với tài liệu, đơn vị thường là góp ý review/trang; với code là góp ý review/KLOC. Ví dụ 150 ÷ 120 = 1,25 góp ý review/trang. Ngưỡng lấy từ **baseline của công ty** cho cùng loại tài liệu và cùng giai đoạn, hoặc chuẩn khách cung cấp; nếu chưa có thì đặt ngưỡng tạm và điều chỉnh sau vài tài liệu đầu. Ngưỡng luôn có **cận trên và cận dưới**: quá cao là tài liệu kém, quá thấp là review có thể hời hợt. Bẫy là quên chuẩn hóa định nghĩa "1 trang" (khổ giấy, mật độ chữ) và loại góp ý review được đếm.
> 📘 PMP: Plan Quality Management định nghĩa quality metrics (công thức, đơn vị, ngưỡng); Control Quality đo và so với ngưỡng.

**Q778. Team 8 người ở khách bảo hiểm phi nhân thọ C viết Detail Design hết 200 giờ công, review hết 12 giờ công. Anh/chị đánh giá thế nào?**
Tỷ lệ công review = 12 ÷ 200 × 100% = 6%. So với khoảng tham khảo thường gặp 10–20% (tham khảo, tùy chuẩn công ty), con số này thấp, gợi ý review chưa đủ sâu. Em không kết luận ngay mà kiểm: 12 giờ công đã ghi đủ chưa (có ai review mà không ghi công), mật độ góp ý review có thấp bất thường không, tài liệu có phải phần lặp lại mẫu nhiều không. Nếu cả tỷ lệ effort và mật độ góp ý review đều thấp, em yêu cầu review bổ sung cho phần rủi ro cao trước khi kết thúc giai đoạn. Bẫy là khi trễ tiến độ, review thường là việc bị cắt đầu tiên.
> 📘 PMP: Cost of quality: chi phí phòng ngừa và thẩm định (review) thấp thường dẫn tới chi phí lỗi (failure cost) cao ở các giai đoạn sau.
> 💡 Nhật: Khách Nhật hay hỏi tỷ lệ này trong báo cáo chất lượng; ghi công review thiếu là nguồn sai số phổ biến ở team offshore.

**Q779. Tài liệu Basic Design module thanh toán của ngân hàng A có mật độ góp ý review 0,2/trang trong khi ngưỡng là 0,8–1,5/trang. Người viết là senior giỏi. Anh/chị xử lý thế nào?**
Em không mặc định là "tài liệu tốt vì người viết giỏi". Bước 1: kiểm thời gian review và tốc độ đọc (trang/giờ); nếu review 80 trang trong 1 giờ thì gần như chắc chắn là đọc lướt. Bước 2: xem loại góp ý review đã có, reviewer là ai, có hiểu nghiệp vụ thanh toán không. Bước 3: cho một reviewer khác review lại một mẫu khoảng 10–20% số trang. Nếu mẫu này cho ra mật độ trong ngưỡng hoặc cao hơn, cần review lại toàn bộ; nếu mẫu vẫn thấp, ghi nhận "chất lượng tốt" kèm bằng chứng vào báo cáo. Kết luận nào cũng phải có lý do bằng dữ liệu.
> 📘 PMP: Control Quality: điểm nằm ngoài giới hạn (kể cả phía "tốt") đều cần phân tích nguyên nhân trước khi chấp nhận.
> 💡 Nhật: Khi trình kết quả review lại theo mẫu, ghi rõ tỷ lệ mẫu và cách chọn mẫu; khách Nhật đánh giá cao việc vendor tự kiểm khi chỉ số bất thường.

**Q780. Detail Design batch tính phí của khách bảo hiểm nhân thọ B có mật độ góp ý review 3,5/trang, gấp đôi cận trên. 40% góp ý review thuộc loại "spec không rõ". Anh/chị đọc và xử lý thế nào?**
Mật độ cao kèm nhiều góp ý "spec không rõ" cho thấy vấn đề có thể không nằm ở người viết Detail Design mà ở **đầu vào**: Basic Design hoặc định nghĩa yêu cầu chưa rõ. Em truy các góp ý này về mục tài liệu gốc, đếm bao nhiêu mục Basic Design liên quan. Hành động: các điểm chưa rõ đưa vào bảng quản lý Q&A hỏi khách, sửa Basic Design nếu là lỗi của vendor, sau đó mới sửa Detail Design và review lại. Em báo khách ảnh hưởng tiến độ nếu có. Phòng ngừa: kiểm tra rà soát các phần Basic Design khác do cùng người viết hoặc cùng nghiệp vụ.
> 📘 PMP: Root cause analysis: phân tích nguồn gốc lỗi theo giai đoạn gây ra; sửa tại nguồn thay vì chỉ sửa triệu chứng.

**Q781. PMO đề nghị PM đánh giá chất lượng review bằng cách kết hợp mật độ góp ý review và tỷ lệ effort review. Anh/chị diễn giải 4 trường hợp kết hợp thế nào?**
Em dùng ma trận 2 trục. ① Công review đủ, góp ý review trong ngưỡng: bình thường. ② Công review đủ, góp ý review cao: tài liệu chất lượng kém, cần xem nguyên nhân phía người viết hoặc đầu vào. ③ Công review thấp, góp ý review thấp: nguy hiểm nhất, có thể review hời hợt, cần review bổ sung. ④ Công review thấp mà góp ý review vẫn cao: tài liệu rất kém, có thể còn nhiều lỗi chưa phát hiện, cân nhắc trả lại người viết làm lại trước khi review tiếp. Em luôn kèm thêm loại góp ý review để tránh kết luận sai. Bẫy là chỉ nhìn một chỉ số rồi kết luận.
> 📘 PMP: Data analysis trong Control Quality: dùng nhiều chỉ số kết hợp (matrix diagram) để chẩn đoán thay vì đọc riêng lẻ.
> 💡 Nhật: Nhiều công ty Nhật có bảng "ma trận đánh giá chất lượng" với cách đọc tương tự; dùng đúng ngôn ngữ này khi báo cáo khách sẽ thuyết phục hơn.

**Q782. Đọc phiếu ghi kết quả review thấy một reviewer review 90 trang Detail Design trong 1,5 giờ và ghi 3 góp ý review. Anh/chị phản ứng thế nào?**
Tốc độ 60 trang/giờ là bất thường so với mức thường thấy cho tài liệu thiết kế (khoảng vài trang đến dưới 10 trang/giờ, tham khảo). Em nói chuyện riêng với reviewer để hiểu: có phải tài liệu chủ yếu là bảng định nghĩa lặp lại, hay reviewer quá tải nên đọc lướt, hay ghi thiếu công. Nếu là đọc lướt, em yêu cầu review lại phần nghiệp vụ trọng yếu và cân đối lại khối lượng review cho reviewer đó. Em thêm chỉ số "trang/giờ" vào kiểm tra tự động của phiếu ghi kết quả review để phát hiện sớm. Mục tiêu là cải thiện quy trình, không trách cá nhân.
> 📘 PMP: Control Quality: dùng dữ liệu đo (tốc độ review) như một control limit để phát hiện quy trình không ổn định.

**Q783. Dự án mới với ngân hàng A chưa có ngưỡng mật độ góp ý review cho từng loại tài liệu. Anh/chị thiết lập ngưỡng cho Basic Design, Detail Design và code như thế nào?**
Em làm 3 bước: ① Lấy baseline công ty từ các dự án tương tự (cùng loại hệ thống, cùng ngôn ngữ), mỗi loại đối tượng một ngưỡng riêng vì đơn vị khác nhau (góp ý review/trang cho tài liệu, góp ý review/KLOC cho code); ② Nếu không có dữ liệu, đặt ngưỡng tạm từ chuẩn công ty hoặc tài liệu tham khảo công khai, ghi rõ là "tạm"; ③ Sau khi review 3–5 tài liệu đầu, tính trung bình và độ lệch thực tế rồi điều chỉnh, có khách đồng ý. Mỗi lần đổi ngưỡng đều ghi lý do. Bẫy là dùng chung một ngưỡng cho mọi loại tài liệu.
> 📘 PMP: Plan Quality Management với benchmarking và progressive elaboration (rolling wave) cho tiêu chí chất lượng.

**Q784. Trong review Detail Design của khách bảo hiểm phi nhân thọ C, 35% góp ý review có giai đoạn sinh ra lỗi là Basic Design. Con số này nói lên điều gì và anh/chị làm gì?**
Giai đoạn gây ra lỗi là Basic Design nhưng phát hiện ở Detail Design nghĩa là **lỗi đã lọt qua review Basic Design**. 35% là tỷ lệ cao, cho thấy review Basic Design chưa hiệu quả. Em làm: ① Liệt kê các mục Basic Design bị ảnh hưởng, sửa và thông báo khách vì Basic Design đã được duyệt; ② Kiểm các chương Basic Design còn lại có cùng loại lỗi; ③ Phân tích vì sao review Basic Design bỏ sót: thiếu checklist, reviewer thiếu nghiệp vụ, thời gian review ít. Em ghi tỷ lệ lọt lỗi theo giai đoạn vào báo cáo chất lượng để theo dõi.
> 📘 PMP: Root cause analysis và cost of quality: lỗi càng phát hiện muộn càng tốn; đo nguồn gốc lỗi giúp cải tiến quy trình ở đúng giai đoạn.
> 💡 Nhật: Khách Nhật rất coi trọng phân tích "lỗi được sinh ra ở giai đoạn nào, được phát hiện ở giai đoạn nào"; thiếu phân tích này báo cáo chất lượng dễ bị trả lại.

**Q785. Sau khi PMO đặt chỉ tiêu mật độ góp ý review tối thiểu, team ở dự án migration của khách bảo hiểm B ghi rất nhiều góp ý review vặt như dấu chấm, cỡ chữ để đạt số. Anh/chị xử lý thế nào?**
Đây là hiện tượng "làm đẹp chỉ số" khi chỉ số biến thành mục tiêu. Em thay đổi cách đo: tách góp ý review theo mức độ và loại, chỉ đếm góp ý review nội dung (thiếu, sai, mơ hồ) vào mật độ góp ý review chính; lỗi trình bày thống kê riêng. Em giải thích lại cho team mục đích của ngưỡng là phát hiện bất thường, không phải chỉ tiêu phải đạt. Em kiểm thêm bằng chỉ số ở giai đoạn sau: nếu bug IT có nguồn gốc thiết kế vẫn cao, review chưa thật sự hiệu quả. Em báo PMO đề xuất bỏ chỉ tiêu tối thiểu cứng, thay bằng khoảng tham khảo kèm phân tích.
> 📘 PMP: Systems thinking (PMBOK 7): chỉ số tác động lên hành vi; Plan Quality Management cần thiết kế metric khó bị thao túng.

**Q786. Đợt sửa đổi Basic Design cho change request ở ngân hàng A chỉ đụng 12 trang trong tài liệu 250 trang, review ra 10 góp ý review. Báo cáo tính mật độ góp ý review = 10 ÷ 250 = 0,04. Cách tính này đúng không?**
Không đúng. Với tài liệu sửa đổi, quy mô phải tính theo **phần thay đổi**: 12 trang sửa, cộng phần đọc lại để kiểm ảnh hưởng nếu chuẩn công ty quy định. 10 ÷ 12 ≈ 0,83 góp ý review/trang, khác hoàn toàn với 0,04. Chia trên toàn bộ 250 trang làm chỉ số thấp giả tạo và che lấp vấn đề. Em sửa báo cáo, ghi rõ quy tắc đo quy mô cho tài liệu sửa đổi vào kế hoạch chất lượng, và kiểm lại các báo cáo trước đó xem có cùng lỗi không. Bẫy tương tự xảy ra với code sửa đổi: phải đo bằng số dòng thêm/sửa/xóa.
> 📘 PMP: Plan Quality Management: định nghĩa đo lường (operational definition) phải rõ ràng và nhất quán thì dữ liệu mới so sánh được.

**Q787. Dự án nhỏ cho khách sản xuất D, team 5 người, cả Basic Design chỉ 30 trang. PMO vẫn yêu cầu đánh giá mật độ góp ý review từng tài liệu so ngưỡng. Anh/chị xử lý thế nào?**
Với quy mô nhỏ, mỗi tài liệu chỉ vài trang nên vài góp ý review thêm hay bớt làm mật độ góp ý review dao động rất mạnh, so ngưỡng từng tài liệu không có ý nghĩa thống kê. Em đề xuất với PMO: tính mật độ góp ý review **gộp theo giai đoạn** thay vì từng tài liệu, và bổ sung đánh giá định tính (loại góp ý review, mức độ, có góp ý review nghiêm trọng không). Em vẫn ghi đầy đủ dữ liệu để tích lũy baseline cho công ty. Cách làm này được ghi vào kế hoạch chất lượng như một điều chỉnh có chủ đích, không phải bỏ quy trình.
> 📘 PMP: Tailoring (PMBOK 7): điều chỉnh mức độ và cách đo theo quy mô dự án, vẫn giữ mục tiêu của quy trình.
> 💡 Nhật: Khách Nhật chấp nhận tailoring khi PM giải thích được "vì sao" bằng logic thống kê; tự ý bỏ mà không giải thích thì bị coi là cẩu thả.

**Q788. Khách bảo hiểm nhân thọ B yêu cầu mỗi tài liệu giao nộp phải có mục "đánh giá kết quả review". Anh/chị viết mục này thế nào để thuyết phục?**
Em viết theo 3 phần: ① Số liệu: quy mô, công review, mật độ góp ý, tỷ lệ effort review so ngưỡng; ② Phân tích: phân loại góp ý (loại, mức độ, giai đoạn sinh ra lỗi), điểm ngoài ngưỡng và nguyên nhân; ③ Kết luận: chất lượng tài liệu đủ để chuyển giai đoạn sau hay chưa, kèm điều kiện nếu có. Ví dụ: "Mật độ góp ý 1,1/trang nằm trong ngưỡng; 70% là mơ hồ do yêu cầu mới làm rõ, đã sửa và xác nhận 100%; đánh giá: đạt". Bẫy là chỉ viết "không có vấn đề" (ghi chung chung) mà không có số và lý do.
> 📘 PMP: Control Quality cho ra quality control measurements; Manage Communications: báo cáo phải có dữ liệu và diễn giải.

## 7.4 Chỉ số test: mật độ test, ngưỡng trên/dưới, tỷ lệ đã chạy test/tỷ lệ pass

**Q789. Interviewer hỏi: "Mật độ test là gì? Ví dụ IT của module 25 KLOC có 1.000 case thì đánh giá thế nào?". Anh/chị trả lời ra sao?**
Mật độ test = số test case ÷ quy mô, thường là case/KLOC hoặc case/FP, tính riêng cho từng giai đoạn UT, IT, ST vì mỗi giai đoạn có cách viết case khác nhau. Ví dụ 1.000 ÷ 25 = 40 case/KLOC. Em so với ngưỡng IT của công ty hoặc của khách cho cùng loại hệ thống (tham khảo); thấp hơn cận dưới thì nghi thiếu case, cao hơn cận trên thì nghi case trùng lặp hoặc chia quá vụn. Sau đó em đối chiếu ma trận quan điểm test để xem độ phủ thật. Bẫy là chỉ nhìn số lượng case mà không xem case có kiểm đúng chỗ rủi ro không.
> 📘 PMP: Plan Quality Management: chọn metric phù hợp từng hoạt động; Control Quality so sánh với ngưỡng đã thống nhất.

**Q790. Khách bảo hiểm phi nhân thọ C hỏi: "Tại sao mật độ bug lại có cả cận dưới? Ít bug chẳng phải là tốt sao?". Anh/chị giải thích thế nào?**
Mật độ bug = số bug phát hiện ÷ quy mô. Ít bug có hai cách hiểu: sản phẩm tốt thật, hoặc **test chưa đủ mạnh để tìm ra bug**. Vì mọi phần mềm đều có lỗi tiềm ẩn ở một mức nào đó, mật độ thấp bất thường là tín hiệu cần kiểm tra: case có đủ quan điểm không, dữ liệu test có đa dạng không, người test có ghi đủ bug không. Ví dụ ngưỡng IT 3–6 bug/KLOC (tham khảo), dự án ra 0,8 thì em phải phân tích và bổ sung test trước khi kết luận chất lượng tốt. Em ghi rõ kết quả phân tích vào báo cáo chất lượng.
> 📘 PMP: Control Quality: giá trị ngoài giới hạn ở cả hai phía đều là tín hiệu quy trình bất thường, cần điều tra nguyên nhân.
> 💡 Nhật: Câu "ít bug có phải do test thiếu không?" là câu khách Nhật hỏi rất thường; PM nên chuẩn bị sẵn phân tích.

**Q791. Báo cáo IT tuần của ngân hàng A ghi tỷ lệ đã chạy test 100%. Khách hỏi "vậy IT xong chưa?" trong khi tỷ lệ pass chỉ 82%. Anh/chị trả lời thế nào?**
Chưa xong. Tỷ lệ đã chạy test 100% nghĩa là mọi case đã được chạy ít nhất 1 lần; tỷ lệ pass 82% nghĩa là 18% case đang NG do bug chưa sửa hoặc chưa retest. IT chỉ kết thúc khi case NG đã sửa, retest đạt và các tiêu chí khác (bug mức cao = 0, hội tụ bug) đều thỏa. Em báo khách: còn bao nhiêu case NG, do bao nhiêu bug, kế hoạch sửa và retest, ngày dự kiến kết thúc. Em cũng sửa mẫu báo cáo để luôn hiển thị hai chỉ số cạnh nhau, tránh hiểu nhầm.
> 📘 PMP: Manage Communications và Control Quality: báo cáo phải phân biệt rõ tiến độ thực hiện và kết quả chất lượng.

**Q792. Giữa IT tại khách bảo hiểm nhân thọ B, đường số case đã chạy thực tế chậm hơn kế hoạch 15 điểm %, còn 2 tuần. Anh/chị phân tích và xử lý thế nào?**
Em tìm nguyên nhân chậm trước: case bị chặn (blocked) do bug, môi trường không ổn định, dữ liệu test chưa có, hay năng suất người test thấp hơn ước lượng. Mỗi nguyên nhân có cách xử lý khác: ưu tiên sửa bug đang chặn nhiều case; ổn định môi trường; chuẩn bị dữ liệu song song; sắp lại thứ tự để chạy case không bị chặn. Nếu vẫn không kịp, em tính phương án tăng người test có kinh nghiệm hoặc lùi mốc, trình khách kèm ảnh hưởng. Em không giảm số case để "đạt" kế hoạch mà không có khách đồng ý.
> 📘 PMP: Control Schedule: dùng variance analysis để tìm nguyên nhân, sau đó crashing hoặc fast-tracking có kiểm soát; thay đổi phạm vi test phải qua change control.
> 💡 Nhật: Khi chậm số case đã chạy, khách Nhật muốn thấy biện pháp bắt kịp cụ thể theo ngày và số case, không phải câu "sẽ cố gắng".

**Q793. Báo cáo ST của khách bảo hiểm phi nhân thọ C có tỷ lệ pass 97%, nhưng anh/chị phát hiện 120 case "đang chờ" (blocked) bị loại khỏi mẫu số. Anh/chị làm gì?**
Em tính lại theo đúng định nghĩa và báo trung thực. Tỷ lệ pass = case đạt ÷ case đã chạy; nhưng case đang chờ phải được hiển thị riêng như một chỉ số, không được biến mất. Em báo cáo đủ ba con số: đã chạy, đạt, đang chờ kèm nguyên nhân chờ (bug chặn, chờ dữ liệu, chờ trả lời QA). Em hỏi người lập báo cáo vì sao loại bỏ, nếu là hiểu nhầm thì hướng dẫn lại; nếu cố ý làm đẹp số thì xử lý nghiêm. Em báo khách ngay rằng con số trước đây chưa phản ánh đầy đủ và gửi số đã điều chỉnh. Định nghĩa từng chỉ số được ghi rõ trong kế hoạch chất lượng.
> 📘 PMP: Code of ethics (honesty) và Manage Communications: báo cáo đầy đủ, không che giấu thông tin bất lợi.
> 💡 Nhật: Khách Nhật phát hiện số bị làm đẹp một lần sẽ yêu cầu kiểm tra lại mọi báo cáo; minh bạch sớm rẻ hơn rất nhiều.

**Q794. Mật độ test của UT ở ngân hàng A đạt 110 case/KLOC, cao hơn cận trên. Kiểm tra thấy nhiều case chỉ khác nhau giá trị đầu vào nhưng cùng một nhánh xử lý. Anh/chị xử lý thế nào?**
Mật độ cao do case trùng lặp không làm tăng chất lượng mà làm tăng công thực hiện và bảo trì. Em yêu cầu team rà lại theo kỹ thuật thiết kế test: phân vùng tương đương (mỗi vùng 1–2 case đại diện), giá trị biên, bảng quyết định, và đối chiếu với độ phủ nhánh C1. Case trùng thì gộp hoặc bỏ; nhánh chưa được phủ thì bổ sung. Em báo khách sau điều chỉnh mật độ thay đổi thế nào và vì sao, kèm ma trận phủ. Bài học: review test spec UT phải kiểm kỹ thuật thiết kế case, không chỉ đếm số lượng.
> 📘 PMP: Manage Quality: dùng design for X và các kỹ thuật thiết kế test để tối ưu cost of quality.

**Q795. Dự án migration COBOL sang Java của khách bảo hiểm nhân thọ B: 300 KLOC Java sinh ra từ công cụ chuyển đổi tự động, 40 KLOC viết tay. Anh/chị tính quy mô để làm mẫu số cho mật độ test và mật độ bug thế nào?**
Em tách hai loại code vì tính chất rủi ro khác nhau. Code viết tay tính bình thường. Code sinh tự động nếu đưa nguyên 300 KLOC vào mẫu số sẽ làm mật độ thấp giả tạo; em đề xuất hoặc dùng hệ số quy đổi (trọng số), hoặc đo theo đơn vị khác như số chương trình, số chức năng nghiệp vụ, số bảng dữ liệu. Ngưỡng cũng đặt riêng cho từng loại. Cách tính phải thống nhất với khách trước khi bắt đầu test và ghi vào kế hoạch chất lượng. Bẫy là đổi cách tính giữa chừng khi số xấu, làm khách mất niềm tin.
> 📘 PMP: Plan Quality Management: định nghĩa quy mô và metric phù hợp với đặc thù dự án (tailoring).
> 💡 Nhật: Dự án migration thường dùng chỉ số "đối chiếu cũ – mới" (so sánh kết quả cũ – mới) làm chính; mật độ bug truyền thống chỉ là phụ.

**Q796. Trong IT của ngân hàng A, module chuyển khoản có mật độ bug 12 bug/KLOC, gấp 3 lần trung bình các module khác. Anh/chị xử lý thế nào?**
Em xem chi tiết bug của module: loại lỗi, nguồn gốc (thiết kế hay code), có tập trung vào một người hoặc một chức năng con không. Nếu lỗi phân tán do thiết kế kém, em cho review lại Detail Design và code toàn module; nếu tập trung vào vài chức năng, em review sâu chỗ đó. Song song, em tăng test cho module này (thêm quan điểm, thêm dữ liệu) vì nơi nhiều bug thường còn nhiều bug ẩn. Em báo khách tình trạng và kế hoạch. Nếu sửa nhiều vòng vẫn không ổn, cân nhắc làm lại phần thiết kế, kèm phân tích chi phí.
> 📘 PMP: Pareto và root cause analysis trong Control Quality: tập trung nguồn lực vào phần sinh ra nhiều lỗi nhất.

**Q797. Dự án cải tạo hệ thống cho khách bảo hiểm phi nhân thọ C có 15 KLOC sửa đổi trong hệ thống 500 KLOC. PMO dùng chung ngưỡng mật độ bug của dự án phát triển mới. Anh/chị góp ý thế nào?**
Code sửa đổi có đặc điểm khác code mới: phần sửa nhỏ nhưng rủi ro ảnh hưởng (lỗi hồi quy (regression) – lỗi thoái lui) lên phần cũ lớn. Dùng ngưỡng của phát triển mới có thể không phản ánh đúng. Em đề xuất: đo mật độ trên phần thay đổi (thêm/sửa/xóa), đặt ngưỡng riêng cho dự án cải tạo từ dữ liệu các dự án cải tạo trước nếu có, và bổ sung chỉ số riêng cho regression như số case kiểm tra lỗi hồi quy và kết quả. Em ghi đề xuất và lý do vào kế hoạch chất lượng, xin PMO và khách đồng ý.
> 📘 PMP: Tailoring và benchmarking: so sánh với dự án tương tự về bản chất, không dùng chung một chuẩn cho mọi loại dự án.

**Q798. Tổng hợp bug IT của khách bảo hiểm nhân thọ B có 250 phiếu, trong đó 40 là "đúng spec" (không phải bug), 15 trùng nhau. Khi tính mật độ bug anh/chị đếm thế nào?**
Em chỉ đếm bug thật vào mật độ bug: 250 − 40 − 15 = 195. Phiếu đúng spec và phiếu trùng vẫn giữ trong hệ thống và thống kê riêng, vì chúng cũng mang thông tin: 40 phiếu đúng spec có thể cho thấy người test chưa hiểu spec, hoặc spec gây hiểu nhầm cần làm rõ. Phiếu trùng nhiều cho thấy quản lý bug chưa tốt. Quy tắc đếm phải ghi trong kế hoạch chất lượng trước khi test và áp dụng nhất quán. Bẫy là phân loại "đúng spec" quá dễ dãi để giảm số bug; em kiểm mẫu ngẫu nhiên để chắc phân loại đúng.
> 📘 PMP: Plan Quality Management: operational definition cho từng metric; Control Quality: dữ liệu phải sạch trước khi phân tích.
> 💡 Nhật: Nếu nhiều phiếu đúng spec, khách Nhật thường hỏi ngược "có phải spec khó hiểu không?"; nên chủ động phân tích trước.

**Q799. Khách ngân hàng A yêu cầu ghi nhận cả bug phát hiện trong UT. Dev trong team 30 người thường tự sửa ngay mà không ghi phiếu. Anh/chị xử lý thế nào?**
Không ghi bug UT thì không tính được mật độ bug UT, không phân tích được nguồn gốc lỗi, và khách sẽ thấy UT "không có bug" là bất thường. Em làm nhẹ quy trình để dev chịu ghi: bug UT ghi dạng đơn giản (module, loại lỗi, nguyên nhân, đã sửa), có thể ghi ngay trong test spec UT hoặc bảng tính chung, không cần phiếu đầy đủ như IT. Em giải thích mục đích cho team và kiểm tra hằng tuần số bug ghi nhận theo người. Nếu ai đó có quá ít bug so với quy mô code, em trao đổi riêng để hiểu, không phạt.
> 📘 PMP: Manage Quality: thu thập dữ liệu phải đơn giản để được tuân thủ; quy trình nặng nề sẽ dẫn đến dữ liệu thiếu.

**Q800. ST của khách bảo hiểm phi nhân thọ C chạy theo kịch bản nghiệp vụ end-to-end, mật độ test theo KLOC rất thấp. Khách hỏi ST có đủ không. Anh/chị chứng minh thế nào?**
Với ST, đo theo KLOC không phù hợp vì một kịch bản nghiệp vụ đi qua rất nhiều chương trình. Em chứng minh bằng **độ phủ nghiệp vụ**: ma trận các luồng nghiệp vụ chính (ký hợp đồng mới, sửa đổi, tái tục, bồi thường, hủy) × loại sản phẩm × kênh × trạng thái đặc biệt, cho thấy bao nhiêu ô đã có kịch bản. Thêm vào đó là độ phủ yêu cầu (bao nhiêu % yêu cầu được truy tới ít nhất 1 kịch bản) và yêu cầu phi chức năng đã test. Em trình bày cùng khách để họ chỉ ra kịch bản còn thiếu theo góc nhìn nghiệp vụ.
> 📘 PMP: Requirements traceability matrix: bảo đảm mọi yêu cầu được kiểm chứng; chọn metric phù hợp với mục tiêu của từng mức test.

**Q801. Sau khi sửa 60 bug IT ở dự án migration của khách bảo hiểm nhân thọ B, team chỉ retest đúng các case NG. Hai tuần sau ST phát hiện 8 bug lỗi hồi quy (regression). Lẽ ra quy trình phải thế nào?**
Sửa bug phải đi kèm hai việc: **retest** case NG để xác nhận đã sửa, và **kiểm tra hồi quy** các chức năng có thể bị ảnh hưởng. Phạm vi hồi quy xác định qua phân tích ảnh hưởng: sửa ở đâu, gọi tới đâu, dùng chung dữ liệu nào. Em lập quy tắc: mỗi phiếu bug phải ghi phạm vi ảnh hưởng và case hồi quy đã chạy; module dùng chung có bộ regression cố định, ưu tiên tự động hóa. Với 8 bug lỗi hồi quy (regression), em phân tích vì sao phân tích ảnh hưởng bỏ sót, rà soát và áp dụng sang chỗ tương tự kiểm các bản sửa khác cùng thời điểm, và báo khách kế hoạch.
> 📘 PMP: Control Quality: verify thay đổi đã được triển khai đúng và không gây tác động ngoài ý muốn; Perform Integrated Change Control có impact analysis.

## 7.5 Đường cong hội tụ bug, phân tích Pareto, phân loại nguyên nhân & giai đoạn gây lỗi

**Q802. Interviewer đưa 3 đồ thị bug tích lũy theo ngày của IT: (a) dốc rồi nằm ngang, (b) đi thẳng lên đều, (c) đang nằm ngang lại dốc lên. Anh/chị đọc từng đồ thị thế nào?**
Đây là đường cong tăng trưởng độ tin cậy. (a) Dạng chữ S nằm ngang ở cuối, trong khi test vẫn đang chạy: bug **đang hội tụ**, có thể xem xét kết thúc nếu các tiêu chí khác đạt. (b) Đi thẳng lên: mỗi ngày vẫn tìm ra số bug như nhau, chưa hội tụ, chất lượng chưa ổn định, không nên kết thúc. (c) Nằm ngang rồi dốc lên: có thể vừa có đợt sửa gây lỗi hồi quy (regression), vừa bắt đầu chạy phần case mới, hoặc vừa vào module chất lượng kém; cần điều tra ngay. Bẫy chung là chỉ nhìn hình dạng mà không đối chiếu với tiến độ chạy case.
> 📘 PMP: Control Quality: dùng run chart và trend analysis để đánh giá độ ổn định của quy trình theo thời gian.
> 💡 Nhật: Khách Nhật thường gọi là "đường cong hội tụ bug" và gần như luôn yêu cầu đồ thị này trong báo cáo chất lượng của IT và ST.

**Q803. Đường cong bug ST của ngân hàng A nằm ngang suốt 5 ngày cuối, leader đề xuất kết thúc ST. Kiểm tra thấy 5 ngày đó chỉ chạy được 3% case do môi trường lỗi. Anh/chị kết luận thế nào?**
Đường cong nằm ngang vì **không có test chạy**, không phải vì hết bug. Đây là bẫy kinh điển khi vẽ trục hoành theo ngày lịch. Em đề nghị vẽ lại với trục hoành là số case đã chạy (hoặc công test), khi đó 5 ngày này gần như là một điểm và đường cong chưa chứng minh được hội tụ. Em không kết thúc ST, mà xử lý môi trường, chạy tiếp phần case còn lại và theo dõi lại. Em báo khách tình trạng môi trường và ảnh hưởng tiến độ. Phòng ngừa: mẫu báo cáo bắt buộc hiển thị đường cong bug cùng với đường số case đã chạy.
> 📘 PMP: Control Quality: phân tích dữ liệu phải xét đúng biến số; kết luận từ dữ liệu thiếu ngữ cảnh dễ sai.

**Q804. ST của khách bảo hiểm nhân thọ B đã chạy 90% case nhưng đường cong bug vẫn dốc lên, mỗi ngày 8–10 bug mới. Còn 3 tuần nữa là UAT. Anh/chị làm gì?**
Em phân tích bug gần đây: tập trung ở module nào, loại gì, mức độ, nguồn gốc giai đoạn. Nếu tập trung vào vài module, em khoanh vùng và review lại thiết kế, code các module đó, thêm test sâu. Nếu phân tán, đây là dấu hiệu chất lượng tổng thể thấp, cần cân nhắc kéo dài ST. Em lập dự báo: với tốc độ hiện tại, khi nào đường cong có thể nằm ngang, và trình khách các phương án: giữ ngày UAT với phạm vi hẹp hơn, lùi UAT, hoặc tăng nguồn lực sửa bug. Em báo ngay, không chờ đến sát ngày UAT mới nói.
> 📘 PMP: Monitor Risks và trend analysis: dự báo dựa trên dữ liệu hiện tại; Perform Integrated Change Control khi phải điều chỉnh baseline.

**Q805. Phân tích 300 bug IT của khách bảo hiểm phi nhân thọ C theo nguyên nhân: 120 do hiểu sai spec, 70 do sót điều kiện biên, 50 do lỗi dữ liệu test, còn lại rải rác 6 nguyên nhân khác. Anh/chị dùng kết quả này thế nào?**
Em vẽ biểu đồ Pareto: 3 nguyên nhân đầu chiếm 240/300 = 80%, nên tập trung xử lý 3 nhóm này trước. Hiểu sai spec: kiểm tra chất lượng tài liệu thiết kế, buổi giải thích spec cho dev, bảng quản lý Q&A có được truyền đạt không. Sót điều kiện biên: bổ sung checklist biên vào review code và thiết kế case UT. Lỗi dữ liệu test: chuẩn hóa quy trình chuẩn bị dữ liệu, có người review dữ liệu. Mỗi biện pháp có người phụ trách và chỉ số kiểm tra hiệu quả ở giai đoạn sau. Em báo khách kết quả phân tích và kế hoạch trong báo cáo chất lượng IT.
> 📘 PMP: Pareto diagram trong Control Quality: nguyên tắc 80/20 để ưu tiên hành động cải tiến.

**Q806. Dự án ngân hàng A bắt đầu IT nhưng phiếu bug chỉ có trường mô tả tự do, không có phân loại nguyên nhân. Anh/chị thiết kế phân loại thế nào để phân tích được về sau?**
Em định nghĩa phân loại ngay trước khi test bắt đầu, dùng danh sách chọn sẵn, mỗi phiếu chọn một giá trị chính. Thường có các trục: ① Nguyên nhân: thiếu sót thiết kế, sai thiết kế, hiểu sai spec, lỗi code logic, lỗi điều kiện biên, lỗi interface, lỗi môi trường, lỗi dữ liệu test; ② Giai đoạn sinh ra lỗi: định nghĩa yêu cầu, Basic Design, Detail Design, lập trình; ③ Mức độ; ④ Module. Định nghĩa mỗi giá trị kèm ví dụ để người phân loại không hiểu khác nhau. Leader duyệt phân loại khi đóng phiếu. Bẫy là quá nhiều giá trị, mọi người chọn "khác".
> 📘 PMP: Plan Quality Management: chuẩn bị check sheet và cách thu thập dữ liệu; dữ liệu chuẩn hóa là nền cho root cause analysis.
> 💡 Nhật: Nhiều khách Nhật có sẵn bảng phân loại nguyên nhân bug (phân loại nguyên nhân bug) theo chuẩn của họ; nên xin và dùng luôn để báo cáo khớp với cách khách phân tích.

**Q807. Phân tích bug IT ở khách bảo hiểm nhân thọ B thấy 40% bug có giai đoạn sinh ra lỗi là Basic Design. Anh/chị diễn giải và hành động thế nào?**
40% bug sinh ra từ Basic Design nhưng đến IT mới phát hiện nghĩa là review Basic Design và Detail Design đều không bắt được, và chi phí sửa lúc này rất cao vì phải sửa tài liệu, code, case test. Em làm: ① Liệt kê các mục Basic Design liên quan, kiểm tra các mục tương tự chưa phát sinh bug; ② Sửa tài liệu và báo khách vì Basic Design đã được duyệt; ③ Phân tích nguyên nhân lọt: review Basic Design thiếu chuyên gia nghiệp vụ, thiếu đối chiếu yêu cầu. Em tính lại tỷ lệ lọt theo giai đoạn để đưa vào báo cáo và đề xuất cải tiến cho giai đoạn sau.
> 📘 PMP: Cost of quality và root cause analysis: lỗi lọt qua nhiều giai đoạn có chi phí sửa tăng mạnh, cần cải tiến ở giai đoạn gây ra.
> 💡 Nhật: Khách Nhật hay yêu cầu bảng "ma trận bug theo giai đoạn sinh ra – giai đoạn phát hiện"; nếu ô Basic Design × IT lớn, họ sẽ yêu cầu review lại Basic Design các phần còn lại.

**Q808. Dự án ngân hàng A có 50 KLOC, ngưỡng mật độ bug tổng IT + ST là 5–8 bug/KLOC (tham khảo). Hiện IT + ST đã tìm được 180 bug và đường cong đang chậm lại. Anh/chị ước lượng số bug còn ẩn thế nào?**
Theo ngưỡng, tổng bug kỳ vọng khoảng 50 × 5 = 250 đến 50 × 8 = 400. Đã tìm 180, còn khoảng 70–220 bug có thể ẩn nếu chất lượng ở mức trung bình. Em kết hợp thêm đường cong hội tụ: nếu fit theo đường Gompertz hoặc logistic cho thấy mức bão hòa khoảng 200, thì khoảng cách với ngưỡng gợi ý hoặc chất lượng tốt, hoặc test chưa đủ phủ. Em không công bố một con số chắc chắn mà trình bày dạng khoảng, kèm hành động: bổ sung test ở module ít bug bất thường. Bẫy là dùng ước lượng như cam kết chất lượng.
> 📘 PMP: Estimate và forecasting dựa trên dữ liệu lịch sử (analogous/parametric); Control Quality dùng dữ liệu để quyết định có test thêm hay không.

**Q809. IT của khách bảo hiểm phi nhân thọ C có 200 bug, 85% mức "Low", chỉ 3 bug "Critical" nhưng cả 3 đều ở logic tính bồi thường. Khách hỏi chất lượng tổng thể có ổn không. Anh/chị trả lời thế nào?**
Em không trả lời dựa vào tỷ lệ mức độ. Phân bố mức độ cho thấy phần lớn lỗi nhẹ, nhưng 3 bug Critical cùng tập trung ở logic bồi thường, là nghiệp vụ trọng yếu, là tín hiệu module này có vấn đề hệ thống. Em trình bày cho khách: tổng quan theo mức độ, sau đó phân tích riêng module bồi thường: nguyên nhân 3 bug, có chung nguồn gốc không, đã rà soát các công thức tương tự chưa, test bổ sung bao nhiêu case. Kết luận: chất lượng chung đạt, riêng module bồi thường cần kiểm tra thêm trước khi kết thúc IT.
> 📘 PMP: Control Quality: phân tích theo nhiều chiều (stratification) để không bị che khuất bởi số tổng.

**Q810. Trong ST tại ngân hàng A, đồ thị "phát sinh – giải quyết" cho thấy số bug mở tăng từ 20 lên 75 trong 2 tuần, khoảng cách giữa hai đường ngày càng rộng. Anh/chị xử lý thế nào?**
Khoảng cách rộng dần nghĩa là tốc độ sửa không theo kịp tốc độ phát hiện; nếu tiếp tục, bug tồn đọng sẽ chặn case và làm trễ ST. Em phân tích: bug mở nằm ở đâu, tuổi bug bao nhiêu ngày, kẹt ở bước nào (chờ phân tích, chờ sửa, chờ retest, chờ khách trả lời spec). Hành động theo điểm nghẽn: bố trí thêm dev sửa bug cho module nhiều bug, ưu tiên bug chặn nhiều case, đẩy nhanh QA với khách, tăng người retest. Em đặt mục tiêu bug mở giảm về dưới một ngưỡng trong 1 tuần và báo khách hằng ngày cho đến khi ổn.
> 📘 PMP: Control Quality kết hợp Control Schedule: dùng trend analysis để phát hiện backlog tăng và xử lý ràng buộc nguồn lực.
> 💡 Nhật: Khách Nhật thường yêu cầu "diễn biến bug chưa giải quyết" trong họp định kỳ hằng tuần, kèm tuổi bug; chuẩn bị sẵn để không bị bất ngờ.

**Q811. Trong UAT của khách bảo hiểm nhân thọ B, khách phát hiện 12 bug. Khách yêu cầu vendor phân tích "lẽ ra phải phát hiện ở giai đoạn nào". Anh/chị làm thế nào?**
Với mỗi bug, em xác định hai thông tin: nơi lỗi sinh ra và giai đoạn lẽ ra phải phát hiện (giai đoạn lẽ ra phải phát hiện, dựa vào phạm vi test đã định của từng giai đoạn). Ví dụ lỗi tính toán trong một hàm thì lẽ ra UT phải bắt; lỗi giao tiếp hai hệ thống thì IT; lỗi luồng nghiệp vụ thì ST. Sau đó em phân tích vì sao giai đoạn đó không bắt được: thiếu case, case có nhưng kỳ vọng sai, dữ liệu test không đủ. Em đưa kết quả vào báo cáo sự cố và đề xuất biện pháp cho từng giai đoạn, kèm rà soát và áp dụng sang chỗ tương tự.
> 📘 PMP: Root cause analysis: phân biệt nguyên nhân phát sinh và nguyên nhân lọt; cải tiến quy trình theo đúng điểm lọt.

**Q812. Dự án migration của khách bảo hiểm phi nhân thọ C, bug ở giai đoạn kiểm chứng dữ liệu tập trung vào 3 loại: sai mapping mã, lỗi mã hóa ký tự, và làm tròn số tiền. Anh/chị phân loại và xử lý thế nào?**
Với dự án migration, em bổ sung phân loại nguyên nhân riêng: định nghĩa mapping, logic chuyển đổi, mã ký tự, làm tròn/định dạng số, dữ liệu nguồn bẩn. Em vẽ Pareto theo các loại này và theo bảng dữ liệu. Sai mapping mã: rà lại toàn bộ bảng mapping với khách, xác nhận bằng văn bản. Ký tự ngoài bảng mã chuẩn: lập danh sách ký tự đặc biệt có trong dữ liệu thật, thống nhất quy tắc chuyển đổi. Làm tròn: thống nhất quy tắc với hệ thống cũ và kiểm bằng sum check. Mỗi loại rà soát và áp dụng sang tất cả bảng có cùng đặc điểm, không chỉ bảng đã phát hiện lỗi.
> 📘 PMP: Pareto và stratification trong Control Quality; tailoring phân loại nguyên nhân theo đặc thù dự án.

**Q813. Đường cong bug IT tổng của ngân hàng A đã hội tụ đẹp, nhưng khi tách theo module, module liên kết hệ thống bên ngoài vẫn dốc lên. Leader đề xuất kết thúc IT vì đồ thị tổng đẹp. Anh/chị quyết định thế nào?**
Em không kết thúc toàn bộ IT dựa trên đồ thị tổng, vì module lớn hội tụ có thể che đi module nhỏ chưa ổn. Em đề xuất kết thúc IT theo phạm vi: các module đã hội tụ và đạt tiêu chí thì đóng, chuyển ST; module liên kết bên ngoài tiếp tục IT với kế hoạch riêng, phân tích nguyên nhân (đặc tả interface chưa rõ, môi trường giả lập không giống thật, bên ngoài thay đổi). Em báo khách tình trạng, kế hoạch và ảnh hưởng tới ST các kịch bản liên quan. Từ giờ báo cáo bắt buộc có đường cong theo module quan trọng.
> 📘 PMP: Systems thinking và Control Quality: phân tích theo từng thành phần để tránh kết luận sai từ dữ liệu tổng hợp.
> 💡 Nhật: Interface với hệ thống bên ngoài (đối tác, hệ thống khác của khách) thường cần khách điều phối; cần đưa vào bảng quản lý vấn đề để khách chịu trách nhiệm phần của họ.

## 7.6 Quản lý Q&A: đặt câu hỏi kèm phương án, hạn trả lời, theo dõi, ảnh hưởng tài liệu

**Q814. Dev hỏi BrSE: "Khi hợp đồng bị hủy giữa kỳ thì hoàn phí thế nào?" và BrSE chuyển nguyên câu này cho khách bảo hiểm nhân thọ B. Anh/chị sẽ viết lại câu hỏi thế nào cho đúng chuẩn?**
Một câu hỏi tốt gồm: ① Bối cảnh và vị trí tài liệu liên quan (tài liệu Basic Design mục nào, màn hình/batch nào); ② Điểm chưa rõ cụ thể; ③ **Phương án đề xuất** (phương án A, phương án B) kèm ảnh hưởng từng phương án; ④ Phương án vendor khuyến nghị và lý do; ⑤ hạn trả lời và ảnh hưởng nếu trễ. Ví dụ: "Hủy giữa kỳ với hợp đồng đóng phí năm: phương án A hoàn phí theo ngày, phương án B hoàn theo tháng làm tròn xuống như hệ thống hiện hành. Khuyến nghị phương án B để giữ nguyên nghiệp vụ. Xin trả lời trước 20/7, trễ sẽ ảnh hưởng 3 batch." Câu hỏi mở bắt khách phải tự nghĩ từ đầu sẽ chậm và dễ hiểu sai.
> 📘 PMP: Manage Communications: thông tin cần rõ ràng, súc tích, có ngữ cảnh (5C của giao tiếp viết) để người nhận ra quyết định được.
> 💡 Nhật: Khách Nhật trả lời nhanh hơn nhiều khi chỉ cần chọn "phương án A" hoặc "phương án B" (nói bằng tiếng Nhật); câu hỏi mở thường bị để lâu vì phải họp nội bộ.

**Q815. Dự án mới với ngân hàng A cần lập bảng quản lý Q&A. Bảng này nên có những cột nào?**
Các cột cơ bản: số QA, ngày hỏi, người hỏi, phân loại (spec, môi trường, dữ liệu, quy trình), tài liệu/mục liên quan, nội dung câu hỏi, phương án đề xuất, mức ưu tiên, hạn trả lời, người trả lời phía khách, ngày trả lời, nội dung trả lời, trạng thái (chưa trả lời, đã trả lời, đã xác nhận, đóng), **tài liệu cần cập nhật và trạng thái cập nhật**, có phải thay đổi spec hay không. Cột "phản ánh vào tài liệu" hay bị bỏ quên nhưng rất quan trọng: QA đã trả lời mà tài liệu không sửa thì về sau không ai biết. Em giữ bảng song ngữ, bản gốc tiếng Nhật là chuẩn.
> 📘 PMP: Manage Communications và Manage Project Knowledge: bảng quản lý Q&A là một phần của issue log và lessons learned, lưu quyết định có thể truy vết.
> 💡 Nhật: Nếu khách có mẫu bảng quản lý Q&A riêng thì dùng mẫu của khách cho bản giao khách; cột phục vụ quản lý nội bộ để ở bản riêng.

**Q816. Ở khách bảo hiểm phi nhân thọ C, bảng quản lý Q&A có 25 câu chưa trả lời, 10 câu đã quá hạn, trong đó 4 câu chặn Detail Design của 2 module trên đường găng. Anh/chị xử lý thế nào?**
Em xác định ảnh hưởng cụ thể của 10 câu quá hạn: 4 câu chặn đường găng thì mỗi ngày trễ làm trễ mốc bao nhiêu. Em sắp lại công việc để team làm phần không bị chặn. Sau đó em báo khách theo cấp: gửi danh sách ưu tiên cho người phụ trách kèm ảnh hưởng tiến độ bằng số; nếu vẫn chậm thì đưa vào họp định kỳ với cấp quản lý của khách; đề xuất họp ngắn 30 phút để trả lời trực tiếp 4 câu quan trọng. Nếu trễ vẫn tiếp diễn, em ghi rủi ro và đề nghị điều chỉnh lịch theo quy trình thay đổi, có biên bản.
> 📘 PMP: Monitor Communications và Manage Stakeholder Engagement: escalate có căn cứ, giải quyết ở cấp thấp nhất trước.
> 💡 Nhật: Ghi "hạn trả lời" và "ảnh hưởng khi quá hạn" ngay trên câu hỏi giúp khách có lý do ưu tiên trong nội bộ của họ.

**Q817. Ở ngân hàng A, khách trả lời QA-085 khác với câu trả lời QA-032 trước đó về cùng một quy tắc tính lãi. Detail Design đã làm theo QA-032. Anh/chị xử lý thế nào?**
Em không tự chọn câu trả lời nào đúng. Em gửi lại khách một câu hỏi xác nhận: nêu rõ QA-032 và QA-085 mâu thuẫn ở điểm nào, phần thiết kế đã làm theo QA-032, ảnh hưởng nếu áp dụng QA-085 (bao nhiêu tài liệu, chương trình, công sức). Khi khách xác nhận, nếu theo QA-085 thì xử lý như một thay đổi: phân tích ảnh hưởng, cập nhật tài liệu, xin chấp thuận về chi phí/tiến độ nếu có. Em đánh dấu QA-032 là "bị thay thế bởi QA-085" để truy vết. Phòng ngừa: khi nhận câu trả lời mới, BrSE kiểm các QA liên quan trước đó.
> 📘 PMP: Perform Integrated Change Control: thay đổi yêu cầu phải phân tích ảnh hưởng và được phê duyệt; quản lý cấu hình đảm bảo truy vết.

**Q818. Khách bảo hiểm nhân thọ B trả lời một QA bằng cách thêm điều kiện mới vào logic tính phí, nhưng gọi đó là "làm rõ spec". Ảnh hưởng ước khoảng 15 MD. Anh/chị xử lý thế nào?**
Em phân biệt làm rõ spec: nội dung đã có trong yêu cầu, chỉ cần nói rõ hơn và thay đổi spec: thêm hoặc đổi nội dung so với baseline. Em đối chiếu với tài liệu định nghĩa yêu cầu đã duyệt: nếu điều kiện mới không có căn cứ trong đó, đây là thay đổi. Em trình bày với khách một cách mềm mỏng: chỉ ra mục tài liệu gốc, ảnh hưởng 15 MD và tới lịch, đề xuất xử lý qua change request. Có thể đề xuất đưa vào phase sau nếu không cấp thiết. Em ghi trong bảng quản lý Q&A rằng QA này dẫn tới CR số mấy.
> 📘 PMP: Control Scope và Perform Integrated Change Control: bảo vệ scope baseline, tránh scope creep qua kênh hỏi đáp.
> 💡 Nhật: Với hợp đồng trọn gói, nếu không làm rõ ngay thì khi nghiệm thu khách sẽ coi là trong phạm vi; nên ghi "vấn đề này được xử lý như thay đổi spec" trong biên bản họp.

**Q819. Thống kê QA tại khách bảo hiểm phi nhân thọ C cho thấy trung bình mỗi câu hỏi mất 2,5 vòng hỏi lại mới chốt được. Anh/chị cải tiến thế nào?**
Em lấy mẫu 10 QA nhiều vòng nhất để xem lý do: câu hỏi mơ hồ, thiếu ngữ cảnh, dịch không chuẩn, hay khách trả lời không đủ. Thường gặp nhất là câu hỏi mở. Em đặt chuẩn: mọi QA phải có ngữ cảnh, câu hỏi đóng hoặc phương án lựa chọn, ví dụ dữ liệu cụ thể; BrSE review câu hỏi trước khi gửi, câu không đạt thì trả lại người hỏi. Với vấn đề phức tạp, chuyển sang họp ngắn có màn hình chia sẻ, sau đó ghi kết quả vào bảng quản lý Q&A. Em đo lại số vòng trung bình sau 1 tháng để xác nhận hiệu quả.
> 📘 PMP: Monitor Communications: đo hiệu quả giao tiếp và điều chỉnh phương pháp; Manage Quality áp dụng cho cả quy trình giao tiếp.

**Q820. Ở dự án ngân hàng A, dev hỏi BrSE qua chat, BrSE hỏi khách qua chat, kết quả chỉ nằm trong tin nhắn. Khi dev nghỉ việc, không ai biết vì sao thiết kế như vậy. Anh/chị chấn chỉnh thế nào?**
Em đặt quy tắc: chat chỉ dùng để trao đổi nhanh, **mọi câu hỏi và trả lời có ảnh hưởng đến spec, thiết kế, dữ liệu, tiến độ đều phải ghi vào bảng quản lý Q&A**, chậm nhất trong ngày. BrSE chịu trách nhiệm ghi nhận khi nhận được trả lời. Leader kiểm khi review tài liệu: chỗ thiết kế khác yêu cầu phải dẫn số QA. Với các trao đổi cũ, em yêu cầu rà lại tin nhắn 1–2 tháng gần nhất, ghi bổ sung các điểm quan trọng và xin khách xác nhận lại nếu cần. Bằng chứng truy vết là thứ bảo vệ vendor khi có tranh chấp.
> 📘 PMP: Manage Project Knowledge: chuyển tri thức ngầm thành tri thức rõ ràng; Manage Communications đảm bảo thông tin được lưu trữ chính thức.

**Q821. Dự án migration của khách bảo hiểm nhân thọ B: rất nhiều QA được khách trả lời là "giữ nguyên như hệ thống cũ" (nói bằng tiếng Nhật), nhưng không có tài liệu hệ thống cũ. Anh/chị xử lý thế nào?**
"giữ nguyên như hệ thống cũ" chỉ là câu trả lời hợp lệ khi hai bên **cùng biết hiện hành là gì**. Em đề nghị khách cung cấp bằng chứng: kết quả màn hình, báo cáo, dữ liệu đầu ra của hệ thống cũ, hoặc source cũ nếu có. Team phân tích hành vi hiện hành, viết lại thành mô tả cụ thể kèm ví dụ dữ liệu, rồi gửi khách xác nhận "hiện hành đúng như thế này". Với phần không xác định được, em ghi rủi ro và đề xuất kiểm chứng bằng so sánh kết quả cũ – mới trong test. Em báo khách công sức phân tích này nếu nằm ngoài ước lượng ban đầu.
> 📘 PMP: Identify Risks và Collect Requirements: giả định ẩn trong "giữ như cũ" phải được làm rõ và ghi nhận trong assumption log.
> 💡 Nhật: "giữ nguyên như hệ thống cũ" là một trong những nguồn rủi ro lớn nhất của dự án migration Nhật; người viết yêu cầu cũ thường đã nghỉ hưu hoặc chuyển bộ phận.

**Q822. Comtor dịch câu trả lời QA của ngân hàng A sang tiếng Việt, nhầm "từ … trở lên" thành "lớn hơn". Team làm sai điều kiện biên ở 5 chương trình. Anh/chị xử lý và phòng ngừa thế nào?**
Em sửa ngay 5 chương trình và test lại giá trị biên, rồi tìm toàn bộ QA và tài liệu khác có các biểu hiện so sánh như "từ … trở lên", "từ … trở xuống", "dưới …", "vượt quá …" để kiểm tra dịch lại. Phòng ngừa: bảng quản lý Q&A luôn giữ nguyên văn tiếng Nhật bên cạnh bản dịch; câu trả lời liên quan đến điều kiện, số liệu, quy tắc tính toán phải được BrSE kiểm lại bản dịch; lập bảng thuật ngữ cho các biểu hiện dễ nhầm. Em ghi lỗi này vào phân tích nguyên nhân để đo chất lượng dịch. Nếu ảnh hưởng đến tiến độ, báo khách theo báo cáo – liên lạc – trao đổi.
> 📘 PMP: Manage Communications: rào cản ngôn ngữ là yếu tố giao tiếp cần quản lý; Manage Quality với checklist cho các điểm dễ sai.

**Q823. Sắp kết thúc Basic Design ở khách bảo hiểm phi nhân thọ C, bảng quản lý Q&A còn 18 câu chưa trả lời. Khách muốn kết thúc giai đoạn đúng hạn. Anh/chị đề xuất thế nào?**
Em phân loại 18 câu: câu nào ảnh hưởng đến cấu trúc thiết kế (màn hình, bảng dữ liệu, interface), câu nào chỉ là chi tiết có thể chốt ở Detail Design. Đề xuất tiêu chí: QA ảnh hưởng cấu trúc phải trả lời xong trước khi kết thúc; QA chi tiết có thể chuyển sang giai đoạn sau nếu có hướng xử lý tạm, hạn trả lời mới và người phụ trách. Em ghi danh sách chuyển tiếp vào báo cáo kết thúc giai đoạn và biên bản, nêu rủi ro làm lại nếu câu trả lời khác giả định. Như vậy khách vẫn giữ được mốc mà rủi ro được nhìn thấy.
> 📘 PMP: Phase gate với tiêu chí rõ ràng; Manage Risks: mục chưa đóng được chuyển tiếp có ghi nhận, không bị lãng quên.

**Q824. Trong 2 tháng Basic Design, team 30 người gửi 220 QA cho khách bảo hiểm nhân thọ B. Phía khách phàn nàn bị "tấn công bằng câu hỏi". Anh/chị xử lý thế nào?**
Em phân tích 220 QA: bao nhiêu câu trùng ý, bao nhiêu câu team có thể tự tìm trong tài liệu, bao nhiêu câu thật sự cần khách quyết. Em đặt quy trình lọc: dev hỏi trong team trước, BrSE gộp câu trùng, chỉ gửi câu cần quyết định của khách; gửi theo đợt cố định (vd 2 lần/tuần) thay vì rải rác; xếp theo ưu tiên. Với chủ đề nhiều câu hỏi, đề xuất buổi giải thích nghiệp vụ hoặc buổi QA trực tiếp. Em cảm ơn khách đã hỗ trợ và báo kế hoạch cải tiến. Đo lại số câu mỗi tuần và thời gian trả lời sau khi áp dụng.
> 📘 PMP: Manage Stakeholder Engagement: điều chỉnh phương pháp giao tiếp theo mức độ chịu tải và mong đợi của stakeholder.

**Q825. Trong họp định kỳ với ngân hàng A, khách trả lời miệng 5 QA quan trọng. Một tháng sau người phụ trách phía khách đổi, người mới nói không biết các trả lời đó. Lẽ ra phải làm gì?**
Trả lời miệng phải được ghi nhận chính thức ngay: cập nhật QAnội dung, người trả lời, ngày, "trả lời tại họp định kỳ ngày …", ghi vào biên bản họp phần quyết định, gửi khách trong 24 giờ và xin xác nhận. Nếu khách không phản hồi trong thời hạn thỏa thuận (vd 3 ngày làm việc), coi như đồng ý theo quy tắc đã ghi trong kế hoạch giao tiếp. Hiện tại, em gửi người mới bản biên bản họp và bảng quản lý Q&A có ghi nhận, giải thích ngữ cảnh và xin họ xác nhận tiếp. Khi khách đổi người, em chủ động tổ chức buổi bàn giao các quyết định quan trọng.
> 📘 PMP: Manage Communications và Manage Stakeholder Engagement: lưu trữ quyết định chính thức; chủ động khi có thay đổi stakeholder.
> 💡 Nhật: Khách Nhật thường luân chuyển nhân sự vào tháng 4; nên lên kế hoạch tổng hợp QA và quyết định trước thời điểm này.

**Q826. Khách sản xuất D trả lời một QA quan trọng về quy tắc tồn kho là "xin giao cho bên anh/chị" (nói bằng tiếng Nhật, nghĩa là giao vendor quyết). Hợp đồng là hợp đồng trọn gói. Anh/chị xử lý thế nào?**
"xin giao cho bên anh/chị" không có nghĩa là vendor chịu toàn bộ trách nhiệm về sau. Em đưa ra phương án cụ thể vendor đề xuất (kèm lý do và ví dụ dữ liệu), ghi vào bảng quản lý Q&A và tài liệu thiết kế dưới dạng "vendor đề xuất, khách xác nhận", sau đó gửi khách xác nhận bằng văn bản. Với hợp đồng trọn gói, nếu sau này khách nói "không phải như vậy" thì phải có bằng chứng là khách đã đồng ý. Em cũng ghi giả định này vào assumption log và kiểm chứng sớm với khách qua demo hoặc dữ liệu mẫu, không chờ đến UAT.
> 📘 PMP: Assumption log và Identify Risks: quyết định thay khách là giả định cần được xác nhận; Manage Stakeholder Engagement duy trì trách nhiệm của khách.

## 7.7 Báo cáo định kỳ trong quy trình (báo cáo ngày/tuần, họp định kỳ, biên bản họp trong 24 giờ)

**Q827. Team 20 người ở dự án ngân hàng A viết báo cáo ngày rất dài, mỗi người mất 20–30 phút/ngày, nhưng PM vẫn không nắm được vấn đề. Anh/chị thiết kế lại báo cáo ngày thế nào?**
Em rút báo cáo ngày về 4 mục ngắn: việc đã xong hôm nay (theo mã task WBS, kèm số liệu như số trang, số case), việc ngày mai, **vấn đề/đang bị chặn** (cần ai giúp, từ khi nào), công thực tế theo task. Mục vấn đề đặt lên đầu, có cờ màu để leader lọc nhanh. Dữ liệu công và số liệu được nhập vào công cụ chung để tổng hợp tự động, không viết lại thành văn. Mục tiêu là mỗi người mất không quá 5–10 phút. Em kiểm hiệu quả bằng việc vấn đề có được phát hiện sớm hơn không, đo bằng số ngày từ khi phát sinh đến khi leader biết.
> 📘 PMP: Manage Communications và work performance data: thu thập dữ liệu đủ dùng, đúng định dạng để chuyển thành thông tin.

**Q828. Khách bảo hiểm nhân thọ B yêu cầu báo cáo tuần trong giai đoạn IT. Báo cáo tuần trong quy trình nên có những phần nào?**
Em cấu trúc báo cáo tuần IT gồm: ① Tóm tắt tình trạng (tốt/chú ý/nguy hiểm) và kết luận trong 3 dòng; ② Tiến độ theo giai đoạn: tỷ lệ đã chạy test thực tế so kế hoạch; ③ Chất lượng: số bug phát sinh/giải quyết/còn mở theo mức độ, đường cong hội tụ, tỷ lệ pass; ④ QA: số câu chưa trả lời, quá hạn, câu cần khách ưu tiên; ⑤ vấn đề và rủi ro kèm đối sách, người phụ trách, hạn; ⑥ kế hoạch tuần sau; ⑦ yêu cầu với khách. Số liệu lấy từ cùng một nguồn với báo cáo nội bộ. Bẫy là báo cáo dài nhưng không có phần "cần khách làm gì".
> 📘 PMP: Manage Communications: work performance reports tổng hợp tiến độ, chất lượng, rủi ro theo nhu cầu thông tin của stakeholder.
> 💡 Nhật: Khách Nhật thích báo cáo có "đèn tín hiệu" (đèn tín hiệu xanh – vàng – đỏ) ở đầu; nhưng màu phải có tiêu chí định lượng, không chọn theo cảm giác.

**Q829. Định kỳ thứ Năm có họp định kỳ với khách bảo hiểm phi nhân thọ C, nhưng tài liệu thường gửi lúc 9 giờ sáng cùng ngày, khách không kịp đọc, họp kéo dài 2 tiếng. Anh/chị cải tiến thế nào?**
Em đặt quy tắc: tài liệu họp định kỳ (gồm báo cáo tuần, bảng quản lý Q&A, bảng quản lý vấn đề) gửi **trước ít nhất 1 ngày làm việc**, kèm agenda và danh sách mục cần khách quyết. Trong họp không đọc lại báo cáo mà tập trung vào ngoại lệ: chỉ số ngoài ngưỡng, vấn đề cần quyết định, QA quá hạn. Thời gian mỗi mục được ấn định, mục cần thảo luận dài thì tách họp riêng. Cuối họp đọc lại kết luận và action item. Em đo thời lượng họp và số mục quyết định được để đánh giá. Để làm được, nội bộ cần chốt số liệu chiều hôm trước, đây là kỷ luật của team.
> 📘 PMP: Manage Communications: meeting management (agenda, phân phối tài liệu trước, kết luận rõ ràng).
> 💡 Nhật: Trước họp định kỳ có mục cần quyết, BrSE nên trao đổi riêng trước với đầu mối liên lạc của khách để buổi họp chỉ còn là xác nhận.

**Q830. Interviewer hỏi: "Ở dự án Nhật, biên bản họp viết thế nào và vì sao phải gửi trong 24 giờ?". Anh/chị trả lời ra sao?**
Biên bản họp gồm: thông tin buổi họp (ngày, người tham dự, tài liệu), **mục đã quyết định**, **mục đang xem xét/vấn đề** (chưa quyết, ai xử lý), **việc cần làm/action item** (ai, làm gì, hạn), và các điểm thống nhất quan trọng về spec, phạm vi, lịch. Em viết theo kết luận, không chép lại toàn bộ đối thoại. Gửi trong 24 giờ vì trí nhớ còn mới, sai sót được phát hiện sớm, và khách có căn cứ để báo cáo nội bộ. Em kèm thời hạn xác nhận (vd 2–3 ngày làm việc), quá hạn coi như đồng ý. Biên bản họp được khách xác nhận là bằng chứng khi có tranh chấp.
> 📘 PMP: Manage Communications: ghi nhận quyết định; Monitor Communications: xác nhận thông tin đã được hiểu đúng.
> 💡 Nhật: Phía nào viết biên bản họp thì phía đó nắm "quyền viết lại sự việc"; vendor nên chủ động nhận viết, đặc biệt các buổi bàn về phạm vi.

**Q831. Một tuần sau họp định kỳ, khách ngân hàng A phản đối biên bản họp ghi "khách đồng ý lùi mốc IT 1 tuần", nói chỉ là "sẽ xem xét" (nói bằng tiếng Nhật). Anh/chị xử lý thế nào?**
Em không tranh cãi ai đúng mà xác nhận lại nội dung: đối chiếu ghi chép, hỏi người tham dự phía vendor, nếu có thể thì xem tài liệu trình chiếu lúc đó. Nếu thực tế khách chưa quyết, em sửa biên bản họp thành "vấn đề đang xem xét", và ngay lập tức đưa vấn đề lùi mốc vào agenda để quyết chính thức, vì team đang làm việc theo giả định mới. Phòng ngừa: cuối mỗi buổi họp đọc lại kết luận và hỏi khách xác nhận tại chỗ; phân biệt rõ "đã quyết định" với "sẽ xem xét"; quy định thời hạn xác nhận biên bản họp. Em ghi bài học này để toàn team áp dụng.
> 📘 PMP: Manage Communications và Manage Stakeholder Engagement: xác nhận chung về quyết định; xử lý xung đột bằng sự kiện, không bằng cảm xúc.

**Q832. Team offshore VN chậm hơn Nhật 2 giờ. Báo cáo ngày của team gửi lúc 19 giờ VN (21 giờ Nhật), khách bảo hiểm nhân thọ B phàn nàn thông tin đến quá muộn. Anh/chị xử lý thế nào?**
Em hỏi khách cần thông tin gì, lúc nào và để làm gì. Thường khách cần biết vấn đề trong ngày làm việc của họ để kịp xử lý. Em đề xuất: báo cáo tình trạng vào **17 giờ Nhật** (15 giờ VN) cho các vấn đề và tiến độ đến thời điểm đó; phần còn lại trong ngày gộp vào báo cáo sáng hôm sau. Vấn đề nghiêm trọng không chờ báo cáo mà liên lạc ngay qua BrSE. Em điều chỉnh lịch nội bộ để dữ liệu chốt kịp. Thời gian báo cáo được ghi vào kế hoạch giao tiếp sau khi khách đồng ý.
> 📘 PMP: Plan Communications Management: xác định thời điểm, tần suất, kênh giao tiếp phù hợp với nhu cầu stakeholder và múi giờ.

**Q833. Trong Detail Design ở khách bảo hiểm phi nhân thọ C, member báo tiến độ "đã xong 80%" suốt 2 tuần liền. Anh/chị đo tiến độ theo giai đoạn thế nào để báo cáo đáng tin?**
Em đổi từ tỷ lệ tự khai sang **đo bằng sản phẩm đầu ra có tiêu chí hoàn thành**. Với thiết kế: mỗi tài liệu đi qua các mốc viết xong, tự review xong, review chéo xong, sửa góp ý review xong, khách duyệt; mỗi mốc có trọng số cố định. Với lập trình: chương trình đã review và lên kho. Với test: số case đã chạy và đạt. Tiến độ = tổng trọng số mốc đã đạt ÷ tổng. Cách đo này loại bỏ hiện tượng "90% mãi" vì không có bằng chứng thì không được tính. Em thống nhất cách đo với khách để số trong báo cáo tuần có cùng nghĩa.
> 📘 PMP: Control Schedule và EVM: dùng quy tắc đo khách quan (0/100, 50/50, weighted milestones) cho earned value.
> 💡 Nhật: Khách Nhật hay hỏi "căn cứ của tỷ lệ tiến độ là gì?"; có quy tắc đo rõ sẽ trả lời được ngay.

**Q834. Thứ Hai, PM phát hiện batch tính phí của khách bảo hiểm nhân thọ B có lỗi thiết kế có thể làm trễ IT 1 tuần. Họp định kỳ là thứ Năm. Anh/chị báo khách khi nào và thế nào?**
Em không chờ họp định kỳ. Theo báo cáo – liên lạc – trao đổi, tin xấu phải báo sớm nhất có thể. Trong ngày thứ Hai, em xác nhận nhanh sự kiện và phạm vi ảnh hưởng ở mức sơ bộ, rồi báo khách qua kênh đã thống nhất (BrSE gọi điện hoặc email kèm tóm tắt): vấn đề là gì, ảnh hưởng có thể có, đang làm gì, khi nào có thông tin chi tiết. Sau 1–2 ngày gửi báo cáo đầy đủ với phương án. Ở họp định kỳ thứ Năm, vấn đề đã được biết trước nên tập trung vào quyết định. Báo sớm kèm "chưa đủ thông tin" vẫn tốt hơn báo muộn kèm đầy đủ.
> 📘 PMP: Manage Communications và Monitor Risks: truyền đạt kịp thời thông tin rủi ro đã thành vấn đề; minh bạch là nguyên tắc stewardship (PMBOK 7).

**Q835. Ở ngân hàng A, số bug trong báo cáo team VN gửi BrSE là 142, BrSE báo khách 138, công cụ quản lý bug hiển thị 145. Khách hỏi số nào đúng. Anh/chị xử lý thế nào?**
Em xác minh nguyên nhân chênh lệch: thời điểm chốt số khác nhau, cách đếm khác nhau (có tính phiếu đúng spec, phiếu trùng không), hay nhập tay sai. Em giải thích cho khách và gửi số đúng theo định nghĩa đã thống nhất. Gốc rễ là có nhiều nguồn dữ liệu: em quy định **một nguồn duy nhất** là công cụ quản lý bug, thời điểm chốt cố định (vd 17 giờ thứ Ba), báo cáo xuất tự động từ đó với cùng điều kiện lọc; không ai được sửa số bằng tay. Mọi báo cáo ghi rõ thời điểm chốt dữ liệu.
> 📘 PMP: Manage Communications và Manage Quality: tính toàn vẹn của dữ liệu báo cáo (single source of truth).

**Q836. Khách bảo hiểm phi nhân thọ C yêu cầu báo cáo chi tiết hằng ngày gồm 15 chỉ số trong suốt ST. Team 10 người mất khoảng 1 giờ/ngày cho việc này. Anh/chị xử lý thế nào?**
Em hỏi khách mục đích của từng chỉ số và ai dùng. Thường khách cần một số ít chỉ số hằng ngày (số case đã chạy, bug mới, bug mở theo mức độ) còn phần lớn chỉ cần hằng tuần. Em đề xuất: báo cáo ngày gồm 4–5 chỉ số cốt lõi, xuất tự động; báo cáo tuần đầy đủ 15 chỉ số kèm phân tích. Em tự động hóa việc lấy số từ công cụ quản lý test và bug để giảm công. Nếu khách vẫn muốn đủ hằng ngày, em tính công này vào kế hoạch và báo ảnh hưởng nếu ngoài phạm vi, chứ không để team làm thêm giờ âm thầm.
> 📘 PMP: Tailoring và Plan Communications Management: cân bằng nhu cầu thông tin với chi phí tạo thông tin.

**Q837. Dự án tích hợp của ngân hàng A có 3 bên: khách, vendor VN (bên anh/chị) và vendor Nhật phụ trách hệ thống core. Vấn đề interface thường bị đẩy qua lại giữa hai vendor. Anh/chị tổ chức báo cáo và họp thế nào?**
Em đề xuất khách tổ chức họp định kỳ liên vendor hằng tuần do khách chủ trì, có **bảng quản lý vấn đề chung** cho các vấn đề interface: mỗi vấn đề có một bên chịu trách nhiệm chính, hạn xử lý, bên liên quan. Đặc tả interface có một phiên bản chung được quản lý thay đổi, mọi thay đổi phải được cả hai bên xác nhận. Biên bản họp liên vendor do một bên viết, cả ba bên xác nhận. Bên em chuẩn bị dữ liệu cụ thể (log, dữ liệu đầu vào/ra) khi nêu vấn đề để tránh tranh luận cảm tính. Em không trực tiếp chỉ đạo vendor khác mà làm qua khách.
> 📘 PMP: Manage Stakeholder Engagement và Manage Communications: thiết lập kênh giao tiếp chính thức giữa nhiều bên; issue log có owner rõ ràng.
> 💡 Nhật: Với khách Nhật, vendor không có quan hệ hợp đồng trực tiếp với nhau; mọi yêu cầu sang vendor kia nên đi qua đầu mối liên lạc của khách.

**Q838. Bản báo cáo tuần tiếng Nhật gửi khách bảo hiểm nhân thọ B ghi "bug còn mở: 12", bản tiếng Việt nội bộ ghi 21, do người dịch đảo số. Khách đã dùng số 12 báo cáo lên cấp trên. Anh/chị xử lý thế nào?**
Em báo khách ngay khi phát hiện, xin lỗi, gửi số đúng kèm giải thích ngắn gọn để khách có thể chỉnh báo cáo nội bộ của họ. Em kiểm tra các báo cáo trước đó xem có sai tương tự không. Gốc rễ là số liệu được gõ tay lại khi dịch: em thay đổi cách làm để phần số liệu và đồ thị xuất tự động từ cùng một nguồn cho cả hai ngôn ngữ, chỉ dịch phần diễn giải; thêm bước kiểm đối chiếu số giữa hai bản trước khi gửi. Em ghi vào báo cáo cải tiến để rà soát và áp dụng sang các báo cáo khác của dự án.
> 📘 PMP: Manage Quality cho quy trình báo cáo: phòng ngừa lỗi bằng tự động hóa (mistake-proofing) thay vì chỉ kiểm tra.

## 7.8 báo cáo chất lượng và phân tích chất lượng theo giai đoạn

**Q839. Lần đầu làm PM cho khách bảo hiểm nhân thọ B, anh/chị được yêu cầu nộp báo cáo chất lượng kết thúc IT. Cấu trúc báo cáo nên gồm những phần nào?**
Em viết theo cấu trúc: ① Tổng quan: phạm vi, quy mô, thời gian, môi trường; ② Đánh giá định lượng: mật độ test, mật độ bug, tỷ lệ đã chạy test, tỷ lệ pass, đường cong hội tụ, bug còn mở theo mức độ, so với ngưỡng; ③ Đánh giá định tính: phân tích bug theo nguyên nhân, giai đoạn sinh ra lỗi, module, các điểm ngoài ngưỡng và lý do; ④ Đánh giá chất lượng tổng thể và kết luận có đạt tiêu chí ra không; ⑤ vấn đề còn lại và kế hoạch xử lý; ⑥ biện pháp cải tiến cho giai đoạn sau. Phụ lục là dữ liệu chi tiết và bằng chứng. Kết luận phải dựa trên số liệu và phân tích.
> 📘 PMP: Control Quality cho ra quality control measurements và verified deliverables; báo cáo là đầu vào cho Validate Scope.
> 💡 Nhật: Khách Nhật đọc phần đánh giá định tính kỹ nhất; một bảng số đẹp mà phân tích sơ sài thường bị trả lại với câu "phân tích nông".

**Q840. Trong báo cáo chất lượng UT của ngân hàng A, mật độ bug của 4/20 module vượt cận trên, team chỉ ghi "đã sửa hết bug". Khách trả lại báo cáo. Lẽ ra phải viết thế nào?**
Mỗi chỉ số ngoài ngưỡng phải có phân tích nguyên nhân và đánh giá ảnh hưởng. Với 4 module: bug tập trung vào loại nào, nguồn gốc từ thiết kế hay code, vì sao module đó nhiều bug (độ phức tạp, người làm mới, spec thay đổi nhiều). Sau đó là đánh giá: sau khi sửa, chất lượng đã đủ chưa, căn cứ là gì (đã review lại code, bổ sung case, retest đạt), và biện pháp cho IT (tăng test ở các module này). Câu "đã sửa hết" chỉ nói về bug đã biết, không trả lời được câu hỏi khách quan tâm: còn bug ẩn không.
> 📘 PMP: Control Quality: phân tích biến động (variance) và nguyên nhân, không chỉ báo cáo kết quả.

**Q841. Công ty dùng thang đánh giá ◎ (tốt), ○ (đạt), △ (cần chú ý), × (không đạt) cho từng chỉ số và tổng thể trong báo cáo chất lượng. Anh/chị xác định tiêu chí đánh giá từng mức thế nào?**
Em định nghĩa tiêu chí trước khi bắt đầu giai đoạn và ghi vào kế hoạch chất lượng. Ví dụ với từng chỉ số: ○ là trong ngưỡng; △ là ngoài ngưỡng nhưng đã phân tích và có lý do hợp lý hoặc đã có biện pháp; × là ngoài ngưỡng chưa giải thích được hoặc có bug mức cao còn mở. Đánh giá tổng thể: đạt khi không có chỉ số ×, các mục △ đều có đối sách và bằng chứng. Mức ◎ chỉ dùng khi có căn cứ rõ ràng, không dùng để trang trí. Tiêu chí cố định giúp đánh giá nhất quán giữa các module và các lần báo cáo.
> 📘 PMP: Plan Quality Management: xác định tiêu chí chấp nhận và cách đánh giá trước khi đo.
> 💡 Nhật: Ký hiệu ◎○△× rất quen với khách Nhật, nhưng thiếu định nghĩa đi kèm thì khách sẽ hỏi lại căn cứ của từng ô.

**Q842. ST của khách bảo hiểm phi nhân thọ C có mật độ bug thấp hơn cận dưới, nhưng PM tin chất lượng tốt vì đây là lần sửa đổi thứ 3 của hệ thống ổn định. Anh/chị viết phần này trong báo cáo chất lượng thế nào để khách chấp nhận?**
Em không chỉ viết "vì hệ thống ổn định" mà đưa ra **bằng chứng có thể kiểm tra**: mật độ test và độ phủ yêu cầu đạt ngưỡng (test đủ); phân tích các bug tìm được cho thấy không tập trung vào nhóm nào; kết quả review ở giai đoạn trước đã loại nhiều lỗi (mật độ góp ý review cao, bug UT/IT đủ); so sánh với dữ liệu hai lần sửa đổi trước của cùng hệ thống. Nếu vẫn còn nghi ngờ, em đề xuất test bổ sung có mục tiêu (vd một nhóm kịch bản bất thường) và ghi kết quả. Kết luận dạng: "mật độ thấp, sau phân tích đánh giá là do chất lượng ổn định, không do thiếu test".
> 📘 PMP: Control Quality: phán đoán dựa trên nhiều nguồn dữ liệu (triangulation) khi một chỉ số nằm ngoài giới hạn.
> 💡 Nhật: Khách Nhật hay chấp nhận ngoại lệ khi vendor chủ động nêu và chứng minh; nếu để khách tự phát hiện thì dù đúng vẫn mất điểm.

**Q843. Khách ngân hàng A trả lại báo cáo chất lượng IT với nhận xét: "ghi là không có vấn đề gì nhưng không có căn cứ". Anh/chị viết lại thế nào?**
Em thay mỗi câu "không có vấn đề" bằng ba yếu tố: **con số** (giá trị so ngưỡng), **phân tích** (vì sao như vậy, có điểm gì đặc biệt), **kết luận có căn cứ**. Ví dụ: "Tỷ lệ pass 99,2% (ngưỡng ≥ 95%); 8 case NG đều do 1 bug interface đã sửa và retest đạt ngày 12/10; không có bug mức cao còn mở; đường cong hội tụ trong 20% case cuối; đánh giá: đạt". Em thêm phần điểm yếu và rủi ro còn lại, vì báo cáo không có điểm yếu nào thì không đáng tin. Trước khi gửi lại, em nhờ bộ phận QA nội bộ review báo cáo.
> 📘 PMP: Manage Communications: báo cáo phải có bằng chứng và diễn giải; Control Quality dùng dữ liệu làm căn cứ.

**Q844. Kết thúc ST ở khách bảo hiểm nhân thọ B, khách yêu cầu phân tích "chất lượng có được xây dựng ở từng giai đoạn không". Anh/chị phân tích thế nào?**
Em lập bảng theo giai đoạn: số góp ý review ở Basic Design, Detail Design, code; số bug ở UT, IT, ST; mật độ từng giai đoạn so ngưỡng. Sau đó là ma trận giai đoạn sinh ra lỗi × giai đoạn phát hiện lỗi: nếu phần lớn lỗi được phát hiện ngay ở giai đoạn sinh ra hoặc giai đoạn kế tiếp, quy trình đang hiệu quả; nếu nhiều lỗi thiết kế lọt đến ST, chất lượng chưa được xây dựng tốt ở thượng nguồn. Em tính tỷ lệ lọt qua từng giai đoạn và đưa nhận định: giai đoạn nào làm tốt, giai đoạn nào yếu, nguyên nhân và đề xuất cho các dự án hoặc phase sau.
> 📘 PMP: Manage Quality: đánh giá hiệu quả quy trình chất lượng (process analysis); lessons learned cho cải tiến tổ chức.

**Q845. Dự án migration của khách bảo hiểm phi nhân thọ C, ngoài test chức năng còn kiểm chứng dữ liệu chuyển đổi 3 lần diễn tập. Báo cáo chất lượng trước cutover nên trình bày phần dữ liệu thế nào?**
Em trình bày riêng một chương chất lượng dữ liệu: ① Phạm vi: số bảng, số bản ghi, loại dữ liệu; ② Kết quả từng lần diễn tập: khớp số bản ghi, khớp tổng kiểm cột tiền, kiểm mẫu chi tiết, số lỗi chuyển đổi theo loại; ③ Xu hướng qua 3 lần: lỗi giảm dần đến 0 ở lần cuối hay chưa; ④ Thời gian chạy chuyển đổi so cửa sổ cho phép; ⑤ các lỗi còn lại và cách xử lý (sửa trước, sửa tay sau chuyển, chấp nhận có điều kiện); ⑥ kết luận sẵn sàng hay chưa. Bằng chứng là log đối chiếu tự động được lưu.
> 📘 PMP: Control Quality với statistical sampling và inspection; Plan Risk Responses cho rủi ro chuyển đổi.
> 💡 Nhật: Khách bảo hiểm Nhật thường yêu cầu "tiêu chí quyết định go/no-go" được ký trước diễn tập; báo cáo phải đối chiếu đúng từng tiêu chí này.

**Q846. Báo cáo chất lượng UT của ngân hàng A có 50 module, bản nháp dài 120 trang vì mỗi module một phân tích. Khách nói không đọc được. Anh/chị cấu trúc lại thế nào?**
Em chia báo cáo hai tầng. Tầng tổng hợp (khoảng 10–15 trang): chỉ số toàn bộ, biểu đồ phân bố mật độ của 50 module (vd biểu đồ phân tán mật độ test × mật độ bug với vùng ngưỡng), danh sách **module ngoài ngưỡng** cùng phân tích chi tiết, phân tích nguyên nhân chung, kết luận. Tầng phụ lục: bảng số liệu từng module, không viết phân tích dài cho các module bình thường. Như vậy khách thấy ngay chỗ cần chú ý. Em hỏi trước khách định dạng mong muốn, vì một số khách vẫn muốn bảng từng module, nhưng phần tóm tắt luôn đặt đầu.
> 📘 PMP: Manage Communications: điều chỉnh mức độ chi tiết theo người nhận; dùng data representation (scatter diagram) để truyền đạt hiệu quả.

**Q847. Công ty có bộ phận đảm bảo chất lượng độc lập. PM muốn gửi thẳng báo cáo chất lượng ST cho khách bảo hiểm nhân thọ B để kịp hạn, bỏ qua bước QA nội bộ review. Anh/chị có đồng ý không?**
Em không đồng ý bỏ bước này. QA nội bộ review là để có góc nhìn độc lập: phát hiện chỉ số tính sai, phân tích thiếu, kết luận không đủ căn cứ, trước khi khách thấy. Nếu thời gian gấp, em làm việc với QA nội bộ từ sớm: gửi bản nháp từng phần ngay khi có dữ liệu, thống nhất thời gian review rút ngắn, hoặc review song song khi đang hoàn thiện. Nếu vẫn không kịp, em báo khách sẽ trễ 1–2 ngày để có báo cáo đã kiểm tra. Báo cáo sai gửi đúng hạn gây mất niềm tin nhiều hơn báo cáo đúng gửi trễ một chút.
> 📘 PMP: Manage Quality: quality audit độc lập bảo đảm quy trình và sản phẩm đạt chuẩn tổ chức.

**Q848. Khách bảo hiểm phi nhân thọ C yêu cầu evidence cho mọi case ST (ảnh chụp màn hình, log, dữ liệu trước/sau). Đến lúc làm báo cáo, 15% case thiếu bằng chứng. Anh/chị xử lý thế nào?**
Em xác định 15% case đó là gì: đã chạy đạt nhưng quên lưu bằng chứng, hay chưa thực sự chạy. Case không có bằng chứng thì không được tính là đạt. Em cho chạy lại các case này và thu bằng chứng, ưu tiên case quan trọng, rồi cập nhật tỷ lệ đã chạy test và tỷ lệ pass trung thực. Nếu ảnh hưởng tiến độ, em báo khách. Phòng ngừa: quy định cái gì, đặt tên thế nào, lưu ở đâu trước khi test; người test chỉ được đổi trạng thái case thành "đạt" khi đã gắn bằng chứng; leader kiểm mẫu hằng ngày. Bằng chứng chứa dữ liệu cá nhân phải được che và lưu đúng nơi được phép.
> 📘 PMP: Control Quality: verified deliverables phải có hồ sơ chứng minh; Manage Quality thiết kế quy trình phòng ngừa thiếu sót.
> 💡 Nhật: Với khách tài chính, evidence thiếu thường bị coi như chưa test; một số khách còn kiểm ngẫu nhiên bằng chứng khi nghiệm thu.

**Q849. Kết thúc IT ở ngân hàng A, còn 6 bug mức Medium và 2 yêu cầu cải tiến chưa xử lý. Khách đồng ý chuyển ST. Trong báo cáo chất lượng phần vấn đề còn lại anh/chị viết thế nào?**
Em liệt kê từng mục với đủ thông tin: mã bug/vấn đề, nội dung, mức độ, ảnh hưởng đến nghiệp vụ và đến ST (có chặn kịch bản nào không), workaround nếu có, phương án xử lý, người phụ trách, hạn hoàn thành, và giai đoạn sẽ kiểm tra lại. Em tách rõ bug và yêu cầu cải tiến (cải tiến có thể là thay đổi, cần change control). Em ghi rõ khách đã đồng ý chuyển ST với các mục này tại buổi nào. Ở các báo cáo tuần ST, danh sách này được theo dõi đến khi đóng. Bẫy là ghi "sẽ xử lý trong ST" không có hạn cụ thể.
> 📘 PMP: Issue log và Monitor Risks: vấn đề còn mở được chuyển tiếp có owner, hạn và theo dõi.

**Q850. Mọi chỉ số ST của khách bảo hiểm nhân thọ B đều trong ngưỡng, nhưng PM thấy lo vì module tính lãi chậm chưa được test với dữ liệu hợp đồng thật cũ hơn 20 năm. Anh/chị thể hiện điều này trong báo cáo chất lượng thế nào?**
Em không giấu nhận định này vì chỉ số đẹp. Trong phần đánh giá định tính hoặc rủi ro còn lại, em ghi rõ: chỉ số đạt, nhưng có **giới hạn của phạm vi test** là dữ liệu hợp đồng rất cũ chưa được kiểm; nêu lý do lo ngại (quy tắc tính lãi thay đổi qua nhiều thời kỳ), ảnh hưởng có thể có, và đề xuất cụ thể: lấy mẫu dữ liệu thật (đã che thông tin) để test bổ sung trước UAT, hoặc đưa vào kịch bản UAT với khách. Báo cáo chất lượng tốt cần trung thực về những gì chưa biết, không chỉ những gì đã đo.
> 📘 PMP: Stewardship và honesty (PMBOK 7, code of ethics): báo cáo đầy đủ rủi ro đã nhận diện; Identify Risks dựa trên phán đoán chuyên gia.

## 7.9 phân tích 5 Why, phòng ngừa tái diễn, rà soát và áp dụng sang chỗ tương tự trong quy trình

**Q851. Interviewer hỏi: "Anh/chị làm phân tích 5 Why thế nào? Khi nào thì dừng hỏi 'tại sao'?". Anh/chị trả lời ra sao?**
Phân tích 5 Why bắt đầu từ một sự kiện mô tả bằng fact cụ thể, không phải nhận định. Mỗi tầng hỏi "tại sao điều này xảy ra", câu trả lời phải là sự kiện kiểm chứng được và có quan hệ nhân quả với tầng trên; một tầng có thể có nhiều nhánh. Em dừng khi đến **nguyên nhân thuộc về quy trình hoặc cơ chế mà team kiểm soát được và có thể đặt biện pháp**, thường sau khoảng 3–5 tầng (tham khảo). Không dừng ở "do người làm bất cẩn" vì đó không phải nguyên nhân có thể sửa bằng quy trình. Cuối cùng đọc ngược từ dưới lên bằng "vì vậy" để kiểm logic.
> 📘 PMP: Root cause analysis với kỹ thuật 5 Whys; kết hợp fishbone (Ishikawa) khi có nhiều nhóm nguyên nhân.
> 💡 Nhật: Khách Nhật sẽ trả lại phân tích nếu kết luận là "thiếu chú ý" hoặc "thiếu kiểm tra" mà không giải thích vì sao cơ chế không ngăn được.

**Q852. Trong UAT của khách bảo hiểm nhân thọ B, phát hiện bug tính sai phí cho hợp đồng có kỳ đóng phí nửa năm. Khách yêu cầu báo cáo sự cố trong 3 ngày. Báo cáo này gồm những phần nào?**
Em viết theo cấu trúc: ① Sự kiện: xảy ra gì, khi nào, ai phát hiện; ② Phạm vi ảnh hưởng: bao nhiêu hợp đồng, sai bao nhiêu tiền, có ảnh hưởng dữ liệu khác không; ③ Xử lý tạm thời đã làm; ④ **Nguyên nhân** gồm nguyên nhân phát sinh và nguyên nhân lọt, phân tích bằng 5 Why; ⑤ biện pháp lâu dài cho cả hai nhánh nguyên nhân; ⑥ **rà soát và áp dụng sang chỗ tương tự**: phạm vi kiểm tra tương tự và kết quả; ⑦ lịch thực hiện và cách xác nhận hiệu quả. Em gửi bản sơ bộ trong ngày nếu khách cần, báo cáo đầy đủ trong hạn.
> 📘 PMP: Control Quality và Manage Communications: báo cáo sự cố có cấu trúc; root cause analysis dẫn đến corrective và preventive action.

**Q853. Biện pháp tái phát trong báo cáo sự cố gửi ngân hàng A ghi "nhắc nhở toàn team cẩn thận hơn khi code điều kiện biên". Khách trả lại. Anh/chị sửa biện pháp thế nào?**
"Nhắc nhở" phụ thuộc vào trí nhớ của người, hiệu quả giảm dần theo thời gian, nên khách không chấp nhận. Em đổi sang biện pháp **cơ chế**: bổ sung mục điều kiện biên vào checklist review code và test spec UT bắt buộc; thêm quy tắc phân tích tĩnh nếu công cụ hỗ trợ; mẫu thiết kế case bắt buộc có giá trị biên; leader kiểm mẫu khi review. Mỗi biện pháp có người phụ trách, ngày áp dụng và cách đo hiệu quả (vd số bug điều kiện biên ở IT giảm). Nhắc nhở vẫn có thể làm, nhưng chỉ là bổ sung.
> 📘 PMP: Corrective/preventive action trong Manage Quality: ưu tiên mistake-proofing và thay đổi quy trình hơn là dựa vào ý thức cá nhân.
> 💡 Nhật: Trong báo cáo sự cố, biện pháp nên ưu tiên "ngăn bằng cơ chế"; cụm "phổ biến triệt để" đứng một mình thường bị đánh giá là yếu.

**Q854. Bug "không xử lý ngày 29/2 khi tính kỳ hạn hợp đồng" được phát hiện trong ST của khách bảo hiểm phi nhân thọ C. Anh/chị triển khai rà soát và áp dụng sang chỗ tương tự thế nào?**
Em xác định **mẫu lỗi** chứ không chỉ chỗ lỗi: logic tính ngày có liên quan năm nhuận và cuối tháng. Sau đó tìm toàn bộ nơi có mẫu tương tự: tìm trong source các hàm và chỗ xử lý ngày, tìm trong tài liệu thiết kế các quy tắc tính kỳ hạn, ngày đến hạn, ngày tái tục. Lập danh sách vị trí, kiểm tra từng chỗ (review code + test với dữ liệu 28/2, 29/2, 31 các tháng), ghi kết quả: không vấn đề, đã sửa, cần xác nhận khách. Em báo phạm vi và kết quả rà soát và áp dụng sang chỗ tương tự trong báo cáo sự cố. Phòng ngừa: đưa dữ liệu ngày đặc biệt vào bộ dữ liệu test chuẩn.
> 📘 PMP: Preventive action và lessons learned: mở rộng biện pháp cho các thành phần có rủi ro tương tự (systems thinking).

**Q855. Phân tích bug UAT ở khách bảo hiểm nhân thọ B, team chỉ hỏi "tại sao lỗi được tạo ra" và kết luận do dev hiểu sai spec. Thiếu gì trong phân tích này?**
Thiếu nhánh nguyên nhân lọt: vì sao lỗi đi qua review Detail Design, review code, UT, IT, ST mà không bị phát hiện. Mỗi lớp kiểm tra có lý do riêng: review không đối chiếu spec, case UT viết theo cách hiểu của chính dev, case IT/ST không có dữ liệu loại hợp đồng này. Em làm 5 Why hai nhánh song song: vì sao tạo ra và vì sao không phát hiện, mỗi nhánh có biện pháp riêng. Thường biện pháp cho nhánh lọt có hiệu quả rộng hơn vì nó bảo vệ cả khỏi các lỗi khác chưa biết.
> 📘 PMP: Root cause analysis: phân tích cả nguyên nhân gốc của lỗi và điểm yếu của hệ thống kiểm soát chất lượng.
> 💡 Nhật: Mẫu báo cáo sự cố của nhiều khách Nhật có sẵn hai cột "nguyên nhân phát sinh" và "nguyên nhân lọt lỗi"; thiếu một cột là báo cáo bị trả lại ngay.

**Q856. Trong buổi phân tích 5 Why về bug nghiêm trọng ở ngân hàng A, leader liên tục chỉ trích dev phụ trách, dev im lặng và không nói thật về những gì đã xảy ra. Anh/chị xử lý thế nào?**
Em dừng lại và đặt lại nguyên tắc buổi phân tích: tìm nguyên nhân ở **quy trình và cơ chế**, không tìm người có lỗi. Câu hỏi được chuyển từ "tại sao em làm vậy" sang "điều gì trong quy trình khiến việc này có thể xảy ra". Em nói chuyện riêng với leader về cách dẫn dắt, và nói riêng với dev để lấy thông tin thật. Nếu cần, em chủ trì buổi phân tích lần sau. Không có an toàn tâm lý thì mọi người sẽ giấu thông tin, phân tích sai, biện pháp không trúng, và lỗi sẽ lặp lại.
> 📘 PMP: Manage Team và nguyên tắc PMBOK 7 về tạo môi trường hợp tác (psychological safety); root cause analysis không quy lỗi cá nhân.

**Q857. Một tháng trước, ở khách bảo hiểm phi nhân thọ C, team áp dụng biện pháp tái phát "thêm checklist review cho xử lý ngoại lệ". Khách hỏi biện pháp có hiệu quả không. Anh/chị chứng minh thế nào?**
Em làm xác nhận hiệu quả bằng dữ liệu đã định trước khi áp dụng: ① Tuân thủ: tỷ lệ review có checklist này được điền đầy đủ; ② Kết quả: số góp ý review về xử lý ngoại lệ phát hiện ở review tăng lên (lỗi được bắt sớm hơn), và số bug về xử lý ngoại lệ ở test giảm so với giai đoạn trước, chuẩn hóa theo quy mô. Nếu tuân thủ thấp, vấn đề là triển khai; nếu tuân thủ cao mà bug không giảm, biện pháp chưa trúng và cần phân tích lại. Em báo khách kết quả dạng so sánh trước/sau, kèm quyết định giữ, sửa hay bỏ biện pháp.
> 📘 PMP: Manage Quality và Control Quality: đo hiệu quả của corrective action theo vòng PDCA.

**Q858. Công ty có 3 dự án đang làm cho cùng nhóm bảo hiểm B. Dự án của anh/chị vừa xử lý bug nghiêm trọng về làm tròn phí. Anh/chị rà soát và áp dụng ra ngoài dự án thế nào?**
Em chia sẻ qua kênh chính thức của tổ chức: gửi PMO và bộ phận phòng đảm bảo chất lượng tóm tắt sự kiện, mẫu lỗi, cách phát hiện, biện pháp; đề nghị PMO yêu cầu 2 dự án kia kiểm tra mẫu lỗi tương tự trong code và tài liệu của họ, có báo cáo kết quả. Em bổ sung bài học vào kho lessons learned và checklist chuẩn của công ty cho ngành bảo hiểm. Nếu khách B có kênh chung cho nhiều dự án, em trao đổi với khách về việc chia sẻ. Thông tin khách được chia sẻ trong phạm vi cho phép.
> 📘 PMP: Manage Project Knowledge và organizational process assets: lessons learned được cập nhật để các dự án khác dùng.
> 💡 Nhật: Khách Nhật đánh giá cao vendor "rà soát và áp dụng sang chỗ tương tự" ra toàn công ty; khi họ phát hiện cùng lỗi ở dự án khác của cùng vendor thì mức tin tưởng giảm mạnh.

**Q859. Phân tích 5 Why cho bug ở ngân hàng A cho thấy nguyên nhân gốc là câu trả lời QA của khách sai, nhưng team cũng không đối chiếu với tài liệu hiện hành. Anh/chị viết phần nguyên nhân trong báo cáo sự cố thế nào?**
Em viết trung thực theo sự kiện, không đổ lỗi và cũng không nhận hết. Nêu chuỗi nguyên nhân: câu trả lời QA số… khác với tài liệu hiện hành mục…; vendor đã không đối chiếu câu trả lời với tài liệu hiện hành trước khi phản ánh vào thiết kế. Biện pháp chia hai phía: phía vendor bổ sung bước đối chiếu QA với tài liệu liên quan và nêu mâu thuẫn trước khi áp dụng; phía khách đề xuất (không áp đặt) quy trình xác nhận QA có ảnh hưởng tính toán. Trước khi gửi, em trao đổi trước với khách (trao đổi riêng trước với từng người liên quan) để phần nguyên nhân phía khách không gây bất ngờ.
> 📘 PMP: Manage Stakeholder Engagement và root cause analysis: trình bày khách quan, tập trung vào giải pháp hệ thống.

**Q860. Sau 6 tháng ở khách bảo hiểm nhân thọ B, dự án đã có 25 biện pháp tái phát từ các báo cáo sự cố. Checklist review dài 180 mục, team bắt đầu tick cho có. Anh/chị xử lý thế nào?**
Em rà lại toàn bộ 25 biện pháp: biện pháp nào trùng nhau, biện pháp nào đã được tự động hóa thay thế, biện pháp nào không còn phù hợp với giai đoạn hiện tại, và đo hiệu quả của từng cái. Gộp và rút gọn checklist theo loại tài liệu và mức rủi ro: mỗi checklist ngắn, tập trung vào mục lỗi hay gặp. Biện pháp chuyển sang công cụ kiểm tự động khi có thể. Thay đổi được trình khách vì một số biện pháp đã cam kết trong báo cáo sự cố. Quy trình phải đơn giản đủ để người ta làm thật, nếu không thì chỉ là giấy tờ.
> 📘 PMP: Manage Quality và continuous improvement: tối ưu quy trình, loại bỏ hoạt động không tạo giá trị (lean thinking).

**Q861. Ba tháng trước ở khách bảo hiểm phi nhân thọ C đã có biện pháp cho lỗi "sai mapping mã sản phẩm", nay lỗi cùng loại lại xảy ra ở diễn tập migration lần 2. Anh/chị làm gì?**
Lỗi tái phát sau khi đã có biện pháp nghĩa là **lần phân tích trước chưa trúng nguyên nhân gốc** hoặc biện pháp không được thực hiện. Em kiểm hai việc: biện pháp cũ có được áp dụng thật không (bằng chứng), và lỗi lần này có đúng cùng cơ chế không. Sau đó làm lại 5 Why, bắt đầu từ câu hỏi "tại sao biện pháp trước không ngăn được". Ví dụ biện pháp chỉ áp dụng cho bảng mapping cũ, còn bảng mới thêm sau không có trong phạm vi. Em báo khách thẳng thắn rằng biện pháp trước chưa đủ, kèm phân tích mới và biện pháp mạnh hơn, như đối chiếu tự động mapping với danh mục gốc.
> 📘 PMP: Control Quality và PDCA: khi corrective action không hiệu quả, quay lại bước phân tích thay vì chỉ thêm biện pháp.

**Q862. Diễn tập migration của khách bảo hiểm nhân thọ B phát hiện tên khách hàng có ký tự ngoài bảng mã chuẩn bị chuyển thành "?" ở bảng hợp đồng. Anh/chị xử lý và rà soát và áp dụng sang chỗ tương tự thế nào?**
Ngay lập tức em xác định phạm vi: bảng hợp đồng có bao nhiêu bản ghi lỗi, ký tự nào. Sau đó rà soát chỗ tương tự theo **dữ liệu** chứ không theo bảng: mọi cột kiểu chữ có thể chứa tên người, địa chỉ, tên công ty trong tất cả các bảng (người được bảo hiểm, người thụ hưởng, đại lý…). Em cùng khách lập danh sách ký tự ngoài bảng mã chuẩn thực tế có trong dữ liệu, thống nhất quy tắc chuyển đổi cho từng ký tự, thêm bước kiểm tự động phát hiện ký tự thay thế sau chuyển đổi. Nguyên nhân lọt: bộ dữ liệu test không có ký tự ngoài bảng mã chuẩn; biện pháp là đưa mẫu dữ liệu thật đã che thông tin vào test.
> 📘 PMP: Root cause analysis và preventive action theo hướng systems thinking: xác định toàn bộ phạm vi rủi ro cùng bản chất.
> 💡 Nhật: Dữ liệu tên người Nhật ở hệ thống cũ thường có ký tự ngoài bảng mã chuẩn do từng công ty tự định nghĩa; cần hỏi khách bảng ký tự ngoài bảng mã chuẩn riêng của họ ngay từ định nghĩa yêu cầu migration.

## 7.10 Câu khó: chỉ số đẹp nhưng chất lượng thật kém, khách yêu cầu chỉ số khác chuẩn, thiếu dữ liệu lịch sử

**Q863. Ở ngân hàng A, ST đạt mọi chỉ số: mật độ test, mật độ bug trong ngưỡng, tỷ lệ pass 99%, đường cong hội tụ. Nhưng tuần đầu UAT khách phát hiện 25 bug, nhiều bug ở luồng nghiệp vụ cơ bản. Anh/chị phân tích thế nào?**
Chỉ số đẹp mà UAT nhiều bug nghĩa là **chỉ số đo sai thứ cần đo**. Em phân tích 25 bug: thuộc luồng nghiệp vụ nào, có kịch bản ST tương ứng không, nếu có thì vì sao không phát hiện (kỳ vọng sai, dữ liệu không thực tế, kiểm tra hời hợt). Thường gặp: kịch bản ST viết theo tài liệu thiết kế của vendor chứ không theo cách khách vận hành thực tế, nên ST xác nhận "làm đúng thiết kế" chứ không xác nhận "đúng nghiệp vụ". Hành động: báo khách ngay, cùng người dùng khách bổ sung kịch bản theo luồng thực tế và chạy lại; về lâu dài, thêm chỉ số độ phủ nghiệp vụ, mời khách review kịch bản ST.
> 📘 PMP: Validate Scope khác Control Quality: đúng thiết kế chưa chắc đúng nhu cầu; tiêu chí chất lượng phải gắn với giá trị cho khách.
> 💡 Nhật: Khách Nhật sẽ hỏi "ST đã xác nhận những gì"; trả lời bằng ma trận nghiệp vụ thuyết phục hơn trả lời bằng số case.

**Q864. Khách bảo hiểm nhân thọ B yêu cầu báo cáo mật độ bug theo FP (function point) và dùng ngưỡng riêng của họ, trong khi chuẩn công ty là KLOC và không có dữ liệu FP lịch sử. Anh/chị xử lý thế nào?**
Em tôn trọng chuẩn của khách vì đó là ngôn ngữ họ dùng để đánh giá. Em đề xuất báo cáo **song song**: theo FP cho khách, theo KLOC cho nội bộ để so với baseline công ty. Cần đo FP: hoặc khách cung cấp FP đã đếm, hoặc em bố trí người có kỹ năng đếm theo phương pháp khách dùng, thống nhất cách đếm với khách trước. Công đo FP thêm vào kế hoạch; nếu ngoài ước lượng ban đầu thì xử lý qua change request. Em ghi việc chuyển đổi đơn vị vào kế hoạch chất lượng, và sau dự án lưu dữ liệu FP để công ty có baseline cho lần sau.
> 📘 PMP: Tailoring và Plan Quality Management: áp dụng tiêu chuẩn của khách; đồng thời đóng góp organizational process assets.

**Q865. Công ty lần đầu làm dự án migration mainframe cho khách bảo hiểm phi nhân thọ C, không có dữ liệu lịch sử để đặt ngưỡng chất lượng. Khách yêu cầu ngưỡng ngay trong kế hoạch chất lượng. Anh/chị xử lý thế nào?**
Em đặt **ngưỡng tạm có cơ chế hiệu chỉnh**. Nguồn tham khảo: dữ liệu dự án tương tự của công ty dù khác công nghệ, chuẩn khách cung cấp nếu có, tài liệu tham khảo công khai như Sách trắng dữ liệu phát triển phần mềm của IPA ở mức tham khảo. Em ghi rõ trong kế hoạch chất lượng: ngưỡng là tạm thời, sẽ hiệu chỉnh sau khi có dữ liệu thực tế của 2–3 module đầu tiên (pilot), việc hiệu chỉnh có khách đồng ý. Song song, em dùng các chỉ số không cần ngưỡng lịch sử: đường cong hội tụ, xu hướng bug mở, so sánh kết quả cũ – mới. Bẫy là đặt ngưỡng cố định rồi bám vào như chân lý.
> 📘 PMP: Progressive elaboration và rolling wave planning áp dụng cho tiêu chí chất lượng; benchmarking khi thiếu dữ liệu nội bộ.
> 💡 Nhật: Khách Nhật chấp nhận "giá trị tạm" nếu kế hoạch ghi rõ thời điểm và cách xem xét lại; điều họ không chấp nhận là ngưỡng thay đổi mà không báo.

**Q866. Phát hiện ở dự án ngân hàng A: một sub-team gộp nhiều bug thành một phiếu và ghi bug UT thành "cải tiến" để mật độ bug nằm trong ngưỡng. Anh/chị xử lý thế nào?**
Em xác nhận sự kiện qua dữ liệu và trao đổi trực tiếp với sub-team, không kết luận vội. Nếu đúng, em yêu cầu phân loại lại phiếu theo quy tắc, tính lại chỉ số và báo khách nếu báo cáo đã gửi bị ảnh hưởng. Gốc rễ thường là áp lực: bị trách khi chỉ số xấu. Em làm rõ với cả team: chỉ số xấu được phân tích và hỗ trợ, còn sửa số là vi phạm nghiêm trọng. Em đổi cách quản lý: không dùng chỉ số để đánh giá cá nhân, kiểm mẫu phân loại phiếu định kỳ, dùng nhiều chỉ số chéo để phát hiện bất thường. Nếu cố ý, xử lý theo quy định công ty.
> 📘 PMP: Code of ethics (honesty, responsibility) và Manage Team: xử lý hành vi sai lệch đồng thời loại bỏ động cơ trong hệ thống.

**Q867. Khách bảo hiểm nhân thọ B đặt điều kiện trong hợp đồng: mật độ bug ST không được vượt 1 bug/KLOC, vượt thì phạt. Team bắt đầu ngại ghi bug. Anh/chị xử lý thế nào?**
Ngưỡng chỉ có cận trên gắn với phạt tạo ra động cơ giấu bug, đi ngược với mục tiêu chất lượng của chính khách. Em vẫn giữ quy tắc trong team: mọi bug phải ghi đầy đủ, ai giấu là vi phạm. Với khách, em đề xuất trao đổi lại (qua người có thẩm quyền và bộ phận hợp đồng) cách đánh giá: dùng chỉ số kết quả như bug lọt sang UAT và production, hoặc bổ sung cận dưới và phân tích. Em chuẩn bị dữ liệu và lập luận rằng cách này bảo vệ khách tốt hơn. Nếu điều khoản không đổi được, em đảm bảo chất lượng tại thượng nguồn để bug ST thấp thật.
> 📘 PMP: Systems thinking (PMBOK 7): cơ chế đo và thưởng phạt tác động lên hành vi; Manage Stakeholder Engagement để điều chỉnh kỳ vọng.

**Q868. Dữ liệu của khách bảo hiểm phi nhân thọ C: review thiết kế có mật độ góp ý review thấp, UT có mật độ test cao, nhưng mật độ bug UT lại rất thấp. Anh/chị đọc tổ hợp này thế nào?**
Từng chỉ số riêng lẻ có thể giải thích được, nhưng tổ hợp này đáng ngờ. Review ít góp ý review có thể do review lỏng; nhiều case UT nhưng ít bug có thể do case viết theo chính code (dev tự viết case khớp với cách mình hiểu) nên không tìm ra lỗi hiểu sai spec. Giả thuyết: lỗi đang ẩn và sẽ xuất hiện ở IT. Em kiểm chứng: lấy mẫu case UT xem có dựa trên Detail Design không, cho người khác viết thêm case độc lập cho vài module, review lại một mẫu thiết kế. Kết quả mẫu cho thấy giả thuyết đúng hay sai, rồi mới quyết định mở rộng.
> 📘 PMP: Data analysis trong Control Quality: phân tích tương quan nhiều chỉ số; kiểm chứng giả thuyết bằng statistical sampling.
> 💡 Nhật: Chuẩn bị sẵn giả thuyết và cách kiểm cho tổ hợp chỉ số bất thường trước khi khách hỏi là điểm cộng lớn trong họp định kỳ với khách Nhật.

**Q869. Khách ngân hàng A muốn bỏ họp phán định kết thúc IT để bắt đầu ST ngay, nói "số liệu gửi email là được". Anh/chị phản hồi thế nào?**
Em hiểu khách muốn tiết kiệm thời gian, nên đề xuất giữ mục đích nhưng gọn hình thức: họp phán định 30 phút tập trung vào các mục chưa đạt và rủi ro chuyển tiếp, tài liệu gửi trước. Lý do cần giữ: đây là thời điểm hai bên cùng chấp nhận rủi ro của các vấn đề còn lại; nếu chỉ gửi email, các điều kiện chuyển tiếp dễ bị hiểu khác nhau. Nếu khách vẫn không muốn họp, em gửi email với kết luận phán định và danh sách điều kiện chuyển tiếp, xin xác nhận bằng văn bản từ người có thẩm quyền trước ngày bắt đầu ST.
> 📘 PMP: Tailoring (PMBOK 7) và phase gate: giữ mục đích kiểm soát, điều chỉnh hình thức cho phù hợp.
> 💡 Nhật: Một số khách gọi buổi này là "họp đánh giá kết thúc giai đoạn"; nếu khách bỏ họp, vẫn nên có "kết quả đánh giá" bằng văn bản vì về sau đây là căn cứ khi có tranh chấp phạm vi.

**Q870. Khách bảo hiểm nhân thọ B có công cụ quản lý bug riêng; số bug ST trên công cụ của khách là 230, trên công cụ của vendor là 195. Khách nói vendor giấu bug. Anh/chị xử lý thế nào?**
Em đề nghị đối chiếu từng phiếu cùng khách, không tranh luận về tổng. Thường chênh lệch do: phiếu khách ghi là bug nhưng vendor phân loại đúng spec hoặc thay đổi yêu cầu; phiếu trùng; phiếu thuộc phạm vi vendor khác hoặc môi trường; thời điểm đồng bộ khác nhau. Em lập bảng đối chiếu với lý do cho từng phiếu chênh, mục nào phân loại chưa thống nhất thì đưa ra họp để quyết. Gốc rễ là hai nguồn dữ liệu: em đề xuất dùng một hệ thống chung hoặc đồng bộ định kỳ có quy tắc phân loại chung được hai bên ký.
> 📘 PMP: Manage Stakeholder Engagement và Control Quality: giải quyết xung đột bằng dữ liệu minh bạch; thống nhất định nghĩa đo.

**Q871. Dự án của khách sản xuất D có 2 vendor: vendor VN (bên anh/chị) làm hệ thống mới, vendor Nhật làm hệ thống liên kết. Hai bên dùng chuẩn chất lượng khác nhau, lỗi interface luôn tranh cãi do chuẩn của ai. Anh/chị đề xuất gì?**
Em đề xuất khách xác lập **chuẩn chung cho phần interface**: đặc tả interface có một phiên bản duy nhất do khách quản lý, tiêu chí vào/ra của IT liên hệ thống thống nhất, quy tắc phân loại bug và mức độ chung, công cụ quản lý vấn đề chung. Mỗi vendor giữ chuẩn nội bộ cho phần của mình, nhưng phần liên kết dùng chuẩn chung. Em chuẩn bị bản đề xuất có so sánh hai chuẩn hiện tại và phương án hợp nhất, trình khách qua họp định kỳ. Khách là người quyết vì là bên có hợp đồng với cả hai.
> 📘 PMP: Plan Quality Management ở cấp chương trình (program) và Manage Stakeholder Engagement: thống nhất tiêu chuẩn tại điểm giao giữa các bên.

**Q872. Hợp đồng theo công sức (T&M) với ngân hàng A, khách tự quản lý chất lượng. PM phía khách nói: "Vendor không cần làm báo cáo chất lượng, chỉ cần báo công". Anh/chị có làm phân tích chất lượng nội bộ không?**
Có. Với hợp đồng theo công sức (T&M), vendor không chịu trách nhiệm hoàn thành kết quả như hợp đồng trọn gói, nhưng vẫn có nghĩa vụ thực hiện công việc với sự cẩn trọng chuyên môn, và chất lượng là uy tín của công ty. Em vẫn thu thập chỉ số và phân tích nội bộ ở mức gọn: bug theo module, đường cong hội tụ, nguyên nhân chính. Khi thấy rủi ro, em chủ động báo khách kèm dữ liệu, vì không báo cũng có thể bị coi là thiếu trách nhiệm. Em hỏi khách muốn nhận thông tin chất lượng ở mức nào, gửi bản tóm tắt nếu khách thấy có ích, không ép khách nhận báo cáo đầy đủ.
> 📘 PMP: Stewardship và tailoring (PMBOK 7): điều chỉnh mức độ báo cáo theo hợp đồng nhưng không bỏ trách nhiệm chuyên môn.
> 💡 Nhật: Nhiều tranh chấp hợp đồng theo công sức (T&M) ở Nhật xoay quanh việc vendor "biết mà không nói"; giữ dữ liệu và bằng chứng đã cảnh báo là cách tự bảo vệ.

**Q873. Khách bảo hiểm phi nhân thọ C muốn phát hành theo 3 đợt nhỏ (mỗi đợt 2 tháng) nhưng vẫn yêu cầu đầy đủ giai đoạn và báo cáo chất lượng như waterfall. Team 15 người lo khối lượng tài liệu gấp 3. Anh/chị tailoring thế nào?**
Em giữ khung giai đoạn và các điểm phán định quan trọng, nhưng điều chỉnh khối lượng: báo cáo chất lượng mỗi đợt viết theo mẫu rút gọn (chỉ số chính, ngoài ngưỡng, kết luận), có báo cáo tổng hợp đầy đủ ở đợt cuối; ngưỡng tính theo phạm vi mỗi đợt, dữ liệu tích lũy qua các đợt để hiệu chỉnh ngưỡng; bộ regression tự động hóa dần vì mỗi đợt phải kiểm hồi quy đợt trước. Em trình khách phương án với danh sách tài liệu mỗi đợt, giải thích cách vẫn đảm bảo mục tiêu kiểm soát. Công sức thêm (nếu có) đưa vào ước lượng.
> 📘 PMP: Tailoring và development approach (PMBOK 7): kết hợp predictive với incremental, giữ mục tiêu quản lý chất lượng.
> 💡 Nhật: Khách quen waterfall thường lo tailoring là cắt bớt; bảng đối chiếu "mục đích kiểm soát → cách đáp ứng mới" giúp khách thấy không mất gì.

**Q874. PMO đề xuất dùng mật độ bug và mật độ góp ý review của từng dev làm KPI đánh giá cá nhân cuối năm tại dự án 40 người. Anh/chị góp ý thế nào?**
Em không ủng hộ dùng trực tiếp. Lý do: ① Dev sẽ ngại ghi bug, reviewer ngại ghi góp ý review, dữ liệu chất lượng bị bóp méo và dự án mất công cụ quản lý; ② Mật độ phụ thuộc độ khó module, chất lượng đầu vào, không chỉ năng lực cá nhân; ③ Khách nhìn vào dữ liệu đã bị bóp méo sẽ đánh giá sai. Em đề xuất: dữ liệu chất lượng dùng để cải tiến quy trình và phát hiện người cần hỗ trợ đào tạo; đánh giá cá nhân dựa trên nhiều yếu tố như đóng góp vào cải tiến, mức độ minh bạch trong báo cáo, kết quả review chéo, có xét bối cảnh.
> 📘 PMP: Systems thinking và Manage Team: chỉ số đo hiệu suất quy trình không nên dùng thẳng để đánh giá cá nhân vì sẽ làm thay đổi hành vi.
> 💡 Nhật: Văn hóa chất lượng Nhật nhấn mạnh "không trách người tạo bug"; khách mà biết vendor dùng bug để phạt người thường lo vendor đang giấu bug.

**Q875. Câu phỏng vấn cuối: "Nếu chỉ được chọn 3 chỉ số để báo khách Nhật về chất lượng một dự án migration ngành bảo hiểm, anh/chị chọn gì và vì sao?"**
Em chọn: ① **Đường cong hội tụ bug** kèm bug còn mở theo mức độ, vì cho thấy xu hướng và mức sẵn sàng, không chỉ một con số tại một thời điểm; ② **Kết quả so sánh cũ – mới và đối chiếu dữ liệu chuyển đổi** (khớp số bản ghi, tổng tiền, kiểm mẫu), vì với migration bảo hiểm, giá trị cốt lõi là dữ liệu hợp đồng và tiền không được sai; ③ **Tỷ lệ lọt lỗi theo giai đoạn**, vì đo được quy trình có đang bắt lỗi sớm không. Em sẽ nói thêm: mỗi chỉ số phải kèm phân tích, và mật độ test/bug vẫn được theo dõi nội bộ để phát hiện bất thường.
> 📘 PMP: Plan Quality Management: chọn metric gắn với giá trị và rủi ro chính của dự án (value-driven, tailoring).
