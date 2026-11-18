# Bảng tra nhanh tài liệu PM (55 tài liệu · 11 câu hỏi)

> Mỗi tài liệu trả lời đúng 1 câu hỏi. Nhớ câu hỏi là nhớ được tài liệu. Bản tương tác có bảng tuần hoàn, họ xBS, chữ V, cặp hay nhầm và luyện nhớ: `bang-tuan-hoan-tai-lieu-PM.html` (tải về, mở bằng trình duyệt). Mindmap: [mindmap-tai-lieu-PM.md](mindmap-tai-lieu-PM.md).

**11 câu hỏi theo thứ tự câu chuyện dự án:** Vì sao làm? → Làm gì? → Chia nhỏ ra sao? → Ai làm, ai duyệt? → Làm thế nào? → Khi nào xong? → Tốn bao nhiêu? → Lệch thì sao? → Đạt chưa? → Báo ai, thế nào? → Xong chưa?

**Giai đoạn (cột GĐ):** 1 Khởi động (立ち上げ) · 2 Lập kế hoạch (計画) · 3 Yêu cầu (要件定義) · 4 Thiết kế (設計) · 5 Làm & kiểm soát (製造・テスト) · 6 Bàn giao & đóng (リリース・検収)

## 1. Vì sao làm? · WHY

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | **BC** | Business Case (Tình huống kinh doanh) | ビジネスケース・企画書 | 1 | Dự án có đáng bỏ tiền không? | BC = 'Bỏ tiền Có đáng?' |
| 2 | **PRP** | Proposal (Đề xuất giải pháp) | 提案書 | 1 | Vì sao khách nên chọn mình? | Proposal là 'lời cầu hôn': nói về người kia trước, về mình sau. |
| 3 | **SOW** | Statement of Work (Bản mô tả công việc theo hợp đồng) | 作業範囲記述書・契約別紙 | 1 | Theo hợp đồng, mình phải giao gì? | SOW = 'Sổ Ước hẹn' với khách: ghi gì làm nấy. |
| 4 | **CHT** | Project Charter (Điều lệ dự án) | プロジェクト憲章 | 1 | Ai cho phép dự án bắt đầu, PM có quyền gì? | Charter = 'giấy khai sinh' của dự án. |

## 2. Làm gì? · WHAT

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 11 | **SS** | Scope Statement (Tuyên bố phạm vi) | スコープ記述書 | 2 | Dự án làm gì và KHÔNG làm gì? | Scope Statement là 'hàng rào': vẽ rõ trong và ngoài. |
| 5 | **BRD** | Business Requirements Document (Tài liệu yêu cầu nghiệp vụ) | 業務要件定義書 | 3 | Doanh nghiệp cần đạt điều gì? | B = Business = 'Bà chủ Ra Đề': nêu mục tiêu, không chỉ cách làm. |
| 6 | **PRD** | Product Requirements Document (Tài liệu yêu cầu sản phẩm) | 製品要求仕様書 | 3 | Sản phẩm cần có gì cho người dùng? | PRD nhìn từ người dùng, BRD nhìn từ doanh nghiệp. |
| 7 | **FRD** | Functional Requirements Document (Tài liệu yêu cầu chức năng) | 機能要件定義書 | 3 | Hệ thống phải làm những chức năng gì? | F = Function = 'hệ thống Phải làm gì'. |
| 8 | **SRS** | Software Requirements Specification (Đặc tả yêu cầu phần mềm) | 要件定義書・ソフトウェア要求仕様書 | 3 | Toàn bộ yêu cầu đã đủ để thiết kế và test chưa? | SRS = 'Sổ Rõ Sạch': đủ rõ để dev làm, QA test. |
| 9 | **NFR** | Non-functional Requirements (Yêu cầu phi chức năng) | 非機能要件定義書 | 3 | Hệ thống phải nhanh, bền, an toàn đến mức nào? | Chức năng là 'làm gì', NFR là 'làm tốt tới đâu': Nhanh, Bền, An toàn. |
| 10 | **US** | User Story / Product Backlog (User story và backlog) | ユーザーストーリー・プロダクトバックログ | 3 | (Agile) Người dùng cần gì, làm cái nào trước? | INVEST: 6 chữ để kiểm một story. |

