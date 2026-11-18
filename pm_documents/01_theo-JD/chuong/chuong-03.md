# Chương 3 · Agile, Scrum, Waterfall & Hybrid trong dự án Nhật (Q201–Q300)

## 3.1 Waterfall & V-model kiểu Nhật

**Q201. Hãy mô tả chuỗi 工程 của một dự án waterfall kiểu Nhật từ đầu đến cuối.**
Chuỗi 工程 (koutei – công đoạn) chuẩn: 要件定義 (youken teigi – định nghĩa yêu cầu) → 基本設計 (kihon sekkei – thiết kế cơ bản) → 詳細設計 (shousai sekkei – thiết kế chi tiết) → 製造 (seizou – lập trình) → 単体テスト (tantai tesuto – unit test) → 結合テスト (ketsugou tesuto – integration test) → 総合テスト (sougou tesuto – system test) → 受入テスト (ukeire tesuto – acceptance test). Mỗi 工程 kết thúc bằng review và phê duyệt 成果物 (seikabutsu – sản phẩm bàn giao) rồi mới sang bước sau. Tên gọi tùy công ty nên em chốt bảng 工程 với khách ngay kickoff.

**Q202. V-model ánh xạ các 工程 thiết kế với các mức test như thế nào?**
Nhánh trái là thiết kế, nhánh phải là test kiểm chứng tương ứng: 要件定義 ↔ 受入テスト, 基本設計 ↔ 総合テスト, 詳細設計 ↔ 結合テスト, 製造 ↔ 単体テスト. Ý nghĩa thực tế: test case mức nào viết dựa trên tài liệu thiết kế mức đó, và test viewpoint nên lập ngay khi thiết kế xong chứ không đợi code. Một số công ty ghép khác (vd 基本設計 ↔ 結合テスト), nên em xác nhận mapping trong kế hoạch test từ đầu.
> 💡 Bẫy: nói "unit test viết từ tài liệu yêu cầu" là sai tầng — interviewer quen V-model sẽ bắt ngay.

**Q203. 上流工程 và 下流工程 khác nhau thế nào, offshore Việt Nam thường nhận phần nào?**
`上流工程` (jouryuu koutei – công đoạn thượng nguồn) gồm 要件定義, 基本設計: xác định "làm gì", cần hiểu nghiệp vụ và làm trực tiếp với khách. `下流工程` (karyuu koutei – hạ nguồn) gồm 詳細設計 → 製造 → test: "làm thế nào". Offshore truyền thống nhận từ 詳細設計 đến 結合テスト, onsite và BrSE (Bridge System Engineer – kỹ sư cầu nối) giữ 基本設計. Muốn lên thượng nguồn để tăng giá trị, Senior PM cần lộ trình năng lực: domain, tiếng Nhật, BrSE.
> 💡 Nói được "muốn nhận 上流 thì phải chứng minh bằng chất lượng 下流 trước" thể hiện tư duy chiến lược.

**Q204. 手戻り là gì và vì sao trong waterfall nó đắt?**
`手戻り` (temodori – làm lại do lỗi từ công đoạn trước) xảy ra khi lỗi yêu cầu/thiết kế đến lúc test mới lộ ra, buộc quay lại sửa tài liệu, code, test case rồi test lại. Phát hiện càng muộn càng đắt vì phải đi ngược qua nhiều 工程 và nhiều 成果物 đã phê duyệt. Cách giảm: review chéo tài liệu, Q&A sớm với khách, prototype màn hình quan trọng và exit criteria rõ cho mỗi 工程.

**Q205. Khi nào waterfall vẫn là lựa chọn đúng?**
Waterfall hợp khi ① yêu cầu ổn định, có quy định rõ (hệ thống lõi ngân hàng, bảo hiểm, kế toán), ② chi phí sai cao và cần audit trail tài liệu, ③ hợp đồng 請負 (ukeoi – khoán theo kết quả) giá cố định với phạm vi chốt, ④ tích hợp nhiều hệ thống cần lịch test liên kết cố định, ⑤ thay thế hệ thống cũ với spec "như hiện trạng". Tiêu chí em dùng: độ bất định yêu cầu thấp và chi phí thay đổi muộn cao → waterfall; ngược lại → agile hoặc hybrid.
> 💡 Đừng chê waterfall — nhiều khách tài chính Nhật vẫn chạy waterfall; trả lời "chọn theo bối cảnh, có tiêu chí" chín chắn hơn.

**Q206. Exit criteria của một 工程 thường gồm những gì?**
Tối thiểu: ① 成果物 hoàn thành theo danh sách đã thống nhất, ② review xong và mọi 指摘 (shiteki – điểm bị chỉ ra khi review) đã đóng hoặc có kế hoạch xử lý, ③ Q&A với khách không còn câu mở ảnh hưởng 工程 sau, ④ chỉ số chất lượng đạt ngưỡng thỏa thuận, ⑤ khách phê duyệt. Em đặt checklist này thành gate trong kế hoạch, không "trượt" sang 工程 sau khi chưa đạt, trừ khi rủi ro được chấp nhận bằng văn bản.

**Q207. Waterfall có thể chạy chồng lấn các 工程 không? Rủi ro gì?**
Có, thường gọi là overlapping: bắt đầu 詳細設計 module A khi 基本設計 module B chưa xong, hoặc chia phase theo module. Lợi ích là rút ngắn lịch; rủi ro là thay đổi thượng nguồn lan xuống và 手戻り nhân lên. Em chỉ cho chồng lấn khi phần thượng nguồn của chính module đó đã được phê duyệt, ghi giả định vào risk register và giữ khoảng 5–10% effort dự phòng cho 手戻り (tham khảo).

**Q208. Trong waterfall, làm sao phát hiện sớm lỗi yêu cầu trước khi code?**
① Prototype/mock màn hình và luồng chính ngay trong 基本設計 để khách "thấy" thay vì chỉ đọc tài liệu, ② walkthrough tài liệu với khách theo checklist, ③ viết test viewpoint của 総合テスト song song 基本設計 — không viết được test nghĩa là yêu cầu chưa rõ, ④ làm spike kỹ thuật cho phần rủi ro như tích hợp, hiệu năng. Đây là cách đưa vòng phản hồi ngắn vào waterfall mà không phá cấu trúc 工程.

**Q209. Waterfall và V-model khác nhau thế nào? Có phải hai mô hình riêng?**
V-model là biến thể của waterfall, nhấn mạnh mỗi mức thiết kế có một mức test kiểm chứng tương ứng. Waterfall thuần chỉ nói thứ tự tuần tự; V-model nói thêm "test được lập kế hoạch từ lúc thiết kế" và phân biệt verification với validation. Ở dự án Nhật, khi khách nói ウォーターフォール (waterfall) gần như luôn ngầm hiểu theo V-model với đủ 単体, 結合, 総合, 受入.

**Q210. Offshore làm đến 結合テスト, khách tự làm 総合テスト nhưng lại tính bug lọt cho offshore. PM xử lý ranh giới trách nhiệm thế nào?**
① Chốt bằng văn bản phạm vi từng 工程 và định nghĩa "bug lọt"; ② thống nhất tiêu chí bàn giao 結合テスト (số case, độ phủ viewpoint, bug còn mở) mà khách đồng ý; ③ khi bug phát sinh ở 総合テスト, phân loại nguồn gốc — lỗi spec/thiết kế phía khách hay lỗi chế tạo offshore — chứ không nhận hết; ④ với bug của mình: phân tích nguyên nhân, 再発防止 (saihatsu boushi – phòng ngừa tái phát) và 横展開 (yokotenkai – áp dụng sang chỗ tương tự).
> 💡 Nhận nhanh và rõ phần lỗi của mình — khách Nhật đánh giá thái độ này cao hơn việc tranh luận đúng sai.

## 3.2 Scrum framework

**Q211. Scrum có những thành phần nào theo Scrum Guide 2020?**
Cấu trúc "3-5-3": ① 3 accountabilities: Product Owner, Scrum Master, Developers; ② 5 events: Sprint (chứa các event khác), Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective; ③ 3 artifacts kèm commitment: Product Backlog → Product Goal, Sprint Backlog → Sprint Goal, Increment → Definition of Done. Nền tảng là empiricism (transparency, inspection, adaptation) và lean thinking.
> 💡 Dùng đúng từ "accountabilities", "Developers" (không phải "roles", "Development Team") cho thấy bạn cập nhật bản 2020.

**Q212. Ba commitment Product Goal, Sprint Goal, DoD có tác dụng gì?**
Mỗi commitment cho artifact một thước đo tiến độ: Product Goal là mục tiêu dài hạn mà Product Backlog hướng tới; Sprint Goal là lý do tồn tại của sprint, giúp team linh hoạt đổi item mà vẫn giữ cam kết; DoD định nghĩa khi nào item đủ chất lượng để thành Increment. Ở dự án outsource em hay gặp sprint thiếu Sprint Goal — sprint thành "danh sách ticket" và khách chỉ đếm số ticket xong.

