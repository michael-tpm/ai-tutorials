# Bảng tra chỉ số PM (64 chỉ số · 9 câu hỏi)

> Mỗi chỉ số trả lời 1 câu hỏi mà lãnh đạo hoặc khách sẽ hỏi. Bản tương tác có máy tính EVM, chất lượng, dự báo Agile, availability, báo cáo tuần mẫu và luyện nhớ: `bang-chi-so-PM.html` (tải về, mở bằng trình duyệt). Mindmap: [mindmap-chi-so-PM.md](mindmap-chi-so-PM.md).

**9 câu hỏi:** Có kịp không? (Tiến độ) · Có lố tiền không? (Chi phí) · Phạm vi có phình không? (Phạm vi) · Chất lượng ổn không? (Chất lượng kiểu Nhật) · Team chạy đều không? (Agile & dòng chảy) · Team có khỏe không? (Nguồn lực & con người) · Khách có hài lòng không? (Khách hàng) · Hệ thống chạy ổn không? (Vận hành & DevOps) · Dự án có lãi không? (Kinh doanh)

Ngưỡng Tốt / Chú ý / Báo động là **mức tham khảo**; dự án thật theo 品質計画書, hợp đồng (SLA) và dữ liệu lịch sử.

## 1. Có kịp không? · SCHEDULE

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | **SV** | Schedule Variance (Chênh lệch tiến độ (quy ra giá trị)) | スケジュール差異 | `SV = EV − PV` | ≥ 0 / từ −5% PV đến 0 / < −5% PV | EV trừ PV: làm được trừ dự định. |
| 2 | **SPI** | Schedule Performance Index (Chỉ số hiệu suất tiến độ) | スケジュール効率指数 | `SPI = EV ÷ PV` | ≥ 0,95 / 0,85 – 0,95 / < 0,85 | S chia: EV / PV. Dưới 1 là chậm. |
| 3 | **%C** | Percent Complete (Tỷ lệ hoàn thành) | 進捗率 | `%C = EV ÷ BAC × 100%  (hoặc số work package xong ÷ tổng)` | lệch ≤ 2 điểm % / lệch 3–5 điểm / lệch > 5 điểm | Đếm cái đã xong, đừng đếm cái 'gần xong'. |
| 4 | **OTD** | On-time Delivery Rate (Tỷ lệ giao đúng hạn) | 納期遵守率 | `OTD = số mốc/release đúng hạn ÷ số mốc/release đã đến hạn × 100%` | ≥ 95% / 85 – 95% / < 85% | Đúng hạn theo ngày ĐÃ HỨA, không theo ngày mới sửa. |
| 5 | **SLIP** | Schedule Slip (days) (Số ngày trễ so kế hoạch) | 予実差異（日数） | `SLIP = ngày xong dự báo (hoặc thực tế) − ngày baseline` | ≤ 0 / 1 – 3 ngày / > 3 ngày hoặc nằm trên critical path | Lãnh đạo hỏi 'trễ mấy ngày?', không hỏi 'SPI bao nhiêu?'. |
| 6 | **TF** | Total Float (Thời gian dự trữ) | トータルフロート | `TF = LS − ES = LF − EF` | > 5 ngày / 1 – 5 ngày / ≤ 0 | Float = khoảng 'được phép chậm' mà chưa ai thấy. |

