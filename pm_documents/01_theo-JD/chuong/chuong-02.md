# Chương 2 · Nền tảng quản lý dự án (PMBOK · PRINCE2 · EVM) (Q101–Q200)

## 2.1 Khung tổng: dự án, vòng đời, quy trình và tailoring

**Q101. Dự án khác vận hành (operation) ở điểm nào, và vì sao PM outsourcing cần phân biệt rõ?**
Dự án là nỗ lực **tạm thời** tạo ra kết quả **duy nhất**, có điểm đầu–cuối; vận hành là công việc **lặp lại, liên tục** để duy trì kết quả đó. Trong outsourcing, ranh giới này quyết định hợp đồng và cách đo: dự án đo theo phạm vi–tiến độ–nghiệm thu, còn 運用保守 (unyou hoshu – vận hành & bảo trì) đo theo SLA, số ticket, thời gian phản hồi. Không tách rõ thì khách dễ đẩy việc vận hành vô hạn vào ngân sách dự án.
> 💡 Ví dụ ghi điểm: sửa lỗi trong thời gian bảo hành thuộc dự án, còn yêu cầu mới phát sinh hằng tháng sau go-live phải chuyển sang hợp đồng vận hành.

**Q102. Vòng đời dự án (project life cycle) khác vòng đời phát triển (development life cycle) thế nào?**
Project life cycle là chuỗi pha từ khởi động đến đóng dự án; development life cycle là cách tạo ra sản phẩm bên trong: predictive (waterfall), iterative, incremental, adaptive hoặc hybrid. Dự án với khách Nhật thường theo pha 要件定義 (youken teigi – định nghĩa yêu cầu) → 基本設計 (kihon sekkei – thiết kế cơ bản) → 詳細設計 (shousai sekkei – thiết kế chi tiết) → lập trình → test, mỗi pha kết thúc bằng tài liệu được duyệt. Chọn development life cycle theo độ chắc của yêu cầu, không theo sở thích của team.

**Q103. Năm nhóm quy trình (process groups) của PMBOK là gì? Chúng có phải các pha tuần tự không?**
Gồm Initiating, Planning, Executing, Monitoring & Controlling, Closing. Chúng **không phải** pha tuần tự mà lặp lại trong từng pha và chồng lấn nhau; riêng Monitoring & Controlling chạy suốt dự án. Ví dụ pha 基本設計 vẫn có lập kế hoạch pha, thực hiện, theo dõi và đóng pha bằng 検収 (kenshuu – nghiệm thu) tài liệu thiết kế.
> 💡 Bẫy kinh điển là đồng nhất process group với phase; nói "process group lặp lại trong mỗi phase" là điểm cộng.

**Q104. PMBOK chuyển từ cách tiếp cận theo quy trình sang theo nguyên tắc và performance domains — điều đó thay đổi gì trong cách làm PM?**
Bản 6 mô tả 5 process group, 10 knowledge area theo input–tool–output; bản 7 (2021) chuyển sang 12 principles (stewardship, value, systems thinking, tailoring…) và 8 performance domains (stakeholders, team, development approach & life cycle, planning, project work, delivery, measurement, uncertainty). Hệ quả: PM không "chạy đủ process" mà chọn cách làm tạo ra **outcome và giá trị**, đo bằng kết quả chứ không bằng số tài liệu. Công cụ cũ (WBS, EVM, risk register) vẫn dùng, nhưng được tailor theo bối cảnh.

**Q105. Project charter gồm những gì, ai ký, và trong outsourcing thì charter thực tế nằm ở đâu?**
Charter chính thức khởi động dự án và **trao quyền cho PM**: mục tiêu đo được, phạm vi cấp cao, milestone chính, ngân sách tổng, rủi ro cấp cao, stakeholder chính, tiêu chí thành công, sponsor. Sponsor ký, không phải PM. Trong outsourcing, nội dung này rải ở hợp đồng, proposal và tài liệu kickoff; em gom thành 1 trang tổng quan có 前提条件 (zentei jouken – điều kiện tiền đề) và 対象外 (taishougai – ngoài phạm vi) để hai bên xác nhận ngay buổi kickoff.
> 💡 Nhấn mạnh charter trao quyền: không có người ký thì PM không có thẩm quyền điều phối nguồn lực.

**Q106. Tailoring là gì? Cho ví dụ tailor quy trình cho dự án 3 tháng và dự án 18 tháng.**
Tailoring là điều chỉnh quy trình, tài liệu, mức kiểm soát cho vừa quy mô, rủi ro, loại hợp đồng và văn hóa khách. Dự án 3 tháng, 5 người: kế hoạch 1 file, báo cáo tuần, risk register gọn, CR duyệt qua email. Dự án 18 tháng, 40 người: chia stage có gate, CCB họp định kỳ, EVM hằng tuần, configuration audit trước mỗi lần giao, báo cáo nhiều tầng. Nguyên tắc: mức kiểm soát tương xứng với rủi ro, không áp nguyên bộ quy trình "cho đủ".

**Q107. Phân biệt project, program và portfolio. Senior PM ở công ty outsourcing liên quan thế nào với hai cấp sau?**
Project tạo một kết quả cụ thể; program là nhóm dự án liên quan được quản lý phối hợp để đạt lợi ích chung; portfolio là tập dự án/program được chọn và ưu tiên theo chiến lược tổ chức. Senior PM thường phụ trách nhiều dự án cho cùng một khách, gần với program: chia sẻ nguồn lực, đồng bộ milestone, quản lý rủi ro chéo. Ở cấp portfolio, PM cung cấp dữ liệu tiến độ, margin, rủi ro để lãnh đạo quyết định ưu tiên.

**Q108. PMO là gì, có những loại nào và PM nên tận dụng PMO ra sao?**
PMO chuẩn hóa quản trị dự án, thường ở 3 mức: supportive (cung cấp template, dữ liệu), controlling (yêu cầu tuân thủ, audit), directive (trực tiếp quản lý dự án). PM tận dụng PMO để lấy dữ liệu dự án cũ cho estimate, template báo cáo, checklist audit, và làm kênh escalation khi thiếu nguồn lực. Đổi lại, PM nộp số liệu đúng hạn để PMO thấy sớm dự án có nguy cơ "đỏ".

**Q109. Cơ cấu tổ chức functional, matrix, projectized ảnh hưởng đến quyền của PM thế nào? Công ty outsourcing thường ở dạng nào?**
Functional: PM ít quyền, nhân sự thuộc trưởng bộ phận; projectized: PM nắm toàn quyền nguồn lực; matrix (weak/balanced/strong) nằm giữa. Công ty outsourcing thường là matrix: kỹ sư thuộc line manager, PM điều phối theo dự án, nên tranh chấp người giữa các dự án là chuyện thường ngày. Cách làm: chốt resource plan với line manager từ đầu, ghi rõ % allocation và thời gian; khi bị rút người thì escalate kèm tác động tiến độ cụ thể.
> 💡 Câu này hay đi kèm "PM có quyền gì khi bị rút người?" — trả lời bằng resource plan đã thống nhất và số liệu tác động, không than phiền.

## 2.2 Tích hợp & kiểm soát thay đổi

**Q110. "Integration management" nghĩa là gì trong công việc hằng ngày của PM?**
Integration là ra quyết định trade-off giữa các ràng buộc (phạm vi, tiến độ, chi phí, chất lượng, rủi ro) để dự án vận hành như một thể thống nhất, thay vì tối ưu từng mảng riêng lẻ. Hằng ngày: gộp kế hoạch con thành project management plan, quyết định nhận CR dựa trên tác động tổng thể, cân nguồn lực giữa sửa bug và làm tính năng mới. PM là người duy nhất nhìn toàn cục nên không thể giao integration cho ai khác.

**Q111. Baseline là gì? Dự án có những baseline nào và khi nào được phép thay đổi?**
Baseline là phiên bản kế hoạch **đã được phê duyệt**, dùng làm mốc đo hiệu suất: scope baseline (scope statement + WBS + WBS dictionary), schedule baseline và cost baseline; ba cái gộp lại là performance measurement baseline (PMB). Baseline chỉ đổi khi có CR được duyệt qua change control, không đổi chỉ vì đang chậm. Mỗi lần re-baseline phải lưu version cũ để còn đo được độ lệch lịch sử.
> 💡 Đừng nói "trễ thì re-baseline" — câu đúng là re-baseline khi có thay đổi được duyệt, hoặc baseline cũ mất ý nghĩa và sponsor đồng ý.

**Q112. Mô tả quy trình xử lý change request (CR) chuẩn từ lúc khách đưa yêu cầu đến khi đóng.**
① Ghi nhận CR vào change log (người yêu cầu, nội dung, lý do, ngày); ② phân tích tác động tới phạm vi, 工数 (kousuu – công số/effort), tiến độ, chất lượng, rủi ro, hợp đồng; ③ trình phương án (làm ngay / gộp đợt sau / không làm) kèm chi phí; ④ người có thẩm quyền hoặc CCB duyệt/từ chối; ⑤ cập nhật baseline, tài liệu, thông báo team; ⑥ theo dõi đến khi nghiệm thu rồi đóng. CR bị từ chối cũng được lưu.
> 💡 Với khách Nhật, tính cả thời gian 稟議 (ringi – trình duyệt nội bộ) của khách vào lịch CR, có khi mất 1–2 tuần (tham khảo).