**Q213. Timebox của các event Scrum là bao nhiêu?**
Với sprint 1 tháng: Sprint ≤ 1 tháng, Sprint Planning tối đa 8 giờ, Daily Scrum 15 phút, Sprint Review tối đa 4 giờ, Sprint Retrospective tối đa 3 giờ; sprint ngắn hơn thì các event thường ngắn hơn. Refinement không phải event; Scrum Guide bản cũ gợi ý không quá 10% capacity. Với khách Nhật, em đặt lịch review cố định cùng thứ, cùng giờ để khách dễ xếp lịch nội bộ.
> 💡 Bẫy PSM: "refinement là event" — sai, đó là hoạt động liên tục.

**Q214. Sprint Planning trả lời những câu hỏi nào?**
Ba chủ đề: ① Why – sprint này mang lại giá trị gì, team cùng PO chốt Sprint Goal; ② What – chọn item từ Product Backlog đủ để đạt goal, dựa trên capacity và hiệu suất quá khứ; ③ How – Developers tách item thành việc nhỏ, thường ≤ 1 ngày. Output là Sprint Backlog gồm Sprint Goal, item đã chọn và kế hoạch thực hiện. Ở offshore, em yêu cầu PO hoặc proxy PO có mặt ít nhất phần Why–What.

**Q215. Daily Scrum đúng nghĩa khác gì một buổi báo cáo tiến độ?**
Daily Scrum là buổi Developers tự inspect tiến độ hướng tới Sprint Goal và điều chỉnh kế hoạch cho 24 giờ tới, không phải báo cáo cho PM hay khách. Scrum Guide 2020 bỏ bắt buộc 3 câu hỏi; team tự chọn cấu trúc, miễn 15 phút và xoay quanh goal. Dấu hiệu sai: mọi người nhìn PM khi nói, hoặc thảo luận kỹ thuật kéo dài — em tách phần đó ra buổi ngắn ngay sau daily.

**Q216. Sprint Review có phải buổi khách nghiệm thu không?**
Không. Sprint Review là buổi làm việc để inspect Increment và điều chỉnh Product Backlog cùng stakeholder, không phải gate phê duyệt; release có thể diễn ra bất cứ lúc nào trong sprint. Tuy vậy với khách Nhật, em vẫn ghi 議事録 (gijiroku – biên bản họp): feedback, item được chấp nhận theo DoD/AC, item quay về backlog — làm bằng chứng tiến độ cho 検収 (kenshuu – nghiệm thu) theo hợp đồng khi cần.

**Q217. Ai có quyền hủy sprint và khi nào nên hủy?**
Chỉ Product Owner có quyền hủy sprint, khi Sprint Goal trở nên lỗi thời — vd khách đổi chiến lược hay dừng tính năng. Hủy sprint tốn kém: item đã Done được review, phần còn lại quay về Product Backlog và lên kế hoạch lại. Thực tế em ưu tiên cùng PO đàm phán lại phạm vi trong sprint, giữ Sprint Goal nếu còn ý nghĩa; hủy là lựa chọn cuối.
> 💡 Bẫy PSM: Scrum Master hoặc stakeholder "hủy sprint" — sai, chỉ PO có quyền này.

**Q218. Definition of Ready (DoR) có trong Scrum Guide không? Có nên dùng?**
DoR không có trong Scrum Guide, đó là practice bổ sung. Nó hữu ích ở outsourcing vì chênh lệch ngôn ngữ: item chỉ vào sprint khi có user story rõ, AC đo được, mockup/API spec, dependency đã xử lý, Q&A với khách đã đóng và đã estimate. Rủi ro: DoR quá cứng biến thành mini-waterfall và chặn dòng chảy; em giữ DoR 5–7 mục, PO có thể nhận item chưa đủ nếu ghi rõ giả định.

**Q219. DoD nên có gì trong dự án outsource cho khách Nhật?**
DoD là tiêu chuẩn chất lượng áp cho mọi item: code review xong, unit test pass và đạt coverage thỏa thuận, không còn bug mức cao, test đủ theo AC, merge vào nhánh chính và deploy được lên staging, tài liệu liên quan đã cập nhật. Với khách Nhật, em thêm mục "đã cập nhật 設計書 (sekkeisho – tài liệu thiết kế) tiếng Nhật" nếu hợp đồng yêu cầu, vì đây là thứ hay bị bỏ quên nhất.
> 💡 Phân biệt rõ DoD (chung cho mọi item) với AC (riêng từng story) — câu PSM rất hay gặp.

**Q220. Product Backlog refinement diễn ra thế nào khi PO ở Nhật, team ở Đà Nẵng?**
Em làm 2 lớp: ① BA/BrSE phía offshore chuẩn bị trước — tách story, viết AC, liệt kê câu hỏi tiếng Nhật trong bảng Q&A; ② buổi refinement online 45–60 phút mỗi tuần với PO để chốt câu hỏi và ưu tiên, team estimate ngay sau đó. Mục tiêu là luôn có backlog "ready" cho 1–2 sprint tới. Câu hỏi chưa được trả lời quá 2 ngày làm việc thì em escalate vì sẽ chặn sprint sau.

**Q221. Scrum Team nên có bao nhiêu người? Team offshore 15 người có nên là một Scrum Team?**
Scrum Guide 2020 khuyến nghị Scrum Team thường từ 10 người trở xuống. Với 15 người, Daily khó giữ 15 phút và kênh giao tiếp tăng mạnh; em tách 2 team theo feature/domain (không tách theo FE/BE), dùng chung một Product Backlog và một PO, đồng bộ qua refinement chung và Scrum of Scrums. Mỗi team phải đủ kỹ năng để tự làm ra Increment.

**Q222. Scrum Guide 2020 thay đổi gì so với bản trước mà PM nên biết?**
Những điểm chính: ① bỏ "Development Team", chỉ còn Developers trong một Scrum Team; ② thêm Product Goal; ③ mỗi artifact có commitment; ④ dùng "accountabilities" thay "roles", "self-managing" thay "self-organizing"; ⑤ bỏ 3 câu hỏi Daily, Sprint Planning thêm chủ đề Why; ⑥ Scrum Master là "true leaders who serve" thay "servant leader"; ⑦ ngôn ngữ bớt IT, dùng được ngoài phần mềm. Câu hỏi bẫy khi thi PSM hay xoáy vào ①②⑤.

## 3.3 Scrum Master, PM và PO trong mô hình outsourcing

**Q223. Scrum không có vai trò PM. Vậy Senior PM ở công ty outsourcing làm gì khi dự án chạy Scrum?**
Scrum Team không có PM, nhưng hợp đồng outsource vẫn cần người chịu trách nhiệm thương mại: ngân sách, hợp đồng, nhân sự, rủi ro cấp dự án, báo cáo cho khách và ban lãnh đạo. Em đứng ngoài Scrum Team ở tầng delivery: bảo vệ team khỏi yêu cầu ngoài luồng, quản lý capacity, quản lý thay đổi hợp đồng, đảm bảo SM và proxy PO làm được việc. Dự án nhỏ em có thể kiêm SM nhưng phải tách bạch lúc nào đang ở vai SM.
> 💡 Đừng nói "PM chính là Scrum Master" — interviewer muốn thấy bạn hiểu khác biệt nhưng vẫn thực dụng.

**Q224. Khách Nhật làm PO được không? Thực tế thường gặp vấn đề gì?**
Được, và là lý tưởng vì khách nắm nghiệp vụ và ưu tiên. Vấn đề hay gặp: ① PO là người kiêm nhiệm, ít thời gian; ② quyết định cần 稟議 (ringi – trình duyệt nội bộ) nên chậm; ③ rào cản ngôn ngữ; ④ PO quen viết spec chi tiết hơn là sắp ưu tiên theo giá trị. Cách làm: lịch refinement/review cố định, SLA trả lời Q&A, proxy PO phía offshore chuẩn bị backlog, và thống nhất quyết định nào PO tự chốt, quyết định nào phải trình cấp trên.

**Q225. Proxy PO phía offshore là gì, rủi ro và cách kiểm soát?**
Proxy PO là người phía offshore (thường BrSE hoặc BA) đại diện PO hằng ngày: làm rõ yêu cầu, viết story/AC, trả lời câu hỏi của team trong phạm vi được ủy quyền. Rủi ro: tự quyết thay khách, đoán nghiệp vụ, thành điểm nghẽn. Kiểm soát: ① ma trận ủy quyền bằng văn bản (được quyết gì, phải hỏi gì), ② mọi quyết định ghi log để khách xem lại hằng tuần, ③ ưu tiên và chấp nhận cuối cùng vẫn thuộc PO thật.
> 💡 Câu "proxy PO không sở hữu ưu tiên, chỉ sở hữu sự rõ ràng của yêu cầu" rất đáng nói.