## 2. Có lố tiền không? · COST · EVM

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 7 | **PV** | Planned Value (Giá trị kế hoạch) | 計画価値 | `PV = tổng ngân sách các việc lên lịch tới hôm nay` | – | P = Plan: 'lẽ ra'. |
| 8 | **EV** | Earned Value (Giá trị thu được) | 出来高 | `EV = % hoàn thành (đo khách quan) × BAC` | – | E = Earned: 'kiếm được thật'. |
| 9 | **AC** | Actual Cost (Chi phí thực tế) | 実コスト | `AC = tổng effort/chi phí thực tế ghi nhận tới hôm nay` | – | A = Actual: 'đã tiêu thật'. |
| 10 | **CV** | Cost Variance (Chênh lệch chi phí) | コスト差異 | `CV = EV − AC` | ≥ 0 / từ −5% EV đến 0 / < −5% EV | EV trừ AC: làm được trừ đã tiêu. |
| 11 | **CPI** | Cost Performance Index (Chỉ số hiệu suất chi phí) | コスト効率指数 | `CPI = EV ÷ AC` | ≥ 0,95 / 0,85 – 0,95 / < 0,85 | C chia: EV / AC. Dưới 1 là lố. |
| 12 | **EAC** | Estimate at Completion (Dự báo tổng chi phí khi hoàn thành) | 完成時総コスト見積 | `EAC = BAC ÷ CPI  ·  = AC + (BAC − EV)  ·  = AC + (BAC − EV) ÷ (CPI × SPI)  ·  = AC + ETC (ước lại từ dưới lên)` | ≤ BAC / BAC đến +5% / > BAC + 5% | 'Nếu cứ thế này thì cuối cùng tốn bao nhiêu?' |
| 13 | **ETC** | Estimate to Complete (Dự báo chi phí còn lại) | 残作業見積 | `ETC = EAC − AC  (hoặc estimate lại phần còn lại từ dưới lên)` | ≤ BAC − AC / vượt nhẹ / vượt nhiều | 'Còn phải tiêu bao nhiêu nữa?' |
| 14 | **VAC** | Variance at Completion (Chênh lệch khi hoàn thành) | 完成時差異 | `VAC = BAC − EAC` | ≥ 0 / từ −5% BAC đến 0 / < −5% BAC | 'Cuối cùng hụt bao nhiêu?' |
| 15 | **TCPI** | To-Complete Performance Index (Hiệu suất cần đạt cho phần còn lại) | 残作業効率指数 | `TCPI = (BAC − EV) ÷ (BAC − AC)  (giữ BAC)  ·  = (BAC − EV) ÷ (EAC − AC)  (theo EAC mới)` | ≤ CPI hiện tại / cao hơn CPI ≤ 0,1 / cao hơn CPI > 0,1 | 'Từ giờ phải giỏi lên bao nhiêu mới kịp tiền?' |
| 16 | **EFV** | Effort Variance (Chênh lệch công số) | 工数予実差異 | `EFV = (effort thực tế − effort kế hoạch) ÷ effort kế hoạch × 100%` | ±5% / ±5 – 15% / > ±15% | 'Tốn công hơn dự tính bao nhiêu, ở đâu?' |
| 17 | **EA** | Estimate Accuracy (Độ chính xác estimate) | 見積精度 | `Sai lệch = (thực tế − estimate) ÷ estimate × 100%  (đo khi đóng dự án/phase)` | ±10% / ±10 – 20% / > ±20% | Dự đoán giỏi cỡ nào? Đo ở cuối, dùng cho lần sau. |

## 3. Phạm vi có phình không? · SCOPE

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 18 | **SCR** | Scope Creep (Tỷ lệ phạm vi phình ngầm) | スコープクリープ率 | `SCR = effort (hoặc số yêu cầu) thêm vào KHÔNG qua CR ÷ baseline × 100%` | < 5% / 5 – 10% / > 10% | Creep = bò lén vào. Có CR thì không còn là creep. |
| 19 | **CRA** | CR Approval Rate (Tỷ lệ CR được duyệt) | 変更要求承認率 | `CRA = số CR (追加見積) khách duyệt ÷ số CR đã gửi × 100%` | ≥ 80% / 60 – 80% / < 60% | 'Gửi 10 CR, khách gật mấy cái?' |
| 20 | **RV** | Requirement Volatility (Tỷ lệ thay đổi yêu cầu) | 要件変更率 | `RV = (số yêu cầu thêm + sửa + xóa trong kỳ) ÷ tổng yêu cầu baseline × 100%` | < 10% mỗi phase / 10 – 20% / > 20% | 'Yêu cầu đang rung bao nhiêu?' |
| 21 | **RCOV** | Requirement Coverage (Độ phủ yêu cầu bằng test) | 要件カバレッジ | `RCOV = số yêu cầu có test case đã chạy đạt ÷ tổng yêu cầu × 100%` | 100% trước UAT / 95 – 99% / < 95% | 'Yêu cầu nào chưa có ai kiểm?' |