**Q113. Change Control Board (CCB) gồm ai, và khi nào PM được tự duyệt thay đổi?**
CCB thường gồm sponsor/đại diện khách, PM hai bên, BA hoặc tech lead, có thể thêm QA và bộ phận hợp đồng. Change management plan nên định ngưỡng thẩm quyền, ví dụ tham khảo: thay đổi không ảnh hưởng milestone và nằm trong 2–3 man-day buffer thì PM tự duyệt và ghi log; vượt ngưỡng hoặc đụng hợp đồng thì lên CCB. Ngưỡng rõ giúp vừa không nghẽn CCB vừa không lọt thay đổi lớn.
> 💡 Nêu được ngưỡng phân quyền cụ thể cho thấy bạn đã vận hành change control thật, không chỉ thuộc lý thuyết.

**Q114. Khách yêu cầu thay đổi qua chat trực tiếp với dev, không qua PM. Bạn xử lý thế nào?**
① Xác nhận nội dung với dev, tạm chưa code; ② liên hệ khách theo 報連相 (hourensou – báo cáo, liên lạc, thảo luận): cảm ơn yêu cầu, xin đưa vào CR để đánh giá tác động; ③ gửi đánh giá trong thời hạn cam kết (vd 1–2 ngày làm việc); ④ phòng ngừa: thống nhất lại kênh nhận yêu cầu trong communication plan, nhắc team quy tắc "yêu cầu mới → báo PM/BrSE (Bridge SE – kỹ sư cầu nối)". Không từ chối khách mà đưa yêu cầu về đúng quy trình.

**Q115. Configuration management khác change control ở điểm nào?**
Change control quyết định **có thay đổi hay không**; 構成管理 (kousei kanri – quản lý cấu hình) đảm bảo **mọi thành phần được nhận diện, đánh version và nhất quán** sau thay đổi: tài liệu, source, môi trường, dữ liệu test. Bốn hoạt động chính: identification, status accounting, kiểm soát thay đổi trên configuration item, verification & audit. Lỗi kinh điển: CR đã duyệt nhưng tài liệu 基本設計 không lên version, dev và tester làm theo hai bản khác nhau.

**Q116. Trong dự án phần mềm outsourcing, bạn đưa những gì vào danh sách configuration item (CI) và kiểm soát ra sao?**
Danh sách CI lập từ đầu: tài liệu yêu cầu/thiết kế, source code, script DB, cấu hình môi trường, test case và test data, tài liệu bàn giao, cả bản estimate. Mỗi CI có owner, nơi lưu (Git, kho tài liệu), quy tắc đặt tên version và trạng thái draft/review/approved/baselined. Trước mỗi lần 納品 (nouhin – giao hàng), em chạy configuration audit: version tài liệu khớp bản release, release note khớp danh sách CR đã duyệt.

**Q117. Khi nào nên gộp nhiều CR nhỏ thành một gói thay vì xử lý từng cái?**
Gộp khi các CR cùng module, không gấp, và chi phí xử lý (phân tích, duyệt, test hồi quy) lớn hơn bản thân thay đổi. Gói CR theo đợt (vd 2 tuần/lần hoặc theo release) giúp khách duyệt một lần, team test hồi quy một lần và estimate chính xác hơn. Ngoại lệ: CR liên quan bảo mật, pháp lý hoặc chặn go-live thì xử lý riêng, ngay.

**Q118. Sponsor phía khách nói: "Thay đổi nhỏ thôi, làm luôn, không cần CR". Bạn phản hồi thế nào mà không làm mất lòng?**
Em đồng ý về tinh thần nhưng vẫn ghi nhận: "Vâng, để hai bên cùng nắm, em ghi vào change log, tác động khoảng X giờ, không ảnh hưởng milestone". Nếu dưới ngưỡng PM tự duyệt thì làm luôn nhưng có dấu vết; khi nhiều "thay đổi nhỏ" cộng dồn vượt buffer, em trình tổng lũy kế để khách thấy và quyết định. Mục tiêu là minh bạch, không phải tính tiền từng việc nhỏ.
> 💡 Ý senior: phân biệt "linh hoạt" với "mất kiểm soát" — linh hoạt vẫn có log, tổng lũy kế có ngưỡng cảnh báo.

## 2.3 Phạm vi & yêu cầu

**Q119. Quản lý phạm vi gồm những quy trình nào, và trong dự án với khách Nhật chúng nằm ở đâu?**
Plan scope management → collect requirements → define scope → create WBS → validate scope → control scope. Yêu cầu, scope statement và WBS hình thành scope baseline; validate và control chạy suốt dự án. Với khách Nhật, collect và define nằm chủ yếu trong pha 要件定義, kết quả là tài liệu 要件定義書 được khách duyệt; WBS do vendor lập trong kế hoạch dự án, làm cơ sở estimate và theo dõi.

**Q120. WBS là gì? Quy tắc 100% (100% rule) nghĩa là gì?**
WBS phân rã toàn bộ deliverable và công việc của dự án thành các cấp nhỏ dần đến work package. Quy tắc 100%: tổng công việc ở các nút con bằng đúng 100% nút cha — không thiếu, không thừa — và toàn bộ WBS bao trùm 100% phạm vi, kể cả quản lý dự án, review, test, tài liệu, bàn giao. Đây là chỗ estimate hay hụt nhất: chỉ liệt kê tính năng mà quên các việc "ẩn".
> 💡 Kể tên việc ẩn hay bị quên (PM, review, setup môi trường, data migration, hỗ trợ UAT, sửa lỗi bảo hành) là cách nhanh nhất chứng minh kinh nghiệm.

**Q121. Work package nên nhỏ cỡ nào? Khi nào bạn dừng phân rã WBS?**
Thông lệ tham khảo là 8–80 giờ công, hoặc không dài quá một chu kỳ báo cáo (1–2 tuần) để theo dõi được tiến độ thật. Em dừng phân rã khi work package: ① estimate được với độ tin cậy chấp nhận được; ② giao được cho một người/nhóm chịu trách nhiệm; ③ có tiêu chí "xong" rõ (vd code + unit test + review đạt). Chia quá nhỏ chỉ tăng chi phí quản lý mà không thêm thông tin.

**Q122. WBS dictionary dùng để làm gì? Dự án nhỏ có cần không?**
WBS dictionary mô tả chi tiết từng work package: nội dung, deliverable, tiêu chí chấp nhận, owner, estimate, phụ thuộc, tài liệu tham chiếu. Nó tránh việc team offshore, onsite và khách hiểu khác nhau về chữ "xong". Dự án nhỏ có thể tailor thành vài cột thêm trong file WBS Excel (mô tả, tiêu chí xong, owner) thay vì tài liệu riêng.

**Q123. Scope statement khác requirement document ở điểm nào? Nên ghi gì để tránh tranh cãi về sau?**
Requirement document mô tả **cần gì** (chức năng, phi chức năng, nghiệp vụ); scope statement mô tả **dự án sẽ giao gì**: deliverable, tiêu chí chấp nhận, ràng buộc, giả định và phần **loại trừ**. Để tránh tranh cãi, em ghi rõ danh sách 対象外, các 前提条件 (vd khách cấp môi trường, dữ liệu test, trả lời Q&A trong 2 ngày làm việc) và số vòng chỉnh sửa tài liệu được tính trong giá.
> 💡 Danh sách out-of-scope và giả định là thứ cứu dự án Fixed Price khỏi tranh chấp — nhắc điều này kèm một ví dụ thật của bạn.

**Q124. Requirement Traceability Matrix (RTM) là gì và bạn dùng nó thế nào?**
RTM liên kết mỗi yêu cầu với nguồn gốc, thiết kế, module, test case, kết quả test và CR liên quan. Em dùng để: ① kiểm tra không yêu cầu nào bị bỏ sót khi test; ② phân tích tác động khi có CR (đổi yêu cầu X ảnh hưởng màn hình, API, test case nào); ③ chứng minh độ phủ khi nghiệm thu. Tiêu chí tham khảo trước UAT: 100% yêu cầu trong phạm vi có test case và kết quả pass hoặc được khách chấp nhận.

**Q125. Scope creep khác gold plating thế nào? Phòng ngừa từng loại ra sao?**
Scope creep là phạm vi phình ra **không qua kiểm soát**, thường từ khách hoặc do BA nhận thêm "tiện thể"; gold plating là **team tự làm thêm** ngoài yêu cầu để khách vui. Cả hai đều tốn effort không được trả tiền, tăng lỗi và khó nghiệm thu. Phòng ngừa: creep → mọi yêu cầu mới qua CR, đối chiếu RTM; gold plating → review và test bám spec, tiêu chí xong rõ, ý tưởng cải tiến đưa qua PM để khách chọn.
> 💡 Bẫy: khen gold plating là "tận tâm". Cách đúng là đề xuất cải tiến cho khách quyết định, không tự ý làm.