**Q226. BrSE có nên kiêm proxy PO hay Scrum Master không?**
BrSE kiêm proxy PO là hợp lý vì đã nắm nghiệp vụ, ngôn ngữ và là đầu mối với khách; nhưng phải giới hạn tải để không thành nút thắt, vd một BrSE phục vụ tốt khoảng một team 5–8 người (tham khảo). BrSE kiêm Scrum Master thì em hạn chế vì xung đột vai: BrSE đại diện yêu cầu, SM bảo vệ quy trình và team; khi áp lực, BrSE thường nghiêng về khách. Bắt buộc kiêm thì em nói rõ ở kickoff và theo dõi qua retro.

**Q227. Scrum Master khác PM truyền thống ở điểm cốt lõi nào?**
PM truyền thống lập kế hoạch, giao việc và điều phối; Scrum Master không giao việc mà phục vụ: coaching team tự quản, gỡ impediment, giúp PO quản backlog hiệu quả, giúp tổ chức hiểu và áp dụng Scrum. Thước đo của SM là team tự vận hành tốt hơn, không phải SM bận hơn. Khi chuyển từ PM sang SM, điều khó nhất là im lặng để team tự ra quyết định trong daily thay vì chỉ đạo.

**Q228. Mô hình ラボ型 và mô hình 請負 phân vai PO/SM/PM khác nhau ra sao?**
`ラボ型開発` (rabo-gata kaihatsu – team chuyên trách thuê theo tháng): khách thường giữ PO, offshore cung cấp team và SM, PM offshore lo capacity, chất lượng, nhân sự; phạm vi linh hoạt nên Scrum chạy tự nhiên. 請負 theo dự án: offshore chịu trách nhiệm kết quả nên PM offshore phải nắm chặt phạm vi, thay đổi và nghiệm thu; PO phía khách vẫn sắp ưu tiên nhưng trong khung phạm vi hợp đồng. Điều khoản hợp đồng chi tiết thuộc phần hợp đồng, ở đây chỉ là phân vai.

**Q229. Khách dự Sprint Review nhưng không bao giờ tham gia refinement. Bạn làm gì?**
① Xác nhận nguyên nhân: thiếu thời gian, chưa hiểu mục đích, hay nghĩ đó là việc của vendor; ② đề xuất định dạng nhẹ: 30 phút, gửi trước câu hỏi tiếng Nhật, PO chỉ chốt ưu tiên và trả lời câu đóng/mở; ③ cho khách thấy chi phí của việc vắng mặt bằng dữ liệu (số item bị chặn, số 手戻り sau review); ④ nếu vẫn không được, thỏa thuận proxy PO chuẩn bị và khách duyệt bất đồng bộ trong 2 ngày làm việc.
> 💡 Số liệu của chính dự án ("3 item bị đẩy sang sprint sau vì chưa có trả lời") thuyết phục khách Nhật hơn lý thuyết agile.

**Q230. Ai chịu trách nhiệm chất lượng trong Scrum Team — SM, PM hay QA?**
Theo Scrum, Developers chịu trách nhiệm chất lượng Increment theo DoD, cả team cùng sở hữu; QA là một kỹ năng trong team chứ không phải trạm kiểm cuối dây chuyền. Về hợp đồng, PM phía offshore vẫn chịu trách nhiệm cuối cùng với khách về chất lượng bàn giao. Em kết hợp hai lớp: team sở hữu chất lượng hằng ngày qua DoD, PM sở hữu quy trình QA và chỉ số chất lượng ở cấp dự án.

**Q231. Senior PM phụ trách 3 dự án Scrum cùng lúc thì nên tham gia event nào?**
Em không dự mọi event của 3 team. Ưu tiên: ① Sprint Review — thấy kết quả thật và gặp khách; ② phần Why–What của Sprint Planning khi có rủi ro phạm vi; ③ đọc kết quả và action retro thay vì ngồi dự, để team nói thật. Daily để SM lo; em theo dõi qua board, burndown và chỉ can thiệp khi chỉ báo lệch ngưỡng, vd Sprint Goal có nguy cơ trượt từ giữa sprint. Thời gian còn lại dành cho khách, nhân sự và rủi ro cấp dự án.

## 3.4 Kanban & flow

**Q232. Kanban khác Scrum ở những điểm chính nào?**
Kanban không có sprint, vai trò hay event bắt buộc; nó tập trung vào dòng chảy liên tục: trực quan hóa workflow, giới hạn WIP, quản lý và cải tiến flow bằng số liệu. Scrum cam kết theo sprint với Sprint Goal; Kanban kéo việc mới khi có chỗ trống. Scrum hay đo velocity, Kanban đo WIP, cycle time, throughput, work item age. Hai cách kết hợp được, vd Scrum dùng board có WIP limit.

**Q233. WIP limit là gì và đặt bao nhiêu là hợp lý?**
WIP limit là số việc tối đa được nằm trong một cột/trạng thái cùng lúc; chạm giới hạn thì phải hoàn thành việc đang dở trước khi kéo việc mới ("stop starting, start finishing"). Điểm khởi đầu tham khảo: bằng hoặc ít hơn số người làm cột đó, rồi điều chỉnh theo dữ liệu — vd nghẽn ở review thì hạ WIP cột dev. Mục đích là làm lộ bottleneck và giảm chuyển đổi ngữ cảnh.
> 💡 Nói "WIP limit làm lộ vấn đề chứ không tự giải quyết vấn đề" cho thấy bạn hiểu bản chất.

**Q234. Phân biệt lead time và cycle time.**
Lead time: từ khi yêu cầu được tạo hoặc cam kết đến khi giao cho khách — là thời gian khách cảm nhận. Cycle time: từ khi bắt đầu làm đến khi xong — phản ánh hiệu năng nội bộ team. Hai số chênh lớn nghĩa là việc nằm chờ lâu trong hàng đợi. Điểm bắt đầu/kết thúc phải thống nhất trước khi đo, nhất là với ticket 障害 (shougai – sự cố) có cam kết SLA với khách.

**Q235. Định luật Little nói gì và PM dùng nó thế nào?**
Little's Law (với hệ ổn định): cycle time trung bình = WIP trung bình / throughput trung bình. Ví dụ team có 20 việc dở, mỗi tuần xong 10 việc → mỗi việc trung bình mất khoảng 2 tuần. Muốn giảm cycle time mà không thêm người thì phải giảm WIP. Em dùng nó để giải thích với khách vì sao liên tục chèn việc gấp vào hàng làm mọi việc khác chậm lại.
> 💡 Minh họa bằng con số đơn giản giúp khách chưa quen agile hiểu ngay — đừng chỉ đọc công thức.

**Q236. Cumulative Flow Diagram (CFD) đọc như thế nào?**
CFD xếp chồng số lượng việc theo từng trạng thái theo thời gian. Khoảng cách dọc giữa các dải ≈ WIP tại thời điểm đó; khoảng cách ngang ≈ thời gian việc đi qua các trạng thái; độ dốc dải Done ≈ throughput. Dấu hiệu xấu: một dải phình to (bottleneck ở trạng thái đó), dải Done đi ngang (không giao được gì), tất cả dải cùng đi ngang (team bị chặn).

**Q237. Khi nào nên chọn Kanban thay Scrum trong dự án Nhật?**
Kanban hợp với 保守運用 (hoshu unyou – bảo trì, vận hành): việc đến không đoán trước (sự cố, yêu cầu nhỏ, câu hỏi), ưu tiên đổi hằng ngày, có SLA phản hồi. Scrum hợp với phát triển tính năng mới cần mục tiêu theo chu kỳ. Nhiều team em chọn kết hợp: Scrum cho phát triển, cộng một làn expedite kiểu Kanban riêng cho 障害 với WIP 1–2 để không phá sprint.

**Q238. Thiết kế classes of service cho team 保守 của khách sản xuất C như thế nào?**
Em chia 3–4 lớp theo chi phí của sự chậm trễ: ① Expedite – sự cố ảnh hưởng dây chuyền sản xuất, vượt hàng chờ, WIP 1; ② Fixed date – thay đổi theo hạn pháp lý/kế toán, ưu tiên theo hạn; ③ Standard – cải tiến thông thường, vào trước làm trước; ④ Intangible – nợ kỹ thuật, nâng version thư viện, giữ tỉ lệ cố định khoảng 10–20% capacity (tham khảo). Mỗi lớp có SLA phản hồi/xử lý thống nhất với khách và đo hằng tháng.
> 💡 Nhắc "phân bổ cố định cho intangible" cho thấy bạn nghĩ đến sức khỏe hệ thống dài hạn, không chỉ chạy theo ticket.

**Q239. Throughput và work item age dùng để dự báo như thế nào?**
Throughput (số việc xong mỗi tuần) cho phép dự báo "khi nào xong N việc" theo xác suất thay vì một ngày cứng, vd lấy dữ liệu 8–12 tuần gần nhất chạy Monte Carlo ra "85% khả năng xong trước ngày X". Work item age (việc đang làm đã bao lâu) là chỉ báo sớm: việc nào có tuổi vượt mốc cycle time phân vị 85% trong lịch sử thì SM/PM xem ngay. Dự báo kèm xác suất rất hợp với khách cần minh bạch.

