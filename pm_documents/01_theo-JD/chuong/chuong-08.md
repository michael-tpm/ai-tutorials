# Chương 8 · Tình huống thực tế dự án với khách Nhật (Q701–Q800)

## 8.1 Trễ tiến độ & 納期 cứng

**Q701. Dự án hệ thống nội bộ cho khách bảo hiểm B, team 12 người, còn 3 tuần nữa vào 結合テスト thì em phát hiện module tính phí trễ khoảng 2 tuần so với WBS. Anh/chị xử lý thế nào?**
① Xác nhận fact trong 1 ngày: đối chiếu WBS với task done thực tế, hỏi tech lead nguyên nhân (estimate sai, blocker hay thiếu người), tính lại ngày hoàn thành dự kiến. ② Khoanh vùng: chuyển 1–2 member từ module đã ổn sang, ưu tiên phần 結合テスト (ketsugou tesuto – kiểm thử tích hợp) cần sớm nhất, OT có giới hạn. ③ 報連相 (hou-ren-sou – báo cáo, liên lạc, thảo luận): báo khách ngay trong 定例会 (teireikai – họp định kỳ) tuần đó, không đợi cạn buffer, kèm 2 phương án đổi thứ tự test. ④ 再発防止 (saihatsu boushi – phòng ngừa tái phát): theo dõi burndown/EVM hằng ngày, lệch > 2 ngày (tham khảo) là phải escalate.
> 💡 Khách Nhật ghét bất ngờ hơn ghét tin xấu: báo sớm kèm phương án luôn ghi điểm hơn âm thầm tự cứu rồi vẫn trễ.

**Q702. Khách sản xuất C nói 納期 ngày 31/3 không thể dời vì gắn với ngày vận hành dây chuyền mới, nhưng team ước tính cần thêm 3 tuần. Anh/chị xử lý thế nào?**
① Fact: cùng khách tách chức năng bắt buộc phải có để dây chuyền chạy ngày 31/3 với phần làm sau được; kiểm lại estimate 3 tuần với tech lead. ② Hành động: đề xuất 段階リリース (dankai ririisu – release theo đợt): đợt 1 đúng 納期 (nouki – hạn bàn giao) với chức năng vận hành tối thiểu, đợt 2 sau 3–4 tuần; xin thêm người cho phần độc lập. ③ Báo khách bảng 3 phương án (cắt scope / thêm người kèm chi phí / giữ nguyên và chấp nhận rủi ro), xin quyết định, ghi 議事録 (gijiroku – biên bản họp). ④ Phòng ngừa: các mốc "không dời" phải chốt từ 要件定義 (youken teigi – định nghĩa yêu cầu) để lập kế hoạch ngược từ 納期.

**Q703. Dự án ngân hàng A chia 2 vendor: vendor khác làm 基本設計, bên mình nhận từ 詳細設計; tài liệu 基本設計 bàn giao trễ 3 tuần và thiếu nhiều chỗ. Anh/chị xử lý thế nào?**
① Fact: lập danh sách điểm thiếu/mâu thuẫn trong 基本設計 (kihon sekkei – thiết kế cơ bản), đo tác động lên lịch 詳細設計 (shousai sekkei – thiết kế chi tiết). ② Hành động: không ngồi chờ — làm trước phần đủ thông tin; phần thiếu ghi 前提条件 (zentei jouken – giả định tiền đề) để làm tiếp, gom câu hỏi vào QA表 (bảng hỏi đáp) gửi khách hằng ngày. ③ Báo khách bằng fact: "đầu vào trễ 3 tuần → mốc của chúng tôi dịch tương ứng", đề nghị khách (bên quản lý cả 2 vendor) chốt lại lịch tổng. ④ Gốc: đề xuất tiêu chí bàn giao giữa các 工程 (koutei – công đoạn), ghi rủi ro phụ thuộc vendor vào risk register.
> 💡 Hợp đồng của mình là với khách, không phải với vendor kia: mọi điều chỉnh đi qua khách, có văn bản, và tuyệt đối không chê vendor kia trước mặt khách.

**Q704. Khách bảo hiểm B hứa gửi data mẫu và spec giao tiếp hệ thống ngoài trước ngày 1/6, đến 10/6 vẫn chưa có, 8 người trong team đang bị chặn. Anh/chị xử lý thế nào?**
① Fact: ghi rõ ngày khách cam kết, task bị chặn, effort đang chờ. ② Hành động: dùng mock interface và data giả lập theo format dự đoán, kéo task phase sau lên làm trước (前倒し maedaoshi – làm sớm) để không ai ngồi không. ③ Báo khách: đưa vào 課題管理表 (kadai kanrihyou – bảng quản lý vấn đề) có hạn trả lời, email lịch sự nêu ảnh hưởng định lượng: "mỗi tuần trễ đầu vào → 納期 dịch khoảng 1 tuần hoặc phát sinh chi phí chờ". ④ Phòng ngừa: kế hoạch dự án liệt kê rõ お客様作業 (okyakusama sagyou – việc phía khách phải làm) với hạn, và điều khoản xử lý khi trễ.

**Q705. Đang 総合テスト, PM phía khách hỏi: "Báo cáo tuần trước còn xanh, sao tuần này đỏ ngay?". Anh/chị xử lý thế nào?**
① Fact: nhận trách nhiệm trước, rồi rà số liệu tuần trước — thường do báo theo % task tự khai thay vì số case thực hiện/pass, bug tồn. ② Hành động: trong ngày gửi lại tiến độ 総合テスト (sougou tesuto – kiểm thử hệ thống) theo chỉ số khách quan và kế hoạch phục hồi theo ngày. ③ Báo khách: xin lỗi ngắn gọn vì báo cáo chưa phản ánh đúng rủi ro, giải thích nguyên nhân, cam kết đổi cách báo. ④ 再発防止: thêm trạng thái "vàng" có tiêu chí định lượng (vd lệch > 3% kế hoạch hoặc blocker > 2 ngày — tham khảo), báo cả xu hướng chứ không chỉ màu.
> 💡 Báo cáo "dưa hấu" (xanh ngoài đỏ trong) làm mất niềm tin nặng nhất — thừa nhận rồi sửa hệ thống báo cáo, đừng bào chữa.

**Q706. Còn 5 ngày đến 納期, team báo "chắc kịp" nhưng 20% case regression chưa chạy. Anh/chị xử lý thế nào?**
① Fact: xác định 20% case chưa chạy thuộc chức năng nào, mức rủi ro (tiền, dữ liệu hay chỉ giao diện). ② Hành động: chạy ngay case rủi ro cao, huy động BA/dev cùng test, dùng automation nếu có; đặt tiêu chí go/no-go rõ trước ngày giao 2 ngày. ③ Báo khách sớm: "đã chạy 80%, phần còn lại thuộc X, dự kiến xong ngày Y"; nếu không kịp, đề xuất giao đúng hạn kèm danh sách case 未実施 (mijisshi – chưa thực hiện) và lịch hoàn tất, để khách quyết. ④ Gốc: kế hoạch test có buffer, tự động hóa dần bộ regression.

**Q707. Khách ngân hàng A muốn kéo 納期 sớm lên 1 tháng vì ban lãnh đạo muốn công bố dịch vụ sớm, dự án đang đúng kế hoạch. Anh/chị xử lý thế nào?**
① Fact: hỏi rõ thứ thật sự cần vào ngày mới: demo, release toàn bộ hay chỉ chức năng công bố. ② Hành động: trong 2–3 ngày tính 3 phương án: (a) release sớm phần cốt lõi, phần còn lại giữ lịch cũ; (b) thêm người kèm chi phí và rủi ro (thêm người muộn không tăng tốc tuyến tính); (c) giữ nguyên. ③ Báo khách bằng văn bản, mỗi phương án có chi phí, rủi ro chất lượng, xin quyết định chính thức. ④ Sau khi chốt: làm CR/phụ lục hợp đồng, cập nhật kế hoạch, theo dõi rủi ro hằng ngày.

**Q708. Dự án migrate hệ thống lõi cho khách sản xuất C có ngày cut-over cố định trong kỳ nghỉ Golden Week, 2 tuần trước đó buổi rehearsal 移行 chạy quá thời gian cho phép 6 tiếng. Anh/chị xử lý thế nào?**
① Fact: phân tích log rehearsal 移行 (ikou – chuyển đổi dữ liệu/hệ thống), tìm bước ngốn thời gian (load data, build index, verify). ② Hành động: tối ưu song song (chia lô, tắt index rồi build lại, chuyển trước data tĩnh), chạy rehearsal lần 2 trong 1 tuần với data quy mô thật; chuẩn bị kế hoạch 切り戻し (kirimodoshi – quay lui/rollback) và điểm dừng giữa chừng. ③ Báo khách ngay sau rehearsal kèm số đo và kế hoạch rút ngắn, đề nghị chốt go/no-go trước cut-over 3 ngày. ④ Phòng ngừa: rehearsal sớm hơn, ít nhất 2 lần, có tiêu chí thời gian cho từng bước.

**Q709. Làm Scrum cho khách Nhật, sprint 2 tuần, team chỉ hoàn thành khoảng 60% story đã nhận lần thứ 3 liên tiếp. Anh/chị xử lý thế nào?**
① Fact: xem velocity thực 3 sprint, phân loại story dở do estimate, do yêu cầu chưa rõ hay do bị chen việc. ② Hành động: sprint tới nhận việc theo velocity trung bình thực tế; tăng refinement để story đạt Definition of Ready trước planning; việc chen ngang phải qua PO. ③ Báo PO/khách bằng số liệu, điều chỉnh release plan theo velocity thật thay vì theo mong muốn. ④ Gốc: retro chọn 1–2 action đo được; với khách quen waterfall, giải thích sprint goal là dự báo, nhưng phải là dự báo tin được.

**Q710. Sau khi dự án ngân hàng A trễ mốc 単体テスト, khách yêu cầu từ mai báo cáo tiến độ hằng ngày bằng tiếng Nhật, team đang rất căng. Anh/chị xử lý thế nào?**
① Fact: hiểu đây là tín hiệu khách mất an tâm, không phải "phạt"; hỏi khách muốn thấy chỉ số gì. ② Hành động: nhận ngay; thiết kế báo cáo 1 trang (kế hoạch/thực tế 単体テスト (tantai tesuto – kiểm thử đơn vị) theo ngày, blocker, việc ngày mai), số lấy tự động từ tool, PM/BrSE viết để dev không mất giờ. ③ Gửi đúng giờ cố định mỗi ngày (vd 17:00 giờ Nhật), tin xấu ở dòng đầu. ④ Khi tiến độ ổn định 2–3 tuần, chủ động đề xuất quay lại tần suất tuần, dựa trên số liệu.

## 8.2 Sự cố 本番 & 障害