**Q126. Validate scope khác control scope và khác quality control thế nào?**
Validate scope là **khách/sponsor chính thức chấp nhận** deliverable (kết quả là accepted deliverables, vd biên bản 検収); control scope là PM **theo dõi phạm vi so với baseline** và quản lý thay đổi. Quality control là team nội bộ kiểm tra deliverable **có đúng không**, thường làm trước validate scope. Thứ tự: QC nội bộ đạt → giao → khách validate → nghiệm thu.

**Q127. Khách đưa yêu cầu mơ hồ như "màn hình dễ dùng, xử lý nhanh". Bạn biến chúng thành yêu cầu kiểm chứng được thế nào?**
Đặt câu hỏi để chuyển thành tiêu chí đo được: "nhanh" → ví dụ "tìm kiếm trả kết quả dưới 3 giây với 100.000 bản ghi, 50 user đồng thời"; "dễ dùng" → số bước tối đa cho thao tác chính, tuân thủ guideline UI của khách. Mỗi yêu cầu phi chức năng ghi vào 要件定義書 kèm cách đo và môi trường đo. Khách chưa chốt được thì em ghi thành giả định có số cụ thể để khách xác nhận hoặc sửa.

**Q128. Product scope và project scope khác nhau thế nào? Cho ví dụ.**
Product scope là đặc tính, chức năng của sản phẩm (vd hệ thống quản lý hợp đồng cho khách bảo hiểm B gồm 30 màn hình, 5 batch), đo theo yêu cầu. Project scope là toàn bộ công việc để tạo ra sản phẩm đó (thiết kế, code, test, chuyển đổi dữ liệu, đào tạo, quản lý dự án), đo theo kế hoạch dự án. Nhiều tranh chấp xảy ra vì khách mặc định data migration, đào tạo user nằm trong project scope dù proposal không ghi.

## 2.4 Tiến độ: CPM, nén lịch, PERT, critical chain

**Q129. Các bước xây dựng schedule từ WBS là gì? Sai lầm hay gặp?**
Define activities từ work package → sequence (phụ thuộc, lead/lag) → estimate durations theo effort và nguồn lực thật → develop schedule (CPM, cân bằng nguồn lực, buffer) → baseline → control. Sai lầm hay gặp: lấy effort chia số người ra duration, bỏ qua % allocation, quên ngày lễ của cả hai nước (Tết, Golden Week, Obon) và thời gian khách review tài liệu.
> 💡 Nhắc lịch lễ hai nước và thời gian review của khách là chi tiết "người làm thật" mà interviewer đánh giá cao.

**Q130. Giải thích bốn loại quan hệ phụ thuộc FS, SS, FF, SF và lead/lag bằng ví dụ phần mềm.**
FS (finish-to-start): xong thiết kế API mới code tích hợp — loại phổ biến nhất. SS: bắt đầu viết test case sau khi bắt đầu thiết kế chi tiết vài ngày (SS + lag). FF: tài liệu hướng dẫn chỉ xong khi code xong. SF hiếm: hệ thống cũ chỉ được tắt khi hệ thống mới bắt đầu chạy. Lead cho việc sau bắt đầu sớm hơn (vd FS − 3 ngày); lag là thời gian chờ bắt buộc (vd chờ khách review 5 ngày).

**Q131. Mini bài toán CPM: A(3 ngày) → B(2) → E(2) → D(2) và A → C(6) → D. Tìm critical path, total float và free float của B và E.**
Hai đường: A-B-E-D = 3+2+2+2 = 9 ngày; A-C-D = 3+6+2 = 11 ngày → critical path A-C-D, dự án 11 ngày. Forward pass: B (ES 3, EF 5), E (ES 5, EF 7), D bắt đầu sớm nhất ngày 9; backward pass: E (LS 7, LF 9), B (LS 5, LF 7). Total float B = E = 2 ngày; free float B = 0 (E bắt đầu ngay khi B xong), free float E = 9 − 7 = 2.
> 💡 Ý cần nói ra: B có total float 2 nhưng free float 0 — B trễ không làm trễ dự án nhưng ăn vào float của E.

**Q132. Float âm nghĩa là gì? Và float nên "thuộc về" ai — có nên công khai float của từng task cho team?**
Float âm xuất hiện khi mốc ràng buộc (vd go-live cố định) sớm hơn ngày kết thúc tính được: kế hoạch hiện tại **không khả thi**, phải crash, fast-track, giảm phạm vi hoặc đàm phán lại mốc. Về float, em coi đó là tài sản của dự án do PM quản lý, không chia sẵn cho từng người, vì theo luật Parkinson và "student syndrome", việc có float thường được làm muộn và tiêu hết float. Team vẫn thấy critical path, nhưng tiến độ đo theo ngày cam kết của từng task.

**Q133. Critical path có thể thay đổi trong dự án không? Bạn theo dõi nó thế nào?**
Có: khi việc ngoài critical path trễ quá float, khi crash làm đường khác dài hơn, hoặc khi thêm CR. Dự án cũng có thể có nhiều critical path song song, rủi ro cao hơn vì trễ đường nào cũng trễ dự án. Em cập nhật schedule hằng tuần, theo dõi thêm các đường near-critical (float ≤ 2–3 ngày, tham khảo) như thể chúng là critical path.

**Q134. Crashing và fast-tracking khác nhau thế nào? Rủi ro của mỗi cách trong dự án phần mềm?**
Crashing: thêm nguồn lực (người, OT) vào việc trên critical path để rút ngắn → **tăng chi phí**; rủi ro là thêm người vào dự án đang trễ có thể làm chậm hơn (luật Brooks) do onboarding và giao tiếp. Fast-tracking: làm song song các việc vốn tuần tự (vd code khi thiết kế chưa chốt hết) → **tăng rủi ro làm lại**. Chọn cách nào tùy: việc có chia nhỏ được không, người thêm vào có domain không, đầu vào đã chắc đến đâu.
> 💡 Nhắc luật Brooks và điều kiện "chỉ crash khi việc tách được và người thêm vào có sẵn context" cho thấy hiểu bản chất, không chỉ thuộc định nghĩa.

**Q135. Mini bài toán crashing: hai việc trên critical path — X: normal 10 ngày/50 triệu, crash 7 ngày/65 triệu; Y: normal 8 ngày/40 triệu, crash 6 ngày/54 triệu. Cần rút 2 ngày, crash việc nào?**
Chi phí crash mỗi ngày: X = (65 − 50)/(10 − 7) = 5 triệu/ngày; Y = (54 − 40)/(8 − 6) = 7 triệu/ngày. Chọn X: rút 2 ngày tốn thêm khoảng 10 triệu (giả định chi phí tuyến tính). Nguyên tắc: chỉ crash việc trên critical path, chọn việc có chi phí/ngày thấp nhất, rút từng ngày và tính lại critical path sau mỗi bước vì đường khác có thể trở thành critical.
> 💡 Câu hỏi chéo hay gặp: "crash việc ngoài critical path có rút ngắn dự án không?" — không, chỉ tốn thêm tiền.

**Q136. PERT ba điểm: O = 4, M = 6, P = 14 ngày. Tính expected duration, độ lệch chuẩn và giải thích ý nghĩa.**
Beta/PERT: E = (O + 4M + P)/6 = (4 + 24 + 14)/6 = 7 ngày; σ = (P − O)/6 = 10/6 ≈ 1,67 ngày. Khoảng ±1σ (≈ 68%) là 5,3–8,7 ngày, ±2σ (≈ 95%) là 3,7–10,3 ngày; nếu dùng phân phối tam giác: (4 + 6 + 14)/3 = 8 ngày. Ý nghĩa: estimate là một khoảng, nên em cam kết với khách theo mức tin cậy (vd 85–90%), không theo giá trị most likely.
> 💡 Chỉ ra rằng P lệch xa (14 so với 6) kéo E lên trên M — và vì sao estimate phần mềm thường lệch về phía trễ — là điểm cộng.

**Q137. Critical chain method khác CPM ở điểm nào?**
CPM tính theo phụ thuộc công việc, ngầm giả định nguồn lực không giới hạn; critical chain tính cả **ràng buộc nguồn lực** (vd chỉ có 1 tech lead review). Critical chain cắt phần đệm an toàn trong từng task (estimate ở mức ~50% tin cậy), gom thành **project buffer** cuối chuỗi và **feeding buffer** tại chỗ nhánh phụ nhập vào chuỗi chính. PM theo dõi tốc độ tiêu buffer so với % hoàn thành (fever chart): buffer tiêu nhanh hơn tiến độ thì hành động.

**Q138. Resource leveling và resource smoothing khác nhau thế nào?**
Leveling điều chỉnh lịch để không ai bị phân bổ quá công suất, **có thể làm đổi critical path và kéo dài ngày kết thúc**. Smoothing chỉ dời việc **trong phạm vi float**, không đổi ngày kết thúc, nên có thể không xử lý hết quá tải. Ví dụ: tech lead vừa review code vừa thiết kế module mới, tải 150% → smoothing dời việc còn float; nếu không đủ, leveling dời thiết kế 1 tuần (dự án trễ) hoặc phải thêm người review.