## 3. Chia nhỏ ra sao? · BREAKDOWN

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 12 | **WBS** | Work Breakdown Structure (Cấu trúc phân rã công việc) | WBS・作業分解構成図 | 2 | Toàn bộ công việc gồm những phần nào? | Quy tắc 100%: các con cộng lại đúng bằng cha. WBS viết bằng danh từ, không bằng động từ. |
| 13 | **PBS** | Product Breakdown Structure (Cấu trúc phân rã sản phẩm) | 成果物分解構成 | 2 | Sản phẩm cuối gồm những mảnh nào? | PBS = 'cái gì' thuần danh từ; WBS = 'cái gì' cộng việc làm ra nó. |
| 14 | **ABS** | Activity Breakdown Structure / Activity List (Danh sách/cấu trúc hoạt động) | アクティビティ一覧 | 2 | Mỗi work package cần làm những bước nào? | A = Action = động từ. WBS là 'cái gì', ABS là 'làm sao để có'. |
| 15 | **OBS** | Organizational Breakdown Structure (Cấu trúc phân rã tổ chức) | 体制図 | 2 | Dự án gồm những nhóm nào, ai báo cáo ai? | O = Org = 'Ông nào'. WBS × OBS = RACI. |
| 16 | **RBS (tài nguyên)** | Resource Breakdown Structure (Cấu trúc phân rã tài nguyên) | 資源分解構成 | 2 | Cần những loại tài nguyên gì? | Có 2 RBS: R-esource (tài nguyên) và R-isk (rủi ro). Nghe 'RBS' thì hỏi lại. |
| 17 | **RBS (rủi ro)** | Risk Breakdown Structure (Cấu trúc phân loại rủi ro) | リスク分解構成 | 2 | Rủi ro có thể đến từ những nguồn nào? | RBS rủi ro là 'bản đồ nguồn nguy hiểm'; Risk Register là 'danh sách nguy hiểm cụ thể'. |
| 18 | **CBS** | Cost Breakdown Structure (Cấu trúc phân rã chi phí) | コスト分解構成 | 2 | Tiền đi vào những hạng mục nào? | C = Cash. WBS × CBS = cost baseline. |

## 4. Ai làm, ai duyệt? · WHO

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 19 | **SHR** | Stakeholder Register (Sổ các bên liên quan) | ステークホルダー登録簿 | 1 | Ai bị ảnh hưởng, ai có tiếng nói? | Lưới Quyền lực × Quan tâm: ô cao-cao thì quản lý chặt nhất. |
| 20 | **RACI** | RACI / Responsibility Assignment Matrix (Ma trận phân công trách nhiệm) | 責任分担表・RACI表 | 2 | Mỗi việc ai làm, ai chịu trách nhiệm, hỏi ai, báo ai? | R-A-C-I = Làm · Chịu · Hỏi · Báo. |
| 21 | **RP** | Resource / Staffing Plan (Kế hoạch nhân sự) | 要員計画 | 2 | Cần bao nhiêu người, vai trò gì, vào ra khi nào? | Đường nhân sự hình 'quả núi': lên dần, đỉnh ở 製造/テスト, xuống dần. |