## 4. Chất lượng ổn không? · QUALITY

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 22 | **TD** | Test Density (Mật độ test) | テスト密度 | `TD = số test case ÷ quy mô (KLOC hoặc FP)` | trong khoảng ngưỡng / lệch ±20% ngưỡng / ngoài ±20% | 'Mỗi 1.000 dòng code được bắn bao nhiêu phát?' |
| 23 | **BD** | Bug Density (Mật độ bug) | バグ密度 | `BD = số bug phát hiện ÷ quy mô (KLOC hoặc FP), tính riêng từng mức test` | trong khoảng ngưỡng / lệch nhẹ / ngoài khoảng (cả cao lẫn thấp) | Thấp quá cũng đáng ngờ như cao quá. |
| 24 | **RCD** | Review Comment Density (Mật độ điểm chỉ ra khi review) | レビュー指摘密度 | `RCD = số 指摘 (điểm chỉ ra) ÷ quy mô (trang tài liệu hoặc KLOC)` | trong khoảng ngưỡng / lệch nhẹ / ngoài khoảng | Bắt lỗi trên giấy rẻ hơn bắt lỗi trong code. |
| 25 | **RER** | Review Effort Ratio (Tỷ lệ công dành cho review) | レビュー工数比率 | `RER = effort review ÷ effort tạo tài liệu/code × 100%` | 10 – 20% / 5 – 10% / < 5% | Review là bảo hiểm rẻ nhất. |
| 26 | **DL** | Defect Leakage (Tỷ lệ lọt lỗi ra khách) | 流出率 | `DL = bug khách/UAT/production phát hiện ÷ (bug nội bộ phát hiện + bug lọt ra) × 100%` | < 5% / 5 – 10% / > 10% | 'Lọt qua lưới bao nhiêu phần trăm?' |
| 27 | **DRE** | Defect Removal Efficiency (Hiệu quả loại bỏ lỗi) | 欠陥除去率 | `DRE = bug bắt trước release ÷ (bug trước release + bug sau release) × 100%  = 100% − DL` | ≥ 95% / 90 – 95% / < 90% | DRE + Leakage = 100%. |
| 28 | **BCV** | Bug Convergence (Độ hội tụ bug) | バグ収束・信頼度成長曲線 | `Vẽ số bug tích lũy theo ngày (hoặc theo số case đã chạy); hội tụ khi đường cong nằm ngang trong lúc vẫn đang chạy test` | nằm ngang ở 20% case cuối / đang cong xuống / vẫn dốc lên | Nằm ngang = gần hết bug, nếu vẫn đang test. |
| 29 | **RW** | Rework Rate (Tỷ lệ làm lại) | 手戻り率 | `RW = effort làm lại (sửa spec, thiết kế, code do lỗi) ÷ tổng effort × 100%` | < 10% / 10 – 20% / > 20% | Làm hai lần một việc là trả tiền hai lần. |
| 30 | **TEX** | Test Execution Rate (Tỷ lệ case đã chạy) | テスト消化率 | `TEX = số case đã chạy ÷ tổng case kế hoạch × 100%` | đúng hoặc vượt kế hoạch / chậm ≤ 5 điểm / chậm > 5 điểm | 消化 = đã 'ăn' được bao nhiêu case. |
| 31 | **TPR** | Test Pass Rate (Tỷ lệ case đạt) | テスト合格率 | `TPR = số case đạt ÷ số case đã chạy × 100%` | ≥ 95% / 90 – 95% / < 90% | 合格 = đậu. |
| 32 | **C0/C1** | Code Coverage (Độ phủ code) | コードカバレッジ | `C0 (statement) = số lệnh đã chạy ÷ tổng lệnh  ·  C1 (branch) = số nhánh đã chạy ÷ tổng nhánh` | đạt ngưỡng / thấp hơn 5 – 10 điểm / thấp hơn > 10 điểm | C0 = dòng, C1 = nhánh. |
| 33 | **OPB** | Open Bugs by Severity (Bug còn mở theo mức độ) | 未解決バグ（重要度別） | `Đếm bug chưa đóng theo severity (Critical / High / Medium / Low), kèm tuổi bug` | 0 Critical, 0 High / còn High có workaround / còn Critical | Đếm theo mức đau, đừng đếm tổng. |

