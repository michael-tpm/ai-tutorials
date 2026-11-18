# Chương 9 · Quản lý nguồn lực & phát triển đội ngũ (Q801–Q900)

## 9.1 Cơ cấu team offshore cho dự án Nhật

**Q801. Trong team offshore làm cho khách Nhật, vai trò PM, BrSE, Tech Lead, Dev, QA/QC và Comtor khác nhau thế nào?**
PM chịu trách nhiệm cuối về **QCD** (chất lượng–chi phí–tiến độ), nguồn lực, rủi ro; BrSE (ブリッジSE, burijji SE – kỹ sư cầu nối) làm rõ yêu cầu với khách và chuyển thành task; Tech Lead quyết giải pháp kỹ thuật, review code; Dev hiện thực theo 詳細設計書 (shousai sekkeisho – tài liệu thiết kế chi tiết); QA/QC kiểm độc lập; Comtor dịch tài liệu và họp. Em chốt ranh giới bằng RACI ngay kick-off, vì lỗi hay gặp là BrSE bị coi như "PM thứ hai".
> 💡 Nói được điểm chồng lấn PM–BrSE và cách tách sẽ ăn điểm hơn đọc định nghĩa.

**Q802. Tỉ lệ BrSE:Dev và QA:Dev bạn thường dùng là bao nhiêu, khi nào cần điều chỉnh?**
Tham khảo: BrSE:Dev khoảng 1:5–8, QA:Dev 1:3–5, Tech Lead 1 cho 5–8 dev. Em tăng BrSE khi yêu cầu còn biến động hoặc Q&A tồn nhiều (vd > 20 câu chưa đóng quá 3 ngày); tăng QA khi domain tài chính/bảo hiểm nhiều rule tính toán hoặc bug lọt sang khách vượt ngưỡng cam kết. Tỉ lệ chỉ là điểm xuất phát, số liệu thực tế của dự án mới là căn cứ.
> 💡 Luôn kèm chữ "tham khảo" và tiêu chí điều chỉnh — nêu một con số cứng dễ bị hỏi vặn.

**Q803. Bạn xây RACI nội bộ thế nào để tránh tình trạng "ai cũng tưởng người khác làm"?**
Em liệt kê 15–25 hoạt động chính (xác nhận yêu cầu, estimate, review thiết kế, release, báo cáo tuần, trả lời Q&A khách…), gán R/A/C/I, mỗi hoạt động **đúng 1 A**. Sau đó soát 3 lỗi: hàng không có A, một người ôm quá nhiều R, người chỉ toàn I nhưng vẫn bị mời họp. RACI để trên wiki, xem lại mỗi khi đổi người hoặc đổi phase.

**Q804. Span of control của PM nên là bao nhiêu người, và khi team vượt ngưỡng thì tổ chức lại thế nào?**
Quản lý trực tiếp hiệu quả khoảng 6–8 người (tham khảo). Team 20–30 người thì em chia sub-team theo module hoặc theo luồng dev–test, mỗi sub-team có leader điều hành hằng ngày; em 1-on-1 trực tiếp với leader và key member. Dấu hiệu phải chia: PM không còn thời gian 1-on-1 hằng tháng, quyết định nhỏ dồn hết về PM, daily kéo dài quá 15 phút.

**Q805. Khi quản lý 2–3 dự án song song, bạn phân bổ thời gian và sự chú ý thế nào?**
Em phân bổ theo rủi ro, không chia đều: dự án đỏ hoặc đang ở mốc quan trọng nhận 50–60% thời gian; dự án ổn định giao leader vận hành, em giữ điểm chạm cố định (họp định kỳ tuần, duyệt báo cáo, gate release). Một dashboard chung (tiến độ, bug, effort, top 3 rủi ro) giúp em quét cả 3 dự án trong 15 phút mỗi sáng.
> 💡 Bẫy: trả lời "chia đều thời gian" — Senior PM phải phân bổ theo rủi ro.

**Q806. Có nên để một member làm đồng thời cho 2 dự án không?**
Hạn chế; nếu bắt buộc (QA, BrSE, chuyên gia hạ tầng) thì tối đa 2 dự án và chia theo ngày cố định (vd thứ 2–4 cho dự án A) thay vì theo giờ, vì context switching ăn mất năng suất. Em ghi rõ % allocation trong kế hoạch nguồn lực, thống nhất trước ai được ưu tiên khi hai deadline đụng nhau, và theo dõi effort thực tế hằng tuần để phát hiện người bị kéo quá 100%.

**Q807. Comtor và BrSE khác nhau thế nào, khi nào dự án chỉ cần Comtor?**
Comtor chủ yếu chuyển ngữ; BrSE hiểu cả kỹ thuật lẫn nghiệp vụ nên phân tích, đề xuất và chịu trách nhiệm độ đúng của yêu cầu. Dự án maintain nhỏ, yêu cầu rõ, Tech Lead vững và khách chấp nhận trao đổi văn bản thì Comtor + Tech Lead có thể đủ. Dự án có 要件定義 (youken teigi – định nghĩa yêu cầu) hoặc domain phức tạp thì cần BrSE, vì Comtor dễ dịch đúng chữ nhưng sai ý nghiệp vụ.

**Q808. Bạn phân biệt vai trò QA và QC trong team dự án Nhật thế nào?**
QC kiểm sản phẩm: viết test case, chạy test, log bug. QA kiểm quy trình: review, checklist, metric chất lượng có được làm đúng và đủ không, phân tích xu hướng bug để cải tiến. Khách Nhật thường muốn báo cáo chất lượng có số (mật độ bug, tỉ lệ review), nên em giao người giữ vai QA theo dõi metric và đề xuất 改善 (kaizen – cải tiến liên tục), không chỉ đếm bug.

**Q809. Tech Lead và PM nên phân quyền quyết định thế nào để không giẫm chân nhau?**
Nguyên tắc: Tech Lead quyết "làm thế nào" (kiến trúc, công nghệ, chuẩn code, chia task kỹ thuật); PM quyết "làm gì, khi nào, tốn bao nhiêu" (phạm vi, ưu tiên, nguồn lực, cam kết với khách). Quyết định kỹ thuật làm đổi chi phí/tiến độ vượt ngưỡng (vd > 2 ngày công hoặc chạm mốc) thì Tech Lead đề xuất, PM duyệt. Em viết thành ma trận quyền ngay từ đầu dự án.

**Q810. Dự án mới khởi động, bạn dựng team đủ người ngay hay ramp-up dần?**
Ramp-up theo phase: giai đoạn yêu cầu/thiết kế chỉ cần BrSE, Tech Lead và 1–2 dev chủ chốt; thiết kế ổn định mới thêm dev; QA vào trước giai đoạn test 2–3 tuần để viết test viewpoint. Đổ người sớm khi yêu cầu chưa rõ chỉ sinh chi phí ngồi chờ và làm lại. Em lập resource histogram theo tuần và chốt với phòng ban liên quan trước 4–6 tuần (tham khảo) cho mỗi đợt tăng người.

**Q811. Team thiếu Tech Lead đủ mạnh trong khi chờ tuyển, bạn xử lý thế nào?**
① Xác định khoảng trống cụ thể: kiến trúc, review code hay hỗ trợ dev. ② Lấp tạm: mượn senior dự án khác 20–30% thời gian để review thiết kế và code lõi. ③ Giảm rủi ro: checklist review, pair programming cho phần quan trọng. ④ Chọn một senior dev trong team làm Tech Lead kế cận với lộ trình 3–6 tháng. Em không tự ôm vai Tech Lead nếu điều đó làm bỏ bê việc PM.

## 9.2 Team building & gắn kết

**Q812. Mô hình Tuckman gồm những giai đoạn nào, PM làm gì ở mỗi giai đoạn?**
**Forming** – làm rõ mục tiêu, vai trò, luật chơi; **Storming** – chủ động đưa va chạm lên bàn, phân xử theo nguyên tắc; **Norming** – chốt working agreement, giao dần quyền; **Performing** – PM lùi lại, gỡ cản trở và phát triển người; **Adjourning** – tổng kết, ghi nhận, bàn giao tri thức. Phong cách lãnh đạo đi dần từ chỉ dẫn sang ủy quyền.
> 💡 Nói thêm: thay người hoặc đổi phase lớn có thể kéo team quay lại Storming — PM phải nhận ra sớm.

