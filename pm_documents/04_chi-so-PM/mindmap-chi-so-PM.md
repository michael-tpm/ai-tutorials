---
title: Mindmap chỉ số PM
markmap:
  initialExpandLevel: 2
---

<!-- Mở bằng markmap (VS Code extension 'Markmap' hoặc markmap.js.org/repl). Bản tương tác: bang-chi-so-PM.html -->

# Chỉ số PM · 9 câu hỏi

## 1. Có kịp không? (SCHEDULE)
### SV · Schedule Variance
- スケジュール差異 (sukejūru sai)
- Công thức: SV = EV − PV
- Ngưỡng (tham khảo): tốt ≥ 0 · chú ý từ −5% PV đến 0 · báo động < −5% PV
- Mẹo: EV trừ PV: làm được trừ dự định.
- Bẫy: Cuối dự án SV luôn về 0 (EV = PV = BAC) kể cả khi trễ. Việc chậm nằm trên critical path có thể nguy hiểm hơn con số SV cho thấy.
### SPI · Schedule Performance Index
- スケジュール効率指数 (sukejūru kōritsu shisū)
- Công thức: SPI = EV ÷ PV
- Ngưỡng (tham khảo): tốt ≥ 0,95 · chú ý 0,85 – 0,95 · báo động < 0,85
- Mẹo: S chia: EV / PV. Dưới 1 là chậm.
- Bẫy: Gần cuối dự án SPI tự tiến về 1 dù dự án trễ, nên đọc kèm số ngày trễ (SLIP) và critical path.
### %C · Percent Complete
- 進捗率 (shinchoku-ritsu)
- Công thức: %C = EV ÷ BAC × 100%  (hoặc số work package xong ÷ tổng)
- Ngưỡng (tham khảo): tốt lệch ≤ 2 điểm % · chú ý lệch 3–5 điểm · báo động lệch > 5 điểm
- Mẹo: Đếm cái đã xong, đừng đếm cái 'gần xong'.
- Bẫy: Dùng % do member tự khai, task cứ '90%' mãi không xong. Hãy dùng quy tắc đo khách quan.
### OTD · On-time Delivery Rate
- 納期遵守率 (nōki junshu-ritsu)
- Công thức: OTD = số mốc/release đúng hạn ÷ số mốc/release đã đến hạn × 100%
- Ngưỡng (tham khảo): tốt ≥ 95% · chú ý 85 – 95% · báo động < 85%
- Mẹo: Đúng hạn theo ngày ĐÃ HỨA, không theo ngày mới sửa.
- Bẫy: Dời ngày kế hoạch liên tục để lúc nào cũng 'đúng hạn'. Phải đo theo baseline đã cam kết và ghi lại mỗi lần đổi.
### SLIP · Schedule Slip (days)
- 予実差異（日数） (yojitsu sai (nissū))
- Công thức: SLIP = ngày xong dự báo (hoặc thực tế) − ngày baseline
- Ngưỡng (tham khảo): tốt ≤ 0 · chú ý 1 – 3 ngày · báo động > 3 ngày hoặc nằm trên critical path
- Mẹo: Lãnh đạo hỏi 'trễ mấy ngày?', không hỏi 'SPI bao nhiêu?'.
- Bẫy: Báo trễ theo ngày lịch thay vì ngày làm việc; quên ngày nghỉ Nhật (Golden Week, お盆, 年末年始) và Việt Nam (Tết).
### TF · Total Float
- トータルフロート (tōtaru furōto)
- Công thức: TF = LS − ES = LF − EF
- Ngưỡng (tham khảo): tốt > 5 ngày · chú ý 1 – 5 ngày · báo động ≤ 0
- Mẹo: Float = khoảng 'được phép chậm' mà chưa ai thấy.
- Bẫy: Tiêu hết float của các việc không găng, rồi xuất hiện nhiều critical path mới cùng lúc.

