---
title: Mindmap tình huống PM
markmap:
  initialExpandLevel: 2
---

<!-- Mở bằng markmap. Bản đầy đủ: tinh-huong-PM.md · bản tương tác: tinh-huong-PM.html -->

# 45 tình huống PM

## Khung 4 nhịp
- ① Xác nhận fact
- ② Hành động ngay
- ③ Báo khách theo 報連相
- ④ Gốc rễ & phòng ngừa

## Tiến độ & 納期
### S01 · Phát hiện trễ ngay trước 結合テスト
- Làm trước: Trong 2 ngày phân tích trễ theo module và critical path, lập 2–3 phương án hồi phục, rồi báo khách.
- Đừng: Ghi 'on track' trong 進捗報告書 khi chưa đối chiếu WBS với deliverable thật.
### S02 · Khách không cho dời 納期 gắn quy định
- Làm trước: Phân loại chức năng theo mức bắt buộc của quy định, đề xuất phát hành phân kỳ: phần bắt buộc đúng 1/4.
- Đừng: Nói 'chúng tôi sẽ cố gắng hết sức' mà không thay đổi biến số nào (phạm vi, người, thời gian).
### S03 · Vendor khác trễ 基本設計, team phải chờ
- Làm trước: Định lượng tác động trong 1 ngày, báo 窓口 khách bằng văn bản, đề xuất làm trước phần đã chốt.
- Đừng: Im lặng chờ đến khi 基本設計 về rồi mới báo khách là đã trễ.
### S04 · Khách trả lời QA chậm, chặn 製造
- Làm trước: Lập danh sách 8 câu quá hạn kèm tác động và giả định đề xuất, xin khách xác nhận tại 定例会.
- Đừng: Hỏi lại câu cũ mà không kèm giả định, khiến khách phải tự nghĩ lại từ đầu.
### S05 · Tiếp nhận dự án đỏ từ PM khác
- Làm trước: Trong 5 ngày làm health check (WBS, 課題, bug, 1-1 với lead/BrSE), gặp khách nghe trước, rồi trình baseline thật.
- Đừng: Đổ lỗi PM cũ trước mặt khách — với khách, đó vẫn là cùng một công ty.

## Phạm vi & thay đổi
### S06 · Khách đổi spec sau khi chốt 基本設計
- Làm trước: Tiếp nhận yêu cầu, phân tích tác động trong 2 ngày, gửi CR kèm 見積 và lịch để khách quyết.
- Đừng: Ước lượng miệng 'khoảng 1 tuần' ngay trong cuộc họp.
### S07 · Yêu cầu 'đương nhiên phải có' (当然)
- Làm trước: Trong 1 ngày đối chiếu 要件定義書, NFR, 議事録, QA管理表 để tìm căn cứ, rồi mới trả lời khách.
- Đừng: Nói 'không có trong spec' như câu chốt mà không đưa tài liệu và phương án.
### S08 · Yêu cầu thay đổi gửi thẳng qua chat
- Làm trước: Gom 14 yêu cầu, đo 工数, phân loại trong/ngoài phạm vi, rồi thống nhất với 窓口 quy trình một cửa.
- Đừng: Trách dev trước cả team vì 'chiều khách' — họ làm vậy vì thiếu quy tắc.
### S09 · Khách từ chối thanh toán CR đã làm
- Làm trước: Gom bằng chứng, cùng sales gặp 窓口 tìm hiểu vướng 稟議, đề xuất cách hợp thức hóa hoặc bù trừ.
- Đừng: Đổ lỗi trưởng nhóm nghiệp vụ trước mặt phòng mua hàng.
### S10 · Hai phòng ban khách yêu cầu mâu thuẫn
- Làm trước: Ghi mâu thuẫn vào 課題管理表 kèm phương án và tác động, nhờ 窓口 chủ trì buổi chốt trước hạn.
- Đừng: Nói với một phòng rằng phòng kia 'đang gây khó'.