**Q813. Ngày đầu tiên của một team dự án mới, bạn làm những gì?**
Chuẩn bị trước: máy, tài khoản, quyền repo, tài liệu. Trong ngày: kick-off nội bộ 60–90 phút gồm bối cảnh khách và giá trị nghiệp vụ, mục tiêu QCD, vai trò–RACI, lịch họp, kênh liên lạc, quy định bảo mật; mỗi người chia sẻ thế mạnh và điều muốn học. Cuối ngày ai cũng có một việc nhỏ hoàn thành được để có cảm giác "đã bắt đầu".

**Q814. Bạn xây working agreement (luật chơi của team) như thế nào?**
Team tự đề xuất trong buổi 60 phút, PM chỉ gợi khung: giờ core, thời gian phản hồi chat (vd ≤ 2 giờ trong giờ làm), quy tắc commit/review, cách báo trễ ("báo ngay khi thấy có thể trễ, không đợi đến hạn"), quy tắc họp. Chốt dưới 10 điều, dán lên wiki, xem lại ở mỗi retro. Luật do team tự đặt thì tự giữ tốt hơn luật PM áp xuống.

**Q815. Những nghi thức (ritual) nào bạn duy trì để gắn kết team?**
Chỉ giữ nghi thức có mục đích: daily ≤ 15 phút; demo cuối sprint để team thấy sản phẩm chạy; 振り返り (furikaeri – nhìn lại, retro) luôn ra hành động cải tiến; ăn mừng milestone (release đầu, nghiệm thu, khách khen). Khi ăn mừng em nêu tên đóng góp cụ thể chứ không chỉ liên hoan. Ngân sách team building xin từ đầu dự án và gắn với các mốc.

**Q816. Psychological safety là gì và bạn tạo nó trong team thế nào?**
Là cảm giác an toàn khi nói "em không biết", báo lỗi, phản biện mà không bị phạt hay chê cười. Em làm bằng hành động: tự nhận lỗi của mình trước team, cảm ơn người báo bug/báo trễ sớm, retro blameless tập trung vào quy trình, hỏi ý junior trước senior. Chỉ báo kiểm tra: rủi ro và trễ hạn được báo sớm hơn, member dám đặt câu hỏi trong họp.
> 💡 Liên hệ 報連相 (hou-ren-sou – báo cáo, liên lạc, thảo luận): thiếu an toàn tâm lý thì team giấu tin xấu đến phút chót.

**Q817. Team chia ở Hà Nội, Đà Nẵng và một người onsite Nhật — làm sao để không thành "ba team"?**
① Một nguồn thông tin: backlog, wiki, chat chung, quyết định được ghi lại, không chốt việc ở bàn nước. ② Họp chung bật camera, luân phiên người chủ trì, không để site đông người áp đảo. ③ Ghép cặp xuyên site (review chéo, pair) thay vì chia module theo địa điểm. ④ Onsite có slot cố định chia sẻ "tiếng nói khách". ⑤ Gặp mặt trực tiếp ở mốc lớn nếu có ngân sách.
> 💡 Bẫy hay gặp: chia module theo site — nhanh chóng thành "chúng tôi vs họ".

**Q818. Làm sao để người onsite ở Nhật không bị cô lập với team offshore?**
Người onsite chịu áp lực khách trực tiếp và lệch múi giờ 2 tiếng, nên em: 1-on-1 riêng 2 tuần/lần, mời vào daily vài buổi mỗi tuần, ghi nhận đóng góp của onsite công khai trong demo, và lên kế hoạch luân chuyển (vd 6–12 tháng, tham khảo) để không ai bị "kẹt" ở onsite. Ngược lại, onsite phải đưa feedback của khách về team đầy đủ, không lọc bớt.

**Q819. Team làm hybrid (vài ngày remote), bạn giữ gắn kết thế nào?**
Em thống nhất ngày lên văn phòng chung cho cả team (vd 2 ngày/tuần) để dồn việc cần tương tác: thiết kế, review khó, retro. Ngày remote dùng giờ core và quy tắc phản hồi rõ. Thêm điểm chạm nhẹ: kênh chat không bàn việc, cà phê online 15 phút. Đo bằng hành vi: người remote có được giao việc thú vị và lên tiếng trong họp như người ở văn phòng không.

**Q820. Team mới ghép từ nhiều dự án, mỗi người quen một cách làm. Bạn thống nhất thế nào?**
Em không áp cách của riêng mình: liệt kê các điểm cần chuẩn chung (coding convention theo yêu cầu khách, Git flow, Definition of Done, mẫu báo cáo), mời người giỏi nhất từng mảng đề xuất, team chốt và chạy thử 2 sprint rồi điều chỉnh ở retro. Điều khách đã quy định thì không bàn lại. Thói quen cũ tốt được đưa vào chuẩn mới để người đó thấy được tôn trọng.

**Q821. Dự án kết thúc, team giải tán — bạn làm gì để giữ gắn kết và bài học?**
Adjourning hay bị bỏ qua. Em làm: buổi tổng kết có số liệu QCD và bài học để 横展開 (yokotenkai – nhân rộng sang dự án khác); thư cảm ơn nêu đóng góp cụ thể từng người, gửi cả quản lý trực tiếp của họ; cập nhật đánh giá dự án vào hồ sơ performance; giới thiệu member sang dự án hợp nguyện vọng. Người rời dự án với cảm giác được ghi nhận sẽ muốn làm cùng mình lần sau.

## 9.3 Tạo động lực & truyền lửa

**Q822. Động lực của kỹ sư IT đến từ đâu, và tiền đóng vai trò gì?**
Em dùng 2 khung: Herzberg — lương, điều kiện làm việc là yếu tố "duy trì": thiếu thì bất mãn, đủ chưa chắc hăng hái; Daniel Pink — động lực nội tại đến từ **autonomy** (tự chủ), **mastery** (giỏi lên), **purpose** (ý nghĩa). Nên em đảm bảo phần tiền công bằng, minh bạch, rồi tạo lửa bằng việc có thách thức, quyền quyết định và hiểu sản phẩm phục vụ ai.
> 💡 Bẫy: nói "tiền không quan trọng" — kỹ sư sẽ không tin; hãy nói tiền là nền, không phải động cơ.

**Q823. Bạn trao autonomy cho member thế nào mà vẫn kiểm soát được rủi ro?**
Em giao "kết quả + ràng buộc", không giao từng bước: vd "module tính phí, xong trước ngày X, pass test viewpoint của QA, effort ≤ Y ngày công", người nhận tự chọn cách làm. Kiểm soát qua điểm chạm nhỏ (review thiết kế đầu, demo giữa chừng) và ngưỡng báo cáo (lệch > 1 ngày phải báo). Mức tự chủ tăng dần theo năng lực đã chứng minh.

**Q824. Bạn ghi nhận (recognition) thành viên thế nào cho hiệu quả?**
Ghi nhận phải **kịp thời, cụ thể, công khai đúng mức**: nói rõ hành vi và tác động ("A phát hiện lỗi làm tròn phí trước UAT, tránh một vòng sửa với khách"), trong vài ngày, trước team hoặc trong báo cáo gửi cấp trên. Lời cảm ơn của khách em chuyển đúng người. Với người hướng nội, em khen riêng và ghi vào hồ sơ review; em cũng ghi nhận cả việc "vô hình" như review kỹ, giúp đồng đội.

**Q825. Dự án maintain nhiều năm, việc lặp lại, team chán. Bạn làm gì?**
① Tạo mastery ngay trong maintain: mục tiêu cải tiến đo được (giảm 20% thời gian xử lý ticket, tự động hóa test hồi quy). ② Xoay vai: dev thử estimate, trả lời Q&A, phỏng vấn ứng viên. ③ Dành 10–15% thời gian (tham khảo) cho refactor hoặc đề xuất 改善 cho khách — khách Nhật thường trân trọng đề xuất chủ động. ④ Cho người muốn đổi môi trường luân chuyển có kế hoạch, thay vì để họ nghỉ.
> 💡 Biến đề xuất cải tiến thành change request có doanh thu — ghi điểm cả với team lẫn công ty.