## 5. Làm thế nào? · HOW

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 23 | **UC** | Use Case (Sơ đồ, đặc tả use case) | ユースケース図 | 3 | Ai dùng hệ thống để làm gì? | Hình người que và hình elip: AI làm GÌ. |
| 24 | **DFD** | Data Flow Diagram (Sơ đồ luồng dữ liệu) | DFD・データフロー図 | 3 | Dữ liệu chảy từ đâu, qua xử lý nào, lưu ở đâu? | DFD là dòng sông (chảy), ERD là hồ chứa (cấu trúc). |
| 22 | **ARC** | Architecture / System Configuration (Sơ đồ kiến trúc, cấu hình hệ thống) | システム構成図 | 4 | Hệ thống gồm những khối nào, nối nhau ra sao? | ARC là 'bản đồ thành phố': có những khu nào, đường nào nối. |
| 25 | **ERD** | Entity Relationship Diagram (Sơ đồ thực thể – quan hệ) | ER図 → テーブル定義書 | 4 | Dữ liệu gồm những thực thể nào, liên kết ra sao? | Entity là danh từ (bảng), Relationship là đường nối; chân chim (crow's foot) nghĩa là 'nhiều'. |
| 26 | **SCR** | Screen Design & Transition (Thiết kế màn hình, sơ đồ chuyển màn hình) | 画面設計書・画面遷移図 | 4 | Người dùng thấy gì, đi từ màn nào sang màn nào? | 遷移 (sen'i) = di chuyển: màn này sang màn kia. |
| 27 | **API** | Interface / API Specification (Đặc tả giao tiếp, API) | IF仕様書・API仕様書 | 4 | Hai hệ thống nói chuyện với nhau bằng gì? | API là 'hợp đồng giữa hai cỗ máy'. |
| 28 | **BD** | Basic Design (External Design) (Thiết kế cơ bản (thiết kế ngoài)) | 基本設計書 | 4 | Hệ thống trông thế nào nhìn từ bên ngoài? | 基本 = bên ngoài, khách thấy; 詳細 = bên trong, dev làm. |
| 29 | **DD** | Detailed Design (Internal Design) (Thiết kế chi tiết (thiết kế trong)) | 詳細設計書 | 4 | Bên trong từng module chạy thế nào? | DD = 'Dev Đọc': viết cho dev. |

## 6. Khi nào xong? · WHEN

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 30 | **PMP** | Project Management Plan (Kế hoạch quản lý dự án) | プロジェクト計画書 | 2 | Dự án sẽ được quản lý như thế nào? | PM Plan là 'luật chơi' của dự án. Đừng nhầm với chứng chỉ PMP. |
| 31 | **NET** | Network Diagram / Critical Path (Sơ đồ mạng, đường găng) | ネットワーク図・PERT図 | 2 | Việc nào phải xong trước, đâu là đường găng? | Critical path = con đường dài nhất quyết định ngày về đích. |
| 32 | **GNT** | Gantt Chart / Schedule (Biểu đồ Gantt, lịch dự án) | ガントチャート・スケジュール表 | 2 | Việc gì làm khi nào, ai làm, đang tới đâu? | Gantt là 'thanh ngang theo lịch'. Ở Nhật người ta hay gọi luôn bảng này là 'WBS', đừng nhầm với cây WBS. |
| 33 | **MS** | Milestone Chart (Bảng mốc) | マイルストーン表 | 2 | Những ngày chốt quan trọng là khi nào? | Milestone là 'cột cây số': không có độ dài, chỉ có vị trí. |
| 34 | **RLP** | Release / Cutover Plan (Kế hoạch release, chuyển đổi production) | リリース計画書・本番移行計画書 | 6 | Đưa lên production thế nào, hỏng thì quay lại ra sao? | Release plan = kịch bản cất cánh kèm kịch bản hạ cánh khẩn. |

## 7. Tốn bao nhiêu? · HOW MUCH

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 35 | **EST** | Estimate / Quotation (Bảng ước lượng, báo giá) | 見積書 | 1 | Mất bao nhiêu công, bao nhiêu tiền? | Estimate = con số + 'nếu…'. Không có 'nếu' (tiền đề) thì chưa phải estimate. |
| 36 | **CB** | Cost Baseline / Budget (Đường cơ sở chi phí, ngân sách) | コストベースライン・予算 | 2 | Ngân sách được duyệt chia theo thời gian ra sao? | Hình chữ S: chậm – nhanh – chậm. |
| 37 | **EVM** | EVM / Budget vs Actual Report (Báo cáo giá trị thu được, kế hoạch – thực tế) | 予実管理 | 5 | Đang nhanh hay chậm, lố hay tiết kiệm? | Kế hoạch – Làm được – Tiêu hết = PV – EV – AC. Chỉ số dưới 1 là xấu. |

## 8. Lệch thì sao? · WHAT IF

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 38 | **RAID** | RAID Log (Nhật ký Rủi ro – Giả định – Vấn đề – Phụ thuộc) | RAIDログ | 2 | Mọi thứ có thể làm lệch dự án được theo dõi ở đâu? | RAID = 'đột kích': Rủi ro – Giả định – Vấn đề – Phụ thuộc. |
| 39 | **RR** | Risk Register (Sổ đăng ký rủi ro) | リスク管理表 | 2 | Điều gì CÓ THỂ xảy ra, đối phó ra sao? | Risk là TƯƠNG LAI (có thể xảy ra); Issue là HIỆN TẠI (đã xảy ra). |
| 40 | **IL** | Issue Log (Nhật ký vấn đề) | 課題管理表 | 5 | Vấn đề gì ĐANG xảy ra, ai xử lý, khi nào xong? | Issue = 'cháy rồi': cần người cầm vòi và giờ dập. |
| 41 | **CR** | Change Request (Yêu cầu thay đổi) | 変更要求書・仕様変更依頼 | 5 | Thay đổi này ảnh hưởng gì, ai duyệt? | CR = 'Cổng Rào': không qua cổng thì không vào baseline. |
| 42 | **IR** | Incident Report (Báo cáo sự cố) | 障害報告書 | 6 | Sự cố gì đã xảy ra, vì sao, làm gì để không lặp lại? | 5 câu: Khi nào – Ảnh hưởng gì – Vì sao – Đã xử lý ra sao – Làm gì để không lặp lại. |

## 9. Đạt chưa? · HOW GOOD

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 43 | **QMP** | Quality Management Plan (Kế hoạch chất lượng) | 品質計画書 | 2 | Thế nào là 'đạt', đo bằng gì, kiểm ở đâu? | QMP là 'luật chấm điểm': viết trước khi thi. |
| 44 | **RTM** | Requirements Traceability Matrix (Ma trận truy vết yêu cầu) | トレーサビリティマトリクス | 3 | Mỗi yêu cầu đã được thiết kế, test ở đâu? | RTM là 'sợi chỉ đỏ' xuyên từ yêu cầu tới test. |
| 45 | **TP** | Test Plan (Kế hoạch kiểm thử) | テスト計画書 | 4 | Test cái gì, khi nào, cách nào, khi nào dừng? | Test plan = 'đánh trận ở đâu'; Test spec = 'từng phát bắn'. |
| 46 | **TS** | Test Specification / Test Cases (Đặc tả kiểm thử, test case) | テスト仕様書 | 4 | Từng bước test là gì, mong đợi kết quả gì? | Mỗi case = 'Cho – Khi – Thì' (Given – When – Then). |
| 47 | **BUG** | Bug List / Defect Log (Danh sách lỗi) | 不具合管理表 | 5 | Có những lỗi nào, nặng cỡ nào, sửa chưa? | Severity = mức đau; Priority = sửa trước hay sau. |
| 48 | **QR** | Quality / Test Report (Báo cáo chất lượng, kết quả test) | 品質報告書・テスト結果報告書 | 5 | Chất lượng hiện tại đủ để release chưa? | Số → So sánh → Lý giải → Kết luận. |

## 10. Báo ai, thế nào? · TALK

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 49 | **CMP** | Communication Plan (Kế hoạch giao tiếp) | コミュニケーション計画書 | 2 | Ai cần biết gì, khi nào, qua kênh nào? | CMP là 'lịch phát sóng': ai nghe kênh nào, giờ nào. |
| 52 | **QA** | Q&A List (Bảng hỏi đáp với khách) | QA管理表 | 3 | Còn câu hỏi nào với khách, đã trả lời chưa? | Hỏi kiểu trắc nghiệm, đừng hỏi tự luận. (QA ở đây là hỏi đáp, không phải Quality Assurance.) |
| 50 | **SR** | Status Report (Báo cáo tiến độ) | 進捗報告書 | 5 | Tuần này dự án đang ở đâu? | RAG: Red – Amber – Green. Không có 'xanh dưa hấu'. |
| 51 | **MoM** | Minutes of Meeting (Biên bản họp) | 議事録 | 5 | Họp đã quyết gì, ai làm gì, hạn khi nào? | Ba thứ phải có: Quyết gì – Ai làm – Bao giờ. |

## 11. Xong chưa? · DONE

| # | Ký hiệu | Tên | Tiếng Nhật | GĐ | Trả lời câu hỏi | Mẹo nhớ |
| --- | --- | --- | --- | --- | --- | --- |
| 53 | **UAT** | UAT & Acceptance Sign-off (Kiểm thử chấp nhận, biên bản nghiệm thu) | 受入テスト・検収書 | 6 | Khách đã chấp nhận sản phẩm chưa? | 検収 = 'ký nhận hàng', ký xong mới có tiền. |
| 54 | **LL** | Lessons Learned (Bài học kinh nghiệm) | 振り返り・教訓 | 6 | Lần sau làm gì khác đi? | KPT: Keep – Problem – Try, cách 振り返り phổ biến ở Nhật. |
| 55 | **CLR** | Closure Report (Báo cáo đóng dự án) | 完了報告書 | 6 | Dự án kết thúc ra sao so với mục tiêu? | CLR = 'Clear': dọn sạch trước khi rời. |

## Họ xBS: công thức ghép

| Ghép | Ra | Để làm gì |
| --- | --- | --- |
| WBS × OBS | **RACI** | ai làm gì |
| WBS → ABS → NET | **Gantt** | lịch có đường găng |
| WBS × CBS | **Cost baseline** | ngân sách theo thời gian |
| PBS + việc quản lý | **WBS** | không sót deliverable |
| RBS rủi ro | **Risk register** | rủi ro cụ thể |
| RBS tài nguyên | **Kế hoạch nhân sự** | ai vào, khi nào |

## Chữ V kiểu Nhật

| Cánh trái (làm ra) | Tài liệu | ↔ | Cánh phải (kiểm chứng) | Tài liệu |
| --- | --- | --- | --- | --- |
| 業務要件 · Yêu cầu nghiệp vụ | BRD, BC | ↔ | 受入テスト · Test chấp nhận (khách) | UAT |
| 要件定義 · Định nghĩa yêu cầu | SRS, FRD, NFR | ↔ | 総合テスト · Test hệ thống | TP, QR |
| 基本設計 · Thiết kế cơ bản | BD, ARC, SCR, API | ↔ | 結合テスト · Test tích hợp | TS, BUG |
| 詳細設計 · Thiết kế chi tiết | DD, ERD | ↔ | 単体テスト · Test đơn vị | TS |

RTM (ma trận truy vết) nối mọi cặp hai cánh.

## 16 cặp hay nhầm

- **BRD và FRD / SRS**: BRD: doanh nghiệp cần đạt gì (mục tiêu, quy trình, KPI); FRD: hệ thống phải làm chức năng gì; SRS: toàn bộ đặc tả, thêm phi chức năng, giao diện, ràng buộc. _Mẹo:_ Đọc theo thứ tự B → F → S: Business → Function → toàn bộ Software. Ở Nhật: 業務要件 → 機能要件 + 非機能要件 = 要件定義書.
- **BRD và PRD**: BRD: dự án do khách đặt hàng, nhìn từ doanh nghiệp; PRD: công ty làm sản phẩm, nhìn từ người dùng thị trường. _Mẹo:_ Outsource cho khách Nhật: gần như luôn là BRD / 要件定義書.
- **WBS và Gantt**: WBS: cây 'cái gì', không có ngày; Gantt: 'khi nào, ai làm', thanh theo lịch. _Mẹo:_ Ở Nhật, bảng Excel lịch hay bị gọi là 'WBS'. Nghe 'WBS' thì hỏi lại: cây phân rã hay lịch?
- **WBS và ABS**: WBS: danh từ, deliverable, work package; ABS / Activity list: động từ, các bước làm ra 1 work package. _Mẹo:_ 'Module thanh toán' là WBS; 'viết thiết kế, code, test' là activity.
- **WBS và PBS**: PBS: chỉ thứ được giao (sản phẩm); WBS: thứ được giao + việc để làm ra nó, kể cả quản lý dự án. _Mẹo:_ PBS + việc quản lý, test, release = WBS.
- **RBS (tài nguyên) và RBS (rủi ro)**: Resource BS: người, thiết bị, phần mềm, dịch vụ; Risk BS: nguồn rủi ro theo nhóm. _Mẹo:_ Cùng tên viết tắt: luôn nói rõ chữ R là Resource hay Risk.
- **OBS và RACI**: OBS (体制図): ai thuộc nhóm nào, ai báo cáo ai; RACI: với từng việc, ai làm, ai chịu, ai được hỏi, ai được báo. _Mẹo:_ RACI = WBS (hàng) × OBS (cột).
- **Risk register và Issue log**: Risk: chưa xảy ra, có xác suất; Issue: đã xảy ra, cần người xử lý và hạn. _Mẹo:_ Rủi ro xảy ra thì chuyển từ リスク管理表 sang 課題管理表.
- **Issue và Change request**: Issue: vấn đề cần giải quyết; CR: đề nghị đổi baseline (phạm vi, lịch, chi phí). _Mẹo:_ Một issue có thể sinh ra CR, nhưng không phải issue nào cũng là CR.
- **ERD và DFD**: ERD: dữ liệu tổ chức thế nào (bảng, khóa, quan hệ); DFD: dữ liệu chảy đi đâu (nguồn, xử lý, kho). _Mẹo:_ ERD là hồ chứa, DFD là dòng sông.
- **基本設計 và 詳細設計**: 基本設計 (Basic Design): nhìn từ ngoài, khách duyệt; 詳細設計 (Detailed Design): nhìn từ trong, viết cho dev. _Mẹo:_ 基本 = khách thấy; 詳細 = dev đọc.
- **Test plan và Test spec**: Test plan: phạm vi, mức test, môi trường, tiêu chí dừng; Test spec: từng case, bước làm, kết quả mong đợi. _Mẹo:_ Plan là chiến lược, spec là từng phát bắn.
- **Charter và SOW / Scope statement**: Charter: cho phép dự án bắt đầu, trao quyền cho PM; SOW: phạm vi theo hợp đồng với khách; Scope statement: phạm vi chi tiết để lập WBS. _Mẹo:_ Charter = giấy khai sinh; SOW = hợp đồng; Scope statement = hàng rào.
- **Estimate và Cost baseline**: Estimate: con số ước tính, kèm tiền đề; Cost baseline: con số đã duyệt, chia theo thời gian, dùng để đo. _Mẹo:_ Estimate là đề xuất; baseline là cam kết.
- **Status report và 議事録 (MoM)**: Status report: trạng thái định kỳ của cả dự án; 議事録: quyết định và việc cần làm của 1 cuộc họp. _Mẹo:_ Báo cáo nhìn cả dự án; biên bản nhìn 1 cuộc họp.
- **Severity và Priority**: Severity: lỗi nặng cỡ nào; Priority: sửa trước hay sau. _Mẹo:_ Lỗi chính tả ở trang chủ: severity thấp, priority cao.
