# 45 tình huống PM kèm đáp án (dự án cho khách Nhật)

> Mỗi tình huống có 4 phương án cho **việc đầu tiên** cần làm. Tự chọn trước rồi bấm **Đáp án** để mở. Bản tương tác (chọn phương án, lưu kết quả, lọc theo nhóm và mức): `tinh-huong-PM.html` (tải về, mở bằng trình duyệt).

**Khung trả lời 4 nhịp:** ① Xác nhận fact → ② Hành động ngay → ③ Báo khách theo 報連相 → ④ Gốc rễ & phòng ngừa (なぜなぜ分析, 再発防止, 横展開).

Tình huống và số liệu là ví dụ dựng sẵn để luyện; tên khách dùng dạng chung. Ngưỡng ghi "tham khảo" là mức kinh nghiệm.

## Mục lục

- **Tiến độ & 納期**: [S01 Phát hiện trễ ngay trước 結合テスト](#s01) · [S02 Khách không cho dời 納期 gắn quy định](#s02) · [S03 Vendor khác trễ 基本設計, team phải chờ](#s03) · [S04 Khách trả lời QA chậm, chặn 製造](#s04) · [S05 Tiếp nhận dự án đỏ từ PM khác](#s05)
- **Phạm vi & thay đổi**: [S06 Khách đổi spec sau khi chốt 基本設計](#s06) · [S07 Yêu cầu 'đương nhiên phải có' (当然)](#s07) · [S08 Yêu cầu thay đổi gửi thẳng qua chat](#s08) · [S09 Khách từ chối thanh toán CR đã làm](#s09) · [S10 Hai phòng ban khách yêu cầu mâu thuẫn](#s10)
- **Chất lượng & bug**: [S11 受入テスト tuần đầu ra 48 phiếu lỗi](#s11) · [S12 Khách chê lỗi chính tả trong tài liệu](#s12) · [S13 Bug density thấp bất thường](#s13) · [S14 Sự cố lặp lại, khách đòi なぜなぜ分析](#s14) · [S15 Deadline ép bỏ bớt test](#s15)
- **Sự cố 本番**: [S16 Lỗi tính lãi phát hiện sau 3 tuần 本番](#s16) · [S17 夜間バッチ dừng giữa chừng lúc 3h sáng](#s17) · [S18 Dữ liệu địa chỉ khách sai sau release](#s18) · [S19 Sự cố 2h sáng, không gọi được 窓口](#s19) · [S20 Release lỗi đúng tuần 年度末](#s20)
- **Khách hàng & giao tiếp**: [S21 課長 phía khách nổi giận giữa 定例会](#s21) · [S22 担当者 phía khách đổi người giữa dự án](#s22) · [S23 Khách im lặng, QA quá hạn 2 tuần](#s23) · [S24 Khách dọa chuyển vendor sau chuỗi trễ hạn](#s24) · [S25 Khách muốn họp thẳng với dev, bỏ BrSE](#s25)
- **Team & con người**: [S26 Tech lead xin nghỉ giữa 結合テスト](#s26) · [S27 BrSE nghỉ đột ngột, chỉ còn 3 ngày](#s27) · [S28 Ramp-up gấp từ 5 lên 20 người](#s28) · [S29 Member giỏi nhất nhưng toxic với team](#s29) · [S30 Team OT kéo dài, dấu hiệu burnout](#s30)
- **Chi phí & hợp đồng**: [S31 請負 vượt effort 30%, CPI 0,77](#s31) · [S32 Sếp ép nhận dự án dưới giá vốn](#s32) · [S33 Khách muốn đổi 準委任 sang 請負 giữa chừng](#s33) · [S34 Khách ép giảm giá vì yên yếu](#s34) · [S35 Estimate sai lộ ra ở 詳細設計](#s35)
- **Rủi ro & bảo mật**: [S36 Member dán code, dữ liệu khách vào ChatGPT](#s36) · [S37 Mất laptop chứa source code dự án](#s37) · [S38 Gửi nhầm email chứa dữ liệu khách](#s38) · [S39 Audit ISMS phát hiện vi phạm ở dự án](#s39) · [S40 Vendor khác trễ IF, chặn dự án](#s40)
- **Tình huống xám**: [S41 Khách gợi ý ghi giảm số bug trong báo cáo](#s41) · [S42 Sếp muốn giấu delay đến sau review](#s42) · [S43 Chọn 納期 hay chất lượng trước 本番](#s43) · [S44 Một PM, hai dự án cùng đỏ](#s44) · [S45 Khách đòi OT cuối tuần không trả thêm](#s45)

## Tiến độ & 納期

<a id="s01"></a>

### S01 · Phát hiện trễ ngay trước 結合テスト

_Mức: Trung cấp_

**Bối cảnh:** Dự án 請負 (khoán trọn gói) cho khách ngân hàng A, team 12 người, đang ở 製造 (code) tuần 8/12. Báo cáo tuần vẫn ghi 'on track', nhưng khi đối chiếu WBS thì SPI = 0,82 và 2/6 module mới xong khoảng 50%. 結合テスト (kiểm thử tích hợp) bắt đầu sau 3 tuần, khách chưa biết gì.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Trong 2 ngày phân tích trễ theo module và critical path, lập 2–3 phương án hồi phục, rồi báo khách.
- **B.** Báo ngay khách rằng dự án trễ khoảng 3 tuần và xin dời ngày bắt đầu 結合テスト.
- **C.** Tăng OT cả team trong 2 tuần để kéo lại tiến độ, tạm chưa báo khách để khách khỏi lo.
- **D.** Xin thêm 3 dev từ bench và đưa ngay vào 2 module đang trễ nhất.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Đúng nhịp: có fact (trễ bao nhiêu, ở đâu, vì sao) và phương án trước, nên khách nhận được 'vấn đề + lựa chọn' chứ không chỉ tin xấu; vẫn đủ sớm, trước khi trễ lan sang 結合テスト.
- **B** ✗ Minh bạch là đúng nhưng con số 3 tuần chưa kiểm chứng; báo sai rồi phải sửa lại làm mất niềm tin hơn việc chậm 2 ngày để có số thật.
- **C** ✗ Che giấu trễ là vi phạm 報連相; OT kéo dài làm tăng bug, và nếu không kéo kịp thì khách biết quá muộn, mất hết lựa chọn.
- **D** ✗ Thêm người khi chưa rõ nguyên nhân dễ làm chậm hơn (onboard, lead bị phân tán); có thể là một phương án nhưng phải sau phân tích.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: PM cùng team lead cập nhật WBS theo deliverable thật (không dùng % tự khai), tính SPI và số ngày trễ theo module, xác định task nằm trên critical path và nguyên nhân (ước lượng sai, spec chưa rõ, người nghỉ…).  
② Hành động ngay: Ngày 2: lập 2–3 phương án (đổi thứ tự để 結合テスト chạy trước phần đã xong, bổ sung 2 người có kinh nghiệm domain, chia phạm vi 2 đợt) kèm 工数 và rủi ro; chốt nội bộ với cấp trên.  
③ Báo khách theo 報連相: Trước 定例会 gần nhất (hoặc xin họp riêng trong tuần): PM và BrSE báo 窓口 khách: trễ bao nhiêu, nguyên nhân, phương án đề xuất, điểm cần khách quyết; gửi 議事録 ngay trong ngày.  
④ Gốc rễ & phòng ngừa: Gốc rễ thường là báo cáo dựa trên % tự khai: chuyển sang đo EV theo deliverable hoàn thành (quy tắc 0/50/100), cảnh báo khi SPI < 0,9 (tham khảo); 横展開 cách đo này cho các dự án khác cùng khách.  

**Đừng làm:**

- Ghi 'on track' trong 進捗報告書 khi chưa đối chiếu WBS với deliverable thật.
- Hứa ngày hồi phục ngay trong cuộc họp khi chưa tính lại 工数.

**Câu tiếng Nhật:** 進捗遅延の要因と挽回策について、ご相談させてください。 (Shinchoku chien no yōin to bankaisaku ni tsuite, go-sōdan sasete kudasai.) — Xin cho phép chúng tôi trao đổi về nguyên nhân chậm tiến độ và phương án lấy lại tiến độ.

**Trả lời 30 giây:** “Em không báo khách ngay một con số trễ chưa kiểm chứng, cũng không âm thầm OT; em dành tối đa 2 ngày đo lại tiến độ thật theo WBS và critical path. Sau đó em mang đến khách 'trễ bao nhiêu, vì sao, 2–3 phương án' — nguyên tắc là báo sớm nhưng báo bằng fact và lựa chọn, khi khách vẫn còn thời gian quyết.”

**Tài liệu dùng:** WBS (Work Breakdown Structure), SR (Status Report), GNT (Gantt Chart / Schedule)  
**Chỉ số theo dõi:** SPI (Schedule Performance Index), SLIP (Schedule Slip (days)), %C (Percent Complete)

</details>

<a id="s02"></a>

### S02 · Khách không cho dời 納期 gắn quy định

_Mức: Khó_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 請負, team 15 người; 本番 (go-live) bắt buộc ngày 1/4 vì quy định mới có hiệu lực từ đầu năm tài chính, ngay sau 年度末. Ước lượng lại cuối 詳細設計 cho thấy team cần thêm khoảng 3 tuần. Trưởng phòng IT bên khách nói thẳng: '納期 (hạn giao) tuyệt đối không dời'.

**Câu hỏi:** Anh/chị đề xuất gì với khách?

- **A.** Cam kết giữ 納期, tăng thêm 5 người và OT, rút gọn 総合テスト để kịp ngày 1/4.
- **B.** Phân loại chức năng theo mức bắt buộc của quy định, đề xuất phát hành phân kỳ: phần bắt buộc đúng 1/4.
- **C.** Giữ đề xuất dời 3 tuần, trình bày rõ rủi ro chất lượng nếu cố giữ 納期.
- **D.** Escalate ngay lên giám đốc hai bên để đàm phán lại hợp đồng và 納期.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Nghe chủ động nhưng tăng người muộn ít hiệu quả, còn cắt test là chuyển rủi ro sang 本番 của hệ thống bảo hiểm — 障害 sau go-live tốn hơn nhiều so với trễ.
- **B** ✅ Khi 納期 bị khóa bởi pháp lý, biến số còn lại là phạm vi: giữ đúng phần quy định bắt buộc, phần còn lại phát hành sau; chất lượng không bị hy sinh và khách có lựa chọn rõ ràng.
- **C** ✗ Đúng về rủi ro nhưng bỏ qua ràng buộc thật của khách; khách sẽ thấy vendor không hiểu nghiệp vụ và chỉ lo cho mình.
- **D** ✗ Escalate khi chưa có phương án là quá sớm và làm căng quan hệ; cấp trên hai bên cũng sẽ hỏi lại 'phương án là gì?'.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: cùng BrSE đối chiếu từng chức năng với văn bản quy định để chia Must (bắt buộc 1/4) / Should / Could, ước lượng lại 工数 nhóm Must và kiểm tra Must có vừa lịch hiện tại không.  
② Hành động ngay: Thiết kế 2 phương án: (1) ngày 1/4 chỉ phát hành Must, phần thiếu vận hành tay tạm thời, đợt 2 sau 4–6 tuần (tham khảo); (2) giữ toàn bộ phạm vi với tăng người có giới hạn, kèm rủi ro định lượng. 根回し với 窓口 trước buổi họp chính.  
③ Báo khách theo 報連相: Trong tuần: PM cùng sales gặp trưởng phòng IT, trình bảng so sánh 2 phương án (phạm vi, chi phí, rủi ro, vận hành tạm); xin quyết định bằng văn bản, ghi 議事録 và lập CR cho phạm vi đợt 2.  
④ Gốc rễ & phòng ngừa: Với dự án gắn quy định pháp lý: gắn nhãn Must/Should cho từng yêu cầu ngay từ 要件定義 và giữ buffer 10–15% (tham khảo) trên critical path; đưa thành mục kiểm tra bắt buộc khi review 見積.  

**Đừng làm:**

- Nói 'chúng tôi sẽ cố gắng hết sức' mà không thay đổi biến số nào (phạm vi, người, thời gian).
- Tự cắt test để giữ ngày mà không có khách đồng ý bằng văn bản.

**Câu tiếng Nhật:** 納期厳守を前提に、段階リリースをご提案いたします。 (Nōki genshu o zentei ni, dankai rirīsu o go-teian itashimasu.) — Lấy việc giữ đúng hạn giao làm tiền đề, chúng tôi xin đề xuất phát hành theo giai đoạn.

**Trả lời 30 giây:** “Khi 納期 bị khóa bởi quy định, em không tranh cãi ngày mà đổi biến số phạm vi: tách phần pháp luật bắt buộc phát hành đúng 1/4, phần còn lại sang đợt 2. Em trình 2 phương án có số liệu để khách quyết, và không bao giờ âm thầm cắt test để giữ ngày.”

**Tài liệu dùng:** MS (Milestone Chart), CR (Change Request), RLP (Release / Cutover Plan)  
**Chỉ số theo dõi:** OTD (On-time Delivery Rate), SLIP (Schedule Slip (days)), TF (Total Float)

</details>

<a id="s03"></a>

### S03 · Vendor khác trễ 基本設計, team phải chờ

_Mức: Khó_

**Bối cảnh:** Khách sản xuất C thuê vendor X làm 基本設計 (thiết kế cơ bản); công ty mình nhận 詳細設計〜製造 theo 請負, team 10 người bắt đầu từ 1/11. Đến ngày bắt đầu, 基本設計書 vẫn còn khoảng 30% màn hình ghi 'TBD' và vendor X nói cần thêm 3 tuần. Hợp đồng của mình có 前提条件 (điều kiện tiên quyết) là 基本設計 đã hoàn tất.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Cho team tự suy luận phần 基本設計 còn TBD và bắt đầu 詳細設計 luôn để không mất thời gian.
- **B.** Liên hệ trực tiếp PM của vendor X để hối thúc và xin lịch giao cụ thể.
- **C.** Tạm rút 6 người về bench để giảm chi phí chờ, đợi 基本設計 xong mới gọi lại.
- **D.** Định lượng tác động trong 1 ngày, báo 窓口 khách bằng văn bản, đề xuất làm trước phần đã chốt.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Nghe chủ động nhưng tự đoán spec của bên khác dẫn tới 手戻り (làm lại) và tranh chấp: phần làm sai không ai trả tiền.
- **B** ✗ Mình không có hợp đồng với vendor X; đi vòng qua khách làm khách mất kiểm soát và dễ biến thành đổ lỗi qua lại giữa hai vendor.
- **C** ✗ Giảm chi phí ngắn hạn nhưng khi 基本設計 về thì khó gom lại người đã nắm domain, dự án còn trễ thêm.
- **D** ✅ Đúng kênh (khách là bên quản lý vendor X), có số liệu tác động và phương án giữ team làm việc có ích, đồng thời ghi nhận 前提条件 để bảo vệ hợp đồng nếu phải dời 納期.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: cùng BrSE lập danh sách màn/chức năng đã chốt và TBD, tính số 人日 làm được ngay, số 人日 phải chờ và số ngày trễ trên critical path nếu phần TBD về muộn 3 tuần.  
② Hành động ngay: Sắp lại WBS: team làm trước 詳細設計 phần đã chốt (~70%), dựng môi trường, framework và dữ liệu test chung; mỗi mục TBD ghi vào 課題管理表 với hạn chót cần có để không trễ thêm.  
③ Báo khách theo 報連相: Trong 2 ngày: PM gửi 窓口 khách báo cáo tác động và đề xuất (làm trước phần đã chốt, hạn nhận phần TBD, chi phí chờ nếu có), nhờ khách điều phối vendor X; nếu 納期 phải dời, chuẩn bị CR dựa trên 前提条件 hợp đồng.  
④ Gốc rễ & phòng ngừa: Với dự án nhiều vendor: ghi vào hợp đồng/PMP điều kiện đầu vào đo được (định nghĩa 'BD hoàn tất'), mốc nhận đầu vào và cách tính chi phí chờ; theo dõi rủi ro phụ thuộc trong RAID ngay từ kick-off.  

**Đừng làm:**

- Im lặng chờ đến khi 基本設計 về rồi mới báo khách là đã trễ.
- Chê vendor X trước mặt khách thay vì nói bằng số liệu tác động.

**Câu tiếng Nhật:** 前工程の遅延による影響と対応案をご報告いたします。 (Zenkōtei no chien ni yoru eikyō to taiōan o go-hōkoku itashimasu.) — Chúng tôi xin báo cáo ảnh hưởng do công đoạn trước bị trễ và phương án xử lý.

**Trả lời 30 giây:** “Em không tự đoán phần spec còn thiếu và cũng không liên hệ thẳng vendor kia, vì khách mới là người quản lý họ. Em đo tác động trong 1 ngày, giữ team làm phần đã chốt, rồi báo khách bằng văn bản kèm phương án và 前提条件 hợp đồng — vừa giữ tiến độ, vừa giữ cơ sở cho CR nếu phải dời.”

**Tài liệu dùng:** IL (Issue Log), CR (Change Request), RAID (RAID Log)  
**Chỉ số theo dõi:** SLIP (Schedule Slip (days)), UTL (Utilization), TF (Total Float)

</details>

<a id="s04"></a>

### S04 · Khách trả lời QA chậm, chặn 製造

_Mức: Cơ bản_

**Bối cảnh:** Dự án 請負 cho khách ngân hàng A, đang 製造 tuần 4/10. QA管理表 (bảng hỏi-đáp với khách) có 25 câu mở, trong đó 8 câu đã quá hạn trả lời trung bình 9 ngày, chặn 2 module tương đương khoảng 30 人日. Khách đang bận chốt sổ cuối quý nên trả lời chậm.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Gửi email nhắc mỗi ngày cho người phụ trách bên khách đến khi có câu trả lời.
- **B.** Ghi vào 進捗報告書 rằng trễ là do khách, để giữ bằng chứng khi có tranh chấp.
- **C.** Lập danh sách 8 câu quá hạn kèm tác động và giả định đề xuất, xin khách xác nhận tại 定例会.
- **D.** Cho dev tự chọn cách hiểu hợp lý nhất và code tiếp, khách trả lời sau thì chỉnh.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Nhắc nhiều nhưng không cho khách thấy hậu quả và không giúp họ trả lời nhanh hơn, còn dễ gây khó chịu.
- **B** ✗ Giữ bằng chứng là cần, nhưng chỉ làm vậy là đổ lỗi thụ động; tiến độ vẫn không được giải quyết.
- **C** ✅ Biến câu hỏi treo thành quyết định dễ: khách chỉ cần đồng ý hoặc sửa giả định, và thấy rõ hạn chót cùng ảnh hưởng 納期 nếu trễ.
- **D** ✗ Code theo phỏng đoán chưa được khách xác nhận dễ gây 手戻り và tranh cãi trách nhiệm sau này.

**Đáp án mẫu:**

① Xác nhận fact: Trong nửa ngày: BrSE lọc QA管理表 các câu quá hạn, ghi mỗi câu đang chặn task nào, bao nhiêu 人日, và ngày muộn nhất phải có trả lời để không ảnh hưởng 納期.  
② Hành động ngay: Với mỗi câu, BrSE soạn sẵn giả định (仮定) hợp lý nhất kèm phương án thay thế; team lead chuyển người sang task không bị chặn để giữ 稼働.  
③ Báo khách theo 報連相: Gửi danh sách cho 窓口 trước 定例会 1 ngày; tại 定例会 xin khách chốt 'đồng ý giả định hoặc trả lời trước ngày X', ghi trong 議事録 rằng quá hạn thì làm theo giả định và thay đổi sau đó xử lý bằng CR.  
④ Gốc rễ & phòng ngừa: Thống nhất từ kick-off SLA trả lời QA (vd 3 ngày làm việc, tham khảo); báo số ngày trả lời trung bình và số câu quá hạn trong 進捗報告書 hằng tuần, cảnh báo khi vượt ngưỡng.  

**Đừng làm:**

- Hỏi lại câu cũ mà không kèm giả định, khiến khách phải tự nghĩ lại từ đầu.
- Để câu hỏi treo mà không ghi ảnh hưởng 納期, đến cuối dự án mới tính trễ.

**Câu tiếng Nhật:** ご回答期限までに未回答の場合、記載の前提で進めてもよろしいでしょうか。 (Go-kaitō kigen made ni mikaitō no baai, kisai no zentei de susumete mo yoroshii deshō ka.) — Nếu đến hạn mà chưa có trả lời, chúng tôi xin tiến hành theo giả định đã ghi, có được không ạ?

**Trả lời 30 giây:** “Em không chỉ nhắc khách trả lời, mà biến mỗi câu hỏi treo thành một giả định soạn sẵn kèm hạn chót và tác động 納期, để khách chỉ cần xác nhận. Thỏa thuận đó ghi vào 議事録, nên vừa giữ được tiến độ vừa có cơ sở làm CR nếu khách đổi ý sau.”

**Tài liệu dùng:** QA (Q&A List), MoM (Minutes of Meeting), IL (Issue Log)  
**Chỉ số theo dõi:** QART (Q&A Response Time), IAGE (Issue Aging), SLIP (Schedule Slip (days))

</details>

<a id="s05"></a>

### S05 · Tiếp nhận dự án đỏ từ PM khác

_Mức: Khó_

**Bối cảnh:** Anh/chị được giao tiếp quản dự án 請負 cho khách bảo hiểm B (team 18 người) vì PM cũ nghỉ việc. Dự án đang ở 製造, SPI báo cáo 0,75, khách đã gửi 2 lần phàn nàn chính thức trong tháng, 課題管理表 có 40 課題 mở, nhiều mục quá 30 ngày. 定例会 tiếp theo diễn ra sau 6 ngày.

**Câu hỏi:** Tuần đầu tiên anh/chị làm gì?

- **A.** Lập ngay kế hoạch hồi phục mới và trình khách trong 3 ngày để sớm lấy lại niềm tin.
- **B.** Trong 5 ngày làm health check (WBS, 課題, bug, 1-1 với lead/BrSE), gặp khách nghe trước, rồi trình baseline thật.
- **C.** Giữ nguyên kế hoạch cũ 2–3 tuần để quan sát, tránh thay đổi đột ngột làm team rối.
- **D.** Thay BrSE và tech lead ngay vì khách đã phàn nàn hai lần trong tháng.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Nghe quyết đoán nhưng kế hoạch dựng trên số liệu của PM cũ (vốn đã sai) dễ phải sửa thêm lần nữa — thất hứa lần thứ ba sẽ rất nặng.
- **B** ✅ Fact trước kế hoạch: hiểu trạng thái thật, nghe kỳ vọng của khách, rồi đặt lại baseline giữ được; khách thấy sự thay đổi ngay từ cách làm.
- **C** ✗ Dự án đỏ không còn thời gian quan sát thụ động; khách cần thấy tín hiệu thay đổi ngay trong tuần đầu.
- **D** ✗ Thay người khi chưa rõ nguyên nhân là đổ lỗi, mất kiến thức dự án và làm team hoảng.

**Đáp án mẫu:**

① Xác nhận fact: Ngày 1–3: đối chiếu WBS với deliverable thật (không dùng % cũ), rà 40 課題 và danh sách bug theo tuổi và mức độ, 1-1 với tech lead, BrSE và 2–3 dev chủ chốt để tìm nguyên nhân (spec, ước lượng, kỹ năng, giao tiếp).  
② Hành động ngay: Ngày 2: cùng sales gặp 窓口 khách để nghe 3 vấn đề họ thấy nặng nhất; trong lúc chưa có kế hoạch, đóng ngay 3–5 課題 quá hạn dễ xử lý để khách thấy thay đổi.  
③ Báo khách theo 報連相: Tại 定例会 ngày 6: trình 'baseline thật' (SPI tính lại, 納期 dự báo), nguyên nhân chính, kế hoạch hồi phục 2 phương án và cơ chế báo cáo mới (hằng tuần, bộ chỉ số cố định); xin khách xác nhận, ghi 議事録.  
④ Gốc rễ & phòng ngừa: Bài học bàn giao: dự án phải có checklist handover (WBS, 課題, rủi ro, quan hệ khách); PMO đặt cảnh báo khi SPI < 0,9 hoặc 課題 quá 14 ngày (tham khảo) để dự án không đỏ âm thầm.  

**Đừng làm:**

- Đổ lỗi PM cũ trước mặt khách — với khách, đó vẫn là cùng một công ty.
- Hứa ngày hoàn thành mới ngay trong buổi chào hỏi đầu tiên.

**Câu tiếng Nhật:** 現状を正確に把握したうえで、改めてご報告いたします。 (Genjō o seikaku ni haaku shita ue de, aratamete go-hōkoku itashimasu.) — Sau khi nắm chính xác hiện trạng, chúng tôi sẽ báo cáo lại với quý công ty.

**Trả lời 30 giây:** “Tiếp nhận dự án đỏ, em không vội trình kế hoạch trên số liệu cũ, vì thất hứa thêm lần nữa còn tệ hơn chậm vài ngày. Em dùng 5 ngày để có fact và nghe khách, trong lúc đó vẫn đóng ngay vài 課題 quá hạn cho khách thấy thay đổi, rồi đặt lại một baseline giữ được.”

**Tài liệu dùng:** IL (Issue Log), SR (Status Report), PMP (Project Management Plan)  
**Chỉ số theo dõi:** SPI (Schedule Performance Index), IAGE (Issue Aging), CSAT (Customer Satisfaction)

</details>


## Phạm vi & thay đổi

<a id="s06"></a>

### S06 · Khách đổi spec sau khi chốt 基本設計

_Mức: Cơ bản_

**Bối cảnh:** Dự án 請負 cho khách sản xuất C; 基本設計書 đã được khách 承認 (phê duyệt) ngày 1/10. 詳細設計 đang được 70% thì khách muốn đổi luồng duyệt đơn hàng từ 2 cấp lên 3 cấp; team ước sơ bộ ảnh hưởng 12 màn hình, khoảng 40 人日. Khách nói: 'chỉ thêm một cấp thôi mà'.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Đồng ý làm luôn vì là thay đổi nhỏ, hấp thụ vào buffer để giữ quan hệ.
- **B.** Từ chối vì 基本設計 đã phê duyệt, mọi thay đổi để sang phase sau.
- **C.** Cho team sửa trước phần dễ để không trễ tiến độ, thủ tục CR làm song song sau.
- **D.** Tiếp nhận yêu cầu, phân tích tác động trong 2 ngày, gửi CR kèm 見積 và lịch để khách quyết.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ 40 人日 không nhỏ; làm miễn phí tạo tiền lệ và ăn hết buffer dành cho rủi ro khác.
- **B** ✗ Cứng nhắc; khách có quyền thay đổi, việc của PM là cho khách thấy cái giá của thay đổi chứ không phải chặn.
- **C** ✗ Nghe nhanh nhưng làm trước khi thống nhất phạm vi và chi phí thì khó đòi tiền và có thể làm sai ý khách.
- **D** ✅ Đúng quy trình 変更管理: hiểu đúng yêu cầu, đo tác động thật (màn, DB, test, lịch), để khách quyết dựa trên chi phí và 納期.

**Đáp án mẫu:**

① Xác nhận fact: Ngày 1: BrSE họp ngắn với khách làm rõ yêu cầu (điều kiện của cấp 3, ngoại lệ, dữ liệu đang có), ghi vào QA管理表; team lead liệt kê màn, bảng, API, test bị ảnh hưởng.  
② Hành động ngay: Ngày 2: ước lượng 工数 theo từng hạng mục, tính ảnh hưởng 納期 với 2 phương án (làm trong phase này và dời lịch, hoặc đưa vào release sau); trong lúc chờ, team tiếp tục phần không bị ảnh hưởng.  
③ Báo khách theo 報連相: Ngày 3: gửi 変更要求書 kèm 見積 cho 窓口 khách và giải thích tại 定例会; chỉ bắt đầu làm khi có phê duyệt bằng văn bản, rồi cập nhật 基本設計書 với version mới.  
④ Gốc rễ & phòng ngừa: Ghi thủ tục 変更管理 (ai yêu cầu, ai duyệt, từ bao nhiêu 人日 phải có CR) vào PMP và nói rõ ở kick-off; theo dõi tỉ lệ thay đổi yêu cầu sau khi chốt 基本設計 trong 進捗報告書.  

**Đừng làm:**

- Ước lượng miệng 'khoảng 1 tuần' ngay trong cuộc họp.
- Sửa tài liệu thiết kế mà không tăng version và không ghi lịch sử thay đổi.

**Câu tiếng Nhật:** 影響範囲を確認のうえ、変更要求書にてご提示いたします。 (Eikyō han'i o kakunin no ue, henkō yōkyūsho nite go-teiji itashimasu.) — Sau khi xác nhận phạm vi ảnh hưởng, chúng tôi sẽ trình bày bằng phiếu yêu cầu thay đổi.

**Trả lời 30 giây:** “Em không nói 'có' hay 'không' ngay, mà tiếp nhận và trong 2 ngày cho khách thấy cái giá của thay đổi: bao nhiêu màn, bao nhiêu 人日, ảnh hưởng 納期 thế nào. Khách quyết bằng văn bản rồi team mới làm — vừa tôn trọng khách, vừa bảo vệ hợp đồng 請負.”

**Tài liệu dùng:** CR (Change Request), EST (Estimate / Quotation), BD (Basic Design (External Design))  
**Chỉ số theo dõi:** RV (Requirement Volatility), SCR (Scope Creep), CRA (CR Approval Rate)

</details>

<a id="s07"></a>

### S07 · Yêu cầu 'đương nhiên phải có' (当然)

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách ngân hàng A, đang 結合テスト. Khách nói chức năng xuất CSV cho mọi danh sách và log thao tác (監査ログ) là 'đương nhiên phải có' (当然ある) với hệ thống ngân hàng, dù 要件定義書 và 基本設計書 không ghi cụ thể. Team ước khoảng 60 人日, trong khi 納期 còn 7 tuần.

**Câu hỏi:** Phản hồi đầu tiên của anh/chị là gì?

- **A.** Trong 1 ngày đối chiếu 要件定義書, NFR, 議事録, QA管理表 để tìm căn cứ, rồi mới trả lời khách.
- **B.** Trả lời ngay bằng email rằng hai chức năng này nằm ngoài phạm vi hợp đồng.
- **C.** Làm luôn vì với ngân hàng audit log là chuẩn ngành, tranh cãi chỉ làm mất quan hệ.
- **D.** Hỏi team mất bao lâu; nếu dưới 10 人日 thì làm miễn phí như một cử chỉ thiện chí.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Tình huống xám: có thể NFR có câu chung về bảo mật/truy vết, có thể 議事録 từng nhắc. Có căn cứ rồi mới tách rõ phần nào là trách nhiệm của mình, phần nào là CR, và giữ thể diện cho cả hai bên.
- **B** ✗ Có thể đúng về hợp đồng nhưng trả lời khi chưa kiểm tra; nếu sau đó tìm thấy một dòng trong NFR thì mất uy tín, và khách thấy bị từ chối lạnh lùng.
- **C** ✗ Nhận 60 人日 không có căn cứ sẽ phá 納期 và lợi nhuận, lại tạo tiền lệ 'đương nhiên' cho các yêu cầu sau.
- **D** ✗ Quyết định dựa trên công sức chứ không dựa trên hợp đồng; khách không biết mình được ưu đãi và lần sau sẽ lại kỳ vọng như vậy.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: BrSE tìm trong 要件定義書, NFR (bảo mật, 監査), 議事録, QA管理表, 提案書 mọi câu liên quan CSV và log; PM xem điều khoản phạm vi trong hợp đồng.  
② Hành động ngay: Tách 3 nhóm: có căn cứ rõ (thiếu sót của mình, làm trong phạm vi); căn cứ mơ hồ (vd NFR ghi 'đảm bảo truy vết' nhưng không chi tiết) → đề xuất mức tối thiểu hợp lý; không có căn cứ → lập CR kèm 見積 và lịch.  
③ Báo khách theo 報連相: Trong 2 ngày: PM và BrSE gặp 窓口 khách, trình bảng đối chiếu từng yêu cầu với tài liệu đã duyệt, dùng ngôn ngữ trung lập ('theo tài liệu đã thống nhất…'), đưa phương án để khách chọn; ghi 議事録.  
④ Gốc rễ & phòng ngừa: Từ 要件定義 của dự án ngân hàng: thêm checklist NFR chuẩn ngành (監査ログ, xuất dữ liệu, phân quyền) và ghi rõ trong/ngoài phạm vi trong SOW, để những điều 'đương nhiên' được nói ra ngay từ đầu.  

**Đừng làm:**

- Nói 'không có trong spec' như câu chốt mà không đưa tài liệu và phương án.
- Đồng ý miệng trong lúc 結合テスト rồi về mới tính 工数.

**Câu tiếng Nhật:** 要件定義書の記載範囲を確認させていただけますでしょうか。 (Yōken teigisho no kisai han'i o kakunin sasete itadakemasu deshō ka.) — Cho phép chúng tôi xác nhận lại phạm vi đã ghi trong tài liệu định nghĩa yêu cầu được không ạ?

**Trả lời 30 giây:** “Với yêu cầu 'đương nhiên', em không trả lời ngay có hay không, mà trong 1 ngày đối chiếu mọi tài liệu đã duyệt để tách phần là thiếu sót của mình, phần mơ hồ và phần thật sự là CR. Sau đó em trình khách bằng tài liệu, giọng trung lập, có phương án — giữ quan hệ mà vẫn bảo vệ phạm vi hợp đồng.”

**Tài liệu dùng:** SRS (Software Requirements Specification), NFR (Non-functional Requirements), CR (Change Request)  
**Chỉ số theo dõi:** SCR (Scope Creep), RV (Requirement Volatility), GM (Gross Margin)

</details>

<a id="s08"></a>

### S08 · Yêu cầu thay đổi gửi thẳng qua chat

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 請負, team 10 người. Người dùng phòng nghiệp vụ được thêm vào kênh Teams chung và nhắn thẳng cho dev 'sửa nút này', 'thêm cột kia'; dev ngại từ chối nên làm luôn. Trong 3 tuần có 14 yêu cầu như vậy, 工数 thực tế vượt kế hoạch 12% và 窓口 chính thức của khách không hề biết.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Cấm dev nhận mọi yêu cầu qua chat và mời người dùng phòng nghiệp vụ ra khỏi kênh.
- **B.** Gửi khách 見積 tính phí cho 14 yêu cầu đã làm để bù phần 工数 bị vượt.
- **C.** Gom 14 yêu cầu, đo 工数, phân loại trong/ngoài phạm vi, rồi thống nhất với 窓口 quy trình một cửa.
- **D.** Nhắc team trong buổi họp sáng không làm việc ngoài kế hoạch và tiếp tục theo dõi.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Đúng hướng nhưng làm đột ngột, không qua 窓口; khách thấy bị đóng cửa và người dùng sẽ tìm kênh khác.
- **B** ✗ Tính phí cho việc khách chưa từng duyệt qua 窓口 sẽ gây tranh chấp; phải có fact và thỏa thuận trước.
- **C** ✅ Có fact (bao nhiêu yêu cầu, tốn bao nhiêu, cái nào ngoài phạm vi) trước, rồi xử lý gốc là kênh tiếp nhận cùng người có quyền bên khách, không đổ lỗi cho ai.
- **D** ✗ Nhắc nhở không thay đổi cơ chế; dev vẫn bị nhắn trực tiếp và 工数 tiếp tục rò rỉ.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: team lead lọc lịch sử chat và commit, lập danh sách 14 yêu cầu (người yêu cầu, ngày, 工数 thực tế, trong hay ngoài phạm vi theo 基本設計書).  
② Hành động ngay: Ngay hôm nay: thống nhất nội bộ để dev trả lời lịch sự 'em ghi nhận, sẽ chuyển qua BrSE'; BrSE nhập mọi yêu cầu mới vào 課題管理表 để không bỏ sót yêu cầu nào.  
③ Báo khách theo 報連相: Trong tuần: PM gặp 窓口 khách, trình danh sách 14 yêu cầu và tác động; đề xuất quy trình: yêu cầu qua 窓口 → BrSE phân tích → CR nếu ngoài phạm vi; bàn cách xử lý các mục ngoài phạm vi đã làm (gộp vào CR hoặc bù trừ).  
④ Gốc rễ & phòng ngừa: Ghi vào Communication plan: kênh chat chỉ dùng hỏi đáp kỹ thuật, mọi thay đổi phải có số phiếu; theo dõi % scope creep hằng tuần trong 進捗報告書; 横展開 quy tắc cho các dự án cùng khách.  

**Đừng làm:**

- Trách dev trước cả team vì 'chiều khách' — họ làm vậy vì thiếu quy tắc.
- Im lặng cho êm, đến cuối dự án mới đòi tiền cả loạt yêu cầu.

**Câu tiếng Nhật:** 今後のご依頼は、ご担当窓口経由でいただけますと幸いです。 (Kongo no go-irai wa, go-tantō madoguchi keiyu de itadakemasu to saiwai desu.) — Từ nay, chúng tôi rất mong nhận các yêu cầu thông qua đầu mối phụ trách của quý công ty.

**Trả lời 30 giây:** “Em xử lý cơ chế chứ không xử lý người: trước hết đo 14 yêu cầu đã tốn bao nhiêu và cái nào ngoài phạm vi, rồi cùng 窓口 khách đặt quy trình một cửa. Như vậy người dùng vẫn được lắng nghe, dev được bảo vệ, và mọi thay đổi có số phiếu để tính CR.”

**Tài liệu dùng:** CMP (Communication Plan), CR (Change Request), IL (Issue Log)  
**Chỉ số theo dõi:** SCR (Scope Creep), EFV (Effort Variance), CRA (CR Approval Rate)

</details>

<a id="s09"></a>

### S09 · Khách từ chối thanh toán CR đã làm

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách sản xuất C. Team đã làm 3 CR tổng cộng 60 人日 dựa trên email đồng ý của trưởng nhóm nghiệp vụ bên khách. Khi xuất hóa đơn, phòng mua hàng (購買) của khách nói không có 稟議 (phê duyệt nội bộ) nên không thể thanh toán, trong khi dự án vẫn còn 2 tháng.

**Câu hỏi:** Hướng xử lý của anh/chị là gì?

- **A.** Gửi văn bản chính thức trích điều khoản hợp đồng, yêu cầu thanh toán trong 30 ngày.
- **B.** Gom bằng chứng, cùng sales gặp 窓口 tìm hiểu vướng 稟議, đề xuất cách hợp thức hóa hoặc bù trừ.
- **C.** Tạm dừng mọi công việc cho đến khi khách xác nhận sẽ thanh toán 60 人日.
- **D.** Chấp nhận mất 60 人日 để giữ quan hệ lâu dài và rút kinh nghiệm cho lần sau.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Có thể đúng pháp lý nhưng bỏ qua 根回し, đẩy trưởng nhóm nghiệp vụ (người đã đồng ý) vào thế khó và làm quan hệ đóng băng.
- **B** ✅ Vướng mắc thật là quy trình nội bộ của khách (稟議), không phải thiện chí; giúp 窓口 có đủ hồ sơ để đi 稟議 (hợp đồng bổ sung, gộp vào phase sau, chia sẻ chi phí) giữ được cả tiền lẫn quan hệ.
- **C** ✗ Gây áp lực quá mức, có thể vi phạm nghĩa vụ phần chính của hợp đồng và đẩy rủi ro 納期 sang cả hai bên.
- **D** ✗ Bỏ 60 人日 làm giảm lợi nhuận và không sửa được lỗ hổng quy trình; chuyện sẽ lặp lại ở CR tiếp theo.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: PM tập hợp email đồng ý, 議事録, nhật ký CR và 工数 thực tế từng CR; cùng sales/pháp chế xem điều khoản thay đổi trong hợp đồng (ai có quyền duyệt CR, hình thức duyệt).  
② Hành động ngay: Cùng sales chuẩn bị 2–3 phương án: ký 変更契約 bổ sung với hồ sơ đầy đủ để khách đi 稟議; gộp vào hợp đồng phase sau; giảm một phần nếu khách duyệt ngay. Từ hôm nay, CR mới chỉ bắt đầu khi có 発注 chính thức.  
③ Báo khách theo 報連相: Trong tuần: 根回し riêng với trưởng nhóm nghiệp vụ trước, rồi sales và PM gặp 窓口 hỏi họ cần giấy tờ gì để đi 稟議 và cam kết hỗ trợ; ghi 議事録 với hạn quyết định.  
④ Gốc rễ & phòng ngừa: Gốc rễ: mình chấp nhận 'đồng ý qua email' của người không có quyền chi tiền. Ghi vào PMP/SOW: CR chỉ bắt đầu khi có 発注 hoặc chữ ký của người có thẩm quyền (ghi tên trong RACI); 横展開 cho các dự án khác.  

**Đừng làm:**

- Đổ lỗi trưởng nhóm nghiệp vụ trước mặt phòng mua hàng.
- Lén giảm chất lượng hoặc tiến độ phần chính để 'bù' cho 60 人日.

**Câu tiếng Nhật:** 本件の費用について、ご相談させていただけますでしょうか。 (Honken no hiyō ni tsuite, go-sōdan sasete itadakemasu deshō ka.) — Chúng tôi xin phép được trao đổi về chi phí của việc này được không ạ?

**Trả lời 30 giây:** “Em coi đây là vấn đề quy trình 稟議 của khách chứ không phải khách cố tình quỵt, nên em đi 根回し cùng sales, giúp 窓口 có đủ hồ sơ để hợp thức hóa hoặc bù trừ, thay vì gửi công văn hay dừng việc. Bài học em mang theo là CR chỉ bắt đầu khi người có thẩm quyền chi tiền đã duyệt.”

**Tài liệu dùng:** CR (Change Request), RACI (RACI / Responsibility Assignment Matrix), MoM (Minutes of Meeting)  
**Chỉ số theo dõi:** CRA (CR Approval Rate), GM (Gross Margin), CV (Cost Variance)

</details>

<a id="s10"></a>

### S10 · Hai phòng ban khách yêu cầu mâu thuẫn

_Mức: Trung cấp_

**Bối cảnh:** Khách ngân hàng A, đang 要件定義 (định nghĩa yêu cầu). Phòng kinh doanh (営業) muốn duyệt khoản vay nhỏ bằng 1 thao tác trên điện thoại; phòng quản lý rủi ro (リスク管理) yêu cầu 2 người duyệt và bắt buộc nhập lý do. Cả hai phát biểu trong buổi review, 窓口 IT của khách chưa chốt, và còn 2 tuần nữa phải đóng 要件定義書.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Chọn theo phòng quản lý rủi ro, vì với ngân hàng tuân thủ luôn được ưu tiên.
- **B.** Thiết kế cả hai chế độ, cấu hình được, để phòng nào cũng hài lòng.
- **C.** Họp riêng từng phòng để thuyết phục họ nhường một bước, rồi báo kết quả cho 窓口.
- **D.** Ghi mâu thuẫn vào 課題管理表 kèm phương án và tác động, nhờ 窓口 chủ trì buổi chốt trước hạn.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Có thể ra kết quả đúng nhưng là PM vendor quyết thay khách; khi phòng kinh doanh phản đối về sau, vendor phải chịu trách nhiệm.
- **B** ✗ Nghe linh hoạt nhưng làm phình phạm vi và độ phức tạp test, che giấu chứ không giải quyết mâu thuẫn nghiệp vụ.
- **C** ✗ Can thiệp vào chuyện nội bộ của khách, dễ bị xem là vượt quyền 窓口 và bị một phòng coi là đứng về phía bên kia.
- **D** ✅ Đúng vai: vendor làm rõ vấn đề và phương án, người có thẩm quyền bên khách quyết; có hạn chốt nên không làm trễ 要件定義.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: BrSE ghi chính xác yêu cầu của mỗi phòng và lý do đằng sau (quy định nội bộ nào, rủi ro gì, chỉ tiêu gì), gửi lại từng bên xác nhận bằng văn bản.  
② Hành động ngay: Soạn 2–3 phương án (vd 1 thao tác cho khoản dưới ngưỡng X, 2 người duyệt khi trên ngưỡng; hoặc duyệt nhanh rồi kiểm tra sau), mỗi phương án có tác động 工数, lịch, rủi ro tuân thủ; ghi vào 課題管理表 với hạn quyết định.  
③ Báo khách theo 報連相: Gửi 窓口 IT sớm hơn hạn đóng 要件定義書 ít nhất 1 tuần, đề nghị 窓口 mời người có thẩm quyền (trưởng dự án phía khách) chủ trì buổi chốt; vendor trình bày phương án trung lập và ghi 議事録.  
④ Gốc rễ & phòng ngừa: Lập Stakeholder Register và RACI ngay từ kick-off, ghi rõ ai quyết khi các phòng mâu thuẫn; đưa vai 'người chốt yêu cầu' vào PMP cho mọi dự án có nhiều phòng ban.  

**Đừng làm:**

- Nói với một phòng rằng phòng kia 'đang gây khó'.
- Để mâu thuẫn trôi sang 基本設計 rồi sửa đi sửa lại.

**Câu tiếng Nhật:** ご判断いただきたい論点を整理いたしました。 (Go-handan itadakitai ronten o seiri itashimashita.) — Chúng tôi đã tổng hợp các điểm cần quý công ty đưa ra quyết định.

**Trả lời 30 giây:** “Mâu thuẫn giữa hai phòng là quyết định nghiệp vụ của khách, nên em không chọn thay và cũng không đi thuyết phục từng bên. Việc của em là làm rõ yêu cầu, soạn phương án có tác động, đặt hạn chốt và nhờ 窓口 đưa người có thẩm quyền ra quyết định.”

**Tài liệu dùng:** IL (Issue Log), SHR (Stakeholder Register), RACI (RACI / Responsibility Assignment Matrix)  
**Chỉ số theo dõi:** IAGE (Issue Aging), RV (Requirement Volatility)

</details>


## Chất lượng & bug

<a id="s11"></a>

### S11 · 受入テスト tuần đầu ra 48 phiếu lỗi

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 請負; tuần đầu 受入テスト (kiểm thử nghiệm thu do khách làm) ghi 48 phiếu lỗi, trong đó 6 phiếu khách đánh mức nghiêm trọng, trong khi kế hoạch dự kiến cả đợt không quá 15. 本番 còn 5 tuần. Trưởng phòng bên khách gọi điện tỏ ý rất không hài lòng.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Trong 24 giờ phân loại 48 phiếu theo bản chất và mức độ, báo khách sơ bộ kèm kế hoạch cho phiếu nghiêm trọng.
- **B.** Huy động cả team OT cuối tuần để sửa hết 48 lỗi trước thứ Hai.
- **C.** Giải thích với khách rằng nhiều phiếu thực ra là yêu cầu mới hoặc lỗi thao tác.
- **D.** Đề nghị dừng 受入テスト, quay lại 総合テスト nội bộ 2 tuần rồi bàn giao lại.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Chưa biết 48 phiếu là gì thì chưa thể sửa đúng hay nói đúng; phân loại nhanh và báo trong ngày cho khách thấy vendor nắm tình hình và ưu tiên đúng phiếu nghiêm trọng.
- **B** ✗ Sửa ồ ạt khi chưa phân loại dễ sửa sai, sinh デグレ (lỗi hồi quy), và có thể sửa cả những thứ không phải lỗi.
- **C** ✗ Có thể đúng một phần nhưng nói khi chưa có fact là đổ lỗi, làm khách giận thêm.
- **D** ✗ Biện pháp mạnh khi chưa rõ nguyên nhân; có thể cần nhưng chỉ quyết sau khi phân loại và phải được khách đồng ý.

**Đáp án mẫu:**

① Xác nhận fact: Trong 24 giờ: BrSE và test lead phân loại 48 phiếu: lỗi thật / khác spec đã duyệt / lỗi thao tác hoặc dữ liệu / yêu cầu mới; theo mức độ và module; tìm điểm tập trung (vd phần lớn rơi vào 1 module).  
② Hành động ngay: Ưu tiên sửa 6 phiếu nghiêm trọng là lỗi thật, kèm regression test; với module tập trung lỗi, rà lại test case 総合テスト xem vì sao lọt; các phiếu 'không phải lỗi' chuẩn bị giải thích có trích tài liệu.  
③ Báo khách theo 報連相: Cuối ngày đầu: PM gọi lại trưởng phòng, báo sơ bộ (đã phân loại, kế hoạch và ngày giao bản sửa cho phiếu nghiêm trọng); trong 2 ngày họp với 窓口 thống nhất từng phiếu; báo tiến độ hằng ngày cho tới khi ổn định.  
④ Gốc rễ & phòng ngừa: Phân tích vì sao lỗi lọt qua 総合テスト (thiếu kịch bản nghiệp vụ, thiếu dữ liệu giống thật…); bổ sung test theo kịch bản nghiệp vụ của khách cho các phase sau và 横展開 sang các module tương tự.  

**Đừng làm:**

- Tranh luận từng phiếu 'lỗi hay không lỗi' qua email trước khi có buổi thống nhất.
- Giao bản sửa vội mà không chạy regression.

**Câu tiếng Nhật:** 不具合の分類結果と対応方針を本日中にご報告いたします。 (Fuguai no bunrui kekka to taiō hōshin o honjitsu-chū ni go-hōkoku itashimasu.) — Trong hôm nay chúng tôi sẽ báo cáo kết quả phân loại lỗi và phương hướng xử lý.

**Trả lời 30 giây:** “Em không sửa ồ ạt và cũng không vội nói đó không phải lỗi; trong 24 giờ em phân loại 48 phiếu rồi gọi lại khách với kế hoạch cho phiếu nghiêm trọng. Có fact rồi mới sửa đúng chỗ, nói đúng điều, và sau đó phân tích vì sao 総合テスト để lọt.”

**Tài liệu dùng:** BUG (Bug List / Defect Log), UAT (UAT & Acceptance Sign-off), QR (Quality / Test Report)  
**Chỉ số theo dõi:** DL (Defect Leakage), OPB (Open Bugs by Severity), BCV (Bug Convergence)

</details>

<a id="s12"></a>

### S12 · Khách chê lỗi chính tả trong tài liệu

_Mức: Cơ bản_

**Bối cảnh:** Khách ngân hàng A review 詳細設計書 (thiết kế chi tiết) tiếng Nhật khoảng 300 trang, trả về 120 指摘 (điểm chỉ ra), trong đó 85 là 誤字脱字 (sai/thiếu chữ) và 表記ゆれ (cách viết không thống nhất). Khách nhận xét: 'chất lượng thấp, khó tin vào nội dung'. Còn 4 tài liệu cùng loại sẽ nộp trong 3 tuần tới.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Giải thích rằng lỗi chính tả không ảnh hưởng logic, đề nghị khách tập trung review nội dung.
- **B.** Cho team sửa hết 120 指摘 và nộp lại trong 2 ngày để thể hiện thiện chí.
- **C.** Xin lỗi, phân loại 120 指摘 trong 1 ngày, lập kế hoạch sửa và rà cả 4 tài liệu sắp nộp.
- **D.** Thuê dịch vụ kiểm tra tiếng Nhật bên ngoài rà lại toàn bộ tài liệu dự án.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Với khách Nhật, tài liệu là bộ mặt của chất lượng; nói vậy khiến khách nghĩ vendor không hiểu văn hóa làm việc, mất niềm tin thêm.
- **B** ✗ Sửa nhanh là tốt nhưng chỉ chữa triệu chứng; 4 tài liệu sau vẫn sẽ mắc cùng loại lỗi.
- **C** ✅ Xin lỗi đúng mực, có fact (lỗi loại gì, ở đâu, do đâu), sửa tài liệu này và 横展開 sang tài liệu sắp nộp — khách thấy vendor xử lý tận gốc.
- **D** ✗ Tốn chi phí và thời gian, không sửa được quy trình review nội bộ; có thể là một phần giải pháp nhưng không phải bước đầu tiên.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: comtor/BrSE phân loại 120 指摘 (誤字, 表記ゆれ, thuật ngữ, nội dung), đếm theo người viết và chương; kiểm tra tài liệu có qua bước review tiếng Nhật trước khi nộp hay không.  
② Hành động ngay: Lập bảng thuật ngữ (用語集) và quy tắc ghi (表記ルール), dùng công cụ kiểm tra chính tả/表記ゆれ; sửa 120 指摘 và áp cùng checklist cho 4 tài liệu sắp nộp; BrSE review tiếng Nhật trước khi gửi.  
③ Báo khách theo 報連相: Ngay ngày hôm sau: PM gửi khách lời xin lỗi kèm kết quả phân loại, ngày nộp lại và biện pháp cho các tài liệu tiếp theo; ở lần nộp sau báo kèm số 指摘/trang để khách thấy cải thiện.  
④ Gốc rễ & phòng ngừa: Đưa vào 品質計画書: mọi tài liệu gửi khách phải qua self-check bằng công cụ và review tiếng Nhật, đo mật độ 指摘/trang theo loại; 横展開 bảng 表記ルール cho toàn bộ team.  

**Đừng làm:**

- Đổ lỗi comtor hoặc người viết trước mặt khách.
- Hứa 'sẽ không còn lỗi nào' mà không có cơ chế kiểm tra.

**Câu tiếng Nhật:** 誤字脱字が多く、大変申し訳ございません。 (Goji datsuji ga ōku, taihen mōshiwake gozaimasen.) — Tài liệu có nhiều lỗi sai, thiếu chữ, chúng tôi thành thật xin lỗi.

**Trả lời 30 giây:** “Em coi 誤字 là tín hiệu về quy trình review chứ không phải chuyện nhỏ, vì khách Nhật dùng tài liệu để đánh giá độ tin cậy. Em xin lỗi kèm fact và kế hoạch, sửa luôn cả các tài liệu sắp nộp, và đặt bước review tiếng Nhật thành cổng bắt buộc trước khi gửi.”

**Tài liệu dùng:** DD (Detailed Design (Internal Design)), QMP (Quality Management Plan), QR (Quality / Test Report)  
**Chỉ số theo dõi:** RCD (Review Comment Density), RW (Rework Rate)

</details>

<a id="s13"></a>

### S13 · Bug density thấp bất thường

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách sản xuất C, team 12 người vừa xong 結合テスト module A. Mật độ bug là 0,3 lỗi/KLOC trong khi mức thường thấy ở công ty khoảng 2–4 lỗi/KLOC (tham khảo), 100% test case pass. Team rất vui, sales muốn báo khách để đề xuất rút ngắn 総合テスト 1 tuần.

**Câu hỏi:** Anh/chị đánh giá thế nào và làm gì tiếp?

- **A.** Báo khách chất lượng vượt kỳ vọng và đề xuất rút ngắn 総合テスト 1 tuần như sales muốn.
- **B.** Coi đây là tín hiệu cần kiểm tra: xem mật độ test, độ bao phủ yêu cầu, loại test case và cách ghi bug.
- **C.** Khen team, giữ nguyên kế hoạch 総合テスト, không cần phân tích thêm.
- **D.** Yêu cầu team viết thêm 50% test case cho toàn bộ module A ngay lập tức.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Nghe là tin vui nhưng bug thấp có thể do test yếu; đã cam kết rút ngắn mà lỗi lọt ra 受入テスト thì rất khó gỡ.
- **B** ✅ Số liệu lệch xa baseline, dù tốt hay xấu, đều cần giải thích; phải kiểm tra độ đầy đủ của test trước khi kết luận về chất lượng sản phẩm.
- **C** ✗ Bỏ qua tín hiệu bất thường; không biết vì sao tốt thì cũng không biết lỗi có đang bị che không.
- **D** ✗ Có thể cần nhưng là hành động trước phân tích; viết thêm test dàn đều thay vì đúng chỗ đang thiếu.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: QA lead so mật độ test (TC/KLOC), độ bao phủ yêu cầu theo RTM, tỉ lệ test 異常系/境界値 so với 正常系, hỏi team có sửa lỗi mà không ghi phiếu không; review mẫu khoảng 10% test case (tham khảo).  
② Hành động ngay: Nếu thiếu: bổ sung test cho phần yếu (異常系, 境界値, dữ liệu lớn) và thống nhất quy tắc mọi lỗi tìm thấy trong kiểm thử đều phải ghi phiếu; nếu đủ: ghi lại nguyên nhân tốt (vd tái sử dụng module đã ổn định) làm bằng chứng.  
③ Báo khách theo 報連相: Báo khách trong 進捗報告書/定例会 bằng bộ số liệu đầy đủ (bug density + mật độ test + coverage); chưa đề xuất rút ngắn 総合テスト cho đến khi có kết quả phân tích, và giải thích rõ lý do với sales.  
④ Gốc rễ & phòng ngừa: Đặt vùng bình thường cho chỉ số chất lượng trong 品質計画書 (vd bug density ngoài 50–200% baseline là phải phân tích, tham khảo); dùng đường hội tụ bug để nhận định thay vì một con số đơn lẻ.  

**Đừng làm:**

- Coi bug density thấp là tốt mà không đặt cạnh mật độ test.
- Để sales cam kết với khách dựa trên một chỉ số đơn lẻ.

**Câu tiếng Nhật:** バグ密度が想定を下回っているため、テスト十分性を確認中です。 (Bagu mitsudo ga sōtei o shitamawatte iru tame, tesuto jūbunsei o kakunin-chū desu.) — Do mật độ lỗi thấp hơn dự kiến, chúng tôi đang kiểm tra độ đầy đủ của kiểm thử.

**Trả lời 30 giây:** “Với em, chỉ số lệch xa baseline, kể cả theo hướng tốt, là tín hiệu cần giải thích chứ chưa phải tin vui. Em kiểm tra mật độ test, coverage và cách ghi bug trước, rồi báo khách bằng bộ số liệu đầy đủ; em không để ai cam kết rút ngắn test dựa trên một con số.”

**Tài liệu dùng:** QR (Quality / Test Report), RTM (Requirements Traceability Matrix), QMP (Quality Management Plan)  
**Chỉ số theo dõi:** BD (Bug Density), TD (Test Density), RCOV (Requirement Coverage)

</details>

<a id="s14"></a>

### S14 · Sự cố lặp lại, khách đòi なぜなぜ分析

_Mức: Trung cấp_

**Bối cảnh:** Hệ thống đặt hàng của khách sản xuất C đã 本番, công ty mình bảo trì theo 準委任. Lần thứ 2 trong 2 tháng xảy ra 障害 (sự cố) tính sai tiền do làm tròn thuế, hôm nay ảnh hưởng khoảng 300 đơn hàng; lần 1 đã nộp 障害報告書 với biện pháp 'tăng cường review'. Khách yêu cầu báo cáo kèm なぜなぜ分析 (phân tích 5 Why) trong 3 ngày.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Trong vài giờ xác nhận phạm vi ảnh hưởng và biện pháp tạm thời, gửi 第一報 (báo cáo nhanh) cho khách.
- **B.** Sửa bug và deploy hotfix ngay trong đêm, viết báo cáo sau khi hệ thống ổn định.
- **C.** Viết ngay なぜなぜ分析 với kết luận dev bất cẩn, cam kết tăng review gấp đôi.
- **D.** Xin khách gia hạn báo cáo 1 tuần để phân tích kỹ, tránh kết luận vội.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Đúng thứ tự xử lý 障害: chặn thiệt hại và cho khách biết tình hình trước (bao nhiêu đơn, xử lý tạm thế nào), rồi mới phân tích gốc rễ bằng fact.
- **B** ✗ Nghe nhanh nhưng hotfix khi chưa rõ phạm vi dễ sửa thiếu hoặc sinh lỗi mới, và khách không được báo trong lúc nghiệp vụ đang chịu ảnh hưởng.
- **C** ✗ Quy cho cá nhân là kiểu なぜなぜ khách Nhật sẽ trả lại; lần 1 đã 'tăng review' mà vẫn lặp lại, nên gốc phải nằm ở quy trình.
- **D** ✗ Cẩn thận nhưng làm khách mất kiên nhẫn; đúng hơn là 第一報, 中間報告 rồi báo cáo cuối đúng hạn.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 giờ: xác định số đơn bị ảnh hưởng, khoảng thời gian, hóa đơn đã gửi ra ngoài hay chưa; cùng khách chọn 暫定対応 (tính tay, tạm dừng chức năng, sửa dữ liệu).  
② Hành động ngay: Trong ngày: sửa lỗi kèm test trên dữ liệu giống thật, deploy theo thủ tục khẩn cấp có khách đồng ý; sửa dữ liệu 300 đơn kèm danh sách đối chiếu trước/sau.  
③ Báo khách theo 報連相: 第一報 trong 2 giờ (tình hình, ảnh hưởng, 暫定対応), 中間報告 ngày 2, 障害報告書 + なぜなぜ ngày 3 do PM trình trực tiếp với 窓口; phân tích cả nguyên nhân phát sinh (vì sao code sai) và nguyên nhân lọt (vì sao test không bắt).  
④ Gốc rễ & phòng ngừa: Hỏi thêm 'vì sao biện pháp lần 1 không hiệu quả' (vd không có test case biên làm tròn, logic thuế nằm rải rác). 恒久対策: gom logic thuế vào một module dùng chung, thêm test tự động cho biên làm tròn, 横展開 rà mọi chỗ tính tiền khác.  

**Đừng làm:**

- Kết luận なぜなぜ bằng 'chú ý hơn', 'tăng cường review' — không đo được, khách sẽ trả lại.
- Chỉ báo khi đã sửa xong, để khách tự phát hiện thêm đơn sai.

**Câu tiếng Nhật:** まずは第一報として、影響範囲と暫定対応をご報告いたします。 (Mazu wa daiippō to shite, eikyō han'i to zantei taiō o go-hōkoku itashimasu.) — Trước hết, chúng tôi xin báo cáo nhanh phạm vi ảnh hưởng và biện pháp tạm thời.

**Trả lời 30 giây:** “Với 障害 lặp lại, em ưu tiên chặn thiệt hại và gửi 第一報 trong 2 giờ, rồi mới phân tích. Trong なぜなぜ em không dừng ở 'dev bất cẩn' mà hỏi tiếp vì sao biện pháp lần trước không chặn được lần này, để ra 恒久対策 đo được và 横展開 sang mọi chỗ tính tiền.”

**Tài liệu dùng:** IR (Incident Report), BUG (Bug List / Defect Log), QR (Quality / Test Report)  
**Chỉ số theo dõi:** INC (Incident Count), MTTR (Mean Time to Restore), DL (Defect Leakage)

</details>

<a id="s15"></a>

### S15 · Deadline ép bỏ bớt test

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách ngân hàng A, 総合テスト (kiểm thử hệ thống) còn 10 ngày nhưng mới chạy 55%, còn 280 test case; với tốc độ hiện tại cần thêm khoảng 14 ngày. Giám đốc sales bên mình và trưởng phòng IT bên khách cùng đề xuất bỏ 30% test case để kịp ngày 本番 đã công bố cho các chi nhánh.

**Câu hỏi:** Anh/chị quyết định thế nào?

- **A.** Đồng ý bỏ 30% test case ít quan trọng nhất để kịp 本番, vì chính khách đã đề xuất.
- **B.** Từ chối, kiên quyết chạy đủ 100% test case dù 本番 phải dời.
- **C.** Bổ sung 4 tester và tăng OT để chạy đủ 280 test case trong 10 ngày.
- **D.** Xếp hạng test case theo rủi ro, chạy hết nhóm cao, trình khách rủi ro còn lại để khách quyết bằng văn bản.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Bỏ theo cảm tính 'ít quan trọng' mà không phân tích rủi ro; khi 障害 xảy ra ở phần bị bỏ, vendor 請負 vẫn chịu trách nhiệm.
- **B** ✗ Bảo vệ chất lượng nhưng bỏ qua ràng buộc kinh doanh của khách; PM senior phải đưa ra lựa chọn chứ không chỉ nói không.
- **C** ✗ Tester mới cần thời gian hiểu nghiệp vụ ngân hàng, OT 10 ngày liền làm tăng sai sót; có thể là một phần phương án nhưng không tự giải quyết được.
- **D** ✅ Cân cả thời gian lẫn rủi ro: phần nguy hiểm (tiền, pháp lý, dữ liệu) được test đủ, phần còn lại có biện pháp bù (test sau 本番, giám sát tăng cường) và rủi ro được khách chấp nhận rõ ràng.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: test lead xếp 280 test case theo rủi ro (tính tiền, pháp lý/báo cáo, số người dùng, tần suất) và theo tình trạng module (số bug mở, đường hội tụ bug); tính số test case chạy được trong 10 ngày.  
② Hành động ngay: Lập kế hoạch: chạy 100% nhóm rủi ro cao và trung bình; nhóm thấp đề xuất test trong 2 tuần sau 本番 với giám sát tăng cường và quy trình rollback; xin thêm 1–2 tester đã quen hệ thống nếu có.  
③ Báo khách theo 報連相: Trong 2 ngày: PM trình trưởng phòng IT (có sales cùng dự) danh sách test case không chạy trước 本番, rủi ro và biện pháp bù; xin quyết định go/no-go bằng văn bản, ghi vào 議事録 và 品質報告書.  
④ Gốc rễ & phòng ngừa: Từ dự án sau: áp dụng risk-based testing ngay trong テスト計画書, theo dõi テスト消化率 hằng ngày và cảnh báo sớm khi tốc độ thực thấp hơn kế hoạch 10% (tham khảo).  

**Đừng làm:**

- Ngầm bỏ test nhưng vẫn báo cáo '100% pass'.
- Để sales quyết thay khách và thay PM về rủi ro chất lượng.

**Câu tiếng Nhật:** 残存リスクをご確認のうえ、ご判断をお願いいたします。 (Zanzon risuku o go-kakunin no ue, go-handan o onegai itashimasu.) — Kính mong quý công ty xác nhận các rủi ro còn lại rồi đưa ra quyết định.

**Trả lời 30 giây:** “Em không đồng ý bỏ test theo cảm tính, cũng không chỉ nói không: em xếp hạng test case theo rủi ro, chạy đủ phần liên quan tiền và pháp lý, phần còn lại có biện pháp bù. Rủi ro còn lại là quyết định của khách, nên em trình bằng văn bản và xin go/no-go chính thức.”

**Tài liệu dùng:** TP (Test Plan), QR (Quality / Test Report), RLP (Release / Cutover Plan)  
**Chỉ số theo dõi:** TEX (Test Execution Rate), OPB (Open Bugs by Severity), BCV (Bug Convergence)

</details>


## Sự cố 本番

<a id="s16"></a>

### S16 · Lỗi tính lãi phát hiện sau 3 tuần 本番

_Mức: Khó_

**Bối cảnh:** Khách ngân hàng A, hợp đồng 請負 (khoán trọn gói), module tính lãi tiền gửi có kỳ hạn đã chạy 本番 (production) được 3 tuần. Chiều thứ Năm, team offshore 15 người tự phát hiện quy tắc làm tròn sai khi ngày đáo hạn rơi vào ngày nghỉ, ước tính sơ bộ khoảng 1.200 tài khoản lệch vài yên. Khách chưa phát hiện; kỳ trả lãi tiếp theo là thứ Hai tuần sau.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Cho dev sửa công thức và deploy hotfix ngay tối nay để kịp trước kỳ trả lãi thứ Hai.
- **B.** Chờ xác minh đủ 100% tài khoản bị ảnh hưởng rồi mới báo khách, tránh báo sai số.
- **C.** Trong 2 giờ khoanh vùng điều kiện lỗi và số tài khoản sơ bộ, rồi báo ngay 窓口 khách bằng 第一報.
- **D.** Báo khách rằng nguyên nhân là 詳細設計 khách đã duyệt không ghi rõ quy tắc ngày nghỉ.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Nghe chủ động nhưng sửa trước khi xác nhận phạm vi, và tự deploy 本番 ngân hàng không qua phê duyệt thay đổi của khách có thể gây lỗi thứ hai.
- **B** ✗ Fact 100% có thể mất vài ngày; ngân hàng cần biết sớm để quyết phương án cho kỳ trả lãi thứ Hai, báo muộn bị coi là che giấu.
- **C** ✅ Đúng nhịp: fact sơ bộ trong thời gian ngắn rồi báo ngay, để khách còn thời gian quyết phương án trước kỳ trả lãi; số liệu chi tiết cập nhật sau.
- **D** ✗ Đổ lỗi spec khi chưa phân tích gốc rễ làm khách phòng thủ; với 請負, vendor chịu trách nhiệm về độ phủ test của mình.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 giờ: tech lead tái hiện lỗi trên môi trường test, xác nhận điều kiện (đáo hạn rơi vào ngày nghỉ), truy vấn 本番 chế độ read-only để ra danh sách tài khoản và tổng chênh lệch sơ bộ.  
② Hành động ngay: Không tự deploy; chuẩn bị song song bản sửa + script tính lại có review chéo, đề xuất phương án tạm (giữ lại kỳ trả lãi của các tài khoản bị ảnh hưởng hoặc tính tay) để khách chọn.  
③ Báo khách theo 報連相: Gửi 第一報 (báo cáo đầu tiên) cho 窓口 và trưởng nhóm phía khách ngay chiều thứ Năm: hiện tượng, phạm vi sơ bộ, phương án đề xuất, giờ báo tiếp; 障害報告書 chính thức trong 2 ngày làm việc.  
④ Gốc rễ & phòng ngừa: Phân tích 5 Why: thiếu test case biên về ngày nghỉ, cuối tháng; bổ sung bộ test lịch nghiệp vụ, review chéo với người nắm nghiệp vụ, 横展開 (rà ngang) sang các module tính phí, lãi vay.  

**Đừng làm:**

- Tự hotfix 本番 hệ thống ngân hàng không qua quy trình phê duyệt thay đổi của khách.
- Giấu lỗi vì 'khách chưa phát hiện, chỉ lệch vài yên' — khi khách tự tìm ra thì mất niềm tin hoàn toàn.

**Câu tiếng Nhật:** 本番障害につきまして、第一報をご報告いたします。 (Honban shōgai ni tsukimashite, daiippō o go-hōkoku itashimasu.) — Về sự cố production, bên em xin gửi báo cáo đầu tiên.

**Trả lời 30 giây:** “Em dành tối đa 2 giờ khoanh vùng điều kiện lỗi và số tài khoản bị ảnh hưởng, rồi gửi 第一報 cho khách ngay dù chưa có số cuối cùng. Với ngân hàng, nguyên tắc là báo sớm bằng fact sơ bộ và không tự deploy 本番, để khách quyết phương án cho kỳ trả lãi thứ Hai.”

**Tài liệu dùng:** IR (Incident Report), BUG (Bug List / Defect Log), TS (Test Specification / Test Cases)  
**Chỉ số theo dõi:** DL (Defect Leakage), INC (Incident Count), MTTR (Mean Time to Restore)

</details>

<a id="s17"></a>

### S17 · 夜間バッチ dừng giữa chừng lúc 3h sáng

_Mức: Cơ bản_

**Bối cảnh:** Khách sản xuất C, hợp đồng 準委任 (bảo trì vận hành), team 8 người. 1h sáng giờ Việt Nam (3h giờ Nhật), 夜間バッチ (batch đêm) tổng hợp tồn kho dừng ở job 5/12 với lỗi timeout DB. Nhà máy vào ca lúc 8h giờ Nhật và cần báo cáo tồn kho từ batch này; runbook đã được khách duyệt có bước rerun từ job lỗi.

**Câu hỏi:** Người trực on-call gọi anh/chị. Anh/chị chỉ đạo việc đầu tiên thế nào?

- **A.** Đọc log xác nhận nguyên nhân và dữ liệu job 1–4, đúng runbook thì rerun từ job 5.
- **B.** Rerun toàn bộ 12 job từ đầu để chắc chắn dữ liệu sạch, khỏi mất thời gian đọc log.
- **C.** Gọi ngay 窓口 khách lúc 3h sáng giờ Nhật xin phép trước khi chạm vào hệ thống.
- **D.** Tăng ngưỡng timeout trong config rồi rerun, vì lỗi timeout cho thấy ngưỡng đang đặt quá thấp.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Đúng thứ tự: dành vài phút xác nhận fact (nguyên nhân, dữ liệu đã commit) rồi khôi phục theo runbook đã được duyệt, kịp giờ nhà máy cần.
- **B** ✗ Rerun từ đầu có thể nhân đôi dữ liệu của job 1–4 và mất gấp đôi thời gian, dễ trễ ca sáng.
- **C** ✗ Runbook đã cho phép rerun; gọi khách lúc 3h sáng khi chưa có fact chỉ làm khách lo, nên báo trước giờ họ cần dữ liệu.
- **D** ✗ Sửa config 本番 lúc nửa đêm khi chưa biết nguyên nhân thật (có thể do lock hoặc dữ liệu tăng), lại là thay đổi chưa được duyệt.

**Đáp án mẫu:**

① Xác nhận fact: Trong 15–20 phút (tham khảo): đọc log job 5, kiểm tra DB (lock, dung lượng, job khác chạy chồng), xác nhận job 1–4 đã commit đủ, ước thời gian rerun có kịp trước 8h giờ Nhật.  
② Hành động ngay: Rerun từ job 5 theo runbook, theo dõi đến job 12; nếu lỗi lần 2 hoặc dự kiến xong sau 7h giờ Nhật thì gọi tech lead và chuẩn bị phương án dự phòng (báo cáo tồn kho ngày trước).  
③ Báo khách theo 報連相: Email cho 窓口 trước 8h giờ Nhật: sự cố, thời gian dừng, giờ rerun xong, dữ liệu đã kiểm; nếu chưa xong thì báo trước 7h kèm phương án tạm; 障害報告書 (báo cáo sự cố) trong ngày.  
④ Gốc rễ & phòng ngừa: Tìm gốc timeout (dữ liệu tăng, thiếu index, trùng lịch backup), đề xuất sửa qua quy trình thay đổi có duyệt, thêm cảnh báo thời gian chạy batch và 横展開 kiểm tra các batch đêm khác.  

**Đừng làm:**

- Rerun toàn bộ batch mà không kiểm tra các job đã commit, gây nhân đôi dữ liệu.
- Rerun xong là thôi, không báo khách vì 'đã ổn' — khách phát hiện qua log sẽ mất niềm tin.

**Câu tiếng Nhật:** 夜間バッチ障害と復旧状況をご報告いたします。 (Yakan batchi shōgai to fukkyū jōkyō o go-hōkoku itashimasu.) — Bên em xin báo cáo sự cố batch đêm và tình trạng khôi phục.

**Trả lời 30 giây:** “Em cho xác nhận fact trong 15–20 phút: nguyên nhân lỗi và trạng thái các job đã chạy, đúng runbook thì rerun từ job lỗi. Nguyên tắc của em là khôi phục theo quy trình khách đã duyệt, không đổi cấu hình lúc nửa đêm, và báo khách trước giờ họ cần dữ liệu.”

**Tài liệu dùng:** IR (Incident Report), IL (Issue Log)  
**Chỉ số theo dõi:** MTTR (Mean Time to Restore), INC (Incident Count), SLO (SLI / SLO / SLA)

</details>

<a id="s18"></a>

### S18 · Dữ liệu địa chỉ khách sai sau release

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 請負, team 12 người. Release thứ Ba có migration chuyển đổi địa chỉ người được bảo hiểm; sáng thứ Tư call center của khách báo 3 trường hợp địa chỉ hiển thị sai tỉnh. Thư thông báo phí bảo hiểm sẽ được in từ dữ liệu này vào tối thứ Sáu.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Rollback ngay toàn bộ release thứ Ba về phiên bản cũ để dừng lỗi lan rộng.
- **B.** Viết script sửa 3 bản ghi khách báo ngay sáng nay để call center tiếp tục làm việc.
- **C.** Họp team truy nguyên nhân migration trước, có root cause rồi mới báo khách cho đầy đủ.
- **D.** Đối chiếu dữ liệu trước/sau migration để đếm bản ghi sai, đồng thời báo khách xin tạm dừng in thư.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Rollback ứng dụng không đảo ngược được migration dữ liệu và có thể mất dữ liệu phát sinh sau release; quyết định lớn khi chưa có fact.
- **B** ✗ Chỉ chữa triệu chứng ở 3 bản ghi khách thấy, trong khi có thể hàng nghìn bản ghi sai đang chờ in thư.
- **C** ✗ Tìm root cause có thể mất 1–2 ngày; khách cần biết ngay để chặn việc in thư, phạm vi ảnh hưởng quan trọng hơn nguyên nhân lúc này.
- **D** ✅ Đối chiếu snapshot là cách lấy fact phạm vi nhanh nhất, và xin tạm dừng in thư chặn thiệt hại không đảo ngược được (thư sai địa chỉ = lộ thông tin cá nhân).

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 giờ: so sánh backup trước migration với dữ liệu hiện tại theo mã hợp đồng, ra số bản ghi sai và quy luật (vd địa chỉ có ký tự đặc biệt, mã bưu chính cũ); kiểm tra hệ thống hạ nguồn nào đã dùng dữ liệu này.  
② Hành động ngay: Đề xuất khách tạm dừng job in thư và khóa chỉnh sửa trên các bản ghi bị ảnh hưởng; chuẩn bị script sửa từ backup, chạy thử trên staging, review chéo trước khi xin duyệt áp dụng 本番.  
③ Báo khách theo 報連相: Gọi điện + email 第一報 cho 窓口 trước trưa thứ Tư: số bản ghi sai sơ bộ, rủi ro thư sai địa chỉ, đề xuất dừng in; cập nhật 2 lần/ngày đến khi sửa xong, 障害報告書 sau khi khôi phục.  
④ Gốc rễ & phòng ngừa: Gốc rễ thường là thiếu bước đối chiếu sau migration; thêm reconcile (đếm bản ghi, checksum, lấy mẫu) vào 本番移行計画書, test migration bằng bản sao dữ liệu thật đã ẩn danh, 横展開 cho các migration sắp tới.  

**Đừng làm:**

- Rollback cả release khi chưa biết dữ liệu phát sinh sau release sẽ bị ảnh hưởng thế nào.
- Chỉ sửa đúng 3 bản ghi khách báo mà không đo phạm vi thật.

**Câu tiếng Nhật:** 印刷処理の一時停止についてご相談させてください。 (Insatsu shori no ichiji teishi ni tsuite go-sōdan sasete kudasai.) — Cho phép bên em được bàn về việc tạm dừng xử lý in.

**Trả lời 30 giây:** “Em đo phạm vi trước bằng cách đối chiếu snapshot trước và sau migration, đồng thời đề nghị khách tạm dừng in thư vì đó là thiệt hại không đảo ngược được. Nguyên tắc: chặn lan rộng ở hạ nguồn trước, sửa dữ liệu khi đã rõ phạm vi và được khách duyệt, không rollback mù.”

**Tài liệu dùng:** IR (Incident Report), RLP (Release / Cutover Plan), BUG (Bug List / Defect Log)  
**Chỉ số theo dõi:** DL (Defect Leakage), CFR (Change Failure Rate), INC (Incident Count)

</details>

<a id="s19"></a>

### S19 · Sự cố 2h sáng, không gọi được 窓口

_Mức: Trung cấp_

**Bối cảnh:** Khách tài chính D, hợp đồng 準委任 vận hành, SLA phản hồi sự cố 30 phút. 2h sáng giờ Nhật, hệ thống tiếp nhận hồ sơ online trả lỗi 500 cho 100% request; on-call xác định nguyên nhân là chứng chỉ SSL nội bộ hết hạn, gia hạn mất khoảng 20 phút. Đã gọi 窓口 (đầu mối) 3 lần và người dự phòng 2 lần đều không nghe máy; hợp đồng quy định mọi thay đổi 本番 phải có khách đồng ý.

**Câu hỏi:** Anh/chị quyết định thế nào trong 30 phút tới?

- **A.** Tự gia hạn chứng chỉ ngay vì nguyên nhân đã rõ, sáng mai giải thích lại với khách.
- **B.** Gọi tiếp tuyến escalation trong 体制図, email ghi nhận các lần gọi, chuẩn bị sẵn thao tác chờ đồng ý.
- **C.** Đợi 9h sáng giờ Nhật khi 窓口 đi làm rồi báo cáo đầy đủ một lần cho gọn.
- **D.** Chuyển hệ thống sang trang bảo trì để ngừng lỗi 500, chờ khách xác nhận rồi mới gia hạn.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Đúng kỹ thuật nhưng vượt quyền hợp đồng; nếu thao tác gây lỗi khác, toàn bộ trách nhiệm thuộc vendor và khách mất niềm tin vào kiểm soát thay đổi.
- **B** ✅ Tuân thủ hợp đồng mà vẫn rút ngắn thời gian: đi hết tuyến escalation đã thỏa thuận, có bằng chứng thời gian, thao tác sẵn sàng chạy ngay khi một người có thẩm quyền đồng ý.
- **C** ✗ Để hệ thống chết 7 tiếng và vi phạm SLA 30 phút; khách sẽ hỏi vì sao không báo bằng văn bản dù không gọi được.
- **D** ✗ Trang bảo trì cũng là thay đổi 本番 chưa được duyệt và không xử lý gốc; nghe an toàn nhưng vẫn vượt quyền.

**Đáp án mẫu:**

① Xác nhận fact: 10 phút: xác nhận lại nguyên nhân (ngày hết hạn chứng chỉ, log), phạm vi (100% request, từ mấy giờ), có mất hồ sơ đã nộp không; ghi timeline từng cuộc gọi.  
② Hành động ngay: Gọi lần lượt tuyến escalation trong 体制図 (sơ đồ tổ chức) và kế hoạch liên lạc (người trực hệ thống, 課長, 部長), gửi email + chat ghi nhận; chuẩn bị thủ tục gia hạn đã thử trên staging để chạy ngay khi có đồng ý.  
③ Báo khách theo 報連相: Email 第一報 trong 30 phút theo SLA dù chưa ai nghe máy: hiện tượng, nguyên nhân, thao tác đề xuất, thời gian dự kiến 20 phút; khôi phục xong gửi 復旧報告, 障害報告書 trong 2 ngày.  
④ Gốc rễ & phòng ngừa: Gốc rễ: không giám sát hạn chứng chỉ và tuyến liên lạc đêm chỉ có 2 người; đề xuất cảnh báo trước 30 ngày, kiểm kê mọi chứng chỉ (横展開), thỏa thuận với khách điều khoản 'làm trước, báo sau' cho lỗi đã biết rõ.  

**Đừng làm:**

- Tự sửa 本番 vì 'chắc chắn đúng' mà không có đồng ý — vượt quyền dù kết quả tốt.
- Không ghi thời điểm các lần gọi, sau này không chứng minh được đã tuân thủ SLA.

**Câu tiếng Nhật:** 緊急のため、取り急ぎメールにてご報告いたします。 (Kinkyū no tame, toriisogi mēru nite go-hōkoku itashimasu.) — Vì khẩn cấp, bên em xin phép báo cáo nhanh qua email.

**Trả lời 30 giây:** “Em đi hết tuyến escalation đã thỏa thuận, gửi 第一報 bằng email đúng SLA và ghi timeline từng cuộc gọi, thao tác sửa để sẵn chờ người có thẩm quyền đồng ý. Nguyên tắc: tốc độ không đổi bằng vượt quyền hợp đồng; sau sự cố em đề xuất thêm điều khoản xử lý khẩn cấp để lần sau không bị kẹt.”

**Tài liệu dùng:** CMP (Communication Plan), OBS (Organizational Breakdown Structure), IR (Incident Report)  
**Chỉ số theo dõi:** MTTR (Mean Time to Restore), SLO (SLI / SLO / SLA), AVL (Availability)

</details>

<a id="s20"></a>

### S20 · Release lỗi đúng tuần 年度末

_Mức: Khó_

**Bối cảnh:** Khách sản xuất C, hợp đồng 請負, release hệ thống quản lý công nợ ngày 25/3 để kịp 年度末 (cuối năm tài chính, 31/3). Sau 1 ngày, báo cáo công nợ theo đối tác lệch số dư với 15% đối tác; chức năng hóa đơn mới chạy tốt và kế toán khách đã nhập 2.000 chứng từ trên bản mới. Kế toán phải chốt sổ ngày 31/3.

**Câu hỏi:** Khách hỏi 'rollback hay fix-forward?'. Anh/chị đề xuất thế nào?

- **A.** Rollback ngay về bản cũ vì rollback là cách an toàn nhất trong tuần 年度末.
- **B.** Fix-forward bằng hotfix trong 24 giờ, cả team OT trong tuần để chắc chắn kịp chốt sổ.
- **C.** Trong nửa ngày so sánh các phương án theo dữ liệu, rủi ro, thời gian, kèm cách tạm để khách quyết.
- **D.** Đề nghị khách lùi chốt sổ sang tuần sau để team có thời gian sửa triệt để.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Rollback làm mất hoặc buộc nhập lại 2.000 chứng từ trong tuần chốt sổ; an toàn về kỹ thuật nhưng không an toàn cho nghiệp vụ khách.
- **B** ✗ Cam kết 24 giờ khi chưa phân tích, dựa vào OT và bỏ qua test hồi quy — dễ sinh lỗi mới đúng tuần quan trọng nhất.
- **C** ✅ Đây là trade-off khách phải quyết: PM đưa phương án có số liệu (2.000 chứng từ, thời gian sửa, rủi ro hồi quy) và cách tạm (đối soát tay 15% đối tác) để khách chọn trong ngày.
- **D** ✗ Hạn chốt sổ 年度末 gắn với quyết toán và kiểm toán của khách, gần như không lùi được; đề nghị này cho thấy chưa hiểu nghiệp vụ.

**Đáp án mẫu:**

① Xác nhận fact: Trong 4 giờ: xác định nguyên nhân lệch số dư và danh sách đối tác bị ảnh hưởng; đánh giá rollback có giữ được 2.000 chứng từ không, fix-forward cần bao nhiêu giờ sửa + test hồi quy.  
② Hành động ngay: Lập bảng so sánh 2–3 phương án (rollback + nhập lại; hotfix + test hồi quy rút gọn; giữ bản mới + đối soát tay 15% đối tác), mỗi phương án có thời gian, rủi ro, người làm; khóa mọi thay đổi khác vào 本番 trong tuần.  
③ Báo khách theo 報連相: Họp khẩn với 窓口 và trưởng kế toán khách ngay ngày 26/3, trình phương án khuyến nghị; chốt quyết định bằng email và 議事録 (biên bản họp), báo tiến độ 2 lần/ngày đến 31/3.  
④ Gốc rễ & phòng ngừa: Gốc rễ: release sát 年度末 và thiếu test đối soát số dư với dữ liệu thật; đề xuất freeze release 2 tuần trước 年度末/決算 (tham khảo), thêm test đối chiếu số dư vào 総合テスト, 横展開 lịch freeze cho các khách khác.  

**Đừng làm:**

- Chọn thay khách giữa rollback và fix-forward khi người chịu thiệt hại là khách.
- Hứa hotfix 24 giờ bằng OT mà không tính thời gian test hồi quy.

**Câu tiếng Nhật:** 対応方針を二案ご用意しましたので、ご判断をお願いいたします。 (Taiō hōshin o ni-an go-yōi shimashita node, go-handan o onegai itashimasu.) — Bên em đã chuẩn bị hai phương án xử lý, kính mong anh/chị quyết định.

**Trả lời 30 giây:** “Em không chọn thay khách: trong nửa ngày em đưa 2–3 phương án có số liệu về dữ liệu, thời gian, rủi ro, kèm cách tạm để kế toán vẫn chốt sổ được. Nguyên tắc là chặn thiệt hại không đảo ngược trước, trade-off thuộc về người chịu thiệt hại, sau đó đề xuất freeze release trước 年度末.”

**Tài liệu dùng:** IR (Incident Report), RLP (Release / Cutover Plan), MoM (Minutes of Meeting)  
**Chỉ số theo dõi:** CFR (Change Failure Rate), MTTR (Mean Time to Restore), DL (Defect Leakage)

</details>


## Khách hàng & giao tiếp

<a id="s21"></a>

### S21 · 課長 phía khách nổi giận giữa 定例会

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 準委任, 定例会 (họp định kỳ) hằng tuần có 6 người phía khách gồm 課長. Giữa buổi, 課長 lớn tiếng vì một loại bug đã báo 2 lần lại tái phát ở 受入テスト (kiểm thử nghiệm thu) và nói 'bên anh không học được gì'. BrSE trẻ đang phiên dịch và bắt đầu giải thích nguyên nhân kỹ thuật.

**Câu hỏi:** Anh/chị (PM) phản ứng thế nào ngay trong buổi họp?

- **A.** Để BrSE giải thích hết nguyên nhân kỹ thuật cho khách hiểu đây không phải lỗi cẩu thả.
- **B.** Tự lên tiếng nhận trách nhiệm, xin lỗi ngắn, nhắc lại đúng vấn đề, hẹn mốc gửi báo cáo đối sách.
- **C.** Đề nghị tạm gác chủ đề này, chuyển sang agenda tiếp theo cho không khí bớt căng.
- **D.** Cam kết ngay tại chỗ cả team sẽ test lại toàn bộ chức năng trong tuần này.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Giải thích kỹ thuật lúc khách đang giận nghe như bào chữa và khiến 課長 giận hơn; nguyên nhân để vào báo cáo sau.
- **B** ✅ Khách giận vì thấy không được lắng nghe; PM chủ động nhận, nhắc lại đúng điểm đau (tái phát lần 3) và hẹn mốc cụ thể giúp hạ nhiệt mà không hứa suông.
- **C** ✗ Chuyển chủ đề khi 課長 đang bức xúc bị coi là né tránh, làm khách mất mặt trước cấp dưới.
- **D** ✗ Hứa test lại toàn bộ trong 1 tuần khi chưa đánh giá khối lượng — dễ thất hứa lần nữa, tệ hơn lỗi ban đầu.

**Đáp án mẫu:**

① Xác nhận fact: Ngay trong họp: PM lên tiếng thay BrSE, nhắc lại vấn đề (bug X tái phát lần 3 ở 受入テスト) để xác nhận hiểu đúng; sau họp trong 2 giờ, kiểm tra 2 lần trước đã có đối sách gì và vì sao không hiệu quả.  
② Hành động ngay: Khoanh vùng: rà các bug cùng loại đang mở và đã đóng, test lại các màn hình liên quan; chỉ định 1 người chịu trách nhiệm phân tích gốc rễ.  
③ Báo khách theo 報連相: Trong ngày gửi email xin lỗi + cảm ơn góp ý tới 課長 kèm mốc; trước 定例会 tuần sau gửi báo cáo nguyên nhân và 再発防止策, gặp riêng 課長 15 phút trước họp (根回し – trao đổi trước) để thống nhất.  
④ Gốc rễ & phòng ngừa: Gốc rễ thường là đối sách lần trước chỉ sửa điểm, không sửa quy trình; thêm checklist review cho loại lỗi này, test hồi quy tự động, 横展開 sang module khác, theo dõi tỉ lệ tái phát trong 進捗報告書.  

**Đừng làm:**

- Để BrSE trẻ đứng ra đỡ đòn và tranh luận kỹ thuật trước mặt 課長.
- Hứa 'sẽ không bao giờ tái phát' mà không có đối sách đo được.

**Câu tiếng Nhật:** ご指摘の通りです。誠に申し訳ございません。 (Go-shiteki no tōri desu. Makoto ni mōshiwake gozaimasen.) — Đúng như anh/chị đã chỉ ra. Chúng tôi thành thật xin lỗi.

**Trả lời 30 giây:** “Em tự lên tiếng thay BrSE, nhận trách nhiệm, nhắc lại đúng vấn đề khách nêu và hẹn mốc gửi báo cáo nguyên nhân + đối sách trước 定例会 tuần sau. Nguyên tắc: trong phòng họp không tranh luận nguyên nhân, hạ nhiệt bằng cam kết có mốc, rồi 根回し với 課長 trước buổi sau.”

**Tài liệu dùng:** MoM (Minutes of Meeting), BUG (Bug List / Defect Log), QR (Quality / Test Report)  
**Chỉ số theo dõi:** CLM (Complaints), CSAT (Customer Satisfaction), DL (Defect Leakage)

</details>

<a id="s22"></a>

### S22 · 担当者 phía khách đổi người giữa dự án

_Mức: Cơ bản_

**Bối cảnh:** Khách ngân hàng A, hợp đồng 請負, đang ở giai đoạn 詳細設計 (thiết kế chi tiết). 担当者 (người phụ trách) phía khách chuyển phòng ban từ 1/4, người mới nhận việc sau 1 tuần bàn giao. 課題管理表 (bảng quản lý issue) có 18 issue mở, trong đó 5 issue người cũ đã đồng ý bằng lời trong họp nhưng chưa ghi vào 議事録.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Gửi người mới toàn bộ tài liệu dự án để họ tự đọc và nắm tình hình.
- **B.** Tranh thủ tuần bàn giao để người cũ chốt nhanh thêm các quyết định đang treo.
- **C.** Chờ người mới ổn định 2–3 tuần rồi mới hẹn họp làm quen, tránh làm phiền.
- **D.** Xin người cũ xác nhận bằng văn bản 5 thỏa thuận miệng, rồi đề xuất họp bàn giao 3 bên.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Đẩy hàng trăm trang cho người mới tự đọc không giúp họ biết đâu là quyết định đã chốt và đâu là việc đang chờ họ.
- **B** ✗ Ép người sắp rời quyết thêm việc dễ ra quyết định thiếu cân nhắc, người mới có thể lật lại.
- **C** ✗ Chờ 2–3 tuần làm 18 issue tồn đọng thêm và thỏa thuận miệng mất người làm chứng.
- **D** ✅ Rủi ro lớn nhất là mất các thỏa thuận chưa có văn bản; chốt bằng chữ khi người cũ còn đó và họp 3 bên giúp người mới tiếp nhận đúng bối cảnh.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1–2 ngày: rà 課題管理表, 議事録, email để lập danh sách quyết định đã chốt, thỏa thuận miệng (5 issue), issue còn mở; hỏi phạm vi quyền hạn của người mới có giống người cũ không.  
② Hành động ngay: Gửi người cũ danh sách 5 thỏa thuận miệng xin xác nhận bằng email và ghi vào 議事録; chuẩn bị tài liệu bàn giao 2–3 trang (mục tiêu, tiến độ, quyết định, issue đang chờ khách).  
③ Báo khách theo 報連相: Đề xuất họp bàn giao 3 bên (người cũ, người mới, PM/BrSE) ngay trong tuần bàn giao, sau đó họp làm quen riêng với người mới; cập nhật 体制図 và danh sách liên lạc.  
④ Gốc rễ & phòng ngừa: Gốc rễ: thỏa thuận miệng không ghi lại; quy định mọi quyết định trong họp phải vào 議事録 gửi trong 24 giờ và được khách xác nhận, 横展開 cho các dự án khác.  

**Đừng làm:**

- Coi thỏa thuận miệng của người cũ là đã chốt — người mới có quyền lật lại.
- Dồn người cũ quyết thêm việc trong tuần cuối khi họ không còn chịu trách nhiệm.

**Câu tiếng Nhật:** 引き継ぎのため、三者でのお打ち合わせをお願いできますでしょうか。 (Hikitsugi no tame, sansha de no o-uchiawase o onegai dekimasu deshō ka.) — Để bàn giao, anh/chị có thể sắp xếp một buổi họp ba bên được không ạ?

**Trả lời 30 giây:** “Em ưu tiên chốt bằng văn bản các thỏa thuận miệng khi người cũ còn ở đó, rồi tổ chức họp bàn giao 3 bên để người mới nắm bối cảnh. Nguyên tắc: đổi người phía khách là rủi ro mất quyết định, nên phải biến mọi thứ thành tài liệu trước khi người cũ rời đi.”

**Tài liệu dùng:** IL (Issue Log), MoM (Minutes of Meeting), SHR (Stakeholder Register)  
**Chỉ số theo dõi:** IAGE (Issue Aging), QART (Q&A Response Time)

</details>

<a id="s23"></a>

### S23 · Khách im lặng, QA quá hạn 2 tuần

_Mức: Cơ bản_

**Bối cảnh:** Khách sản xuất C, hợp đồng 請負, giai đoạn 基本設計 (thiết kế cơ bản). QA管理表 có 12 câu hỏi quá hạn trả lời trung bình 14 ngày, 4 câu chặn việc thiết kế màn hình tính giá; team 10 người đang làm các phần không phụ thuộc. Mốc nộp 基本設計書 còn 3 tuần.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Phân loại 12 câu theo mức chặn, gửi 窓口 danh sách ưu tiên kèm phương án đề xuất và hạn trả lời mới.
- **B.** Tự đặt giả định cho 4 câu chặn để team làm tiếp, khi khách trả lời thì sửa sau.
- **C.** Escalate lên 部長 phía khách vì 窓口 đã chậm quá lâu, ảnh hưởng trực tiếp đến 納期 dự án.
- **D.** Đưa cả 12 câu vào agenda 定例会 tới để hỏi trực tiếp và chốt từng câu với khách tại chỗ.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Khách thường chậm vì câu hỏi khó trả lời; gửi kèm phương án đề xuất và nói rõ tác động 納期 (hạn giao) giúp khách quyết nhanh mà vẫn giữ quan hệ với 窓口.
- **B** ✗ Giả định chưa được khách đồng ý dễ dẫn đến 手戻り (làm lại) và tranh chấp phạm vi khi khách trả lời khác.
- **C** ✗ Escalate qua đầu 窓口 khi chưa nhắc có hạn rõ ràng làm 窓口 mất mặt, quan hệ xấu đi lâu dài.
- **D** ✗ Đợi đến 定例会 mất thêm nhiều ngày, và dồn 12 câu một lúc khiến khách không trả lời kịp tại chỗ.

**Đáp án mẫu:**

① Xác nhận fact: Trong ngày: chia 12 câu thành chặn/không chặn, ghi tác động từng câu (trễ bao nhiêu ngày nếu chưa có trả lời), kiểm tra câu hỏi đã rõ chưa, có cần người khác phía khách trả lời không.  
② Hành động ngay: Viết lại 4 câu chặn dạng có phương án (A/B + khuyến nghị) để khách chỉ cần chọn; team tiếp tục phần không phụ thuộc; nếu buộc phải làm trước thì dùng giả định ghi rõ và được khách đồng ý tạm.  
③ Báo khách theo 報連相: Gửi 窓口 email danh sách ưu tiên + hạn trả lời mới (vd 4 câu chặn trước thứ Sáu), nêu rõ ảnh hưởng 納期; gọi điện hoặc chat ngắn xác nhận đã nhận, theo dõi tại 定例会.  
④ Gốc rễ & phòng ngừa: Thỏa thuận SLA trả lời QA (vd 3 ngày làm việc – tham khảo), báo QA回答日数 hằng tuần trong 進捗報告書, câu hỏi luôn kèm phương án đề xuất; quá hạn 2 lần mới đưa lên cấp trên phía khách.  

**Đừng làm:**

- Tự giả định rồi coi im lặng là khách đã đồng ý.
- Escalate qua đầu 窓口 khi chưa gửi nhắc có hạn rõ ràng.

**Câu tiếng Nhật:** ご多忙のところ恐縮ですが、ご回答をお願いいたします。 (Go-tabō no tokoro kyōshuku desu ga, go-kaitō o onegai itashimasu.) — Biết anh/chị đang bận, kính mong anh/chị phản hồi giúp.

**Trả lời 30 giây:** “Em phân loại câu hỏi theo mức chặn, viết lại thành dạng có phương án để khách chỉ cần chọn, rồi gửi kèm hạn trả lời và tác động 納期. Nguyên tắc: làm cho khách dễ trả lời trước, đo QA回答日数 để có dữ liệu, chỉ escalate khi đã nhắc có hạn mà vẫn quá.”

**Tài liệu dùng:** QA (Q&A List), SR (Status Report), RR (Risk Register)  
**Chỉ số theo dõi:** QART (Q&A Response Time), IAGE (Issue Aging), SLIP (Schedule Slip (days))

</details>

<a id="s24"></a>

### S24 · Khách dọa chuyển vendor sau chuỗi trễ hạn

_Mức: Khó_

**Bối cảnh:** Khách bảo hiểm B, ラボ型 (lab – team riêng) 20 người, hợp tác 3 năm, chiếm 30% doanh thu đơn vị. Ba sprint liên tiếp giao trễ (say/do 60%), 部長 phía khách email cho giám đốc công ty mình: 'đang xem xét chuyển sang vendor khác từ kỳ hợp đồng tháng 10'. Còn 4 tháng đến kỳ gia hạn.

**Câu hỏi:** Với vai trò PM, việc đầu tiên anh/chị làm là gì?

- **A.** Đề xuất giảm giá 10% kỳ tới để giữ khách trước khi họ bắt đầu tìm vendor khác.
- **B.** Bổ sung ngay 5 người giỏi từ dự án khác để tăng tốc giao hàng 2 sprint tới.
- **C.** Xin gặp 部長 trong tuần để nghe trực tiếp mức độ bất mãn, rồi trình kế hoạch cải thiện có KPI.
- **D.** Phân tích kỹ 3 sprint trễ trong 2 tuần để có báo cáo hoàn chỉnh rồi mới gặp khách.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Giảm giá trả lời câu hỏi khách chưa hỏi, mất biên lợi nhuận và ngầm nhận yếu kém mà không sửa được việc giao hàng.
- **B** ✗ Thêm 5 người giữa chừng làm team cũ mất thời gian kèm, giao hàng có thể trễ hơn (luật Brooks), lại chưa biết gốc vấn đề.
- **C** ✅ Email dọa đổi vendor là tín hiệu mất niềm tin, không chỉ là trễ hạn; nghe trực tiếp để biết khách thật sự cần gì, rồi trả lời bằng kế hoạch có KPI đo được thay vì giảm giá hay thêm người.
- **D** ✗ Phân tích là cần nhưng im lặng 2 tuần sau email dọa đổi vendor bị hiểu là thờ ơ; phải gặp sớm và phân tích song song.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 ngày: phân tích nhanh 3 sprint (say/do, nguyên nhân trễ: ước lượng, đổi yêu cầu, chất lượng); xin lịch gặp 部長 để nghe vấn đề thật là trễ hạn, chất lượng hay giao tiếp.  
② Hành động ngay: Lập kế hoạch cải thiện 90 ngày: cam kết ít hơn nhưng giao đúng (say/do ≥ 90% – tham khảo), sửa cách ước lượng, thay vị trí yếu nếu có; thống nhất nội bộ về nguồn lực trước khi trình.  
③ Báo khách theo 報連相: Gặp 部長 trong tuần cùng giám đốc phía mình: nhận trách nhiệm, trình kế hoạch + KPI, báo cáo 2 tuần/lần; gửi 議事録 sau buổi gặp và báo cáo tiến độ cải thiện đều đặn đến kỳ gia hạn.  
④ Gốc rễ & phòng ngừa: Gốc rễ thường là không cảnh báo sớm khi say/do giảm; đặt ngưỡng cảnh báo (vd 2 sprint liền dưới 80%) để chủ động báo khách trước khi khách lên tiếng, khảo sát CSAT theo quý, 横展開 cho các team lab khác.  

**Đừng làm:**

- Giảm giá ngay — giữ được khách ngắn hạn nhưng vấn đề giao hàng vẫn nguyên.
- Im lặng nhiều tuần để chuẩn bị báo cáo hoàn hảo trong khi khách đang tìm vendor mới.

**Câu tiếng Nhật:** 直接お話を伺うお時間をいただけないでしょうか。 (Chokusetsu o-hanashi o ukagau o-jikan o itadakenai deshō ka.) — Anh/chị có thể dành thời gian để bên em được nghe trực tiếp không ạ?

**Trả lời 30 giây:** “Em xin gặp 部長 trong tuần cùng giám đốc phía mình để nghe trực tiếp, sau đó trình kế hoạch cải thiện 90 ngày có KPI say/do và báo cáo định kỳ đến kỳ gia hạn. Nguyên tắc: khủng hoảng niềm tin phải xử lý bằng gặp mặt và cam kết đo được, không bằng giảm giá hay thêm người.”

**Tài liệu dùng:** MoM (Minutes of Meeting), SR (Status Report), RR (Risk Register)  
**Chỉ số theo dõi:** SDR (Say/Do Ratio), CSAT (Customer Satisfaction), VEL (Velocity)

</details>

<a id="s25"></a>

### S25 · Khách muốn họp thẳng với dev, bỏ BrSE

_Mức: Trung cấp_

**Bối cảnh:** Khách sản xuất C, hợp đồng 準委任 (giao khoán theo công sức), team 9 người có 1 BrSE. Sau 2 lần hiểu sai yêu cầu qua BrSE, 担当者 khách đề nghị từ tuần sau họp hằng ngày bằng tiếng Anh trực tiếp với 3 dev, không qua BrSE. Tiếng Anh của dev ở mức đọc hiểu; BrSE đang ôm 4 cuộc họp mỗi ngày.

**Câu hỏi:** Anh/chị trả lời đề nghị của khách thế nào?

- **A.** Đồng ý ngay theo yêu cầu vì khách là người trả tiền và muốn trao đổi nhanh hơn.
- **B.** Tìm hiểu vì sao hiểu sai 2 lần, đề xuất họp kỹ thuật có dev tham gia, BrSE điều phối, thử 2 tuần.
- **C.** Từ chối lịch sự vì theo 体制 đã thống nhất trong hợp đồng, mọi trao đổi yêu cầu phải qua BrSE.
- **D.** Thay BrSE hiện tại bằng một BrSE kinh nghiệm hơn ngay tuần tới để khách sớm lấy lại tin tưởng.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Đồng ý ngay khi dev chưa đủ tiếng Anh và không ai ghi 議事録 dễ sinh thêm hiểu sai và yêu cầu ngoài phạm vi không qua CR.
- **B** ✅ Khách thật ra cần ít hiểu sai hơn chứ không cần bỏ BrSE; tìm gốc rồi đề xuất mô hình có dev tham gia trực tiếp nhưng vẫn có người giữ yêu cầu và 議事録, thử có thời hạn và tiêu chí.
- **C** ✗ Viện dẫn 体制 để từ chối đúng hình thức nhưng bỏ qua vấn đề thật, khách sẽ thấy vendor cứng nhắc.
- **D** ✗ Thay BrSE khi chưa biết lỗi do người, do tài liệu hay do quá tải; BrSE mới ôm 4 họp/ngày cũng sẽ gặp lại vấn đề cũ.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 ngày: xem lại 2 lần hiểu sai (do dịch, tài liệu thiếu, hay BrSE quá tải), hỏi 担当者 điều họ thật sự cần (tốc độ hay độ chính xác), hỏi dev có sẵn sàng tham gia không.  
② Hành động ngay: Đề xuất mô hình thử 2 tuần: họp kỹ thuật 2–3 lần/tuần có dev demo trên màn hình, BrSE điều phối và chốt yêu cầu, 議事録 trong 24 giờ; giảm tải BrSE bằng cách để comtor lo họp nội bộ.  
③ Báo khách theo 報連相: Trả lời 担当者 trước tuần sau bằng email + gọi ngắn: cảm ơn góp ý, nhận phần lỗi hiểu sai, trình mô hình thử và tiêu chí đánh giá (số lần hiểu sai, thời gian chốt QA); review sau 2 tuần tại 定例会.  
④ Gốc rễ & phòng ngừa: Gốc rễ: BrSE quá tải và yêu cầu truyền miệng; chuẩn hóa mẫu xác nhận yêu cầu (ví dụ, màn hình, điều kiện), theo dõi tỉ lệ 手戻り do hiểu sai, cân đối tải BrSE trong 要員計画.  

**Đừng làm:**

- Để dev nhận yêu cầu trực tiếp không có 議事録, phạm vi phình ra mà không qua CR.
- Bảo vệ BrSE theo kiểu 'đúng quy trình' mà bỏ qua lý do khách khó chịu.

**Câu tiếng Nhật:** まずは二週間、試行という形でいかがでしょうか。 (Mazu wa ni-shūkan, shikō to iu katachi de ikaga deshō ka.) — Trước mắt, mình thử áp dụng trong hai tuần có được không ạ?

**Trả lời 30 giây:** “Em không đồng ý ngay cũng không từ chối, mà tìm vì sao 2 lần hiểu sai rồi đề xuất họp kỹ thuật có dev tham gia, BrSE điều phối và chốt 議事録, thử 2 tuần có tiêu chí đo. Nguyên tắc: giải quyết nỗi đau thật của khách nhưng vẫn giữ một đầu mối kiểm soát yêu cầu.”

**Tài liệu dùng:** CMP (Communication Plan), MoM (Minutes of Meeting), RP (Resource / Staffing Plan)  
**Chỉ số theo dõi:** RW (Rework Rate), CSAT (Customer Satisfaction), QART (Q&A Response Time)

</details>


## Team & con người

<a id="s26"></a>

### S26 · Tech lead xin nghỉ giữa 結合テスト

_Mức: Trung cấp_

**Bối cảnh:** Khách ngân hàng A, hợp đồng 請負, team 14 người đang ở 結合テスト (kiểm thử tích hợp), còn 10 tuần đến 納期. Tech lead nộp đơn nghỉ, ngày làm cuối sau 30 ngày; anh là người duy nhất hiểu module kết nối hệ thống core banking (bus factor = 1). Lý do nêu trong đơn: nhận offer lương cao hơn 30%.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Nói chuyện riêng với tech lead trong ngày để hiểu lý do thật và chốt kế hoạch bàn giao 30 ngày.
- **B.** Đề xuất công ty counter-offer tăng lương ngay để giữ tech lead đến hết dự án.
- **C.** Báo ngay khách là tech lead nghỉ và xin lùi 納期 2 tuần để có dự phòng.
- **D.** Giao ngay 2 dev senior tự đọc code module core banking để nắm trong 30 ngày.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Cuộc nói chuyện cho biết lý do thật (có giữ được không) và quyết định chất lượng bàn giao; 30 ngày chỉ đủ nếu kế hoạch bắt đầu ngay và tech lead hợp tác.
- **B** ✗ Counter-offer khi chưa biết lý do thật thường chỉ giữ được ngắn hạn và tạo tiền lệ; dù thế nào vẫn cần kế hoạch bàn giao.
- **C** ✗ Báo khách và xin lùi 納期 khi chưa có kế hoạch, chưa đánh giá ảnh hưởng — báo cáo thiếu fact và làm khách hoảng.
- **D** ✗ Tự đọc code không có tech lead hướng dẫn rất chậm với module core banking, lại bỏ phí 30 ngày tech lead còn ở đây.

**Đáp án mẫu:**

① Xác nhận fact: Trong ngày: gặp riêng tech lead hỏi lý do và khả năng ở lại (nếu vì lương, hỏi HR trong 2 ngày có điều chỉnh được không); liệt kê kiến thức chỉ anh nắm: module core banking, môi trường, issue đang dở.  
② Hành động ngay: Kế hoạch bàn giao 30 ngày: chọn 1–2 người kế nhiệm, pair programming hằng ngày, viết tài liệu thiết kế và vận hành module, bàn giao issue 結合テスト; trước ngày cuối kiểm tra người kế nhiệm tự xử lý được lỗi thật.  
③ Báo khách theo 報連相: Báo khách tại 定例会 gần nhất, trong vòng 1 tuần, khi đã có kế hoạch: thay đổi 体制, người kế nhiệm, kế hoạch bàn giao, đánh giá ảnh hưởng 納期 (nếu có); cập nhật 体制図 và リスク管理表.  
④ Gốc rễ & phòng ngừa: Gốc rễ: bus factor = 1 và không theo dõi rủi ro nghỉ việc; quy định mỗi module quan trọng có ≥ 2 người nắm, review code chéo, 1-on-1 định kỳ để phát hiện sớm, 横展開 đánh giá bus factor ở các dự án khác.  

**Đừng làm:**

- Counter-offer bằng tiền ngay mà không hiểu lý do — thường chỉ giữ được vài tháng.
- Giấu khách việc đổi tech lead đến khi chất lượng giảm mới lộ ra.

**Câu tiếng Nhật:** 体制変更について、ご報告とご相談がございます。 (Taisei henkō ni tsuite, go-hōkoku to go-sōdan ga gozaimasu.) — Bên em có việc cần báo cáo và xin ý kiến về thay đổi nhân sự dự án.

**Trả lời 30 giây:** “Em nói chuyện riêng với tech lead ngay trong ngày để biết lý do thật và chốt kế hoạch bàn giao 30 ngày có người kế nhiệm, pair hằng ngày, kiểm tra năng lực trước ngày cuối. Sau đó mới báo khách thay đổi 体制 kèm kế hoạch; nguyên tắc là module quan trọng phải có bus factor ≥ 2.”

**Tài liệu dùng:** OBS (Organizational Breakdown Structure), RR (Risk Register), RP (Resource / Staffing Plan)  
**Chỉ số theo dõi:** BUS (Bus Factor), ATR (Attrition Rate), TTP (Time to Productivity)

</details>

<a id="s27"></a>

### S27 · BrSE nghỉ đột ngột, chỉ còn 3 ngày

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B, hợp đồng 準委任, team 10 người chỉ có 1 BrSE (kỹ sư cầu nối). Thứ Hai, BrSE báo nghỉ việc vì lý do cá nhân, chỉ còn làm 3 ngày; thứ Năm có 定例会 và 7 câu hỏi trong QA管理表 đang chờ khách. Team có 1 comtor (phiên dịch) N2; công ty cần khoảng 3–4 tuần để điều hoặc tuyển BrSE khác (tham khảo).

**Câu hỏi:** Trong 3 ngày còn lại của BrSE, anh/chị ưu tiên làm gì đầu tiên?

- **A.** Tập trung thuyết phục BrSE ở lại thêm 1 tháng vì hiện không ai thay thế được.
- **B.** Giao comtor thay BrSE chủ trì 定例会 và trả lời khách từ thứ Năm.
- **C.** Chưa báo khách để tránh lo lắng, chờ có BrSE mới rồi giới thiệu luôn một lần.
- **D.** Liệt kê việc BrSE đang giữ, bàn giao theo ưu tiên trong 3 ngày, báo khách 体制 tạm trước 定例会.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Có thể thử song song, nhưng nếu thất bại thì đã mất 3 ngày quý giá; bàn giao phải làm bất kể kết quả thuyết phục.
- **B** ✗ Comtor giỏi tiếng nhưng không nắm kỹ thuật và nghiệp vụ; đứng thay BrSE mà không có người hỗ trợ dễ hiểu sai yêu cầu.
- **C** ✗ Khách sẽ nhận ra ngay ở 定例会; giấu thay đổi 体制 vi phạm 報連相 và làm mất niềm tin.
- **D** ✅ 3 ngày là tài nguyên khan hiếm nhất: rút kiến thức ra tài liệu theo ưu tiên, dựng 体制 tạm và báo khách khi BrSE còn có mặt để chuyển giao quan hệ.

**Đáp án mẫu:**

① Xác nhận fact: Ngày 1: ngồi với BrSE liệt kê mọi thứ đang giữ: QA đang chờ, thỏa thuận chưa ghi, tài liệu đang dịch, quan hệ với từng người phía khách, tài khoản và công cụ; xếp ưu tiên theo hạn.  
② Hành động ngay: Ngày 1–3: bàn giao có ghi lại (record buổi bàn giao, cập nhật QA管理表, 議事録); phân vai tạm: PM chủ trì 定例会, comtor dịch, 1 dev senior trả lời kỹ thuật; đề nghị công ty điều BrSE thay thế, mục tiêu 3–4 tuần.  
③ Báo khách theo 報連相: Trước 定例会 thứ Năm, PM email cho 窓口 (BrSE còn có mặt để giới thiệu): thay đổi 体制, cách làm việc tạm thời, ngày dự kiến có BrSE mới; đề nghị tạm xác nhận mọi yêu cầu bằng văn bản để giảm hiểu sai.  
④ Gốc rễ & phòng ngừa: Gốc rễ: chỉ 1 BrSE nên bus factor giao tiếp = 1; đưa vào 要員計画 người dự phòng (dev biết tiếng Nhật hoặc BrSE dùng chung), mọi QA và quyết định nằm trong QA管理表/議事録 thay vì hộp thư cá nhân, 横展開 cho các dự án 1 BrSE.  

**Đừng làm:**

- Giấu khách việc BrSE nghỉ — khách sẽ nhận ra ngay ở 定例会.
- Đẩy comtor đứng thay BrSE mà không có người kỹ thuật hỗ trợ.

**Câu tiếng Nhật:** 体制変更に伴い、当面の対応体制をご報告いたします。 (Taisei henkō ni tomonai, tōmen no taiō taisei o go-hōkoku itashimasu.) — Do thay đổi nhân sự, bên em xin báo cáo cơ cấu xử lý tạm thời.

**Trả lời 30 giây:** “Em dùng 3 ngày còn lại để bàn giao theo ưu tiên: QA đang chờ, thỏa thuận chưa ghi, quan hệ với từng người phía khách, rồi báo khách 体制 tạm thời trước 定例会 khi BrSE còn có mặt. Nguyên tắc: minh bạch với khách sớm, kiến thức phải vào tài liệu chung, và vai trò giao tiếp không được để bus factor = 1.”

**Tài liệu dùng:** OBS (Organizational Breakdown Structure), QA (Q&A List), RP (Resource / Staffing Plan)  
**Chỉ số theo dõi:** BUS (Bus Factor), QART (Q&A Response Time), ATR (Attrition Rate)

</details>

<a id="s28"></a>

### S28 · Ramp-up gấp từ 5 lên 20 người

_Mức: Khó_

**Bối cảnh:** Khách sản xuất C hài lòng với giai đoạn 1 (ラボ型 5 người) và muốn mở rộng lên 20 người trong 1 tháng cho 4 module mới, bắt đầu 製造 (lập trình) sau 6 tuần. Đơn vị chỉ có 6 người bench phù hợp; kiến thức nghiệp vụ phần lớn nằm trong đầu 5 người cũ. Sales đã hứa miệng với khách 'không vấn đề'.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Tuyển gấp 15 người qua agency để đủ 20 người trong 1 tháng như sales đã hứa.
- **B.** Từ chối mở rộng vì team chỉ hấp thụ được khoảng 3–4 người mới mỗi tháng.
- **C.** Đo năng lực onboarding thật, lập kế hoạch ramp-up theo đợt, thống nhất nội bộ rồi trình khách.
- **D.** Nhận đủ 20 người ngay, giao 5 người cũ làm mentor toàn thời gian, tạm dừng việc giai đoạn 1.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Đủ đầu người nhưng chất lượng tuyển gấp khó kiểm soát, và 5 người cũ không kèm nổi 15 người mới cùng lúc.
- **B** ✗ Từ chối thẳng làm mất cơ hội và quan hệ; nên đưa phương án thay thế có số liệu thay vì nói 'không'.
- **C** ✅ Giới hạn thật là khả năng hấp thụ người mới (mentor, tài liệu, môi trường), không phải số đầu người; kế hoạch theo đợt có số liệu giúp điều chỉnh lời hứa của sales trước khi khách lập kế hoạch dựa trên nó.
- **D** ✗ Nghe quyết đoán nhưng dừng giai đoạn 1 làm gián đoạn cam kết hiện có, và tỉ lệ 1 mentor : 3 người mới vẫn quá tải.

**Đáp án mẫu:**

① Xác nhận fact: Trong 3–5 ngày: xác định nhu cầu thật theo module và thời điểm (4 module có cần 20 người cùng lúc không), năng lực kèm của 5 người cũ, kỹ năng 6 người bench, thời gian tuyển thêm (tham khảo 4–8 tuần).  
② Hành động ngay: Thiết kế ramp-up 3 đợt (vd 5→10→15→20 trong 8–10 tuần), mỗi đợt có onboarding kit (tài liệu nghiệp vụ, môi trường, bài tập), chia team theo module có sub-lead, giữ 2–3 người cũ cho giai đoạn 1; thống nhất với sales, HR, quản lý đơn vị trước.  
③ Báo khách theo 報連相: Trình khách trong 1 tuần: kế hoạch theo đợt, rủi ro nếu ép 20 người trong 1 tháng (chất lượng, 手戻り), mốc 製造 khả thi, KPI theo dõi; chốt bằng SOW mới và 体制図.  
④ Gốc rễ & phòng ngừa: Gốc rễ: sales cam kết không hỏi delivery; đề xuất quy trình PM review bắt buộc trước khi hứa quy mô, theo dõi thời gian đạt năng suất và バグ密度 từng đợt để điều chỉnh tốc độ, 横展開 bộ onboarding cho dự án khác.  

**Đừng làm:**

- Chạy theo con số 20 người — năng suất có thể giảm vì người cũ mất thời gian kèm.
- Coi lời hứa miệng của sales là cam kết mà không trình lại khách kế hoạch thực tế.

**Câu tiếng Nhật:** 段階的な増員計画をご提案させてください。 (Dankaiteki na zōin keikaku o go-teian sasete kudasai.) — Cho phép bên em đề xuất kế hoạch tăng nhân sự theo từng giai đoạn.

**Trả lời 30 giây:** “Em không chạy theo con số 20 người mà đo năng lực onboarding thật: mentor, tài liệu, người bench, thời gian tuyển, rồi lập kế hoạch ramp-up theo đợt, thống nhất nội bộ và trình khách trong 1 tuần. Nguyên tắc: hứa theo năng lực hấp thụ, có KPI thời gian đạt năng suất và chất lượng để điều chỉnh từng đợt.”

**Tài liệu dùng:** RP (Resource / Staffing Plan), OBS (Organizational Breakdown Structure), SOW (Statement of Work)  
**Chỉ số theo dõi:** TTP (Time to Productivity), PROD (Productivity), BD (Bug Density)

</details>

<a id="s29"></a>

### S29 · Member giỏi nhất nhưng toxic với team

_Mức: Khó_

**Bối cảnh:** Khách ngân hàng A, hợp đồng 準委任, team 12 người. Senior dev giỏi nhất (xử lý khoảng 40% bug khó) thường xuyên chê bai code người khác trên kênh chat chung; 2 junior đã xin chuyển dự án trong tháng này. Khách đánh giá rất cao anh này và từng khen tên anh trong 定例会.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Tạm bỏ qua vì đóng góp kỹ thuật quá lớn, tập trung động viên 2 junior ở lại.
- **B.** Thu thập ví dụ cụ thể, gặp riêng nói rõ hành vi, tác động và kỳ vọng, có thời hạn theo dõi.
- **C.** Nhắc nhở công khai trong họp team để mọi người thấy PM không thiên vị ai.
- **D.** Đề xuất chuyển anh này sang dự án khác ngay để giữ không khí làm việc của team.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Dung túng hành vi tiêu cực vì năng lực khiến team mất thêm người, cuối cùng chi phí lớn hơn đóng góp của một người.
- **B** ✅ Vấn đề là hành vi chứ không phải con người; feedback riêng dựa trên ví dụ cụ thể (SBI), cho cơ hội sửa trong thời hạn rõ, đồng thời giữ được năng lực kỹ thuật cho team.
- **C** ✗ Phê bình công khai làm người giỏi mất mặt, dễ phản kháng hoặc nghỉ, không sửa được hành vi.
- **D** ✗ Chuyển đi ngay khi chưa cho cơ hội sửa làm mất 40% năng lực xử lý bug khó, và khách có thể phản ứng vì họ đánh giá cao anh này.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 ngày: thu thập ví dụ cụ thể (tin nhắn, review comment), nói chuyện riêng với 2 junior về lý do muốn chuyển, hỏi thêm vài người trong team có cùng cảm nhận không.  
② Hành động ngay: Gặp 1-on-1 theo SBI (tình huống – hành vi – tác động): ghi nhận đóng góp, nói rõ hành vi không chấp nhận, kỳ vọng cụ thể (góp ý trong review riêng, kèm đề xuất sửa), theo dõi 4–6 tuần (tham khảo); giao vai trò mentor có chuẩn mực để biến năng lực thành tài sản team.  
③ Báo khách theo 報連相: Không đưa chuyện nội bộ lên khách; báo quản lý trực tiếp/HR để có hồ sơ; nếu hết thời hạn không cải thiện và phải đổi người, báo khách thay đổi 体制 kèm kế hoạch bàn giao trước ít nhất 1 tháng.  
④ Gốc rễ & phòng ngừa: Gốc rễ: chưa có chuẩn hành vi chung và phụ thuộc 1 người cho bug khó; lập team agreement về cách review code, pair để giảm bus factor, theo dõi tỉ lệ nghỉ việc và khảo sát team định kỳ, 横展開 chuẩn review cho các dự án.  

**Đừng làm:**

- Dung túng vì 'người giỏi khó thay' — team sẽ dần mất những người tốt khác.
- Phê bình công khai hoặc chuyển người đột ngột mà không cho cơ hội sửa.

**Câu tiếng Nhật:** 後任への引き継ぎ計画を添えてご報告いたします。 (Kōnin e no hikitsugi keikaku o soete go-hōkoku itashimasu.) — Bên em xin báo cáo kèm kế hoạch bàn giao cho người kế nhiệm.

**Trả lời 30 giây:** “Em gặp riêng anh ấy với ví dụ cụ thể theo SBI, ghi nhận đóng góp nhưng nói rõ hành vi không chấp nhận và kỳ vọng có thời hạn theo dõi, đồng thời giao vai trò mentor có chuẩn mực. Nguyên tắc: tách hành vi khỏi năng lực, không dung túng vì team sẽ mất người tốt, và không đưa chuyện nội bộ ra khách.”

**Tài liệu dùng:** RP (Resource / Staffing Plan), RR (Risk Register), LL (Lessons Learned)  
**Chỉ số theo dõi:** ATR (Attrition Rate), BUS (Bus Factor), PROD (Productivity)

</details>

<a id="s30"></a>

### S30 · Team OT kéo dài, dấu hiệu burnout

_Mức: Trung cấp_

**Bối cảnh:** Khách tài chính D, hợp đồng 請負, team 11 người ở 総合テスト (kiểm thử tổng thể), còn 5 tuần đến 納期. OT trung bình 55 giờ/tháng suốt 3 tháng, 2 người nghỉ ốm tuần này, tỉ lệ bug phát sinh khi sửa bug tăng từ 5% lên 15%. Team lead đề xuất làm thêm thứ Bảy đến hết dự án.

**Câu hỏi:** Anh/chị quyết định thế nào?

- **A.** Dừng tăng OT, đo lại khối lượng còn và năng suất thật, trình khách phương án phạm vi/納期 theo số liệu.
- **B.** Đồng ý làm thứ Bảy nhưng tăng phụ cấp OT để giữ động lực trong 5 tuần cuối.
- **C.** Bổ sung 4 người mới vào team ngay tuần tới để chia bớt tải test và sửa bug.
- **D.** Giữ nguyên kế hoạch, hứa cho cả team nghỉ bù sau khi giao hàng vì chỉ còn 5 tuần.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ OT kéo dài cùng bug do sửa bug tăng gấp 3 là dấu hiệu kế hoạch không còn khả thi; có số liệu rồi để khách chọn giữa phạm vi và 納期 là cách bảo vệ cả chất lượng lẫn con người.
- **B** ✗ Phụ cấp không chữa được kiệt sức; thêm thứ Bảy làm năng suất và chất lượng giảm tiếp, kèm rủi ro vượt giới hạn làm thêm theo luật lao động.
- **C** ✗ Thêm người mới ở 総合テスト làm team cũ tốn thời gian kèm, hiệu quả thường đến khi dự án đã gần kết thúc.
- **D** ✗ Bỏ qua tín hiệu rõ ràng (người ốm, bug tăng); thêm 5 tuần ở tốc độ này có thể mất người và chất lượng giao hàng.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 ngày: tính khối lượng còn lại (test case chưa chạy, bug mở theo mức độ), năng suất thật 2 tuần gần nhất, xu hướng bug do sửa bug; 1-on-1 ngắn với những người OT nhiều nhất.  
② Hành động ngay: Giới hạn OT ngay theo quy định công ty và luật lao động (vd ≤ 30 giờ/tháng – tham khảo), cho 2 người ốm nghỉ đủ, test theo rủi ro (chức năng quan trọng trước), dời việc không thiết yếu; chỉ thêm 1–2 người đã quen hệ thống cho việc độc lập như chạy test.  
③ Báo khách theo 報連相: Trước 定例会 tuần này: trình khách số liệu (khối lượng còn, năng suất, chất lượng đang giảm) và 2 phương án: giữ 納期 với phạm vi giảm hoặc phát hành theo đợt, hoặc lùi 納期 X tuần với đủ phạm vi; chốt bằng 議事録.  
④ Gốc rễ & phòng ngừa: Gốc rễ: ước lượng thấp và không cảnh báo sớm khi OT vượt ngưỡng; đưa ngưỡng cảnh báo OT vào 進捗報告書 (vd 2 tháng liền > 45 giờ – tham khảo), có buffer test trong kế hoạch, 横展開 theo dõi OT toàn đơn vị.  

**Đừng làm:**

- Dùng OT để che giấu trễ hạn với khách — chất lượng giảm và rủi ro lao động tăng.
- Thêm người mới ở giai đoạn cuối khiến team cũ mất thêm thời gian kèm.

**Câu tiếng Nhật:** 現状を踏まえ、スケジュールについてご相談させてください。 (Genjō o fumae, sukejūru ni tsuite go-sōdan sasete kudasai.) — Dựa trên tình hình hiện tại, cho phép bên em được bàn về lịch trình.

**Trả lời 30 giây:** “Em dừng tăng OT, đo lại khối lượng còn lại và năng suất thật, rồi trình khách phương án giảm phạm vi hoặc lùi 納期 dựa trên số liệu trước 定例会. Nguyên tắc: OT kéo dài là tín hiệu kế hoạch sai chứ không phải giải pháp; che giấu bằng OT làm chất lượng giảm và mất người.”

**Tài liệu dùng:** SR (Status Report), GNT (Gantt Chart / Schedule), RR (Risk Register)  
**Chỉ số theo dõi:** OT (Overtime Hours), RW (Rework Rate), BCV (Bug Convergence)

</details>


## Chi phí & hợp đồng

<a id="s31"></a>

### S31 · 請負 vượt effort 30%, CPI 0,77

_Mức: Trung cấp_

**Bối cảnh:** Dự án 請負 (ukeoi – hợp đồng khoán, giá cố định) cho khách bảo hiểm B, BAC 1.200 人日 (man-day), team 15 người, đang ở 結合テスト (kiểm thử tích hợp) tuần 3/6. Báo cáo 予実 (kế hoạch – thực tế) cuối tháng: EV 720 人日, AC 940 人日 → CPI ≈ 0,77, effort vượt khoảng 30%. SPI vẫn 0,95 vì team OT nhiều, 納期 (hạn giao) còn 7 tuần. Phòng tài chính cảnh báo 粗利 (lãi gộp) dự án có thể âm.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Đề nghị khách bổ sung phí ngay vì effort thực tế vượt estimate 30%, có số liệu 予実 làm căn cứ.
- **B.** Điều thêm 3 người từ bench vào 結合テスト để giữ 納期, chi phí xử lý sau khi bàn giao.
- **C.** Phân tích phần vượt theo nguyên nhân: thay đổi yêu cầu ngầm, rework, estimate sai, năng suất; rồi tính EAC.
- **D.** Rút bớt test case và vòng review còn lại để effort phần còn lại khớp ngân sách ban đầu.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ 請負 là giá cố định; chưa tách được phần do khách đổi yêu cầu thì không có căn cứ đòi phí, dễ mất uy tín và vị thế đàm phán.
- **B** ✗ Thêm người khi chưa biết gốc rễ làm CPI tệ hơn, người mới cần thời gian làm quen giữa 結合テスト nên khó kéo được tiến độ.
- **C** ✅ Phải biết 30% vượt đến từ đâu: phần do khách thay đổi (làm CR được) và phần do nội bộ (rework, estimate sai) — cùng EAC thật — thì mới có lập trường đúng với khách và cấp trên.
- **D** ✗ Cắt test âm thầm để giữ chi phí là đẩy rủi ro sang 本番 (production); với 請負 công ty còn chịu 契約不適合責任 (trách nhiệm bảo hành) nên cuối cùng tốn hơn.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày, PM cùng leader lấy timesheet theo WBS, so 予実 từng hạng mục và gắn nhãn phần vượt: (a) thay đổi không qua CR, (b) rework/bug, (c) estimate sai, (d) năng suất; tính EAC = BAC/CPI và ETC còn lại.  
② Hành động ngay: Dừng OT kéo dài không kiểm soát, ưu tiên đóng bug chặn 結合テスト; gom các thay đổi phát sinh có bằng chứng (議事録, QA管理表) để chuẩn bị 変更要求書.  
③ Báo khách theo 報連相: Trong tuần, báo sếp và sales trước: EAC, GM dự kiến, phương án; sau đó ở 定例会 với khách chỉ đưa phần thay đổi phạm vi có bằng chứng dưới dạng 変更要求書 kèm estimate, không than effort nội bộ.  
④ Gốc rễ & phòng ngừa: Ghi bài học: estimate thiếu buffer cho 結合テスト; quy tắc mọi QA làm đổi yêu cầu phải đánh giá impact effort trong 2 ngày; theo dõi CPI hằng tuần, cảnh báo khi < 0,9 (tham khảo).  

**Đừng làm:**

- Đòi khách trả cho toàn bộ phần vượt, kể cả phần do lỗi nội bộ.
- Giấu CPI với cấp trên đến khi kết thúc dự án mới lộ lỗ.

**Câu tiếng Nhật:** 仕様変更分の追加見積をご相談させてください。 (Shiyō henkō-bun no tsuika mitsumori o go-sōdan sasete kudasai.) — Cho phép chúng tôi trao đổi về báo giá bổ sung cho phần thay đổi đặc tả.

**Trả lời 30 giây:** “Em không đòi phí hay thêm người ngay mà tách 30% vượt thành phần do khách đổi yêu cầu và phần do nội bộ, rồi tính EAC. Phần thay đổi có bằng chứng thì làm 変更要求書 với khách, phần nội bộ thì báo sếp kèm phương án giữ GM. Nguyên tắc của em: số liệu trước, đàm phán sau, và không cắt chất lượng để che lỗ.”

**Tài liệu dùng:** EVM (EVM / Budget vs Actual Report), CR (Change Request), EST (Estimate / Quotation)  
**Chỉ số theo dõi:** CPI (Cost Performance Index), EAC (Estimate at Completion), EFV (Effort Variance)

</details>

<a id="s32"></a>

### S32 · Sếp ép nhận dự án dưới giá vốn

_Mức: Khó_

**Bối cảnh:** Khách sản xuất C (khách mới) mời báo giá dự án 請負 thay hệ thống quản lý kho, 8 tháng. Estimate của anh/chị là 90 人月 (person-month); ngân sách khách chỉ tương đương 60 人月, nhận full scope ở giá đó thì dự án lỗ. Giám đốc chi nhánh muốn nhận để 'vào cửa' khách mới và yêu cầu anh/chị sửa estimate xuống 60 人月 trước buổi 提案 (thuyết trình đề xuất) thứ Hai.

**Câu hỏi:** Anh/chị phản hồi sếp thế nào?

- **A.** Sửa estimate xuống 60 人月 như sếp yêu cầu, sau khi trúng thầu sẽ dùng CR để bù phần thiếu.
- **B.** Trình sếp 2–3 phương án có số: giảm scope, chia giai đoạn, hoặc nhận lỗ có kiểm soát qua 稟議.
- **C.** Từ chối sửa estimate vì dưới giá vốn, đề nghị sếp không nộp báo giá cho khách này.
- **D.** Đồng ý 60 人月 nhưng xếp team chủ yếu là junior để hạ chi phí thực tế xuống mức hòa vốn.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Hạ con số không làm effort thật giảm đi; trông vào CR để bù là đặt cược vào điều khách chưa đồng ý, dễ thành tranh chấp giữa dự án.
- **B** ✅ Nhận lỗ để vào cửa là quyết định kinh doanh của cấp trên, nhưng PM phải đưa đủ số (GM, rủi ro, phương án scope/phase) để sếp quyết có thông tin và chịu trách nhiệm qua 稟議 (phiếu phê duyệt).
- **C** ✗ Bỏ qua mục tiêu chiến lược hợp lý của sếp; PM không nên khép cửa khi còn phương án như giảm scope hay chia phase.
- **D** ✗ Dồn junior để ép giá là rủi ro chất lượng ẩn với khách mới, và estimate gửi khách vẫn không trung thực.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày, rà lại estimate: tách phần chắc chắn và buffer rủi ro, tìm hạng mục có thể cắt hoặc đẩy sang phase 2; tính giá vốn và GM ở các mức 60/75/90 人月.  
② Hành động ngay: Dựng 3 phương án: (1) 60 人月 với scope rút gọn, ghi rõ 前提条件 (điều kiện tiền đề) và 除外事項 (hạng mục loại trừ); (2) chia phase, phase 1 = 60 人月; (3) full scope 60 人月 = lỗ bao nhiêu, cần 稟議 và chiến lược thu hồi.  
③ Báo khách theo 報連相: Gặp sếp trước thứ Sáu, trình bảng so sánh; nếu sếp chọn nhận lỗ, đề nghị ghi vào 稟議 và đưa 前提条件 vào 提案書 để khoanh scope với khách.  
④ Gốc rễ & phòng ngừa: Đề xuất quy định: báo giá dưới giá vốn phải có 稟議 và kế hoạch thu hồi; theo dõi GM thực tế so với kế hoạch từ tháng đầu dự án.  

**Đừng làm:**

- Hạ estimate nhưng giữ nguyên scope và không ghi điều kiện tiền đề.
- Cãi với sếp bằng cảm xúc thay vì bằng bảng số.

**Câu tiếng Nhật:** 前提条件を明記した上で再度お見積りいたします。 (Zentei jōken o meiki shita ue de saido o-mitsumori itashimasu.) — Chúng tôi sẽ báo giá lại sau khi ghi rõ các điều kiện tiền đề.

**Trả lời 30 giây:** “Em không tự hạ estimate cũng không từ chối thẳng, mà đưa sếp 3 phương án có số: giảm scope, chia phase, hoặc nhận lỗ có kiểm soát. Quyết định nhận lỗ là của cấp trên qua 稟議, việc của PM là làm rõ cái giá và khoanh scope bằng 前提条件. Nguyên tắc: estimate phải trung thực, còn giá bán là quyết định kinh doanh.”

**Tài liệu dùng:** EST (Estimate / Quotation), PRP (Proposal), BC (Business Case)  
**Chỉ số theo dõi:** GM (Gross Margin), EA (Estimate Accuracy)

</details>

<a id="s33"></a>

### S33 · Khách muốn đổi 準委任 sang 請負 giữa chừng

_Mức: Khó_

**Bối cảnh:** Dự án cho khách ngân hàng A chạy 準委任 (jun-inin – hợp đồng theo công sức, không cam kết kết quả) 6 tháng, team 10 người, đang ở 詳細設計 (thiết kế chi tiết) tháng thứ 3. Bộ phận mua hàng của khách muốn chuyển sang 請負 từ tháng 4, giá trần bằng tổng effort còn lại theo kế hoạch hiện tại. QA管理表 vẫn còn 25 câu hỏi về yêu cầu chưa chốt.

**Câu hỏi:** Anh/chị xử lý đề nghị này thế nào?

- **A.** Đồng ý ngay để giữ quan hệ, vì effort còn lại đã nằm sẵn trong kế hoạch được khách duyệt.
- **B.** Từ chối, giải thích rằng với yêu cầu chưa ổn định, công ty chỉ nhận 準委任 cho dự án này.
- **C.** Đồng ý chuyển nhưng cộng thêm 30% buffer rủi ro vào giá trần để phòng scope phát sinh.
- **D.** Hỏi lý do của khách, rà scope còn mở, rồi đề xuất điều kiện chuyển: chốt yêu cầu trước, estimate lại.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Effort kế hoạch của 準委任 không có buffer cho trách nhiệm hoàn thành; 25 QA chưa chốt sẽ thành rủi ro scope mà công ty phải gánh trọn.
- **B** ✗ Khách thường có lý do chính đáng (ngân sách 年度末, kiểm soát chi phí); từ chối thẳng làm mất cơ hội và quan hệ.
- **C** ✗ Buffer 30% không có căn cứ sẽ bị bộ phận mua hàng bác, và vẫn chưa xử lý gốc là scope chưa chốt.
- **D** ✅ Hiểu động cơ của khách trước, rồi đặt điều kiện để 請負 khả thi (yêu cầu đóng, 前提条件, estimate lại, quy trình CR, tiêu chí 検収) — đó là chuyển hợp đồng có kiểm soát.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2–3 ngày: qua 窓口 (đầu mối) hỏi lý do (ngân sách, phê duyệt nội bộ, muốn 検収 theo kết quả?); phân loại 25 QA theo mức ảnh hưởng effort; xem EFV và năng suất 3 tháng qua.  
② Hành động ngay: Dựng lộ trình: giữ 準委任 đến khi 詳細設計 chốt và 25 QA đóng; chuyển 請負 từ 製造 (coding) với estimate mới, 前提条件, quy trình CR và tiêu chí 検収 (nghiệm thu) rõ ràng.  
③ Báo khách theo 報連相: Gửi khách đề xuất kèm bảng so sánh rủi ro trước 定例会 tuần sau; nội bộ xin ý kiến sales và pháp chế về điều khoản 契約不適合責任 trước khi ký.  
④ Gốc rễ & phòng ngừa: Ghi bài học: khi khởi đầu 準委任, thỏa thuận sẵn điểm có thể chuyển sang 請負 (sau 基本設計 hoặc 詳細設計); đưa vào checklist hợp đồng của PMO.  

**Đừng làm:**

- Ký 請負 khi scope còn mở mà không có điều kiện tiền đề và quy trình CR.
- Lấy effort kế hoạch của 準委任 làm giá 請負 mà không estimate lại.

**Câu tiếng Nhật:** 契約形態の変更について、条件をご相談させてください。 (Keiyaku keitai no henkō ni tsuite, jōken o go-sōdan sasete kudasai.) — Cho phép chúng tôi trao đổi về các điều kiện khi thay đổi hình thức hợp đồng.

**Trả lời 30 giây:** “Em không đồng ý hay từ chối ngay mà hỏi lý do khách muốn đổi, rồi đặt điều kiện để 請負 khả thi: chốt 25 QA còn mở, estimate lại theo scope đã chốt, có 前提条件 và quy trình CR. Với em, 請負 chỉ ký khi scope đã đóng; còn mở thì giữ 準委任.”

**Tài liệu dùng:** SOW (Statement of Work), EST (Estimate / Quotation), QA (Q&A List)  
**Chỉ số theo dõi:** EA (Estimate Accuracy), RV (Requirement Volatility), EFV (Effort Variance)

</details>

<a id="s34"></a>

### S34 · Khách ép giảm giá vì yên yếu

_Mức: Trung cấp_

**Bối cảnh:** Khách bảo hiểm B có hợp đồng ラボ型 (lab team dài hạn) với team 12 người, đơn giá tính bằng USD, gia hạn theo năm. Trước kỳ gia hạn tháng 4 (đầu 年度 – năm tài chính), 窓口 báo vì yên yếu nên chi phí quy ra yên của họ tăng mạnh, đề nghị giảm đơn giá 15%, nếu không sẽ cắt 3 người. GM hiện tại của dự án khoảng 28%.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Tính GM ở từng mức giảm và chuẩn bị 2–3 gói thay thế (đổi cơ cấu team, chia sẻ tỉ giá) trước khi đàm phán.
- **B.** Chấp nhận giảm 15% ngay để giữ đủ 12 người, thể hiện thiện chí đồng hành với khách.
- **C.** Giữ nguyên đơn giá và đồng ý giảm còn 9 người như khách đề nghị để bảo vệ GM.
- **D.** Từ chối giảm giá, giải thích theo hợp đồng thì rủi ro tỉ giá thuộc về phía khách.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Trước khi trả lời, PM cần biết mức sàn còn giữ GM mục tiêu và có gói thay thế để đàm phán theo giá trị thay vì chỉ có/không.
- **B** ✗ Giảm 15% kéo GM từ khoảng 28% xuống khoảng 15%; nhượng bộ hết ngay lần đầu làm mất vị thế và tạo tiền lệ cho các năm sau.
- **C** ✗ Cắt 3 người làm giảm năng lực, ảnh hưởng roadmap của khách và đẩy 3 người về bench; chưa hỏi khách ưu tiên gì.
- **D** ✗ Đúng về hợp đồng nhưng cứng nhắc; khách có thể không gia hạn hoặc chuyển vendor.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: tính GM ở các mức giảm 0/5/10/15%, chi phí bench nếu cắt 3 người; hỏi 窓口 ngân sách yên năm tới và ưu tiên backlog.  
② Hành động ngay: Dựng gói: (1) giảm 5–7% kèm cam kết năng suất; (2) giữ giá, đổi cơ cấu 1 senior thành junior có mentor; (3) điều khoản chia sẻ tỉ giá theo biên độ. Xin sếp/sales mức sàn GM trước khi gặp khách.  
③ Báo khách theo 報連相: Trước kỳ gia hạn ít nhất 4 tuần, gặp 窓口 và người quyết ngân sách; trình các gói kèm số liệu thành quả năm qua (velocity, bug 流出, CSAT) để đàm phán dựa trên giá trị.  
④ Gốc rễ & phòng ngừa: Đề xuất điều khoản điều chỉnh tỉ giá trong hợp đồng mới; theo dõi GM theo quý và chuẩn bị báo cáo giá trị hằng năm trước mùa lập 予算 của khách (tháng 1–2, tham khảo).  

**Đừng làm:**

- Nhượng bộ toàn bộ mức giảm ngay trong cuộc gọi đầu tiên.
- Đàm phán mà không biết trước mức sàn GM của công ty.

**Câu tiếng Nhật:** ご予算に合わせた体制案を複数ご提案いたします。 (Go-yosan ni awaseta taisei-an o fukusū go-teian itashimasu.) — Chúng tôi xin đề xuất một số phương án cơ cấu team phù hợp ngân sách của quý khách.

**Trả lời 30 giây:** “Em không gật hay lắc ngay mà tính GM ở từng mức giảm và chuẩn bị 2–3 gói thay thế như đổi cơ cấu team hoặc chia sẻ rủi ro tỉ giá. Khi đàm phán em dùng số liệu thành quả năm qua để khách thấy đang mua năng lực chứ không chỉ mua giờ công. Nguyên tắc: biết mức sàn trước, đàm phán bằng phương án chứ không bằng có/không.”

**Tài liệu dùng:** SOW (Statement of Work), EST (Estimate / Quotation), SR (Status Report)  
**Chỉ số theo dõi:** GM (Gross Margin), RPH (Revenue per Head), CSAT (Customer Satisfaction)

</details>

<a id="s35"></a>

### S35 · Estimate sai lộ ra ở 詳細設計

_Mức: Trung cấp_

**Bối cảnh:** Dự án 請負 cho khách sản xuất C, team 9 người, đang ở 詳細設計 tuần 2/4. Khi viết 詳細設計書, team phát hiện module 原価計算 (tính giá thành) có 40 quy tắc tính, trong khi estimate chỉ tính 12 quy tắc liệt kê trong 基本設計書; effort module dự kiến gấp 2,5 lần. 基本設計書 đã được khách duyệt, có câu 'chi tiết quy tắc xác định ở 詳細設計'.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Báo khách ngay rằng phạm vi tăng từ 12 lên 40 quy tắc và gửi CR cho 28 quy tắc mới.
- **B.** Cho team OT để làm đủ 40 quy tắc, giữ 納期 và không làm phiền khách khi BD đã duyệt.
- **C.** Đối chiếu 40 quy tắc với 基本設計書, 議事録 và 前提条件 của estimate để phân loại phần nào là scope mới.
- **D.** Đề xuất khách bỏ bớt các quy tắc ít dùng để effort module quay về mức trong estimate.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Chưa đối chiếu bằng chứng mà gọi là CR; nếu khách chỉ ra 基本設計 đã bao hàm thì mất uy tín và khó đàm phán phần thật sự mới.
- **B** ✗ OT che giấu đẩy cả effort lẫn rủi ro vào 製造/テスト, và tự gánh luôn phần có thể là scope mới của khách.
- **C** ✅ Phải biết bao nhiêu quy tắc đã nằm trong 基本設計 (lỗi estimate của mình) và bao nhiêu là mới (căn cứ CR) thì mới có lập trường đúng với cả khách và nội bộ.
- **D** ✗ Cắt quy tắc có thể làm sai nghiệp vụ tính giá thành của khách; chưa biết quy tắc nào ít dùng thì chưa đủ căn cứ đề xuất.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày, BrSE và BA lập bảng đối chiếu 40 quy tắc với 基本設計書, 議事録, QA管理表 và 前提条件 trong 見積書, chia 3 loại: có trong BD, suy ra được từ BD, mới hoàn toàn; estimate lại từng loại.  
② Hành động ngay: Phần đã chắc tiếp tục 詳細設計; tạm dừng thiết kế nhóm 'mới hoàn toàn' chờ thống nhất; cập nhật リスク管理表 với tác động lên 納期.  
③ Báo khách theo 報連相: Báo sếp trước; rồi trước 定例会 tuần này gửi khách bảng đối chiếu: phần nội bộ chịu (không tính phí, có kế hoạch giữ 納期) và phần mới đề xuất 変更要求書 kèm estimate, tác động lịch.  
④ Gốc rễ & phòng ngừa: Thêm bước đếm quy tắc/màn hình/IF thực tế trước khi chốt estimate và ghi số lượng vào 前提条件; đo EA sau mỗi giai đoạn để hiệu chỉnh hệ số estimate.  

**Đừng làm:**

- Gộp cả phần lỗi estimate của mình vào CR đòi khách trả.
- Im lặng xử lý nội bộ đến khi 製造 trễ mới báo.

**Câu tiếng Nhật:** 見積前提との差異について、ご報告とご相談がございます。 (Mitsumori zentei to no sai ni tsuite, go-hōkoku to go-sōdan ga gozaimasu.) — Chúng tôi có báo cáo và muốn trao đổi về chênh lệch so với điều kiện tiền đề của báo giá.

**Trả lời 30 giây:** “Em đối chiếu 40 quy tắc với 基本設計書 và 前提条件 của estimate trước khi nói với ai, để tách phần do mình estimate sai và phần thật sự là scope mới. Phần mình sai thì nội bộ chịu và có kế hoạch giữ 納期, phần mới thì làm CR có bằng chứng. Nguyên tắc: phân loại bằng chứng trước, đàm phán sau.”

**Tài liệu dùng:** DD (Detailed Design (Internal Design)), EST (Estimate / Quotation), CR (Change Request)  
**Chỉ số theo dõi:** EA (Estimate Accuracy), EFV (Effort Variance), SCR (Scope Creep)

</details>


## Rủi ro & bảo mật

<a id="s36"></a>

### S36 · Member dán code, dữ liệu khách vào ChatGPT

_Mức: Trung cấp_

**Bối cảnh:** Dự án cho khách ngân hàng A, team 14 người. Chiều thứ Tư, một tester báo anh/chị: một developer đã dán đoạn source code xử lý chuyển khoản và một file log có số tài khoản khách hàng thật vào ChatGPT bản cá nhân để nhờ debug. NDA với khách cấm đưa thông tin dự án lên dịch vụ bên ngoài chưa được phép.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Xác nhận ngay nội dung đã dán, số bản ghi, cài đặt tài khoản, rồi báo bộ phận bảo mật nội bộ trong ngày.
- **B.** Yêu cầu developer xóa ngay lịch sử chat và nhắc cả team không dùng AI ngoài với dữ liệu dự án.
- **C.** Báo khách ngay trong chiều nay rằng dữ liệu đã bị rò rỉ, để thể hiện tinh thần minh bạch.
- **D.** Kỷ luật developer và rút khỏi dự án ngay, để chứng minh với khách là công ty xử lý nghiêm.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Sự cố bảo mật cần fact chính xác (dữ liệu gì, bao nhiêu bản ghi, tài khoản có cho phép dùng dữ liệu để huấn luyện không) và phải đi qua kênh bảo mật nội bộ để quyết định cách báo khách theo hợp đồng.
- **B** ✗ Xóa lịch sử có thể mất bằng chứng cần cho điều tra, và chỉ nhắc nhở nội bộ là che giấu một vi phạm NDA.
- **C** ✗ Khách phải được báo, nhưng báo khi chưa biết phạm vi dễ sai mức độ; việc báo sự cố bảo mật cần bộ phận bảo mật cùng quyết định, trong thời hạn hợp đồng.
- **D** ✗ Đổ lỗi cá nhân không xử lý được rủi ro dữ liệu và không sửa gốc rễ quy trình; kỷ luật là việc sau khi điều tra.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1–2 giờ: phỏng vấn developer, chụp lại nội dung đã dán (không xóa), xác định số tài khoản/bản ghi, loại tài khoản và cài đặt dùng dữ liệu cho huấn luyện; khóa quyền truy cập file log gốc.  
② Hành động ngay: Báo bộ phận bảo mật/ISMS trong ngày theo quy trình インシデント (sự cố); theo hướng dẫn của họ gửi yêu cầu xóa dữ liệu tới nhà cung cấp nếu có kênh; tạm chặn dịch vụ AI chưa được duyệt trên máy dự án.  
③ Báo khách theo 報連相: Cùng bộ phận bảo mật báo 窓口 và người phụ trách bảo mật của khách trong thời hạn hợp đồng (thường trong 24 giờ – tham khảo): sự việc, phạm vi, biện pháp tạm thời, lịch gửi 事故報告書 chính thức.  
④ Gốc rễ & phòng ngừa: Gốc rễ: chưa có quy định và công cụ AI được duyệt, log test chứa dữ liệu thật. 再発防止: chính sách dùng AI, công cụ AI doanh nghiệp nếu khách cho phép, che dữ liệu (masking) trong log, đào tạo lại team; 横展開 sang các dự án khác.  

**Đừng làm:**

- Bảo developer xóa lịch sử chat cho 'xong chuyện' — vừa mất bằng chứng vừa che giấu.
- Chỉ xử lý cá nhân mà không sửa quy định và dữ liệu thật trong log.

**Câu tiếng Nhật:** 情報セキュリティ事故について、至急ご報告いたします。 (Jōhō sekyuriti jiko ni tsuite, shikyū go-hōkoku itashimasu.) — Chúng tôi xin khẩn cấp báo cáo về sự cố an toàn thông tin.

**Trả lời 30 giây:** “Em xác nhận fact trong 1–2 giờ: đã dán gì, bao nhiêu bản ghi thật, cài đặt tài khoản ra sao, giữ nguyên bằng chứng, rồi kích hoạt quy trình sự cố của bộ phận bảo mật. Báo khách cùng bộ phận bảo mật trong thời hạn hợp đồng, sau đó sửa gốc là quy định dùng AI và dữ liệu thật trong log. Nguyên tắc: không xóa, không giấu, không đổ lỗi cá nhân.”

**Tài liệu dùng:** IR (Incident Report), RR (Risk Register)  
**Chỉ số theo dõi:** INC (Incident Count), CLM (Complaints)

</details>

<a id="s37"></a>

### S37 · Mất laptop chứa source code dự án

_Mức: Cơ bản_

**Bối cảnh:** Tối thứ Sáu, một developer dự án khách bảo hiểm B báo mất laptop công ty trên taxi; máy chứa source code dự án và tài liệu 詳細設計. Quy định công ty yêu cầu mã hóa ổ đĩa và khóa màn hình, nhưng chưa ai xác minh máy này đã bật mã hóa chưa. Developer vẫn còn đăng nhập VPN và Git trên máy.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Liên hệ hãng taxi tìm lại máy trước, đến thứ Hai nếu chưa thấy thì mới báo IT và quản lý.
- **B.** Báo khách ngay tối nay rằng source code dự án đã bị lộ ra ngoài và xin lỗi trước.
- **C.** Tự khóa tài khoản dev, đổi mật khẩu repo, xử lý gọn trong nội bộ dự án không cần báo IT.
- **D.** Báo IT/bảo mật ngay tối nay để xác nhận mã hóa, khóa máy từ xa và thu hồi mọi quyền truy cập.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Mất máy là sự cố bảo mật; mỗi giờ chậm là cửa sổ rủi ro còn mở, và quy định thường yêu cầu báo ngay khi phát hiện.
- **B** ✗ Chưa biết máy có mã hóa, đã khóa từ xa được chưa thì chưa thể nói 'đã lộ'; báo sai mức độ gây hoảng và mất uy tín.
- **C** ✗ Thu hồi quyền là đúng nhưng làm riêng trong dự án bỏ qua IT/bảo mật: không có log quản lý thiết bị, không có quyết định báo khách theo quy trình.
- **D** ✅ IT có công cụ quản lý thiết bị để xác minh mã hóa, khóa/xóa từ xa và thu hồi VPN, token; đây là cách khoanh vùng nhanh nhất và đúng quy trình.

**Đáp án mẫu:**

① Xác nhận fact: Trong 30 phút: hỏi developer thời gian, địa điểm, máy có khóa màn hình không, có dữ liệu thật của khách không; IT tra hệ thống quản lý thiết bị xem mã hóa đã bật chưa và lần kết nối cuối.  
② Hành động ngay: Ngay tối nay: IT khóa/xóa máy từ xa, thu hồi VPN, token Git, SSH key của developer; đổi các secret dùng chung có trên máy; song song liên hệ hãng taxi, trình báo công an nếu quy định yêu cầu.  
③ Báo khách theo 報連相: Trong 24 giờ (hoặc theo hợp đồng), cùng bộ phận bảo mật báo 窓口 và người phụ trách bảo mật của khách: sự việc, tình trạng mã hóa, biện pháp đã làm, lịch gửi báo cáo sự cố chính thức.  
④ Gốc rễ & phòng ngừa: 横展開: rà toàn bộ máy dự án đã bật mã hóa và quản lý thiết bị chưa; quy định không lưu dữ liệu thật trên laptop, hạn chế mang máy dự án ra ngoài; kiểm tra định kỳ hằng tháng.  

**Đừng làm:**

- Chờ đến ngày làm việc tiếp theo mới báo vì 'biết đâu tìm lại được'.
- Không thu hồi token, SSH key vì nghĩ máy đã có mật khẩu đăng nhập.

**Câu tiếng Nhật:** 端末紛失の件、現時点の状況をご報告いたします。 (Tanmatsu funshitsu no ken, genjiten no jōkyō o go-hōkoku itashimasu.) — Về việc mất thiết bị, chúng tôi xin báo cáo tình hình tại thời điểm hiện tại.

**Trả lời 30 giây:** “Em báo IT và bảo mật ngay trong tối để xác minh mã hóa, khóa máy từ xa và thu hồi mọi quyền truy cập, không đợi tìm được máy. Có fact rồi thì cùng bộ phận bảo mật báo khách trong thời hạn hợp đồng, kèm biện pháp đã làm. Nguyên tắc: khoanh vùng trong giờ đầu, báo đúng kênh, rồi 横展開 kiểm tra toàn bộ thiết bị.”

**Tài liệu dùng:** IR (Incident Report), RR (Risk Register)  
**Chỉ số theo dõi:** INC (Incident Count), MTTR (Mean Time to Restore)

</details>

<a id="s38"></a>

### S38 · Gửi nhầm email chứa dữ liệu khách

_Mức: Cơ bản_

**Bối cảnh:** 10 giờ sáng, BrSE gửi file Excel 'test data' cho khách sản xuất C nhưng autocomplete chọn nhầm địa chỉ của một người ở khách bảo hiểm B (dự án khác của công ty). File chứa 300 dòng thông tin nhân viên của khách C (họ tên, email, số điện thoại) và không đặt mật khẩu. BrSE phát hiện sau 20 phút.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Gửi ngay email xin lỗi người nhận nhầm, đề nghị họ xóa file, rồi coi như đã xử lý xong.
- **B.** Xác nhận người nhận và nội dung file, báo bộ phận bảo mật, yêu cầu người nhận xóa có xác nhận.
- **C.** Gọi khách C ngay để xin lỗi, báo dữ liệu nhân viên đã bị lộ trước khi tìm hiểu thêm.
- **D.** Dùng chức năng thu hồi (recall) của Outlook để rút email lại, rồi theo dõi thêm.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Xin xóa là đúng nhưng chưa có xác nhận bằng văn bản, chưa báo bộ phận bảo mật và chủ dữ liệu là khách C — vẫn là che giấu sự cố.
- **B** ✅ Fact (ai nhận, có CC/forward không, file có gì) quyết định mức độ; song song báo bảo mật nội bộ và yêu cầu người nhận xóa có xác nhận là khoanh vùng đúng.
- **C** ✗ Khách C phải được báo, nhưng nên báo trong vài giờ cùng fact và biện pháp đã làm, không phải trước khi biết gì.
- **D** ✗ Recall chỉ hiệu quả trong cùng hệ thống mail và khi người nhận chưa đọc; gửi ra ngoài công ty hầu như không thu hồi được, tạo cảm giác an toàn giả.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 giờ: xác định chính xác địa chỉ nhận, có CC/forward không, số bản ghi và loại thông tin cá nhân; nếu được, hỏi người nhận đã mở file chưa.  
② Hành động ngay: Báo bộ phận bảo mật/ISMS ngay; nhờ PM phụ trách khách B liên hệ người nhận đề nghị xóa file khỏi hộp thư và thùng rác, xin xác nhận xóa bằng văn bản.  
③ Báo khách theo 報連相: Trong ngày, cùng bộ phận bảo mật báo khách C qua 窓口: sự việc, dữ liệu liên quan, người nhận là ai, đã xác nhận xóa chưa, lịch gửi 事故報告書; đồng thời báo phía khách B.  
④ Gốc rễ & phòng ngừa: Gốc rễ: autocomplete địa chỉ, file không mã hóa, không có bước kiểm tra lần 2. 再発防止: cảnh báo khi gửi ra ngoài + hẹn giờ gửi, bắt buộc dùng link chia sẻ có phân quyền, test data phải che dữ liệu thật; 横展開 cho các team.  

**Đừng làm:**

- Dựa vào recall rồi không báo ai.
- Chỉ xin lỗi người nhận nhầm mà không báo chủ dữ liệu là khách C.

**Câu tiếng Nhật:** メールの誤送信につきまして、深くお詫び申し上げます。 (Mēru no gosōshin ni tsukimashite, fukaku o-wabi mōshiagemasu.) — Về việc gửi nhầm email, chúng tôi thành thật xin lỗi.

**Trả lời 30 giây:** “Em xác nhận trong 1 giờ ai đã nhận và file có bao nhiêu dữ liệu cá nhân, đồng thời báo bộ phận bảo mật và yêu cầu người nhận xóa có xác nhận bằng văn bản. Trong ngày, em cùng bộ phận bảo mật báo khách C là chủ dữ liệu, rồi sửa gốc: cảnh báo gửi ra ngoài, link có phân quyền, che dữ liệu thật. Nguyên tắc: không dựa vào recall và không giấu chủ dữ liệu.”

**Tài liệu dùng:** IR (Incident Report), RR (Risk Register)  
**Chỉ số theo dõi:** INC (Incident Count), CLM (Complaints)

</details>

<a id="s39"></a>

### S39 · Audit ISMS phát hiện vi phạm ở dự án

_Mức: Trung cấp_

**Bối cảnh:** Audit nội bộ ISMS (ISO 27001) tháng 11 phát hiện tại dự án khách ngân hàng A: 4 tài khoản của người đã rời dự án 2–3 tháng vẫn còn quyền vào server staging của khách, và tài liệu 基本設計 (thiết kế cơ bản) nằm trên Google Drive cá nhân của 1 thành viên. Auditor ghi 2 điểm không phù hợp nhẹ (minor), hạn khắc phục 30 ngày. Khách dự kiến tự audit vendor vào tháng 1.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Thu hồi 4 tài khoản và xóa file trên Drive ngay trong ngày, rồi báo auditor là đã khắc phục xong.
- **B.** Giải thích với auditor rằng staging không chứa dữ liệu thật, đề nghị hạ mức hoặc bỏ phát hiện.
- **C.** Khắc phục ngay 2 điểm, rà toàn bộ phạm vi tương tự, rồi phân tích gốc rễ và lập 是正処置 có hạn.
- **D.** Báo ngay khách ngân hàng A về 2 phát hiện để chủ động minh bạch trước audit tháng 1.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Sửa triệu chứng nhanh là cần, nhưng chưa rà còn tài khoản/file nào khác và chưa sửa quy trình offboarding thì lần audit sau sẽ lặp lại.
- **B** ✗ Tranh luận để hạ mức không làm rủi ro giảm; ISMS đánh giá việc tuân thủ quy trình, kể cả với môi trường không có dữ liệu thật.
- **C** ✅ Khắc phục tức thời (修正) + rà toàn bộ phạm vi + sửa gốc rễ (是正処置 – hành động khắc phục) là cấu trúc mà auditor và khách ngân hàng mong đợi, và chuẩn bị tốt cho audit tháng 1.
- **D** ✗ Có thể phải báo nếu hợp đồng yêu cầu, nhưng cần fact phạm vi và kế hoạch khắc phục trước; báo khi chưa có gì chỉ làm khách lo.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: so toàn bộ tài khoản trên mọi hệ thống của khách (staging, VPN, Git, công cụ quản lý ticket) với danh sách thành viên hiện tại; rà thêm tài liệu trên lưu trữ cá nhân; kiểm log truy cập của 4 tài khoản sau ngày rời dự án.  
② Hành động ngay: Thu hồi ngay quyền thừa; chuyển tài liệu về kho lưu trữ được duyệt và xóa bản cá nhân có xác nhận; nếu log cho thấy có truy cập sau ngày rời thì nâng thành sự cố và kích hoạt quy trình báo cáo.  
③ Báo khách theo 報連相: Gửi auditor kế hoạch 是正処置 có hạn trong 2 tuần; kiểm hợp đồng về nghĩa vụ báo khách — nếu có, hoặc log có bất thường, báo 窓口 kèm kết quả rà soát và biện pháp; trình lại ở 定例会 trước audit tháng 1.  
④ Gốc rễ & phòng ngừa: Gốc rễ: offboarding không có checklist quyền trên hệ thống của khách, thiếu kho lưu trữ được duyệt dễ dùng. 再発防止: checklist offboarding có người duyệt, rà quyền hằng tháng, chặn Drive cá nhân trên máy dự án; 横展開 các dự án khác.  

**Đừng làm:**

- Chỉ sửa đúng 2 điểm bị phát hiện mà không rà toàn bộ.
- Tranh luận với auditor để hạ mức thay vì sửa quy trình.

**Câu tiếng Nhật:** 是正処置計画を作成し、改めてご報告いたします。 (Zesei shochi keikaku o sakusei shi, aratamete go-hōkoku itashimasu.) — Chúng tôi sẽ lập kế hoạch khắc phục và báo cáo lại với quý khách.

**Trả lời 30 giây:** “Em khắc phục ngay 2 điểm nhưng không dừng ở đó: rà toàn bộ tài khoản và tài liệu trên mọi hệ thống, kiểm log xem có truy cập sau ngày rời không, rồi lập 是正処置 có hạn cho quy trình offboarding. Nếu log có bất thường thì nâng thành sự cố và báo khách. Nguyên tắc: sửa triệu chứng, rà phạm vi, sửa gốc rễ — đủ cả 3.”

**Tài liệu dùng:** RR (Risk Register), IL (Issue Log), LL (Lessons Learned)  
**Chỉ số theo dõi:** IAGE (Issue Aging), INC (Incident Count)

</details>

<a id="s40"></a>

### S40 · Vendor khác trễ IF, chặn dự án

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách bảo hiểm B, team 11 người, đang ở 結合テスト; hệ thống của mình kết nối với hệ thống core do vendor X phát triển (vendor X ký hợp đồng trực tiếp với khách). Vendor X đã trễ 2 tuần việc cung cấp môi trường test IF và bản IF仕様書 sửa đổi; trễ thêm 1 tuần nữa thì 総合テスト (kiểm thử hệ thống) và 納期 cuối tháng 3 (年度末) của mình sẽ trễ. Anh/chị không có quyền chỉ đạo vendor X.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Định lượng tác động lên lịch, báo khách bằng văn bản, đề nghị khách điều phối vendor X, kèm phương án stub.
- **B.** Liên hệ thẳng PM của vendor X để thúc, và đề nghị team mình làm giúp phần IF cho nhanh.
- **C.** Dựng stub để test tiếp và tạm chưa báo khách, vì hiện tại 納期 vẫn chưa bị ảnh hưởng.
- **D.** Ghi vào リスク管理表, chờ đến 定例会 tháng sau nếu trễ thực sự ảnh hưởng thì mới báo khách.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Vendor X ký với khách nên chỉ khách có quyền điều phối; PM phải biến rủi ro thành số (ngày trễ, ngày chót cần IF) và văn bản để trách nhiệm không rơi vào mình, đồng thời chủ động giảm ảnh hưởng bằng stub.
- **B** ✗ Trao đổi kỹ thuật trực tiếp có thể hữu ích, nhưng thúc vendor khác là vượt vai trò, và làm thay phần IF là nhận trách nhiệm ngoài hợp đồng.
- **C** ✗ Stub là đúng, nhưng không báo thì khi trễ thật khách sẽ hỏi vì sao không cảnh báo sớm — trách nhiệm chuyển sang mình.
- **D** ✗ Báo khi đã trễ là quá muộn để khách điều phối; 報連相 yêu cầu báo rủi ro khi còn cứu được.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: liệt kê IF bị chặn và test case phụ thuộc, tính ngày chót phải có môi trường IF để không ảnh hưởng 総合テスト; tập hợp các lần đã yêu cầu vendor X qua khách (ngày, nội dung).  
② Hành động ngay: Dựng stub theo IF仕様書 hiện có để test tiếp logic nội bộ; sắp lại thứ tự test, làm trước phần không phụ thuộc IF; cập nhật リスク管理表 và 課題管理表 với owner phía khách.  
③ Báo khách theo 報連相: Trong tuần, gửi 窓口 văn bản ご相談: tác động lịch theo kịch bản trễ thêm 1/2/3 tuần, ngày chót cần IF, đề nghị khách điều phối vendor X và họp 3 bên; ghi vào 議事録 và 課題管理表 có hạn trả lời.  
④ Gốc rễ & phòng ngừa: Từ kế hoạch: đưa mốc giao IF của bên thứ 3 vào 前提条件 hợp đồng và Gantt với owner là khách; họp 3 bên 2 tuần/lần ở giai đoạn 結合テスト; 横展開 cho các dự án có nhiều vendor.  

**Đừng làm:**

- Tự làm thay phần IF của vendor khác, nhận trách nhiệm ngoài hợp đồng.
- Chỉ báo miệng mà không có văn bản, 議事録 ghi ngày chót cần IF.

**Câu tiếng Nhật:** 連携先システムの遅延影響について、ご相談させてください。 (Renkei-saki shisutemu no chien eikyō ni tsuite, go-sōdan sasete kudasai.) — Cho phép chúng tôi trao đổi về ảnh hưởng do hệ thống liên kết bị chậm trễ.

**Trả lời 30 giây:** “Em không có quyền với vendor X, nên việc của em là định lượng tác động: ngày chót cần IF, kịch bản trễ 1/2/3 tuần, rồi báo khách bằng văn bản và đề nghị khách điều phối, họp 3 bên. Trong lúc chờ, em dựng stub và sắp lại thứ tự test để giảm ảnh hưởng. Nguyên tắc: phụ thuộc bên ngoài phải có owner phía khách và có văn bản.”

**Tài liệu dùng:** RR (Risk Register), IL (Issue Log), API (Interface / API Specification)  
**Chỉ số theo dõi:** SLIP (Schedule Slip (days)), TF (Total Float), IAGE (Issue Aging)

</details>


## Tình huống xám

<a id="s41"></a>

### S41 · Khách gợi ý ghi giảm số bug trong báo cáo

_Mức: Khó_

**Bối cảnh:** Cuối 総合テスト dự án cho khách ngân hàng A, 品質報告書 (báo cáo chất lượng) ghi 182 bug, bug density vượt ngưỡng trên trong 品質計画書. Trưởng nhóm phía khách gợi ý: 'Gộp các bug cùng nguyên nhân và bỏ bug giao diện nhẹ, để số còn khoảng 120, nếu không cấp trên khó duyệt chuyển sang 受入テスト (UAT)'. Anh/chị biết gộp một phần là hợp lý về kỹ thuật.

**Câu hỏi:** Anh/chị xử lý gợi ý này thế nào?

- **A.** Làm theo gợi ý, vì chính khách yêu cầu và họ chịu trách nhiệm với cấp trên của họ.
- **B.** Từ chối thẳng, nói rõ rằng chỉnh số liệu chất lượng là vi phạm đạo đức nghề nghiệp.
- **C.** Giữ nguyên số 182, không giải thích thêm, để cấp trên phía khách tự đánh giá.
- **D.** Giữ số gốc, bổ sung phân tích theo nguyên nhân, mức độ và xu hướng hội tụ để giải thích đúng chất lượng.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Báo cáo chất lượng sai với khách tài chính là rủi ro lớn nhất: nếu 本番 có 障害 (sự cố), số liệu bị chỉnh sẽ quay lại thành vấn đề của vendor, kể cả khi khách là người gợi ý.
- **B** ✗ Đúng nguyên tắc nhưng làm mất mặt người phụ trách và bỏ qua mối lo chính đáng của họ là khó được duyệt.
- **C** ✗ Trung thực nhưng thiếu phân tích làm số 182 bị hiểu thành 'chất lượng kém', trong khi có thể bug đã hội tụ và phần lớn là mức nhẹ.
- **D** ✅ Số gốc là sự thật; phân tích theo nguyên nhân gốc, mức độ, đường cong hội tụ giúp người phụ trách có câu chuyện trung thực để trình cấp trên — giải quyết đúng mối lo của họ.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1–2 ngày: QA lead phân loại 182 bug theo nguyên nhân gốc, mức độ, giai đoạn phát sinh; vẽ đường cong hội tụ 4 tuần cuối; đếm số bug thật sự trùng nguyên nhân.  
② Hành động ngay: Viết lại 品質報告書: giữ tổng 182, thêm bảng số nguyên nhân gốc, tỉ lệ bug nhẹ, xu hướng hội tụ, giải thích vì sao vượt ngưỡng (ví dụ test dày hơn kế hoạch) và biện pháp cho vùng nhiều bug.  
③ Báo khách theo 報連相: Trước buổi duyệt, 根回し (trao đổi trước) riêng với trưởng nhóm khách: cảm ơn gợi ý, giải thích công ty không sửa số gốc nhưng đã thêm phân tích để dễ trình; nếu họ vẫn ép, báo sếp mình và ghi lại trao đổi.  
④ Gốc rễ & phòng ngừa: Chốt từ đầu dự án trong 品質計画書 quy tắc đếm bug (gộp trùng nguyên nhân, phân loại UI) để cuối kỳ không tranh cãi số liệu; ghi vào bài học dự án.  

**Đừng làm:**

- Chỉnh số để làm hài lòng một người phía khách mà không có quy tắc đếm đã thống nhất.
- Giữ số gốc nhưng không phân tích, để số bug bị hiểu sai.

**Câu tiếng Nhật:** 件数は修正せず、分析を追記してご説明いたします。 (Kensū wa shūsei sezu, bunseki o tsuiki shite go-setsumei itashimasu.) — Chúng tôi không chỉnh sửa số lượng, mà sẽ bổ sung phân tích để giải thích.

**Trả lời 30 giây:** “Em không chỉnh số bug nhưng cũng không từ chối suông: giữ nguyên 182, bổ sung phân tích theo nguyên nhân gốc, mức độ và đường cong hội tụ để người phụ trách có câu chuyện trung thực trình cấp trên. Quy tắc đếm bug em chốt trong 品質計画書 ngay từ đầu để cuối kỳ không phải tranh cãi. Nguyên tắc: số liệu không đổi, cách giải thích thì làm tốt hơn.”

**Tài liệu dùng:** QR (Quality / Test Report), QMP (Quality Management Plan), BUG (Bug List / Defect Log)  
**Chỉ số theo dõi:** BD (Bug Density), BCV (Bug Convergence), OPB (Open Bugs by Severity)

</details>

<a id="s42"></a>

### S42 · Sếp muốn giấu delay đến sau review

_Mức: Khó_

**Bối cảnh:** Dự án 請負 cho khách sản xuất C đang ở 製造 (coding), SPI 0,82, ước trễ 納期 khoảng 2 tuần nếu không có biện pháp. Giám đốc delivery yêu cầu chưa báo khách trước buổi review 6 tháng tuần sau — buổi quyết định gia hạn hợp đồng giai đoạn 2 — vì 'team sẽ OT để kéo lại'. 定例会 (họp định kỳ) với khách là thứ Sáu này.

**Câu hỏi:** Anh/chị làm gì trước 定例会 thứ Sáu?

- **A.** Làm theo sếp, cho team OT 2 tuần để kéo lại, nếu sau buổi review vẫn trễ thì mới báo khách.
- **B.** Lập kế hoạch phục hồi có số, thuyết phục sếp báo khách kèm kế hoạch đó trước buổi review.
- **C.** Tự báo khách ở 定例会 thứ Sáu, vì minh bạch với khách quan trọng hơn chỉ đạo của sếp.
- **D.** Báo khách là có 'một số rủi ro về lịch' nhưng chưa nêu con số trễ cụ thể.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: B**

- **A** ✗ Nếu OT không kéo kịp, khách phát hiện trễ sau khi đã gia hạn sẽ mất niềm tin nặng hơn nhiều; OT 2 tuần liên tục còn làm tăng bug và nguy cơ nghỉ việc.
- **B** ✅ Sếp lo mất hợp đồng giai đoạn 2; điều thuyết phục được là kế hoạch phục hồi có số và lập luận rằng báo sớm kèm giải pháp tăng uy tín trong review. Nếu vẫn bị chặn, PM ghi lại và đi qua kênh PMO/QA theo quy định.
- **C** ✗ Vượt mặt sếp phá vỡ chuỗi chỉ huy và quan hệ nội bộ khi chưa dùng hết kênh nội bộ.
- **D** ✗ Nói mập mờ cũng là che giấu; khách Nhật sẽ hỏi số cụ thể và mất tin khi biết vendor đã có số từ trước.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1–2 ngày: phân tích gốc của SPI 0,82 (task nào, vì sao), tính ngày hoàn thành theo 3 kịch bản: giữ nguyên, OT vừa phải, thêm người hoặc giảm scope.  
② Hành động ngay: Lập kế hoạch phục hồi: biện pháp, nguồn lực, SPI mục tiêu từng tuần, ngày bắt kịp; OT có giới hạn (ví dụ ≤ 20 giờ/tháng/người – tham khảo).  
③ Báo khách theo 報連相: Trước thứ Năm, gặp sếp trình kế hoạch và đề xuất báo khách ở 定例会 theo kiểu 'phát hiện sớm + đã có kế hoạch'; nếu sếp vẫn không đồng ý, gửi email ghi lại ý kiến của mình và hỏi PMO/QA theo quy định, không tự vượt cấp với khách.  
④ Gốc rễ & phòng ngừa: Đưa vào kế hoạch truyền thông quy tắc: SPI < 0,9 hai tuần liên tiếp thì phải báo khách kèm kế hoạch (tham khảo); 進捗報告書 hằng tuần dùng số EVM để việc báo cáo không phụ thuộc ý chí cá nhân.  

**Đừng làm:**

- Dùng OT dài ngày để che trễ thay vì báo sớm có kế hoạch.
- Vượt cấp báo khách khi chưa dùng hết kênh nội bộ.

**Câu tiếng Nhật:** 遅延の可能性と挽回策について、ご報告いたします。 (Chien no kanōsei to bankai-saku ni tsuite, go-hōkoku itashimasu.) — Chúng tôi xin báo cáo về khả năng chậm trễ và biện pháp khắc phục.

**Trả lời 30 giây:** “Em hiểu sếp lo hợp đồng giai đoạn 2, nên em mang đến kế hoạch phục hồi có số và lập luận rằng báo sớm kèm giải pháp giữ uy tín tốt hơn để khách tự phát hiện. Nếu sếp vẫn không đồng ý, em ghi lại bằng văn bản và đi qua kênh PMO chứ không vượt cấp. Nguyên tắc: không giấu delay, nhưng báo có kế hoạch và đúng kênh.”

**Tài liệu dùng:** SR (Status Report), GNT (Gantt Chart / Schedule), CMP (Communication Plan)  
**Chỉ số theo dõi:** SPI (Schedule Performance Index), SLIP (Schedule Slip (days)), OT (Overtime Hours)

</details>

<a id="s43"></a>

### S43 · Chọn 納期 hay chất lượng trước 本番

_Mức: Khó_

**Bối cảnh:** Dự án cho khách bảo hiểm B, リリース lên 本番 cố định ngày 1/4 (gắn với ra mắt sản phẩm bảo hiểm mới của khách). Còn 10 ngày, 総合テスト tiêu hóa 85%, còn 6 bug mức trung ở báo cáo nội bộ và 1 bug mức cao ở tính phí cho một loại hợp đồng đặc biệt (khoảng 2% số hợp đồng). Team chia 2 phe: release đúng hạn hoặc lùi 1 tuần.

**Câu hỏi:** Anh/chị đề xuất gì với khách?

- **A.** Lùi release 1 tuần để chạy đủ 100% test và sửa hết bug, vì chất lượng là trên hết.
- **B.** Release đúng 1/4 với toàn bộ chức năng, các bug còn lại sửa bằng hotfix sau release.
- **C.** Phân tích rủi ro từng bug, đề xuất release 1/4 có điều kiện: chặn hoặc xử lý thủ công phần lỗi, hotfix theo lịch.
- **D.** Cho team OT tối đa trong 10 ngày để chạy đủ test và sửa hết bug, giữ cả 納期 lẫn chất lượng.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: C**

- **A** ✗ Ngày 1/4 gắn với sản phẩm mới của khách; lùi release có thể gây thiệt hại kinh doanh lớn hơn bug, và quyết định này không phải của vendor.
- **B** ✗ Đưa bug tính phí mức cao lên 本番 của khách bảo hiểm là rủi ro tính sai tiền cho khách hàng thật — không chấp nhận được nếu không có biện pháp.
- **C** ✅ Không phải chọn 1 trong 2 mà khoanh rủi ro: bug tính phí có thể chặn nhập loại hợp đồng đó hoặc xử lý thủ công tạm, bug báo cáo nội bộ có workaround; khách quyết dựa trên bảng rủi ro rõ ràng.
- **D** ✗ OT dồn dập 10 ngày cuối dễ sinh bug mới, test vội khó tin cậy, và vẫn không đảm bảo kịp.

**Đáp án mẫu:**

① Xác nhận fact: Trong 1 ngày: đánh giá từng bug — ảnh hưởng nghiệp vụ, số hợp đồng bị ảnh hưởng, có workaround không, thời gian sửa + retest; xác định 15% test chưa chạy thuộc vùng nào, ưu tiên vùng tính phí.  
② Hành động ngay: Dồn lực sửa bug tính phí và chạy hết test vùng tính phí trước; chuẩn bị phương án vận hành tạm (chặn loại hợp đồng đặc biệt trên màn hình, xử lý thủ công), kế hoạch hotfix và rollback.  
③ Báo khách theo 報連相: Trong 2 ngày, gửi khách tài liệu ご相談: bảng rủi ro, 3 phương án (release đủ / release có điều kiện / lùi), khuyến nghị của mình; để cấp có thẩm quyền phía khách quyết định ở buổi 出荷判定 (go/no-go) và ghi 議事録.  
④ Gốc rễ & phòng ngừa: Gốc: tiêu hóa test chậm do không ưu tiên theo rủi ro. Từ dự án sau: テスト計画書 ưu tiên theo rủi ro nghiệp vụ, chốt tiêu chí 出荷判定 ngay trong 品質計画書.  

**Đừng làm:**

- Tự quyết lùi hay giữ ngày release thay khách mà không đưa phương án.
- Release mà không có biện pháp tạm cho bug liên quan đến tính tiền.

**Câu tiếng Nhật:** 条件付きリリース案について、ご判断をお願いいたします。 (Jōken-tsuki rirīsu-an ni tsuite, go-handan o onegai itashimasu.) — Kính mong quý khách đưa ra quyết định về phương án release có điều kiện.

**Trả lời 30 giây:** “Em không coi đây là chọn 納期 hay chất lượng mà khoanh rủi ro theo từng bug: bug tính phí phải sửa hoặc chặn bằng vận hành tạm, bug báo cáo nội bộ có workaround và hotfix theo lịch. Em đưa khách bảng rủi ro với 3 phương án kèm khuyến nghị, quyết định là của khách. Nguyên tắc: không đưa lỗi tính tiền lên 本番 khi chưa có biện pháp, và không tự quyết thay khách.”

**Tài liệu dùng:** QR (Quality / Test Report), RLP (Release / Cutover Plan), RR (Risk Register)  
**Chỉ số theo dõi:** TEX (Test Execution Rate), OPB (Open Bugs by Severity), DL (Defect Leakage)

</details>

<a id="s44"></a>

### S44 · Một PM, hai dự án cùng đỏ

_Mức: Khó_

**Bối cảnh:** Anh/chị là PM của 2 dự án: dự án 1 cho khách ngân hàng A đang 受入テスト, khách vừa báo 3 bug mức cao, 検収 dự kiến cuối tháng; dự án 2 cho khách sản xuất C đang 詳細設計, trễ 8 ngày, khách yêu cầu họp giải trình trong tuần. Cả 2 đều đỏ trên báo cáo PMO. Tuần này anh/chị chỉ đủ thời gian xử lý sâu 1 dự án.

**Câu hỏi:** Anh/chị phân bổ thời gian thế nào?

- **A.** Đánh giá tác động và độ khẩn của mỗi dự án, ưu tiên 1 bên, xin sếp người hỗ trợ bên còn lại.
- **B.** Chia đều 50/50 thời gian cho 2 dự án để cả 2 khách đều thấy PM đang theo sát.
- **C.** Tập trung dự án ngân hàng A vì khách tài chính quan trọng hơn, dự án 2 giao leader tự xử lý.
- **D.** Làm thêm giờ buổi tối và cuối tuần để tự xử lý sâu cả 2 dự án song song trong tuần này.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: A**

- **A** ✅ Ưu tiên phải dựa trên tác động (doanh thu 検収, rủi ro 本番, niềm tin của khách) và độ khẩn, và phải công khai với sếp để có người đỡ bên còn lại — không chọn trong im lặng.
- **B** ✗ Chia đều nghe công bằng nhưng cả 2 bên đều xử lý nửa vời, dễ đỏ tiếp cả 2.
- **C** ✗ Ưu tiên theo loại khách là cảm tính; giao dự án 2 cho leader mà không báo sếp, không chuẩn bị giải trình sẽ làm buổi họp với khách C thất bại.
- **D** ✗ Ôm hết một mình làm giảm chất lượng quyết định ở cả 2 dự án và che giấu vấn đề nguồn lực với cấp trên.

**Đáp án mẫu:**

① Xác nhận fact: Trong nửa ngày: với mỗi dự án, xác định việc chỉ PM làm được (quyết định, gặp khách) và việc giao được; tác động nếu trễ thêm 1 tuần (検収 trượt sang tháng sau, mất doanh thu tháng; khách C mất niềm tin).  
② Hành động ngay: Dồn sức dự án 1 cho phân tích 3 bug UAT (gắn với 検収 và doanh thu); dự án 2 chuẩn bị tài liệu giải trình (nguyên nhân trễ, kế hoạch bắt kịp) và giao leader/BrSE theo dõi hằng ngày.  
③ Báo khách theo 報連相: Ngay hôm nay báo sếp/PMO về xung đột, đề xuất 1 PM hoặc senior hỗ trợ dự án 2 trong 2 tuần; với khách C, vẫn tự dự buổi giải trình (1–2 giờ) vì đó là cam kết trực tiếp với khách.  
④ Gốc rễ & phòng ngừa: Đề xuất PMO cảnh báo khi 1 PM có từ 2 dự án ở giai đoạn quan trọng trùng nhau; mỗi dự án có phó PM/leader được ủy quyền để giảm bus factor.  

**Đừng làm:**

- Tự chọn bỏ một dự án mà không báo sếp.
- Chia đều thời gian khiến cả hai dự án không được xử lý dứt điểm.

**Câu tiếng Nhật:** 体制を強化し、挽回計画をご説明いたします。 (Taisei o kyōka shi, bankai keikaku o go-setsumei itashimasu.) — Chúng tôi sẽ tăng cường đội ngũ và trình bày kế hoạch khắc phục.

**Trả lời 30 giây:** “Em đánh giá tác động và độ khẩn của từng dự án, ưu tiên bên gắn với 検収 và rủi ro lớn hơn, đồng thời báo sếp ngay để có người đỡ bên còn lại. Cam kết trực tiếp với khách như buổi giải trình thì em vẫn tự dự. Nguyên tắc: ưu tiên công khai theo tiêu chí, không ôm một mình và không bỏ rơi khách nào trong im lặng.”

**Tài liệu dùng:** SR (Status Report), RP (Resource / Staffing Plan), OBS (Organizational Breakdown Structure)  
**Chỉ số theo dõi:** BUS (Bus Factor), UTL (Utilization), SLIP (Schedule Slip (days))

</details>

<a id="s45"></a>

### S45 · Khách đòi OT cuối tuần không trả thêm

_Mức: Trung cấp_

**Bối cảnh:** Dự án 準委任 cho khách ngân hàng A, team 10 người, đơn giá theo tháng dựa trên 160 giờ/người. 4 tuần liên tiếp, 窓口 khách nhắn thẳng cho leader yêu cầu team làm thứ Bảy để kịp mốc nội bộ của họ, nói 'đơn giá tháng đã bao gồm'. OT trung bình đã 35 giờ/người/tháng, 2 thành viên vừa xin nghỉ việc.

**Câu hỏi:** Việc đầu tiên anh/chị làm là gì?

- **A.** Tiếp tục đáp ứng vì khách ngân hàng là khách lớn, ghi nhận OT nội bộ để tính thưởng cho team.
- **B.** Từ chối mọi yêu cầu làm cuối tuần từ nay để bảo vệ sức khỏe và giữ chân team.
- **C.** Gửi khách hóa đơn bổ sung cho toàn bộ giờ OT 4 tuần qua theo đơn giá giờ.
- **D.** Đối chiếu hợp đồng và số giờ OT thực tế, rồi đề xuất khách quy tắc làm thêm có duyệt, có phí.

<details><summary>Đáp án</summary>

**Lựa chọn tốt nhất: D**

- **A** ✗ Đáp ứng mãi biến OT thành thường lệ, mất người (đã 2 người xin nghỉ) và tạo tiền lệ khách bỏ qua hợp đồng.
- **B** ✗ Cấm hẳn làm hỏng quan hệ khi khách có thể có nhu cầu gấp hợp lý; cần quy tắc chứ không phải lệnh cấm.
- **C** ✗ Tính phí hồi tố khi chưa thỏa thuận dễ thành tranh chấp; nếu hợp đồng có 精算幅 (khoảng giờ điều chỉnh) thì một phần OT có thể đã nằm trong đó.
- **D** ✅ Dựa vào hợp đồng (giờ chuẩn, 精算幅, đơn giá vượt giờ) và số OT thật, PM đề xuất quy tắc: yêu cầu qua PM, duyệt trước, có phí hoặc đổi ưu tiên backlog — vừa bảo vệ team vừa minh bạch với khách.

**Đáp án mẫu:**

① Xác nhận fact: Trong 2 ngày: kiểm hợp đồng (giờ chuẩn, 精算幅 ví dụ 140–180 giờ – tham khảo, đơn giá vượt giờ); tổng hợp giờ thực tế từng người 4 tuần qua; nói chuyện 1-1 với 2 người xin nghỉ.  
② Hành động ngay: Ngay tuần này: mọi yêu cầu làm thêm phải qua PM, không qua leader; giới hạn OT theo luật lao động và quy định công ty; xếp lại ưu tiên để mốc nội bộ của khách tập trung vào phần quan trọng nhất.  
③ Báo khách theo 報連相: Trước 定例会 tuần tới, gửi 窓口 bảng giờ thực tế so với hợp đồng và đề xuất: làm thêm cần duyệt trước, tính đơn giá vượt giờ khi vượt 精算幅, hoặc đổi ưu tiên/tăng người; nếu không thống nhất, xin họp với cấp quản lý của họ cùng sếp mình.  
④ Gốc rễ & phòng ngừa: Ghi rõ trong kế hoạch truyền thông kênh nhận yêu cầu và quy tắc làm thêm; theo dõi OT và tỉ lệ nghỉ việc hằng tháng, cảnh báo khi OT > 30 giờ/người/tháng (tham khảo).  

**Đừng làm:**

- Để khách giao việc thẳng cho leader, bỏ qua PM.
- Im lặng chịu OT đến khi team nghỉ việc hàng loạt.

**Câu tiếng Nhật:** 休日作業のルールについて、ご相談させてください。 (Kyūjitsu sagyō no rūru ni tsuite, go-sōdan sasete kudasai.) — Cho phép chúng tôi trao đổi về quy tắc làm việc ngày nghỉ.

**Trả lời 30 giây:** “Em không đáp ứng mãi cũng không cấm, mà đối chiếu hợp đồng — giờ chuẩn, 精算幅, đơn giá vượt giờ — với số OT thật, rồi đề xuất khách quy tắc: làm thêm qua PM, duyệt trước, có phí hoặc đổi ưu tiên. Song song em giới hạn OT và nói chuyện với người xin nghỉ. Nguyên tắc: hợp đồng là căn cứ, sức bền của team là tài sản của cả hai bên.”

**Tài liệu dùng:** SOW (Statement of Work), CMP (Communication Plan), SR (Status Report)  
**Chỉ số theo dõi:** OT (Overtime Hours), ATR (Attrition Rate), UTL (Utilization)

</details>