**Q826. Dự án đỏ kéo dài 3 tháng, team mệt và mất tinh thần. Bạn giữ lửa thế nào?**
Không hô hào, mà: ① nói thật tình hình và kế hoạch phục hồi với các mốc nhỏ thắng được trong 1–2 tuần; ② bảo vệ team: đàm phán giảm phạm vi/lùi mốc, xin thêm người, chặn yêu cầu mới; ③ ăn mừng từng mốc nhỏ; ④ theo dõi OT, cho nghỉ bù luân phiên; ⑤ có mặt cùng team lúc khó nhất. Người ta chịu được khó khi thấy đích và thấy PM đứng về phía mình.

**Q827. Có nên tổ chức team building khi dự án đang đỏ, deadline gấp?**
Không làm buổi lớn tốn nửa ngày giữa nước rút; nhưng giữ hoạt động nhỏ, ít tốn thời gian: bữa trưa chung, ăn tối khi OT, khen công khai sau mỗi mốc. Hoạt động lớn để sau milestone, như một buổi "ăn mừng phục hồi". Quan trọng hơn team building là giảm tải thật: bỏ họp không cần thiết, chặn việc ngoài phạm vi.
> 💡 Câu trade-off — trả lời "tùy" kèm tiêu chí rõ ràng được đánh giá cao hơn "có" hay "không".

**Q828. Làm outsource, member không gặp người dùng cuối — làm sao để họ thấy "purpose"?**
Em kể câu chuyện nghiệp vụ: hệ thống của khách bảo hiểm B phục vụ ai, một lỗi tính phí ảnh hưởng người dùng thế nào; mời BrSE hoặc khách chia sẻ 15 phút ở kick-off về bối cảnh kinh doanh; chuyển feedback của người dùng cuối về team. Purpose còn là sự phát triển của chính họ: dự án này giúp họ đạt kỹ năng, chứng chỉ gì (Cloud/AWS, tiếng Nhật).

**Q829. Động lực của member trẻ (Gen Z) khác thế hệ trước thế nào, bạn điều chỉnh gì?**
Em tránh khái quát theo thế hệ, nhưng thực tế nhóm trẻ thường cần: feedback thường xuyên (không đợi 6 tháng), lộ trình nhìn thấy được, linh hoạt giờ giấc, được giải thích "vì sao". Em điều chỉnh: 1-on-1 dày hơn, mục tiêu ngắn 1–3 tháng, giải thích lý do của quy trình Nhật (vì sao checklist, vì sao review kỹ) thay vì bắt tuân thủ. Chuẩn chất lượng thì không hạ.
> 💡 Bẫy: nói "Gen Z lười, thiếu cam kết" — lập tức mất điểm leadership.

**Q830. Một member giỏi nói "em làm đủ việc, không muốn nhận thêm trách nhiệm". Bạn xử lý thế nào?**
Đó là lựa chọn hợp lệ nếu họ hoàn thành tốt việc hiện tại. Em hỏi để hiểu (giai đoạn cuộc sống, sợ thất bại, hay thấy thăng tiến không đáng), tôn trọng quyết định, giao việc chuyên sâu kỹ thuật thay cho trách nhiệm quản lý nếu họ thích, và nói rõ cánh cửa vẫn mở. Không ép lên leader, vì người không muốn quản lý thường quản lý kém.

**Q831. Bạn đo tinh thần team bằng gì thay vì cảm tính?**
Kết hợp khảo sát và chỉ báo hành vi: ① pulse survey ẩn danh 3–5 câu mỗi tháng (thang 1–5, xem xu hướng chứ không xem số tuyệt đối); ② số đề xuất cải tiến ở retro; ③ OT, nghỉ đột xuất, trễ hạn bị báo muộn; ④ tín hiệu trong 1-on-1. Điểm giảm 2 kỳ liên tiếp hoặc một nhóm tụt mạnh là trigger để em đào sâu, không đợi có người nộp đơn nghỉ.

## 9.4 Mentoring & coaching

**Q832. Bạn tổ chức 1-on-1 thế nào: tần suất, thời lượng, nội dung?**
Tham khảo: 30 phút, 2 tuần/lần với direct report và key member; 1 tháng/lần với người báo cáo qua leader. Đó là buổi **của member**: họ đặt chủ đề, em hỏi nhiều hơn nói. Nội dung xoay quanh 3 phần: đang vướng gì, cảm nhận/động lực, phát triển dài hạn. Kết thúc có 1–2 action, ghi ngắn và kiểm lại lần sau.
> 💡 Bẫy: dùng 1-on-1 để hỏi tiến độ — tiến độ đã có daily và tool.

**Q833. Những câu hỏi nào bạn hay dùng trong 1-on-1?**
Câu mở em hay dùng: "Tuần này việc gì làm em tốn năng lượng nhất?", "Có việc gì em muốn làm mà chưa được giao?", "Nếu em là PM, em sẽ đổi điều gì trong dự án?", "6 tháng nữa em muốn giỏi thêm điều gì?". Câu cuối luôn là xin feedback cho chính em: "Anh/chị nên làm khác điều gì?". Tránh câu đóng kiểu "ổn không em?" vì đáp án luôn là "ổn ạ".

**Q834. IDP (kế hoạch phát triển cá nhân) bạn xây với member gồm những gì?**
① Mục tiêu nghề nghiệp 1–2 năm (vd lên Tech Lead, thành BrSE); ② khoảng cách kỹ năng so với mục tiêu; ③ 2–3 mục tiêu 6 tháng đo được, khớp chu kỳ review 2 lần/năm; ④ cách đạt theo tỉ lệ 70-20-10 (việc thực tế – học từ người khác – khóa học); ⑤ hỗ trợ cần có (dự án, mentor, chi phí thi). Em gắn IDP vào phân công thật, vd người muốn làm BrSE được trả lời Q&A khách có BrSE chính kèm.
> 💡 Nối IDP với chính sách sẵn có của công ty (đào tạo tiếng Nhật, hỗ trợ thi Cloud/AWS/PMP) cho thấy bạn đã đọc kỹ JD.

**Q835. Mô hình coaching GROW là gì? Cho ví dụ áp dụng.**
GROW = **Goal** (muốn đạt gì) → **Reality** (hiện tại ra sao) → **Options** (có những cách nào) → **Will** (sẽ làm gì, khi nào). Ví dụ junior hay trễ task: G – ước lượng sát thực tế hơn; R – thường lệch 50% vì không chia nhỏ việc; O – chia task ≤ 1 ngày, hỏi senior trước khi estimate, ghi thực tế để so; W – áp dụng 2 sprint, xem lại ở 1-on-1. Coach đặt câu hỏi để member tự tìm ra, không đưa đáp án.

**Q836. Khi nào bạn mentoring (chỉ dẫn), khi nào coaching (đặt câu hỏi)?**
Tùy năng lực và mức rủi ro: người chưa có kiến thức về vấn đề → mentoring, chỉ cách làm và lý do; người đã có nền tảng → coaching để họ tự tư duy. Khi rủi ro cao, gấp (sự cố production) em chỉ dẫn trực tiếp, xong việc mới dùng buổi nhìn lại để coaching. Coaching người hoàn toàn chưa biết chỉ làm họ bối rối và tốn thời gian.

**Q837. Bạn đào tạo một dev thành BrSE kế cận thế nào?**
Lộ trình tham khảo 6–12 tháng: ① tiếng Nhật đủ đọc tài liệu (mục tiêu N2) và thuật ngữ nghiệp vụ; ② shadow BrSE chính: dự họp, đọc Q&A, viết biên bản; ③ tự xử lý Q&A nhỏ, BrSE chính duyệt trước khi gửi; ④ phụ trách trọn một module với khách. Song song rèn thói quen 確認 (kakunin – xác nhận lại hiểu biết) và viết email nghiệp vụ. Đo bằng số Q&A hiểu sai và phản hồi của khách.

**Q838. Bạn đào tạo một sub-leader trong team như thế nào?**
Em chọn người được đồng nghiệp tin và chủ động báo cáo, rồi giao quyền theo bậc: chủ trì daily → estimate một module → review code của junior → dẫn một sub-team 3–4 người với quyền phân task thật. 3 tháng đầu em làm "lưới an toàn": 1-on-1 hằng tuần, cùng xem quyết định khó, sai thì gỡ cùng chứ không lấy lại quyền. Trao quyền chứ không chỉ trao việc.