**Q139. Milestone là gì? Bạn đặt milestone thế nào cho dự án outsourcing với khách Nhật?**
Milestone là mốc không có duration, đánh dấu sự kiện quan trọng (xong pha, giao hàng, nghiệm thu). Em đặt milestone gắn với **deliverable kiểm chứng được** và lịch nghiệm thu/thanh toán: chốt 要件定義, duyệt thiết kế, code complete, xong integration test, bắt đầu UAT, go-live. Milestone đưa vào báo cáo tuần dạng kế hoạch–thực tế, và báo khách ngay khi dự báo lệch mốc đã cam kết, vd lệch > 1 ngày (tham khảo).

## 2.5 Chi phí & EVM

**Q140. Quản lý chi phí của PM outsourcing gồm những gì?**
Plan cost management → estimate costs → determine budget (cost baseline) → control costs. Trong outsourcing, chi phí chủ yếu là 工数 nhân sự (theo 人月 (ningetsu – man-month) và đơn giá nội bộ từng level), cộng chi phí onsite, license, hạ tầng, đi lại. PM làm 予実管理 (yojitsu kanri – quản lý kế hoạch so với thực tế) hằng tuần: so effort thực tế với kế hoạch theo từng work package để thấy sớm phần nào đang "đốt" ngân sách.

**Q141. Cost baseline, contingency reserve và management reserve khác nhau thế nào?**
Cost baseline = tổng estimate các work package + **contingency reserve** (dự phòng cho rủi ro đã nhận diện — known-unknowns), phân bổ theo thời gian, PM dùng theo risk plan. **Management reserve** dành cho unknown-unknowns, **không nằm trong cost baseline** nhưng nằm trong tổng ngân sách (project budget = cost baseline + MR); dùng phải được sponsor/lãnh đạo duyệt, khi dùng thì cost baseline được cập nhật. EVM đo theo cost baseline, không tính MR.
> 💡 Bẫy kinh điển trong đề PMP: MR không thuộc cost baseline và PM không được tự ý dùng.

**Q142. Giải thích PV, EV, AC bằng ngôn ngữ đơn giản cho người không làm PM.**
PV (planned value): **lẽ ra** đến hôm nay phải làm xong bao nhiêu việc, quy theo ngân sách kế hoạch. EV (earned value): **thực tế** đã làm xong bao nhiêu việc, cũng quy theo ngân sách kế hoạch. AC (actual cost): **thực tế** đã tiêu bao nhiêu. So EV với PV biết nhanh hay chậm; so EV với AC biết tiết kiệm hay lố. EV là chìa khóa vì nó đo giá trị đã tạo ra, không phải số tiền đã tiêu.

**Q143. Nêu công thức CV, SV, CPI, SPI và cách đọc dấu/giá trị.**
CV = EV − AC, SV = EV − PV: âm là xấu (lố chi phí/chậm tiến độ), dương là tốt. CPI = EV/AC, SPI = EV/PV: < 1 là xấu, > 1 là tốt; vd CPI 0,8 nghĩa là mỗi 1 đồng bỏ ra chỉ tạo được 0,8 đồng giá trị. Mẹo nhớ: luôn bắt đầu bằng EV; "C" (cost) đi với AC, "S" (schedule) đi với PV.

**Q144. Mini bài toán: BAC = 100.000 USD, kế hoạch 10 tuần chia đều. Cuối tuần 4 hoàn thành 35% công việc, đã chi 42.000 USD. Tính PV, EV, AC, CV, SV, CPI, SPI.**
PV = 40% × 100.000 = 40.000; EV = 35% × 100.000 = 35.000; AC = 42.000. CV = 35.000 − 42.000 = −7.000; SV = 35.000 − 40.000 = −5.000. CPI = 35/42 ≈ 0,83; SPI = 35/40 = 0,875. Kết luận: dự án vừa **lố chi phí** vừa **chậm tiến độ**; mỗi 1 USD bỏ ra chỉ tạo ra khoảng 0,83 USD giá trị.

**Q145. Tiếp bài Q144: tính EAC, ETC, VAC với giả định hiệu suất chi phí hiện tại tiếp diễn.**
EAC = BAC/CPI = 100.000/(35/42) = 120.000; ETC = EAC − AC = 120.000 − 42.000 = 78.000; VAC = BAC − EAC = −20.000. Nghĩa là nếu không thay đổi gì, dự án sẽ vượt 20% ngân sách. Khi báo cáo, em đưa kèm nguyên nhân (vd estimate module X thiếu, rework do yêu cầu đổi) và phương án kéo CPI lên, thay vì chỉ báo con số.

**Q146. Có những công thức EAC nào và khi nào dùng từng công thức?**
① EAC = AC + bottom-up ETC: khi estimate ban đầu sai căn bản, phải ước lại phần còn lại. ② EAC = AC + (BAC − EV): khi độ lệch là **bất thường**, phần còn lại sẽ chạy đúng kế hoạch. ③ EAC = BAC/CPI: khi hiệu suất chi phí hiện tại sẽ **tiếp diễn**. ④ EAC = AC + (BAC − EV)/(CPI × SPI): khi cả chi phí lẫn tiến độ cùng tác động (vd phải đuổi deadline cố định). Với số Q144: ② = 107.000, ③ = 120.000, ④ ≈ 131.100 USD.
> 💡 Trình bày một dải EAC (lạc quan–bi quan) cho sponsor thay vì một con số duy nhất giúp ra quyết định tốt hơn và thể hiện tư duy senior.

**Q147. TCPI là gì? Tính TCPI cho bài Q144 và diễn giải.**
TCPI (to-complete performance index) là hiệu suất chi phí **cần đạt** cho phần việc còn lại để về đích đúng mục tiêu: TCPI = (BAC − EV)/(BAC − AC) nếu giữ BAC, hoặc (BAC − EV)/(EAC − AC) nếu theo EAC mới. Bài Q144: (100.000 − 35.000)/(100.000 − 42.000) = 65/58 ≈ 1,12. CPI hiện tại chỉ 0,83 mà phải nhảy lên 1,12 là rất khó; kinh nghiệm tham khảo: TCPI cao hơn CPI quá ~0,1 thì coi BAC không còn khả thi và trình EAC mới.

**Q148. Mini bài toán theo 人月: BAC = 50 MM. Sau 3 tháng: PV = 30 MM, EV = 24 MM, AC = 32 MM. Đánh giá và đề xuất.**
CPI = 24/32 = 0,75; SPI = 24/30 = 0,8; EAC = 50/0,75 ≈ 66,7 MM (vượt ~16,7 MM); TCPI = (50 − 24)/(50 − 32) = 26/18 ≈ 1,44 — gần như không thể đạt. Đề xuất: ① phân tích nguyên nhân (estimate thiếu, rework, năng suất người mới); ② phần thay đổi chưa tính tiền thì đưa vào CR với khách; ③ trình lãnh đạo EAC mới và phương án giảm lỗ (đổi cơ cấu team, dừng gold plating); ④ ghi bài học để hiệu chỉnh hệ số estimate cho dự án sau.

**Q149. Đo EV cho task phần mềm thế nào để tránh "hội chứng 90%"?**
"Hội chứng 90%" là task báo 90% rất lâu vì % do người làm tự ước. Em dùng quy tắc đo khách quan: 0/100 (chỉ ghi nhận khi xong hẳn, cho task ngắn hơn một chu kỳ báo cáo), 50/50 hoặc 20/80 (ghi một phần khi bắt đầu, phần còn lại khi xong), hoặc weighted milestone (thiết kế 20% – code 50% – review/test 30%). Ví dụ: A 10 MM đã xong, B 20 MM đang làm (50/50), C 10 MM chưa bắt đầu → EV = 10 + 10 = 20 MM.

**Q150. CPI > 1 nhưng SPI < 1 nói lên điều gì? Và trường hợp ngược lại?**
CPI > 1, SPI < 1: tiêu ít hơn giá trị làm được nhưng chậm hơn kế hoạch — thường do **nguồn lực chưa vào đủ** như kế hoạch; còn dư địa chi phí để bổ sung người. CPI < 1, SPI > 1: nhanh nhưng tốn — thường do **OT, đổ thêm người** để kịp; cần xem có bền vững không và OT có ăn vào margin không. Luôn soi thêm chất lượng: chỉ số đẹp mà bug tăng là tín hiệu giả.
> 💡 Câu này kiểm tra khả năng đọc chỉ số kết hợp — nêu giả thuyết nguyên nhân kèm cách kiểm chứng là đủ ghi điểm.