## 5. Team chạy đều không? · AGILE · FLOW

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 34 | **VEL** | Velocity (Tốc độ sprint) | ベロシティ | `VEL = tổng story point của các story Done trong 1 sprint (dùng trung bình 3–5 sprint gần nhất)` | dao động ≤ ±15% / ±15 – 30% / > ±30% | Velocity là đồng hồ tốc độ của 1 xe, không phải để đua giữa 2 xe. |
| 35 | **SDR** | Say/Do Ratio (Tỷ lệ giữ cam kết sprint) | コミットメント達成率 | `SDR = điểm Done ÷ điểm cam kết đầu sprint × 100%` | 85 – 100% / 70 – 85% / < 70% hoặc liên tục > 110% | 'Nói 10 làm mấy?' |
| 36 | **BDN** | Burndown (Biểu đồ đốt việc) | バーンダウンチャート | `Đường việc còn lại (điểm hoặc giờ) theo ngày, so với đường lý tưởng` | bám đường lý tưởng / lệch nhưng đang hội tụ / đi ngang hoặc tăng | Đi ngang = kẹt; nhảy lên = thêm việc. |
| 37 | **LT** | Lead Time (Thời gian từ lúc yêu cầu tới lúc giao) | リードタイム | `LT = thời điểm giao − thời điểm yêu cầu được tạo` | ≤ SLA / vượt SLA ≤ 20% / vượt SLA > 20% | Lead = góc nhìn khách: từ lúc xin tới lúc nhận. |
| 38 | **CT** | Cycle Time (Thời gian xử lý) | サイクルタイム | `CT = thời điểm xong − thời điểm bắt đầu làm  ·  Little's Law: CT ≈ WIP ÷ Throughput` | ổn định hoặc giảm / tăng ≤ 20% / tăng > 20% | Cycle = góc nhìn team: từ lúc bắt tay tới lúc xong. |
| 39 | **THR** | Throughput (Thông lượng) | スループット | `THR = số item hoàn thành ÷ kỳ` | ổn định / giảm ~20% / giảm > 30% | 'Mỗi tuần ra lò bao nhiêu việc?' |
| 40 | **WIP** | Work in Progress (Việc đang làm dở) | 仕掛り作業 | `WIP = số item ở trạng thái 'đang làm'  ·  CT ≈ WIP ÷ Throughput` | ≤ giới hạn WIP / vượt nhẹ / vượt nhiều, việc tồn lâu | Ít dở dang thì nhanh xong. |

## 6. Team có khỏe không? · PEOPLE

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 41 | **UTL** | Utilization (Tỷ lệ sử dụng nguồn lực) | 稼働率 | `UTL = giờ làm việc dự án ÷ giờ có thể làm × 100%` | 75 – 85% / 85 – 95% hoặc 60 – 75% / > 95% hoặc < 60% | 100% giống đường kẹt xe: không còn chỗ để xoay. |
| 42 | **BIL** | Billable Rate (Tỷ lệ giờ tính tiền được) | 請求可能率 | `BIL = giờ tính tiền khách ÷ tổng giờ làm × 100%` | ≥ 80% / 70 – 80% / < 70% | 'Giờ nào khách trả tiền?' |
| 43 | **OT** | Overtime Hours (Giờ làm thêm) | 残業時間 | `OT/người/tháng = tổng giờ OT ÷ số người` | thấp, ổn định / tăng 2 tuần liền / vượt giới hạn công ty/luật hoặc kéo dài > 1 tháng | OT là cơn sốt: chữa nguyên nhân, đừng chỉ hạ sốt. |
| 44 | **ATR** | Attrition Rate (Tỷ lệ nghỉ việc) | 離職率 | `ATR = số người nghỉ trong kỳ ÷ số người bình quân × 100% (thường tính theo năm)` | thấp hơn mức công ty / ngang mức công ty / cao hơn rõ, hoặc mất người chủ chốt | Không chỉ bao nhiêu người đi, mà ai đi. |
| 45 | **BUS** | Bus Factor (Số người 'không thể mất') | 属人化リスク | `Số người ít nhất mà nếu cùng vắng thì một module/kiến thức bị đình trệ (đo theo từng module)` | ≥ 2 ở mọi module quan trọng / = 1 ở module phụ / = 1 ở module chủ chốt hoặc BrSE | Nếu 1 người nghỉ đột ngột, dự án có dừng không? |
| 46 | **PROD** | Productivity (Năng suất) | 生産性 | `PROD = quy mô sản phẩm ÷ effort  (vd FP/人月, KLOC/人月)` | gần mức lịch sử / lệch 10 – 20% / lệch > 20% | 'Mỗi người-tháng làm ra được bao nhiêu?' |
| 47 | **TTP** | Time to Productivity (Thời gian để người mới làm được việc) | 戦力化までの期間 | `Số tuần từ ngày vào dự án tới khi người mới tự hoàn thành task chuẩn (vd đạt khoảng 80% năng suất trung bình)` | ≤ 2 – 4 tuần / 4 – 8 tuần / > 8 tuần | 'Người mới chín sau mấy tuần?' |