**Q839. Bạn phát triển kỹ năng tiếng Nhật cho team dự án thế nào?**
Gắn tiếng Nhật với việc thật: ① glossary nghiệp vụ Nhật–Việt dùng chung; ② đọc 設計書 (sekkeisho – tài liệu thiết kế) bản gốc, Comtor hỗ trợ khi vướng; ③ luân phiên viết daily report tiếng Nhật, Comtor sửa; ④ đặt mục tiêu JLPT trong IDP và tận dụng chương trình đào tạo tiếng Nhật của công ty. Dev đọc được tài liệu gốc thì giảm rõ lỗi hiểu sai do dịch qua nhiều tầng.

**Q840. Member có thói quen 指示待ち (shiji machi – chờ chỉ thị). Bạn giúp họ chủ động thế nào?**
Thường do môi trường cũ: từng bị phạt khi tự quyết, hoặc không được biết "vì sao". Em: ① luôn giải thích mục đích của việc; ② giao ownership một phần trọn vẹn; ③ yêu cầu "mang vấn đề thì mang kèm đề xuất" — 2 phương án và chọn 1; ④ khen hành vi chủ động kể cả khi kết quả chưa hoàn hảo; ⑤ nói rõ được tự quyết đến đâu. Sau 1–2 tháng đo bằng số đề xuất tự đưa ra.
> 💡 Đừng đổ hết cho tính cách — chỉ ra môi trường đã tạo ra 指示待ち và PM sửa môi trường.

**Q841. Bạn đánh giá hiệu quả mentoring thế nào?**
Đo bằng thay đổi hành vi và kết quả, không bằng số buổi: mentee đạt mục tiêu IDP đúng hạn không; mức cần hỗ trợ giảm dần (số lần hỏi lại cùng một loại vấn đề); output cải thiện (bug, comment review); mentee bắt đầu kèm người khác. Em xin thêm feedback ẩn danh về mentor, và đưa kết quả mentoring vào tiêu chí đánh giá của senior/leader để việc kèm người được ghi nhận.

**Q842. Senior giỏi nhưng không muốn chia sẻ kiến thức vì sợ mất vị thế. Bạn làm gì?**
Em hiểu nỗi sợ đó và đổi hệ thống khuyến khích: ① đưa chia sẻ kiến thức vào tiêu chí đánh giá và điều kiện lên Tech Lead/Expert; ② ghi nhận công khai khi họ làm tech talk, viết tài liệu; ③ cho thấy team mạnh lên thì họ được giao việc khó, giá trị hơn. Song song giảm 属人化 (zokujinka – phụ thuộc vào một người) bằng review chéo và pair bắt buộc cho phần lõi.

## 9.5 Đánh giá hiệu suất (review 2 lần/năm)

**Q843. Với review performance 2 lần/năm, bạn chuẩn bị đánh giá member thế nào?**
Không dồn cuối kỳ: em ghi nhật ký hiệu suất ngắn mỗi tháng cho từng người (sự việc, số liệu, feedback khách), thống nhất mục tiêu đầu kỳ, check-in giữa kỳ. Trước buổi review: member tự đánh giá, em thu số liệu khách quan và feedback 360°, so với mục tiêu rồi mới chấm. Buổi review là trao đổi hai chiều, kết thúc bằng mục tiêu kỳ sau; nguyên tắc "không có bất ngờ" — vấn đề phải được nói trong 1-on-1 trước đó.

**Q844. KPI bạn đặt cho dev, QA và BrSE trong dự án Nhật là gì?**
Tham khảo: **Dev** — tỉ lệ task đúng hạn, mật độ bug do QA/khách phát hiện trên khối lượng, chất lượng review; **QA** — tỉ lệ bug lọt sang UAT/khách, độ phủ test viewpoint, tỉ lệ bug hợp lệ; **BrSE** — số Q&A hiểu sai yêu cầu, thời gian phản hồi khách, chất lượng tài liệu. Mỗi vai 3–5 KPI, cộng phần định tính (thái độ, teamwork, kèm người) khoảng 30–40%.
> 💡 Bẫy: KPI số dòng code hay số bug tìm được — dễ bị lách và phá teamwork.

**Q845. Bạn dùng OKR hay KPI cho team, và hai thứ khác nhau thế nào?**
KPI đo hiệu suất vận hành ổn định (đúng hạn, chất lượng), dùng để đánh giá; OKR đặt mục tiêu tham vọng để thay đổi, đạt 60–70% vẫn là tốt, không nên gắn thẳng vào lương thưởng. Em dùng KPI cho phần đánh giá chính và 1–2 OKR cho phát triển, vd "O: team tự giao tiếp được với khách; KR: 3 dev viết daily report tiếng Nhật, 50% Q&A trả lời không cần dịch".

**Q846. Làm sao đánh giá công bằng khi mỗi người làm module có độ khó khác nhau?**
Em chuẩn hóa theo độ khó: so thực tế với estimate team đã thống nhất (không so số task), cân nhắc độ phức tạp và rủi ro, nhìn xu hướng cả kỳ thay vì một sự việc. Ghi rõ bối cảnh: người nhận module legacy không tài liệu không thể đánh giá như người làm màn hình CRUD. Kết quả được calibrate với các PM/leader khác để cùng một thang.

**Q847. Làm feedback 360° thế nào để có ích chứ không thành chấm điểm cảm tính?**
Chọn 3–5 người làm việc trực tiếp (leader, đồng nghiệp, QA, BrSE, có thể cả onsite); hỏi bằng câu hỏi hành vi ("người này báo rủi ro sớm thế nào? cho ví dụ") thay vì thang điểm chung; đảm bảo ẩn danh; chỉ dùng xu hướng lặp lại từ nhiều người. Feedback của khách Nhật thì quy về sự việc cụ thể, tránh hiểu sai sắc thái của lời nói gián tiếp.

**Q848. Những bias phổ biến khi đánh giá là gì, bạn tránh bằng cách nào?**
Hay gặp: **recency** (chỉ nhớ 1–2 tháng gần nhất), **halo/horn** (một điểm tốt/xấu lan sang mọi tiêu chí), **leniency/central tendency** (ai cũng tốt hoặc trung bình cho an toàn), **similar-to-me** (ưu ái người giống mình). Cách tránh tương ứng: nhật ký hiệu suất hằng tháng, chấm từng tiêu chí riêng có bằng chứng, calibration giữa các PM, và tự hỏi "nếu người khác làm việc này mình chấm thế nào".
> 💡 Kể tên bias kèm biện pháp tương ứng — cấu trúc gọn và thuyết phục.

**Q849. Buổi calibration giữa các PM/leader là gì, vì sao quan trọng?**
Là buổi những người đánh giá đặt kết quả cạnh nhau để thống nhất thang, tránh "PM dễ" và "PM khó" gây bất công giữa các team. Mỗi người trình bằng chứng cho mức cao nhất và thấp nhất, xem phân bố có lệch không. Em mang số liệu và ví dụ hành vi; sẵn sàng điều chỉnh khi bằng chứng của mình yếu, nhưng bảo vệ member khi có dữ liệu.

**Q850. Mô hình SBI là gì? Cho ví dụ một feedback khó.**
SBI = **Situation** – **Behavior** – **Impact**. Ví dụ: "Trong buổi họp với khách thứ Ba (S), em trả lời ngay 'được' khi khách hỏi thêm chức năng mà chưa kiểm effort (B); khách hiểu là đã cam kết, team phải làm thêm 3 ngày ngoài kế hoạch (I)." Sau đó em hỏi "em thấy thế nào?" và cùng chốt cách làm lần sau. Nói về hành vi quan sát được, không nhận xét tính cách ("em ẩu").

**Q851. Bạn gắn kết quả đánh giá với thưởng dự án thế nào cho minh bạch?**
Nguyên tắc công bố từ đầu dự án: thưởng phụ thuộc kết quả chung (đúng hạn, chất lượng, lợi nhuận) và mức đóng góp cá nhân theo tiêu chí biết trước. Em đề xuất phân bổ kèm bằng chứng (vai trò, độ khó, kết quả, phản hồi khách) trong khung chính sách công ty — không chia đều cho yên ổn, không thưởng theo cảm tình. Member hiểu vì sao mình nhận mức đó dù không biết mức của người khác.