**Q240. Team chuyển sang Kanban, khách lo lắng vì "không còn deadline". Bạn xử lý sao?**
① Xác nhận lo lắng cụ thể: khách cần ngày cho release hay cho báo cáo nội bộ; ② bổ sung nhịp: replenishment hằng tuần để khách chọn ưu tiên, demo 2 tuần/lần, báo cáo tháng; ③ cam kết bằng SLA theo class of service và dự báo xác suất từ throughput; ④ việc có hạn cố định đưa vào lớp fixed date. Kanban không bỏ cam kết — nó chuyển cam kết từ "danh sách việc" sang "mức dịch vụ đo được".

## 3.5 Ước lượng & metrics Agile

**Q241. Story point là gì và vì sao không nên quy đổi thẳng ra giờ?**
Story point là đơn vị tương đối đo độ lớn của item — gộp khối lượng, độ phức tạp và độ không chắc chắn — so với một story chuẩn của team. Quy đổi cứng "1 point = 8 giờ" làm mất lợi ích ước lượng tương đối và sinh áp lực "thực tế vượt giờ". Nhưng khách Nhật thường cần 人月 (ningetsu – người-tháng) cho ngân sách; em quy đổi ở cấp release bằng số sprint × chi phí team, không quy đổi từng story.
> 💡 Chuẩn bị sẵn cách nói chuyện point ↔ 人月 với khách — đây là câu hỏi thực tế, không chỉ lý thuyết.

**Q242. Planning poker diễn ra thế nào và hay sai ở đâu?**
Mỗi người chọn lá bài theo dãy kiểu Fibonacci (1, 2, 3, 5, 8, 13…), lật cùng lúc; người chọn cao nhất và thấp nhất giải thích, rồi chọn lại đến khi hội tụ. Mục tiêu là làm lộ những cách hiểu khác nhau, không phải ra con số. Lỗi hay gặp: lead/BrSE nói số trước gây neo (anchoring), PM ép số, item quá lớn (≥ 13) không tách, thành viên trẻ ngại phản biện — em để người ít kinh nghiệm giải thích trước.

**Q243. Velocity dùng để làm gì và không được dùng để làm gì?**
Velocity là tổng point Done mỗi sprint, dùng để ① team tự lên kế hoạch sprint, ② PO dự báo release theo khoảng, vd trung bình 3–5 sprint gần nhất kèm min/max. Không dùng để so sánh giữa các team (point mỗi team một thang), đánh giá năng suất cá nhân hay làm KPI ép tăng. Velocity bị biến thành KPI sẽ dẫn đến lạm phát point — số tăng nhưng giá trị giao không đổi.
> 💡 Nhắc định luật Goodhart (chỉ số thành mục tiêu thì mất giá trị đo) là điểm cộng ở câu này.

**Q244. Ban lãnh đạo muốn so sánh velocity giữa 3 team offshore để đánh giá. Bạn phản hồi thế nào?**
Em giải thích velocity là thước đo nội bộ: point của team A không cùng đơn vị với team B, so sánh sẽ kéo theo lạm phát point và hành vi đối phó. Em đề xuất bộ chỉ số so sánh được: ① tỉ lệ đạt Sprint Goal, ② lead time cho cùng loại việc, ③ chất lượng — bug lọt sau release, 手戻り, ④ mức hài lòng khách qua khảo sát định kỳ. Lãnh đạo cần quản lý; việc của PM là đưa đúng thước đo, không chỉ nói "không".

**Q245. Burndown và burnup khác nhau thế nào? Khi nào nên dùng burnup?**
Burndown cho thấy công việc còn lại giảm dần về 0; đơn giản nhưng khi phạm vi tăng, đường đi ngang và khó biết là team chậm hay việc tăng. Burnup có hai đường: tổng phạm vi và phần đã xong — thấy rõ scope creep. Với khách hay thêm yêu cầu, em dùng burnup cấp release để thảo luận đánh đổi: "phạm vi tăng 20%, ngày dự báo lùi 2 sprint; muốn giữ ngày thì bỏ item nào?".
> 💡 Burnup là công cụ đàm phán phạm vi rất mạnh — kể một lần bạn đã dùng nó với khách.

**Q246. Predictability (độ tin cậy dự báo) đo như thế nào?**
Cách đơn giản: tỉ lệ point hoặc item Done so với cam kết đầu sprint, và tỉ lệ sprint đạt Sprint Goal. Ngưỡng tham khảo em dùng: ổn định 80–100% là tốt; dưới 70% liên tục là kế hoạch quá lạc quan hoặc bị gián đoạn nhiều; thường xuyên trên 100% là team đang để dự phòng quá dày. Điều quan trọng là xu hướng ổn định, vì khách Nhật đánh giá vendor qua độ tin cậy của lời hứa hơn là tốc độ.

**Q247. Khách yêu cầu "tăng velocity 20% từ sprint tới". Bạn trả lời thế nào?**
① Hỏi lại mục tiêu thật: giao tính năng X sớm hơn hay giảm chi phí; ② giải thích velocity tăng theo mệnh lệnh thường chỉ là đổi cách ước lượng hoặc hy sinh chất lượng, sau đó quay lại thành 手戻り; ③ đưa phương án thật: thu hẹp phạm vi theo ưu tiên, gỡ trở ngại (chờ Q&A, môi trường test), thêm người kèm thời gian ramp-up, hoặc tách release; ④ cùng khách theo dõi lead time và tỉ lệ đạt goal thay cho velocity.

**Q248. #NoEstimates là gì? Có áp dụng được cho dự án Nhật không?**
Cách tiếp cận #NoEstimates giảm hoặc bỏ ước lượng từng item, thay bằng tách item về kích thước tương đương rồi đếm số item và dùng throughput để dự báo. Ưu điểm: tiết kiệm thời gian, ít tranh cãi. Với khách Nhật cần 見積 (mitsumori – báo giá/ước lượng) cho ngân sách và 稟議, em không bỏ ước lượng ở cấp hợp đồng; bên trong team có thể dùng đếm item cho 保守 hoặc khi item đã đều cỡ.

**Q249. Làm sao dự báo release khi chưa có velocity (team mới)?**
① Ước velocity ban đầu từ capacity: số người × ngày khả dụng × hệ số tập trung khoảng 60–70% (tham khảo), rồi thử lên kế hoạch sprint đầu xem team nhận được bao nhiêu point; ② tham chiếu dữ liệu team tương tự nếu có; ③ báo khách dự báo dạng khoảng rộng và cam kết thu hẹp sau 3 sprint khi có velocity thật. Em ghi rõ giả định trong kế hoạch để con số đầu tiên không bị coi là lời hứa.
> 💡 "Cone of uncertainty — cam kết thu hẹp khoảng dự báo sau 3 sprint" vừa trung thực vừa giữ được niềm tin khách.

**Q250. Có nên gán story point cho bug và việc kỹ thuật không?**
Có hai trường phái: ① gán point cho mọi việc để velocity phản ánh tổng capacity; ② không gán cho bug để velocity chỉ phản ánh giá trị mới — bug làm velocity giảm chính là tín hiệu chất lượng. Em chọn theo mục đích dự báo: bug phát sinh đều thì không gán point và dành khoảng 10–15% capacity (tham khảo); việc lớn do khách đổi yêu cầu thì estimate như story để minh bạch chi phí. Quan trọng là nhất quán trong một team.

**Q251. Báo cáo agile hằng tuần cho khách Nhật nên có gì?**
Một trang, tiếng Nhật: ① Sprint Goal và trạng thái 達成 (tassei – đạt)/未達 (mitatsu – chưa đạt) kèm lý do, ② burnup release với ngày dự báo dạng khoảng, ③ chất lượng: bug mới/đóng, bug lọt sau release, ④ rủi ro và việc cần khách quyết, có hạn trả lời, ⑤ thay đổi phạm vi trong tuần. Tránh đưa velocity thô vì khách dễ hiểu thành năng suất. Màu xanh/vàng/đỏ có tiêu chí rõ, vd đỏ khi ngày dự báo lệch quá 1 sprint (tham khảo).

## 3.6 Hybrid: Water-Scrum-Fall & agile trong hợp đồng cố định

**Q252. Water-Scrum-Fall là gì? Tốt hay xấu?**
Đây là mô hình rất phổ biến: phần đầu kiểu waterfall (要件定義, ngân sách, phê duyệt), phần giữa phát triển theo sprint, phần cuối kiểu waterfall (総合テスト, 受入テスト, release lớn). Nó không xấu nếu có chủ đích, vì hợp với tổ chức cần ngân sách năm và kiểm soát release. Nó xấu khi phần giữa không có feedback của khách và test dồn cuối — chỉ là waterfall đổi tên. Câu em dùng để kiểm: khách có thấy phần mềm chạy được trước 総合テスト không?
> 💡 Nói thẳng "phần lớn dự án Nhật thực tế là hybrid" cho thấy bạn hiểu thực tiễn, không lý tưởng hóa agile.