## 7. Khách có hài lòng không? · CLIENT

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 48 | **CSAT** | Customer Satisfaction (Mức hài lòng của khách) | 顧客満足度 | `Điểm khảo sát trung bình (thang 1–5 hoặc 1–10), theo kỳ hoặc sau mỗi milestone` | ≥ 8/10 (≥ 4/5) / 6 – 8 / < 6 | Hỏi định kỳ, hỏi đúng người, hỏi theo mục. |
| 49 | **NPS** | Net Promoter Score (Chỉ số sẵn lòng giới thiệu) | ネットプロモータースコア | `NPS = % chấm 9–10 (ủng hộ) − % chấm 0–6 (chê), với câu hỏi 'khả năng giới thiệu' thang 0–10` | > +30 / 0 – +30 / < 0 | Ủng hộ trừ chê; người chấm 7–8 không tính. |
| 50 | **QART** | Q&A Response Time (Thời gian trả lời Q&A) | QA回答日数 | `Số ngày trung bình từ lúc gửi câu hỏi tới lúc có trả lời (đo cả hai chiều)` | ≤ 2 ngày / 3 – 5 ngày / > 5 ngày hoặc có câu quá hạn chặn việc | Mỗi ngày chờ câu trả lời là một ngày trễ tiềm ẩn. |
| 51 | **IAGE** | Issue Aging (Số ngày vấn đề còn tồn) | 課題滞留日数 | `Số ngày từ lúc mở issue tới hôm nay (với issue còn mở); theo dõi các issue tồn quá N ngày` | không có issue quá hạn / 1 – 2 issue quá hạn / issue quá hạn chặn critical path | Issue để lâu thành rủi ro, rủi ro để lâu thành sự cố. |
| 52 | **CLM** | Complaints (Số lần khách phàn nàn) | クレーム件数 | `Số lần khách phàn nàn trong kỳ, phân theo loại (chất lượng, tiến độ, giao tiếp)` | 0 / 1, đã xử lý xong / ≥ 2 hoặc lặp lại cùng loại | Một lời nhắc nhẹ của khách Nhật bằng một lời khiếu nại. |