**Q852. Member tự đánh giá xuất sắc, bạn đánh giá chỉ đạt. Bạn dẫn buổi review thế nào?**
① Nghe trước: hỏi căn cứ của họ, ghi nhận phần đúng. ② Đưa bằng chứng theo từng tiêu chí: mục tiêu đầu kỳ, số liệu, sự việc. ③ Phân biệt "làm nhiều" với "đạt mục tiêu". ④ Nếu họ có dữ kiện em bỏ sót, em điều chỉnh. ⑤ Chốt cụ thể cần đạt gì để được xuất sắc kỳ sau. Khoảng cách lớn thường do mục tiêu đầu kỳ không rõ — đó cũng là bài học của em.
> 💡 Nhận phần trách nhiệm của PM (mục tiêu chưa rõ, feedback chưa đủ sớm) thể hiện sự trưởng thành.

**Q853. Member xin tăng lương giữa kỳ, trước kỳ review vài tháng. Bạn trả lời thế nào?**
Không hứa, không từ chối ngay: lắng nghe lý do (mặt bằng thị trường, có offer ngoài, đang gánh trách nhiệm lớn hơn), giải thích chu kỳ review 2 lần/năm của công ty. Nếu có cơ sở, em chuẩn bị bằng chứng để đề xuất ở kỳ gần nhất hoặc trao đổi với HR về ngoại lệ. Em hẹn mốc trả lời cụ thể và giữ đúng hẹn; nếu có offer ngoài thì chuyển sang câu chuyện retention.

## 9.6 Low performer & kỷ luật

**Q854. Member làm kém — bạn chẩn đoán nguyên nhân thế nào trước khi xử lý?**
Em phân 3 nhóm: ① **năng lực** (thiếu kỹ năng, giao sai việc, chưa hiểu domain); ② **động lực** (chán, mâu thuẫn, không thấy tương lai); ③ **hoàn cảnh** (sức khỏe, gia đình, quá tải). Thu fact từ số liệu, leader và 1-on-1 hỏi mở; đồng thời soát lỗi hệ thống: kỳ vọng có rõ không, onboarding có đủ không. Mỗi nguyên nhân một cách xử lý: đào tạo, đổi việc, hỗ trợ hay kỷ luật.
> 💡 Câu đầu tiên PM nên tự hỏi là "mình đã giao việc và kỳ vọng rõ chưa" — interviewer đánh giá cao người nhìn hệ thống trước.

**Q855. PIP (performance improvement plan) bạn xây như thế nào?**
PIP gồm: vấn đề cụ thể có bằng chứng; 2–4 mục tiêu đo được (vd task đúng hạn ≥ 85%, bug lọt ≤ mức trung bình team); thời hạn 1–3 tháng (tham khảo); hỗ trợ cụ thể (mentor, đào tạo, giảm tải); check-in hằng tuần; hệ quả nếu không đạt. Làm cùng HR theo quy chế công ty, member ký xác nhận đã hiểu. Mục tiêu thật của PIP là giúp người đó đạt, không phải thủ tục để cho nghỉ.

**Q856. Khi nào bạn chọn chuyển vai trò cho member thay vì tiếp tục PIP?**
Khi thái độ tốt nhưng không hợp vai hiện tại: dev tư duy logic, cẩn thận nhưng code chậm có thể hợp QA automation; người giao tiếp tốt, tiếng Nhật khá nhưng code yếu có thể theo hướng Comtor/BrSE. Em trao đổi thẳng, để họ chọn, có giai đoạn thử 1–2 tháng với tiêu chí đánh giá mới. Chuyển vai không phải "đẩy đi" mà là đặt đúng người đúng chỗ.

**Q857. Khi nào phải cho member rời dự án hoặc rời công ty, và PM làm gì?**
Khi đã chẩn đoán và hỗ trợ đủ (PIP có hỗ trợ thật) mà không cải thiện, hoặc vi phạm nghiêm trọng (bảo mật, gian lận). Rút khỏi dự án thì PM phối hợp phòng ban quyết; cho nghỉ việc thì PM không tự quyết, mà cung cấp hồ sơ bằng chứng cho HR/cấp trên xử lý theo quy chế công ty và Bộ luật Lao động. Em giữ thái độ tôn trọng, bàn giao đầy đủ, và rút kinh nghiệm khâu tuyển/onboard.
> 💡 Bẫy: nói "em cho nghỉ ngay" — lộ ra chưa hiểu quy trình HR và pháp lý.

**Q858. Xử lý "toxic high performer" — làm rất giỏi nhưng thái độ gây hại cho team — thế nào?**
Em coi hành vi gây hại là vấn đề hiệu suất ngang chất lượng code: ① feedback riêng bằng SBI với ví dụ cụ thể (chê junior trước đám đông, từ chối review); ② đặt kỳ vọng hành vi rõ ràng, đưa vào tiêu chí đánh giá; ③ giảm phụ thuộc bằng chia sẻ kiến thức; ④ không thay đổi sau thời hạn thì chấp nhận rời họ dù ảnh hưởng ngắn hạn. Cái giá của một người toxic là cả team chậm lại và người giỏi khác bỏ đi.
> 💡 Câu senior: cho thấy bạn dám đánh đổi năng suất ngắn hạn để giữ văn hóa team.

**Q859. Khách Nhật rất quý một member giỏi, nhưng người này đang gây căng thẳng trong team. Bạn cân bằng thế nào?**
Tách bạch hai việc: giá trị với khách là thật, hành vi trong team là vấn đề phải sửa. Em giữ người đó ở vai giao tiếp khách (điểm mạnh) nhưng đặt kỳ vọng hành vi rõ, đồng thời đào tạo người thứ hai đủ năng lực để khách không phụ thuộc một người. Chuyện nội bộ không đưa ra với khách; nếu cuối cùng phải thay người, em lên kế hoạch bàn giao và thông báo khách sớm.

**Q860. Member đẩy source code của khách lên repo cá nhân public. Bạn xử lý thế nào?**
① Khoanh vùng ngay: gỡ repo, thu hồi quyền, đổi secret, kiểm tra phạm vi lộ. ② Báo cấp trên và bộ phận bảo mật theo quy trình sự cố. ③ Báo khách theo hợp đồng và 報連相, nêu phạm vi ảnh hưởng và biện pháp. ④ Xử lý member theo quy chế, phân biệt cố ý hay thiếu hiểu biết. ⑤ 再発防止 (saihatsu boushi – phòng ngừa tái phát): đào tạo lại, chặn bằng kỹ thuật (secret scan, chặn push ra ngoài), 横展開 sang dự án khác.

**Q861. Member hay đi muộn, nghỉ đột xuất, ảnh hưởng tiến độ. Bạn làm gì?**
Nói chuyện riêng sớm, hỏi nguyên nhân trước (có thể là sức khỏe, gia đình) và nhắc lại quy định đã thống nhất. Có lý do chính đáng thì thử điều chỉnh giờ làm trong phạm vi chính sách; không thì ghi nhận bằng văn bản, đặt cam kết cụ thể và mốc kiểm tra 2–4 tuần. Lặp lại thì xử lý theo nội quy cùng HR. Không phê bình trước team.

**Q862. Có nên công khai điểm đánh giá hay xếp hạng từng member trước team không?**
Không công khai điểm đánh giá, thưởng cá nhân — đó là thông tin riêng và dễ gây so bì. Có thể công khai chỉ số chung của team (tiến độ, chất lượng) và ghi nhận đóng góp tích cực cụ thể. Bảng xếp hạng cá nhân theo bug hay số task khiến member chọn việc dễ, giấu lỗi và ngại giúp nhau.

**Q863. Junior làm hỏng dữ liệu môi trường test của khách do thao tác sai. Bạn xử lý với member thế nào?**
Khắc phục trước, tìm trách nhiệm sau: em cùng team khôi phục và báo khách. Với junior: buổi nhìn lại blameless hỏi "vì sao hệ thống cho phép một junior làm được việc đó" (quyền quá rộng, không review, không backup) thay vì quy kết cá nhân; junior tham gia viết 再発防止 để học. Chỉ khi cố tình làm trái quy trình đã được đào tạo mới xét trách nhiệm cá nhân.
> 💡 Đây là câu kiểm tra psychological safety — phạt nặng junior thì lần sau lỗi sẽ bị giấu.

## 9.7 Xung đột nội bộ