**Q253. Làm agile trong hợp đồng 請負 giá cố định như thế nào?**
請負 cố định phạm vi, giá và 納期 (nouki – hạn giao hàng), mâu thuẫn với phạm vi linh hoạt của agile. Cách làm: ① cố định giá và ngày, linh hoạt phạm vi trong khung ưu tiên MoSCoW, Must chiếm khoảng ≤ 60% effort (tham khảo); ② cơ chế đổi item cùng kích thước không tính phát sinh; ③ chia hợp đồng theo release/phase nhỏ; ④ vẫn chạy sprint nội bộ để minh bạch tiến độ dù hợp đồng tính theo 成果物. Điều khoản chi tiết thuộc phần hợp đồng.

**Q254. Khách muốn agile nhưng cần ngân sách và 納期 cố định. Bạn đề xuất mô hình nào?**
Em đề xuất "cố định thời gian và chi phí, linh hoạt phạm vi": ① workshop đầu dựng product backlog thô và estimate theo khoảng; ② ngân sách = số sprint × chi phí team, ngày release cố định; ③ nhóm Must được cam kết, Should/Could làm theo khả năng; ④ review 2 tuần/lần để khách đánh đổi phạm vi dựa trên burnup; ⑤ điểm hiệu chỉnh sau 2–3 sprint đầu để cả hai cập nhật dự báo. Khách giữ được ngân sách, team giữ được chất lượng.

**Q255. Hợp đồng 準委任 khác 請負 thế nào khi chạy agile?**
準委任契約 (jun-inin keiyaku – hợp đồng ủy thác, trả theo công sức) không buộc hoàn thành một 成果物 cố định nên hợp tự nhiên với agile và ラボ型; mẫu hợp đồng phát triển agile do IPA Nhật công bố cũng theo hướng 準委任. Rủi ro là khách trả theo tháng nhưng kỳ vọng kết quả như khoán. Em làm rõ bằng văn bản: vendor chịu trách nhiệm thực thi đúng quy trình và chất lượng theo DoD, còn ưu tiên và phạm vi do PO phía khách quyết.

**Q256. Chia release trong dự án hybrid như thế nào để giảm rủi ro?**
① Release 1 là khung xương chạy end-to-end cho luồng nghiệp vụ chính, vd tra cứu hợp đồng của khách bảo hiểm B; ② mỗi release 2–3 tháng, có 総合テスト rút gọn và 受入テスト riêng thay vì dồn cuối; ③ phần rủi ro kỹ thuật (tích hợp hệ thống cũ, hiệu năng) đưa vào release sớm; ④ mỗi release là một mốc nghiệm thu nhỏ. Cách này biến dự án 12 tháng thành 4–5 lần "tập dượt" nghiệm thu.

**Q257. Trong hybrid, tài liệu 基本設計 nên viết trước toàn bộ hay theo sprint?**
Em chia hai lớp: ① viết trước phần khung ổn định — kiến trúc, mô hình dữ liệu cốt lõi, danh sách màn hình/chức năng, interface với hệ thống ngoài — vì nhiều team và hệ thống phụ thuộc vào nó; ② chi tiết màn hình/logic viết theo kiểu just-in-time, đi trước phát triển 1 sprint, cập nhật sau review. Thỏa thuận với khách: tài liệu được chốt phiên bản theo release, không phải chốt trước khi code.
> 💡 "Tài liệu just-in-time, đi trước dev 1 sprint" là câu trả lời cân bằng mà khách Nhật chấp nhận được.

**Q258. Đưa 総合テスト và 受入テスト kiểu Nhật vào nhịp sprint như thế nào?**
① Trong sprint: DoD gồm unit test, integration test và test theo AC trên staging; ② cuối mỗi release: một giai đoạn 総合テスト ngắn cho regression, hiệu năng, liên kết hệ thống — Scrum thuần coi "hardening sprint" là dấu hiệu DoD chưa đủ, nên em coi đây là tạm thời và thu ngắn dần bằng automation regression; ③ 受入テスト do khách làm theo release, offshore hỗ trợ dữ liệu và kịch bản. Độ dài giai đoạn hardening là chỉ số em theo dõi qua từng release.

**Q259. Quản lý thay đổi trong hybrid khác waterfall thế nào?**
Waterfall: mọi thay đổi sau phê duyệt đi qua 変更管理 (henkou kanri – quản lý thay đổi) chính thức, đánh giá ảnh hưởng, có thể tính phát sinh. Hybrid chia 2 loại: ① thay đổi trong backlog chưa bắt đầu — PO tự sắp xếp, đổi item cùng kích thước, không cần CR; ② thay đổi vượt khung — thêm epic, đổi kiến trúc, đổi ngày release, sửa thứ đã nghiệm thu — đi CR chính thức. Ngưỡng phân loại thống nhất từ kickoff để không tranh cãi từng lần.

**Q260. Khách liên tục đổi ưu tiên giữa sprint trong hợp đồng giá cố định. Bạn xử lý thế nào?**
① Đo fact: bao nhiêu lần đổi, ảnh hưởng bao nhiêu point và ngày; ② ngay lập tức bảo vệ Sprint Goal — việc mới vào backlog sprint sau, trừ việc khẩn thì đổi item cùng kích thước và ghi lại; ③ báo khách theo 報連相 (hourensou – báo cáo, liên lạc, thảo luận) kèm burnup cho thấy ngày dự báo dịch chuyển; ④ giải pháp gốc: rút sprint xuống 1 tuần nếu ưu tiên thật sự biến động, hoặc mở làn Kanban riêng cho việc khẩn có WIP giới hạn.
> 💡 Đề xuất rút ngắn sprint thay vì cấm khách đổi ý — cho thấy bạn thích ứng chứ không cứng nhắc.

**Q261. Hybrid dễ "lấy cái tệ của cả hai". Đó là gì và tránh thế nào?**
Rủi ro: ① tài liệu dày như waterfall nhưng phạm vi trôi như agile thiếu kiểm soát; ② sprint không ra Increment chạy được, test dồn cuối; ③ khách vừa đòi CR chính thức vừa muốn đổi ý tự do; ④ team vừa làm báo cáo waterfall vừa dự đủ event Scrum, quá tải họp. Cách tránh: viết một "operating model" 1 trang ngay kickoff — phần nào cố định, phần nào linh hoạt, ai quyết, tài liệu nào bắt buộc — và xem lại sau release đầu.

**Q262. Dự án ngân hàng A bắt buộc waterfall ở core, nhưng app mobile muốn agile. Bạn phối hợp hai track thế nào?**
① Thiết kế sớm interface (API contract) giữa core và mobile, chốt theo version, có mock/stub để mobile chạy sprint không phải chờ core; ② lịch tích hợp cố định theo milestone của core, mobile lập kế hoạch release bám các mốc đó; ③ một bảng rủi ro/dependency chung, họp đồng bộ hằng tuần giữa hai lead; ④ 結合テスト và 総合テスト liên kết chạy chung theo lịch waterfall. Nguyên tắc: track nhanh không phụ thuộc trực tiếp vào track chậm, chỉ qua contract.
> 💡 Từ khóa "tách phụ thuộc qua contract + mock" là điều interviewer có nền kỹ thuật muốn nghe.

## 3.7 Agile với khách hàng Nhật

**Q263. Vì sao khách Nhật truyền thống thường e ngại agile?**
Thường vì: ① văn hóa tài liệu và 合意形成 (goui keisei – tạo đồng thuận), mọi thứ cần duyệt trước; ② ngân sách và 稟議 theo năm, cần con số cố định; ③ hiểu "agile = không kế hoạch, không tài liệu"; ④ trách nhiệm chất lượng phải rõ theo hợp đồng; ⑤ từng gặp vendor "agile" giao sản phẩm thiếu ổn định. Hiểu đúng từng nỗi lo thì mới thuyết phục được: trả lời mỗi nỗi lo bằng một cơ chế kiểm soát cụ thể.

**Q264. Bạn thuyết phục khách bảo hiểm B vốn quen waterfall chuyển sang agile như thế nào?**
Em không bán chữ "agile" mà bán kết quả: ① bắt đầu bằng pilot nhỏ, rủi ro thấp (1 module, 2–3 tháng); ② giữ những gì khách cần — ngân sách cố định, báo cáo tiến độ, tài liệu bàn giao — và cho thấy phần thêm vào: demo phần mềm chạy được mỗi 2 tuần, phát hiện hiểu sai sớm; ③ đo trước/sau: số 手戻り, thời gian phản hồi thay đổi; ④ mở rộng khi có số liệu. Dùng từ 反復型開発 (hanpuku-gata kaihatsu – phát triển lặp) đôi khi dễ được chấp nhận hơn.
> 💡 Pilot nhỏ + số liệu của chính khách là cách thuyết phục bền vững nhất với tổ chức Nhật.