## 8. Hệ thống chạy ổn không? · OPERATIONS

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 53 | **AVL** | Availability (Tỷ lệ sẵn sàng của hệ thống) | システム稼働率 | `AVL = thời gian hoạt động ÷ tổng thời gian cam kết × 100%  ·  ≈ MTBF ÷ (MTBF + MTTR)` | ≥ SLA / sát SLA / < SLA | 99,9% ≈ 43 phút/tháng; 99,99% ≈ 4 phút/tháng. |
| 54 | **SLO** | SLI / SLO / SLA (Chỉ số, mục tiêu và cam kết dịch vụ) | SLI・SLO・SLA | `SLI = số đo thực tế (vd % request < 400ms)  ·  SLO = mục tiêu nội bộ cho SLI  ·  SLA = cam kết hợp đồng, có phạt` | SLI ≥ SLO / SLA ≤ SLI < SLO / SLI < SLA | I = đo · O = nhắm · A = hứa trên giấy (có phạt). |
| 55 | **MTTR** | Mean Time to Restore (Thời gian khôi phục trung bình) | 平均復旧時間 | `MTTR = tổng thời gian khôi phục ÷ số sự cố` | đạt SLA khôi phục / sát SLA / vượt SLA | 'Ngã rồi, bao lâu đứng dậy?' |
| 56 | **MTBF** | Mean Time Between Failures (Thời gian trung bình giữa hai sự cố) | 平均故障間隔 | `MTBF = tổng thời gian hoạt động ÷ số sự cố` | tăng hoặc ổn định / giảm nhẹ / giảm mạnh | 'Bao lâu thì ngã một lần?' |
| 57 | **CFR** | Change Failure Rate (Tỷ lệ deploy gây lỗi (DORA)) | 変更失敗率 | `CFR = số lần deploy gây sự cố, rollback hoặc hotfix ÷ tổng số lần deploy × 100%` | ≤ 15% / 15 – 30% / > 30% | 'Mười lần lên production, mấy lần quay xe?' |
| 58 | **DF** | Deployment Frequency (Tần suất deploy (DORA)) | デプロイ頻度 | `DF = số lần deploy production ÷ kỳ` | đúng nhịp đã thống nhất / chậm hơn nhịp / dồn release lớn, hiếm | 'Bao lâu ship một lần?' |
| 59 | **LTC** | Lead Time for Changes (Thời gian từ commit tới production (DORA)) | 変更のリードタイム | `LTC = thời điểm chạy production − thời điểm commit` | ổn định hoặc giảm / tăng nhẹ / tăng mạnh | Từ code xong tới khách dùng được. |
| 60 | **p95** | Latency p95 (Thời gian phản hồi phân vị 95) | 95パーセンタイル応答時間 | `p95 = giá trị mà 95% request nhanh hơn` | ≤ mục tiêu NFR / vượt ≤ 20% / vượt > 20% | Trung bình dễ nói dối; percentile nói thật hơn. |
| 61 | **INC** | Incident Count (Số sự cố production) | 障害件数 | `Số sự cố production trong kỳ, theo mức độ (P1–P4) và theo nguyên nhân` | 0 P1 / có P2 đã xử lý xong / có P1 hoặc lặp lại cùng nguyên nhân | Đếm theo mức độ và nguyên nhân, đừng đếm tổng. |

## 9. Dự án có lãi không? · BUSINESS

| # | Ký hiệu | Tên | Tiếng Nhật | Công thức | Tốt / Chú ý / Báo động | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 62 | **GM** | Gross Margin (Biên lợi nhuận gộp) | 粗利率 | `GM = (doanh thu − chi phí trực tiếp) ÷ doanh thu × 100%` | ≥ mục tiêu công ty / thấp hơn ≤ 5 điểm / thấp hơn > 5 điểm hoặc lỗ | 'Thu về bao nhiêu thì giữ lại bao nhiêu?' |
| 63 | **RPH** | Revenue per Head (Doanh thu bình quân đầu người) | 一人当たり売上 | `RPH = doanh thu ÷ số người bình quân trong kỳ` | tăng hoặc ổn định / giảm nhẹ / giảm mạnh | 'Mỗi người mang về bao nhiêu?' |
| 64 | **BCH** | Bench Rate (Tỷ lệ người chờ dự án) | 待機率 | `BCH = số người không có dự án tính tiền ÷ tổng số người × 100%` | ≤ 5 – 10% / 10 – 15% / > 15% | Ghế chờ trống quá thì lỗ, đầy quá thì không có người dự phòng. |

## Báo cáo tuần mẫu (ví dụ minh họa)

| Chỉ số | Giá trị | Màu | Ghi chú |
| --- | --- | --- | --- |
| SPI | 0,93 | Vàng | Chậm 7% khối lượng; nguyên nhân: chờ khách trả lời Q&A |
| CPI | 0,98 | Xanh | Chi phí sát kế hoạch |
| SLIP | +2 ngày | Vàng | Mốc 基本設計 dời từ 15/11 sang 19/11; chưa ảnh hưởng 納期 |
| QART | 4 câu quá hạn | Đỏ | Cần khách trả lời trước thứ Sáu để giữ mốc |
| IAGE | 1 issue > 10 ngày | Vàng | Môi trường test phía khách |
| BCV | đang hội tụ | Xanh | Bug mới/ngày giảm từ 12 xuống 2 |
| DL | 3% | Xanh | Release tháng trước: 3 bug khách báo / 100 bug |
| OT | 11 giờ/người | Xanh | Trong mức cho phép |
| CSAT | 8,2 / 10 | Xanh | Khảo sát sau milestone 2 |

## 16 cặp chỉ số hay nhầm