**Q864. Mô hình Thomas–Kilmann gồm những phong cách xử lý xung đột nào, khi nào dùng?**
Năm phong cách trên hai trục quyết đoán–hợp tác: **Competing** (áp đặt — sự cố khẩn, vi phạm bảo mật); **Collaborating** (cùng tìm win-win — vấn đề quan trọng, có thời gian); **Compromising** (mỗi bên nhượng một phần — gấp, hai bên ngang quyền); **Avoiding** (tạm né — chuyện nhỏ, cần để nguội); **Accommodating** (nhường — khi mình sai hoặc quan hệ quan trọng hơn). Không có phong cách đúng tuyệt đối, chỉ có đúng tình huống.
> 💡 Cho một ví dụ dùng Competing đúng chỗ — chứng tỏ bạn không "hòa cả làng".

**Q865. Dev và QA tranh cãi "đây là bug hay là spec". Bạn xử lý thế nào?**
① Quay về nguồn: tài liệu yêu cầu, 設計書, Q&A đã chốt với khách. ② Tài liệu không rõ → đó là lỗ hổng spec; BrSE hỏi khách, không để dev và QA tự định nghĩa. ③ Trong lúc chờ, đặt trạng thái "pending spec" thay vì cãi tiếp. ④ Chốt quy tắc bug triage có tiêu chí và người quyết cuối (BrSE/PM). Tranh cãi lặp lại là dấu hiệu khâu review yêu cầu đang yếu.

**Q866. QA bị dev coi là "người bắt lỗi", quan hệ căng thẳng. Bạn cải thiện thế nào?**
Đổi khung từ đối đầu sang cùng mục tiêu "không lọt bug sang khách": ① QA vào sớm từ review yêu cầu/thiết kế, chia sẻ test viewpoint trước khi dev code; ② bug report viết theo sự việc, không phán xét; ③ KPI chung cho dev và QA về bug lọt sang khách; ④ ghi nhận QA khi bắt được lỗi quan trọng trước UAT. Mỗi bug QA bắt được là một lần khách không phải nhìn thấy.

**Q867. Senior và junior bất đồng cách làm, junior thấy bị áp đặt. Bạn làm gì?**
Tách hai việc: quyết định kỹ thuật và cách giao tiếp. Về kỹ thuật, hai bên trình phương án theo tiêu chí chung (đúng yêu cầu, rủi ro, effort, khả năng bảo trì), Tech Lead chốt và giải thích lý do. Về giao tiếp, em feedback riêng với senior: giải thích "vì sao" thay vì ra lệnh, vì kèm junior là trách nhiệm của senior. Junior được ghi nhận nếu ý tưởng hay, dù cuối cùng không được chọn.

**Q868. Team Hà Nội và Đà Nẵng đổ lỗi cho nhau khi tích hợp lỗi. Bạn xử lý thế nào?**
① Dừng đổ lỗi bằng dữ liệu: log, commit, interface spec cho thấy lỗi nằm ở đâu. ② Nguyên nhân gốc thường là ranh giới: interface không rõ, thiếu integration test chung, không ai sở hữu việc tích hợp. ③ Lập owner tích hợp, contract API thống nhất, CI tích hợp chạy hằng ngày. ④ Về con người: retro chung hai site, ghép cặp xuyên site. Em không đứng về phía site mình đang ngồi.
> 💡 Câu này kiểm tra bạn có thiên vị nơi mình ngồi không — trả lời bằng dữ liệu và cơ chế.

**Q869. Khi nào PM nên làm trọng tài, khi nào để team tự giải quyết xung đột?**
Để team tự xử khi: xung đột về cách làm, hai bên ngang hàng, chưa ảnh hưởng tiến độ, team đã ở Norming/Performing. PM vào cuộc khi: kéo dài quá vài ngày gây tắc việc, chạm cam kết với khách, có yếu tố xúc phạm cá nhân, hoặc liên quan quyền hạn/nguồn lực ngoài tầm team. Ngay cả khi làm trọng tài, em ưu tiên giúp hai bên tự thỏa thuận rồi mới quyết thay.

**Q870. Hai member xung đột cá nhân, không còn nói chuyện với nhau. Bạn làm gì?**
① Gặp riêng từng người, nghe góc nhìn và tìm fact, không phán xét. ② Gặp chung khi cả hai sẵn sàng, đặt luật: nói về hành vi và tác động, không công kích. ③ Tìm điểm chung (cùng muốn dự án tốt), chốt cam kết cụ thể về cách phối hợp. ④ Theo dõi 2–4 tuần. Không cải thiện và ảnh hưởng team thì cân nhắc tách sang module/dự án khác — giải pháp cuối, không phải đầu tiên.

**Q871. Bạn xử lý thế nào khi chính mình bất đồng với Tech Lead về một quyết định?**
Tranh luận riêng, không trước team, dựa trên dữ kiện và ma trận quyền đã thống nhất. Nếu là quyết định kỹ thuật thuộc quyền Tech Lead và rủi ro chấp nhận được, em tôn trọng và ủng hộ công khai ("disagree and commit"). Nếu chạm cam kết QCD với khách, em đưa trade-off rõ ràng lên cấp trên hoặc một chuyên gia trung lập. Trước team phải là một tiếng nói thống nhất.
> 💡 "Disagree and commit" là tinh thần interviewer muốn nghe ở vị trí senior.

**Q872. Xung đột nội bộ có mặt tích cực không? Làm sao khuyến khích "xung đột tốt"?**
Có — tranh luận về ý tưởng giúp lộ rủi ro sớm, tránh groupthink, nhất là khi cả văn hóa Việt lẫn Nhật đều ngại phản đối trực diện. Em khuyến khích: ở review thiết kế chỉ định một người đóng vai phản biện, hỏi "điều gì có thể làm phương án này thất bại?", khen người dám nêu điểm yếu. Ranh giới rõ: tranh luận về vấn đề, không về con người.

## 9.8 OT, burnout & sức khỏe team

**Q873. Bạn quản lý OT trong dự án thế nào?**
OT là công cụ ngắn hạn có kế hoạch, không phải cách bù estimate sai. Em: ① lập kế hoạch OT trước (ai, bao nhiêu giờ, mục đích, đến khi nào); ② theo dõi giờ OT từng người hằng tuần, ngưỡng cảnh báo nội bộ tham khảo > 20 giờ/tháng; ③ tuân thủ giới hạn của Bộ luật Lao động và quy chế công ty, có sự đồng ý của người lao động; ④ OT kéo dài > 2 tuần là tín hiệu phải xử lý gốc: phạm vi, estimate, nguồn lực.
> 💡 Nói "OT là triệu chứng, không phải giải pháp" kèm cách theo dõi bằng số.

**Q874. Dấu hiệu burnout của member là gì, bạn phát hiện sớm thế nào?**
Dấu hiệu: chất lượng giảm đột ngột (bug tăng ở người vốn cẩn thận), trễ việc, im lặng trong họp, dễ cáu, nghỉ ốm nhiều, làm khuya thường xuyên dù không ai yêu cầu, hoài nghi về dự án. Em phát hiện qua dữ liệu (OT, commit lúc nửa đêm, nghỉ đột xuất) kết hợp 1-on-1. Thấy dấu hiệu thì hỏi thẳng và giảm tải ngay, không đợi họ nộp đơn.

**Q875. Một member có dấu hiệu burnout nặng ngay giữa giai đoạn nước rút. Bạn làm gì?**
① Sức khỏe trước: nói chuyện riêng, đề xuất nghỉ vài ngày hoặc giảm tải ngay. ② Phân bổ lại: chuyển phần nằm trên critical path cho người khác, giao họ việc ít áp lực thời gian. ③ Cập nhật kế hoạch, rủi ro; nếu chạm mốc thì báo cấp trên và khách sớm theo 報連相. ④ Sau nước rút: tìm nguyên nhân gốc (quá tải, thiếu hỗ trợ) để 再発防止. Một người gục giữa chừng tốn hơn nhiều so với cho nghỉ 2 ngày.