**Q265. Sprint Review với khách Nhật nên tổ chức thế nào để hiệu quả?**
① Gửi trước 1–2 ngày bằng tiếng Nhật: agenda, Sprint Goal, item sẽ demo, điểm cần khách quyết; ② demo trên staging với dữ liệu gần thật, theo kịch bản nghiệp vụ chứ không theo từng ticket; ③ hỏi câu cụ thể ("thứ tự thao tác này đúng với bộ phận nghiệp vụ chưa?") vì khách Nhật ít phản đối trực tiếp tại họp; ④ gửi 議事録 trong 24 giờ, liệt kê feedback → item backlog để khách xác nhận.
> 💡 Khách im lặng trong review không có nghĩa là đồng ý — luôn chừa kênh phản hồi sau họp.

**Q266. Khách hiếm khi góp ý tại Sprint Review, sau đó lại gửi email rất nhiều feedback. Làm sao thu feedback sớm hơn?**
① Cho khách xem sớm, không đợi review: link staging và video ngắn cho item xong giữa sprint; ② trong review, hỏi dạng có/không hoặc chọn A/B thay vì "có ý kiến gì không?"; ③ mời người dùng nghiệp vụ thật, không chỉ bộ phận IT của khách; ④ dùng bảng feedback tiếng Nhật có hạn 2–3 ngày; ⑤ coi feedback sau họp là bình thường do 合意形成 nội bộ của khách, chừa sẵn capacity xử lý thay vì phàn nàn.

**Q267. Trình bày Sprint Review bằng tiếng Nhật cần lưu ý gì về ngôn ngữ?**
① Nói kết luận trước theo kiểu 結論から (ketsuron kara – bắt đầu từ kết luận); ② nói rõ item nào 完了 (kanryou – hoàn thành) theo DoD, item nào 未完了 (mikanryou – chưa xong) kèm lý do và kế hoạch, không dùng "gần xong"; ③ dùng thuật ngữ nghiệp vụ của khách thay vì thuật ngữ Scrum; ④ không hứa miệng tại họp — nói 持ち帰って検討します (mochikaette kentou shimasu – xin mang về xem xét) rồi trả lời bằng văn bản; ⑤ BrSE chuẩn bị script và glossary trước cho người demo.

**Q268. Khách yêu cầu tài liệu thiết kế đầy đủ như waterfall dù dự án chạy Scrum. Bạn phản ứng thế nào?**
① Hỏi mục đích thật của tài liệu: phục vụ 保守 sau này, audit nội bộ hay 稟議; ② đề xuất tài liệu "đủ và sống": giữ tài liệu có giá trị lâu dài (kiến trúc, dữ liệu, API, đặc tả màn hình), cập nhật theo sprint và đưa vào DoD; bỏ tài liệu trung gian chỉ để duyệt; ③ ước lượng effort tài liệu minh bạch trong backlog; ④ thống nhất mẫu tài liệu từ đầu. Tài liệu là yêu cầu chính đáng, không phải "phản agile".
> 💡 Agile Manifesto nói phần mềm chạy được được coi trọng HƠN tài liệu, không phải "không cần tài liệu" — trích đúng là điểm cộng.

**Q269. Khách sản xuất C muốn mọi thay đổi phải được duyệt bằng văn bản, kể cả trong sprint. Làm sao giữ tốc độ?**
① Tôn trọng vì đó là kiểm soát nội bộ của khách; ② phân loại theo mức ảnh hưởng: thay đổi nhỏ (câu chữ UI, sắp lại item chưa làm) gom duyệt theo lô hằng tuần, thay đổi lớn duyệt riêng; ③ dùng trạng thái "khách xác nhận" ngay trên ticket thay vì công văn; ④ thống nhất SLA duyệt 2 ngày làm việc, quá hạn thì item chuyển sang sprint sau. Tốc độ đến từ duyệt theo lô, không phải từ bỏ bước duyệt.

**Q270. Người phụ trách phía khách đồng ý agile, nhưng cấp trên của họ vẫn đánh giá theo WBS và % tiến độ. Bạn làm gì?**
Em giúp người phụ trách "dịch" agile sang ngôn ngữ cấp trên: ① lập bản đồ epic ↔ hạng mục WBS/chức năng trong hợp đồng; ② báo % hoàn thành theo phạm vi Done trên burnup thay vì % công sức đã bỏ ra; ③ mốc release ánh xạ vào mốc kế hoạch tổng; ④ chuẩn bị tài liệu để họ dùng khi 根回し (nemawashi – vận động, thống nhất trước) trong nội bộ. Giúp người phụ trách thành công trong tổ chức của họ là cách bền nhất để giữ agile.

**Q271. Có nên dùng tiếng Nhật cho toàn bộ backlog khi team offshore không giỏi tiếng Nhật?**
Em phân theo người đọc: ① thứ khách đọc và quyết — tiêu đề story, AC, Q&A, báo cáo — viết tiếng Nhật, có BrSE kiểm; ② thảo luận kỹ thuật nội bộ, sub-task có thể dùng tiếng Anh/Việt; ③ duy trì glossary nghiệp vụ Nhật–Anh–Việt chung. Dịch máy hỗ trợ được, nhưng AC phải được người biết tiếng Nhật xác nhận. Mục tiêu: không tồn tại "hai sự thật" giữa bản tiếng Nhật và cách team hiểu.

**Q272. Làm thế nào để khách Nhật tin vào ước lượng dạng khoảng thay vì một con số?**
① Giải thích bằng lịch sử của chính dự án họ — các lần ước lượng trước lệch bao nhiêu; ② đưa con số kèm mức tin cậy ("85% xong trước ngày X, 50% trước ngày Y") thay vì khoảng mơ hồ; ③ cam kết cập nhật dự báo mỗi sprint và báo ngay khi lệch quá ngưỡng, vd quá 1 sprint; ④ giữ đều các lời hứa nhỏ để tích lũy uy tín. Khách Nhật không ghét con số dạng khoảng, họ ghét bất ngờ; cái họ cần là 見通し (mitooshi – triển vọng dự báo) đáng tin.

**Q273. Khách muốn tham gia daily scrum mỗi ngày qua video call. Có nên đồng ý?**
Có thể đồng ý nhưng thiết kế lại: ① khách tham gia với vai quan sát, hoặc với vai PO trả lời nhanh câu hỏi đang chặn, không phải người nhận báo cáo; ② giữ 15 phút, nói tiếng Nhật đơn giản hoặc có BrSE tóm tắt; ③ nếu daily biến thành buổi khách giao việc, kiểm tra từng người, em đề xuất buổi sync 15 phút 2–3 lần/tuần riêng với PO và trả daily lại cho team. Lý do cần nói rõ: team phải được nêu vấn đề thẳng thắn mà không sợ mất mặt trước khách.

## 3.8 Scaling nhiều team offshore

**Q274. Scrum of Scrums vận hành thế nào và khi nào là đủ?**
Mỗi team cử đại diện — thường là người nắm dependency kỹ thuật, không nhất thiết là SM — họp 2–3 lần/tuần, 15–30 phút: việc vừa làm ảnh hưởng team khác, việc sắp làm, vướng mắc, chỗ sắp "đụng" nhau. Đủ dùng khi có 2–4 team chung một sản phẩm, dependency vừa phải, kèm board dependency chung và refinement liên team. Khi cần đồng bộ kế hoạch quý, ngân sách và nhiều PO thì phải lên khung lớn hơn.

**Q275. SAFe là gì và PI Planning diễn ra thế nào?**
SAFe (Scaled Agile Framework) gom nhiều team thành Agile Release Train (ART), thường khoảng 50–125 người, đồng bộ theo PI — Program Increment, bản mới gọi là Planning Interval — thường 8–12 tuần. PI Planning là sự kiện khoảng 2 ngày cho toàn ART: phía business trình bày tầm nhìn và ưu tiên; các team lập kế hoạch, ước lượng, đánh dấu dependency trên program board, cam kết PI Objectives và bỏ phiếu mức tự tin. Người điều phối train là RTE (Release Train Engineer).

**Q276. Tổ chức PI Planning khi team ở Đà Nẵng và khách ở Tokyo có gì khó?**
Khó ở: ① Nhật đi trước Việt Nam 2 giờ, khung giờ làm việc trùng nhau chỉ khoảng 6 giờ/ngày nếu trừ giờ nghỉ trưa lệch nhau; ② ngôn ngữ, cần BrSE thông dịch song song; ③ khách ngại cam kết trực tiếp tại chỗ. Cách làm: chuẩn bị trước 2 tuần (feature đã refine, dependency sơ bộ), chia thành 2–3 ngày ngắn hơn, dùng board online, bỏ phiếu tự tin ẩn danh. Nếu ngân sách cho phép, PI đầu tiên nên gặp trực tiếp.

