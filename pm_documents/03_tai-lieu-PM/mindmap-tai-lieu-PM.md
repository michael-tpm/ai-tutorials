---
title: Mindmap tài liệu PM
markmap:
  initialExpandLevel: 2
---

<!-- Mở bằng markmap (VS Code extension 'Markmap' hoặc markmap.js.org/repl). Bản tương tác: bang-tuan-hoan-tai-lieu-PM.html -->

# Tài liệu PM · 11 câu hỏi

## 1. Vì sao làm? (WHY)
### BC · Business Case
- ビジネスケース・企画書 (bijinesu kēsu, kikakusho)
- Trả lời: Dự án có đáng bỏ tiền không?
- Mẹo: BC = 'Bỏ tiền Có đáng?'
- Bẫy: Lợi ích không đo được ('tăng hiệu quả') nên sau dự án không ai kiểm được.
### PRP · Proposal
- 提案書 (teiansho)
- Trả lời: Vì sao khách nên chọn mình?
- Mẹo: Proposal là 'lời cầu hôn': nói về người kia trước, về mình sau.
- Bẫy: Nói về công ty mình quá nhiều, nói về vấn đề của khách quá ít.
### SOW · Statement of Work
- 作業範囲記述書・契約別紙 (sagyō han'i kijutsusho, keiyaku besshi)
- Trả lời: Theo hợp đồng, mình phải giao gì?
- Mẹo: SOW = 'Sổ Ước hẹn' với khách: ghi gì làm nấy.
- Bẫy: Không ghi 'ngoài phạm vi', nên mọi yêu cầu thêm đều thành 'đương nhiên phải có'.
### CHT · Project Charter
- プロジェクト憲章 (purojekuto kenshō)
- Trả lời: Ai cho phép dự án bắt đầu, PM có quyền gì?
- Mẹo: Charter = 'giấy khai sinh' của dự án.
- Bẫy: Không ghi quyền của PM, nên quyết định nhỏ nào cũng phải xin.

## 2. Làm gì? (WHAT)
### SS · Scope Statement
- スコープ記述書 (sukōpu kijutsusho)
- Trả lời: Dự án làm gì và KHÔNG làm gì?
- Mẹo: Scope Statement là 'hàng rào': vẽ rõ trong và ngoài.
- Bẫy: Thiếu mục 'ngoài phạm vi', nên scope cứ phình ra.
### BRD · Business Requirements Document
- 業務要件定義書 (gyōmu yōken teigisho)
- Trả lời: Doanh nghiệp cần đạt điều gì?
- Mẹo: B = Business = 'Bà chủ Ra Đề': nêu mục tiêu, không chỉ cách làm.
- Bẫy: Viết giải pháp vào BRD ('cần nút xanh góc phải'), làm bó tay team thiết kế.
### PRD · Product Requirements Document
- 製品要求仕様書 (seihin yōkyū shiyōsho)
- Trả lời: Sản phẩm cần có gì cho người dùng?
- Mẹo: PRD nhìn từ người dùng, BRD nhìn từ doanh nghiệp.
- Bẫy: Viết như BRD của dự án outsource nên thiếu persona và metric sản phẩm.
### FRD · Functional Requirements Document
- 機能要件定義書 (kinō yōken teigisho)
- Trả lời: Hệ thống phải làm những chức năng gì?
- Mẹo: F = Function = 'hệ thống Phải làm gì'.
- Bẫy: Chỉ mô tả luồng đẹp, quên ngoại lệ, nên bug dồn về 結合テスト.
### SRS · Software Requirements Specification
- 要件定義書・ソフトウェア要求仕様書 (yōken teigisho)
- Trả lời: Toàn bộ yêu cầu đã đủ để thiết kế và test chưa?
- Mẹo: SRS = 'Sổ Rõ Sạch': đủ rõ để dev làm, QA test.
- Bẫy: Viết câu không kiểm được ('hệ thống nhanh'), nên không test được.
### NFR · Non-functional Requirements
- 非機能要件定義書 (hi-kinō yōken teigisho)
- Trả lời: Hệ thống phải nhanh, bền, an toàn đến mức nào?
- Mẹo: Chức năng là 'làm gì', NFR là 'làm tốt tới đâu': Nhanh, Bền, An toàn.
- Bẫy: Để trống NFR, cuối dự án khách mới nói 'phải chịu 10.000 user'.
### US · User Story / Product Backlog
- ユーザーストーリー・プロダクトバックログ (yūzā sutōrī, purodakuto bakkurogu)
- Trả lời: (Agile) Người dùng cần gì, làm cái nào trước?
- Mẹo: INVEST: 6 chữ để kiểm một story.
- Bẫy: Đưa story quá to (epic) vào sprint nên không xong trong 1 sprint.

## 3. Chia nhỏ ra sao? (BREAKDOWN)
### WBS · Work Breakdown Structure
- WBS・作業分解構成図 (sagyō bunkai kōseizu)
- Trả lời: Toàn bộ công việc gồm những phần nào?
- Mẹo: Quy tắc 100%: các con cộng lại đúng bằng cha. WBS viết bằng danh từ, không bằng động từ.
- Bẫy: Liệt kê việc theo người ('việc của Nam') thay vì theo deliverable.
### PBS · Product Breakdown Structure
- 成果物分解構成 (seikabutsu bunkai kōsei)
- Trả lời: Sản phẩm cuối gồm những mảnh nào?
- Mẹo: PBS = 'cái gì' thuần danh từ; WBS = 'cái gì' cộng việc làm ra nó.
- Bẫy: Nhầm với WBS: PBS chỉ có 'thứ được giao', WBS có cả 'việc để làm ra nó'.
### ABS · Activity Breakdown Structure / Activity List
- アクティビティ一覧 (akutibiti ichiran)
- Trả lời: Mỗi work package cần làm những bước nào?
- Mẹo: A = Action = động từ. WBS là 'cái gì', ABS là 'làm sao để có'.
- Bẫy: Nhảy từ WBS sang Gantt luôn, bỏ qua quan hệ phụ thuộc, nên lịch không có critical path.
### OBS · Organizational Breakdown Structure
- 体制図 (taisei-zu)
- Trả lời: Dự án gồm những nhóm nào, ai báo cáo ai?
- Mẹo: O = Org = 'Ông nào'. WBS × OBS = RACI.
- Bẫy: Chỉ vẽ phía vendor, quên phía khách, nên không biết ai duyệt, ai quyết.
### RBS (tài nguyên) · Resource Breakdown Structure
- 資源分解構成 (shigen bunkai kōsei)
- Trả lời: Cần những loại tài nguyên gì?
- Mẹo: Có 2 RBS: R-esource (tài nguyên) và R-isk (rủi ro). Nghe 'RBS' thì hỏi lại.
- Bẫy: Trùng tên viết tắt với Risk Breakdown Structure. Luôn nói rõ 'RBS tài nguyên' hay 'RBS rủi ro'.
### RBS (rủi ro) · Risk Breakdown Structure
- リスク分解構成 (risuku bunkai kōsei)
- Trả lời: Rủi ro có thể đến từ những nguồn nào?
- Mẹo: RBS rủi ro là 'bản đồ nguồn nguy hiểm'; Risk Register là 'danh sách nguy hiểm cụ thể'.
- Bẫy: Có RBS nhưng không dùng để rà rủi ro mỗi tuần, nên nó chỉ là hình vẽ.
### CBS · Cost Breakdown Structure
- コスト分解構成 (kosuto bunkai kōsei)
- Trả lời: Tiền đi vào những hạng mục nào?
- Mẹo: C = Cash. WBS × CBS = cost baseline.
- Bẫy: Quên chi phí ẩn: BrSE, dịch tài liệu, onsite, môi trường test.

## 4. Ai làm, ai duyệt? (WHO)
### SHR · Stakeholder Register
- ステークホルダー登録簿 (sutēkuhorudā tōrokubo)
- Trả lời: Ai bị ảnh hưởng, ai có tiếng nói?
- Mẹo: Lưới Quyền lực × Quan tâm: ô cao-cao thì quản lý chặt nhất.
- Bẫy: Chỉ ghi người họp hằng tuần, quên người duyệt 稟議 và người dùng cuối.
### RACI · RACI / Responsibility Assignment Matrix
- 責任分担表・RACI表 (sekinin buntanhyō)
- Trả lời: Mỗi việc ai làm, ai chịu trách nhiệm, hỏi ai, báo ai?
- Mẹo: R-A-C-I = Làm · Chịu · Hỏi · Báo.
- Bẫy: Một việc có 2 chữ A, nên thật ra không ai chịu trách nhiệm.
### RP · Resource / Staffing Plan
- 要員計画 (yōin keikaku)
- Trả lời: Cần bao nhiêu người, vai trò gì, vào ra khi nào?
- Mẹo: Đường nhân sự hình 'quả núi': lên dần, đỉnh ở 製造/テスト, xuống dần.
- Bẫy: Ramp-up quá nhiều người cùng lúc, năng suất tụt (Brooks's law).

## 5. Làm thế nào? (HOW)
### UC · Use Case
- ユースケース図 (yūsukēsu zu)
- Trả lời: Ai dùng hệ thống để làm gì?
- Mẹo: Hình người que và hình elip: AI làm GÌ.
- Bẫy: Vẽ use case kiểu 'nhấn nút': quá chi tiết, đó là màn hình chứ không phải mục tiêu người dùng.
### DFD · Data Flow Diagram
- DFD・データフロー図 (dēta furō zu)
- Trả lời: Dữ liệu chảy từ đâu, qua xử lý nào, lưu ở đâu?
- Mẹo: DFD là dòng sông (chảy), ERD là hồ chứa (cấu trúc).
- Bẫy: Nhầm DFD với flowchart: DFD không có rẽ nhánh if/else.
### ARC · Architecture / System Configuration
- システム構成図 (shisutemu kōseizu)
- Trả lời: Hệ thống gồm những khối nào, nối nhau ra sao?
- Mẹo: ARC là 'bản đồ thành phố': có những khu nào, đường nào nối.
- Bẫy: Chỉ có hình đẹp, không có lý do chọn; khách hỏi 'vì sao không dùng X' là lúng túng.
### ERD · Entity Relationship Diagram
- ER図 → テーブル定義書 (ī-āru zu, tēburu teigisho)
- Trả lời: Dữ liệu gồm những thực thể nào, liên kết ra sao?
- Mẹo: Entity là danh từ (bảng), Relationship là đường nối; chân chim (crow's foot) nghĩa là 'nhiều'.
- Bẫy: Sửa ERD giữa chừng mà không đánh giá ảnh hưởng, vỡ nhiều màn hình và báo cáo.
### SCR · Screen Design & Transition
- 画面設計書・画面遷移図 (gamen sekkeisho, gamen sen'izu)
- Trả lời: Người dùng thấy gì, đi từ màn nào sang màn nào?
- Mẹo: 遷移 (sen'i) = di chuyển: màn này sang màn kia.
- Bẫy: Không có danh sách message lỗi, mỗi dev viết một kiểu, khách Nhật chê không thống nhất.
### API · Interface / API Specification
- IF仕様書・API仕様書 (intāfēsu shiyōsho)
- Trả lời: Hai hệ thống nói chuyện với nhau bằng gì?
- Mẹo: API là 'hợp đồng giữa hai cỗ máy'.
- Bẫy: Đổi IF mà không báo bên kia, lỗi chỉ lộ ra ở 結合テスト.
### BD · Basic Design (External Design)
- 基本設計書 (kihon sekkeisho)
- Trả lời: Hệ thống trông thế nào nhìn từ bên ngoài?
- Mẹo: 基本 = bên ngoài, khách thấy; 詳細 = bên trong, dev làm.
- Bẫy: Viết quá sâu vào code ở 基本設計: khách không đọc nổi, lại sai phạm vi.
### DD · Detailed Design (Internal Design)
- 詳細設計書 (shōsai sekkeisho)
- Trả lời: Bên trong từng module chạy thế nào?
- Mẹo: DD = 'Dev Đọc': viết cho dev.
- Bẫy: Bỏ 詳細設計 vì 'làm agile' trong dự án khách yêu cầu, nên thiếu deliverable lúc 検収.

## 6. Khi nào xong? (WHEN)
### PMP · Project Management Plan
- プロジェクト計画書 (purojekuto keikakusho)
- Trả lời: Dự án sẽ được quản lý như thế nào?
- Mẹo: PM Plan là 'luật chơi' của dự án. Đừng nhầm với chứng chỉ PMP.
- Bẫy: Viết xong rồi để đó; sau 1 tháng kế hoạch không còn khớp thực tế.
### NET · Network Diagram / Critical Path
- ネットワーク図・PERT図 (nettowāku zu)
- Trả lời: Việc nào phải xong trước, đâu là đường găng?
- Mẹo: Critical path = con đường dài nhất quyết định ngày về đích.
- Bẫy: Không nhận ra critical path, dồn người vào việc không găng.
### GNT · Gantt Chart / Schedule
- ガントチャート・スケジュール表 (ganto chāto, sukejūru hyō)
- Trả lời: Việc gì làm khi nào, ai làm, đang tới đâu?
- Mẹo: Gantt là 'thanh ngang theo lịch'. Ở Nhật người ta hay gọi luôn bảng này là 'WBS', đừng nhầm với cây WBS.
- Bẫy: Không lưu baseline, nên không chứng minh được trễ bao nhiêu và vì sao.
### MS · Milestone Chart
- マイルストーン表 (mairusutōn hyō)
- Trả lời: Những ngày chốt quan trọng là khi nào?
- Mẹo: Milestone là 'cột cây số': không có độ dài, chỉ có vị trí.
- Bẫy: Mốc không có tiêu chí đạt, nên 'xong' theo cảm giác.
### RLP · Release / Cutover Plan
- リリース計画書・本番移行計画書 (rirīsu keikakusho, honban ikō keikakusho)
- Trả lời: Đưa lên production thế nào, hỏng thì quay lại ra sao?
- Mẹo: Release plan = kịch bản cất cánh kèm kịch bản hạ cánh khẩn.
- Bẫy: Không diễn tập (rehearsal), lần chạy đầu tiên lại là lần thật.

## 7. Tốn bao nhiêu? (HOW MUCH)
### EST · Estimate / Quotation
- 見積書 (mitsumorisho)
- Trả lời: Mất bao nhiêu công, bao nhiêu tiền?
- Mẹo: Estimate = con số + 'nếu…'. Không có 'nếu' (tiền đề) thì chưa phải estimate.
- Bẫy: Gửi con số mà không gửi 前提条件, nên mọi thay đổi sau đều bị coi là 'trong giá'.
### CB · Cost Baseline / Budget
- コストベースライン・予算 (kosuto bēsurain, yosan)
- Trả lời: Ngân sách được duyệt chia theo thời gian ra sao?
- Mẹo: Hình chữ S: chậm – nhanh – chậm.
- Bẫy: Tiêu contingency như tiền thường, đến khi rủi ro thật xảy ra thì hết dự phòng.
### EVM · EVM / Budget vs Actual Report
- 予実管理 (yojitsu kanri)
- Trả lời: Đang nhanh hay chậm, lố hay tiết kiệm?
- Mẹo: Kế hoạch – Làm được – Tiêu hết = PV – EV – AC. Chỉ số dưới 1 là xấu.
- Bẫy: Đo EV bằng % cảm tính, task cứ '90%' mãi không xong.

## 8. Lệch thì sao? (WHAT IF)
### RAID · RAID Log
- RAIDログ (reido rogu)
- Trả lời: Mọi thứ có thể làm lệch dự án được theo dõi ở đâu?
- Mẹo: RAID = 'đột kích': Rủi ro – Giả định – Vấn đề – Phụ thuộc.
- Bẫy: Giả định không ai kiểm, khi nó sai thì đã muộn.
### RR · Risk Register
- リスク管理表 (risuku kanrihyō)
- Trả lời: Điều gì CÓ THỂ xảy ra, đối phó ra sao?
- Mẹo: Risk là TƯƠNG LAI (có thể xảy ra); Issue là HIỆN TẠI (đã xảy ra).
- Bẫy: Ghi rủi ro chung chung ('trễ tiến độ') thay vì nguyên nhân cụ thể.
### IL · Issue Log
- 課題管理表 (kadai kanrihyō)
- Trả lời: Vấn đề gì ĐANG xảy ra, ai xử lý, khi nào xong?
- Mẹo: Issue = 'cháy rồi': cần người cầm vòi và giờ dập.
- Bẫy: Ghi vấn đề không có hạn và người phụ trách, nên bảng dài mãi.
### CR · Change Request
- 変更要求書・仕様変更依頼 (henkō yōkyūsho)
- Trả lời: Thay đổi này ảnh hưởng gì, ai duyệt?
- Mẹo: CR = 'Cổng Rào': không qua cổng thì không vào baseline.
- Bẫy: Nhận thay đổi qua chat rồi làm luôn: mất tiền và mất baseline.
### IR · Incident Report
- 障害報告書 (shōgai hōkokusho)
- Trả lời: Sự cố gì đã xảy ra, vì sao, làm gì để không lặp lại?
- Mẹo: 5 câu: Khi nào – Ảnh hưởng gì – Vì sao – Đã xử lý ra sao – Làm gì để không lặp lại.
- Bẫy: Nguyên nhân dừng ở 'do người làm sai'; khách Nhật không chấp nhận, họ cần nguyên nhân ở quy trình.

## 9. Đạt chưa? (HOW GOOD)
### QMP · Quality Management Plan
- 品質計画書 (hinshitsu keikakusho)
- Trả lời: Thế nào là 'đạt', đo bằng gì, kiểm ở đâu?
- Mẹo: QMP là 'luật chấm điểm': viết trước khi thi.
- Bẫy: Đặt ngưỡng chỉ số mà không có số liệu lịch sử, ngưỡng thành vô nghĩa.
### RTM · Requirements Traceability Matrix
- トレーサビリティマトリクス (torēsabiriti matorikusu)
- Trả lời: Mỗi yêu cầu đã được thiết kế, test ở đâu?
- Mẹo: RTM là 'sợi chỉ đỏ' xuyên từ yêu cầu tới test.
- Bẫy: Chỉ làm RTM lúc cuối để đối phó, nên không giúp gì khi có thay đổi giữa chừng.
### TP · Test Plan
- テスト計画書 (tesuto keikakusho)
- Trả lời: Test cái gì, khi nào, cách nào, khi nào dừng?
- Mẹo: Test plan = 'đánh trận ở đâu'; Test spec = 'từng phát bắn'.
- Bẫy: Không có tiêu chí kết thúc, nên test mãi hoặc dừng theo deadline.
### TS · Test Specification / Test Cases
- テスト仕様書 (tesuto shiyōsho)
- Trả lời: Từng bước test là gì, mong đợi kết quả gì?
- Mẹo: Mỗi case = 'Cho – Khi – Thì' (Given – When – Then).
- Bẫy: Kết quả mong đợi ghi 'hiển thị đúng', nên không kiểm được.
### BUG · Bug List / Defect Log
- 不具合管理表 (fuguai kanrihyō)
- Trả lời: Có những lỗi nào, nặng cỡ nào, sửa chưa?
- Mẹo: Severity = mức đau; Priority = sửa trước hay sau.
- Bẫy: Không ghi nguyên nhân và pha gây lỗi, nên không phân tích được để cải tiến.
### QR · Quality / Test Report
- 品質報告書・テスト結果報告書 (hinshitsu hōkokusho)
- Trả lời: Chất lượng hiện tại đủ để release chưa?
- Mẹo: Số → So sánh → Lý giải → Kết luận.
- Bẫy: Chỉ đưa số, không có phân tích và kết luận; khách tự suy diễn.

## 10. Báo ai, thế nào? (TALK)
### CMP · Communication Plan
- コミュニケーション計画書 (komyunikēshon keikakusho)
- Trả lời: Ai cần biết gì, khi nào, qua kênh nào?
- Mẹo: CMP là 'lịch phát sóng': ai nghe kênh nào, giờ nào.
- Bẫy: Không có quy tắc trả lời câu hỏi: khách đợi, team đợi, cùng trễ.
### QA · Q&A List
- QA管理表 (kyū-ē kanrihyō)
- Trả lời: Còn câu hỏi nào với khách, đã trả lời chưa?
- Mẹo: Hỏi kiểu trắc nghiệm, đừng hỏi tự luận. (QA ở đây là hỏi đáp, không phải Quality Assurance.)
- Bẫy: Hỏi câu mở ('cái này thế nào ạ?') nên khách trả lời chậm. Hãy hỏi kèm phương án A/B.
### SR · Status Report
- 進捗報告書 (shinchoku hōkokusho)
- Trả lời: Tuần này dự án đang ở đâu?
- Mẹo: RAG: Red – Amber – Green. Không có 'xanh dưa hấu'.
- Bẫy: Báo xanh suốt rồi đột nhiên đỏ (báo cáo 'dưa hấu': vỏ xanh ruột đỏ).
### MoM · Minutes of Meeting
- 議事録 (gijiroku)
- Trả lời: Họp đã quyết gì, ai làm gì, hạn khi nào?
- Mẹo: Ba thứ phải có: Quyết gì – Ai làm – Bao giờ.
- Bẫy: Ghi diễn biến dài dòng, không ghi rõ quyết định; sau này cãi nhau.

## 11. Xong chưa? (DONE)
### UAT · UAT & Acceptance Sign-off
- 受入テスト・検収書 (ukeire tesuto, kenshūsho)
- Trả lời: Khách đã chấp nhận sản phẩm chưa?
- Mẹo: 検収 = 'ký nhận hàng', ký xong mới có tiền.
- Bẫy: Tiêu chí nghiệm thu không ghi trong SOW, khách kéo dài 検収.
### LL · Lessons Learned
- 振り返り・教訓 (furikaeri, kyōkun)
- Trả lời: Lần sau làm gì khác đi?
- Mẹo: KPT: Keep – Problem – Try, cách 振り返り phổ biến ở Nhật.
- Bẫy: Viết xong cất đi, dự án sau không ai đọc.
### CLR · Closure Report
- 完了報告書 (kanryō hōkokusho)
- Trả lời: Dự án kết thúc ra sao so với mục tiêu?
- Mẹo: CLR = 'Clear': dọn sạch trước khi rời.
- Bẫy: Đóng dự án khi chưa bàn giao tài liệu vận hành, bên bảo trì gọi lại liên tục.

## Họ xBS: cùng 1 cây, 7 chiếc kính
### WBS: Công việc (danh từ, theo deliverable)
- Website TMĐT
  - 1. Quản lý dự án
    - 1.1 Kế hoạch
    - 1.2 Báo cáo tuần
  - 2. Yêu cầu & thiết kế
    - 2.1 要件定義書
    - 2.2 基本設計書
  - 3. Phát triển
    - 3.1 Giỏ hàng
    - 3.2 Thanh toán
  - 4. Test & release
    - 4.1 結合テスト
    - 4.2 Release
### PBS: Sản phẩm (chỉ thứ được giao)
- Website TMĐT
  - Front-end
    - Trang sản phẩm
    - Trang giỏ hàng
  - Back-end API
    - API đơn hàng
    - API thanh toán
  - Cơ sở dữ liệu
    - Bảng User
    - Bảng Order
  - Tài liệu bàn giao
    - 設計書
    - Hướng dẫn vận hành
### ABS: Hoạt động (động từ, tách từ 1 work package)
- WP 3.2 Thanh toán
  - Thiết kế
    - Viết 詳細設計
    - Review thiết kế
  - Lập trình
    - Code API
    - Nối cổng thanh toán
  - Kiểm thử
    - Viết case UT
    - Chạy UT
  - Review & sửa
    - Code review
    - Sửa 指摘
### OBS: Tổ chức (ai thuộc nhóm nào)
- Ban dự án
  - PM
    - Sub-PM
    - PMO
  - BrSE / Comtor
    - BrSE onsite
    - Comtor
  - Team Dev
    - Team FE
    - Team BE
  - Team QA
    - QA lead
    - Tester
### RBS · tài nguyên: Tài nguyên (cần những gì)
- Tài nguyên
  - Con người
    - Dev BE × 4
    - Tester × 2
  - Thiết bị
    - Laptop
    - Máy test iOS/Android
  - Phần mềm
    - License IDE
    - Công cụ quản lý
  - Dịch vụ
    - Cloud
    - Môi trường staging
### RBS · rủi ro: Nguồn rủi ro (nguy hiểm đến từ đâu)
- Rủi ro dự án
  - Kỹ thuật
    - Hiệu năng
    - Tích hợp IF
  - Yêu cầu
    - Spec mơ hồ
    - Đổi spec
  - Con người
    - Nghỉ việc
    - Thiếu tiếng Nhật
  - Bên ngoài
    - Vendor khác trễ
    - Luật thay đổi
### CBS: Chi phí (tiền đi đâu)
- Ngân sách
  - Nhân công
    - Dev
    - QA & BrSE
  - Hạ tầng
    - Cloud
    - Môi trường test
  - License
    - Công cụ
    - Thư viện
  - Dự phòng
    - Contingency
    - Mgmt reserve
### Công thức
- WBS × OBS = RACI (ai làm gì)
- WBS → ABS → NET = Gantt (lịch có đường găng)
- WBS × CBS = Cost baseline (ngân sách theo thời gian)
- PBS + việc quản lý = WBS (không sót deliverable)
- RBS rủi ro = Risk register (rủi ro cụ thể)
- RBS tài nguyên = Kế hoạch nhân sự (ai vào, khi nào)

## Chữ V kiểu Nhật
### 業務要件 ↔ 受入テスト
- Làm ra: BRD, BC
- Kiểm chứng: UAT
### 要件定義 ↔ 総合テスト
- Làm ra: SRS, FRD, NFR
- Kiểm chứng: TP, QR
### 基本設計 ↔ 結合テスト
- Làm ra: BD, ARC, SCR, API
- Kiểm chứng: TS, BUG
### 詳細設計 ↔ 単体テスト
- Làm ra: DD, ERD
- Kiểm chứng: TS
- RTM nối mọi cặp

## Đừng nhầm
### BRD và FRD / SRS
- BRD: doanh nghiệp cần đạt gì (mục tiêu, quy trình, KPI)
- FRD: hệ thống phải làm chức năng gì
- SRS: toàn bộ đặc tả, thêm phi chức năng, giao diện, ràng buộc
- Mẹo: Đọc theo thứ tự B → F → S: Business → Function → toàn bộ Software. Ở Nhật: 業務要件 → 機能要件 + 非機能要件 = 要件定義書.
### BRD và PRD
- BRD: dự án do khách đặt hàng, nhìn từ doanh nghiệp
- PRD: công ty làm sản phẩm, nhìn từ người dùng thị trường
- Mẹo: Outsource cho khách Nhật: gần như luôn là BRD / 要件定義書.
### WBS và Gantt
- WBS: cây 'cái gì', không có ngày
- Gantt: 'khi nào, ai làm', thanh theo lịch
- Mẹo: Ở Nhật, bảng Excel lịch hay bị gọi là 'WBS'. Nghe 'WBS' thì hỏi lại: cây phân rã hay lịch?
### WBS và ABS
- WBS: danh từ, deliverable, work package
- ABS / Activity list: động từ, các bước làm ra 1 work package
- Mẹo: 'Module thanh toán' là WBS; 'viết thiết kế, code, test' là activity.
### WBS và PBS
- PBS: chỉ thứ được giao (sản phẩm)
- WBS: thứ được giao + việc để làm ra nó, kể cả quản lý dự án
- Mẹo: PBS + việc quản lý, test, release = WBS.
### RBS (tài nguyên) và RBS (rủi ro)
- Resource BS: người, thiết bị, phần mềm, dịch vụ
- Risk BS: nguồn rủi ro theo nhóm
- Mẹo: Cùng tên viết tắt: luôn nói rõ chữ R là Resource hay Risk.
### OBS và RACI
- OBS (体制図): ai thuộc nhóm nào, ai báo cáo ai
- RACI: với từng việc, ai làm, ai chịu, ai được hỏi, ai được báo
- Mẹo: RACI = WBS (hàng) × OBS (cột).
### Risk register và Issue log
- Risk: chưa xảy ra, có xác suất
- Issue: đã xảy ra, cần người xử lý và hạn
- Mẹo: Rủi ro xảy ra thì chuyển từ リスク管理表 sang 課題管理表.
### Issue và Change request
- Issue: vấn đề cần giải quyết
- CR: đề nghị đổi baseline (phạm vi, lịch, chi phí)
- Mẹo: Một issue có thể sinh ra CR, nhưng không phải issue nào cũng là CR.
### ERD và DFD
- ERD: dữ liệu tổ chức thế nào (bảng, khóa, quan hệ)
- DFD: dữ liệu chảy đi đâu (nguồn, xử lý, kho)
- Mẹo: ERD là hồ chứa, DFD là dòng sông.
### 基本設計 và 詳細設計
- 基本設計 (Basic Design): nhìn từ ngoài, khách duyệt
- 詳細設計 (Detailed Design): nhìn từ trong, viết cho dev
- Mẹo: 基本 = khách thấy; 詳細 = dev đọc.
### Test plan và Test spec
- Test plan: phạm vi, mức test, môi trường, tiêu chí dừng
- Test spec: từng case, bước làm, kết quả mong đợi
- Mẹo: Plan là chiến lược, spec là từng phát bắn.
### Charter và SOW / Scope statement
- Charter: cho phép dự án bắt đầu, trao quyền cho PM
- SOW: phạm vi theo hợp đồng với khách
- Scope statement: phạm vi chi tiết để lập WBS
- Mẹo: Charter = giấy khai sinh; SOW = hợp đồng; Scope statement = hàng rào.
### Estimate và Cost baseline
- Estimate: con số ước tính, kèm tiền đề
- Cost baseline: con số đã duyệt, chia theo thời gian, dùng để đo
- Mẹo: Estimate là đề xuất; baseline là cam kết.
### Status report và 議事録 (MoM)
- Status report: trạng thái định kỳ của cả dự án
- 議事録: quyết định và việc cần làm của 1 cuộc họp
- Mẹo: Báo cáo nhìn cả dự án; biên bản nhìn 1 cuộc họp.
### Severity và Priority
- Severity: lỗi nặng cỡ nào
- Priority: sửa trước hay sau
- Mẹo: Lỗi chính tả ở trang chủ: severity thấp, priority cao.