**Q151. Hạn chế của SPI ở giai đoạn cuối dự án là gì?**
Khi dự án xong, EV = BAC = tổng PV nên SPI luôn tiến về 1 (SV về 0) dù thực tế dự án trễ nhiều tuần. Ngoài ra SPI đo theo giá trị, không theo critical path: làm nhiều việc không quan trọng vẫn có SPI đẹp trong khi critical path đang trễ. Khắc phục: theo dõi song song critical path và milestone, có thể dùng Earned Schedule để đo tiến độ theo đơn vị thời gian.

**Q152. Với dự án Fixed Price cho khách Nhật, EVM còn ý nghĩa gì khi khách không quan tâm chi phí nội bộ của mình?**
Với FP, khách trả giá cố định nên chi phí vượt là **lỗ của chính công ty mình**; EVM nội bộ là công cụ bảo vệ margin. Em theo dõi 原価 (genka – chi phí gốc) theo effort thực tế × đơn giá nội bộ, dùng CPI để dự báo lợi nhuận, SPI và milestone để báo khách. Báo cáo cho khách chỉ gồm tiến độ, chất lượng; báo cáo nội bộ thêm EAC, margin dự kiến và các CR chưa thu tiền.

**Q153. Cost baseline phân bổ theo thời gian có dạng "S-curve". Bạn dùng S-curve để làm gì?**
S-curve là đường PV lũy kế theo thời gian, thường dốc nhất ở giữa dự án khi nhân sự đông nhất. Vẽ chung PV, EV, AC trên một biểu đồ là cách 見える化 (mieruka – trực quan hóa) xu hướng: EV dưới PV là chậm, AC trên EV là lố. Em dùng nó trong báo cáo nội bộ hằng tháng và review dự án với lãnh đạo; nó cũng giúp lập kế hoạch dòng tiền và kế hoạch điều phối nhân sự.

## 2.6 Quản lý rủi ro

**Q154. Risk khác issue thế nào? Cho ví dụ cùng một chủ đề.**
Risk là sự kiện **chưa xảy ra, không chắc chắn**, tác động tích cực hoặc tiêu cực; issue là sự việc **đã xảy ra**, phải xử lý. Ví dụ: "Tech lead có thể nghỉ việc giữa dự án" là risk (theo dõi trong risk register, có kế hoạch giảm thiểu); "Tech lead đã nộp đơn nghỉ" là issue (vào 課題管理表 (kadai kanrihyou – bảng quản lý vấn đề), có người xử lý và hạn xử lý). Risk xảy ra thì chuyển thành issue và kích hoạt kế hoạch ứng phó đã chuẩn bị.

**Q155. Risk register gồm những cột gì?**
Tối thiểu: ID, mô tả theo cấu trúc **nguyên nhân – sự kiện – tác động** ("Do khách chưa chốt API của ngân hàng A, tích hợp có thể trễ, dẫn tới UAT trễ 2 tuần"), category, probability, impact, điểm ưu tiên, trigger, chiến lược ứng phó, hành động cụ thể + hạn, risk owner, trạng thái, residual risk. Em review register hằng tuần trong họp nội bộ và đưa top rủi ro vào 進捗報告 (shinchoku houkoku – báo cáo tiến độ) gửi khách.
> 💡 Viết rủi ro theo mẫu "nguyên nhân – sự kiện – tác động" giúp phân biệt với lo lắng chung chung kiểu "rủi ro về tiến độ".

**Q156. Đánh giá rủi ro định tính và định lượng khác nhau thế nào? Khi nào cần định lượng?**
Định tính: chấm probability × impact theo thang (vd 1–5) trên ma trận để xếp ưu tiên — nhanh, dùng cho mọi dự án. Định lượng: quy ra số tiền/ngày cụ thể bằng EMV, decision tree, mô phỏng Monte Carlo cho tiến độ — dùng cho dự án lớn, FP rủi ro cao hoặc khi phải quyết định dự phòng bao nhiêu. Thực tế em đánh giá định tính toàn bộ, định lượng cho top 5–10 rủi ro chạm tới hợp đồng hoặc milestone.

**Q157. Tính EMV: rủi ro A xác suất 30%, tác động −50 triệu; rủi ro B xác suất 10%, tác động −200 triệu; cơ hội C xác suất 20%, tác động +40 triệu. Dùng kết quả thế nào?**
EMV = xác suất × tác động: A = −15 triệu, B = −20 triệu, C = +8 triệu; tổng = −27 triệu. Con số này là cơ sở đặt contingency reserve cho các rủi ro đã nhận diện (khoảng 27 triệu, cộng biên an toàn tùy chính sách). B xác suất thấp nhưng EMV lớn nhất — đáng đầu tư giảm thiểu nếu chi phí giảm thiểu nhỏ hơn phần EMV giảm được.

**Q158. Decision tree: tự phát triển module (200 triệu, 40% khả năng phát sinh thêm 100 triệu) hay mua package (230 triệu, 10% khả năng tốn thêm 50 triệu tùy biến)?**
Tự làm: 200 + 0,4 × 100 = 240 triệu. Mua: 230 + 0,1 × 50 = 235 triệu. Theo EMV, mua rẻ hơn 5 triệu, nhưng chênh lệch nhỏ nên phải xét thêm yếu tố phi tiền tệ: phụ thuộc nhà cung cấp, license dài hạn, mức tùy biến, yêu cầu bảo mật của khách tài chính. Decision tree giúp định lượng, không thay thế phán đoán.

**Q159. Năm chiến lược ứng phó rủi ro tiêu cực là gì? Cho ví dụ trong dự án phần mềm.**
**Avoid**: loại bỏ nguyên nhân, vd không dùng thư viện chưa ổn định. **Transfer**: chuyển tác động cho bên thứ ba, vd thuê nhà cung cấp hạ tầng có cam kết SLA và điều khoản bồi thường. **Mitigate**: giảm xác suất/tác động, vd làm PoC tích hợp sớm, cho 2 người cùng nắm module chủ chốt. **Accept**: chấp nhận chủ động (có contingency) hoặc bị động. **Escalate**: rủi ro vượt thẩm quyền/phạm vi dự án thì chuyển lên cấp phù hợp, vd chính sách nhân sự toàn công ty.

**Q160. Chiến lược cho cơ hội (positive risk): exploit, enhance, share khác nhau thế nào?**
**Exploit**: làm cho cơ hội chắc chắn xảy ra, vd giao người giỏi nhất để xong sớm và nhận thưởng giao sớm. **Enhance**: tăng xác suất/tác động, vd tái sử dụng framework nội bộ để giảm effort. **Share**: chia cơ hội với bên nắm bắt tốt hơn, vd liên kết với đối tác cloud. Ngoài ra còn escalate và accept. Trong outsourcing, cơ hội hay bị bỏ quên trong register; em luôn ghi vài dòng như mở rộng phạm vi giai đoạn sau, tái sử dụng component.
> 💡 Có cơ hội trong risk register cho thấy tư duy tạo giá trị và doanh thu — đúng điều công ty outsourcing cần ở Senior PM.

**Q161. Trigger và risk owner là gì? Vì sao risk owner không nên luôn là PM?**
Trigger là dấu hiệu cảnh báo rủi ro sắp hoặc đã xảy ra, vd "khách trả lời Q&A trễ quá 3 ngày" là trigger của rủi ro trễ thiết kế. Risk owner theo dõi trigger và thực thi kế hoạch ứng phó. PM chịu trách nhiệm cả quy trình, nhưng owner nên là người gần nguồn rủi ro nhất: rủi ro kỹ thuật → tech lead, rủi ro môi trường phía khách → onsite/BrSE, rủi ro nhân sự → line manager. Như vậy phản ứng nhanh hơn và PM không thành điểm nghẽn.

**Q162. Secondary risk và residual risk khác nhau thế nào?**
Residual risk là phần rủi ro **còn lại** sau khi đã ứng phó (vd làm PoC rồi vẫn còn khả năng API của khách thay đổi) — cần contingency hoặc chấp nhận. Secondary risk là rủi ro **mới sinh ra** từ chính biện pháp ứng phó (vd thêm 3 người mới để giảm rủi ro trễ → phát sinh rủi ro chất lượng vì người mới chưa nắm nghiệp vụ). Cả hai đều phải ghi vào register, không coi rủi ro "đã xử lý" là hết.

**Q163. Contingency plan, fallback plan và workaround khác nhau thế nào?**
Contingency plan là kế hoạch **chuẩn bị trước**, kích hoạt khi trigger xảy ra; fallback plan là phương án **dự phòng thứ hai** khi contingency không hiệu quả. Workaround là cách xử lý **không có kế hoạch trước**, cho rủi ro chưa nhận diện hoặc đã chấp nhận bị động. Ví dụ go-live: contingency = rollback theo kịch bản đã diễn tập; fallback = chạy song song hệ thống cũ thêm 1 tuần; workaround = nhập liệu tay tạm thời cho một batch lỗi không lường trước.