## 2. Có lố tiền không? (COST · EVM)
### PV · Planned Value
- 計画価値 (keikaku kachi)
- Công thức: PV = tổng ngân sách các việc lên lịch tới hôm nay
- Mẹo: P = Plan: 'lẽ ra'.
- Bẫy: Không có baseline thì không có PV, và không làm EVM được.
### EV · Earned Value
- 出来高 (dekidaka)
- Công thức: EV = % hoàn thành (đo khách quan) × BAC
- Mẹo: E = Earned: 'kiếm được thật'.
- Bẫy: Ước EV theo cảm tính thì mọi chỉ số phía sau đều sai.
### AC · Actual Cost
- 実コスト (jitsu kosuto)
- Công thức: AC = tổng effort/chi phí thực tế ghi nhận tới hôm nay
- Mẹo: A = Actual: 'đã tiêu thật'.
- Bẫy: Timesheet ghi muộn hoặc ghi nhầm dự án, AC thấp giả và CPI đẹp giả.
### CV · Cost Variance
- コスト差異 (kosuto sai)
- Công thức: CV = EV − AC
- Ngưỡng (tham khảo): tốt ≥ 0 · chú ý từ −5% EV đến 0 · báo động < −5% EV
- Mẹo: EV trừ AC: làm được trừ đã tiêu.
- Bẫy: CV dương vì timesheet ghi thiếu, không phải vì làm giỏi.
### CPI · Cost Performance Index
- コスト効率指数 (kosuto kōritsu shisū)
- Công thức: CPI = EV ÷ AC
- Ngưỡng (tham khảo): tốt ≥ 0,95 · chú ý 0,85 – 0,95 · báo động < 0,85
- Mẹo: C chia: EV / AC. Dưới 1 là lố.
- Bẫy: Kinh nghiệm EVM phổ biến: CPI ít khi tự hồi phục nhiều sau khoảng 20% dự án. Đừng hứa 'sẽ bù lại' nếu không có hành động cụ thể.
### EAC · Estimate at Completion
- 完成時総コスト見積 (kanseiji sō-kosuto mitsumori)
- Công thức: EAC = BAC ÷ CPI  ·  = AC + (BAC − EV)  ·  = AC + (BAC − EV) ÷ (CPI × SPI)  ·  = AC + ETC (ước lại từ dưới lên)
- Ngưỡng (tham khảo): tốt ≤ BAC · chú ý BAC đến +5% · báo động > BAC + 5%
- Mẹo: 'Nếu cứ thế này thì cuối cùng tốn bao nhiêu?'
- Bẫy: Chỉ đưa 1 con số EAC. Nên đưa một dải (lạc quan – bi quan) kèm giả định.
### ETC · Estimate to Complete
- 残作業見積 (zansagyō mitsumori)
- Công thức: ETC = EAC − AC  (hoặc estimate lại phần còn lại từ dưới lên)
- Ngưỡng (tham khảo): tốt ≤ BAC − AC · chú ý vượt nhẹ · báo động vượt nhiều
- Mẹo: 'Còn phải tiêu bao nhiêu nữa?'
- Bẫy: Lấy BAC − AC làm ETC, tức là giả định phần còn lại chạy đúng kế hoạch dù đang lố.
### VAC · Variance at Completion
- 完成時差異 (kanseiji sai)
- Công thức: VAC = BAC − EAC
- Ngưỡng (tham khảo): tốt ≥ 0 · chú ý từ −5% BAC đến 0 · báo động < −5% BAC
- Mẹo: 'Cuối cùng hụt bao nhiêu?'
- Bẫy: VAC âm nhưng không báo sớm, lãnh đạo biết khi đã hết tiền.
### TCPI · To-Complete Performance Index
- 残作業効率指数 (zansagyō kōritsu shisū)
- Công thức: TCPI = (BAC − EV) ÷ (BAC − AC)  (giữ BAC)  ·  = (BAC − EV) ÷ (EAC − AC)  (theo EAC mới)
- Ngưỡng (tham khảo): tốt ≤ CPI hiện tại · chú ý cao hơn CPI ≤ 0,1 · báo động cao hơn CPI > 0,1
- Mẹo: 'Từ giờ phải giỏi lên bao nhiêu mới kịp tiền?'
- Bẫy: Hứa 'team sẽ cố' khi TCPI 1,12 mà CPI 0,83: gần như không khả thi.
### EFV · Effort Variance
- 工数予実差異 (kōsū yojitsu sai)
- Công thức: EFV = (effort thực tế − effort kế hoạch) ÷ effort kế hoạch × 100%
- Ngưỡng (tham khảo): tốt ±5% · chú ý ±5 – 15% · báo động > ±15%
- Mẹo: 'Tốn công hơn dự tính bao nhiêu, ở đâu?'
- Bẫy: Chỉ xem tổng dự án nên không thấy phase nào gây lố.
### EA · Estimate Accuracy
- 見積精度 (mitsumori seido)
- Công thức: Sai lệch = (thực tế − estimate) ÷ estimate × 100%  (đo khi đóng dự án/phase)
- Ngưỡng (tham khảo): tốt ±10% · chú ý ±10 – 20% · báo động > ±20%
- Mẹo: Dự đoán giỏi cỡ nào? Đo ở cuối, dùng cho lần sau.
- Bẫy: Cộng hết CR vào baseline rồi mới so, che mất sai số của estimate gốc.