- **SV và SPI**: SV = EV − PV: chênh lệch, đơn vị tiền/人月; SPI = EV ÷ PV: tỉ lệ, không đơn vị. _Mẹo:_ Cả hai đều KHÔNG ra số ngày. Muốn nói 'trễ mấy ngày' thì xem lịch (SLIP).
- **SPI và CPI**: SPI so với kế hoạch tiến độ (PV); CPI so với chi phí thực tế (AC). _Mẹo:_ Chia 4 ô: SPI < 1 và CPI < 1 là xấu nhất; SPI > 1 mà CPI < 1 là đang đốt tiền để chạy nhanh; SPI < 1 mà CPI > 1 thường là thiếu người.
- **EAC và ETC · VAC**: EAC: tổng chi phí dự báo khi xong; ETC: phần còn phải tiêu (EAC − AC); VAC: hụt so với ngân sách (BAC − EAC). _Mẹo:_ Tổng – Còn lại – Hụt.
- **TCPI và CPI**: CPI: hiệu suất ĐÃ đạt; TCPI: hiệu suất CẦN đạt cho phần còn lại. _Mẹo:_ TCPI cao hơn CPI nhiều thì ngân sách gốc không còn khả thi.
- **Lead time và Cycle time**: Lead time: từ lúc khách yêu cầu tới lúc giao; Cycle time: từ lúc team bắt tay tới lúc xong. _Mẹo:_ Lead = góc khách; Cycle = góc team. Lead time = thời gian chờ + cycle time.
- **Velocity và Throughput**: Velocity: tổng story point Done mỗi sprint; Throughput: số item xong mỗi kỳ, không cần point. _Mẹo:_ Team bảo trì, ticket đều cỡ: throughput dễ dùng hơn.
- **テスト消化率 và テスト合格率**: 消化率: đã chạy bao nhiêu % case; 合格率: trong số đã chạy, bao nhiêu % đạt. _Mẹo:_ Báo cả hai: chạy 100% mà đạt 70% thì chưa xong.
- **バグ密度 và 流出率**: バグ密度: bug trên mỗi KLOC/FP, đo hiệu quả test; 流出率: phần trăm bug lọt ra tới khách. _Mẹo:_ Mật độ cao trong test có thể tốt (bắt được nhiều); lọt ra khách thì lúc nào cũng xấu.
- **Defect leakage và DRE**: Leakage: phần trăm lọt ra; DRE: phần trăm bắt được trước khi giao. _Mẹo:_ Leakage + DRE = 100%, nếu cùng mẫu số.
- **Utilization và Billable rate**: Utilization: giờ làm dự án ÷ giờ có thể làm; Billable: giờ khách trả tiền ÷ tổng giờ làm. _Mẹo:_ Làm nhiều (utilization cao) chưa chắc được trả tiền nhiều (billable).
- **稼働率 (người) và システム稼働率**: 稼働率 của người: utilization; システム稼働率: availability của hệ thống. _Mẹo:_ Cùng chữ 稼働率; nghe ngữ cảnh 'người' hay 'hệ thống'.
- **SLI · SLO và SLA**: SLI: số đo thực tế; SLO: mục tiêu nội bộ; SLA: cam kết hợp đồng có phạt. _Mẹo:_ SLO chặt hơn SLA để còn thời gian phản ứng.
- **MTTR và MTBF**: MTTR: bao lâu sửa xong; MTBF: bao lâu mới hỏng lại. _Mẹo:_ Availability ≈ MTBF ÷ (MTBF + MTTR): muốn tăng thì hoặc ít hỏng, hoặc sửa nhanh.
- **CSAT và NPS**: CSAT: hài lòng với lần giao này; NPS: có sẵn lòng giới thiệu không. _Mẹo:_ CSAT đo trải nghiệm gần; NPS đo lòng tin lâu dài.
- **Scope creep và Requirement volatility**: Scope creep: phần thêm vào KHÔNG qua CR; Volatility: mọi thay đổi yêu cầu, kể cả có CR. _Mẹo:_ Volatility cao vẫn ổn nếu đi qua CR; scope creep thì lúc nào cũng xấu.
- **Lead time (LT) và Lead time for changes (LTC)**: LT: từ yêu cầu của khách tới lúc giao; LTC (DORA): từ commit tới production. _Mẹo:_ LTC là một đoạn nằm trong LT.