**Q277. LeSS khác SAFe thế nào?**
LeSS (Large-Scale Scrum) giữ Scrum gần nguyên bản: một Product Owner, một Product Backlog, một DoD, một Sprint chung cho nhiều team (bản cơ bản khoảng 2–8 team), Sprint Review chung và retro tổng thể; team là feature team. SAFe thêm nhiều lớp vai trò, cấp độ và sự kiện (ART, PI, RTE, portfolio). LeSS đòi tổ chức thay đổi cấu trúc mạnh; SAFe dễ gắn vào tổ chức lớn có phân cấp sẵn nhưng nặng và dễ thành thủ tục hành chính.

**Q278. Chi nhánh Đà Nẵng có 4 team cùng làm cho một khách tài chính. Bạn chọn mô hình scale nào?**
Em bắt đầu nhẹ nhất có thể: một Product Backlog, một PO phía khách cộng proxy PO, sprint đồng bộ cùng ngày bắt đầu/kết thúc, refinement liên team, Scrum of Scrums 2–3 lần/tuần, Sprint Review chung — gần tinh thần LeSS/Nexus. Chỉ lên SAFe khi khách đã dùng SAFe nội bộ hoặc cần đồng bộ nhiều train và ngân sách theo quý. Tiêu chí để nâng cấp: số dependency chặn liên team mỗi sprint và tỉ lệ item trễ vì phụ thuộc.
> 💡 "Scale nhẹ nhất có thể, chỉ thêm khung khi số liệu chứng minh cần" là tư duy senior mà interviewer muốn nghe.

**Q279. Khi nào KHÔNG nên áp dụng SAFe?**
① Quy mô nhỏ, vài team — chi phí vai trò và sự kiện lớn hơn lợi ích; ② sản phẩm tách được thành nhiều phần độc lập ít dependency — tách kiến trúc tốt hơn scale quy trình; ③ lãnh đạo chỉ muốn đổi tên quy trình cũ mà không trao quyền cho team; ④ khách không tham gia PI Planning — kế hoạch thành kế hoạch nội bộ của vendor. Scale quy trình là bước sau cùng; trước hết giảm dependency bằng feature team và kiến trúc module rõ ràng.

**Q280. Feature team hay component team — chọn thế nào khi có nhiều team offshore?**
Component team (team FE, team BE, team DB) dễ lập từ cơ cấu kỹ năng sẵn có, nhưng mỗi tính năng phải đi qua nhiều team → chờ nhau, không team nào tự giao được Increment trọn vẹn. Feature team đa kỹ năng giao tính năng end-to-end, giảm phối hợp nhưng đòi kiến thức rộng và kiến trúc rõ. Em ưu tiên feature team, giữ một nhóm chuyên gia nhỏ (hạ tầng, bảo mật) hỗ trợ nhiều team theo kiểu enabling team.

**Q281. Quản lý dependency giữa các team offshore với team onsite và khách như thế nào?**
① Trực quan hóa: board dependency ghi ai cần gì, khi nào, trạng thái; ② phát hiện sớm ở refinement liên team — item có dependency chưa giải quyết không được vào sprint; ③ giảm dependency từ gốc bằng API contract, mock và tách module; ④ dependency với khách (dữ liệu test, môi trường, quyết định) quản lý như rủi ro có owner và hạn, báo cáo hằng tuần. Chỉ số em theo dõi: số item bị chặn quá 2 ngày vì phụ thuộc bên ngoài.

**Q282. Team ở Đà Nẵng và team ở một site khác cùng làm một sản phẩm nhưng "văn hóa Scrum" khác nhau. Bạn đồng bộ thế nào?**
Em chốt "khung tối thiểu bắt buộc" và để phần còn lại tự do. Bắt buộc chung: DoD, nhịp sprint, cách estimate cho release, công cụ, định dạng báo cáo khách. Tự do: cách chạy daily, format retro, kỹ thuật nội bộ. Bổ sung: luân chuyển người giữa hai site 1–2 tuần, retro liên site mỗi quý, community of practice cho SM. Mục tiêu là khách nhìn thấy một vendor thống nhất, không phải hai công ty.

## 3.9 Retrospective & cải tiến liên tục

**Q283. Sprint Retrospective nên có cấu trúc thế nào để không nhàm chán?**
Khung 5 bước phổ biến: ① set the stage (check-in), ② gather data (sự kiện, số liệu sprint), ③ generate insights (tìm nguyên nhân), ④ decide what to do (chọn 1–3 action), ⑤ close. Đổi format sau vài sprint: KPT, Start/Stop/Continue, 4Ls, Sailboat, Mad/Sad/Glad, timeline. Luôn mở đầu bằng việc xem lại action của retro trước — retro không có follow-up là lý do lớn nhất khiến team chán retro.
> 💡 Nói "mở đầu bằng review action cũ" cho thấy bạn quan tâm kết quả, không chỉ hình thức.

**Q284. KPT là gì và vì sao phổ biến ở Nhật?**
KPT (Keep – Problem – Try) là format 振り返り (furikaeri – nhìn lại) rất phổ biến ở công ty Nhật: Keep là điều làm tốt cần giữ, Problem là vấn đề gặp phải, Try là điều thử ở lần sau để giải quyết Problem hoặc phát huy Keep. Nó đơn giản, dễ cho người mới và gần tư duy 改善 (kaizen – cải tiến liên tục). Bẫy hay gặp: Try chung chung kiểu "cẩn thận hơn"; em yêu cầu mỗi Try có owner, hạn và cách kiểm đã làm hay chưa.

**Q285. Làm sao biến kết quả retro thành hành động thật?**
① Chọn tối đa 1–3 action, viết cụ thể, có owner, có hạn, đo được — vd "từ sprint 12, PR trên 400 dòng phải tách; SM thống kê cuối sprint"; ② đưa action vào Sprint Backlog như một item, không để trong trang ghi chú; ③ đầu retro sau kiểm lại: làm chưa, có hiệu quả không, giữ hay bỏ; ④ action vượt quyền team (môi trường, phía khách) thì SM/PM nhận và báo lại tiến độ. Tỉ lệ action hoàn thành là chỉ số em dùng để đo chính retro.

**Q286. Team offshore ít nói trong retro, chỉ bảo "không có vấn đề gì". Bạn làm gì?**
① Tạo an toàn tâm lý: PM/lead vắng mặt hoặc nói sau cùng, nhắc Prime Directive — ai cũng đã làm tốt nhất có thể với thông tin lúc đó; ② cho viết sticky ẩn danh trước khi nói, rồi dot-voting; ③ mở đầu bằng dữ liệu (bug lọt, item trượt, giờ OT) để bàn về sự kiện chứ không về cá nhân; ④ chia nhóm 2–3 người; ⑤ xử lý ngay ý kiến đầu tiên để team thấy nói ra là có thay đổi.
> 💡 Team im lặng thường vì lần trước nói ra mà không có gì thay đổi — sửa nguyên nhân đó trước khi đổi format.

**Q287. Retrospective liên hệ với Kaizen và PDCA như thế nào?**
Retro là vòng 改善 ở quy mô sprint: cải tiến nhỏ, liên tục, do chính người làm đề xuất. Mỗi action retro là một vòng PDCA: Plan (thử gì, kỳ vọng gì), Do (áp dụng trong sprint), Check (retro sau đo kết quả), Act (chuẩn hóa nếu hiệu quả, bỏ nếu không). Khi báo cáo với khách Nhật, em trình bày retro như hoạt động 振り返り và 改善 của team kèm vài action tiêu biểu — dễ được đánh giá cao vì khớp văn hóa cải tiến họ quen.

**Q288. Khi nào nên mời khách tham gia retrospective?**
Sprint retro là của Scrum Team; nếu PO là người phía khách thì PO đã là thành viên. Với stakeholder khác của khách, em tổ chức retro chung theo release hoặc theo quý, tập trung vào cách phối hợp: tốc độ trả lời Q&A, chất lượng yêu cầu, quy trình review. Điều kiện: đã có đủ tin cậy và có người điều phối trung lập; kết quả luôn hai chiều — việc vendor cải tiến và việc khách cải tiến.

**Q289. Phân biệt retrospective với なぜなぜ分析 sau sự cố.**
Retro là cải tiến định kỳ về cách làm việc, phạm vi rộng, không cần chờ có vấn đề. なぜなぜ分析 (nazenaze bunseki – hỏi "tại sao" lặp lại, thường 5 lần) là phân tích sâu một sự cố cụ thể để tìm nguyên nhân gốc, dẫn tới 再発防止 và 横展開, thường có báo cáo gửi khách. Sự cố nghiêm trọng thì phân tích ngay, không đợi retro; retro dùng để kiểm lại biện pháp đã áp dụng có hiệu quả không.
> 💡 Dừng phân tích ở nguyên nhân quy trình/hệ thống, đừng dừng ở "do A bất cẩn" — khách Nhật sẽ hỏi tiếp "vì sao quy trình để lọt".