## 3. Phạm vi có phình không? (SCOPE)
### SCR · Scope Creep
- スコープクリープ率 (sukōpu kurīpu-ritsu)
- Công thức: SCR = effort (hoặc số yêu cầu) thêm vào KHÔNG qua CR ÷ baseline × 100%
- Ngưỡng (tham khảo): tốt < 5% · chú ý 5 – 10% · báo động > 10%
- Mẹo: Creep = bò lén vào. Có CR thì không còn là creep.
- Bẫy: Nhầm thay đổi đã duyệt là scope creep, hoặc ngược lại 'làm luôn cho khách vui' không ghi lại.
### CRA · CR Approval Rate
- 変更要求承認率 (henkō yōkyū shōnin-ritsu)
- Công thức: CRA = số CR (追加見積) khách duyệt ÷ số CR đã gửi × 100%
- Ngưỡng (tham khảo): tốt ≥ 80% · chú ý 60 – 80% · báo động < 60%
- Mẹo: 'Gửi 10 CR, khách gật mấy cái?'
- Bẫy: Tỷ lệ cao vì chỉ gửi CR nhỏ, còn CR lớn thì 'làm luôn cho xong'. Đọc kèm SCR.
### RV · Requirement Volatility
- 要件変更率 (yōken henkō-ritsu)
- Công thức: RV = (số yêu cầu thêm + sửa + xóa trong kỳ) ÷ tổng yêu cầu baseline × 100%
- Ngưỡng (tham khảo): tốt < 10% mỗi phase · chú ý 10 – 20% · báo động > 20%
- Mẹo: 'Yêu cầu đang rung bao nhiêu?'
- Bẫy: RV cao sau 基本設計 mà vẫn giữ giá cố định 請負, dự án lỗ.
### RCOV · Requirement Coverage
- 要件カバレッジ (yōken kabarejji)
- Công thức: RCOV = số yêu cầu có test case đã chạy đạt ÷ tổng yêu cầu × 100%
- Ngưỡng (tham khảo): tốt 100% trước UAT · chú ý 95 – 99% · báo động < 95%
- Mẹo: 'Yêu cầu nào chưa có ai kiểm?'
- Bẫy: Có test case nhưng chưa chạy, hoặc chạy chưa đạt, vẫn tính là 'đã phủ'.

## 4. Chất lượng ổn không? (QUALITY)
### TD · Test Density
- テスト密度 (tesuto mitsudo)
- Công thức: TD = số test case ÷ quy mô (KLOC hoặc FP)
- Ngưỡng (tham khảo): tốt trong khoảng ngưỡng · chú ý lệch ±20% ngưỡng · báo động ngoài ±20%
- Mẹo: 'Mỗi 1.000 dòng code được bắn bao nhiêu phát?'
- Bẫy: Đạt mật độ bằng cách nhân bản các case gần giống nhau.
### BD · Bug Density
- バグ密度 (bagu mitsudo)
- Công thức: BD = số bug phát hiện ÷ quy mô (KLOC hoặc FP), tính riêng từng mức test
- Ngưỡng (tham khảo): tốt trong khoảng ngưỡng · chú ý lệch nhẹ · báo động ngoài khoảng (cả cao lẫn thấp)
- Mẹo: Thấp quá cũng đáng ngờ như cao quá.
- Bẫy: Ăn mừng khi バグ密度 rất thấp; khách Nhật sẽ hỏi 'test đã đủ chưa?'.
### RCD · Review Comment Density
- レビュー指摘密度 (rebyū shiteki mitsudo)
- Công thức: RCD = số 指摘 (điểm chỉ ra) ÷ quy mô (trang tài liệu hoặc KLOC)
- Ngưỡng (tham khảo): tốt trong khoảng ngưỡng · chú ý lệch nhẹ · báo động ngoài khoảng
- Mẹo: Bắt lỗi trên giấy rẻ hơn bắt lỗi trong code.
- Bẫy: Review hời hợt ra ít 指摘 nên tưởng tài liệu tốt; bug dồn xuống giai đoạn test.
### RER · Review Effort Ratio
- レビュー工数比率 (rebyū kōsū hiritsu)
- Công thức: RER = effort review ÷ effort tạo tài liệu/code × 100%
- Ngưỡng (tham khảo): tốt 10 – 20% · chú ý 5 – 10% · báo động < 5%
- Mẹo: Review là bảo hiểm rẻ nhất.
- Bẫy: Review là việc bị cắt đầu tiên khi trễ tiến độ, rồi bug tăng ở cuối.
### DL · Defect Leakage
- 流出率 (ryūshutsu-ritsu)
- Công thức: DL = bug khách/UAT/production phát hiện ÷ (bug nội bộ phát hiện + bug lọt ra) × 100%
- Ngưỡng (tham khảo): tốt < 5% · chú ý 5 – 10% · báo động > 10%
- Mẹo: 'Lọt qua lưới bao nhiêu phần trăm?'
- Bẫy: Nói 'leakage < 5%' mà không nói mẫu số có tính 指摘 review hay không; interviewer tính lại sẽ ra số khác.
### DRE · Defect Removal Efficiency
- 欠陥除去率 (kekkan jokyo-ritsu)
- Công thức: DRE = bug bắt trước release ÷ (bug trước release + bug sau release) × 100%  = 100% − DL
- Ngưỡng (tham khảo): tốt ≥ 95% · chú ý 90 – 95% · báo động < 90%
- Mẹo: DRE + Leakage = 100%.
- Bẫy: Đo quá sớm sau release, bug sau release chưa kịp xuất hiện nên DRE đẹp giả.
### BCV · Bug Convergence
- バグ収束・信頼度成長曲線 (bagu shūsoku, shinraido seichō kyokusen)
- Công thức: Vẽ số bug tích lũy theo ngày (hoặc theo số case đã chạy); hội tụ khi đường cong nằm ngang trong lúc vẫn đang chạy test
- Ngưỡng (tham khảo): tốt nằm ngang ở 20% case cuối · chú ý đang cong xuống · báo động vẫn dốc lên
- Mẹo: Nằm ngang = gần hết bug, nếu vẫn đang test.
- Bẫy: Đường nằm ngang vì đã ngừng test, không phải vì hết bug.
### RW · Rework Rate
- 手戻り率 (temodori-ritsu)
- Công thức: RW = effort làm lại (sửa spec, thiết kế, code do lỗi) ÷ tổng effort × 100%
- Ngưỡng (tham khảo): tốt < 10% · chú ý 10 – 20% · báo động > 20%
- Mẹo: Làm hai lần một việc là trả tiền hai lần.
- Bẫy: Không tách rework khỏi effort thường, nên không thấy tiền đang chảy mất ở đâu.
### TEX · Test Execution Rate
- テスト消化率 (tesuto shōka-ritsu)
- Công thức: TEX = số case đã chạy ÷ tổng case kế hoạch × 100%
- Ngưỡng (tham khảo): tốt đúng hoặc vượt kế hoạch · chú ý chậm ≤ 5 điểm · báo động chậm > 5 điểm
- Mẹo: 消化 = đã 'ăn' được bao nhiêu case.
- Bẫy: Nhầm với tỷ lệ đạt: chạy 100% nhưng chỉ đạt 70% thì vẫn chưa xong.
### TPR · Test Pass Rate
- テスト合格率 (tesuto gōkaku-ritsu)
- Công thức: TPR = số case đạt ÷ số case đã chạy × 100%
- Ngưỡng (tham khảo): tốt ≥ 95% · chú ý 90 – 95% · báo động < 90%
- Mẹo: 合格 = đậu.
- Bẫy: Bỏ các case 'pending/blocked' ra khỏi mẫu số cho số đẹp.
### C0/C1 · Code Coverage
- コードカバレッジ (kōdo kabarejji)
- Công thức: C0 (statement) = số lệnh đã chạy ÷ tổng lệnh  ·  C1 (branch) = số nhánh đã chạy ÷ tổng nhánh
- Ngưỡng (tham khảo): tốt đạt ngưỡng · chú ý thấp hơn 5 – 10 điểm · báo động thấp hơn > 10 điểm
- Mẹo: C0 = dòng, C1 = nhánh.
- Bẫy: Coverage cao nhưng test không kiểm kết quả (không assert): code được chạy qua mà không được kiểm.
### OPB · Open Bugs by Severity
- 未解決バグ（重要度別） (mikaiketsu bagu (jūyōdo-betsu))
- Công thức: Đếm bug chưa đóng theo severity (Critical / High / Medium / Low), kèm tuổi bug
- Ngưỡng (tham khảo): tốt 0 Critical, 0 High · chú ý còn High có workaround · báo động còn Critical
- Mẹo: Đếm theo mức đau, đừng đếm tổng.
- Bẫy: Hạ severity trước release cho đẹp số.