## Chất lượng & bug
### S11 · 受入テスト tuần đầu ra 48 phiếu lỗi
- Làm trước: Trong 24 giờ phân loại 48 phiếu theo bản chất và mức độ, báo khách sơ bộ kèm kế hoạch cho phiếu nghiêm trọng.
- Đừng: Tranh luận từng phiếu 'lỗi hay không lỗi' qua email trước khi có buổi thống nhất.
### S12 · Khách chê lỗi chính tả trong tài liệu
- Làm trước: Xin lỗi, phân loại 120 指摘 trong 1 ngày, lập kế hoạch sửa và rà cả 4 tài liệu sắp nộp.
- Đừng: Đổ lỗi comtor hoặc người viết trước mặt khách.
### S13 · Bug density thấp bất thường
- Làm trước: Coi đây là tín hiệu cần kiểm tra: xem mật độ test, độ bao phủ yêu cầu, loại test case và cách ghi bug.
- Đừng: Coi bug density thấp là tốt mà không đặt cạnh mật độ test.
### S14 · Sự cố lặp lại, khách đòi なぜなぜ分析
- Làm trước: Trong vài giờ xác nhận phạm vi ảnh hưởng và biện pháp tạm thời, gửi 第一報 (báo cáo nhanh) cho khách.
- Đừng: Kết luận なぜなぜ bằng 'chú ý hơn', 'tăng cường review' — không đo được, khách sẽ trả lại.
### S15 · Deadline ép bỏ bớt test
- Làm trước: Xếp hạng test case theo rủi ro, chạy hết nhóm cao, trình khách rủi ro còn lại để khách quyết bằng văn bản.
- Đừng: Ngầm bỏ test nhưng vẫn báo cáo '100% pass'.

## Sự cố 本番
### S16 · Lỗi tính lãi phát hiện sau 3 tuần 本番
- Làm trước: Trong 2 giờ khoanh vùng điều kiện lỗi và số tài khoản sơ bộ, rồi báo ngay 窓口 khách bằng 第一報.
- Đừng: Tự hotfix 本番 hệ thống ngân hàng không qua quy trình phê duyệt thay đổi của khách.
### S17 · 夜間バッチ dừng giữa chừng lúc 3h sáng
- Làm trước: Đọc log xác nhận nguyên nhân và dữ liệu job 1–4, đúng runbook thì rerun từ job 5.
- Đừng: Rerun toàn bộ batch mà không kiểm tra các job đã commit, gây nhân đôi dữ liệu.
### S18 · Dữ liệu địa chỉ khách sai sau release
- Làm trước: Đối chiếu dữ liệu trước/sau migration để đếm bản ghi sai, đồng thời báo khách xin tạm dừng in thư.
- Đừng: Rollback cả release khi chưa biết dữ liệu phát sinh sau release sẽ bị ảnh hưởng thế nào.
### S19 · Sự cố 2h sáng, không gọi được 窓口
- Làm trước: Gọi tiếp tuyến escalation trong 体制図, email ghi nhận các lần gọi, chuẩn bị sẵn thao tác chờ đồng ý.
- Đừng: Tự sửa 本番 vì 'chắc chắn đúng' mà không có đồng ý — vượt quyền dù kết quả tốt.
### S20 · Release lỗi đúng tuần 年度末
- Làm trước: Trong nửa ngày so sánh các phương án theo dữ liệu, rủi ro, thời gian, kèm cách tạm để khách quyết.
- Đừng: Chọn thay khách giữa rollback và fix-forward khi người chịu thiệt hại là khách.