**Q164. Làm sao nhận diện rủi ro hiệu quả ở đầu dự án outsourcing cho khách tài chính Nhật?**
Kết hợp: ① checklist từ lessons learned dự án cũ (khách mới, công nghệ mới, team mới, yêu cầu chưa chốt, phụ thuộc bên thứ ba); ② workshop với tech lead, BrSE, QA; ③ phân tích giả định và ràng buộc trong proposal — giả định nào có thể sai thì thành rủi ro; ④ hỏi khách rủi ro phía họ (lịch release hệ thống lõi, quy định bảo mật, audit). Với khách tài chính, chú ý thêm bảo mật dữ liệu, phê duyệt nhiều tầng và môi trường test bị giới hạn truy cập.
> 💡 Nói được "giả định sai chính là rủi ro" (assumption analysis) là cầu nối đẹp giữa proposal và quản lý rủi ro.

## 2.7 Stakeholder & giao tiếp

**Q165. Bạn nhận diện và phân tích stakeholder thế nào? Power/interest grid dùng ra sao?**
Nguồn đầu tiên là 体制図 (taiseizu – sơ đồ tổ chức dự án) của hai bên; liệt kê cả phía khách (sponsor, IT, người dùng nghiệp vụ, bảo mật/audit), phía mình (lãnh đạo, line manager, onsite, team, QA) và bên thứ ba. Xếp vào lưới: power cao–interest cao → **manage closely**; power cao–interest thấp → **keep satisfied**; power thấp–interest cao → **keep informed**; thấp–thấp → **monitor**. Kết quả là stakeholder register có chiến lược riêng cho từng nhóm.

**Q166. Stakeholder engagement assessment matrix là gì?**
Ma trận so sánh mức tham gia **hiện tại (C)** và **mong muốn (D)** của từng stakeholder theo 5 mức: unaware, resistant, neutral, supportive, leading. Khoảng cách C–D chỉ ra hành động cần làm: vd trưởng phòng nghiệp vụ của khách đang resistant vì sợ hệ thống mới tăng việc, mong muốn supportive → demo sớm, mời review màn hình, chỉ ra lợi ích cụ thể cho bộ phận họ. Em cập nhật ma trận ở mỗi milestone.

**Q167. RACI là gì? Lỗi phổ biến khi lập RACI?**
RACI xác định cho mỗi hoạt động/deliverable: Responsible (người làm), Accountable (chịu trách nhiệm cuối, duyệt), Consulted (được hỏi ý kiến), Informed (được thông báo). Lỗi phổ biến: nhiều A cho một việc (rốt cuộc không ai chịu trách nhiệm), không có R, quá nhiều C làm chậm quyết định, lập xong không ai dùng. Ví dụ tài liệu 要件定義書: R = BrSE/BA, A = PM, C = người dùng nghiệp vụ của khách, I = team dev.
> 💡 Quy tắc hay bị hỏi lại: mỗi việc có đúng một A.

**Q168. Số kênh giao tiếp tính thế nào? Team đang 10 người, thêm 5 người thì tăng bao nhiêu kênh?**
Công thức n(n − 1)/2. 10 người: 10 × 9/2 = 45 kênh; 15 người: 15 × 14/2 = 105 kênh; tăng 60 kênh. Ý nghĩa thực tế: số kênh tăng gần theo bình phương, nên team lớn phải chia nhóm nhỏ có lead, chuẩn hóa ai báo ai qua công cụ gì, và hạn chế họp toàn đội. Đây cũng là lý do thêm người không làm năng suất tăng tuyến tính.
> 💡 Đề PMP hay hỏi "tăng thêm bao nhiêu kênh" — phải lấy hai kết quả trừ nhau, đừng dừng ở một con số.

**Q169. Communication management plan gồm những gì?**
Trả lời: ai cần thông tin gì, khi nào, qua kênh nào, định dạng và ngôn ngữ nào, ai gửi, mức chi tiết. Ví dụ: báo cáo tuần bằng tiếng Nhật gửi khách thứ Sáu; họp định kỳ 30 phút/tuần có 議事録 (gijiroku – biên bản họp) gửi trong 24 giờ; báo cáo tháng nội bộ cho lãnh đạo; quy tắc escalation theo mức nghiêm trọng (vd sự cố nghiêm trọng báo khách trong 1 giờ — tham khảo). Plan gắn với stakeholder register để mỗi nhóm nhận đúng mức thông tin.

**Q170. Push, pull và interactive communication khác nhau thế nào? Khi nào dùng từng loại?**
Interactive (họp, gọi) hiệu quả nhất cho vấn đề phức tạp, cần quyết định hoặc nhạy cảm như thông báo trễ tiến độ. Push (email, báo cáo gửi đi) cho thông tin cần đến đúng người nhưng không cần phản hồi ngay. Pull (wiki, dashboard, công cụ quản lý ticket) cho thông tin nhiều người tự tra cứu khi cần. Với khách Nhật, tin xấu nên báo bằng interactive trước, rồi gửi email xác nhận bằng văn bản để lưu vết.

**Q171. Một status report tốt gửi khách gồm những gì?**
Trạng thái tổng (xanh/vàng/đỏ có tiêu chí rõ), tiến độ theo milestone và % hoàn thành có cơ sở đo, chỉ số chất lượng (số bug, mật độ bug), top rủi ro và issue cần khách hỗ trợ kèm hạn trả lời, CR, kế hoạch tuần tới. Nguyên tắc: kết luận trước, chi tiết sau; số liệu thay tính từ; luôn có mục "cần khách quyết định gì". Báo cáo đỏ không bao giờ là bất ngờ — khách đã được báo miệng trước.
> 💡 Định nghĩa tiêu chí màu (vd vàng: dự báo trễ milestone ≤ 3 ngày, còn kiểm soát được; đỏ: trễ hơn hoặc cần khách quyết định) để tránh báo cáo "dưa hấu" — ngoài xanh trong đỏ.

**Q172. Làm thế nào quản lý stakeholder quyền lực cao nhưng ít quan tâm (nhóm keep satisfied)?**
Họ ít đọc báo cáo chi tiết nhưng có thể can thiệp bất ngờ, vd giám đốc khối của khách dừng dự án ngay tại buổi review. Cách làm: gửi tóm tắt 1 trang theo tháng/milestone, tập trung vào lợi ích và quyết định cần họ; mời vào các buổi demo quan trọng; qua sponsor trao đổi trước các quyết định lớn theo kiểu 根回し (nemawashi – vận động, thống nhất trước) thay vì đưa thẳng vào cuộc họp lớn. Mục tiêu: họ không bao giờ bị bất ngờ.

**Q173. Một stakeholder phía khách liên tục phản đối thiết kế đã được duyệt. Bạn tiếp cận thế nào?**
① Tìm nguyên nhân thật qua trao đổi riêng (sợ mất quyền, bị bỏ qua lúc lấy yêu cầu, hay có nhu cầu nghiệp vụ chưa được hiểu); ② cập nhật engagement matrix và trao đổi với sponsor; ③ điểm nào hợp lý thì đưa vào CR có đánh giá tác động, điểm nào không thì để sponsor phía khách quyết định dựa trên dữ liệu; ④ phòng ngừa: mời họ vào review sớm ở các pha sau. PM không tranh luận đúng sai với khách mà tạo cơ chế để khách tự quyết.

**Q174. Dự án có onsite ở Nhật và offshore ở Đà Nẵng: bạn tổ chức luồng giao tiếp ra sao?**
Thiết kế luồng một cửa: khách ↔ onsite/BrSE ↔ PM/team offshore, kèm quy tắc khi nào được trao đổi trực tiếp (vd dev giải thích kỹ thuật thì cc BrSE). Có một nơi duy nhất lưu Q&A表 (Q&A hyou – bảng hỏi đáp), quyết định và tài liệu; họp ngắn onsite–offshore hằng ngày, tận dụng chênh lệch 2 giờ (Nhật sớm hơn Việt Nam). PM theo dõi số Q&A quá hạn và thời gian trả lời trung bình để phát hiện nghẽn.

## 2.8 Procurement & loại hợp đồng (góc nhìn quốc tế)

**Q175. So sánh hợp đồng Fixed Price (FP) và Time & Material (T&M) từ góc độ rủi ro.**
FP: giá cố định cho phạm vi xác định — rủi ro chi phí **nằm ở bên cung cấp**, khách dễ dự toán; hợp khi yêu cầu rõ và ổn định. T&M: khách trả theo effort thực tế × đơn giá — rủi ro chi phí **nằm ở bên mua**, linh hoạt khi yêu cầu chưa rõ. Với vendor, FP có thể lãi cao nếu estimate tốt nhưng lỗ nặng nếu phạm vi trôi; T&M margin ổn định hơn nhưng khách đòi minh bạch effort và năng suất.

**Q176. Hợp đồng cost-reimbursable (CPFF, CPIF, CPAF) là gì? Có gặp trong outsourcing phần mềm không?**
Bên mua trả chi phí thực tế hợp lệ cộng phí: CPFF (cost plus fixed fee) — phí cố định; CPIF (cost plus incentive fee) — phí thưởng theo mục tiêu, phần tiết kiệm/vượt chia theo tỷ lệ; CPAF (cost plus award fee) — thưởng theo đánh giá của bên mua. Dạng thuần túy hiếm gặp trong outsourcing phần mềm thương mại, nhưng tinh thần "chia sẻ rủi ro, thưởng theo mục tiêu" xuất hiện trong T&M có trần hoặc thưởng khi giao sớm, đạt chất lượng.