## 5. Team chạy đều không? (AGILE · FLOW)
### VEL · Velocity
- ベロシティ (beroshiti)
- Công thức: VEL = tổng story point của các story Done trong 1 sprint (dùng trung bình 3–5 sprint gần nhất)
- Ngưỡng (tham khảo): tốt dao động ≤ ±15% · chú ý ±15 – 30% · báo động > ±30%
- Mẹo: Velocity là đồng hồ tốc độ của 1 xe, không phải để đua giữa 2 xe.
- Bẫy: So velocity giữa 2 team hoặc ép tăng velocity, team sẽ thổi phồng điểm.
### SDR · Say/Do Ratio
- コミットメント達成率 (komittomento tassei-ritsu)
- Công thức: SDR = điểm Done ÷ điểm cam kết đầu sprint × 100%
- Ngưỡng (tham khảo): tốt 85 – 100% · chú ý 70 – 85% · báo động < 70% hoặc liên tục > 110%
- Mẹo: 'Nói 10 làm mấy?'
- Bẫy: Cam kết thấp để lúc nào cũng đạt 100%.
### BDN · Burndown
- バーンダウンチャート (bāndaun chāto)
- Công thức: Đường việc còn lại (điểm hoặc giờ) theo ngày, so với đường lý tưởng
- Ngưỡng (tham khảo): tốt bám đường lý tưởng · chú ý lệch nhưng đang hội tụ · báo động đi ngang hoặc tăng
- Mẹo: Đi ngang = kẹt; nhảy lên = thêm việc.
- Bẫy: Đường đẹp vì mọi người cập nhật dồn vào cuối sprint.
### LT · Lead Time
- リードタイム (rīdo taimu)
- Công thức: LT = thời điểm giao − thời điểm yêu cầu được tạo
- Ngưỡng (tham khảo): tốt ≤ SLA · chú ý vượt SLA ≤ 20% · báo động vượt SLA > 20%
- Mẹo: Lead = góc nhìn khách: từ lúc xin tới lúc nhận.
- Bẫy: Nhầm với cycle time; khách cảm nhận lead time chứ không cảm nhận cycle time.
### CT · Cycle Time
- サイクルタイム (saikuru taimu)
- Công thức: CT = thời điểm xong − thời điểm bắt đầu làm  ·  Little's Law: CT ≈ WIP ÷ Throughput
- Ngưỡng (tham khảo): tốt ổn định hoặc giảm · chú ý tăng ≤ 20% · báo động tăng > 20%
- Mẹo: Cycle = góc nhìn team: từ lúc bắt tay tới lúc xong.
- Bẫy: Nhiều việc dở dang cùng lúc làm cycle time dài ra.
### THR · Throughput
- スループット (surūputto)
- Công thức: THR = số item hoàn thành ÷ kỳ
- Ngưỡng (tham khảo): tốt ổn định · chú ý giảm ~20% · báo động giảm > 30%
- Mẹo: 'Mỗi tuần ra lò bao nhiêu việc?'
- Bẫy: Các item to nhỏ quá khác nhau thì throughput khó so; nên chia việc đều cỡ.
### WIP · Work in Progress
- 仕掛り作業 (shikakari sagyō)
- Công thức: WIP = số item ở trạng thái 'đang làm'  ·  CT ≈ WIP ÷ Throughput
- Ngưỡng (tham khảo): tốt ≤ giới hạn WIP · chú ý vượt nhẹ · báo động vượt nhiều, việc tồn lâu
- Mẹo: Ít dở dang thì nhanh xong.
- Bẫy: Mở nhiều việc để 'ai cũng bận', rốt cuộc không việc nào xong.