**Q290. Làm sao đo được retro có hiệu quả hay không?**
Em theo dõi 3 nhóm: ① đầu ra — tỉ lệ action hoàn thành đúng hạn, mục tiêu tham khảo ≥ 70%; ② tác động — chỉ số mà action nhắm tới có cải thiện không, vd thời gian review PR, bug lọt; ③ sức khỏe — vấn đề cũ có lặp lại không và mức hài lòng của team qua khảo sát ngắn. Một Problem lặp lại 3 sprint liên tiếp là dấu hiệu action quá yếu hoặc vấn đề nằm ngoài quyền team — lúc đó PM phải escalate.

## 3.10 Câu kiểu PMI-ACP & câu senior

**Q291. Agile Manifesto có 4 giá trị nào? Hiểu sai phổ biến nhất là gì?**
Bốn giá trị: con người và tương tác hơn quy trình và công cụ; phần mềm chạy được hơn tài liệu toàn diện; cộng tác với khách hàng hơn đàm phán hợp đồng; phản hồi thay đổi hơn bám theo kế hoạch. Câu kết: các mục bên phải vẫn có giá trị, nhưng mục bên trái được coi trọng hơn. Hiểu sai phổ biến nhất: "agile = không tài liệu, không kế hoạch, không hợp đồng". Với khách Nhật, nhấn mạnh câu kết này giúp gỡ nỗi lo ngay.
> 💡 Nhắc được câu "các mục bên phải vẫn có giá trị" cho thấy bạn đọc Manifesto thật, không học qua slide.

**Q292. "Fake agile" (agile hình thức) có những dấu hiệu nào?**
① Có đủ event nhưng không sprint nào ra Increment chạy được; ② Sprint Review là buổi đọc slide báo cáo; ③ PO không có quyền ưu tiên, mọi thứ đã chốt trong spec từ đầu; ④ velocity là KPI để ép team; ⑤ retro lặp lại cùng vấn đề không ai xử lý; ⑥ "agile" được dùng làm lý do để không viết tài liệu, không kiểm soát phạm vi. Khi tiếp quản dự án như vậy, em không tuyên bố "làm lại Scrum" mà chọn 1–2 dấu hiệu gây hại nhất để sửa trước.

**Q293. Đo giá trị (value) thay vì output trong dự án outsource như thế nào?**
Output là số story/point; value là thay đổi trong nghiệp vụ của khách. Cách đo: ① mỗi epic có giả thuyết giá trị và chỉ số nghiệp vụ thống nhất với PO, vd giảm thời gian xử lý hồ sơ của khách bảo hiểm B, giảm lỗi nhập liệu ở nhà máy của khách sản xuất C; ② đo sau release bằng dữ liệu khách cung cấp; ③ ưu tiên backlog theo giá trị/chi phí, vd WSJF hoặc ma trận value–effort. Vendor thường không có dữ liệu nghiệp vụ, nên phải thỏa thuận chia sẻ từ đầu.
> 💡 Câu này kiểm tra bạn nghĩ như "đối tác" hay "nhà thầu" — trả lời bằng chỉ số nghiệp vụ của khách.

**Q294. Servant leadership trong agile có nghĩa gì với một Senior PM?**
Là lãnh đạo bằng cách phục vụ: gỡ trở ngại, tạo môi trường để team tự quản và tự quyết, phát triển năng lực từng người, che chắn team khỏi áp lực không cần thiết — thay vì ra lệnh và kiểm soát chi tiết. Nó không có nghĩa là chiều mọi người hay né quyết định: khi team bế tắc hoặc rủi ro vượt quyền team, Senior PM vẫn phải quyết và chịu trách nhiệm. Scrum Guide 2020 dùng cụm "true leaders who serve" chính để nhấn mạnh điều này.

**Q295. Câu kiểu PMI-ACP: Giữa sprint, một developer báo item sẽ không kịp. Hành động ĐẦU TIÊN của Scrum Master là gì?**
Đáp án thường đúng theo tinh thần agile: để Developers cùng thảo luận tại Daily hoặc ngay sau đó, đánh giá tác động lên Sprint Goal và tự đề xuất cách xử lý — hỗ trợ nhau, tách item, hoặc cùng PO đàm phán lại phạm vi. Đáp án sai thường gặp: SM tự gán thêm người, báo ngay lên quản lý/khách, kéo dài sprint. Nguyên tắc chọn đáp án ACP: ưu tiên tự quản, minh bạch, cộng tác; tránh hành động mệnh lệnh khi team chưa được tham gia.
> 💡 Mẹo thi ACP: phân vân thì chọn đáp án "team cùng quyết + minh bạch với PO" thay vì đáp án PM/SM tự xử lý.

**Q296. Dự án Scrum chạy 6 tháng, velocity tăng đều nhưng khách phàn nàn chất lượng giảm. Bạn phân tích thế nào?**
① Xác nhận fact: bug lọt theo sprint, bug do sửa hỏng chỗ cũ (regression), độ phủ test, nợ kỹ thuật; ② giả thuyết thường gặp: DoD lỏng hoặc không được tuân thủ, point bị lạm phát, regression chưa tự động hóa; ③ hành động ngay: siết DoD, dành 1 sprint ưu tiên sửa bug mức cao, báo khách theo 報連相 kèm kế hoạch; ④ phòng ngừa: dành capacity cố định cho nợ kỹ thuật và automation, báo cáo chất lượng song song velocity. Velocity tăng mà chất lượng giảm nghĩa là team đang vay nợ.

**Q297. Trade-off: sprint 1 tuần hay 2 tuần cho team offshore làm với khách Nhật?**
Sprint 1 tuần: feedback nhanh, hợp khi yêu cầu biến động, nhưng chi phí event chiếm tỉ lệ cao, khách khó sắp lịch review hằng tuần và thiếu thời gian 合意形成. Sprint 2 tuần: cân bằng phổ biến, đủ thời gian cho Q&A qua lại. Sprint 3–4 tuần: hợp tổ chức ra quyết định chậm nhưng phát hiện vấn đề muộn. Em thường chọn 2 tuần, rút về 1 tuần ở giai đoạn đầu hoặc khi ưu tiên đổi mạnh, và giữ độ dài cố định để có số liệu ổn định.

**Q298. Khi nào agile là lựa chọn SAI, dù khách muốn?**
① Khách không thể cử PO hoặc người ra quyết định tham gia định kỳ — agile thiếu feedback chỉ là waterfall không tài liệu; ② hợp đồng 請負 phạm vi cứng và khách từ chối đánh đổi phạm vi; ③ hệ thống không thể test/release từng phần, vd phụ thuộc phần cứng hoặc môi trường test chỉ mở theo lịch; ④ team chưa có nền tảng kỹ thuật (CI, test tự động) để giao Increment mỗi sprint. Khi đó em đề xuất hybrid hoặc waterfall có vòng lặp, nêu lý do bằng văn bản thay vì chiều khách.
> 💡 Dám nói "không" có lý do với khách là phẩm chất Senior PM — interviewer đang kiểm tra đúng điều này.

**Q299. Làm sao chuyển một dự án đang chạy waterfall sang agile mà không làm khách mất niềm tin?**
① Không chuyển giữa một 工程 đang dở; chọn điểm chuyển tự nhiên như đầu phase hoặc release mới; ② thay đổi từng phần: trước tiên thêm demo định kỳ và backlog có ưu tiên, giữ nguyên báo cáo và tài liệu khách quen; ③ thống nhất bằng văn bản cái gì đổi, cái gì giữ, ai quyết; ④ đặt tiêu chí đánh giá sau 3 sprint (hài lòng, 手戻り, đúng hạn) và sẵn sàng quay lại nếu không đạt. Khách Nhật chấp nhận thay đổi khi nó có kế hoạch và có đường lui.

**Q300. Nếu được giao xây dựng cách làm agile cho một chi nhánh mới ở Đà Nẵng, bạn làm gì trong 90 ngày đầu?**
① Ngày 1–30: khảo sát dự án và khách hiện có, chọn 1–2 dự án pilot, thống nhất khung tối thiểu (DoD mẫu, nhịp sprint, công cụ, mẫu báo cáo tiếng Nhật); ② ngày 31–60: chạy pilot, đào tạo SM/BrSE, lập community of practice, đo baseline (đúng hạn, bug lọt, hài lòng khách); ③ ngày 61–90: review kết quả với lãnh đạo và khách, chuẩn hóa thành playbook, lập kế hoạch nhân rộng. Nguyên tắc: bắt đầu nhỏ, đo được, không áp một khuôn cho mọi khách.
> 💡 Gắn câu trả lời với lợi thế "setup chi nhánh mới ở Đà Nẵng" trong JD — biến câu hỏi chung thành điểm mạnh riêng.