**Q711. Hệ thống ngân hàng A đang chạy 本番, khách phát hiện tiền lãi tính sai cho một nhóm tài khoản sau bản release sửa lỗi tuần trước. Anh/chị xử lý thế nào?**
① Fact trong 1–2 giờ: tái hiện lỗi trên 本番 (honban – môi trường production) bằng log/dữ liệu, xác định điều kiện, số tài khoản, khoảng thời gian — tức 影響範囲 (eikyou han'i – phạm vi ảnh hưởng). ② 暫定対応 (zantei taiou – xử lý tạm): cùng khách quyết định dừng job tính lãi hoặc 切り戻し về bản trước; script tính lại chỉ chạy khi khách duyệt. ③ 報連相: gửi 第一報 (daiippou – báo cáo đầu tiên) ngay dù chưa rõ nguyên nhân, cập nhật theo mốc giờ cố định, sau đó nộp 障害報告書 (shougai houkokusho – báo cáo sự cố). ④ 恒久対応 (koukyuu taiou – xử lý triệt để): sửa code, bổ sung test biên, 横展開 (yokotenkai – nhân rộng kiểm tra) sang các công thức tính tương tự.
> 💡 Lỗi liên quan đến tiền: không tự ý sửa dữ liệu production — mọi thao tác data phải có khách duyệt và lưu log.

**Q712. Batch đêm của khách sản xuất C chết lúc 3h sáng giờ Nhật, 7h sáng nhà máy cần dữ liệu để chạy ca sản xuất. Anh/chị xử lý thế nào?**
① Fact: người trực xem log, xác định bước lỗi và dữ liệu đã xử lý đến đâu, ước tính thời gian chạy lại. ② Hành động: lỗi do data/hạ tầng tạm thời → rerun từ checkpoint theo runbook; nếu không kịp trước 7h → chuẩn bị phương án thay thế (dùng dữ liệu hôm trước, xuất tay phần thiết yếu) để khách chọn. ③ Báo: gọi đầu mối trực của khách theo danh sách liên lạc khẩn ngay khi xác nhận có ảnh hưởng, cập nhật mỗi 30 phút. ④ Sau sự cố: なぜなぜ分析 (naze naze bunseki – hỏi "tại sao" lặp lại đến gốc), thêm alert sớm, retry tự động, cập nhật runbook.

**Q713. Lúc 2h sáng giờ Nhật (0h Việt Nam), monitoring báo hệ thống web của khách bảo hiểm B không truy cập được, đầu mối trực phía khách không nghe máy. Anh/chị xử lý thế nào?**
① Fact: kiểm tra phạm vi (toàn bộ hay một phần), nguyên nhân sơ bộ (deploy mới, hạ tầng, bị tấn công). ② Hành động: làm các bước runbook đã được khách duyệt (restart, failover, rollback); việc ngoài thẩm quyền đã thỏa thuận thì không tự làm. ③ Báo: gọi lần lượt danh sách escalation (người thứ 2, thứ 3), đồng thời gửi email/chat để lưu dấu thời gian và hiện trạng, cập nhật định kỳ. ④ Sau sự cố: cùng khách rà lại danh sách liên lạc khẩn và phạm vi quyền xử lý ban đêm, ghi vào tài liệu vận hành.

**Q714. Release bản cập nhật cho khách bảo hiểm B vào ngày 31/3 (年度末), sau 1 giờ phát hiện lỗi ở màn hình báo cáo quyết toán. Anh/chị xử lý thế nào?**
① Fact: lỗi chặn nghiệp vụ quyết toán hay chỉ sai hiển thị; có workaround không. ② Hành động: chặn nghiệp vụ → đề xuất rollback ngay theo kế hoạch 切り戻し; có workaround → hướng dẫn người dùng, làm hotfix có test và duyệt trong ngày. ③ Báo khách trong 30 phút với 4 ý: hiện tượng, ảnh hưởng, việc đang làm, giờ báo tiếp theo. ④ Phòng ngừa: đưa quy tắc "đóng băng release" quanh 年度末 (nendomatsu – cuối năm tài chính, thường là cuối tháng 3) vào kế hoạch năm, chỉ cho phép release sửa lỗi khẩn.

**Q715. Hai tuần sau khi chuyển đổi dữ liệu, khách phát hiện tên khách hàng hiển thị sai ở khoảng 1% bản ghi. Anh/chị xử lý thế nào?**
① Fact: so với dữ liệu nguồn, tìm pattern — thường là 外字 (gaiji – chữ Kanji ngoài bảng mã chuẩn) hoặc chuyển đổi Shift_JIS ↔ UTF-8. ② Hành động: viết script đối chiếu toàn bộ, xác định chính xác bản ghi lỗi và dữ liệu phát sinh sau đó có bị lan không. ③ Báo khách bản đầu trong ngày, kèm danh sách bản ghi lỗi và kế hoạch sửa; script sửa chỉ chạy khi khách duyệt. ④ Gốc: thêm bước verify sau chuyển đổi (so khớp 100% trường quan trọng), 横展開 kiểm các bảng có trường tên/địa chỉ tương tự.
> 💡 外字 và Shift_JIS là bẫy kinh điển khi migrate hệ thống Nhật — nêu ra được cho thấy bạn đã làm thật.

**Q716. Sự cố production vừa xử lý xong, khách bảo hiểm B yêu cầu nộp 障害報告書 trong 2 ngày làm việc. Anh/chị xử lý thế nào?**
① Fact: dựng timeline chính xác (phát hiện, báo, xử lý tạm, khôi phục) từ log và lịch sử chat, không viết theo trí nhớ. ② Hành động: viết theo cấu trúc chuẩn: 現象 (genshou – hiện tượng) · 影響範囲 · 原因 (gen'in – nguyên nhân trực tiếp và gốc) · 暫定対応 · 恒久対応 · 再発防止 · 横展開. ③ Báo: BrSE kiểm tiếng Nhật, cấp trên/QA duyệt trước khi gửi; xin 30 phút giải thích trực tiếp với khách. ④ Mỗi biện pháp phòng ngừa có người phụ trách + hạn, báo trạng thái trong 定例会 đến khi đóng.

**Q717. Cần hotfix khẩn cho khách ngân hàng A trong 4 giờ, nhưng quy trình release chuẩn của khách yêu cầu review và test 2 ngày. Anh/chị xử lý thế nào?**
① Fact: mức nghiêm trọng thật sự, có workaround tạm (tắt chức năng, xử lý tay) để giảm áp lực thời gian không. ② Hành động: có workaround → áp dụng, hotfix đi quy trình đầy đủ; không có → xin áp dụng quy trình 緊急リリース (kinkyuu ririisu – release khẩn cấp) nếu khách có, review chéo 2 người, test phần thay đổi + smoke test. ③ Báo khách: không tự ý bỏ bước, xin phê duyệt ngoại lệ bằng văn bản từ người có thẩm quyền. ④ Sau release: bổ sung test đầy đủ và hồ sơ release trong 1–2 ngày.

**Q718. Cùng một lỗi production lặp lại lần thứ 3 trong 2 tháng dù team đã nộp 障害報告書 hai lần. Anh/chị xử lý thế nào?**
① Fact: đọc lại 2 báo cáo cũ — thường 再発防止 chỉ dừng ở "nhắc nhở cẩn thận", nguyên nhân gốc chưa chạm tới quy trình. ② Hành động: xử lý sự cố lần 3, rồi tổ chức なぜなぜ分析 mới có người ngoài team (QA/PMO), đi đến nguyên nhân ở mức cơ chế. ③ Báo khách: thừa nhận biện pháp trước chưa hiệu quả, xin lỗi chính thức cùng cấp trên của mình, trình biện pháp cơ chế (check tự động trong CI, checklist bắt buộc có người ký). ④ Theo dõi chỉ số tái phát 3 tháng, báo trong 定例会.
> 💡 "Đào tạo lại / nhắc nhở" không được khách Nhật chấp nhận là 再発防止 — phải là cơ chế khiến lỗi không thể lặp lại.

**Q719. Sau release, người dùng phía khách sản xuất C báo hệ thống chậm gấp 3 lần, nhưng môi trường test của team không tái hiện được. Anh/chị xử lý thế nào?**
① Fact: xin log/metric production (response time, slow query, số user đồng thời), so volume dữ liệu thật với môi trường test. ② Hành động: khoanh vùng các thay đổi trong release; nếu ảnh hưởng nặng → rollback hoặc tắt tính năng mới rồi phân tích offline. ③ Báo khách: xác nhận đã nhận, nêu các bước điều tra và mốc cập nhật; không bao giờ trả lời "bên em không thấy lỗi". ④ Gốc: bổ sung performance test với dữ liệu cỡ production và monitoring APM.

**Q720. Member offshore lỡ chạy lệnh xóa dữ liệu trên staging của khách, môi trường dùng chung với vendor khác đang làm 受入テスト. Anh/chị xử lý thế nào?**
① Fact: dữ liệu nào bị xóa, có backup không, ai đang bị ảnh hưởng. ② Hành động: dừng mọi thao tác, nhờ khách/bên vận hành restore từ backup, hỗ trợ dựng lại data test. ③ Báo khách trong 30 phút, nói thật nguyên nhân là thao tác của bên mình; gửi lời xin lỗi tới vendor bị ảnh hưởng qua khách để họ điều chỉnh lịch 受入テスト (ukeire tesuto – kiểm thử nghiệm thu). ④ 再発防止: tách quyền (member không có quyền xóa trên môi trường chung), lệnh nguy hiểm phải ダブルチェック (daburu chekku – 2 người xác nhận), 横展開 rà quyền ở các môi trường khác.

## 8.3 Yêu cầu mơ hồ & thay đổi

**Q721. Khách bảo hiểm B đã duyệt 基本設計 được 2 tuần, nay muốn đổi luồng phê duyệt hợp đồng từ 2 cấp thành 3 cấp, team đang ở 詳細設計. Anh/chị xử lý thế nào?**
① Fact: xác nhận đây là 仕様変更 (shiyou henkou – thay đổi đặc tả) so với bản đã duyệt; phân tích ảnh hưởng tới màn hình, DB, phân quyền, test, tài liệu. ② Hành động: trong 2–3 ngày làm impact analysis + estimate effort/lịch; trong lúc chờ, team không làm theo spec mới. ③ Báo khách: gửi CR có effort, chi phí, ảnh hưởng 納期 và 2 lựa chọn thời điểm áp dụng (ngay hoặc phase sau). ④ Khách duyệt xong mới cập nhật tài liệu thiết kế, traceability; ghi số CR để báo cáo xu hướng thay đổi.

**Q722. Đang 総合テスト, khách nói "chức năng xuất CSV thì 当然 phải có" dù không có trong 要件定義. Anh/chị xử lý thế nào?**
① Fact: rà tài liệu yêu cầu, 議事録, QA表; nếu từng được nhắc mà bên mình bỏ sót → nhận lỗi và lên kế hoạch làm. ② Nếu không có: ghi nhận nhu cầu, estimate nhanh. ③ Báo khách khéo, không cãi đúng sai trong họp: "Theo tài liệu đã chốt, chức năng này chưa nằm trong phạm vi; chúng tôi đề xuất xử lý như CR, effort X ngày" — việc nhỏ, quan hệ quan trọng thì có thể làm miễn phí, ghi rõ là ngoại lệ. ④ Gốc: checklist các yêu cầu kiểu 当然 (touzen – "đương nhiên", khách không nói ra) như export, in, log, phân quyền để hỏi ngay ở 要件定義.

**Q723. Dự án 請負 cho khách sản xuất C, sau mỗi buổi demo khách lại "nhờ chỉnh nhỏ một chút", tích lại đã khoảng 15% effort ngoài scope. Anh/chị xử lý thế nào?**
① Fact: liệt kê toàn bộ chỉnh sửa ngoài yêu cầu kèm effort thực tế đã tiêu. ② Hành động: từ hôm nay, mọi yêu cầu mới vào bảng CR và phân loại: lỗi/bỏ sót (mình chịu) hay thay đổi (CR). ③ Báo khách: gặp riêng người quyết định, trình số liệu 15% và ảnh hưởng tới 納期/chất lượng; đề xuất 3 hướng: tính phí phần vượt, đổi lấy cắt phần khác, hoặc gom vào phase 2. ④ Phòng ngừa: định nghĩa "chỉnh nhỏ" đo được (vd < 0,5 ngày công/yêu cầu, tổng mỗi tháng có trần) trong quy trình CR của hợp đồng 請負 (ukeoi – hợp đồng trọn gói, cam kết kết quả).
> 💡 Trong 請負, scope creep là tiền công ty mất trực tiếp — mở số liệu sớm, đừng đợi cuối dự án mới đòi.

**Q724. Người phụ trách phía khách nhắn qua Teams lúc 21h: "Sửa luôn màn hình này nhé, gấp", không có email hay CR. Anh/chị xử lý thế nào?**
① Fact: đọc kỹ, phân biệt đây là sửa lỗi hay thay đổi, ảnh hưởng tới đâu. ② Hành động: trả lời ngay trong chat là đã nhận và sẽ báo đánh giá ảnh hưởng trong N giờ; việc nhỏ và gấp thật thì có thể bắt đầu, nhưng sau khi xác nhận lại bằng văn bản. ③ Báo: chuyển thành ticket/CR, gửi email "chúng tôi hiểu yêu cầu như sau…, effort…, ảnh hưởng…, xin xác nhận", cc 窓口 (madoguchi – đầu mối chính thức) phía khách. ④ Gốc: chốt lại trong 定例会 kênh tiếp nhận yêu cầu chính thức; chat chỉ để liên lạc nhanh.

**Q725. Khách gửi spec màn hình chỉ là ảnh chụp Excel, không mô tả logic, còn 2 tuần là hết hạn 詳細設計. Anh/chị xử lý thế nào?**
① Fact: liệt kê các điểm thiếu: validate, xử lý lỗi, phân quyền, điều kiện hiển thị, giá trị mặc định. ② Hành động: BA/BrSE tự đề xuất spec theo 前提 hợp lý nhất (dựa trên màn tương tự, nghiệp vụ chung), viết QA表 dạng câu hỏi đóng "Chúng tôi hiểu là A, đúng không?". ③ Báo khách: gửi QA表 theo đợt hằng ngày có hạn trả lời; thống nhất trước quy tắc câu quá hạn sẽ làm theo 前提 và ghi rủi ro làm lại. ④ Gốc: đề xuất template spec màn hình cho các module sau.

**Q726. Khách ngân hàng A trả lời "検討します" cho 12 câu hỏi quan trọng trong QA表 suốt 3 tuần, team bắt đầu bị chặn. Anh/chị xử lý thế nào?**
① Fact: phân loại 12 câu theo ảnh hưởng: câu nào chặn công việc 2 tuần tới, câu nào chờ được. ② Hành động: với câu chặn, đưa đề xuất mặc định kèm hạn quyết định, tạm làm theo 前提 và ghi rủi ro làm lại. ③ Báo: hỏi nhẹ ai là người quyết định thật, xin 30 phút họp có người đó; nêu ngày quyết định muộn nhất và hệ quả nếu trễ (ảnh hưởng 納期, chi phí). ④ Gốc: thêm cột "hạn quyết định" vào 課題管理表, báo số issue quá hạn trong 定例会 có cấp trên phía khách dự.
> 💡 "検討します" (kentou shimasu – sẽ xem xét) kéo dài thường nghĩa là người đối diện không có thẩm quyền hoặc chưa muốn quyết — tìm người quyết định thay vì hỏi lại cùng một người.

**Q727. Đang 結合テスト, team phát hiện hai tài liệu 基本設計 của khách mâu thuẫn về cách làm tròn số tiền phí bảo hiểm. Anh/chị xử lý thế nào?**
① Fact: ghi rõ 2 chỗ mâu thuẫn kèm ví dụ số cho thấy kết quả khác nhau (切り上げ kiriage – làm tròn lên, so với 切り捨て kirisute – bỏ phần lẻ). ② Hành động: tạm dừng các test case liên quan, test phần khác. ③ Báo khách ngay trong ngày, mức ưu tiên cao vì liên quan tiền; hỏi dạng chọn "A hay B", kèm ảnh hưởng và đề xuất của team. ④ Sau khi chốt: sửa cả hai tài liệu, 横展開 rà toàn bộ chỗ có làm tròn, thuế, phân bổ tiền trong hệ thống.

**Q728. Khách sản xuất C muốn bỏ qua 要件定義 vì "cứ làm giống hệ thống cũ" (現行踏襲), nhưng hệ thống cũ không có tài liệu. Anh/chị xử lý thế nào?**
① Fact: đánh giá hệ cũ: số màn hình, batch, logic ẩn; còn source không, ai còn hiểu nghiệp vụ. ② Hành động: đề xuất giai đoạn ngắn phân tích ngược (reverse engineering, vd 2–4 tuần) để lập tài liệu hiện trạng — là deliverable có phí, nên tính theo công sức. ③ Báo khách: "giống hệ cũ" không đo được thì không nghiệm thu được; xin khách xác nhận tài liệu hiện trạng làm đầu vào. ④ Gốc: ghi phạm vi 現行踏襲 (genkou toushuu – kế thừa nguyên hiện trạng) và 前提条件 vào hợp đồng; khác biệt phát hiện sau xử lý như CR.
> 💡 "Giống hệ cũ" là câu nguy hiểm nhất của dự án migrate: phải biến nó thành tài liệu kiểm chứng được trước khi báo giá cố định.

**Q729. Sau 受入テスト, khách yêu cầu đổi toàn bộ wording giao diện theo thuật ngữ mới của phòng kinh doanh và release trong 1 tuần. Anh/chị xử lý thế nào?**
① Fact: đếm số chuỗi, màn hình, tài liệu, message lỗi bị ảnh hưởng; kiểm text đã tách thành resource file chưa. ② Hành động: có resource file → effort nhỏ, sửa nhanh + regression giao diện; nếu hardcode → effort lớn, đề xuất làm trước màn hình người dùng ngoài. ③ Báo khách: đây là CR, nêu effort và rủi ro release gấp; xin 用語集 (yougoshuu – bảng thuật ngữ) chính thức một lần duy nhất để không sửa nhiều vòng. ④ Gốc: từ đầu dự án quản lý text bằng resource file và bảng thuật ngữ có người duyệt.

**Q730. Ngay trước 総合テスト, khách bảo hiểm B gửi 30 yêu cầu thay đổi cùng lúc, tất cả đều ghi "ưu tiên cao". Anh/chị xử lý thế nào?**
① Fact: estimate sơ bộ từng CR, đánh dấu CR gắn với luật/quy định hay go-live và CR chỉ là mong muốn. ② Hành động: tổ chức workshop 1–2 giờ, dùng MoSCoW hoặc so sánh từng cặp để xếp hạng; chỉ nhận số CR vừa năng lực còn lại, phần còn lại vào release sau. ③ Báo: gửi bảng xếp hạng + ảnh hưởng 納期/chi phí cho người có thẩm quyền ký duyệt. ④ Gốc: đưa "giai đoạn đóng băng thay đổi" (vd 2 tuần trước mỗi vòng test — tham khảo) vào kế hoạch và hợp đồng.

## 8.4 Khiếu nại chất lượng & mất niềm tin

**Q731. Khách ngân hàng A trả lại tài liệu 詳細設計 với 40 指摘, phần lớn là lỗi chính tả tiếng Nhật và định dạng không thống nhất. Anh/chị xử lý thế nào?**
① Fact: phân loại 40 指摘 (shiteki – điểm bị chỉ ra) theo nội dung/chính tả/định dạng; xác định lỗi do người viết hay do bỏ bước review. ② Hành động: sửa toàn bộ trong 2–3 ngày, gửi bảng đối chiếu từng 指摘 → nội dung đã sửa. ③ Báo khách: xin lỗi vì làm tốn thời gian review của họ, nêu biện pháp: người giỏi tiếng Nhật review trước khi gửi, checklist định dạng. ④ 再発防止: tool kiểm chính tả/định dạng, đo số 指摘 trên mỗi trang làm chỉ số chất lượng tài liệu, 横展開 cho các tài liệu còn lại.
> 💡 Với khách Nhật, lỗi chính tả là dấu hiệu thiếu cẩn thận và kéo theo nghi ngờ cả chất lượng code — đừng coi là chuyện nhỏ.

**Q732. Sau một sự cố, khách bảo hiểm B yêu cầu bản なぜなぜ分析 khoảng 10 trang, team cho rằng chỉ tốn thời gian. Anh/chị xử lý thế nào?**
① Fact: hiểu khách cần tài liệu này để giải trình nội bộ với cấp trên của họ — làm tốt là giúp 担当者 (tantousha – người phụ trách phía khách). ② Hành động: PM chủ trì một buổi 2 giờ với người liên quan, đi tới nguyên nhân gốc ở mức quy trình/cơ chế; viết theo format khách quen, có sơ đồ cây nguyên nhân. ③ Báo: gửi bản nháp để 担当者 góp ý trước, chỉnh rồi mới nộp chính thức. ④ Với team: giải thích giá trị, chia việc để không ảnh hưởng tiến độ; dùng kết quả làm bài học 横展開 cho dự án khác.

**Q733. 受入テスト của khách sản xuất C ra 50 bug trong tuần đầu, khách gửi email bày tỏ lo ngại về chất lượng. Anh/chị xử lý thế nào?**
① Fact: phân loại 50 bug: lỗi thật / không phải lỗi / trùng / do spec chưa rõ; theo mức độ và module để tìm điểm tập trung. ② Hành động: lập đội xử lý bug chặn nghiệp vụ trong 48 giờ; rà lại test case nội bộ để biết vì sao lọt. ③ Báo khách trong 1–2 ngày: nhận trách nhiệm trước rồi mới làm rõ các mục "không phải lỗi"; kế hoạch sửa theo ngày, cập nhật số bug mở/đóng hằng ngày. ④ 再発防止: bổ sung test case theo góc nhìn nghiệp vụ người dùng, 横展開 rà module tương tự trước khi khách test tiếp.

**Q734. Sau 2 lần release lỗi, khách yêu cầu được review từng dòng code trước mỗi lần release. Anh/chị xử lý thế nào?**
① Fact: hiểu khách cần cảm giác kiểm soát; tính xem việc khách review làm chậm mỗi release bao lâu. ② Hành động: nhận ngay ở giai đoạn đầu; chuẩn bị diff gọn, mô tả thay đổi, kết quả test và review nội bộ đi kèm. ③ Đồng thời minh bạch chỉ số chất lượng (coverage, static analysis, checklist review) để khách thấy cơ chế, không chỉ thấy code. ④ Sau 3–4 release ổn định, đề xuất bằng số liệu chuyển sang review theo rủi ro (chỉ logic tính tiền, bảo mật), giảm gánh cho cả hai bên.

**Q735. Trong 定例会, khách nói: "Nếu chất lượng không cải thiện, tháng sau chúng tôi sẽ cân nhắc chuyển vendor". Anh/chị xử lý thế nào?**
① Fact: ghi nhận nghiêm túc, hỏi rõ khách muốn thấy "cải thiện" ở chỉ số nào (số bug, thời gian phản hồi, chất lượng tài liệu). ② Hành động: trong 1 tuần lập 品質改善計画 (hinshitsu kaizen keikaku – kế hoạch cải thiện chất lượng) với chỉ số đo được và mốc 30/60 ngày; bổ sung người kinh nghiệm/QA. ③ Báo: escalate nội bộ ngay tới cấp trên/account manager, cùng gặp khách để thể hiện cam kết cấp công ty. ④ Báo cáo tiến triển hằng tuần theo đúng chỉ số đã thống nhất đến khi khách xác nhận ổn.
> 💡 Câu "chuyển vendor" là tín hiệu cần cấp quản lý cao hơn vào cuộc — PM tự xử lý một mình là sai.

**Q736. Khách phàn nàn email hỏi đáp của team thường trả lời chậm 2–3 ngày, còn team cho rằng câu hỏi phức tạp nên cần thời gian điều tra. Anh/chị xử lý thế nào?**
① Fact: đo thời gian phản hồi thực tế 1 tháng qua theo loại câu hỏi. ② Hành động: tách "xác nhận đã nhận" và "trả lời nội dung": xác nhận trong vài giờ làm việc kèm thời điểm sẽ trả lời; câu cần điều tra lâu thì gửi cập nhật giữa chừng. ③ Báo khách quy tắc phản hồi mới và cam kết thời gian theo mức ưu tiên. ④ Phân công người trực inbox theo ca, theo dõi chỉ số phản hồi trong báo cáo tuần.

**Q737. Khách bảo hiểm B phát hiện một số test case được ghi "OK" nhưng không có screenshot hay log làm bằng chứng. Anh/chị xử lý thế nào?**
① Fact: kiểm toàn bộ: bao nhiêu case thiếu bằng chứng, có case nào thực chất chưa test không. ② Hành động: test lại mọi case thiếu bằng chứng, lưu エビデンス (ebidensu – bằng chứng kiểm thử) đầy đủ theo format khách. ③ Báo khách trung thực: số lượng, nguyên nhân (hiểu sai quy định hay bỏ bước), kế hoạch test lại; không che giấu. ④ 再発防止: định nghĩa evidence bắt buộc cho từng loại case, QA kiểm ngẫu nhiên khoảng 10% (tham khảo) trước khi nộp, 横展開 cho các đợt test khác.
> 💡 Khách Nhật coi evidence test như chứng từ kế toán: không có bằng chứng nghĩa là chưa test.

**Q738. Khách sản xuất C nói trong họp: "Vendor làm module bên cạnh rất ít bug, sao bên anh nhiều vậy?". Anh/chị xử lý thế nào?**
① Fact: không phản bác tại chỗ; cảm ơn và xin dữ liệu so sánh (độ phức tạp, quy mô, cách đếm bug), đồng thời rà số liệu của mình. ② Hành động: phân tích bug theo nguyên nhân (thiết kế, code, hiểu sai yêu cầu) và giai đoạn phát hiện, chọn 2–3 điểm cải thiện ngay. ③ Báo khách bằng số liệu: thừa nhận phần đúng, nêu nhẹ nhàng khác biệt khách quan nếu có, trình kế hoạch cải thiện. ④ Cùng khách thống nhất cách đo chung (bug/KLOC hoặc bug/test case), theo dõi xu hướng theo tuần.

**Q739. Khách đòi xem kết quả 単体テスト theo từng hàm dạng bảng Excel, trong khi team chỉ có unit test tự động trên CI. Anh/chị xử lý thế nào?**
① Fact: xem hợp đồng/quy định chất lượng của khách có yêu cầu deliverable 単体テスト仕様書 (tantai tesuto shiyousho – tài liệu test case đơn vị) không. ② Hành động: nếu bắt buộc → bổ sung, nhưng sinh tự động từ code test (tên test, điều kiện, kết quả mong đợi) + báo cáo coverage, tránh viết tay. ③ Báo khách: demo cách làm tự động, đề xuất format thay thế; khách vẫn cần Excel thì xuất đúng format khách. ④ Gốc: lần sau chốt danh sách deliverable và format ngay từ kickoff.

**Q740. Sau 1 năm hợp tác suôn sẻ, khách bảo hiểm B bất ngờ giảm 50% khối lượng order cho phase tiếp theo mà không nói rõ lý do. Anh/chị xử lý thế nào?**
① Fact: hỏi qua kênh tin cậy (BrSE, account manager) nguyên nhân thật: ngân sách, chất lượng, giá hay chính sách nội bộ. ② Hành động: xin một buổi 振り返り (furikaeri – nhìn lại) với khách, nghe phản hồi thẳng thắn, không phòng thủ. ③ Báo nội bộ để sales/account cùng xử lý; nếu nguyên nhân là chất lượng/giá → đưa kế hoạch cải thiện cụ thể. ④ Giữ chất lượng phần việc còn lại ở mức tốt nhất, chuẩn bị đề xuất giá trị (tự động hóa, cải tiến vận hành) để giành lại phần đã mất.

## 8.5 Onsite–offshore & cầu nối

**Q741. BrSE onsite nói team offshore Đà Nẵng code sai spec, team offshore nói BrSE truyền đạt sai, khách đang chờ bản sửa. Anh/chị xử lý thế nào?**
① Fact: sửa cho khách trước, truy sự thật sau — đối chiếu email/ticket gốc của khách → bản BrSE truyền đạt → code. ② Hành động: giao 1 người chịu trách nhiệm sửa ngay; BrSE xác nhận lại spec trực tiếp với khách trong ngày. ③ Báo khách với tư cách 1 team: xin lỗi, hẹn giờ giao bản sửa; không để khách thấy nội bộ đổ lỗi. ④ Gốc: họp 3 bên không truy lỗi cá nhân, đặt quy tắc spec truyền đạt phải bằng văn bản và offshore gửi bản 認識合わせ (ninshiki awase – đồng bộ cách hiểu) trước khi code.
> 💡 Với khách, onsite và offshore là một công ty — PM phải dập việc đổ lỗi trước khi nó lọt ra ngoài.

**Q742. BrSE duy nhất của dự án ngân hàng A xin nghỉ việc, còn 2 tuần bàn giao, dự án đang giữa 詳細設計. Anh/chị xử lý thế nào?**
① Fact: liệt kê những gì chỉ BrSE nắm: quan hệ với khách, spec chưa ghi lại, issue đang mở, cam kết miệng. ② Hành động: ngay hôm đó lập kế hoạch 引継ぎ (hikitsugi – bàn giao công việc) 2 tuần; người thay (BrSE khác hoặc member giỏi tiếng Nhật) dự mọi cuộc họp, tài liệu hóa mọi thứ. ③ Báo khách sau khi đã có người thay: giới thiệu người mới, lịch bàn giao, cam kết mốc; nếu được, BrSE cũ cùng dự buổi chào khách. ④ Gốc: mọi vai trò cầu nối đều có backup nắm thông tin khách, giảm phụ thuộc 1 người.

**Q743. Comtor dịch "以上" thành "lớn hơn" (đúng ra là "lớn hơn hoặc bằng") trong spec điều kiện giảm phí, team code sai giá trị biên, khách phát hiện khi 総合テスト. Anh/chị xử lý thế nào?**
① Fact: xác nhận lỗi phát sinh ở khâu dịch, kiểm các điều kiện biên khác trong tài liệu đã dịch. ② Hành động: sửa code + test biên ngay; rà toàn bộ spec có 以上/以下/未満/超 (≥, ≤, <, >). ③ Báo khách: nhận lỗi của bên mình (không đẩy cho cá nhân comtor), kèm số chỗ đã rà và kết quả. ④ 再発防止: glossary dịch bắt buộc cho từ khóa điều kiện, test case biên viết trực tiếp từ bản tiếng Nhật gốc, spec tính tiền phải có BrSE review bản dịch.
> 💡 Cặp 以上/超 và 以下/未満 là bẫy dịch kinh điển — kể ví dụ này cho thấy bạn hiểu rủi ro ngôn ngữ thật.

**Q744. Phát hiện BrSE onsite đã nhận 5 yêu cầu từ khách trong 2 tuần nhưng không báo offshore, đến khi khách hỏi tiến độ mới lộ ra. Anh/chị xử lý thế nào?**
① Fact: thu thập 5 yêu cầu: ngày nhận, nội dung, BrSE đã hứa gì với khách. ② Hành động: estimate và xếp lịch ngay, xác định yêu cầu nào là CR cần xử lý hợp đồng. ③ Báo khách lịch xử lý thực tế, xin lỗi vì chậm; với CR vẫn đi đúng quy trình dù BrSE đã "hứa". ④ Gốc: yêu cầu nhận ở onsite phải vào ticket trong 24 giờ, PM xem backlog hằng ngày; nói chuyện riêng với BrSE để hiểu nguyên nhân (quá tải, ngại từ chối khách) và gỡ.

**Q745. Team offshore than BrSE chỉ chuyển tiếp nguyên email khách mà không phân tích, mỗi câu hỏi mất 1–2 ngày mới có câu trả lời. Anh/chị xử lý thế nào?**
① Fact: đo số câu hỏi/tuần và thời gian chờ trung bình; xem khối lượng việc của BrSE. ② Hành động: họp ngắn onsite–offshore 15 phút đầu ngày để gom câu hỏi; định nghĩa BrSE chịu trách nhiệm "làm rõ + phân tích", không chỉ chuyển tiếp. ③ Đề xuất với khách một khung giờ Q&A cố định hoặc cho tech lead offshore dự họp kỹ thuật trực tiếp (BrSE hỗ trợ). ④ Gốc: ghi rõ vai trò BrSE trong 体制図 (taiseizu – sơ đồ tổ chức dự án) và ma trận RACI, theo dõi chỉ số thời gian trả lời.

**Q746. Khách muốn làm việc trực tiếp với dev offshore qua chat cho nhanh, bỏ qua BrSE và PM. Anh/chị xử lý thế nào?**
① Fact: hỏi lý do — thường là kênh hiện tại chậm, tức là tín hiệu cần sửa phía mình. ② Hành động: đồng ý có khung: mở kênh trực tiếp cho Q&A kỹ thuật, nhưng mọi yêu cầu thay đổi/giao việc vẫn qua ticket; PM/BrSE ở trong channel. ③ Báo khách quy tắc kênh và lợi ích (kiểm soát scope, chất lượng, lưu vết). ④ Định kỳ rà chat để phát hiện CR ngầm; cải thiện tốc độ phản hồi của BrSE/PM để kênh chính không bị bỏ qua.

**Q747. Dự án có comtor nhưng không có BrSE, các buổi họp spec 2 giờ với khách chỉ ra 議事録 sơ sài, team hiểu sai nhiều chỗ. Anh/chị xử lý thế nào?**
① Fact: xem 議事録 các buổi trước, đếm số lần làm lại do hiểu sai. ② Hành động: gửi agenda và câu hỏi trước bằng tiếng Nhật; tech lead cùng dự; ghi âm nếu khách đồng ý; trong 24 giờ sau họp gửi 議事録 có danh sách quyết định + action để khách xác nhận. ③ Báo khách: đề nghị coi 議事録 đã xác nhận là văn bản chốt. ④ Gốc: đề xuất công ty bổ sung BrSE hoặc đào tạo comtor về domain; xây glossary dự án.

**Q748. Khách phàn nàn: mỗi lần giao việc, offshore đều trả lời "はい、わかりました" nhưng sau đó vẫn làm sai. Anh/chị xử lý thế nào?**
① Fact: nhận diện vấn đề văn hóa — member nói "đã hiểu" vì ngại hỏi lại. ② Hành động: áp dụng 復唱 (fukushou – nhắc lại để xác nhận): sau mỗi yêu cầu, member viết lại bằng lời mình kèm ví dụ input/output và gửi khách xác nhận trước khi làm. ③ Báo khách biện pháp mới, mời khách chỉ ra ngay nếu bản xác nhận sai. ④ Nội bộ: tạo môi trường hỏi an toàn, khen câu hỏi tốt; đo số lần làm lại do hiểu sai mỗi tháng.
> 💡 "わかりました" của người không nói tiếng mẹ đẻ thường chỉ có nghĩa "tôi đã nghe" — PM phải thiết kế bước xác nhận, không tin câu trả lời.

**Q749. Member onsite làm tại văn phòng khách ở Nhật bị phàn nàn về thái độ: đi muộn, dùng điện thoại trong họp. Anh/chị xử lý thế nào?**
① Fact: hỏi khách sự việc cụ thể, nghe cả phía member. ② Hành động: nói chuyện riêng với member trong ngày, nhắc quy tắc ứng xử tại văn phòng khách (có mặt trước giờ, điện thoại im lặng, báo trước khi vắng), đặt kỳ vọng rõ; tái diễn thì thay người. ③ Báo khách: cảm ơn phản hồi, xin lỗi, nêu biện pháp và theo dõi. ④ Phòng ngừa: đào tạo ビジネスマナー (bijinesu manaa – phép lịch sự công sở Nhật) bắt buộc trước khi cử onsite, hỏi phản hồi khách sau tháng đầu.

**Q750. Đội onsite 3 người và offshore 15 người dùng hai phiên bản tài liệu khác nhau, khách phát hiện deliverable bị lẫn bản cũ. Anh/chị xử lý thế nào?**
① Fact: xác định deliverable nào sai phiên bản, đã ảnh hưởng tới đâu (code, test, khách đã dùng chưa). ② Hành động: thu hồi và gửi lại bản đúng; rà toàn bộ deliverable đã gửi trong tháng. ③ Báo khách: xin lỗi, liệt kê tài liệu đã gửi lại và phạm vi đã rà. ④ Gốc: một kho tài liệu duy nhất có quản lý version, mọi tài liệu có 改訂履歴 (kaitei rireki – lịch sử sửa đổi), gửi deliverable qua checklist (tên file, version, người duyệt).

## 8.6 Nguồn lực

**Q751. Tech lead của dự án bảo hiểm B (team 15 người) báo nghỉ việc với 30 ngày báo trước, đúng lúc chuẩn bị 結合テスト. Anh/chị xử lý thế nào?**
① Fact: đánh giá phần chỉ tech lead nắm (kiến trúc, module phức tạp, môi trường, deploy), chọn ứng viên kế nhiệm trong team. ② Hành động: tuần đầu lập kế hoạch 引継ぎ có checklist, pair-working hằng ngày; xin công ty 1 senior từ dự án khác làm backup giai đoạn test. ③ Báo khách khi đã có phương án: người kế nhiệm, lịch bàn giao, mốc giữ nguyên hay ảnh hưởng ra sao. ④ Gốc: nguyên tắc mỗi module ít nhất 2 người hiểu sâu, tài liệu kiến trúc cập nhật theo sprint.
> 💡 Báo khách khi đã có phương án — khách Nhật lo về 体制 (taisei – đội hình dự án) hơn là lo một cá nhân.

**Q752. Khách sản xuất C ký thêm phase lớn, cần ramp-up team từ 5 lên 20 người trong 1 tháng. Anh/chị xử lý thế nào?**
① Fact: xác định skill cần (ngôn ngữ, domain, tiếng Nhật), nhu cầu người theo tuần; kiểm năng lực tuyển/điều chuyển của công ty. ② Hành động: tăng theo đợt (vd tuần 1–2 thêm 5, tuần 3–4 thêm 10) thay vì một lần; 5 người cũ làm sub-leader, mỗi người kèm 3 người mới; chuẩn bị bộ onboarding (domain, coding convention, môi trường) để rút ngắn thời gian vào việc. ③ Báo khách kế hoạch 体制, năng suất kỳ vọng theo tháng và rủi ro giai đoạn đầu. ④ Kiểm soát chất lượng: review 100% code người mới trong tháng đầu, theo dõi bug theo người.

**Q753. Khách bảo hiểm B yêu cầu thay một developer vì "chậm và hay sai", nhưng em đánh giá bạn ấy đang tiến bộ. Anh/chị xử lý thế nào?**
① Fact: xin khách ví dụ cụ thể, đối chiếu dữ liệu bug/tiến độ của member trong 1–2 tháng. ② Hành động: nếu khách đúng → chuyển member sang phần ít tiếp xúc khách hoặc dự án khác, bố trí người thay có thời gian chồng lấn bàn giao; nếu khách chưa thấy tiến bộ → trình số liệu, xin theo dõi 2–4 tuần với tiêu chí rõ. ③ Báo khách quyết định và kế hoạch, không tranh luận cảm tính. ④ Với member: phản hồi riêng, giữ thể diện, có kế hoạch phát triển cụ thể.

**Q754. Sắp vào 要件定義, dự án cần 4 người giao tiếp trực tiếp với khách bằng tiếng Nhật mức N2 nhưng team chỉ có 1 người. Anh/chị xử lý thế nào?**
① Fact: xác định vai trò nào thật sự cần tiếng Nhật (họp, viết tài liệu, Q&A) và vai trò nào làm qua tài liệu được. ② Hành động: người N2 làm cầu nối chính; xin thêm BrSE/comtor từ pool công ty cho giai đoạn 要件定義; member khác làm qua tài liệu đã dịch, dịch máy chỉ dùng tool công ty cho phép, không đưa dữ liệu khách vào tool công cộng. ③ Báo khách 体制 giao tiếp rõ: ai là đầu mối, ai viết 議事録. ④ Dài hạn: lộ trình học tiếng Nhật cho member, tận dụng chương trình đào tạo tiếng Nhật của công ty.

**Q755. Tết Nguyên đán rơi vào tháng 2, trùng giai đoạn 総合テスト trước 年度末 của khách bảo hiểm B, khách muốn team làm xuyên Tết. Anh/chị xử lý thế nào?**
① Fact: lập lịch nghỉ thực tế từng người, tính effort mất. ② Hành động: đưa lịch Tết vào WBS (nếu chưa, làm ngay), kéo việc lên trước Tết, bố trí ca trực luân phiên tự nguyện có phụ cấp cho hỗ trợ khẩn, dồn lực ngay sau Tết. ③ Báo khách sớm (tham khảo ≥ 2–3 tháng trước) lịch nghỉ và phương án đảm bảo mốc, giải thích Tết với người Việt tương tự お正月 (oshougatsu – Tết của Nhật). ④ Lưu lịch nghỉ hai nước (Tết, Golden Week, お盆 obon) vào template kế hoạch cho mọi dự án.
> 💡 So sánh Tết với お正月 giúp khách Nhật hiểu ngay vì sao không thể làm như bình thường.

**Q756. Hai dự án trong cùng bộ phận cần chung một senior DB, PM dự án kia đang giữ người trong khi dự án của em sắp vào giai đoạn tối ưu performance cho khách. Anh/chị xử lý thế nào?**
① Fact: tính chính xác số ngày công cần, thời điểm, rủi ro với khách nếu thiếu. ② Hành động: gặp trực tiếp PM kia, đề xuất chia lịch (vd 3 ngày/tuần) hoặc pair để chuyển giao kiến thức cho người thứ hai. ③ Không thống nhất được → escalate lên quản lý chung bằng dữ liệu (ảnh hưởng tới khách, doanh thu, cam kết hợp đồng) để quyết theo ưu tiên công ty; báo khách nếu mốc bị ảnh hưởng. ④ Lâu dài: đề xuất kế hoạch nguồn lực cấp bộ phận nhìn trước 1–2 tháng.

**Q757. Khách sản xuất C yêu cầu xem CV và phỏng vấn từng member trước khi họ vào dự án. Anh/chị xử lý thế nào?**
① Fact: hiểu mục đích (lo năng lực, từng gặp member yếu) và xem hợp đồng quy định gì về 体制. ② Hành động: chuẩn bị スキルシート (sukiru shiito – bảng kỹ năng) chuẩn, chỉ gồm thông tin nghề nghiệp, có sự đồng ý của nhân viên khi gửi ra ngoài. ③ Đề xuất với khách: phỏng vấn các vị trí key (PM, tech lead, BrSE); các vị trí khác vendor chịu trách nhiệm tuyển chọn theo tiêu chí kỹ năng đã thống nhất. ④ Theo dõi đánh giá của khách sau tháng đầu để điều chỉnh tiêu chí chọn người.

**Q758. Khách bảo hiểm B cắt ngân sách, yêu cầu giảm team từ 12 xuống 8 người từ tháng sau nhưng giữ nguyên scope và 納期. Anh/chị xử lý thế nào?**
① Fact: tính lại capacity: 8 người làm được bao nhiêu % scope trong thời hạn. ② Hành động: đưa 3 phương án: giữ scope và kéo dài thời gian; giữ 納期 và cắt scope theo ưu tiên; hoặc giảm dần người trong 2 tháng. Chọn 8 người ở lại sao cho không mất key person. ③ Báo khách bằng bảng số liệu, nói rõ giữ nguyên cả scope lẫn thời gian khi giảm 1/3 người là không khả thi nếu không hy sinh chất lượng. ④ Nội bộ: 4 người rời dự án được bàn giao đầy đủ và bố trí sang dự án khác.

**Q759. Khách ngân hàng A muốn ghi vào hợp đồng cam kết không thay đổi thành viên key trong suốt 18 tháng dự án. Anh/chị xử lý thế nào?**
① Fact: xác định danh sách "key" khách muốn (PM, tech lead, BrSE) và rủi ro nghỉ việc thực tế. ② Hành động: không cam kết tuyệt đối điều mình không kiểm soát; đề xuất điều khoản thay thế: báo trước tối thiểu X tuần, người thay có kỹ năng tương đương, thời gian chồng lấn bàn giao Y tuần, khách được phỏng vấn người thay. ③ Báo khách thẳng thắn lý do và cơ chế đảm bảo. ④ Nội bộ: kế hoạch giữ chân key member (lộ trình, thưởng gắn dự án) và backup cho từng vai trò.
> 💡 Hứa điều không kiểm soát được rồi vi phạm còn tệ hơn từ chối có giải thích kèm phương án thay thế.

**Q760. Khách yêu cầu 2 kỹ sư có chứng chỉ AWS cho phần hạ tầng theo quy định nội bộ của họ, công ty chưa có người rảnh đáp ứng. Anh/chị xử lý thế nào?**
① Fact: hỏi khách yêu cầu là bắt buộc chứng chỉ hay chấp nhận kinh nghiệm tương đương, mốc cần người. ② Hành động: ngắn hạn điều chuyển/mượn người có chứng chỉ từ dự án khác hoặc tuyển; song song chọn 2 member tiềm năng ôn thi, tận dụng chính sách hỗ trợ thi Cloud/AWS của công ty. ③ Báo khách 体制 tạm thời và lộ trình đạt chứng chỉ có ngày cụ thể. ④ Lần sau đưa yêu cầu chứng chỉ vào checklist giai đoạn proposal để chuẩn bị người sớm.

## 8.7 Chi phí & hợp đồng

**Q761. Dự án 請負 cho khách bảo hiểm B, đến giữa giai đoạn 製造 đã tiêu vượt 30% effort so với 見積. Anh/chị xử lý thế nào?**
① Fact: phân tích nguồn vượt — estimate sai, CR không thu phí, năng suất thấp hay rework do chất lượng; dự báo tổng chi phí khi hoàn thành (EAC). ② Hành động: tách phần vượt do phía khách (CR, trễ đầu vào) có bằng chứng; tối ưu phần còn lại (tái sử dụng, giảm rework). ③ Báo nội bộ ngay cho cấp trên/tài chính, không giấu; với khách chỉ đề nghị chi phí cho phần có căn cứ hợp đồng. ④ Gốc: cập nhật dữ liệu năng suất cho 見積 (mitsumori – báo giá/ước tính) lần sau, review chi phí theo tháng với ngưỡng cảnh báo (tham khảo lệch > 10%) ngay từ đầu 製造 (seizou – giai đoạn lập trình).
> 💡 Phần vượt do mình estimate sai thì công ty chịu — đừng "hợp thức hóa" bằng CR không có thật.

**Q762. Khách ngân hàng A từ chối trả phí 5 CR đã làm xong, cho rằng đó là "do vendor hiểu sai yêu cầu ban đầu". Anh/chị xử lý thế nào?**
① Fact: với từng CR, gom bằng chứng: tài liệu đã duyệt, 議事録, email yêu cầu, ngày khách xác nhận. ② Hành động: phân loại CR có bằng chứng rõ là thay đổi và CR "vùng xám" (tài liệu gốc mơ hồ). ③ Báo: họp với người có thẩm quyền, trình từng CR kèm bằng chứng; vùng xám có thể nhượng bộ (chia sẻ chi phí) để đổi lấy quy trình CR chặt hơn; số tiền lớn thì sales/ban giám đốc cùng vào. ④ Gốc: không bắt đầu làm CR khi chưa có xác nhận phí bằng văn bản.

**Q763. Sếp yêu cầu nhận dự án mới với giá thấp hơn giá vốn khoảng 15% để vào được một tập đoàn tài chính lớn. Anh/chị xử lý thế nào?**
① Fact: tính rõ giá vốn, mức lỗ dự kiến và rủi ro vượt thêm (khách tài chính yêu cầu chất lượng, bảo mật cao). ② Hành động: không từ chối cảm tính; trình sếp phân tích và điều kiện để nhận: coi là khoản đầu tư có ngân sách lỗ rõ, scope khóa chặt, phase sau giá hợp lý, không cắt bước chất lượng. ③ Nếu công ty quyết nhận: ghi lại quyết định và mức lỗ chấp nhận, không để team phải bù bằng OT. ④ Theo dõi chi phí sát, báo định kỳ, đề xuất ngưỡng dừng/đàm phán lại nếu lỗ vượt mức.
> 💡 Quyết định chiến lược là của công ty, nhưng PM phải đưa đủ số liệu và không để "giá rẻ" biến thành "chất lượng rẻ".

**Q764. Khách sản xuất C đang ký 準委任 theo tháng, giữa chừng muốn chuyển sang 請負 giá cố định cho phần còn lại để chủ động ngân sách. Anh/chị xử lý thế nào?**
① Fact: đánh giá độ rõ của phần còn lại: yêu cầu đã chốt chưa, rủi ro kỹ thuật. ② Hành động: chỉ chuyển sang 請負 phần đã đủ rõ (vd đã xong 基本設計); phần chưa rõ giữ 準委任 (jun-inin – hợp đồng theo công sức, không cam kết kết quả) hoặc chia hợp đồng nhiều giai đoạn; báo giá có risk buffer (tham khảo 10–20% tùy độ rõ). ③ Báo khách: giải thích khác biệt trách nhiệm — 請負 có nghĩa vụ hoàn thành và 契約不適合責任 (keiyaku futekigou sekinin – trách nhiệm khi sản phẩm không đúng hợp đồng), nên giá phản ánh rủi ro. ④ Trước khi ký, chốt tiêu chí 検収 (kenshuu – nghiệm thu) và quy trình CR.

**Q765. Khách yêu cầu báo giá bằng tiếng Nhật cho một hệ thống mới trong 3 ngày, tài liệu chỉ có 5 trang mô tả. Anh/chị xử lý thế nào?**
① Fact: liệt kê chức năng đọc được và điểm chưa rõ. ② Hành động: estimate bằng 2 cách để đối chiếu (WBS sơ bộ + so sánh dự án tương tự), ghi rõ 前提条件 và スコープ外 (sukoopu gai – ngoài phạm vi); đưa khoảng giá hoặc đề xuất 2 bước: 要件定義 theo 準委任 rồi mới báo giá cố định. ③ Gửi đúng hạn theo format khách quen, kèm danh sách câu hỏi và mức tin cậy của con số. ④ Lưu 見積 để so với thực tế khi dự án chạy, cải thiện dữ liệu estimate.
> 💡 Báo giá ghi kỹ 前提条件 là "lá chắn" của vendor khi phạm vi thay đổi — khách Nhật cũng đánh giá cao sự rõ ràng này.

**Q766. Cuối dự án 請負, khách chậm 検収 2 tháng vì "vẫn còn vài bug nhỏ", ảnh hưởng dòng tiền của công ty. Anh/chị xử lý thế nào?**
① Fact: đối chiếu tiêu chí nghiệm thu trong hợp đồng với danh sách bug còn lại và mức độ. ② Hành động: sửa nhanh các bug thuộc trách nhiệm trong 1–2 tuần; bug nhỏ không chặn vận hành → đề xuất 検収 kèm danh sách 残課題 (zankadai – việc còn tồn) và lịch sửa trong thời gian bảo hành. ③ Báo khách bằng văn bản có dẫn điều khoản; nhờ sales/account làm việc với bộ phận mua hàng phía khách. ④ Gốc: hợp đồng sau định nghĩa tiêu chí nghiệm thu đo được (vd 0 bug nghiêm trọng, bug nhỏ ≤ N và có kế hoạch sửa).

**Q767. Dự án 準委任 tính theo người-tháng, khách muốn thêm 1 tester nhưng không muốn tăng tổng chi phí. Anh/chị xử lý thế nào?**
① Fact: khách thực sự cần thêm năng lực test hay cần yên tâm về chất lượng; team hiện có ai chưa dùng hết công suất. ② Hành động: đưa phương án: thay 1 dev bằng tester trong giai đoạn test, tự động hóa regression để tăng năng lực, hoặc tester bán thời gian; nêu đánh đổi tiến độ của từng phương án. ③ Báo khách bảng phương án với chi phí không đổi và ảnh hưởng tương ứng, xin quyết định. ④ Ghi thay đổi 体制 vào biên bản hoặc phụ lục hợp đồng.

**Q768. Sau khi ký 請負, team phát hiện 見積 đã bỏ sót hẳn hạng mục batch đối soát, chiếm khoảng 15% effort, khách chưa biết. Anh/chị xử lý thế nào?**
① Fact: kiểm hạng mục có trong tài liệu yêu cầu khách đưa lúc báo giá không — có thì lỗi estimate là của mình. ② Hành động: lỗi của mình → vẫn làm đủ, công ty chịu chi phí, tìm cách tối ưu (tái sử dụng, thiết kế đơn giản trong phạm vi yêu cầu); nếu yêu cầu gốc không có → xử lý như CR. ③ Báo nội bộ ngay để điều chỉnh dự báo lợi nhuận; với khách, trung thực về ảnh hưởng lịch nếu có, không đòi phí phần lỗi của mình. ④ Gốc: checklist estimate (batch, migration, phi chức năng, vận hành) và review chéo trước khi gửi báo giá.

**Q769. Đồng Yên mất giá làm biên lợi nhuận dự án 準委任 dài hạn với khách bảo hiểm B giảm rõ, công ty muốn đàm phán tăng đơn giá ở kỳ gia hạn. Anh/chị xử lý thế nào?**
① Fact: chuẩn bị dữ liệu: năng suất, chất lượng, các cải tiến team đã mang lại, đơn giá hiện tại và chi phí tăng. ② Hành động: cùng sales chuẩn bị đề xuất từ 2–3 tháng trước kỳ gia hạn, kèm giá trị gia tăng (tự động hóa, nâng kỹ năng, giảm sự cố) để khách có lý do trình nội bộ. ③ PM không tự đàm phán giá một mình — cung cấp dữ liệu và nói về giá trị; có thể đề xuất tăng theo lộ trình. ④ Song song tối ưu chi phí nội bộ (tỉ lệ senior/junior) để giảm rủi ro nếu tăng giá không được như kỳ vọng.
> 💡 Khách Nhật cần lý do để giải trình với cấp trên (説明責任 setsumei sekinin – trách nhiệm giải trình): đưa họ tài liệu để họ tự trình nội bộ.

**Q770. Khách đòi vendor chịu chi phí sửa một lỗi phát hiện sau 8 tháng go-live, trong khi thời hạn bảo hành trong hợp đồng là 6 tháng. Anh/chị xử lý thế nào?**
① Fact: xác định đây là lỗi không đúng spec của mình hay do thay đổi môi trường/cách dùng; đọc điều khoản bảo hành và 契約不適合責任. ② Hành động: lỗi nhỏ, rõ do mình → cân nhắc sửa miễn phí như thiện chí, ghi rõ là ngoại lệ; lỗi lớn → đề xuất tính phí hoặc chia sẻ chi phí. ③ Báo khách khéo: ưu tiên giải quyết vấn đề vận hành trước, chi phí thảo luận song song qua sales. ④ Đề xuất hợp đồng 保守 (hoshu – bảo trì) dài hạn để những tình huống sau có khung rõ ràng.

## 8.8 Xung đột & stakeholder

**Q771. Phòng kế toán và phòng kinh doanh của khách sản xuất C đưa ra yêu cầu mâu thuẫn về cách tính và hiển thị đơn hàng, bên nào cũng muốn theo ý mình. Anh/chị xử lý thế nào?**
① Fact: viết 2 yêu cầu dạng bảng so sánh, nêu tác động mỗi phương án (effort, nghiệp vụ, rủi ro). ② Hành động: không tự chọn bên; đề xuất phương án dung hòa nếu có (vd cấu hình theo vai trò) kèm chi phí. ③ Báo 窓口/chủ dự án phía khách quyết định, đề nghị họp 3 bên có người quyết định; ghi kết quả vào 議事録. ④ Gốc: đề nghị khách xác định người có quyền quyết định cuối cho từng loại yêu cầu (RACI phía khách).
> 💡 Vendor đứng ra phân xử nội bộ khách là tự biến mình thành "người bị ghét" — chuẩn bị dữ liệu và để người của khách quyết.

**Q772. Trong 受入テスト, người dùng cuối phía khách phản đối luồng nghiệp vụ mà 窓口 đã chốt ở 要件定義: "Thế này không ai dùng được". Anh/chị xử lý thế nào?**
① Fact: thu thập phản hồi cụ thể (bước nào, vì sao khó), đối chiếu tài liệu đã chốt. ② Hành động: lập danh sách điểm cần đổi + estimate, phân loại bắt buộc cho go-live hay cải tiến sau. ③ Báo 窓口 trước, không vượt mặt; giúp 窓口 giữ thể diện bằng cách trình là "phản hồi thực tế từ người dùng" kèm đề xuất CR có ưu tiên. ④ Gốc: lần sau mời người dùng cuối review prototype sớm ở 要件定義/基本設計.

**Q773. Trong họp, trưởng phòng phía khách nổi giận, nói to và chỉ trích team trước nhiều người vì một lỗi production. Anh/chị xử lý thế nào?**
① Fact: lắng nghe hết, không ngắt lời, không giải thích ngay; ghi lại các điểm khách nêu. ② Hành động: xin lỗi chân thành về ảnh hưởng gây ra (chưa cần kết luận nguyên nhân khi chưa rõ), nói rõ việc đang làm và giờ báo cáo tiếp. ③ Sau họp trong ngày: email tóm tắt, báo cấp trên, xin gặp riêng trưởng phòng cùng cấp trên của mình với báo cáo sự cố sơ bộ. ④ Giữ đúng mọi mốc đã hứa để lấy lại niềm tin; bảo vệ team, không trút áp lực xuống member.
> 💡 Trong cuộc họp nóng chỉ cần ① tiếp nhận ② xin lỗi về ảnh hưởng ③ hẹn mốc — tranh luận nguyên nhân để buổi sau, có dữ liệu.

**Q774. 担当者 phía khách đổi người giữa dự án, người mới không đồng ý nhiều quyết định người cũ đã chốt và muốn xem lại spec từ đầu. Anh/chị xử lý thế nào?**
① Fact: chuẩn bị hồ sơ: tài liệu đã duyệt, 議事録, các quyết định và lý do. ② Hành động: tổ chức buổi 引継ぎ cho người mới (mời cả người cũ nếu được), giải thích bối cảnh từng quyết định. ③ Báo: điểm nào người mới muốn đổi thì xử lý như CR với ảnh hưởng chi phí/lịch; thay đổi lớn thì trình cấp trên phía khách. ④ Xây quan hệ: họp 1–1 tìm hiểu mục tiêu của người mới, chọn 1–2 cải tiến nhỏ giúp họ có kết quả sớm — người mới thường muốn để lại dấu ấn, hãy giúp họ thành công trong phạm vi có kiểm soát.

**Q775. Cấp trên của 窓口 gửi email trực tiếp cho em, yêu cầu thêm một tính năng mà 窓口 không biết. Anh/chị xử lý thế nào?**
① Fact: ghi nhận yêu cầu, đánh giá ảnh hưởng sơ bộ. ② Hành động: trả lời lịch sự xác nhận đã nhận, nói sẽ phối hợp với 窓口 để đánh giá và trả lời; báo ngay cho 窓口 (cc hoặc báo riêng). ③ Cùng 窓口 đưa estimate và trình lại; không làm ngay chỉ vì người yêu cầu có chức vụ cao. ④ Gốc: nhắc lại quy trình tiếp nhận yêu cầu trong 定例会, giữ 窓口 ở vị trí trung tâm để không ai mất mặt.

**Q776. Khách muốn team bổ sung miễn phí 2 người trong tháng cao điểm, trong khi ban giám đốc yêu cầu dự án phải tăng biên lợi nhuận quý này. Anh/chị xử lý thế nào?**
① Fact: nhu cầu thật của khách (khối lượng, thời gian), chi phí 2 người × 1 tháng, giá trị quan hệ (phase tiếp, tiềm năng mở rộng). ② Hành động: tìm phương án giữa: hỗ trợ miễn phí 1 người trong 2 tuần đỉnh điểm, phần còn lại tính phí; hoặc đổi lấy cam kết phase tiếp. ③ Báo ban giám đốc phân tích chi phí–lợi ích, xin quyết định; báo khách phương án cụ thể. ④ Ghi rõ thỏa thuận là ngoại lệ có thời hạn để không thành tiền lệ "miễn phí" lặp lại.

**Q777. Khách sản xuất C ra quyết định rất chậm vì mỗi CR phải qua 稟議 nhiều cấp, mất 3–4 tuần, dự án bị đình trệ. Anh/chị xử lý thế nào?**
① Fact: vẽ lại quy trình 稟議 (ringi – xin phê duyệt nội bộ qua nhiều cấp) của khách: ai duyệt, mất bao lâu, cần tài liệu gì. ② Hành động: soạn tài liệu CR đúng format khách cần để trình (lý do, chi phí, rủi ro nếu không làm); đẩy sớm các quyết định dự đoán được; gom CR thành đợt. ③ Báo: thống nhất với 窓口 lịch quyết định, đưa vào kế hoạch dự án như một ràng buộc có mốc. ④ Đề xuất cơ chế ngân sách dự phòng cho CR nhỏ (dưới ngưỡng thì 窓口 tự duyệt).
> 💡 Soạn sẵn tài liệu trình 稟議 giúp 担当者 là cách nhanh nhất để rút ngắn thời gian quyết định.

**Q778. Khách gửi email lúc 22h giờ Nhật yêu cầu trả lời trước 9h sáng hôm sau về nguyên nhân một lỗi hiển thị nhỏ, team đã hết giờ làm. Anh/chị xử lý thế nào?**
① Fact: xác định mức độ: lỗi nhỏ, không ảnh hưởng vận hành. ② Hành động: PM trả lời ngắn ngay tối đó: đã nhận, sẽ điều tra đầu giờ, hẹn mốc cụ thể (vd 11h giờ Nhật, tức 9h Việt Nam); sáng hôm sau giao người điều tra ngay. ③ Báo khách đúng mốc đã hẹn, kèm nguyên nhân và kế hoạch sửa. ④ Gốc: thống nhất với khách SLA phản hồi theo mức độ sự cố (lỗi nghiêm trọng 24/7, lỗi nhỏ trong giờ làm việc) và ghi vào tài liệu vận hành.

**Q779. Khách ngân hàng A thêm một vendor khác làm song song các module khác và giao PM bên mình điều phối cả vendor kia. Anh/chị xử lý thế nào?**
① Fact: làm rõ vai trò — điều phối lịch/kỹ thuật hay chịu trách nhiệm kết quả của vendor kia; hợp đồng nói gì. ② Hành động: đề xuất thỏa thuận bằng văn bản về phạm vi điều phối, quyền hạn, trách nhiệm (không chịu trách nhiệm chất lượng của bên không ký hợp đồng với mình); dựng interface spec, lịch tích hợp, 課題管理表 chung. ③ Báo khách cơ chế điều phối và mẫu báo cáo chung. ④ Bảo vệ thông tin nội bộ (giá, nguồn lực, tài sản trí tuệ) khi làm việc chung.
> 💡 "Điều phối" mà không có quyền hạn rõ là cái bẫy: nhận trách nhiệm nhưng không có quyền.

**Q780. Sales của công ty đã hứa miệng với khách bảo hiểm B sẽ làm thêm module báo cáo trong cùng ngân sách để chốt hợp đồng, team delivery không được báo. Anh/chị xử lý thế nào?**
① Fact: xác nhận với sales nội dung đã hứa, có văn bản không; estimate module. ② Hành động: họp nội bộ với sales + cấp trên, đưa số liệu ảnh hưởng (lợi nhuận, lịch); thống nhất một tiếng nói trước khi trao đổi với khách. ③ Báo khách: nếu công ty giữ lời → lên kế hoạch thực hiện; nếu không → sales và PM cùng gặp khách giải thích, đưa phương án (phase sau, giá ưu đãi). ④ Gốc: quy trình bàn giao sales → delivery có danh sách cam kết, PM review proposal trước khi gửi.

## 8.9 Bảo mật & tuân thủ

**Q781. Phát hiện một developer đã dán source code và dữ liệu mẫu của khách ngân hàng A vào ChatGPT bản cá nhân để debug. Anh/chị xử lý thế nào?**
① Fact: hỏi riêng member ngay: dán gì, khi nào, bao nhiêu lần, có dữ liệu cá nhân hay secret không; lưu lại bằng chứng. ② Hành động: dừng ngay; secret bị lộ thì rotate trong ngày; báo bộ phận bảo mật nội bộ để đánh giá theo quy trình sự cố (lưu ý không đảm bảo xóa được dữ liệu đã gửi ra ngoài). ③ Báo khách: đây có thể là sự cố rò rỉ thông tin theo NDA — cùng pháp lý/ban giám đốc báo khách trung thực, đúng hạn hợp đồng yêu cầu. ④ 再発防止: chính sách dùng AI rõ (tool được phép, dữ liệu cấm), chặn kỹ thuật, đào tạo, 横展開 toàn công ty.
> 💡 Giấu sự cố rò rỉ là lỗi lớn hơn chính sự cố — với khách tài chính Nhật, báo sớm là điều kiện để còn giữ được hợp đồng.

**Q782. Member báo mất laptop công ty chứa source code dự án khách bảo hiểm B trên taxi tối qua. Anh/chị xử lý thế nào?**
① Fact: thời điểm, nơi mất, ổ đĩa có mã hóa không, có dữ liệu cá nhân của khách không, những tài khoản nào đang đăng nhập. ② Hành động trong vài giờ đầu: IT khóa/xóa từ xa nếu có MDM, đổi mật khẩu, thu hồi token/VPN/SSH key; liên hệ hãng taxi và báo cơ quan chức năng. ③ Báo bộ phận bảo mật, và gửi khách 第一報 trong thời hạn hợp đồng quy định, kèm đánh giá rủi ro. ④ 再発防止: bắt buộc mã hóa ổ đĩa, không lưu dữ liệu khách trên máy local, quy định mang thiết bị ra ngoài; 横展開 kiểm toàn bộ máy trong dự án.

**Q783. Member gửi nhầm email đính kèm tài liệu 基本設計 của khách sản xuất C cho một khách hàng khác của công ty. Anh/chị xử lý thế nào?**
① Fact: ai gửi, lúc nào, cho ai, đính kèm gì, mức mật của tài liệu. ② Hành động: liên hệ ngay người nhận nhầm, đề nghị xóa, không chuyển tiếp và xác nhận đã xóa bằng văn bản; thử thu hồi email nếu hệ thống hỗ trợ. ③ Báo bộ phận bảo mật và báo khách C trung thực, sớm, kèm xác nhận xóa của bên nhận. ④ 再発防止: cảnh báo khi gửi ra ngoài domain, gửi file qua link có phân quyền thay vì đính kèm, ダブルチェック địa chỉ với tài liệu mật.
> 💡 Văn bản xác nhận đã xóa từ người nhận nhầm là bằng chứng quan trọng nhất trong báo cáo sự cố gửi khách.

**Q784. Phát hiện một member đăng ảnh chụp màn hình giao diện hệ thống khách lên mạng xã hội để khoe dự án. Anh/chị xử lý thế nào?**
① Fact: chụp lại bài đăng làm bằng chứng, xác định thông tin bị lộ (tên khách, dữ liệu, URL nội bộ), mức lan truyền nếu biết. ② Hành động: yêu cầu gỡ ngay, kiểm tra các bài đăng khác; báo bộ phận bảo mật. ③ Báo khách nếu có thông tin khách bị lộ, theo đúng NDA, kèm bằng chứng đã gỡ. ④ Nhắc lại quy định NDA cho cả team, xử lý theo quy chế công ty; đưa tình huống thật (ẩn danh) vào đào tạo onboarding.

**Q785. Audit ISMS nội bộ phát hiện dự án ngân hàng A có 6 điểm không phù hợp: dùng tài khoản chung, không review quyền truy cập định kỳ, log không lưu đủ thời hạn. Anh/chị xử lý thế nào?**
① Fact: xác nhận từng điểm, mức độ, nguyên nhân (thiếu quy trình hay không tuân thủ). ② Hành động: lập kế hoạch 是正処置 (zesei shochi – hành động khắc phục) có người phụ trách + hạn: xóa tài khoản chung trong 1 tuần, review quyền hằng tháng, cấu hình lưu log đúng yêu cầu. ③ Báo cấp trên; nếu hợp đồng yêu cầu báo khách về kết quả audit/vi phạm thì báo kèm kế hoạch khắc phục. ④ 横展開 sang các dự án khác, đưa các điểm này vào checklist kickoff dự án.

**Q786. Khách bảo hiểm B yêu cầu dữ liệu test phải được ẩn danh, nhưng team đang dùng bản copy dữ liệu production thật trên môi trường dev. Anh/chị xử lý thế nào?**
① Fact: dữ liệu được copy từ khi nào, theo chỉ thị của ai, ai có quyền truy cập, có lưu ở nơi nào ngoài môi trường được phép. ② Hành động: dừng dùng ngay, xóa dữ liệu thật theo quy trình có biên bản xác nhận, thay bằng dữ liệu đã masking. ③ Báo khách qua bộ phận bảo mật: đây có thể vi phạm điều khoản xử lý dữ liệu — báo trung thực kèm biện pháp đã làm. ④ Phòng ngừa: tool masking tự động, phân quyền môi trường, checklist dữ liệu test trước mỗi giai đoạn.

**Q787. Khách yêu cầu điền checklist bảo mật khoảng 200 mục trong 1 tuần trước khi cấp VPN vào môi trường của họ. Anh/chị xử lý thế nào?**
① Fact: phân loại câu hỏi: mục thuộc chính sách công ty (bộ phận bảo mật trả lời) và mục thuộc dự án (PM trả lời). ② Hành động: phối hợp bộ phận ISMS dùng câu trả lời chuẩn đã có, trả lời trung thực; mục chưa đáp ứng → ghi rõ kế hoạch và ngày đáp ứng. ③ Nộp đúng hạn, kèm danh sách mục đang khắc phục. ④ Lưu bộ câu trả lời làm tài sản dùng lại cho khách sau.
> 💡 Không bao giờ ghi "có" cho mục chưa làm — checklist bảo mật thường bị khách audit lại sau này.

**Q788. Member muốn dùng một thư viện mã nguồn mở license GPL trong sản phẩm giao cho khách sản xuất C để kịp tiến độ. Anh/chị xử lý thế nào?**
① Fact: kiểm license — GPL có thể buộc công bố mã nguồn khi phân phối sản phẩm phái sinh, tùy cách dùng; xem quy định OSS của khách. ② Hành động: tạm chưa dùng đến khi có kết luận; tìm thư viện thay thế license dễ dãi hơn (MIT, Apache 2.0). ③ Báo khách: nếu buộc phải dùng, xin phê duyệt bằng văn bản theo quy định OSS của khách. ④ Phòng ngừa: danh sách license được phép, tool scan license trong CI, nộp danh sách OSS khi bàn giao.

**Q789. Khách yêu cầu team làm trong phòng riêng có kiểm soát ra vào, cấm điện thoại, nhưng văn phòng Đà Nẵng chưa có phòng như vậy. Anh/chị xử lý thế nào?**
① Fact: đọc chi tiết yêu cầu (thẻ ra vào, camera, cấm thiết bị cá nhân, máy khóa USB) và hạn phải đáp ứng. ② Hành động: phối hợp admin/IT ước tính chi phí, thời gian thiết lập; trong lúc chờ đề xuất phương án tạm khách chấp nhận được (khu vực ngăn riêng, máy khóa USB, làm qua VDI). ③ Báo khách lịch đáp ứng và phương án tạm, mời khách kiểm tra online hoặc trực tiếp. ④ Đưa chi phí bảo mật vật lý vào 見積 cho các dự án tài chính sau.

**Q790. Phát hiện một member đã nghỉ việc 2 tuần nhưng tài khoản Git và VPN vào môi trường khách vẫn còn hoạt động. Anh/chị xử lý thế nào?**
① Fact: kiểm log truy cập từ ngày nghỉ đến nay có hoạt động không. ② Hành động: khóa ngay mọi tài khoản, rotate các secret dùng chung người đó từng biết. ③ Báo bộ phận bảo mật; nếu log có truy cập bất thường hoặc hợp đồng yêu cầu thì báo khách. ④ 再発防止: checklist offboarding gắn với HR (khóa quyền ngay trong ngày nghỉ), review quyền định kỳ hằng tháng, 横展開 rà toàn bộ tài khoản dự án.

## 8.10 Tình huống xám, đạo đức & tổng hợp

**Q791. 担当者 phía khách gợi ý: "Báo cáo chất lượng gửi lên cấp trên nên ghi số bug ít đi, không thì tôi khó giải thích". Anh/chị xử lý thế nào?**
① Fact: hiểu áp lực của 担当者, nhưng sửa số là làm sai lệch hồ sơ, người chịu trách nhiệm cuối cùng là vendor. ② Hành động: từ chối khéo, không đổi số; đề xuất cách trình bày giúp họ: phân loại theo mức độ, xu hướng giảm, tỉ lệ đã sửa, nguyên nhân chính đã xử lý. ③ Báo cấp trên của mình biết sự việc, không làm to chuyện phía khách để giữ thể diện 担当者. ④ Nguyên tắc: số liệu đúng + diễn giải có lợi cho khách thì được; ngụy tạo thì không, vì khi lộ ra cả hai bên mất uy tín.
> 💡 Câu xám: nói rõ nguyên tắc "không sửa số, nhưng giúp diễn giải" — interviewer muốn thấy bạn có giới hạn đạo đức nhưng vẫn mềm dẻo.

**Q792. Dự án trễ 2 tuần, sếp bảo cứ báo khách "đúng tiến độ" đến sau buổi review nội bộ tuần sau vì sợ ảnh hưởng đánh giá. Anh/chị xử lý thế nào?**
① Fact: kiểm lại mức trễ và tính khả thi của kế hoạch phục hồi. ② Hành động: gặp riêng sếp, trình rủi ro: khách tự phát hiện thì mất niềm tin, giấu thêm 1 tuần là mất 1 tuần xử lý; đề xuất báo khách ngay kèm kế hoạch phục hồi — thành câu chuyện "phát hiện sớm, chủ động xử lý", có lợi cả cho buổi review. ③ Nếu sếp vẫn yêu cầu giấu: không gửi báo cáo sai, escalate theo kênh phù hợp (PMO/cấp cao hơn). ④ Nguyên tắc: trung thực với khách là giới hạn không đánh đổi; thời điểm và cách nói thì thương lượng được.

**Q793. Còn 3 ngày đến 納期, còn 8 bug mức trung bình chưa sửa, khách nói "giao đúng ngày là quan trọng nhất" còn team muốn xin thêm 1 tuần. Anh/chị xử lý thế nào?**
① Fact: phân tích 8 bug: ảnh hưởng nghiệp vụ, có workaround không, có rủi ro dữ liệu/tiền/bảo mật không. ② Hành động: sửa trước bug ảnh hưởng dữ liệu/tiền; bug có workaround thì giao đúng ngày kèm 既知不具合一覧 (kichi fuguai ichiran – danh sách lỗi đã biết) và lịch sửa. ③ Báo khách trước 2 ngày, để khách quyết với đủ thông tin. ④ Nguyên tắc chọn: lỗi gây sai dữ liệu, tiền hoặc bảo mật thì không giao dù trễ; lỗi hiển thị có workaround thì ưu tiên 納期 — người quyết cuối cùng là khách.
> 💡 Câu "chọn A hay B" không có đáp án đúng — điểm nằm ở tiêu chí chọn rõ ràng và việc khách được quyết với đủ thông tin.

**Q794. Anh/chị quản lý 2 dự án cùng lúc, cùng một tuần cả hai chuyển đỏ: dự án ngân hàng A trễ mốc, dự án sản xuất C có sự cố production. Anh/chị xử lý thế nào?**
① Fact: xếp ưu tiên theo nguyên tắc an toàn dữ liệu/vận hành của khách > cam kết hợp đồng > tiến độ nội bộ → sự cố C là số 1. ② Hành động: PM trực tiếp chỉ huy sự cố ở C; dự án A giao tech lead/sub-PM chạy kế hoạch phục hồi, PM duyệt 15 phút mỗi ngày. ③ Báo cả 2 khách trung thực trong phạm vi từng bên; xin cấp trên thêm người hoặc PM hỗ trợ tạm thời. ④ Sau khủng hoảng: đánh giá lại khả năng ôm 2 dự án, đề xuất deputy PM cho mỗi dự án.

**Q795. Anh/chị tiếp nhận một dự án 炎上 từ PM khác vừa nghỉ: trễ 6 tuần, khách mất niềm tin, team kiệt sức. Anh/chị xử lý thế nào trong 2 tuần đầu?**
① Fact (tuần 1): gặp khách nghe trực tiếp, 1–1 với từng member, tự rà tiến độ thật, chất lượng, hợp đồng, issue mở — không tin báo cáo cũ. ② Hành động: ổn định ngay: tạm đóng băng thay đổi mới, dồn lực cho issue chặn, cắt OT vô ích, xin công ty thêm senior. ③ Báo khách cuối tuần 2: hiện trạng trung thực + 再計画 (saikeikaku – lập lại kế hoạch) có mốc thực tế, tần suất báo cáo dày hơn. ④ Phân tích vì sao dự án 炎上 (enjou – "cháy", khủng hoảng) — estimate, scope hay đội hình — và tạo vài kết quả nhanh để lấy lại niềm tin.
> 💡 Đừng hứa ngày mới trước khi tự kiểm hết thực trạng — kế hoạch phục hồi lần 2 mà lại trễ thì gần như hết đường.

**Q796. Khách bảo hiểm B hỏi bóng gió về hệ thống công ty đang làm cho một công ty bảo hiểm khác, muốn "tham khảo cách họ làm". Anh/chị xử lý thế nào?**
① Fact: đây là thông tin mật của khách khác theo NDA, dù khách hỏi với thiện ý. ② Hành động: từ chối lịch sự, rõ ràng: "Chúng tôi không thể chia sẻ thông tin của khách hàng khác, cũng như chúng tôi bảo vệ thông tin của quý công ty". ③ Đề xuất thay thế: chia sẻ kiến thức chung của ngành, best practice công khai, hoặc giải pháp dựa trên kinh nghiệm tổng quát không lộ chi tiết. ④ Nhắc team không trao đổi chéo thông tin giữa các dự án cùng ngành; lời từ chối này thường làm khách tin mình hơn.

**Q797. Team tự phát hiện một lỗi tiềm ẩn trong phần đã bàn giao và khách đã 検収 từ 3 tháng trước, khách chưa biết, sửa mất khoảng 5 ngày công không ai trả. Anh/chị xử lý thế nào?**
① Fact: đánh giá mức độ, điều kiện xảy ra, đã ảnh hưởng dữ liệu thật chưa. ② Hành động: chuẩn bị bản sửa và test ngay. ③ Báo khách chủ động: lỗi gì, điều kiện, ảnh hưởng, đề xuất bản sửa và thời điểm release; chi phí công ty chịu nếu là lỗi của mình. ④ Phân tích vì sao lọt test, 横展開 sang phần tương tự. Nguyên tắc: báo trước khi khách gặp sự cố — 5 ngày công rẻ hơn rất nhiều so với mất niềm tin khi lỗi nổ trên production.

**Q798. Để kịp 納期, khách muốn cắt 結合テスト từ 4 tuần xuống 2 tuần và nói sẽ tự chịu rủi ro. Anh/chị xử lý thế nào?**
① Fact: xác định test case rủi ro cao (tiền, interface ngoài, dữ liệu, bảo mật). ② Hành động: đề xuất test theo rủi ro: 2 tuần cho case ưu tiên cao + regression tự động, phần còn lại chạy song song sau đó hoặc gộp vào 受入テスト. ③ Báo khách bằng văn bản: phạm vi test bị cắt, rủi ro cụ thể, xin khách xác nhận chấp nhận rủi ro bằng văn bản. ④ Nguyên tắc: khách có quyền chọn rủi ro, PM có nghĩa vụ làm rõ và lưu bằng chứng; phần test liên quan tiền/pháp lý thì kiên quyết giữ.

**Q799. Khách sản xuất C ngỏ ý muốn tuyển 2 member giỏi nhất của team về làm cho công ty con của họ với lương cao hơn. Anh/chị xử lý thế nào?**
① Fact: xác nhận đề nghị là chính thức hay xã giao; hợp đồng có điều khoản không lôi kéo nhân sự không. ② Hành động: báo cấp trên/sales ngay; nói chuyện với 2 member để hiểu nguyện vọng, không đe dọa. ③ Phản hồi khách qua cấp quản lý, khéo léo nhắc điều khoản hợp đồng và đề xuất phương án khác (bố trí team dedicated, cử member onsite). ④ Nội bộ: rà lại đãi ngộ, lộ trình cho key member; giảm phụ thuộc vào 2 người bằng chia sẻ kiến thức.

**Q800. Tình huống tổng hợp: dự án ngân hàng A đang 総合テスト, cùng tuần BrSE nghỉ ốm 2 tuần, khách đổi 担当者, và phát hiện một lỗi tính phí trên production từ release trước. Anh/chị xử lý thế nào?**
① Fact (ngày 1): xếp ưu tiên — lỗi production liên quan tiền là số 1; hai việc còn lại là rủi ro vận hành dự án. ② Hành động: PM trực tiếp chỉ huy sự cố (khoanh vùng, 暫定対応); người giỏi tiếng Nhật nhất tạm thay BrSE, xin công ty hỗ trợ BrSE; 総合テスト tiếp tục dưới test lead. ③ 報連相: gửi 第一報 sự cố cho khách ngay; giới thiệu người thay BrSE; gặp 担当者 mới với hồ sơ bàn giao. ④ Trong 1–2 tuần: 障害報告書 + 再発防止, cập nhật kế hoạch test, thiết lập backup cố định cho vai trò cầu nối.
> 💡 Câu tổng hợp kiểm tra khả năng xếp ưu tiên: nói thứ tự và lý do trước, rồi mới kể hành động.