## 6. Team có khỏe không? (PEOPLE)
### UTL · Utilization
- 稼働率 (kadō-ritsu)
- Công thức: UTL = giờ làm việc dự án ÷ giờ có thể làm × 100%
- Ngưỡng (tham khảo): tốt 75 – 85% · chú ý 85 – 95% hoặc 60 – 75% · báo động > 95% hoặc < 60%
- Mẹo: 100% giống đường kẹt xe: không còn chỗ để xoay.
- Bẫy: 稼働率 cũng là từ chỉ độ sẵn sàng của hệ thống (システム稼働率); hỏi rõ ngữ cảnh. Ép 100% dễ dẫn tới burnout.
### BIL · Billable Rate
- 請求可能率 (seikyū kanō-ritsu)
- Công thức: BIL = giờ tính tiền khách ÷ tổng giờ làm × 100%
- Ngưỡng (tham khảo): tốt ≥ 80% · chú ý 70 – 80% · báo động < 70%
- Mẹo: 'Giờ nào khách trả tiền?'
- Bẫy: Đẩy billable bằng cách bỏ đào tạo, bỏ review nội bộ; chất lượng giảm theo.
### OT · Overtime Hours
- 残業時間 (zangyō jikan)
- Công thức: OT/người/tháng = tổng giờ OT ÷ số người
- Ngưỡng (tham khảo): tốt thấp, ổn định · chú ý tăng 2 tuần liền · báo động vượt giới hạn công ty/luật hoặc kéo dài > 1 tháng
- Mẹo: OT là cơn sốt: chữa nguyên nhân, đừng chỉ hạ sốt.
- Bẫy: Coi OT là giải pháp; OT kéo dài thường do estimate sai hoặc scope creep.
### ATR · Attrition Rate
- 離職率 (rishoku-ritsu)
- Công thức: ATR = số người nghỉ trong kỳ ÷ số người bình quân × 100% (thường tính theo năm)
- Ngưỡng (tham khảo): tốt thấp hơn mức công ty · chú ý ngang mức công ty · báo động cao hơn rõ, hoặc mất người chủ chốt
- Mẹo: Không chỉ bao nhiêu người đi, mà ai đi.
- Bẫy: Chỉ đếm số người, không xem ai nghỉ.
### BUS · Bus Factor
- 属人化リスク (zokujinka risuku)
- Công thức: Số người ít nhất mà nếu cùng vắng thì một module/kiến thức bị đình trệ (đo theo từng module)
- Ngưỡng (tham khảo): tốt ≥ 2 ở mọi module quan trọng · chú ý = 1 ở module phụ · báo động = 1 ở module chủ chốt hoặc BrSE
- Mẹo: Nếu 1 người nghỉ đột ngột, dự án có dừng không?
- Bẫy: Bus factor bằng 1 ở BrSE, kênh duy nhất với khách.
### PROD · Productivity
- 生産性 (seisansei)
- Công thức: PROD = quy mô sản phẩm ÷ effort  (vd FP/人月, KLOC/人月)
- Ngưỡng (tham khảo): tốt gần mức lịch sử · chú ý lệch 10 – 20% · báo động lệch > 20%
- Mẹo: 'Mỗi người-tháng làm ra được bao nhiêu?'
- Bẫy: So năng suất giữa các dự án khác ngôn ngữ, khác domain, khác mức tài liệu.
### TTP · Time to Productivity
- 戦力化までの期間 (senryokuka made no kikan)
- Công thức: Số tuần từ ngày vào dự án tới khi người mới tự hoàn thành task chuẩn (vd đạt khoảng 80% năng suất trung bình)
- Ngưỡng (tham khảo): tốt ≤ 2 – 4 tuần · chú ý 4 – 8 tuần · báo động > 8 tuần
- Mẹo: 'Người mới chín sau mấy tuần?'
- Bẫy: Ramp-up nhiều người cùng lúc mà không tính TTP, kế hoạch quá lạc quan.