## Khách hàng & giao tiếp
### S21 · 課長 phía khách nổi giận giữa 定例会
- Làm trước: Tự lên tiếng nhận trách nhiệm, xin lỗi ngắn, nhắc lại đúng vấn đề, hẹn mốc gửi báo cáo đối sách.
- Đừng: Để BrSE trẻ đứng ra đỡ đòn và tranh luận kỹ thuật trước mặt 課長.
### S22 · 担当者 phía khách đổi người giữa dự án
- Làm trước: Xin người cũ xác nhận bằng văn bản 5 thỏa thuận miệng, rồi đề xuất họp bàn giao 3 bên.
- Đừng: Coi thỏa thuận miệng của người cũ là đã chốt — người mới có quyền lật lại.
### S23 · Khách im lặng, QA quá hạn 2 tuần
- Làm trước: Phân loại 12 câu theo mức chặn, gửi 窓口 danh sách ưu tiên kèm phương án đề xuất và hạn trả lời mới.
- Đừng: Tự giả định rồi coi im lặng là khách đã đồng ý.
### S24 · Khách dọa chuyển vendor sau chuỗi trễ hạn
- Làm trước: Xin gặp 部長 trong tuần để nghe trực tiếp mức độ bất mãn, rồi trình kế hoạch cải thiện có KPI.
- Đừng: Giảm giá ngay — giữ được khách ngắn hạn nhưng vấn đề giao hàng vẫn nguyên.
### S25 · Khách muốn họp thẳng với dev, bỏ BrSE
- Làm trước: Tìm hiểu vì sao hiểu sai 2 lần, đề xuất họp kỹ thuật có dev tham gia, BrSE điều phối, thử 2 tuần.
- Đừng: Để dev nhận yêu cầu trực tiếp không có 議事録, phạm vi phình ra mà không qua CR.

## Team & con người
### S26 · Tech lead xin nghỉ giữa 結合テスト
- Làm trước: Nói chuyện riêng với tech lead trong ngày để hiểu lý do thật và chốt kế hoạch bàn giao 30 ngày.
- Đừng: Counter-offer bằng tiền ngay mà không hiểu lý do — thường chỉ giữ được vài tháng.
### S27 · BrSE nghỉ đột ngột, chỉ còn 3 ngày
- Làm trước: Liệt kê việc BrSE đang giữ, bàn giao theo ưu tiên trong 3 ngày, báo khách 体制 tạm trước 定例会.
- Đừng: Giấu khách việc BrSE nghỉ — khách sẽ nhận ra ngay ở 定例会.
### S28 · Ramp-up gấp từ 5 lên 20 người
- Làm trước: Đo năng lực onboarding thật, lập kế hoạch ramp-up theo đợt, thống nhất nội bộ rồi trình khách.
- Đừng: Chạy theo con số 20 người — năng suất có thể giảm vì người cũ mất thời gian kèm.
### S29 · Member giỏi nhất nhưng toxic với team
- Làm trước: Thu thập ví dụ cụ thể, gặp riêng nói rõ hành vi, tác động và kỳ vọng, có thời hạn theo dõi.
- Đừng: Dung túng vì 'người giỏi khó thay' — team sẽ dần mất những người tốt khác.
### S30 · Team OT kéo dài, dấu hiệu burnout
- Làm trước: Dừng tăng OT, đo lại khối lượng còn và năng suất thật, trình khách phương án phạm vi/納期 theo số liệu.
- Đừng: Dùng OT để che giấu trễ hạn với khách — chất lượng giảm và rủi ro lao động tăng.

## Chi phí & hợp đồng
### S31 · 請負 vượt effort 30%, CPI 0,77
- Làm trước: Phân tích phần vượt theo nguyên nhân: thay đổi yêu cầu ngầm, rework, estimate sai, năng suất; rồi tính EAC.
- Đừng: Đòi khách trả cho toàn bộ phần vượt, kể cả phần do lỗi nội bộ.
### S32 · Sếp ép nhận dự án dưới giá vốn
- Làm trước: Trình sếp 2–3 phương án có số: giảm scope, chia giai đoạn, hoặc nhận lỗ có kiểm soát qua 稟議.
- Đừng: Hạ estimate nhưng giữ nguyên scope và không ghi điều kiện tiền đề.
### S33 · Khách muốn đổi 準委任 sang 請負 giữa chừng
- Làm trước: Hỏi lý do của khách, rà scope còn mở, rồi đề xuất điều kiện chuyển: chốt yêu cầu trước, estimate lại.
- Đừng: Ký 請負 khi scope còn mở mà không có điều kiện tiền đề và quy trình CR.
### S34 · Khách ép giảm giá vì yên yếu
- Làm trước: Tính GM ở từng mức giảm và chuẩn bị 2–3 gói thay thế (đổi cơ cấu team, chia sẻ tỉ giá) trước khi đàm phán.
- Đừng: Nhượng bộ toàn bộ mức giảm ngay trong cuộc gọi đầu tiên.
### S35 · Estimate sai lộ ra ở 詳細設計
- Làm trước: Đối chiếu 40 quy tắc với 基本設計書, 議事録 và 前提条件 của estimate để phân loại phần nào là scope mới.
- Đừng: Gộp cả phần lỗi estimate của mình vào CR đòi khách trả.