**Q177. Hợp đồng FPIF (fixed price incentive fee) tính thế nào? Cho mini ví dụ.**
FPIF có target cost, target profit, tỷ lệ chia (share ratio) và ceiling price. Ví dụ: target cost 100, target profit 10, share 80/20 (bên mua/bên bán), ceiling 120. Actual cost 90: tiết kiệm 10, bên bán hưởng 20% = 2 → profit 12, giá 102. Actual cost 110: vượt 10, bên bán chịu 2 → profit 8, giá 118 (dưới ceiling). Chi phí đẩy giá vượt ceiling thì bên bán tự chịu toàn bộ phần vượt.

**Q178. Make-or-buy analysis là gì? Ngoài chi phí, bạn cân nhắc những yếu tố nào?**
Make-or-buy quyết định tự làm hay mua/thuê ngoài một phần dự án (module, dịch vụ, nhân sự). Ngoài tổng chi phí sở hữu, em xét: năng lực cốt lõi (phần tạo lợi thế thì giữ), thời gian, kiểm soát chất lượng và IP, bảo mật dữ liệu, tải nguồn lực hiện có, rủi ro phụ thuộc. Hợp đồng với khách Nhật thường yêu cầu xin phép trước khi 再委託 (saiitaku – giao lại cho bên thứ ba), nên phải xử lý điều này trước khi chọn "buy".

**Q179. Quy trình procurement gồm những bước chính nào, và vì sao PM phía vendor cũng cần hiểu?**
Plan procurement (mua gì, loại hợp đồng, tiêu chí chọn) → conduct procurement (gửi RFI/RFQ/RFP, chấm đề xuất theo tiêu chí có trọng số, đàm phán, ký) → control procurement (theo dõi hiệu suất nhà cung cấp, thanh toán theo nghiệm thu, xử lý claim, đóng hợp đồng). PM ở công ty outsourcing thường đứng ở phía "được mua": hiểu quy trình này giúp viết proposal bám tiêu chí chấm và đoán trước những gì khách sẽ kiểm soát.

**Q180. RFI, RFQ, RFP khác nhau thế nào? Khi nhận RFP, bạn đọc gì đầu tiên?**
RFI: hỏi thông tin năng lực để sàng lọc; RFQ: xin báo giá khi yêu cầu đã rõ, chủ yếu so giá; RFP: xin đề xuất giải pháp kèm giá cho bài toán phức tạp. Khi nhận RFP, tiếng Nhật là 提案依頼書 (teian iraisho – thư yêu cầu đề xuất), em đọc trước tiêu chí đánh giá và trọng số, phạm vi, ràng buộc (deadline, công nghệ, bảo mật), hình thức hợp đồng, rồi lập danh sách câu hỏi làm rõ gửi khách trong hạn hỏi đáp.
> 💡 Nhiều proposal thua vì trình bày theo ý mình thay vì bám tiêu chí chấm của RFP — nói ra điều này cho thấy kinh nghiệm presales.

**Q181. Khi nào nên chọn T&M có trần (not-to-exceed) hoặc mô hình lai thay vì FP thuần?**
Khi yêu cầu chưa rõ hoàn toàn nhưng khách cần kiểm soát ngân sách: T&M có trần cho phép linh hoạt mà khách vẫn có giới hạn chi. Mô hình lai phổ biến: giai đoạn đầu (làm rõ yêu cầu, PoC) theo T&M, khi yêu cầu đã chốt thì chuyển phần phát triển sang FP. Cách này giảm rủi ro estimate sai cho vendor và giảm rủi ro "trả tiền không giới hạn" cho khách.

**Q182. Bạn quản lý một đối tác phụ (subcontractor) cung cấp nhân sự hoặc module cho dự án như thế nào?**
Hợp đồng với đối tác phải phản ánh cam kết với khách theo kiểu back-to-back: phạm vi, tiêu chuẩn chất lượng, bảo mật, NDA, mốc giao. Khi thực hiện: đưa đối tác vào cùng quy trình (coding convention, review, báo cáo tuần), đo bằng chỉ số rõ (đúng hạn, mật độ bug, tỷ lệ review không đạt), nghiệm thu từng phần trước khi tích hợp. Với khách, mình vẫn chịu trách nhiệm cuối cùng — không thể nói "lỗi do đối tác".
> 💡 Từ khóa "back-to-back" và "trách nhiệm cuối cùng vẫn là của mình" thể hiện đúng tinh thần chịu trách nhiệm cao nhất mà JD yêu cầu.

## 2.9 Đóng dự án, lessons learned & đo thành công

**Q183. Các hoạt động chính khi đóng dự án (hoặc đóng một pha) là gì?**
① Xác nhận nghiệm thu chính thức tất cả deliverable (biên bản 検収 có chữ ký); ② bàn giao tài liệu, source, tài khoản, kiến thức cho khách/team vận hành; ③ đóng hợp đồng: đối chiếu CR, thanh toán, nghĩa vụ bảo hành; ④ giải phóng nguồn lực kèm đánh giá thành viên; ⑤ lessons learned và 完了報告書 (kanryou houkokusho – báo cáo hoàn thành); ⑥ lưu trữ hồ sơ. Dự án bị hủy giữa chừng cũng phải đóng theo quy trình này.
> 💡 Nhắc "dự án hủy cũng phải đóng chính thức" — đề PMP hay bẫy đúng điểm này.

**Q184. Lessons learned nên thu thập khi nào và làm sao để chúng thực sự được dùng lại?**
Thu thập **suốt dự án** (cuối mỗi pha/milestone, ngay sau sự cố), không đợi cuối dự án khi người đã quên hoặc đã rời đi. Mỗi bài học ghi theo dạng: bối cảnh – chuyện gì xảy ra – nguyên nhân gốc – hành động đề xuất – áp dụng cho ai. Để dùng lại: đưa vào kho lessons learned của tổ chức, cập nhật checklist rủi ro, hệ số estimate, template và 横展開 (yokotenkai – nhân rộng sang dự án khác); khi mở dự án mới, bắt buộc đọc bài học của dự án tương tự.

**Q185. Ngoài tam giác sắt (phạm vi–thời gian–chi phí), bạn đo thành công dự án bằng gì?**
Thêm: chất lượng (mật độ bug sau release, số sự cố production trong thời gian bảo hành), sự hài lòng của khách (khảo sát, khách có gia hạn hoặc mở rộng hợp đồng không), margin thực tế so với kế hoạch, sức khỏe team (nghỉ việc, OT, mức hài lòng) và lợi ích kinh doanh khách đạt được khi dùng hệ thống. Dự án đúng hạn, đúng ngân sách nhưng khách không ký tiếp hoặc team kiệt sức thì chưa thể gọi là thành công.
> 💡 Câu trả lời senior nhấn vào "khách ký tiếp hợp đồng" — chỉ số kinh doanh mà công ty outsourcing thực sự quan tâm.

**Q186. Benefits realization là gì? PM phía vendor có trách nhiệm gì với lợi ích sau dự án?**
Benefits realization là đảm bảo lợi ích kinh doanh dự kiến trong business case (vd minh họa: giảm 30% thời gian xử lý hồ sơ bảo hiểm) thực sự đạt được, thường đo sau khi dự án đóng. Trách nhiệm chính thuộc sponsor/khách, nhưng PM vendor nên hiểu mục tiêu kinh doanh từ đầu để ưu tiên đúng, đề xuất chỉ số đo, và sau go-live hỏi lại khách về kết quả. Đây cũng là cơ sở tự nhiên để đề xuất giai đoạn tiếp theo.

**Q187. Business case và benefits management plan khác project charter thế nào?**
Business case trả lời "**vì sao** đáng đầu tư": vấn đề, các phương án, chi phí–lợi ích, rủi ro; benefits management plan mô tả **lợi ích nào, đo thế nào, khi nào, ai chịu trách nhiệm**. Hai tài liệu này thường có trước dự án và là đầu vào của charter; charter thì chính thức khởi động dự án và trao quyền cho PM. Khi bối cảnh đổi khiến business case không còn hợp lý, dự án nên được xem xét dừng.

**Q188. NPV, IRR, payback period dùng thế nào khi chọn dự án? Nếu chúng mâu thuẫn thì sao?**
NPV: giá trị hiện tại ròng của dòng tiền — dương mới đáng làm, càng lớn càng tốt. IRR: lãi suất làm NPV = 0 — càng cao càng tốt. Payback: thời gian hoàn vốn — càng ngắn càng ít rủi ro. Khi mâu thuẫn, ưu tiên NPV vì phản ánh trực tiếp giá trị tạo thêm. Hai khái niệm đi kèm: opportunity cost là giá trị của phương án tốt nhất bị bỏ qua; sunk cost (chi phí đã bỏ ra) không được dùng để quyết định.
> 💡 Bẫy kinh điển: lấy sunk cost biện minh tiếp tục dự án ("đã tốn 2 tỷ rồi") — PM chỉ nhìn chi phí và lợi ích phía trước.