**Q876. Khách Nhật dồn việc vào 年度末 (nendomatsu – cuối năm tài chính). Bạn chuẩn bị team thế nào?**
Nhiều doanh nghiệp Nhật kết thúc năm tài chính cuối tháng 3, nên tháng 1–3 thường dồn release và nghiệm thu. Em chuẩn bị từ quý trước: ① hỏi khách kế hoạch 年度末 sớm để lập capacity plan; ② hạn chế key member nghỉ dài giai đoạn này nhưng bố trí nghỉ bù trước/sau; ③ cross-training, nguồn lực dự phòng; ④ chốt phạm vi ưu tiên với khách. Tết Nguyên đán thường rơi đúng giai đoạn này, phải tính từ đầu.
> 💡 Chi tiết Tết Nguyên đán trùng 年度末 cho thấy bạn đã thực sự vận hành dự án Nhật.

**Q877. Member có quyền từ chối OT không? Nhiều người từ chối OT lúc gấp thì sao?**
Có — theo Bộ luật Lao động, làm thêm giờ cần người lao động đồng ý, trừ một số trường hợp đặc biệt luật quy định. Em không ép, không đánh giá thấp người từ chối OT. Nhiều người cùng từ chối là tín hiệu: em tìm lý do (mệt, kéo dài, không được ghi nhận), xoay vòng OT, ưu tiên lại phạm vi, xin thêm nguồn lực hoặc đàm phán mốc. Kế hoạch phải dựa vào OT bắt buộc là kế hoạch sai.
> 💡 Bẫy: "em sẽ thuyết phục mọi người OT vì dự án" — nghe như tư duy quản lý cũ.

**Q878. Khách liên tục đẩy yêu cầu gấp, bạn bảo vệ team mà vẫn giữ khách hài lòng thế nào?**
Em làm "lớp đệm" có nguyên tắc: mọi yêu cầu gấp đi qua PM/BrSE, được đánh giá effort và tác động, rồi đưa khách lựa chọn (làm ngay thì lùi việc nào, hoặc phát sinh chi phí). Member không nhận việc trực tiếp ngoài kênh. Em đếm số yêu cầu "gấp" mỗi tháng; nếu thành thường xuyên, đưa số liệu vào họp định kỳ để thống nhất lại quy trình. Bảo vệ team không phải nói "không", mà là làm rõ trade-off.

**Q879. Bạn sắp xếp nghỉ phép cho team thế nào để không ảnh hưởng dự án?**
Đầu năm/đầu quý em thu kế hoạch nghỉ dài, đưa vào lịch dự án cùng lịch nghỉ lễ lớn của Nhật (Golden Week, Obon, nghỉ cuối năm) và Việt Nam. Quy tắc: key member không nghỉ trùng nhau, người nghỉ có backup đã được bàn giao, nghỉ ≥ 3 ngày báo trước 1–2 tuần (tham khảo). Em khuyến khích nghỉ đủ phép, vì người cả năm không nghỉ là rủi ro burnout.

**Q880. PM có nên ở lại OT cùng team không?**
Em có mặt ở thời điểm quan trọng (release, sự cố, đêm deploy) để gỡ vướng và quyết nhanh, nhưng không ngồi lại chỉ để "làm gương" khi không có việc của PM — điều đó tạo áp lực ngầm buộc người khác ở lại. Em cũng không nhắn việc lúc khuya trừ khi khẩn, vì member sẽ hiểu là phải trả lời. Giữ sức cho PM cũng là giữ chất lượng quyết định.

**Q881. Sau giai đoạn OT dồn dập, bạn phục hồi team thế nào?**
① Nghỉ bù có kế hoạch, luân phiên để dự án vẫn chạy. ② Một sprint "nhẹ" cho nợ kỹ thuật, tài liệu, cải tiến — ít áp lực nhưng có giá trị. ③ Retro riêng về nguyên nhân OT (estimate, phạm vi, rủi ro bỏ sót) để 再発防止. ④ Ghi nhận cụ thể đóng góp, đưa vào đánh giá và đề xuất thưởng dự án. Bỏ qua phục hồi thì giai đoạn khó tiếp theo team sẽ vỡ.

## 9.9 Retention & quản lý tri thức

**Q882. Vì sao kỹ sư nhảy việc, và PM tác động được phần nào?**
Thường gặp: lương dưới thị trường, không thấy lộ trình, dự án nhàm/công nghệ cũ, quan hệ với quản lý trực tiếp, quá tải kéo dài. PM không quyết hết về lương nhưng tác động trực tiếp phần còn lại: phân việc có thử thách, IDP rõ, chặn quá tải, đối xử tôn trọng, và đề xuất tăng lương/thăng chức có bằng chứng ở mỗi kỳ review. Người ta thường rời người quản lý chứ không chỉ rời công ty.

**Q883. Stay interview là gì và bạn làm thế nào?**
Là buổi trò chuyện chủ động với người đang làm tốt để hiểu vì sao họ ở lại và điều gì có thể khiến họ đi — trước khi họ có ý định nghỉ (khác exit interview vốn chỉ để rút kinh nghiệm). Câu hỏi: "Điều gì khiến em muốn tiếp tục ở đây?", "Nếu điều gì thay đổi, em sẽ cân nhắc rời đi?", "Em muốn học gì mà chưa có cơ hội?". Em làm 1–2 lần/năm với key member và hành động ngay trên ít nhất một điều.

**Q884. Exit interview làm thế nào để có thông tin thật?**
Nên để HR hoặc người không phải quản lý trực tiếp thực hiện, vì người sắp nghỉ ít khi nói thật với PM của mình. Hỏi theo sự việc: "Khi nào em bắt đầu nghĩ đến việc rời đi?", "Nếu điều gì khác đi thì em đã ở lại?". Em tổng hợp xu hướng qua nhiều người (vd 3 người nghỉ cùng vì lộ trình) để đổi chính sách, thay vì xem từng ca riêng lẻ.

**Q885. Key member báo nghỉ vì có offer cao hơn 30%. Bạn có đưa counter offer không?**
Xác định lý do thật là tiền hay điều khác. Nếu chỉ là tiền và lương hiện tại thật sự dưới thị trường, em đề xuất điều chỉnh với cấp trên/HR trong khung chính sách (lẽ ra phải phát hiện sớm hơn). Nếu lý do là lộ trình, dự án hay quản lý, counter offer chỉ trì hoãn vài tháng và tạo tiền lệ bất công với người khác. Dù kết quả thế nào, em kích hoạt kế hoạch bàn giao ngay và không gây áp lực đạo đức.
> 💡 Nêu được rủi ro của counter offer (tiền lệ, bất công nội bộ, chỉ trì hoãn) là tư duy hệ thống của senior.

**Q886. Bus factor là gì, bạn đo và giảm bus factor thế nào?**
Bus factor là số người tối thiểu phải rời đi để dự án đình trệ; bằng 1 nghĩa là 属人化 nặng. Em lập skill matrix (module × người, mức 0–3), mục tiêu mỗi module quan trọng có ít nhất 2 người ở mức tự làm được. Cách giảm: review chéo bắt buộc, luân phiên task, pair cho phần lõi, tài liệu hóa, BrSE và Tech Lead đều có người kế cận.
> 💡 Đưa ra skill matrix cụ thể thuyết phục hơn câu chung chung "tài liệu hóa đầy đủ".

**Q887. Bạn tài liệu hóa kiến thức dự án thế nào mà không thành gánh nặng?**
Tài liệu hóa đúng chỗ: ① tài liệu "sống" gần code (README, ghi chép quyết định kiến trúc ngắn, runbook vận hành); ② glossary nghiệp vụ Nhật–Việt; ③ FAQ đúc kết từ Q&A với khách; ④ video ngắn cho thao tác phức tạp. Đưa "cập nhật tài liệu" vào Definition of Done của task thay vì dồn cuối dự án. Chỉ số kiểm: người mới tự setup và nắm tổng quan trong 2–3 ngày (tham khảo).

**Q888. Key member nghỉ, còn 30 ngày. Bạn tổ chức 引き継ぎ (hikitsugi – bàn giao) thế nào?**
① Ngày 1–2: chọn người nhận (ưu tiên 2 người), lập danh mục: module, tài liệu, tài khoản, việc dở dang, đầu mối với khách. ② Tuần 1–2: shadowing — người nhận ngồi cùng; tuần 3: reverse shadowing — người nhận làm, người đi review. ③ Viết 引き継ぎ書 (hikitsugi-sho – tài liệu bàn giao) có checklist ký xác nhận. ④ Báo khách thay đổi nhân sự kèm kế hoạch bàn giao. ⑤ Thu hồi quyền truy cập đúng ngày cuối.
> 💡 Reverse shadowing hay bị bỏ qua — người nhận phải "làm thật" khi người cũ vẫn còn đó.