## 7. Khách có hài lòng không? (CLIENT)
### CSAT · Customer Satisfaction
- 顧客満足度 (kokyaku manzokudo)
- Công thức: Điểm khảo sát trung bình (thang 1–5 hoặc 1–10), theo kỳ hoặc sau mỗi milestone
- Ngưỡng (tham khảo): tốt ≥ 8/10 (≥ 4/5) · chú ý 6 – 8 · báo động < 6
- Mẹo: Hỏi định kỳ, hỏi đúng người, hỏi theo mục.
- Bẫy: Chỉ hỏi 窓口 thân thiện; nên hỏi cả người duyệt và người dùng nghiệp vụ.
### NPS · Net Promoter Score
- ネットプロモータースコア (netto puromōtā sukoa)
- Công thức: NPS = % chấm 9–10 (ủng hộ) − % chấm 0–6 (chê), với câu hỏi 'khả năng giới thiệu' thang 0–10
- Ngưỡng (tham khảo): tốt > +30 · chú ý 0 – +30 · báo động < 0
- Mẹo: Ủng hộ trừ chê; người chấm 7–8 không tính.
- Bẫy: Dự án B2B có ít người trả lời, con số dao động mạnh; đọc kèm nhận xét.
### QART · Q&A Response Time
- QA回答日数 (kyū-ē kaitō nissū)
- Công thức: Số ngày trung bình từ lúc gửi câu hỏi tới lúc có trả lời (đo cả hai chiều)
- Ngưỡng (tham khảo): tốt ≤ 2 ngày · chú ý 3 – 5 ngày · báo động > 5 ngày hoặc có câu quá hạn chặn việc
- Mẹo: Mỗi ngày chờ câu trả lời là một ngày trễ tiềm ẩn.
- Bẫy: Không đo phía khách, nên khi trễ vì chờ khách thì không có căn cứ.
### IAGE · Issue Aging
- 課題滞留日数 (kadai tairyū nissū)
- Công thức: Số ngày từ lúc mở issue tới hôm nay (với issue còn mở); theo dõi các issue tồn quá N ngày
- Ngưỡng (tham khảo): tốt không có issue quá hạn · chú ý 1 – 2 issue quá hạn · báo động issue quá hạn chặn critical path
- Mẹo: Issue để lâu thành rủi ro, rủi ro để lâu thành sự cố.
- Bẫy: Đóng issue không có kết luận để giảm số.
### CLM · Complaints
- クレーム件数 (kurēmu kensū)
- Công thức: Số lần khách phàn nàn trong kỳ, phân theo loại (chất lượng, tiến độ, giao tiếp)
- Ngưỡng (tham khảo): tốt 0 · chú ý 1, đã xử lý xong · báo động ≥ 2 hoặc lặp lại cùng loại
- Mẹo: Một lời nhắc nhẹ của khách Nhật bằng một lời khiếu nại.
- Bẫy: Chỉ đếm khiếu nại bằng văn bản; khách Nhật hay 'nhắc nhẹ' trong họp, cũng phải ghi.