## Rủi ro & bảo mật
### S36 · Member dán code, dữ liệu khách vào ChatGPT
- Làm trước: Xác nhận ngay nội dung đã dán, số bản ghi, cài đặt tài khoản, rồi báo bộ phận bảo mật nội bộ trong ngày.
- Đừng: Bảo developer xóa lịch sử chat cho 'xong chuyện' — vừa mất bằng chứng vừa che giấu.
### S37 · Mất laptop chứa source code dự án
- Làm trước: Báo IT/bảo mật ngay tối nay để xác nhận mã hóa, khóa máy từ xa và thu hồi mọi quyền truy cập.
- Đừng: Chờ đến ngày làm việc tiếp theo mới báo vì 'biết đâu tìm lại được'.
### S38 · Gửi nhầm email chứa dữ liệu khách
- Làm trước: Xác nhận người nhận và nội dung file, báo bộ phận bảo mật, yêu cầu người nhận xóa có xác nhận.
- Đừng: Dựa vào recall rồi không báo ai.
### S39 · Audit ISMS phát hiện vi phạm ở dự án
- Làm trước: Khắc phục ngay 2 điểm, rà toàn bộ phạm vi tương tự, rồi phân tích gốc rễ và lập 是正処置 có hạn.
- Đừng: Chỉ sửa đúng 2 điểm bị phát hiện mà không rà toàn bộ.
### S40 · Vendor khác trễ IF, chặn dự án
- Làm trước: Định lượng tác động lên lịch, báo khách bằng văn bản, đề nghị khách điều phối vendor X, kèm phương án stub.
- Đừng: Tự làm thay phần IF của vendor khác, nhận trách nhiệm ngoài hợp đồng.

## Tình huống xám
### S41 · Khách gợi ý ghi giảm số bug trong báo cáo
- Làm trước: Giữ số gốc, bổ sung phân tích theo nguyên nhân, mức độ và xu hướng hội tụ để giải thích đúng chất lượng.
- Đừng: Chỉnh số để làm hài lòng một người phía khách mà không có quy tắc đếm đã thống nhất.
### S42 · Sếp muốn giấu delay đến sau review
- Làm trước: Lập kế hoạch phục hồi có số, thuyết phục sếp báo khách kèm kế hoạch đó trước buổi review.
- Đừng: Dùng OT dài ngày để che trễ thay vì báo sớm có kế hoạch.
### S43 · Chọn 納期 hay chất lượng trước 本番
- Làm trước: Phân tích rủi ro từng bug, đề xuất release 1/4 có điều kiện: chặn hoặc xử lý thủ công phần lỗi, hotfix theo lịch.
- Đừng: Tự quyết lùi hay giữ ngày release thay khách mà không đưa phương án.
### S44 · Một PM, hai dự án cùng đỏ
- Làm trước: Đánh giá tác động và độ khẩn của mỗi dự án, ưu tiên 1 bên, xin sếp người hỗ trợ bên còn lại.
- Đừng: Tự chọn bỏ một dự án mà không báo sếp.
### S45 · Khách đòi OT cuối tuần không trả thêm
- Làm trước: Đối chiếu hợp đồng và số giờ OT thực tế, rồi đề xuất khách quy tắc làm thêm có duyệt, có phí.
- Đừng: Để khách giao việc thẳng cho leader, bỏ qua PM.