**Q889. Bạn phản ứng thế nào khi biết một member đang đi phỏng vấn nơi khác?**
Không coi là phản bội, cũng không giả vờ không biết. Em tạo 1-on-1 tự nhiên hỏi về mức hài lòng và mong muốn phát triển — không truy hỏi "em có đi phỏng vấn không". Điều gì công ty đáp ứng được thì hành động; song song âm thầm tăng chia sẻ kiến thức ở module của người đó. Đối xử khác đi (ngừng giao việc hay, loại khỏi quyết định) chỉ đẩy họ đi nhanh hơn.

**Q890. Ngoài lương, bạn có công cụ nào để giữ người giỏi?**
① Việc có thử thách, công nghệ mới, cơ hội onsite hoặc làm việc trực tiếp với khách; ② lộ trình rõ (Tech Lead, BrSE, PM) gắn với kỳ review; ③ hỗ trợ học và thi chứng chỉ (tiếng Nhật, Cloud/AWS, PMP theo chính sách công ty); ④ ghi nhận đúng người; ⑤ quyền tự chủ, được tham gia quyết định; ⑥ môi trường không toxic. Em hỏi từng người điều gì quan trọng với họ, vì không có một công thức chung.

## 9.10 Tuyển, onboard cấp dự án & phong cách lãnh đạo

**Q891. Phỏng vấn dev cho dự án Nhật, ngoài kỹ thuật bạn đánh giá gì?**
Kỹ thuật để Tech Lead đánh giá; em tập trung: ① độ cẩn thận — đưa một đoạn spec ngắn, hỏi họ sẽ xác nhận gì trước khi code; ② thói quen 報連相 — "kể lần em biết mình sẽ trễ, em đã làm gì"; ③ thái độ với quy trình, review; ④ khả năng học tiếng Nhật, đọc tài liệu; ⑤ độ hợp với team hiện tại. Dự án Nhật cần người cẩn thận, minh bạch hơn người nhanh nhưng ẩu.

**Q892. Bạn phỏng vấn một BrSE như thế nào?**
Em kiểm 3 lớp: ① tiếng Nhật thực tế — đọc một đoạn yêu cầu tiếng Nhật, tóm tắt và chỉ ra điểm mơ hồ cần hỏi khách, viết thử email xác nhận; ② tư duy nghiệp vụ–kỹ thuật — chia yêu cầu thành task, estimate sơ bộ; ③ tình huống — khách đổi yêu cầu sát deadline thì làm gì. Chứng chỉ JLPT chỉ là điều kiện cần; khả năng phát hiện điểm mơ hồ mới là năng lực lõi của BrSE.
> 💡 Bài test "tìm điểm mơ hồ trong spec" phân loại BrSE rất nhanh.

**Q893. Kế hoạch onboarding 2 tuần cho thành viên mới vào dự án gồm những gì?**
Tuần 1: môi trường, tài khoản, quy định bảo mật của khách; tổng quan nghiệp vụ và kiến trúc; coding convention, quy trình review, checklist; gán buddy; làm 1–2 task nhỏ được review kỹ. Tuần 2: nhận task thật cỡ 1–2 ngày, dự họp với BrSE, đọc tài liệu thiết kế tiếng Nhật có glossary. Cuối tuần 2: 30 phút với PM xem tiến bộ và vướng mắc. Đích đo được: tự hoàn thành task nhỏ mà không cần kèm sát.

**Q894. Đào tạo fresher cho dự án Nhật, bạn tập trung vào những gì?**
Ngoài kỹ thuật, fresher cần thói quen làm việc dự án Nhật: ① 報連相 — báo sớm, báo cả tin xấu; ② đọc hiểu 設計書, hỏi khi chưa rõ thay vì tự đoán; ③ tự review theo checklist trước khi gửi; ④ ghi chép, tuân thủ quy trình; ⑤ hiểu vì sao khách khắt khe về chất lượng. Em dùng buddy + task tăng dần độ khó + review kỹ trong 1–3 tháng đầu, đánh giá theo mốc rõ ràng.

**Q895. Bạn ủy quyền (delegation) thế nào, làm sao biết nên giao đến mức nào?**
Mức ủy quyền theo năng lực và rủi ro: "làm theo hướng dẫn" → "đề xuất, PM duyệt" → "tự quyết, báo sau" → "tự quyết hoàn toàn". Khi giao: nói rõ kết quả, giới hạn (ngân sách, mốc), quyền hạn và điểm kiểm tra. Việc em không ủy quyền: cam kết cuối với khách, đánh giá hiệu suất, quyết định nhân sự nhạy cảm. Giao việc mà không giao quyền là giao gánh nặng.

**Q896. Situational leadership là gì? Ví dụ áp dụng với các member khác nhau trong cùng team.**
Mô hình Hersey–Blanchard: phong cách thay đổi theo mức phát triển của từng người với từng việc — **Directing**, **Coaching**, **Supporting**, **Delegating**. Ví dụ: fresher → chỉ dẫn từng bước; dev 2 năm lần đầu làm BrSE → coaching (vừa chỉ vừa động viên); senior giỏi vừa gặp thất bại → supporting, lắng nghe, củng cố tự tin; Tech Lead vững → delegating. Cùng một người có thể ở mức khác nhau với việc khác nhau.

**Q897. Bạn quản lý member lớn tuổi hơn hoặc giỏi kỹ thuật hơn mình thế nào?**
Em xác định là khác vai chứ không phải hơn kém: họ là chuyên gia kỹ thuật, em chịu trách nhiệm điều phối và cam kết với khách. Tôn trọng bằng hành động: hỏi ý kiến họ trước quyết định kỹ thuật, giao việc khó với quyền tự chủ cao, ghi nhận công khai. Nhưng thỏa thuận chung (báo cáo, quy trình, deadline) áp dụng như mọi người. Xưng hô và lễ độ phù hợp với văn hóa trọng tuổi tác.
> 💡 Bẫy: "em sẽ chứng tỏ năng lực để họ phục" — nghe như cạnh tranh; hãy nói về phân vai và tôn trọng.

**Q898. Servant leadership có phù hợp với môi trường dự án Nhật vốn trọng thứ bậc không?**
Servant leadership là lãnh đạo bằng phục vụ: gỡ cản trở, phát triển người, đặt thành công của team lên trước. Em kết hợp: với khách và cấp trên, PM là đầu mối chịu trách nhiệm rõ ràng, đúng thứ bậc; với team nội bộ, em là servant leader — chặn yêu cầu ngoài luồng, lo nguồn lực, để team tập trung. Phục vụ không có nghĩa là thiếu quyết đoán: khi sự cố hay deadline gấp, em vẫn chỉ đạo trực tiếp.

**Q899. Có nên đề bạt dev giỏi kỹ thuật nhất làm leader không?**
Không mặc định. Leader cần năng lực khác: phân việc, kèm người, chịu trách nhiệm kết quả của người khác. Em xét bằng hành vi đã thấy (từng kèm junior chưa, xử lý bất đồng ra sao), cho thử vai nhỏ 2–3 tháng có hỗ trợ, và đề xuất lộ trình chuyên gia song song để người giỏi kỹ thuật không phải "lên quản lý mới được tăng lương". Đề bạt sai có thể mất cả một dev giỏi lẫn một leader tốt.
> 💡 Nhắc "dual career ladder" (lộ trình kép chuyên gia/quản lý) là câu trả lời mang tầm senior.

**Q900. Làm sao bạn biết mình đang lãnh đạo tốt, và xin feedback từ cấp dưới thế nào?**
Em nhìn 3 nhóm chỉ báo: kết quả (QCD dự án), sức khỏe team (pulse survey, OT, tỉ lệ nghỉ việc) và mức tự chủ (bao nhiêu việc team tự giải quyết không cần em). Feedback từ dưới lên: khảo sát ẩn danh mỗi kỳ review, câu hỏi cố định cuối 1-on-1, retro có mục dành cho PM. Quan trọng là hành động và nói lại đã thay đổi gì; thước đo cuối cùng: team vẫn chạy tốt khi em vắng một tuần.