## 8. Hệ thống chạy ổn không? (OPERATIONS)
### AVL · Availability
- システム稼働率 (shisutemu kadō-ritsu)
- Công thức: AVL = thời gian hoạt động ÷ tổng thời gian cam kết × 100%  ·  ≈ MTBF ÷ (MTBF + MTTR)
- Ngưỡng (tham khảo): tốt ≥ SLA · chú ý sát SLA · báo động < SLA
- Mẹo: 99,9% ≈ 43 phút/tháng; 99,99% ≈ 4 phút/tháng.
- Bẫy: Không nói rõ có loại trừ thời gian bảo trì kế hoạch hay không. Và 稼働率 còn nghĩa là utilization của người.
### SLO · SLI / SLO / SLA
- SLI・SLO・SLA (esu-eru-ai, esu-eru-ō, esu-eru-ē)
- Công thức: SLI = số đo thực tế (vd % request < 400ms)  ·  SLO = mục tiêu nội bộ cho SLI  ·  SLA = cam kết hợp đồng, có phạt
- Ngưỡng (tham khảo): tốt SLI ≥ SLO · chú ý SLA ≤ SLI < SLO · báo động SLI < SLA
- Mẹo: I = đo · O = nhắm · A = hứa trên giấy (có phạt).
- Bẫy: Đặt SLO bằng SLA, không còn vùng đệm để cảnh báo.
### MTTR · Mean Time to Restore
- 平均復旧時間 (heikin fukkyū jikan)
- Công thức: MTTR = tổng thời gian khôi phục ÷ số sự cố
- Ngưỡng (tham khảo): tốt đạt SLA khôi phục · chú ý sát SLA · báo động vượt SLA
- Mẹo: 'Ngã rồi, bao lâu đứng dậy?'
- Bẫy: Đo từ lúc phát hiện thay vì từ lúc xảy ra, che mất việc phát hiện chậm.
### MTBF · Mean Time Between Failures
- 平均故障間隔 (heikin koshō kankaku)
- Công thức: MTBF = tổng thời gian hoạt động ÷ số sự cố
- Ngưỡng (tham khảo): tốt tăng hoặc ổn định · chú ý giảm nhẹ · báo động giảm mạnh
- Mẹo: 'Bao lâu thì ngã một lần?'
- Bẫy: Gộp sự cố nhỏ và lớn, con số không phản ánh rủi ro thật.
### CFR · Change Failure Rate
- 変更失敗率 (henkō shippai-ritsu)
- Công thức: CFR = số lần deploy gây sự cố, rollback hoặc hotfix ÷ tổng số lần deploy × 100%
- Ngưỡng (tham khảo): tốt ≤ 15% · chú ý 15 – 30% · báo động > 30%
- Mẹo: 'Mười lần lên production, mấy lần quay xe?'
- Bẫy: Không tính các hotfix vội sau release là 'thất bại'.
### DF · Deployment Frequency
- デプロイ頻度 (depuroi hindo)
- Công thức: DF = số lần deploy production ÷ kỳ
- Ngưỡng (tham khảo): tốt đúng nhịp đã thống nhất · chú ý chậm hơn nhịp · báo động dồn release lớn, hiếm
- Mẹo: 'Bao lâu ship một lần?'
- Bẫy: Khách tài chính Nhật thường release theo lịch cố định (tháng/quý); không áp chỉ số DORA một cách máy móc.
### LTC · Lead Time for Changes
- 変更のリードタイム (henkō no rīdo taimu)
- Công thức: LTC = thời điểm chạy production − thời điểm commit
- Ngưỡng (tham khảo): tốt ổn định hoặc giảm · chú ý tăng nhẹ · báo động tăng mạnh
- Mẹo: Từ code xong tới khách dùng được.
- Bẫy: Nhầm với lead time tính từ lúc khách yêu cầu (LT).
### p95 · Latency p95
- 95パーセンタイル応答時間 (kyūjūgo pāsentairu ōtō jikan)
- Công thức: p95 = giá trị mà 95% request nhanh hơn
- Ngưỡng (tham khảo): tốt ≤ mục tiêu NFR · chú ý vượt ≤ 20% · báo động vượt > 20%
- Mẹo: Trung bình dễ nói dối; percentile nói thật hơn.
- Bẫy: Báo trung bình (average) che đi nhóm request rất chậm.
### INC · Incident Count
- 障害件数 (shōgai kensū)
- Công thức: Số sự cố production trong kỳ, theo mức độ (P1–P4) và theo nguyên nhân
- Ngưỡng (tham khảo): tốt 0 P1 · chú ý có P2 đã xử lý xong · báo động có P1 hoặc lặp lại cùng nguyên nhân
- Mẹo: Đếm theo mức độ và nguyên nhân, đừng đếm tổng.
- Bẫy: Chỉ đếm tổng; không thấy sự cố lặp lại. Khách Nhật rất nhạy với sự cố lặp lại.

## 9. Dự án có lãi không? (BUSINESS)
### GM · Gross Margin
- 粗利率 (arari-ritsu)
- Công thức: GM = (doanh thu − chi phí trực tiếp) ÷ doanh thu × 100%
- Ngưỡng (tham khảo): tốt ≥ mục tiêu công ty · chú ý thấp hơn ≤ 5 điểm · báo động thấp hơn > 5 điểm hoặc lỗ
- Mẹo: 'Thu về bao nhiêu thì giữ lại bao nhiêu?'
- Bẫy: Không tính rework, CR chưa duyệt, BrSE, onsite vào chi phí, margin thành ảo.
### RPH · Revenue per Head
- 一人当たり売上 (hitori atari uriage)
- Công thức: RPH = doanh thu ÷ số người bình quân trong kỳ
- Ngưỡng (tham khảo): tốt tăng hoặc ổn định · chú ý giảm nhẹ · báo động giảm mạnh
- Mẹo: 'Mỗi người mang về bao nhiêu?'
- Bẫy: Tăng RPH bằng cách giảm người mà giữ nguyên phạm vi, team quá tải và chất lượng giảm.
### BCH · Bench Rate
- 待機率 (taiki-ritsu)
- Công thức: BCH = số người không có dự án tính tiền ÷ tổng số người × 100%
- Ngưỡng (tham khảo): tốt ≤ 5 – 10% · chú ý 10 – 15% · báo động > 15%
- Mẹo: Ghế chờ trống quá thì lỗ, đầy quá thì không có người dự phòng.
- Bẫy: Bench bằng 0 nghe tốt, nhưng không còn người dự phòng khi khách cần ramp-up gấp.