**Q189. Bạn tổ chức buổi lessons learned cuối dự án với khách Nhật thế nào để không thành buổi đổ lỗi?**
Chuẩn bị dữ liệu trước (timeline sự kiện, chỉ số tiến độ, bug, CR) để thảo luận theo fact; đặt quy tắc "bàn về quy trình, không bàn về cá nhân"; dùng khung KPT (Keep–Problem–Try) quen thuộc ở Nhật. Làm nội bộ trước để team nói thẳng, sau đó làm với khách dưới dạng 振り返り (furikaeri – nhìn lại) có danh sách hành động cụ thể cho giai đoạn sau. Sự cố lớn thì gửi kèm biện pháp 再発防止 (saihatsu boushi – phòng ngừa tái phát).

**Q190. Dự án bị dừng giữa chừng vì khách cắt ngân sách. PM cần làm gì?**
① Xin xác nhận quyết định dừng và ngày hiệu lực bằng văn bản; ② dừng phát sinh chi phí mới, chốt trạng thái thực tế: deliverable nào xong, cái nào dở dang ở mức nào; ③ thống nhất với khách phần được nghiệm thu, thanh toán theo hợp đồng, bàn giao tài liệu và source; ④ bố trí lại nhân sự với line manager, làm lessons learned nội bộ. Giữ quan hệ tốt, vì khách cắt ngân sách năm nay có thể quay lại năm sau.

## 2.10 PRINCE2 & câu hỏi kiểu đề PMP

**Q191. PRINCE2 có 7 principles nào? Nguyên tắc nào bạn thấy hữu ích nhất trong outsourcing?**
Continued business justification, learn from experience, defined roles and responsibilities, manage by stages, manage by exception, focus on products, tailor to suit the project. Hữu ích nhất với em là **manage by stages** (chia giai đoạn, cuối mỗi giai đoạn quyết định có đi tiếp không) và **focus on products** (định nghĩa sản phẩm và tiêu chí chất lượng trước khi làm), vì khớp với cách khách Nhật nghiệm thu theo pha và theo tài liệu.

**Q192. Kể tên 7 themes và 7 processes của PRINCE2.**
Themes (theo bản 2017; bản cập nhật sau đổi tên gọi một số mục): Business Case, Organization, Quality, Plans, Risk, Change, Progress. Processes: Starting up a Project, Directing a Project, Initiating a Project, Controlling a Stage, Managing Product Delivery, Managing a Stage Boundary, Closing a Project. Themes là các khía cạnh phải quản lý liên tục; processes mô tả ai làm gì theo trình tự, từ trước khi khởi động đến khi đóng dự án.

**Q193. Management by exception và tolerances trong PRINCE2 vận hành thế nào?**
Project Board đặt tolerance (dung sai cho phép) cho PM theo các khía cạnh time, cost, scope, quality, risk, benefits — vd stage này ±10% chi phí, ±1 tuần (tham khảo). Trong dung sai, PM tự quyết và chỉ báo cáo định kỳ (Highlight Report); khi **dự báo** vượt dung sai, PM lập Exception Report trình Board, Board quyết định chấp nhận, yêu cầu Exception Plan hay dừng dự án. Cơ chế này giúp lãnh đạo không phải quản lý vi mô mà vẫn kiểm soát được.
> 💡 Chữ quan trọng là "dự báo vượt" — escalate khi thấy xu hướng, không đợi vượt rồi mới báo.

**Q194. Tổ chức dự án PRINCE2 gồm những vai trò nào? Ánh xạ sang dự án outsourcing với khách Nhật ra sao?**
Project Board gồm Executive (chịu trách nhiệm business case, quyết định cuối), Senior User (đại diện người dùng), Senior Supplier (đại diện bên cung cấp); bên dưới là Project Manager, Team Manager, Project Assurance, Project Support. Ánh xạ tham khảo: Executive = sponsor phía khách; Senior User = trưởng bộ phận nghiệp vụ của khách; Senior Supplier = lãnh đạo delivery phía vendor; Team Manager = team leader offshore; Assurance = QA độc lập hoặc PMO.

**Q195. PRINCE2 khác PMBOK ở điểm cơ bản nào? Có dùng chung được không?**
PMBOK là **bộ hướng dẫn kiến thức**: mô tả cần quản lý gì và kỹ thuật nào (EVM, CPM, quản lý stakeholder), không áp đặt vai trò cụ thể. PRINCE2 là **phương pháp có quy định** rõ vai trò, quy trình, tài liệu quản lý và cơ chế stage/tolerance. Dùng chung rất tốt: PRINCE2 cho khung quản trị (ai quyết, khi nào), PMBOK cho kỹ thuật (lập lịch, chi phí, rủi ro) — em thường lấy stage gate + tolerance của PRINCE2 và EVM/CPM của PMBOK.

**Q196. Câu kiểu đề PMP: Một thành viên báo rằng khách nhờ thêm một tính năng nhỏ và bạn ấy đã làm xong. PM nên làm gì đầu tiên?**
Không phạt thành viên, cũng chưa đưa thẳng lên CCB; trước hết **đánh giá tác động** của thay đổi đã làm (phạm vi, tiến độ, chất lượng, hợp đồng). Sau đó đưa vào change control để được duyệt hoặc gỡ ra, cập nhật tài liệu và nhắc lại quy trình với team. Logic đề PMP: phát hiện thay đổi → phân tích tác động → quy trình chính thức → cập nhật kế hoạch → truyền thông.
> 💡 Trong đề PMP, đáp án "phân tích tác động trước" gần như luôn thắng các đáp án hành động ngay khi chưa có thông tin.

**Q197. Câu kiểu đề PMP: Giữa dự án, một rủi ro chưa có trong register đã xảy ra. PM làm gì trước tiên?**
Rủi ro chưa nhận diện mà đã xảy ra thì là issue: PM áp dụng **workaround** để khống chế tác động, ghi vào issue log, sau đó phân tích nguyên nhân, cập nhật risk register (rủi ro tương tự có thể còn) và xem lại cách nhận diện rủi ro. Tác động vượt thẩm quyền thì escalate. Khác với rủi ro đã nhận diện: khi đó bước đầu tiên là kích hoạt kế hoạch ứng phó đã chuẩn bị.

**Q198. Câu kiểu đề PMP: Giữa dự án, khách cử một trưởng phòng mới làm người duyệt nghiệm thu. PM nên làm gì trước tiên?**
Trước tiên **cập nhật stakeholder register** và phân tích người này: quyền hạn, kỳ vọng, mức quan tâm, yêu cầu riêng. Sau đó gặp trực tiếp để giới thiệu dự án, xác nhận lại tiêu chí nghiệm thu và các quyết định đã chốt, rồi cập nhật communication plan. Đừng mặc định người mới chấp nhận mọi thỏa thuận cũ — khả năng họ mở lại yêu cầu đã chốt phải đưa vào risk register.
> 💡 Trong đề PMP, stakeholder mới xuất hiện → đáp án thường là "cập nhật stakeholder register và phân tích" trước mọi hành động khác.

**Q199. Câu kiểu đề PMP: Sponsor yêu cầu rút ngắn 2 tuần nhưng không tăng ngân sách, không giảm phạm vi. PM xử lý thế nào?**
Xét fast-tracking trên critical path trước (không tốn thêm tiền nhưng tăng rủi ro làm lại) và phân bổ lại nguồn lực trong team, rồi trình sponsor phân tích: rút được bao nhiêu ngày, kèm rủi ro gì. Nếu không đủ 2 tuần, đưa các phương án trade-off: crash với chi phí X, hoãn phạm vi Y sang release sau, hoặc chấp nhận rủi ro Z. PM không tự ý cắt test hay nhận bừa — sponsor quyết định dựa trên dữ liệu, mọi lựa chọn được ghi lại.
> 💡 Đề PMP ưu tiên "phân tích và đưa phương án cho sponsor", không phải "từ chối" hay "đồng ý rồi bắt team OT".

**Q200. PMP, PRINCE2, PMI-ACP, PSM/CSM khác nhau thế nào và có giá trị gì với Senior PM outsourcing?**
PMP (PMI) bao quát quản lý dự án cả predictive, agile và hybrid; PRINCE2 là phương pháp quản trị theo stage, phổ biến ở Anh và châu Âu; PMI-ACP tập trung vào agile; PSM (Scrum.org) và CSM (Scrum Alliance) chuyên về vai trò Scrum Master. Giá trị thực tế: tạo ngôn ngữ chung với khách và đồng nghiệp, tăng độ tin cậy trong proposal, nhưng không thay được kinh nghiệm xử lý tình huống thật. Lộ trình hợp lý: PMP làm nền, thêm PSM hoặc PMI-ACP nếu làm nhiều dự án agile.
> 💡 JD ghi ưu tiên các chứng chỉ này và công ty hỗ trợ thi PMP — nếu chưa có, hãy nêu kế hoạch học và thi cụ thể thay vì né câu hỏi.