## Đừng nhầm
### SV và SPI
- SV = EV − PV: chênh lệch, đơn vị tiền/人月
- SPI = EV ÷ PV: tỉ lệ, không đơn vị
- Mẹo: Cả hai đều KHÔNG ra số ngày. Muốn nói 'trễ mấy ngày' thì xem lịch (SLIP).
### SPI và CPI
- SPI so với kế hoạch tiến độ (PV)
- CPI so với chi phí thực tế (AC)
- Mẹo: Chia 4 ô: SPI < 1 và CPI < 1 là xấu nhất; SPI > 1 mà CPI < 1 là đang đốt tiền để chạy nhanh; SPI < 1 mà CPI > 1 thường là thiếu người.
### EAC và ETC · VAC
- EAC: tổng chi phí dự báo khi xong
- ETC: phần còn phải tiêu (EAC − AC)
- VAC: hụt so với ngân sách (BAC − EAC)
- Mẹo: Tổng – Còn lại – Hụt.
### TCPI và CPI
- CPI: hiệu suất ĐÃ đạt
- TCPI: hiệu suất CẦN đạt cho phần còn lại
- Mẹo: TCPI cao hơn CPI nhiều thì ngân sách gốc không còn khả thi.
### Lead time và Cycle time
- Lead time: từ lúc khách yêu cầu tới lúc giao
- Cycle time: từ lúc team bắt tay tới lúc xong
- Mẹo: Lead = góc khách; Cycle = góc team. Lead time = thời gian chờ + cycle time.
### Velocity và Throughput
- Velocity: tổng story point Done mỗi sprint
- Throughput: số item xong mỗi kỳ, không cần point
- Mẹo: Team bảo trì, ticket đều cỡ: throughput dễ dùng hơn.
### テスト消化率 và テスト合格率
- 消化率: đã chạy bao nhiêu % case
- 合格率: trong số đã chạy, bao nhiêu % đạt
- Mẹo: Báo cả hai: chạy 100% mà đạt 70% thì chưa xong.
### バグ密度 và 流出率
- バグ密度: bug trên mỗi KLOC/FP, đo hiệu quả test
- 流出率: phần trăm bug lọt ra tới khách
- Mẹo: Mật độ cao trong test có thể tốt (bắt được nhiều); lọt ra khách thì lúc nào cũng xấu.
### Defect leakage và DRE
- Leakage: phần trăm lọt ra
- DRE: phần trăm bắt được trước khi giao
- Mẹo: Leakage + DRE = 100%, nếu cùng mẫu số.
### Utilization và Billable rate
- Utilization: giờ làm dự án ÷ giờ có thể làm
- Billable: giờ khách trả tiền ÷ tổng giờ làm
- Mẹo: Làm nhiều (utilization cao) chưa chắc được trả tiền nhiều (billable).
### 稼働率 (người) và システム稼働率
- 稼働率 của người: utilization
- システム稼働率: availability của hệ thống
- Mẹo: Cùng chữ 稼働率; nghe ngữ cảnh 'người' hay 'hệ thống'.
### SLI · SLO và SLA
- SLI: số đo thực tế
- SLO: mục tiêu nội bộ
- SLA: cam kết hợp đồng có phạt
- Mẹo: SLO chặt hơn SLA để còn thời gian phản ứng.
### MTTR và MTBF
- MTTR: bao lâu sửa xong
- MTBF: bao lâu mới hỏng lại
- Mẹo: Availability ≈ MTBF ÷ (MTBF + MTTR): muốn tăng thì hoặc ít hỏng, hoặc sửa nhanh.
### CSAT và NPS
- CSAT: hài lòng với lần giao này
- NPS: có sẵn lòng giới thiệu không
- Mẹo: CSAT đo trải nghiệm gần; NPS đo lòng tin lâu dài.
### Scope creep và Requirement volatility
- Scope creep: phần thêm vào KHÔNG qua CR
- Volatility: mọi thay đổi yêu cầu, kể cả có CR
- Mẹo: Volatility cao vẫn ổn nếu đi qua CR; scope creep thì lúc nào cũng xấu.
### Lead time (LT) và Lead time for changes (LTC)
- LT: từ yêu cầu của khách tới lúc giao
- LTC (DORA): từ commit tới production
- Mẹo: LTC là một đoạn nằm trong LT.
