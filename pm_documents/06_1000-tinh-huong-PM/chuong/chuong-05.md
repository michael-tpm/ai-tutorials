# Chương 5 · Chất lượng deliverable theo chuẩn khách Nhật và tuân thủ bảo mật ngành bảo hiểm (Q501–Q625)

## 5.1 Tài liệu thiết kế (基本設計書, 詳細設計書)

**Q501. Khách bảo hiểm nhân thọ B trả lại 基本設計書 (kihon sekkei-sho – tài liệu thiết kế cơ bản) bản đầu với 37 chỉ trích, trong đó 22 chỉ trích là 誤字脱字 (goji datsuji – lỗi chính tả, sót chữ) và dùng thuật ngữ không thống nhất. Việc đầu tiên PM làm là gì?**
① Em phân loại 37 chỉ trích vào 指摘管理表 (bảng quản lý chỉ trích) theo nhóm: chính tả, thuật ngữ, nội dung nghiệp vụ, format, để thấy 60% là lỗi "không đáng có". ② Sửa ngay toàn bộ, đồng thời quét cả tài liệu (không chỉ chỗ bị chỉ) bằng tool kiểm chính tả và bảng 用語集 (yougoshuu – bảng thuật ngữ). ③ Báo khách trong 1–2 ngày: số lỗi đã sửa, nguyên nhân, biện pháp, kèm lời xin lỗi ngắn gọn, không biện minh. ④ Phân tích gốc: thiếu bước self-check và không có bảng thuật ngữ chung; bổ sung checklist chính tả và review thuật ngữ trước khi nộp, áp dụng 横展開 (yokotenkai – nhân rộng phòng ngừa) cho các tài liệu khác đang viết.
> 📘 PMP: Control Quality kết hợp Pareto: tập trung vào nhóm lỗi chiếm tỷ trọng lớn nhất trước, rồi cập nhật quality checklist trong Manage Quality.
> 💡 Nhật: Khách Nhật đánh giá "品質意識" (ý thức chất lượng) qua lỗi chính tả; 22 lỗi nhỏ gây mất niềm tin nặng hơn 1 lỗi logic lớn.

**Q502. Dự án 請負 (ukeoi – trọn gói) cho ngân hàng A, team offshore 20 người sẽ code từ 詳細設計書 (shousai sekkei-sho – thiết kế chi tiết) do team onsite viết. Dev phàn nàn tài liệu quá sơ sài, 30% câu hỏi QA là về logic không ghi trong tài liệu. PM điều chỉnh độ chi tiết thế nào?**
① Em lấy danh sách câu hỏi QA, phân loại vùng thiếu: điều kiện rẽ nhánh, xử lý lỗi, giá trị biên, mapping item. ② Thống nhất "mức chi tiết tối thiểu" bằng mẫu: mỗi xử lý phải có input/output, điều kiện, xử lý ngoại lệ, message ID; dev đọc xong viết được code mà không phải hỏi. ③ Báo PM onsite và lãnh đạo: chi phí QA hiện tại (giờ chờ, giờ hỏi đáp) để có lý do bổ sung công sức viết lại. ④ Gốc rễ là không có tiêu chí "xong" cho tài liệu; đưa tiêu chí vào checklist review và cho dev offshore đọc thử 1 module trước khi viết hàng loạt.
> 📘 PMP: Plan Quality Management: định nghĩa quality metrics và tiêu chí chấp nhận cho deliverable trung gian, không chỉ cho sản phẩm cuối.

**Q503. Khách bảo hiểm B đang review 基本設計書 bản v1.3 thì team gửi v1.4 có sửa thêm. Khách viết chỉ trích lên v1.3, trong đó 9 chỉ trích đã được sửa ở v1.4, khách bực vì "mất công review lại". PM xử lý và phòng ngừa thế nào?**
① Em đối chiếu 9 chỉ trích với v1.4, ghi rõ trạng thái "đã sửa ở v1.4, mục X" trong 指摘管理表 để khách không phải tìm. ② Thống nhất ngay với khách: trong thời gian khách review, team **đóng băng** bản đang review, mọi sửa đổi gom lại và phát hành 1 lần sau khi nhận chỉ trích. ③ Xin lỗi vì gây lãng phí thời gian khách, báo quy tắc phát hành mới trong 定例会 (teireikai – họp định kỳ). ④ Đưa quy tắc version vào kế hoạch quản lý tài liệu: ai được phát hành, đánh số version, ghi 改訂履歴 (kaitei rireki – lịch sử sửa đổi) và kênh phát hành duy nhất.
> 📘 PMP: Configuration Management trong Perform Integrated Change Control: kiểm soát phiên bản deliverable, baseline bản đang review.
> 💡 Nhật: Thời gian review của khách là chi phí của họ; gửi bản mới khi khách đang đọc bản cũ bị xem là thiếu tôn trọng.

**Q504. Khi viết 詳細設計書, team phát hiện 12 chỗ tên item màn hình khác với 基本設計書 đã được khách duyệt (ví dụ "契約者名" và "契約者氏名"). Dev đề nghị cứ dùng tên mới vì "nghĩa giống nhau". PM quyết định thế nào?**
① Em xác nhận 12 chỗ khác nhau là do lỗi viết hay do thay đổi có chủ đích. ② Nguyên tắc: 基本設計書 đã duyệt là baseline, 詳細設計書 phải dùng đúng tên ở baseline; nếu tên mới thật sự tốt hơn thì phải sửa cả 基本設計書 và xin khách duyệt lại, không sửa một phía. ③ Báo khách danh sách 12 điểm, đề xuất thống nhất theo 1 tên, kèm ảnh hưởng (màn hình, CSV, báo cáo). ④ Phòng ngừa: lập 項目定義書 (bảng định nghĩa item) dùng chung làm nguồn duy nhất, các tài liệu tham chiếu ID item thay vì gõ lại tên.
> 📘 PMP: Requirements traceability matrix giúp đảm bảo tính nhất quán giữa các tầng deliverable; thay đổi baseline phải qua change control.
> 💡 Nhật: Với khách bảo hiểm, "契約者名" và "契約者氏名" có thể là hai trường khác nhau trên hợp đồng; đừng tự cho là đồng nghĩa.

**Q505. 詳細設計書 do team Việt Nam viết bằng tiếng Việt, comtor dịch sang tiếng Nhật có dùng công cụ dịch nội bộ được phép. Khách phản hồi nhiều câu "không tự nhiên, khó hiểu", có câu nghĩa ngược. PM cải thiện thế nào?**
① Em lấy mẫu 3–5 trang, nhờ BrSE đánh giá lỗi thuộc loại nào: sai thuật ngữ nghiệp vụ, câu quá dài, sai chủ ngữ, sai phủ định. ② Hành động ngay: BrSE review lại các câu chứa logic điều kiện (phủ định, "trừ khi", "ngoại trừ") trước, vì sai nghĩa ở đây gây bug. ③ Báo khách kế hoạch sửa và thời điểm nộp lại. ④ Phòng ngừa: viết nguồn tiếng Việt theo câu ngắn có cấu trúc (điều kiện → xử lý), dùng 用語集 song ngữ, thêm bước 逆翻訳 (dịch ngược) cho phần logic quan trọng, và để dev viết bằng mẫu bảng thay vì văn xuôi.
> 📘 PMP: Manage Quality: cải tiến quy trình tạo deliverable (process improvement) thay vì chỉ sửa đầu ra.

**Q506. Khách phi nhân thọ C hỏi: "v2.0 và v2.1 của 基本設計書 khác nhau chỗ nào?". 改訂履歴 chỉ ghi "指摘反映" (phản ánh chỉ trích), không có vị trí, và file không bật theo dõi thay đổi. PM xử lý thế nào?**
① Em dùng công cụ so sánh file để liệt kê chính xác các thay đổi giữa hai bản, đối chiếu với 指摘管理表. ② Gửi khách bảng khác biệt: mục, trang, nội dung trước/sau, lý do (số chỉ trích hoặc số CR), và đánh dấu thay đổi trong tài liệu (赤字 – chữ đỏ hoặc 変更箇所 có viền). ③ Xin lỗi vì 改訂履歴 sơ sài. ④ Quy định từ nay: mỗi dòng 改訂履歴 phải có version, ngày, người sửa, mục/trang, nội dung tóm tắt, lý do; bản gửi khách luôn kèm phiên bản có đánh dấu thay đổi; đưa vào checklist trước khi nộp.
> 📘 PMP: Configuration management: mọi thay đổi trên deliverable phải truy vết được nguồn gốc và lý do.
> 💡 Nhật: Khách Nhật thường muốn bản 新旧対照表 (bảng đối chiếu cũ – mới) cho thay đổi quan trọng; chủ động gửi sẽ được đánh giá cao.

**Q507. Khách ngân hàng A muốn review 基本設計書 theo kiểu 読み合わせ (yomiawase – đọc chung từng trang trong họp), dự kiến 6 buổi × 2 giờ. Team lo tốn thời gian và muốn gửi để khách tự đọc. PM chọn phương án nào, vì sao?**
① Em xác nhận lý do khách muốn đọc chung: có thể vì lần trước tài liệu bị hiểu sai giữa các bộ phận. ② Đề xuất kết hợp: phần nghiệp vụ quan trọng (tính phí, điều kiện hợp đồng, quyền hạn) đọc chung; phần màn hình, message thì khách tự đọc trước và chỉ thảo luận chỉ trích. ③ Chuẩn bị kỹ: gửi tài liệu trước 3 ngày, lập danh sách điểm cần khách quyết định, có người ghi 議事録 (gijiroku – biên bản) theo thời gian thực. ④ Sau mỗi buổi gửi biên bản và chỉ trích trong 24 giờ (tham khảo) để khách xác nhận, tránh hiểu khác nhau sau họp.
> 📘 PMP: Manage Stakeholder Engagement và tailoring: chọn hình thức review phù hợp với kỳ vọng và mức rủi ro của từng phần.

**Q508. Trong 詳細設計書 hệ thống hợp đồng bảo hiểm nhân thọ, team dùng lẫn lộn 契約者 (người ký hợp đồng), 被保険者 (người được bảo hiểm) và 受取人 (người thụ hưởng); dev đã code sai 2 chức năng. PM xử lý thế nào?**
① Em xác nhận phạm vi: rà toàn bộ tài liệu và code tìm các chỗ dùng 3 thuật ngữ, đánh dấu chỗ sai nghĩa. ② Sửa tài liệu và mở bug cho 2 chức năng đã code sai, ưu tiên vì ảnh hưởng tính đúng nghiệp vụ. ③ Báo khách: phạm vi sai, đã sửa gì, test lại thế nào; nhờ khách xác nhận định nghĩa chính thức. ④ Gốc rễ là team không hiểu nghiệp vụ bảo hiểm; lập 用語集 có định nghĩa, ví dụ và tên trường DB tương ứng, tổ chức 1 buổi học nghiệp vụ cho team, và thêm mục "thuật ngữ nghiệp vụ" vào checklist review.
> 📘 PMP: Root cause analysis (5 Whys) rồi cập nhật organizational process assets (glossary, checklist) để tránh lặp lại.
> 💡 Nhật: Trong bảo hiểm Nhật, 3 vai trò này có thể là 3 người khác nhau; sai vai trò dẫn tới gửi thông báo nhầm người, rủi ro khiếu nại lớn.

**Q509. Sau 3 vòng review 基本設計書, khách bảo hiểm B có 210 chỉ trích nằm rải rác trong email, file comment và biên bản họp. Team bỏ sót 14 chỉ trích, khách phát hiện ở vòng 4. PM tổ chức lại thế nào?**
① Em gom toàn bộ chỉ trích vào một 指摘管理表 duy nhất, mỗi dòng có ID, nguồn, người chỉ trích, mục, nội dung, phân loại, người phụ trách, trạng thái, ngày sửa, người xác nhận. ② Đối chiếu lại toàn bộ nguồn để chắc không còn sót, xử lý ngay 14 chỉ trích bị bỏ sót. ③ Báo khách xin lỗi, giới thiệu bảng mới và đề nghị từ nay chỉ trích ghi trực tiếp vào bảng. ④ Quy tắc: chỉ trích chỉ "đóng" khi người chỉ trích bên khách xác nhận; trước khi nộp vòng sau, chạy lọc trạng thái để đảm bảo 0 chỉ trích mở không có lý do.
> 📘 PMP: Issue log và Monitor Communications: một nguồn thông tin duy nhất giúp theo dõi và đóng vấn đề.

**Q510. Khách phi nhân thọ C yêu cầu 詳細設計書 dùng template của công ty họ (font, đánh số mục, header có mã tài liệu), nhưng team đã viết 40% bằng template của VTI. Team đề nghị nộp template VTI cho nhanh. PM quyết định thế nào?**
① Em xác nhận yêu cầu template có trong hợp đồng hoặc tiêu chuẩn tài liệu của khách không, và thời điểm khách thông báo. ② Nếu là yêu cầu chính thức thì phải tuân theo; ước tính công chuyển đổi 40% (thường chủ yếu là format, có thể dùng macro). ③ Báo khách kế hoạch chuyển đổi và hỏi có thể chấp nhận chuyển ở lần nộp chính thức không. Nếu yêu cầu đến muộn và làm tăng công đáng kể thì nêu ảnh hưởng để xử lý như thay đổi. ④ Bài học: xác nhận template, tiêu chuẩn tài liệu và mẫu đặt tên ngay ở giai đoạn khởi động dự án.
> 📘 PMP: Collect Requirements bao gồm cả yêu cầu về hình thức deliverable; ghi vào quality management plan từ đầu.
> 💡 Nhật: Nhiều khách tài chính có 文書管理規程 (quy định quản lý tài liệu) riêng; tài liệu sai format có thể không được đưa vào hồ sơ kiểm tra nội bộ.

**Q511. Đang 総合テスト (sougou tesuto – ST), khách bảo hiểm B phát hiện hệ thống xử lý đúng theo CR-15 đã duyệt nhưng 基本設計書 và 詳細設計書 vẫn mô tả logic cũ. Khách hỏi: "tài liệu nào là đúng?". PM xử lý thế nào?**
① Em xác nhận phạm vi: rà tất cả CR đã duyệt và kiểm tra tài liệu nào chưa cập nhật, không chỉ CR-15. ② Cập nhật tài liệu cho các CR còn thiếu, ghi 改訂履歴 tham chiếu số CR, gửi khách bản đánh dấu thay đổi. ③ Báo khách: hệ thống đúng theo CR, tài liệu chậm cập nhật là lỗi của team, kèm danh sách và hạn hoàn tất. ④ Gốc rễ: quy trình CR chỉ theo dõi code; bổ sung vào checklist đóng CR mục "tài liệu thiết kế, test spec, tài liệu vận hành đã cập nhật", CR chỉ đóng khi đủ.
> 📘 PMP: Perform Integrated Change Control: change được duyệt phải cập nhật tất cả project documents và baselines liên quan.

**Q512. Khách ngân hàng A muốn nhận 基本設計書 sớm 1 tuần để kịp 稟議 (ringi – xin phê duyệt nội bộ). Team chỉ xong 80%, 20% còn lại là phần xử lý ngoại lệ chưa xác nhận xong. PM đề xuất thế nào?**
① Em xác nhận với khách 稟議 cần những phần nào: thường là phạm vi, chức năng chính, chi phí, lịch. ② Đề xuất nộp sớm bản ghi rõ trạng thái: phần đã hoàn thiện, phần "未確定" (chưa xác định) có danh sách vấn đề mở, người quyết định và hạn; không trình bày bản 80% như bản hoàn chỉnh. ③ Báo lãnh đạo hai bên về rủi ro: phần ngoại lệ có thể đổi công sức. ④ Đặt lịch nộp bản hoàn chỉnh và lần review riêng cho 20% còn lại; ghi thỏa thuận vào biên bản để tránh sau này khách coi bản sớm là bản đã duyệt toàn bộ.
> 📘 PMP: Rolling wave planning và quản lý kỳ vọng: minh bạch mức độ hoàn thiện, không đánh đổi chất lượng ngầm lấy tiến độ.
> 💡 Nhật: Ghi rõ "暫定版" (bản tạm) trên bìa và header; khách Nhật chấp nhận bản tạm nếu được báo trước, nhưng rất khó chịu nếu bản tạm bị coi như bản chính.

**Q513. Khách bảo hiểm B yêu cầu nộp 基本設計書 dạng Excel và in ra giấy để các trưởng phòng đóng dấu. Bản in bị cắt cột, sơ đồ tràn trang, số trang sai, trưởng phòng trả lại. PM làm gì?**
① Em xác nhận cách khách dùng tài liệu: in khổ A4 hay A3, đen trắng hay màu, đóng dấu ở đâu. ② Chỉnh vùng in, ngắt trang, tỷ lệ in, header/footer có tên tài liệu, version, số trang "n/N" cho từng sheet; in thử toàn bộ một lần trước khi gửi. ③ Gửi lại kèm xin lỗi và xác nhận bản in đã đúng. ④ Thêm vào checklist trước khi nộp mục "印刷プレビュー確認" (kiểm tra xem trước bản in), giao cho người self-check thực hiện cho mọi tài liệu Excel; đây là chi tiết nhỏ nhưng ảnh hưởng trực tiếp tới hình ảnh chất lượng.
> 📘 PMP: Định nghĩa quality requirements cần bao gồm cả cách stakeholder sử dụng deliverable, không chỉ nội dung.
> 💡 Nhật: Nhiều khách tài chính vẫn duyệt bằng giấy và dấu; bản in xấu khiến người duyệt cấp cao đánh giá thấp vendor dù chưa đọc nội dung.

## 5.2 Parameter sheet (パラメータシート) hạ tầng/middleware

**Q514. Dự án migration hệ thống core của khách bảo hiểm nhân thọ B, member hạ tầng mới hỏi: "パラメータシート (parameter sheet – bảng giá trị cấu hình) cần có những cột gì để khách chấp nhận?". PM hướng dẫn thế nào?**
Em hướng dẫn tối thiểu các cột: phân loại (OS, DB, AP server, mạng), tên tham số, giá trị cài đặt cho từng môi trường, giá trị mặc định của sản phẩm, có đổi so với mặc định không, 設定根拠 (lý do cài đặt), tài liệu tham chiếu (方式設計書 – thiết kế phương thức), người lập, người kiểm tra. Mỗi sheet có header ghi tên server, phiên bản sản phẩm, version tài liệu. Bằng chứng tốt nhất là sheet đối chiếu được với kết quả lệnh xuất cấu hình thật. Bẫy hay gặp: ghi "デフォルト" thay vì giá trị cụ thể, và không ghi phiên bản sản phẩm nên khi nâng cấp không biết mặc định đã đổi.
> 📘 PMP: Plan Quality Management: định nghĩa cấu trúc và tiêu chí chấp nhận của deliverable trước khi bắt đầu tạo nó.

**Q515. Trong 結合テスト (ketsugou tesuto – IT), batch của khách ngân hàng A bị timeout. Kiểm tra thì パラメータシート ghi timeout DB connection 60 giây, nhưng môi trường thật đang là 30 giây. Việc đầu tiên PM làm là gì?**
① Em xác nhận giá trị nào đúng theo 方式設計書 và ai đã cài 30 giây, vào lúc nào. ② Không sửa vội trên môi trường; đánh giá ảnh hưởng, nếu 60 giây là giá trị đã duyệt thì sửa môi trường theo thủ tục thay đổi, ghi lại thao tác và chạy lại test. ③ Báo khách: nguyên nhân timeout, sai lệch tài liệu và môi trường, đã xử lý thế nào. ④ Gốc rễ là thiếu bước kiểm chéo sau khi cài; rà toàn bộ tham số của các server khác cùng loại (横展開) bằng script so sánh sheet với cấu hình thật trước khi tiếp tục IT.
> 📘 PMP: Control Quality: phát hiện sai lệch giữa baseline cấu hình và thực tế, xử lý qua change control rồi mở rộng kiểm tra tương tự.
> 💡 Nhật: Khách Nhật sẽ hỏi "他は大丈夫ですか" (chỗ khác có ổn không); chuẩn bị sẵn kết quả rà toàn bộ trước khi báo.

**Q516. Team hạ tầng 6 người lập パラメータシート cho 40 server. Khách phi nhân thọ C yêu cầu bằng chứng sheet khớp với môi trường thật. PM tổ chức kiểm chéo thế nào?**
① Em yêu cầu xuất cấu hình thật từ mỗi server bằng lệnh hoặc script chuẩn (lưu file kết quả có tên server, ngày giờ). ② Dùng script so sánh tự động giữa giá trị trong sheet và file xuất, sinh danh sách khác biệt; người kiểm chéo là người không cài server đó. ③ Mỗi khác biệt phải được kết luận: sửa sheet (nếu môi trường đúng và đã được duyệt) hoặc sửa môi trường qua thủ tục thay đổi. ④ Nộp khách sheet kèm kết quả so sánh "0 khác biệt chưa giải thích" làm エビデンス (evidence – bằng chứng). Bẫy: so sánh bằng mắt 40 server rất dễ bỏ sót, và chỉ so mẫu vài server.
> 📘 PMP: Control Quality bằng inspection; tự động hóa kiểm tra giúp kết quả lặp lại được.

**Q517. Team copy パラメータシート từ môi trường 本番 (honban – production) sang 検証 (môi trường kiểm chứng) rồi sửa. Khi cài 検証, IP kết nối của 2 server vẫn trỏ về IP production, may mà firewall chặn. PM xử lý thế nào?**
① Em xác nhận ngay không có kết nối nào từ 検証 tới production đã thành công (kiểm log firewall và log ứng dụng). ② Sửa giá trị trên môi trường 検証, rà toàn bộ tham số có tính chất "địa chỉ" (IP, hostname, URL, đường dẫn mount) ở mọi server. ③ Báo khách sự việc dù chưa gây ảnh hưởng, vì đây là rủi ro bảo mật và có thể gây ghi dữ liệu nhầm. ④ Phòng ngừa: tách sheet theo môi trường với tham số đặc thù môi trường được đánh màu, cấm copy nguyên sheet, có bước kiểm "không còn giá trị production trong sheet 検証" bằng tìm kiếm tự động.
> 📘 PMP: Identify Risks và near-miss: báo cáo cả sự cố suýt xảy ra để cập nhật risk register và lessons learned.
> 💡 Nhật: Near-miss (ヒヤリハット) được khách Nhật coi trọng; chủ động báo cáo sẽ được tin tưởng hơn là giấu vì "chưa có hậu quả".

**Q518. Khách bảo hiểm B nâng cấp bản vá middleware AP server. Sau nâng cấp, số thread mặc định đổi, hiệu năng giảm 20%. パラメータシート chỉ ghi "デフォルト" cho tham số này. PM làm gì?**
① Em xác nhận giá trị mặc định trước và sau bản vá (từ release note chính thức của nhà sản xuất), đo lại hiệu năng để chắc nguyên nhân. ② Đề xuất cài giá trị cụ thể bằng giá trị cũ đã được kiểm chứng, đi qua thủ tục thay đổi, test lại hiệu năng. ③ Báo khách nguyên nhân và đề xuất. ④ Phòng ngừa: sheet phải ghi giá trị thực tế kể cả khi bằng mặc định; trước mỗi bản vá, đọc release note tìm thay đổi mặc định và so sánh cấu hình trước/sau bản vá như một bước bắt buộc.
> 📘 PMP: Perform Integrated Change Control: phân tích ảnh hưởng của thay đổi môi trường trước khi áp dụng, kể cả thay đổi "nhỏ" như bản vá.

**Q519. Khách ngân hàng A yêu cầu ghi 設定根拠 cho từng tham số. Team hạ tầng 5 người không trả lời được lý do của 30% tham số vì "copy từ hệ thống cũ". PM xử lý thế nào?**
① Em phân loại 30% đó: tham số ảnh hưởng hiệu năng, bảo mật, dung lượng (quan trọng) và tham số ít ảnh hưởng. ② Với nhóm quan trọng: tìm nguồn gốc trong tài liệu hệ cũ, hỏi vendor/khách đã vận hành, hoặc đo kiểm để có lý do mới; với nhóm còn lại ghi "引継ぎ値 (giá trị kế thừa từ hệ cũ), đã xác nhận vận hành ổn định từ ngày…". ③ Báo khách trung thực những tham số chưa có lý do và kế hoạch làm rõ, không bịa lý do. ④ Bài học: trong migration, "giống hệ cũ" cũng là một lý do nhưng phải được khách đồng ý bằng văn bản.
> 📘 PMP: Assumption log: ghi giả định "giữ nguyên giá trị hệ cũ" và xin xác nhận, thay vì để thành rủi ro ngầm.
> 💡 Nhật: Câu trả lời "前任者がそう設定したから" (người trước cài vậy) là điều tối kỵ trước khách tài chính; nói rõ cái chưa biết và kế hoạch xác minh.

**Q520. Lúc xử lý sự cố đêm trong IT, kỹ sư hạ tầng sửa trực tiếp 3 tham số kernel trên server để chạy tiếp, không cập nhật パラメータシート. Hai tuần sau khách phát hiện chênh lệch khi kiểm tra. PM làm gì?**
① Em xác nhận 3 tham số, ai sửa, lúc nào, lý do, và có được phép theo quy trình khẩn cấp không. ② Đánh giá xem giá trị mới có nên giữ không; nếu giữ thì đi thủ tục thay đổi hậu kiểm (事後承認), cập nhật sheet và các môi trường khác cần đồng bộ. ③ Báo khách trung thực, kèm log thao tác. ④ Quy định: sửa khẩn cấp được phép nhưng phải ghi vào nhật ký thao tác ngay và trong 1 ngày làm việc (tham khảo) phải hoàn tất cập nhật sheet và xin duyệt; định kỳ chạy script so sánh để phát hiện drift.
> 📘 PMP: Configuration management: thay đổi khẩn cấp vẫn phải được ghi nhận và hợp thức hóa qua change control sau đó.

**Q521. Team cần gửi khách phi nhân thọ C パラメータシート có chứa IP nội bộ, tài khoản dịch vụ và mật khẩu khởi tạo. Member định đính kèm file zip có mật khẩu qua email và gửi mật khẩu ở email thứ hai. PM xử lý thế nào?**
① Em xác nhận quy định trao đổi tài liệu bảo mật của khách và của công ty. ② Tách thông tin: mật khẩu không bao giờ nằm trong パラメータシート, chỉ ghi "管理台帳参照" (xem sổ quản lý) và quản lý mật khẩu bằng kênh riêng do khách chỉ định. ③ Gửi sheet qua kho lưu trữ có kiểm soát quyền mà khách cho phép, không qua email đính kèm. ④ Rà lại các sheet đã gửi trước đó xem có chứa mật khẩu không; nếu có thì báo khách để đổi mật khẩu. Bẫy: cách "zip có mật khẩu + mật khẩu gửi email riêng" nhiều tổ chức Nhật đã bỏ vì không thật sự an toàn.
> 📘 PMP: Plan Communications Management cần xác định kênh trao đổi cho thông tin nhạy cảm, không chỉ tần suất và người nhận.
> 💡 Nhật: Cách gửi này thường gọi là "PPAP" và nhiều doanh nghiệp, cơ quan Nhật đã ngừng dùng; hỏi khách kênh chính thức trước.

**Q522. Còn 3 ngày tới 本番移行 (honban ikou – cutover) của ngân hàng A, kiểm tra cuối cho thấy 15% tham số OS trên server production không khớp パラメータシート. Lãnh đạo hỏi có nên hoãn không. PM xử lý thế nào?**
① Em phân loại 15% khác biệt theo mức ảnh hưởng: hiệu năng, bảo mật, ổn định, chỉ là hiển thị/log. ② Xác định khác biệt nào do sheet sai, khác biệt nào do môi trường sai; với nhóm ảnh hưởng cao, sửa theo thủ tục thay đổi và chạy lại kiểm tra hiệu năng/khởi động, ước thời gian cần. ③ Báo khách và lãnh đạo bằng dữ liệu: số khác biệt từng nhóm, đã xử lý bao nhiêu, rủi ro còn lại, và đề xuất go/no-go theo tiêu chí đã thống nhất. ④ Không tự giấu hay tự hoãn; quyết định go/no-go là của khách dựa trên thông tin đầy đủ.
> 📘 PMP: Monitor Risks và quyết định dựa trên dữ liệu; PM cung cấp phân tích ảnh hưởng để người có thẩm quyền ra quyết định.
> 💡 Nhật: Khách Nhật rất ngại hoãn cutover, nhưng còn ngại hơn sự cố ngày đầu; trình bày rõ phương án và điều kiện go sẽ dễ được chấp nhận.

**Q523. Hạ tầng do vendor khác của khách bảo hiểm B phụ trách, team VTI chỉ làm ứng dụng nhưng phụ thuộc vào パラメータシート của vendor đó. Team phát hiện sheet ghi sai cổng kết nối DB, làm IT chậm 2 ngày. PM xử lý thế nào?**
① Em xác nhận chính xác giá trị sai và giá trị thật (kèm kết quả kiểm tra kết nối). ② Không tự sửa tài liệu hay môi trường của vendor khác; gửi yêu cầu xác nhận qua 窓口 (madoguchi – đầu mối) đã thống nhất của khách, kèm bằng chứng. ③ Báo khách ảnh hưởng 2 ngày và đề xuất cách bù, ghi vào 課題管理表 (bảng quản lý vấn đề) với người phụ trách là vendor/khách. ④ Phòng ngừa: đề xuất khách tổ chức buổi kiểm chéo sheet giữa các vendor trước mỗi giai đoạn test, và ghi rõ trong kế hoạch dự án rủi ro phụ thuộc này.
> 📘 PMP: Manage Stakeholder Engagement và quản lý dependency với bên ngoài qua đúng kênh, có bằng chứng.

**Q524. Khách phi nhân thọ C đề nghị bỏ nhập tay パラメータシート, chuyển sang sinh tự động từ công cụ quản lý cấu hình (IaC). Team 8 người hạ tầng chưa quen. PM đánh giá đề xuất thế nào?**
① Em xác nhận mục tiêu khách: giảm sai lệch tài liệu – môi trường, hay giảm công. ② Đánh giá theo: kỹ năng team, công cụ có được phép dùng trong môi trường khách không, định dạng đầu ra có đáp ứng tiêu chuẩn tài liệu (cột 設定根拠 vẫn phải viết tay), chi phí chuyển đổi so với thời gian còn lại. ③ Đề xuất thử trên 1 nhóm server ở môi trường 検証, đo thời gian và số sai lệch so với cách cũ, rồi mới quyết định mở rộng. ④ Nếu áp dụng, cập nhật kế hoạch chất lượng và đào tạo; tránh đổi phương pháp ngay trước cutover.
> 📘 PMP: Tailoring và thử nghiệm nhỏ (pilot) trước khi áp dụng thay đổi quy trình; quyết định dựa trên số đo.
> 💡 Nhật: Khách Nhật thích cải tiến nhưng ghét rủi ro đổi giữa chừng; đề xuất "trial trên 検証 trước" dễ được duyệt hơn.

**Q525. Trưởng nhóm hạ tầng tự lập và tự review パラメータシート cho khách ngân hàng A, khách hỏi "ai đã kiểm tra, kiểm tra theo tài liệu nào?". PM thiết kế quy trình review sheet thế nào?**
Em quy định 3 lớp: người lập tự kiểm theo checklist; người thứ hai (không lập) kiểm chéo đối chiếu với 方式設計書 làm gốc, kiểm cả tính nhất quán giữa các server cùng vai trò; trưởng nhóm hoặc PM duyệt cuối, ghi tên và ngày vào sheet. Mỗi giá trị phải truy về được một dòng trong 方式設計書 hoặc một quyết định đã duyệt. Bằng chứng gửi khách: lịch sử review, danh sách chỉ trích nội bộ đã đóng, kết quả so sánh với môi trường thật. Bẫy: người lập tự duyệt chính mình, và review chỉ nhìn format mà không đối chiếu tài liệu gốc.
> 📘 PMP: Manage Quality: tách vai trò tạo và kiểm tra (independent review), lưu bằng chứng audit được.

## 5.3 Test spec (テスト仕様書)

**Q526. Member mới được giao viết テスト仕様書 (tesuto shiyousho – tài liệu đặc tả test) cho IT màn hình đăng ký hợp đồng bảo hiểm, hỏi PM: "テスト観点 (tesuto kanten – góc nhìn test) là gì, lập thế nào?". PM hướng dẫn thế nào?**
Em giải thích テスト観点 là danh sách "cần kiểm cái gì" trước khi viết từng case "kiểm thế nào". Cách lập: lấy từng chức năng trong thiết kế, tách theo nhóm quan điểm chuẩn như 正常系 (luồng đúng), 異常系 (luồng lỗi), giá trị biên, tổ hợp điều kiện, quyền hạn, đồng thời, dữ liệu đặc thù nghiệp vụ (ngày hiệu lực, tuổi, loại hợp đồng). Mỗi quan điểm truy về mục thiết kế, rồi mới sinh case. Bằng chứng tốt: bảng 観点一覧 được khách review trước khi viết case. Bẫy hay gặp: viết thẳng case từ màn hình nên thiếu hẳn cả nhóm quan điểm như quyền hạn hay xử lý đồng thời.
> 📘 PMP: Plan Quality Management: xác định phạm vi và phương pháp kiểm tra trước khi tạo test case chi tiết.
> 💡 Nhật: Khách Nhật thường muốn review 観点 trước, case sau; nộp thẳng 2000 case mà không có 観点一覧 dễ bị trả lại.

**Q527. Khách bảo hiểm nhân thọ B review テスト仕様書 IT và chỉ trích: 85% case là 正常系, gần như không có 異常系 (lỗi kết nối, dữ liệu sai định dạng, timeout). Việc đầu tiên PM làm là gì?**
① Em xác nhận chỉ trích bằng số: thống kê case theo 観点 cho từng chức năng, chỉ ra chức năng nào thiếu 異常系. ② Bổ sung 観点 異常系 theo danh mục chuẩn (input sai, dữ liệu không tồn tại, lỗi hệ thống bên ngoài, timeout, trùng xử lý), ưu tiên chức năng liên quan tiền và hợp đồng. ③ Gửi khách 観点一覧 đã bổ sung để xác nhận trước khi viết case, kèm lịch hoàn thành. ④ Gốc rễ là không có danh mục 観点 chuẩn; đưa danh mục này thành mẫu cho mọi テスト仕様書, kiểm tỷ lệ 異常系 ở bước self-check trước khi nộp.
> 📘 PMP: Control Quality và cập nhật quality checklist; sửa quy trình tạo test spec chứ không chỉ thêm case.

**Q528. Hệ thống tính phí bảo hiểm phi nhân thọ của khách C có quy tắc theo tuổi (18–69) và số năm lái xe. Khách chỉ ra テスト仕様書 chỉ test giá trị giữa khoảng, không có giá trị biên. PM bổ sung thế nào?**
① Em liệt kê mọi điều kiện có ngưỡng trong thiết kế tính phí: tuổi, năm lái xe, ngày hiệu lực, số tiền bảo hiểm. ② Với mỗi ngưỡng dùng phân tích giá trị biên: dưới biên, đúng biên, trên biên (ví dụ 17, 18, 69, 70), cộng phân vùng tương đương cho từng khoảng; với nhiều điều kiện kết hợp dùng bảng quyết định để chọn tổ hợp. ③ Gửi khách bảng ngưỡng và tổ hợp đã chọn để khách xác nhận cách tính tuổi (theo ngày sinh hay theo năm bảo hiểm). ④ Bẫy: biên của "tuổi" phụ thuộc quy tắc nghiệp vụ, phải xác nhận định nghĩa trước khi viết case.
> 📘 PMP: Kỹ thuật thiết kế test (boundary value, equivalence partitioning, decision table) thuộc Control Quality; định nghĩa chính xác là yêu cầu, không phải giả định.
> 💡 Nhật: Bảo hiểm Nhật có thể tính tuổi theo cách riêng của sản phẩm; hỏi khách định nghĩa chính thức thay vì tự suy.

**Q529. テスト仕様書 của team có 400 case ghi kết quả mong đợi là "正常に表示されること" (hiển thị bình thường). Khách ngân hàng A nói: "không kiểm được, thế nào là bình thường?". PM xử lý thế nào?**
① Em lọc toàn bộ case có kết quả mong đợi mơ hồ (bằng từ khóa như 正常, 適切, 問題なく). ② Viết lại theo nguyên tắc đo được: giá trị cụ thể hiển thị ở item nào, message ID nào, dữ liệu DB nào thay đổi thành giá trị gì, trạng thái nào. ③ Báo khách kế hoạch sửa và mẫu viết mới, xin khách duyệt mẫu trước khi sửa hàng loạt. ④ Đưa quy tắc "kết quả mong đợi phải kiểm được bởi người thứ ba" vào checklist; người review thử đọc case và tự hỏi "người khác chạy có ra cùng kết luận không".
> 📘 PMP: Quality requirements phải đo được; tiêu chí chấp nhận mơ hồ khiến Control Quality không có ý nghĩa.

**Q530. Khách bảo hiểm B hỏi: "yêu cầu số R-045 được test ở case nào?". Team mất 2 ngày mới trả lời được vì テスト仕様書 không tham chiếu tới yêu cầu. PM cải thiện thế nào?**
① Em xác nhận khách cần truy vết ở mức nào: yêu cầu → thiết kế → case. ② Lập ma trận truy vết: mỗi yêu cầu liệt kê mục 基本設計, 詳細設計 và ID case tương ứng; mỗi case có cột "yêu cầu tham chiếu". ③ Dùng ma trận để tìm yêu cầu chưa có case (khoảng trống) và báo khách kết quả cùng kế hoạch bổ sung. ④ Phòng ngừa: ma trận cập nhật mỗi khi có CR hoặc thêm case; trước mỗi giai đoạn test, kiểm 100% yêu cầu trong phạm vi có ít nhất 1 case.
> 📘 PMP: Requirements traceability matrix: liên kết yêu cầu với deliverable và test để đảm bảo mọi yêu cầu được kiểm.
> 💡 Nhật: Khách tài chính thường bị kiểm toán nội bộ hỏi đúng câu này; ma trận truy vết giúp họ trả lời kiểm toán, nên họ đánh giá rất cao.

**Q531. Hợp đồng 請負 với khách phi nhân thọ C quy định khách review テスト仕様書 ST trước khi bắt đầu test. Còn 5 ngày đến ngày bắt đầu ST nhưng khách chưa review vì bận 年度末 (nendomatsu – cuối năm tài chính). PM chọn phương án nào?**
① Em xác nhận khách có thể review phần nào trong 5 ngày, phần nào không. ② Đề xuất ưu tiên: khách review 観点一覧 và case của chức năng rủi ro cao trước; bắt đầu ST với các phần đó, phần còn lại review song song. ③ Báo khách và lãnh đạo rủi ro: phần chưa review có thể phải chạy lại nếu khách chỉ trích; ghi thỏa thuận vào biên bản, không tự bắt đầu ngầm. ④ Nếu khách không thể review, đề xuất dời mốc hoặc chấp nhận rủi ro bằng văn bản; cập nhật lịch review của khách vào kế hoạch các giai đoạn sau, tránh trùng 年度末.
> 📘 PMP: Manage Stakeholder Engagement và Monitor Risks: dependency vào khách là rủi ro cần quản lý minh bạch.
> 💡 Nhật: Tháng 3 là cao điểm của khách tài chính Nhật; lập lịch review rơi vào cuối tháng 3 gần như chắc chắn trễ.

**Q532. Batch tính lãi hằng đêm của ngân hàng A có テスト仕様書 chỉ test ngày thường. Khách hỏi case cho cuối tháng, cuối năm tài chính, năm nhuận, ngày nghỉ liên tiếp. PM xử lý thế nào?**
① Em xác nhận trong thiết kế batch có quy tắc nào phụ thuộc lịch: ngày làm việc, ngày nghỉ ngân hàng, số ngày tính lãi. ② Bổ sung 観点 "lịch đặc thù": 月末, 年度末, ngày 29/2, ngày nghỉ dài, ngày chuyển giờ hệ thống nếu có, và xử lý chạy bù khi batch bị dừng qua đêm. ③ Thống nhất với khách cách giả lập ngày hệ thống trong môi trường test và lịch nghỉ dùng cho test. ④ Thêm "観点 lịch" vào danh mục chuẩn cho mọi chức năng batch và tính toán theo ngày.
> 📘 PMP: Identify Risks từ các điều kiện ít xảy ra nhưng ảnh hưởng lớn; test cần phủ cả trường hợp hiếm có tác động tài chính.

**Q533. Team tái sử dụng テスト仕様書 từ dự án trước cho khách bảo hiểm B. Khách phát hiện trong file còn tên công ty khách cũ và tên sản phẩm của họ ở 3 sheet ẩn. PM xử lý thế nào?**
① Em xác nhận phạm vi: file đã gửi cho ai, có thông tin gì của khách cũ, có dữ liệu cá nhân hay không. ② Thu hồi/đề nghị khách xóa file, gửi bản sạch; báo nội bộ bộ phận bảo mật theo quy trình vì đây là rò rỉ thông tin của khách cũ. ③ Xin lỗi khách B, giải thích nguyên nhân và biện pháp. ④ Gốc rễ là tái sử dụng file thật thay vì template; quy định chỉ dùng template sạch, trước khi nộp chạy kiểm tra sheet ẩn, thuộc tính file, comment, tên người tạo và tìm từ khóa tên khách khác.
> 📘 PMP: Manage Quality kết hợp quy trình bảo mật của tổ chức (organizational process assets); sự cố cần được ghi vào lessons learned.
> 💡 Nhật: Lộ tên khách khác bị khách Nhật xem là dấu hiệu "công ty này cũng sẽ lộ thông tin của mình"; mất niềm tin nặng hơn nhiều so với lỗi kỹ thuật.

**Q534. テスト仕様書 do tester Việt Nam viết tiếng Việt rồi comtor dịch. Khách phi nhân thọ C nói nhiều bước thao tác không làm theo được vì không rõ bấm nút nào, nhập gì. PM cải thiện thế nào?**
① Em chọn 10 case ngẫu nhiên, nhờ một người chưa biết chức năng chạy theo đúng chữ viết để tìm chỗ mơ hồ. ② Chuẩn hóa cách viết bước: tên màn hình/nút đúng như hiển thị bằng tiếng Nhật, dữ liệu nhập cụ thể, một bước một thao tác. ③ Báo khách mẫu cách viết mới và lịch sửa. ④ Phòng ngừa: tester viết tên màn hình, item bằng tiếng Nhật ngay từ nguồn (copy từ thiết kế), comtor chỉ dịch phần mô tả; thêm bước "chạy thử bởi người khác" cho case mẫu mỗi chức năng.
> 📘 PMP: Manage Quality: chuẩn hóa quy trình và mẫu để giảm biến thiên chất lượng giữa các người viết.

**Q535. ST cho khách bảo hiểm B có 3.000 case nhưng chỉ còn đủ thời gian chạy khoảng 2.200 case. Khách yêu cầu "chất lượng không được giảm". PM chọn phương án nào?**
① Em xác nhận thời gian và nguồn lực thực tế, không giả định làm thêm giờ vô hạn. ② Phân loại case theo rủi ro (ảnh hưởng tiền, hợp đồng, pháp lý, tần suất dùng) và theo trùng lặp với IT đã chạy; đề xuất bộ ưu tiên phải chạy 100%, phần còn lại chạy giảm hoặc chuyển sang giai đoạn sau. ③ Trình khách các phương án: tăng người, kéo dài lịch, hoặc giảm phạm vi theo rủi ro, kèm rủi ro từng phương án; khách quyết định. ④ Ghi quyết định vào biên bản và cập nhật テスト仕様書 với cột "đối tượng/ngoài đối tượng".
> 📘 PMP: Risk-based testing và phân tích trade-off phạm vi – thời gian – chất lượng; quyết định qua change control, không tự cắt.
> 💡 Nhật: Không bao giờ tự bỏ case rồi báo "đã test xong"; khách Nhật phát hiện sau sẽ coi là gian dối, không chỉ là sai sót.

**Q536. Trong lúc chạy IT, team thêm 120 case và sửa 80 case trong テスト仕様書 nhưng không ghi lại. Khi nộp 品質報告書 (hinshitsu houkokusho – báo cáo chất lượng), số case không khớp với bản khách đã duyệt. PM xử lý thế nào?**
① Em đối chiếu bản đã duyệt và bản hiện tại để liệt kê chính xác case thêm, sửa, xóa và lý do. ② Lập bảng thay đổi, cập nhật 改訂履歴, gửi khách xin xác nhận các thay đổi, đặc biệt case bị sửa kết quả mong đợi. ③ Báo khách trung thực việc không ghi thay đổi kịp thời. ④ Quy định: テスト仕様書 trong lúc chạy test vẫn quản lý version; thêm case thì đánh ID mới, không ghi đè; sửa kết quả mong đợi phải có người duyệt vì có thể che giấu bug.
> 📘 PMP: Configuration management cho test artifacts; thay đổi kết quả mong đợi cần kiểm soát như thay đổi yêu cầu.

**Q537. Khách ngân hàng A yêu cầu team VTI viết luôn テスト仕様書 cho 受入テスト (ukeire tesuto – UAT) trong khi hợp đồng ghi UAT là trách nhiệm khách. PM xử lý thế nào?**
① Em xác nhận phạm vi hợp đồng và khách mong muốn mức hỗ trợ nào: soạn toàn bộ, soạn mẫu, hay chỉ review. ② Giải thích lý do UAT nên do khách thiết kế: kiểm theo nghiệp vụ thực tế của người dùng, khác với ST do vendor kiểm theo thiết kế. ③ Đề xuất phương án hỗ trợ có phạm vi rõ: cung cấp mẫu và 観点 gợi ý, hoặc soạn nháp theo kịch bản nghiệp vụ khách cung cấp, xử lý như thay đổi phạm vi nếu tăng công. ④ Ghi rõ trách nhiệm phê duyệt UAT spec vẫn là khách vào biên bản.
> 📘 PMP: Control Scope và Perform Integrated Change Control: yêu cầu ngoài phạm vi được đánh giá và phê duyệt, không làm ngầm.
> 💡 Nhật: Nhiều khách Nhật quen vendor "làm hộ" UAT spec; nếu vendor tự viết toàn bộ, UAT dễ trở thành chạy lại ST và bỏ sót lỗi nghiệp vụ.

**Q538. Sau khi sửa 25 bug ở ST, khách bảo hiểm B hỏi phạm vi 回帰テスト (kaiki tesuto – regression test) dựa trên căn cứ gì. Team định chạy lại toàn bộ 2.500 case, mất 3 tuần. PM chọn phương án nào?**
① Em phân tích ảnh hưởng từng bug sửa: module, bảng dữ liệu, chức năng gọi chung bị thay đổi. ② Chọn regression theo ảnh hưởng: case của chức năng bị sửa, chức năng dùng chung module/bảng đó, cộng bộ case cốt lõi (golden path nghiệp vụ) luôn chạy. ③ Trình khách bảng "bug → phạm vi ảnh hưởng → case regression" làm căn cứ, kèm số case và thời gian; khách duyệt. ④ Phòng ngừa: duy trì ma trận module – case để lần sau chọn nhanh, và tự động hóa bộ case cốt lõi nếu môi trường cho phép.
> 📘 PMP: Phân tích ảnh hưởng (impact analysis) và tối ưu chi phí chất lượng (cost of quality) thay vì kiểm toàn bộ theo thói quen.

## 5.4 Evidence (エビデンス)

**Q539. Bắt đầu IT cho khách bảo hiểm nhân thọ B, tester mới hỏi エビデンス (ebidensu – bằng chứng test) cần gồm gì và đặt tên file thế nào. PM hướng dẫn thế nào?**
Em hướng dẫn: エビデンス phải chứng minh được "đã chạy case nào, lúc nào, ai chạy, kết quả thực tế so với mong đợi". Gồm ảnh màn hình trước/sau thao tác có hiển thị ngày giờ, log liên quan, kết quả truy vấn DB trước/sau, file đầu ra. Đặt tên theo quy tắc cố định, ví dụ `<giai đoạn>_<ID chức năng>_<ID case>_<số thứ tự>`, lưu theo cây thư mục giống テスト仕様書. Bằng chứng tốt là người thứ ba mở file theo ID case tìm ra ngay. Bẫy: chụp chỉ một phần màn hình không thấy item cần kiểm, và đặt tên tùy ý khiến khách lấy mẫu không tìm được.
> 📘 PMP: Control Quality: work performance data phải được lưu đủ để xác minh kết quả và phục vụ kiểm tra sau này.
> 💡 Nhật: Thống nhất quy tắc エビデンス bằng văn bản với khách trước khi test; mỗi khách có "thói quen" khác nhau, đổi giữa chừng rất tốn công.

**Q540. Khách ngân hàng A lấy mẫu 30 file エビデンス IT, thấy 11 file không thấy ngày giờ chạy và không chụp phần item đối chiếu với kết quả mong đợi. Việc đầu tiên PM làm là gì?**
① Em xác nhận tỷ lệ thật trên toàn bộ: rà tự động/ngẫu nhiên lớn hơn để biết vấn đề chỉ ở vài tester hay toàn team. ② Với case thiếu bằng chứng ở phần quan trọng, chạy lại và chụp đúng chuẩn; không chỉnh sửa ảnh cũ. ③ Báo khách tỷ lệ thật, kế hoạch bổ sung và thời hạn. ④ Gốc rễ: quy tắc chụp chưa cụ thể; ban hành mẫu "1 case = các ảnh bắt buộc", đồng hồ hệ thống luôn hiển thị, người kiểm chéo kiểm エビデンス ngay trong ngày thay vì cuối giai đoạn.
> 📘 PMP: Control Quality bằng sampling và inspection; mở rộng kiểm tra khi mẫu cho thấy lỗi hệ thống.

**Q541. Sau IT, kiểm tra cho thấy 8% case đã ghi "OK" nhưng không có エビデンス. Tester nói "em đã chạy rồi, chỉ quên chụp". Khách phi nhân thọ C chưa biết. PM xử lý thế nào?**
① Em xác nhận danh sách chính xác các case thiếu và môi trường còn chạy lại được không. ② Đổi trạng thái các case đó sang "chưa có bằng chứng", chạy lại và lấy エビデンス mới với ngày giờ thật; không chụp lại rồi ghi ngày cũ. ③ Báo khách trung thực: số case thiếu, đã chạy lại, kết quả, ảnh hưởng tới lịch nếu có. ④ Quy định "không có エビデンス = chưa test"; kết quả chỉ được ghi OK khi file đã lưu đúng chỗ, và tổng hợp hằng ngày đối chiếu số case OK với số file.
> 📘 PMP: Nguyên tắc stewardship và trung thực (PMI Code of Ethics): báo cáo đúng trạng thái thật, không trình bày kết quả chưa được chứng minh.
> 💡 Nhật: Câu "実施したがエビデンスがない" (đã làm nhưng không có bằng chứng) với khách Nhật tương đương "chưa làm"; đừng dùng nó để xin miễn.

**Q542. Khi kiểm chéo, PM phát hiện một tester dùng cùng một ảnh màn hình cho 6 case khác nhau, chỉ đổi tên file, để kịp tiến độ. PM xử lý thế nào?**
① Em xác nhận sự thật bằng cách so sánh file (hash, nội dung) và nói chuyện riêng với tester, không kết luận vội. ② Đổi trạng thái toàn bộ case của tester đó sang "cần xác minh", chạy lại 6 case và kiểm mẫu các case khác do người này thực hiện. ③ Báo lãnh đạo nội bộ ngay vì đây là vấn đề tính trung thực; báo khách nếu エビデンス đã nộp hoặc kết quả đã báo cáo. ④ Tìm gốc rễ: áp lực tiến độ, chỉ tiêu số case/ngày không thực tế; điều chỉnh kế hoạch, nhắc toàn team rằng làm giả bằng chứng là vi phạm nghiêm trọng, xử lý kỷ luật theo quy định công ty.
> 📘 PMP: PMI Code of Ethics (honesty, responsibility) và root cause analysis: xử lý cả cá nhân và nguyên nhân hệ thống tạo ra áp lực.
> 💡 Nhật: Với khách tài chính, làm giả エビデンス có thể khiến khách yêu cầu kiểm lại toàn bộ giai đoạn và xem xét lại hợp đồng; báo sớm giảm thiệt hại.

**Q543. Khách bảo hiểm B phát hiện một số ảnh エビデンス chụp cả màn hình máy tester, lộ cửa sổ chat nội bộ, tên file của dự án khác và đường dẫn thư mục cá nhân. PM xử lý thế nào?**
① Em xác nhận số ảnh bị ảnh hưởng và thông tin lộ có nhạy cảm không (thông tin khách khác, dữ liệu cá nhân). ② Thay ảnh bằng ảnh chụp lại chỉ vùng ứng dụng cần thiết; nếu có thông tin của khách khác thì xử lý theo quy trình sự cố bảo mật nội bộ. ③ Báo khách, xin lỗi, gửi bản thay thế và đề nghị xóa bản cũ. ④ Quy định cách chụp: chỉ chụp cửa sổ ứng dụng, đóng các ứng dụng khác trong lúc test, dùng máy/VDI chỉ dành cho dự án; thêm mục "không có thông tin ngoài phạm vi" vào checklist kiểm tra エビデンス.
> 📘 PMP: Manage Quality và quản lý rủi ro bảo mật thông tin như một phần yêu cầu chất lượng deliverable.

**Q544. Một case batch của ngân hàng A sinh log 2 GB. Tester đính kèm toàn bộ log làm エビデンス, khách phàn nàn không tìm được dòng chứng minh kết quả. PM hướng dẫn thế nào?**
① Em xác nhận case cần chứng minh điều gì: batch kết thúc bình thường, số bản ghi xử lý, không có lỗi. ② Hướng dẫn trích các dòng liên quan: dòng bắt đầu/kết thúc, mã kết thúc, số bản ghi, các dòng cảnh báo/lỗi (nếu có), ghi rõ tên file log gốc, vị trí dòng và lệnh trích. ③ Lưu log đầy đủ ở kho エビデンス để khách cần thì tra, nhưng file nộp là phần trích có đánh dấu. ④ Chuẩn hóa mẫu エビデンス batch cho cả team; kiểm log không chứa dữ liệu cá nhân trước khi lưu ra ngoài môi trường test.
> 📘 PMP: Manage Communications: thông tin phải phù hợp người nhận; bằng chứng tốt là bằng chứng kiểm được nhanh.
> 💡 Nhật: Khách Nhật thích エビデンス có đánh dấu (khung đỏ, chú thích) chỉ vào đúng chỗ chứng minh kết quả.

**Q545. Case cập nhật hợp đồng của khách phi nhân thọ C, tester chỉ chụp màn hình "更新しました" (đã cập nhật). Khách hỏi: "lấy gì chứng minh DB đã thay đổi đúng các cột?". PM hướng dẫn bổ sung thế nào?**
① Em xác nhận thiết kế: thao tác này thay đổi bảng nào, cột nào, có ghi lịch sử hay audit log không. ② Quy định エビデンス cho thao tác cập nhật: kết quả truy vấn DB trước và sau thao tác cho đúng bản ghi, đánh dấu cột thay đổi, cộng bản ghi lịch sử/log nếu có. ③ Chạy lại các case cập nhật quan trọng để bổ sung, báo khách lịch hoàn tất. ④ Đưa mẫu "before/after" vào hướng dẫn; dùng câu truy vấn chuẩn lưu sẵn theo chức năng để giảm sai sót và đảm bảo không truy vấn thừa dữ liệu cá nhân.
> 📘 PMP: Control Quality: xác minh kết quả ở mức dữ liệu chứ không chỉ ở giao diện, đúng với tiêu chí chấp nhận.

**Q546. エビデンス ST của khách bảo hiểm B được lưu trong file Excel mỗi file 300 MB, khách không mở được trên máy của họ. PM xử lý thế nào?**
① Em xác nhận môi trường của khách: phần mềm, giới hạn dung lượng, cách họ xem エビデンス. ② Đề xuất thay đổi định dạng: tách file theo chức năng, nén ảnh ở độ phân giải vẫn đọc được chữ, hoặc lưu ảnh dạng file riêng kèm danh mục liên kết; thử mở trên cấu hình máy tương đương khách. ③ Xin khách duyệt định dạng mới bằng văn bản trước khi chuyển đổi hàng loạt. ④ Bài học: thống nhất định dạng, dung lượng tối đa và cách nộp エビデンス ngay khi lập kế hoạch test.
> 📘 PMP: Plan Quality Management: tiêu chuẩn deliverable bao gồm khả năng sử dụng của người nhận.

**Q547. Khách ngân hàng A hỏi: "エビデンス lưu ở đâu, ai xem được, giữ bao lâu, xóa thế nào?". Team đang lưu trên ổ chia sẻ chung của văn phòng Việt Nam. PM xử lý thế nào?**
① Em xác nhận hiện trạng: vị trí lưu, quyền truy cập, có dữ liệu nhạy cảm hay không, và yêu cầu hợp đồng về lưu giữ. ② Chuyển エビデンス về nơi lưu được khách chấp thuận (thường là trong môi trường của khách hoặc kho có kiểm soát), giới hạn quyền theo thành viên dự án, bật log truy cập. ③ Trả lời khách bằng văn bản: vị trí, danh sách quyền, thời hạn lưu theo hợp đồng, cách xóa và chứng nhận xóa khi kết thúc. ④ Đưa quy định này vào kế hoạch quản lý thông tin dự án ngay từ đầu cho các dự án sau.
> 📘 PMP: Manage Project Knowledge và tuân thủ yêu cầu bảo mật của stakeholder; thông tin dự án cũng là tài sản cần kiểm soát.
> 💡 Nhật: Khách tài chính có thể hỏi điều này trong audit bảo mật; trả lời "ổ chung, ai cũng xem được" là điểm trừ nặng.

**Q548. Phát hiện một nhóm tester chạy test trước, ghi kết quả OK, rồi cuối tuần mới chạy lại để chụp エビデンス. Lần chạy lại có 3 case cho kết quả khác. PM xử lý thế nào?**
① Em xác nhận 3 case khác nhau vì môi trường thay đổi, dữ liệu thay đổi hay vì lần đầu thực ra chưa đúng. ② Lấy kết quả có bằng chứng làm kết quả thật: 3 case chuyển NG, mở bug, điều tra. ③ Báo khách 3 case NG theo luồng bình thường và giải thích tình trạng quy trình đã được chỉnh. ④ Quy định: エビデンス lấy ngay khi thực hiện, kết quả và bằng chứng phải cùng một lần chạy; chụp sau là "後付け" (bổ sung sau) không được chấp nhận. Tăng kiểm chéo hằng ngày cho nhóm này.
> 📘 PMP: Data integrity trong Control Quality: work performance data phải phản ánh đúng lần thực hiện.

**Q549. Team đề xuất dùng tool test tự động chụp màn hình và sinh báo cáo cho 1.200 case regression của khách bảo hiểm B, nhưng khách quen nhận Excel dán ảnh tay. PM đề xuất thế nào?**
① Em xác nhận yêu cầu thật của khách với エビデンス: nhìn thấy kết quả, có ngày giờ, truy theo ID case, lưu lâu dài. ② Chứng minh tool đáp ứng các yêu cầu đó: báo cáo có ID case, ảnh có timestamp, log chạy, kết quả so sánh; làm mẫu 20 case để khách xem. ③ Xin khách duyệt định dạng mới bằng văn bản trước khi áp dụng toàn bộ; nếu khách vẫn cần Excel, xuất báo cáo tool sang định dạng tương tự. ④ Kiểm tra tool có được phép cài trong môi trường khách không.
> 📘 PMP: Tailoring: điều chỉnh công cụ và phương pháp, nhưng tiêu chí chấp nhận của khách vẫn là chuẩn đánh giá.
> 💡 Nhật: Khách Nhật chấp nhận tự động hóa khi thấy bằng chứng mẫu rõ ràng; đề xuất bằng lời "tool này tốt hơn" thường bị từ chối.

**Q550. Khách phi nhân thọ C yêu cầu エビデンス 単体テスト (tantai tesuto – UT) bằng ảnh debug từng nhánh điều kiện cho 600 hàm, team ước tốn 25 ngày công. Team muốn dùng báo cáo test tự động. PM xử lý thế nào?**
① Em xác nhận mục đích khách: chứng minh mọi nhánh điều kiện đã được chạy và kết quả đúng. ② Đề xuất bằng chứng thay thế đạt cùng mục đích: kết quả chạy unit test tự động (danh sách case, pass/fail), báo cáo độ phủ nhánh, và chỉ chụp debug cho logic phức tạp hoặc nhánh tool không đo được. ③ Trình so sánh công sức và độ tin cậy hai phương án, xin khách duyệt; nếu khách vẫn giữ yêu cầu cũ và nó vượt ước tính ban đầu thì xử lý như thay đổi. ④ Ghi tiêu chuẩn エビデンス UT vào kế hoạch test.
> 📘 PMP: Cost of quality: chọn cách chứng minh chất lượng hiệu quả nhất đạt cùng tiêu chí chấp nhận, quyết định qua đối thoại với khách.

**Q551. Khách ngân hàng A audit エビデンス ST, lấy mẫu 50 case, phát hiện 3 case ảnh cho thấy kết quả khác kết quả mong đợi nhưng vẫn ghi "OK". Khách yêu cầu giải thích trong 2 ngày. PM xử lý thế nào?**
① Em xác nhận 3 case: kết quả thực sự sai hay kết quả mong đợi trong spec sai, ai đã chạy và ai đã kiểm. ② Mở bug hoặc sửa spec qua thủ tục, chạy lại; đồng thời mở rộng kiểm tra: rà toàn bộ case của cùng tester/cùng chức năng, hoặc kiểm toàn bộ nếu tỷ lệ cao. ③ Trả lời khách đúng hạn: kết quả điều tra, phạm vi rà soát mở rộng, số lỗi tìm thêm, biện pháp. ④ Gốc rễ thường là tester so sánh hời hợt và kiểm chéo chỉ xem có ảnh hay không; bổ sung quy tắc người kiểm chéo phải đối chiếu kết quả với spec, đánh dấu chỗ đối chiếu.
> 📘 PMP: Control Quality bằng statistical sampling; lỗi trong mẫu buộc mở rộng kiểm tra và root cause analysis.
> 💡 Nhật: Khách Nhật sẽ hỏi "サンプル以外は大丈夫か" (ngoài mẫu có ổn không); trả lời bằng kết quả rà mở rộng, không phải lời hứa.

## 5.5 Tài liệu vận hành (運用設計書, 運用手順書, 障害対応手順)

**Q552. Khách bảo hiểm nhân thọ B yêu cầu nộp cả 運用設計書 (unyou sekkei-sho – thiết kế vận hành) và 運用手順書 (unyou tejunsho – sổ tay thao tác vận hành). Member hỏi hai tài liệu khác nhau thế nào. PM giải thích thế nào?**
Em giải thích: 運用設計書 trả lời "vận hành cái gì, khi nào, ai làm, theo nguyên tắc nào": lịch batch, giám sát, backup, quản lý tài khoản, xử lý sự cố, phân vai giữa khách và vendor, SLA. 運用手順書 trả lời "làm từng bước thế nào": lệnh cụ thể, màn hình, kết quả mong đợi mỗi bước, điểm kiểm tra, cách quay lại nếu thất bại. Mỗi thủ tục trong 手順書 phải truy về một mục trong 設計書. Bằng chứng tốt là người vận hành chưa biết hệ thống làm theo 手順書 được trong buổi diễn tập. Bẫy: viết 手順書 như mô tả chức năng, thiếu kết quả mong đợi và điểm dừng.
> 📘 PMP: Transition và Close Project: deliverable bàn giao phải đủ để tổ chức vận hành nhận lợi ích (value delivery, PMBOK 7).
> 💡 Nhật: Người vận hành phía khách Nhật thường làm đúng từng chữ trong 手順書; chỗ nào phải "tự hiểu" là chỗ sẽ xảy ra sai sót.

**Q553. Diễn tập 運用手順書 với nhóm vận hành của ngân hàng A, người vận hành dừng ở bước 7 vì tài liệu ghi "ログを確認する" (kiểm tra log) mà không nói log nào, kiểm gì. Có 42 bước tương tự. PM xử lý thế nào?**
① Em ghi lại toàn bộ điểm người vận hành dừng hoặc hỏi trong buổi diễn tập làm danh sách sửa. ② Viết lại các bước theo mẫu: đường dẫn file, lệnh cụ thể, chuỗi cần tìm, kết quả bình thường trông như thế nào, nếu bất thường thì chuyển sang thủ tục nào. ③ Báo khách kế hoạch sửa và đặt lịch diễn tập lại. ④ Phòng ngừa: quy định mỗi 手順書 phải được một người không viết nó chạy thử trên môi trường kiểm chứng trước khi nộp; mục tiêu là diễn tập lại không có điểm dừng do tài liệu mơ hồ.
> 📘 PMP: Control Quality bằng kiểm thử với người dùng thật của deliverable; sửa đến khi đạt tiêu chí chấp nhận.

**Q554. 障害対応手順 (shougai taiou tejun – thủ tục xử lý sự cố) của khách phi nhân thọ C chỉ có bước kỹ thuật, không có ai liên lạc ai, trong bao lâu. Khách chỉ trích "không dùng được lúc nửa đêm". PM bổ sung thế nào?**
① Em xác nhận với khách cơ cấu liên lạc thực tế: ca trực, người phụ trách, vendor liên quan, ngưỡng thời gian. ② Bổ sung 連絡体制 (cơ cấu liên lạc): phân cấp mức độ sự cố, ai nhận báo đầu tiên, trong bao nhiêu phút phải báo cấp trên (ngưỡng theo thỏa thuận với khách), kênh liên lạc, người thay thế khi không liên lạc được. ③ Gửi khách bản sửa, xin xác nhận danh sách và số liên lạc. ④ Quy định cập nhật danh sách liên lạc khi có thay đổi nhân sự, và diễn tập liên lạc thử một lần trước go-live.
> 📘 PMP: Plan Communications Management cho tình huống khẩn cấp: escalation path, thời gian phản hồi, người thay thế.
> 💡 Nhật: Khách Nhật coi 初動 (phản ứng ban đầu) là thước đo chính khi đánh giá xử lý sự cố; thủ tục phải nói rõ 30 phút đầu ai làm gì.

**Q555. Còn 3 tuần tới go-live của khách bảo hiểm B, tài liệu vận hành mới xong 30% vì team dồn hết sức cho ST. Team đề nghị go-live trước, bổ sung tài liệu sau. PM chọn phương án nào?**
① Em xác nhận phần nào bắt buộc trước go-live: thủ tục khởi động/dừng, batch, backup, xử lý sự cố, giám sát; phần nào có thể bổ sung sau (thủ tục ít dùng). ② Lập kế hoạch dồn người viết phần bắt buộc, diễn tập phần quan trọng nhất trước go-live. ③ Báo khách trung thực tiến độ và đề xuất danh sách phân pha, khách quyết định có chấp nhận không; nếu thiếu phần bắt buộc thì go-live là rủi ro cần đưa vào tiêu chí go/no-go. ④ Bài học: tài liệu vận hành phải nằm trong WBS từ giai đoạn thiết kế, không phải việc cuối dự án.
> 📘 PMP: Monitor Risks và Control Schedule; deliverable bàn giao vận hành là một phần của phạm vi, không phải phần thêm.

**Q556. 運用手順書 của ngân hàng A có 28 chỗ ghi "適宜対応する" (xử lý phù hợp) hoặc "必要に応じて再実行" (chạy lại nếu cần). Khách nói người vận hành không có quyền tự phán đoán. PM xử lý thế nào?**
① Em lọc toàn bộ các cụm mơ hồ trong tài liệu. ② Thay mỗi chỗ bằng điều kiện cụ thể: điều kiện nào thì chạy lại, chạy lại tối đa bao nhiêu lần, nếu vẫn lỗi thì liên lạc ai; chỗ nào thật sự cần phán đoán thì ghi rõ "liên lạc người phụ trách X để quyết định". ③ Gửi khách bản sửa kèm bảng đối chiếu cũ – mới. ④ Đưa danh sách từ cấm (適宜, 必要に応じて, 問題なければ…) vào checklist tự động cho mọi tài liệu vận hành.
> 📘 PMP: Quality requirements phải rõ ràng và kiểm chứng được; tài liệu vận hành cũng là deliverable có tiêu chí chấp nhận.

**Q557. Khi review 運用手順書, BrSE phát hiện một lệnh xóa file tạm có đường dẫn sai, nếu chạy đúng như tài liệu sẽ xóa thư mục dữ liệu của batch. Tài liệu đã nộp khách bảo hiểm B 1 tuần trước. PM làm gì?**
① Em xác nhận ngay: khách đã dùng tài liệu này để thao tác ở môi trường nào chưa, đặc biệt môi trường có dữ liệu. ② Báo khách ngay trong ngày, yêu cầu tạm ngừng dùng thủ tục đó, gửi bản sửa có đánh dấu. ③ Rà toàn bộ lệnh có tính phá hủy (xóa, ghi đè, dừng dịch vụ) trong mọi 手順書 đã nộp. ④ Gốc rễ là lệnh được gõ tay, không chạy thử; quy định mọi lệnh trong 手順書 phải copy từ lần chạy thử thành công trên môi trường kiểm chứng, lệnh phá hủy phải có bước xác nhận đường dẫn trước khi chạy.
> 📘 PMP: Issue cần escalate ngay khi ảnh hưởng tiềm tàng cao; minh bạch với stakeholder là nghĩa vụ.
> 💡 Nhật: Báo lỗi này ngay, kể cả khi chưa ai bị ảnh hưởng; khách Nhật sẽ đánh giá cao hành động tự phát hiện và tự báo.

**Q558. Sau go-live, hệ thống của khách phi nhân thọ C sẽ do một 運用ベンダー (vendor vận hành) khác tiếp nhận. Họ yêu cầu tài liệu theo format của họ và từ chối nhận 2 tài liệu của VTI. PM xử lý thế nào?**
① Em xác nhận hợp đồng của VTI quy định format nào và ai chịu trách nhiệm chuyển đổi. ② Họp ba bên (khách, VTI, vendor vận hành) để thống nhất danh mục tài liệu bàn giao, format, tiêu chí chấp nhận; khách là bên quyết định. ③ Nếu chuyển format nằm ngoài phạm vi, ước tính công và xử lý như thay đổi; nếu trong phạm vi thì lập kế hoạch thực hiện. ④ Bài học: xác định bên nhận vận hành và yêu cầu của họ từ giai đoạn thiết kế vận hành, mời họ review sớm.
> 📘 PMP: Identify Stakeholders sớm, kể cả bên tiếp nhận sau dự án; Manage Stakeholder Engagement thông qua khách là chủ thể hợp đồng.

**Q559. Trong 運用手順書 batch đêm của ngân hàng A chỉ có thủ tục chạy bình thường, không có thủ tục chạy lại khi job thứ 5 trong chuỗi 12 job thất bại. Khách hỏi: "chạy lại từ đâu, dữ liệu có bị trùng không?". PM xử lý thế nào?**
① Em xác nhận thiết kế từng job: có thể chạy lại an toàn không (idempotent), cần xóa dữ liệu tạm hay khôi phục trước không. ② Bổ sung cho từng job: điều kiện khởi động lại, điểm bắt đầu lại, bước dọn dữ liệu nếu cần, cách xác nhận không trùng, thời hạn trễ nhất trước giờ mở dịch vụ. ③ Diễn tập kịch bản lỗi job thứ 5 trên môi trường kiểm chứng, lưu エビデンス. ④ Đưa "thủ tục chạy lại cho mỗi job" vào tiêu chí hoàn thành của thiết kế batch.
> 📘 PMP: Identify Risks và lập contingency plan cho kịch bản thất bại đã biết trước.

**Q560. Thủ tục backup/restore trong tài liệu vận hành của khách bảo hiểm B chưa từng được chạy restore thật, chỉ chạy backup. Còn 4 tuần tới go-live. PM làm gì?**
① Em xác nhận môi trường nào có thể diễn tập restore mà không ảnh hưởng test đang chạy. ② Lên lịch diễn tập restore đầy đủ: thời gian thực hiện, kiểm tra tính toàn vẹn dữ liệu sau restore, so với mục tiêu thời gian khôi phục đã thống nhất với khách. ③ Báo khách kết quả, sửa thủ tục theo những gì phát sinh khi diễn tập. ④ Đưa diễn tập restore vào tiêu chí go-live; một thủ tục backup chưa restore thử thì chưa được coi là hoàn thành.
> 📘 PMP: Plan Risk Responses: contingency plan phải được kiểm chứng, không chỉ viết ra.
> 💡 Nhật: Khách tài chính Nhật thường được kiểm tra nội bộ về khả năng khôi phục; có エビデンス diễn tập restore là điểm cộng lớn.

**Q561. Sau 2 lần CR thay đổi giao diện màn hình quản trị, 40% ảnh chụp trong 運用手順書 của khách phi nhân thọ C không còn khớp với màn hình thật. Người vận hành báo bị nhầm nút. PM xử lý thế nào?**
① Em xác nhận màn hình nào đã đổi và thủ tục nào bị ảnh hưởng (dùng danh sách CR). ② Cập nhật ảnh và bước thao tác, ưu tiên thủ tục dùng hằng ngày và thủ tục sự cố. ③ Báo khách và người vận hành bản mới, thu hồi bản cũ khỏi nơi lưu dùng chung. ④ Gốc rễ là quy trình CR không có bước cập nhật tài liệu vận hành; bổ sung mục này vào checklist đóng CR, và hạn chế ảnh chụp toàn màn hình bằng cách ghi tên nút, tên menu bằng chữ để ít phải cập nhật.
> 📘 PMP: Perform Integrated Change Control: change phải cập nhật mọi deliverable liên quan, kể cả tài liệu vận hành.

**Q562. Chuẩn bị 運用引継ぎ (unyou hikitsugi – bàn giao vận hành) cho bộ phận vận hành nội bộ của ngân hàng A, khách hỏi: "làm sao biết bàn giao đã đủ?". PM thiết kế thế nào?**
Em thiết kế danh sách bàn giao có tiêu chí: tài liệu (設計書, 手順書, 障害対応手順, danh sách tài khoản, パラメータシート), buổi giải thích, diễn tập với người vận hành, bảng hỏi đáp đã đóng. Mỗi mục có người nhận ký xác nhận. Thêm giai đoạn hỗ trợ sau go-live với phạm vi và thời hạn rõ. Bằng chứng: biên bản diễn tập, danh sách câu hỏi đã trả lời, chữ ký nhận. Bẫy: chỉ gửi tài liệu qua email rồi coi là đã bàn giao, và không thống nhất thời điểm trách nhiệm chuyển sang khách.
> 📘 PMP: Close Project or Phase: chuyển giao deliverable và có xác nhận chính thức (formal acceptance).
> 💡 Nhật: Khách Nhật thích 引継ぎチェックリスト có ô ký cho cả hai bên; không có chữ ký thì về sau trách nhiệm rất khó phân định.

**Q563. Khách bảo hiểm B yêu cầu bổ sung vào 障害対応手順 kịch bản "nghi ngờ rò rỉ dữ liệu khách hàng", trong khi tài liệu hiện chỉ có sự cố kỹ thuật. PM xử lý thế nào?**
① Em xác nhận khách đã có quy trình xử lý sự cố bảo mật cấp công ty chưa, vì thủ tục hệ thống phải khớp với quy trình đó. ② Phối hợp với bộ phận bảo mật của khách để viết phần hệ thống: dấu hiệu phát hiện, bảo toàn log và bằng chứng (không xóa, không khởi động lại tùy tiện), cô lập, liên lạc đầu mối bảo mật, ai có quyền quyết định báo cáo ra ngoài. ③ Báo khách nếu yêu cầu vượt phạm vi để xử lý như thay đổi. ④ Đề xuất diễn tập trên bàn (tabletop) một lần trước go-live.
> 📘 PMP: Plan Risk Responses cho rủi ro ảnh hưởng cao; phối hợp với stakeholder chuyên môn (bảo mật, pháp chế) thay vì tự quyết.

## 5.6 Quy trình kiểm tra chất lượng deliverable trước khi nộp

**Q564. PM mới nhận dự án 基本設計 cho khách bảo hiểm nhân thọ B, team 15 người chưa có quy trình kiểm tra trước khi nộp, tài liệu viết xong là gửi. PM thiết lập quy trình thế nào?**
Em thiết lập 4 lớp: ① người viết self-check theo checklist (nội dung, format, chính tả, thuật ngữ); ② cross-check bởi người khác trong team, đối chiếu với tài liệu đầu vào; ③ BrSE/PM kiểm điểm nghiệp vụ và cách diễn đạt tiếng Nhật; ④ quality gate trước khi gửi: đủ chữ ký các lớp, 0 chỉ trích nội bộ mở, đúng version và tên file. Bằng chứng là bảng theo dõi review có người, ngày, kết quả từng lớp. Bẫy: đặt 4 lớp nhưng không có thời gian trong lịch, nên lớp sau bị bỏ; phải đưa thời gian review vào WBS ngay từ đầu.
> 📘 PMP: Manage Quality (quality assurance): xây quy trình để chất lượng được tạo ra, không chỉ kiểm ở cuối.
> 💡 Nhật: Khách Nhật hay hỏi "社内レビューは済んでいますか" (đã review nội bộ chưa); có bảng ghi review nội bộ là câu trả lời thuyết phục nhất.

**Q565. Team viết 詳細設計書 cho khách phi nhân thọ C hỏi checklist self-check nên có những mục gì, vì checklist hiện tại chỉ có 5 dòng chung chung. PM hướng dẫn thế nào?**
Em hướng dẫn checklist chia nhóm: hình thức (bìa, version, 改訂履歴, mục lục, số trang, bản in), nhất quán (tên item, ID, thuật ngữ khớp 基本設計書 và 用語集), nội dung (mọi xử lý có input/output, điều kiện, ngoại lệ, message), truy vết (yêu cầu và CR liên quan), ngôn ngữ (chính tả, câu mơ hồ, từ cấm), bảo mật (không có dữ liệu thật, không có thông tin khách khác, không còn comment nội bộ). Mỗi mục là câu hỏi trả lời có/không. Bằng chứng: checklist đã tick lưu cùng tài liệu. Bẫy: checklist quá dài khiến người dùng tick cho xong; nên gom từ chỉ trích thật của khách.
> 📘 PMP: Checklist là công cụ của Manage Quality và Control Quality; cập nhật từ lessons learned để có giá trị thực tế.

**Q566. Mọi tài liệu gửi khách ngân hàng A đều phải qua 1 BrSE duy nhất kiểm tra tiếng Nhật. Hàng đợi tồn 14 tài liệu, chậm 5 ngày. PM xử lý thế nào?**
① Em xác nhận BrSE đang làm những việc gì trong review: sửa chính tả, sửa thuật ngữ, kiểm logic nghiệp vụ. ② Chuyển phần việc không cần BrSE về lớp trước: tool kiểm chính tả và 用語集, comtor kiểm câu; BrSE chỉ tập trung vào logic nghiệp vụ và điểm khách hay chỉ trích. ③ Báo khách lịch nộp điều chỉnh nếu ảnh hưởng mốc, xếp ưu tiên tài liệu theo mốc. ④ Phát triển thêm 1 người kiểm tiếng Nhật (member có năng lực) bằng kèm cặp, để không phụ thuộc một người.
> 📘 PMP: Resource optimization và loại bỏ bottleneck; Develop Team để giảm rủi ro phụ thuộc một cá nhân.
> 💡 Nhật: BrSE làm "máy sửa chính tả" là lãng phí lớn nhất của dự án offshore Nhật; giá trị của BrSE là hiểu ý khách.

**Q567. Cross-check trong team khách bảo hiểm B được làm theo cặp cố định, hai người kiểm cho nhau. Khách vẫn tìm ra lỗi cùng loại mà cross-check đã "OK". PM điều chỉnh thế nào?**
① Em đối chiếu lỗi khách tìm ra với checklist cross-check: lỗi nằm ngoài checklist hay checklist có mà người kiểm bỏ qua. ② Đổi cặp luân phiên, người kiểm phải ghi rõ đã kiểm theo tài liệu đầu vào nào và để lại ít nhất phát hiện hoặc xác nhận cụ thể từng mục, không chỉ chữ "OK". ③ Báo khách biện pháp cải tiến khi trả lời chỉ trích. ④ Gốc rễ: cặp cố định dễ chủ quan, tin nhau; xoay vòng và để PM/BrSE kiểm lấy mẫu kết quả cross-check định kỳ.
> 📘 PMP: Manage Quality: giảm thiên lệch (bias) trong review bằng tính độc lập và kiểm tra chéo có bằng chứng.

**Q568. Lãnh đạo VTI yêu cầu PM định nghĩa "quality gate" trước khi nộp deliverable cho khách phi nhân thọ C, vì lần trước một tài liệu thiếu nửa chương vẫn được gửi. PM định nghĩa thế nào?**
Em định nghĩa quality gate là điều kiện bắt buộc phải đạt, ai kiểm, trước khi deliverable rời team: đủ các mục theo mục lục đã thống nhất; self-check và cross-check có chữ ký; 0 chỉ trích nội bộ mức nghiêm trọng còn mở; mọi chỉ trích vòng trước của khách đã xử lý; đúng tên file, version, định dạng; kiểm bảo mật (không dữ liệu thật, không comment nội bộ). Người duyệt gate là PM hoặc QA, không phải người viết. Bằng chứng là bản ghi gate cho từng lần nộp. Bẫy: gate bị "mở cửa" khi gấp; mọi ngoại lệ phải được ghi và báo khách trạng thái thật.
> 📘 PMP: Phase gate / quality gate với tiêu chí đi tiếp rõ ràng; ngoại lệ phải được phê duyệt chính thức.

**Q569. Team đề xuất dùng tool kiểm tra tự động cho 誤字脱字, từ cấm, nhất quán thuật ngữ trên tài liệu Excel/Word trước khi nộp khách ngân hàng A. PM đánh giá thế nào?**
① Em xác nhận tool chạy được trong môi trường làm việc (máy dự án, VDI) và không gửi nội dung tài liệu ra dịch vụ bên ngoài. ② Thử trên 2–3 tài liệu đã có chỉ trích của khách, xem tool bắt được bao nhiêu phần trăm lỗi đã biết và bao nhiêu báo nhầm. ③ Nếu hiệu quả, đưa vào bước self-check như bắt buộc, nhưng không thay người review nội dung. ④ Duy trì danh sách từ cấm và 用語集 làm đầu vào cho tool, cập nhật từ chỉ trích mới.
> 📘 PMP: Automation trong Manage Quality; đánh giá bằng thử nghiệm và dữ liệu trước khi áp dụng.
> 💡 Nhật: Tool trên cloud hoặc AI công cộng có thể vi phạm quy định bảo mật của khách tài chính; luôn hỏi trước khi cho tài liệu khách đi qua bất kỳ dịch vụ ngoài nào.

**Q570. Tài liệu gửi khách bảo hiểm B được viết tiếng Việt rồi comtor dịch. Sau khi dịch không ai kiểm lại nội dung kỹ thuật, khách phát hiện 2 điều kiện bị dịch ngược nghĩa. PM bổ sung bước kiểm tra thế nào?**
① Em xác nhận dạng lỗi: chủ yếu ở câu điều kiện, phủ định, đơn vị, số liệu. ② Thêm bước sau dịch: người viết gốc (hoặc dev) đọc bản tiếng Nhật ở các phần logic, hoặc dùng dịch ngược có kiểm soát để so ý; BrSE kiểm phần nghiệp vụ. ③ Báo khách nguyên nhân và biện pháp khi trả lời chỉ trích. ④ Giảm lượng cần dịch: viết logic bằng bảng điều kiện, giữ tên item/thông điệp bằng tiếng Nhật từ đầu, chỉ dịch phần mô tả.
> 📘 PMP: Manage Quality: thêm kiểm soát tại điểm có rủi ro lỗi cao trong quy trình (process analysis).

**Q571. Khách phi nhân thọ C yêu cầu nộp 詳細設計書 theo 4 đợt (分割納品). Đợt 3 có 15 chỗ mâu thuẫn với đợt 1 đã được duyệt (tên bảng, mã lỗi). PM xử lý thế nào?**
① Em xác nhận mâu thuẫn do đợt 3 sai hay đợt 1 cần thay đổi. ② Nếu đợt 1 cần đổi, xử lý như thay đổi tài liệu đã duyệt: cập nhật đợt 1, ghi 改訂履歴, xin khách duyệt lại; không để hai đợt mô tả khác nhau. ③ Báo khách danh sách 15 chỗ và cách xử lý. ④ Phòng ngừa: dùng các tài liệu dùng chung (định nghĩa bảng, danh sách mã lỗi, 用語集) làm nguồn duy nhất cho mọi đợt; mỗi đợt nộp có bước kiểm nhất quán với các đợt trước.
> 📘 PMP: Configuration management và quản lý baseline xuyên suốt nhiều lần bàn giao.

**Q572. Ba tháng qua, khách ngân hàng A lặp lại cùng một loại chỉ trích "message ID không khớp danh sách message" ở 5 tài liệu khác nhau. PM xử lý thế nào để không lặp lại lần 6?**
① Em xác nhận lỗi này đến từ đâu: danh sách message thay đổi thường xuyên hay người viết không tra danh sách. ② Thực hiện 横展開: rà mọi tài liệu đang viết và đã nộp để sửa chủ động trước khi khách chỉ. ③ Báo khách kết quả rà soát và biện pháp, thể hiện đã hiểu vấn đề ở mức hệ thống. ④ Phòng ngừa bằng cơ chế chứ không bằng nhắc nhở: thêm mục kiểm message vào checklist, tạo công thức/tool đối chiếu message ID tự động với danh sách gốc.
> 📘 PMP: Lessons learned và root cause analysis; biện pháp phòng ngừa phải loại bỏ nguyên nhân, không chỉ sửa triệu chứng.
> 💡 Nhật: Khách Nhật chấp nhận lỗi lần đầu, nhưng 同じ指摘 (chỉ trích lặp lại) bị coi là vendor không học; đó là lúc niềm tin giảm mạnh.

**Q573. PM phát hiện một member mới tick đủ 40 mục checklist self-check trong 3 phút cho tài liệu 60 trang, và tài liệu đó có 9 lỗi khách tìm ra. PM xử lý thế nào?**
① Em nói chuyện riêng với member để hiểu: không hiểu mục checklist, bị áp lực thời gian hay coi là thủ tục. ② Cùng member làm lại self-check một tài liệu để hướng dẫn cách kiểm từng mục, giải thích mỗi mục bắt nguồn từ chỉ trích thật nào. ③ Sửa 9 lỗi và rà các tài liệu khác của member. ④ Thay đổi cơ chế: checklist yêu cầu ghi bằng chứng ngắn cho mục quan trọng (ví dụ số chỗ đã đối chiếu), người cross-check kiểm lấy mẫu chất lượng self-check, và đảm bảo kế hoạch có đủ thời gian self-check.
> 📘 PMP: Develop Team (coaching) và Manage Quality; tìm nguyên nhân trong hệ thống trước khi quy lỗi cá nhân.

**Q574. Member gửi nhầm cho khách bảo hiểm B bản 詳細設計書 nội bộ, còn comment tiếng Việt như "chỗ này khách đòi vô lý" và ghi chú ước tính công. PM làm gì trước tiên?**
① Em xác nhận file đã gửi cho ai, nội dung comment, có thông tin nhạy cảm khác không. ② Liên lạc khách ngay, xin lỗi, đề nghị xóa bản đó, gửi bản chính thức; không giải thích vòng vo về comment. ③ Báo lãnh đạo nội bộ vì ảnh hưởng quan hệ khách hàng; nếu comment gây hiểu lầm, chuẩn bị gặp trực tiếp người phụ trách bên khách. ④ Phòng ngừa: tách thư mục nội bộ và thư mục nộp, chỉ file đã qua quality gate mới được chuyển sang thư mục nộp; bước cuối dùng chức năng kiểm tra tài liệu để xóa comment và thuộc tính trước khi gửi.
> 📘 PMP: Manage Stakeholder Engagement khi có sự cố quan hệ; minh bạch và hành động sửa nhanh.
> 💡 Nhật: Viết comment nội bộ như thể khách sẽ đọc; người Nhật đọc được bản dịch và một câu chê khách có thể làm hỏng quan hệ lâu dài.

**Q575. Khi 検収 (kenshuu – nghiệm thu), khách ngân hàng A đối chiếu 納品物一覧 (danh sách deliverable) với hợp đồng và thấy thiếu 3 tài liệu, 2 tài liệu sai version. Khách tạm dừng nghiệm thu. PM xử lý thế nào?**
① Em đối chiếu hợp đồng, danh sách deliverable đã thống nhất và các CR để xác định chính xác thiếu gì, version nào là đúng. ② Hoàn thiện và nộp bổ sung trong thời gian sớm nhất, kèm danh sách cập nhật có version và ngày của từng file. ③ Báo khách lịch nộp bổ sung, báo lãnh đạo nội bộ vì ảnh hưởng thanh toán. ④ Phòng ngừa: lập 納品物一覧 từ đầu dự án theo hợp đồng, cập nhật khi có CR, kiểm đối chiếu từng dòng trước khi nộp nghiệm thu.
> 📘 PMP: Validate Scope: nghiệm thu chính thức dựa trên deliverable đã được xác minh và đối chiếu với tiêu chí trong hợp đồng.

**Q576. Dự án của khách bảo hiểm B có 60 người chia 4 team, chất lượng tài liệu chênh lệch lớn: team 1 hầu như không bị chỉ trích, team 3 bị chỉ trích gấp nhiều lần. PM chuẩn hóa thế nào?**
① Em xác nhận khác biệt ở đâu: template, checklist, kỹ năng, nghiệp vụ khó hơn hay thời gian review ít hơn. ② Lấy cách làm của team 1 làm chuẩn chung: template, checklist, ví dụ tài liệu mẫu đạt chuẩn; mỗi team cử 1 người phụ trách chất lượng tài liệu. ③ Thêm bước cross-check giữa các team cho tài liệu đầu tiên của mỗi team để đồng bộ cách hiểu. ④ Báo khách và lãnh đạo kế hoạch chuẩn hóa; theo dõi chỉ trích theo team để thấy cải thiện.
> 📘 PMP: Manage Quality ở cấp chương trình: chuẩn hóa quy trình và chia sẻ best practice giữa các team (Manage Project Knowledge).
> 💡 Nhật: Khách Nhật không phân biệt team nào; một team kém kéo hình ảnh cả vendor xuống, nên chuẩn hóa là việc của PM tổng.

## 5.7 Mạng đóng (閉域網), môi trường cách ly, VDI

**Q577. Dự án mới với khách bảo hiểm nhân thọ B yêu cầu làm việc trong 閉域網 (heiikimou – mạng đóng, tách khỏi internet). Member hỏi điều này ảnh hưởng gì tới cách làm việc. PM giải thích thế nào?**
Em giải thích: mọi tài liệu, source, dữ liệu của khách chỉ nằm trong mạng đóng, truy cập qua VDI hoặc máy được cấp; không internet tự do, không copy ra ngoài, không cài phần mềm tùy ý. Ảnh hưởng: tra cứu bên ngoài phải làm trên máy khác và không mang nội dung khách sang; thư viện, tool phải xin phép mang vào; trao đổi file ra/vào phải qua thủ tục 持ち出し/持ち込み申請 (xin mang ra/mang vào). Bằng chứng tuân thủ là log truy cập và sổ xin phép. Bẫy: ước tính công như môi trường mở, không tính thời gian xin phép và độ chậm của VDI.
> 📘 PMP: Enterprise environmental factors ảnh hưởng tới kế hoạch; tailoring ước tính và lịch theo ràng buộc môi trường.
> 💡 Nhật: Khách tài chính Nhật thường dẫn chiếu chuẩn FISC (bộ chuẩn an toàn hệ thống tài chính) cho môi trường làm việc; PM nên biết khách áp dụng ở mức nào.

**Q578. VDI của khách ngân hàng A chậm, build mất 20 phút. Hai dev đề nghị copy source về laptop công ty để code rồi đưa lại vào, "chỉ là code, không có dữ liệu khách". PM trả lời thế nào?**
① Em xác nhận quy định hợp đồng và bảo mật: source của khách là tài sản thông tin của khách, thường không được mang ra khỏi môi trường quy định. ② Từ chối rõ ràng, nhắc không được tự làm. ③ Giải quyết gốc vấn đề: đo thời gian chờ build, tính ảnh hưởng năng suất, đề xuất khách tăng tài nguyên VDI hoặc cấu hình build tăng dần; báo khách bằng số liệu. ④ Nếu không cải thiện được, đưa ảnh hưởng vào kế hoạch và báo cáo tiến độ, không để team tự tìm "đường tắt".
> 📘 PMP: Tuân thủ là ràng buộc (constraint); PM quản lý ảnh hưởng của ràng buộc bằng đề xuất qua đúng kênh, không vượt qua nó.

**Q579. Trong ODC (phòng làm việc riêng cho khách), PM thấy một member dùng điện thoại chụp màn hình tài liệu thiết kế của khách bảo hiểm B "để tối về đọc". PM xử lý thế nào?**
① Em yêu cầu dừng ngay, cùng member xác nhận ảnh đã chụp và xóa trước mặt, kiểm tra ảnh có được gửi hoặc đồng bộ lên cloud chưa. ② Báo bộ phận bảo mật nội bộ theo quy trình sự cố; nếu ảnh đã rời thiết bị hoặc quy định yêu cầu, báo khách. ③ Ghi lại sự việc, xử lý theo quy định công ty. ④ Gốc rễ: điện thoại được mang vào khu vực, member chưa hiểu mức độ nghiêm trọng; siết quy định gửi điện thoại ở tủ trước khi vào, đào tạo lại toàn team bằng ví dụ thực tế.
> 📘 PMP: Ethics và compliance: PM chịu trách nhiệm đảm bảo team tuân thủ quy định, xử lý vi phạm minh bạch.
> 💡 Nhật: "Chỉ để đọc tối nay" không phải là lý do được chấp nhận; khách Nhật đánh giá theo hành vi, không theo ý định.

**Q580. Để điều tra lỗi, team cần phân tích file log 500 MB trên môi trường của khách phi nhân thọ C bằng tool chỉ có ở máy offshore. Clipboard và truyền file bị chặn. PM làm gì?**
① Em xác nhận trước tiên có thể phân tích trong môi trường khách không: xin mang tool vào (持ち込み申請) thường an toàn hơn mang dữ liệu ra. ② Nếu bắt buộc mang log ra, kiểm log có dữ liệu cá nhân không, che/xóa phần đó, rồi làm 持ち出し申請 theo thủ tục của khách, ghi rõ mục đích, nội dung, nơi lưu, thời hạn xóa. ③ Báo khách lý do và thời gian cần thiết. ④ Sau khi dùng, xóa theo cam kết và báo xác nhận xóa; lưu hồ sơ thủ tục.
> 📘 PMP: Tuân thủ quy trình của tổ chức khách (organizational process assets); lựa chọn phương án ít rủi ro nhất.

**Q581. Một member dán đoạn 詳細設計書 của khách ngân hàng A vào một dịch vụ AI công cộng để dịch nhanh. PM phát hiện qua trao đổi nhóm. PM xử lý thế nào?**
① Em xác nhận nội dung đã dán: phần nào, có dữ liệu cá nhân hay thông tin nhạy cảm không, dán qua tài khoản nào, dịch vụ có lưu dữ liệu không. ② Dừng ngay, báo bộ phận bảo mật nội bộ; theo hợp đồng và quy định, báo khách vì thông tin của khách đã đi ra dịch vụ bên ngoài. ③ Xử lý theo hướng dẫn của bảo mật: xóa lịch sử nếu có thể, ghi nhận sự việc. ④ Phòng ngừa: ban hành quy định rõ về công cụ AI được và không được dùng, chặn kỹ thuật nếu có thể, và cung cấp công cụ dịch được phép để member không phải tự tìm.
> 📘 PMP: Manage Risks và compliance; ngăn ngừa bằng quy định rõ và công cụ thay thế hợp lệ.
> 💡 Nhật: Khách tài chính Nhật ngày càng hỏi cụ thể về việc vendor dùng AI; có sẵn chính sách bằng văn bản giúp trả lời audit dễ hơn.

**Q582. Công ty cho phép làm từ xa, một member truy cập VDI của khách bảo hiểm B từ quán cà phê bằng wifi công cộng. Hợp đồng không ghi rõ địa điểm làm việc. PM xử lý thế nào?**
① Em xác nhận quy định của khách về địa điểm và mạng truy cập (thường có trong quy định bảo mật hoặc phụ lục hợp đồng), và quy định của công ty. ② Trong lúc chưa rõ, áp dụng mức thận trọng: chỉ truy cập từ văn phòng hoặc nhà với điều kiện đã duyệt, không dùng mạng công cộng, không làm ở nơi người khác nhìn thấy màn hình. ③ Hỏi khách để có quy định chính thức bằng văn bản, ghi vào kế hoạch dự án. ④ Thông báo cho toàn team, không chỉ member vi phạm.
> 📘 PMP: Khi quy định chưa rõ, PM làm rõ với stakeholder và ghi lại thay vì tự suy diễn theo hướng thuận tiện.

**Q583. Khởi động dự án 40 người cho khách ngân hàng A, khách yêu cầu ODC có kiểm soát ra vào bằng thẻ, cấm điện thoại, camera, máy không có cổng USB. Chuẩn bị trong 3 tuần. PM lập kế hoạch thế nào?**
① Em lấy danh sách yêu cầu bảo mật của khách bằng văn bản, chuyển thành checklist có tiêu chí kiểm. ② Phân việc cho bộ phận hành chính, IT, bảo mật với mốc cụ thể: phòng, khóa thẻ, camera, tủ giữ đồ, cấu hình máy, mạng riêng; ký cam kết bảo mật với từng thành viên. ③ Mời khách kiểm tra trước khi bắt đầu (hoặc gửi ảnh, biên bản kiểm tra), báo rủi ro nếu không kịp 3 tuần. ④ Kế hoạch dự phòng: nhóm làm việc không cần dữ liệu khách có thể bắt đầu trước ở khu vực khác.
> 📘 PMP: Plan Resource Management và quản lý ràng buộc môi trường; requirement bảo mật là phần của phạm vi khởi động.

**Q584. Đường kết nối mạng đóng giữa văn phòng Việt Nam và khách phi nhân thọ C bị gián đoạn 2 ngày, team 25 người gần như không làm được việc. PM xử lý thế nào?**
① Em xác nhận nguyên nhân, bên chịu trách nhiệm (nhà mạng, khách, VTI), và dự kiến thời gian khôi phục. ② Sắp xếp việc không cần môi trường khách: ôn lại nghiệp vụ bằng tài liệu được phép, chuẩn bị test data giả, đào tạo; không cho phép đường tắt như gửi tài liệu qua email cá nhân. ③ Báo khách ảnh hưởng tiến độ hằng ngày, ghi vào 課題管理表. ④ Sau sự cố, đề xuất phương án dự phòng (đường kết nối thứ hai, quy trình xử lý khi mất kết nối), cập nhật risk register.
> 📘 PMP: Implement Risk Responses và cập nhật risk register; rủi ro phụ thuộc hạ tầng cần có kế hoạch dự phòng.
> 💡 Nhật: Báo cáo ảnh hưởng bằng giờ công mất cụ thể; khách Nhật cần số này để giải thích nội bộ hoặc xem xét bù tiến độ.

**Q585. Team cần một thư viện OSS mới cho chức năng xuất PDF của khách bảo hiểm B. Môi trường đóng không tải được. Một dev đề nghị tải về USB rồi cắm vào máy dự án. PM làm gì?**
① Em xác nhận quy trình 持ち込み của khách: cần thông tin gì (tên, phiên bản, license, nguồn), quét virus ở đâu, ai duyệt. ② Kiểm license có phù hợp dùng thương mại và hợp đồng không, kiểm lỗ hổng đã biết của phiên bản. ③ Nộp đơn xin phép, chờ duyệt, mang vào theo kênh khách chỉ định; không dùng USB nếu không được phép. ④ Đưa thời gian xin phép vào kế hoạch; tổng hợp danh sách thư viện cần dùng từ sớm (ở giai đoạn thiết kế) để xin một lần.
> 📘 PMP: Procurement và compliance: thành phần bên ngoài phải được đánh giá và duyệt theo quy trình của tổ chức.

**Q586. Kiểm tra định kỳ phát hiện máy của 2 member ở dự án khách ngân hàng A không bị chặn cổng USB như cam kết, và có lịch sử cắm thiết bị lưu trữ. PM xử lý thế nào?**
① Em xác nhận qua log: thiết bị nào, thời điểm nào, file nào đã được sao chép (nếu log có), máy có tài liệu khách không. ② Khóa cổng ngay, thu thiết bị để kiểm tra cùng bộ phận bảo mật; nếu có khả năng dữ liệu khách bị sao chép thì báo khách theo quy trình. ③ Rà cấu hình của toàn bộ máy dự án để tìm máy khác bị sót. ④ Gốc rễ là lỗi cấu hình và kiểm tra lúc cấp máy chưa đủ; bổ sung bước kiểm có bằng chứng khi cấp máy và kiểm định kỳ.
> 📘 PMP: Control Quality áp dụng cho kiểm soát bảo mật; phát hiện lệch phải mở rộng kiểm tra toàn bộ (横展開).
> 💡 Nhật: Khách Nhật quan tâm câu "cam kết với khách đã không được thực hiện" hơn là có rò rỉ hay không; trả lời bằng kết quả rà toàn bộ.

**Q587. Dự án với khách phi nhân thọ C kết thúc. Hợp đồng yêu cầu xóa toàn bộ thông tin của khách và nộp データ消去証明 (chứng nhận xóa dữ liệu). PM thực hiện thế nào?**
Em lập danh sách nơi có thể còn thông tin khách: máy dự án, ổ chia sẻ, email, công cụ quản lý công việc, bản sao lưu, giấy in, tài khoản trên hệ thống khách. Với từng nơi, xác định cách xóa (xóa an toàn, hủy giấy, thu hồi tài khoản), người thực hiện, người xác nhận và bằng chứng (log xóa, biên bản hủy). Tổng hợp thành chứng nhận có danh sách, ngày, chữ ký, gửi khách. Bẫy hay gặp: quên bản sao lưu, email cá nhân của member, file tải về thư mục tạm, và tài liệu giữ lại "để tham khảo dự án sau" mà không được khách đồng ý.
> 📘 PMP: Close Project or Phase: thực hiện các nghĩa vụ hợp đồng khi đóng dự án, lưu hồ sơ đóng.

**Q588. Lỗi production ở ngân hàng A chỉ tái hiện với một tổ hợp dữ liệu thật. Khách không cho mang dữ liệu ra, team offshore không có quyền vào môi trường production. Lỗi đang ảnh hưởng 200 giao dịch/ngày. PM xử lý thế nào?**
① Em xác nhận thông tin có thể lấy mà không lộ dữ liệu: log lỗi, stack trace, đặc điểm dữ liệu (độ dài, ký tự đặc biệt, null) mà không cần giá trị thật. ② Đề xuất các phương án hợp lệ: nhân viên khách hoặc kỹ sư onsite có quyền điều tra theo hướng dẫn của team; tạo dữ liệu giả có cùng đặc điểm để tái hiện ở môi trường test; phiên điều tra có giám sát nếu khách đồng ý. ③ Báo khách các phương án và rủi ro, khách quyết định. ④ Song song, đề xuất biện pháp giảm ảnh hưởng tạm thời; không ai được "mượn" dữ liệu ra ngoài vì áp lực.
> 📘 PMP: Problem solving trong ràng buộc: đưa nhiều phương án, phân tích rủi ro, để người có thẩm quyền quyết định.
> 💡 Nhật: Khách Nhật thường chấp nhận cách "nhân viên khách làm theo hướng dẫn của vendor" hơn là mở quyền cho vendor; chuẩn bị hướng dẫn thật chi tiết.

## 5.8 Phân quyền tối thiểu, quản lý tài khoản, tài khoản đặc quyền

**Q589. Khách bảo hiểm nhân thọ B yêu cầu team VTI đề xuất phân quyền truy cập cho 30 thành viên vào các môi trường dev, kiểm chứng, production. PM áp dụng nguyên tắc nào?**
Em áp dụng nguyên tắc phân quyền tối thiểu (最小権限): mỗi người chỉ có quyền cần cho vai trò, trong thời gian cần. Cách làm: lập ma trận vai trò × môi trường × quyền (đọc, ghi, quản trị); mặc định không ai trong team offshore có quyền production, quyền quản trị chỉ cấp tạm thời theo đơn; tài khoản gắn với từng cá nhân, không dùng chung. Bằng chứng: bảng phân quyền được khách duyệt, danh sách tài khoản thực tế đối chiếu được với bảng. Bẫy: cấp quyền rộng "cho tiện" lúc đầu rồi không thu lại, và cấp theo người thay vì theo vai trò.
> 📘 PMP: RACI và Plan Resource Management: vai trò, trách nhiệm và quyền hạn được định nghĩa rõ ràng.
> 💡 Nhật: Khách tài chính Nhật thường yêu cầu nộp 権限一覧 (danh sách quyền) như một deliverable; chuẩn bị theo format của khách ngay từ đầu.

**Q590. Một member dự án ngân hàng A nghỉ việc ngày thứ Sáu. Thứ Ba tuần sau khi rà soát, PM thấy tài khoản VDI và tài khoản hệ thống test của người đó vẫn hoạt động. PM xử lý thế nào?**
① Em yêu cầu vô hiệu hóa ngay tất cả tài khoản của người đó, kiểm log xem có lần đăng nhập nào sau ngày nghỉ không. ② Nếu có truy cập bất thường, xử lý như sự cố bảo mật và báo khách; nếu không, vẫn báo khách theo quy định về chậm thu hồi. ③ Rà toàn bộ người đã rời dự án trong 3 tháng gần đây xem còn tài khoản nào sót. ④ Gốc rễ: quy trình nghỉ việc của công ty không kết nối với danh sách tài khoản dự án; lập checklist rời dự án có danh sách tất cả tài khoản, thu hồi trong ngày cuối và xác nhận bằng chữ ký.
> 📘 PMP: Manage Team và release resources: quy trình rút nhân sự phải bao gồm thu hồi quyền truy cập.

**Q591. Phát hiện team 12 người ở dự án khách phi nhân thọ C dùng chung 1 tài khoản để đăng nhập DB môi trường kiểm chứng, mật khẩu ghi trên bảng trắng. PM xử lý thế nào?**
① Em xác nhận phạm vi: tài khoản nào dùng chung, môi trường nào, có dữ liệu nhạy cảm không, từ bao lâu. ② Đổi mật khẩu ngay, xóa thông tin trên bảng; xin khách cấp tài khoản cá nhân cho từng người theo vai trò. ③ Báo khách trung thực vì log hiện tại không truy được ai đã làm gì. ④ Gốc rễ: quy trình xin tài khoản mất thời gian nên team dùng chung cho nhanh; làm việc với khách để có quy trình cấp tài khoản theo nhóm vai trò nhanh hơn, và đưa kiểm tra tài khoản dùng chung vào rà soát định kỳ.
> 📘 PMP: Root cause analysis: vi phạm thường xuất phát từ quy trình khó dùng; sửa quy trình để tuân thủ dễ hơn vi phạm.
> 💡 Nhật: Tài khoản dùng chung làm mất khả năng truy vết trong 監査ログ (kansa rogu – log kiểm toán); với khách tài chính đây là lỗi nghiêm trọng, không phải tiểu tiết.

**Q592. Khách bảo hiểm B yêu cầu quản lý 特権ID (tokken ID – tài khoản đặc quyền như root, admin DB) chặt chẽ. Team hạ tầng hiện dùng root hằng ngày cho mọi thao tác. PM thiết kế cách làm thế nào?**
Em thiết kế: thao tác hằng ngày dùng tài khoản cá nhân quyền thường; 特権ID chỉ dùng khi cần, theo đơn xin có mục đích, thời gian, lệnh dự kiến, người duyệt; cấp tạm thời và thu hồi sau khi xong; mọi thao tác bằng 特権ID được ghi log (lệnh, thời gian, người) và người khác đối chiếu đơn với log sau đó. Mật khẩu 特権ID do khách hoặc công cụ quản lý giữ, không để người dùng biết cố định. Bằng chứng: sổ đơn xin, log thao tác, kết quả đối chiếu. Bẫy: duyệt đơn cho "cả tuần" khiến 特権 thành quyền thường.
> 📘 PMP: Plan Risk Responses (mitigate) cho rủi ro thao tác sai/lạm dụng quyền; kiểm soát bằng quy trình có bằng chứng.

**Q593. Member chuyển từ dự án ngân hàng A sang dự án khách khác đã 2 tháng nhưng vẫn còn trong nhóm có quyền đọc kho tài liệu của ngân hàng A. PM xử lý thế nào?**
① Em xác nhận quyền còn lại, có truy cập nào sau khi chuyển dự án không (kiểm log). ② Thu hồi ngay, báo bộ phận bảo mật; nếu log cho thấy có truy cập sau khi chuyển, điều tra mục đích và báo khách. ③ Rà toàn bộ người đã chuyển dự án. ④ Phòng ngừa: quy trình điều chuyển nhân sự (không chỉ nghỉ việc) phải kích hoạt thu hồi quyền; danh sách thành viên dự án và danh sách quyền đối chiếu hằng tháng.
> 📘 PMP: Control Resources: theo dõi việc phân bổ và giải phóng nguồn lực, bao gồm quyền truy cập.

**Q594. Khách phi nhân thọ C yêu cầu team VTI làm 棚卸し (tanaoroshi – kiểm kê) tài khoản hằng quý. Lần đầu làm, PM thấy 18 trong 95 tài khoản không xác định được ai đang dùng. PM xử lý thế nào?**
① Em xác nhận 18 tài khoản: tên, môi trường, quyền, lần đăng nhập cuối, ai đã xin cấp. ② Tạm khóa các tài khoản không xác định được chủ (không xóa ngay để giữ log), thông báo cho team; ai cần thì xin lại theo quy trình. ③ Báo khách kết quả kiểm kê trung thực kèm hành động. ④ Phòng ngừa: sổ quản lý tài khoản ghi chủ sở hữu, mục đích, ngày hết hạn cho mỗi tài khoản; tài khoản không có chủ sở hữu không được cấp.
> 📘 PMP: Monitor và audit định kỳ là một phần của kiểm soát; dữ liệu kiểm kê là work performance information.
> 💡 Nhật: Khách Nhật quen làm 棚卸し định kỳ cho mọi tài sản; vendor tự làm trước khi khách yêu cầu được đánh giá là "安心できる" (đáng tin cậy).

**Q595. Sự cố production đêm ở ngân hàng A, dev VTI cần quyền đọc DB production để điều tra gấp, nhưng thủ tục cấp quyền bình thường mất 2 ngày. PM xử lý thế nào?**
① Em xác nhận khách có quy trình khẩn cấp (break-glass) không: ai được duyệt trong đêm, cấp quyền gì, trong bao lâu. ② Đi đúng quy trình khẩn cấp: xin duyệt người có thẩm quyền của khách, cấp quyền đọc tối thiểu, có thời hạn, mọi thao tác ghi log, có người của khách giám sát nếu yêu cầu. ③ Sau sự cố, thu hồi quyền, nộp báo cáo thao tác đã thực hiện. ④ Nếu chưa có quy trình khẩn cấp, đề xuất khách xây dựng ngay sau sự cố; tuyệt đối không mượn tài khoản người khác.
> 📘 PMP: Contingency plan cho tình huống khẩn cấp phải được thiết lập trước; vẫn tuân thủ kiểm soát ở mức tối thiểu.

**Q596. Trong thư mục dự án khách bảo hiểm B có file Excel "account_list.xlsx" ghi user và mật khẩu của 40 tài khoản môi trường test, ai trong team cũng mở được. PM xử lý thế nào?**
① Em xác nhận file có những tài khoản nào, môi trường nào, có tài khoản production hay đặc quyền không, ai đã mở file (log). ② Xóa file, đổi mật khẩu toàn bộ tài khoản trong danh sách, ưu tiên tài khoản quyền cao. ③ Báo khách theo quy định bảo mật. ④ Thay bằng cách quản lý mật khẩu được phép (công cụ quản lý mật khẩu hoặc do khách cấp riêng từng người), mỗi người chỉ biết mật khẩu của mình; quy định cấm lưu mật khẩu dạng văn bản và đưa vào kiểm tra định kỳ.
> 📘 PMP: Identify Risks từ thói quen làm việc; mitigate bằng công cụ và quy định thay vì chỉ nhắc nhở.

**Q597. Sau release, khách phi nhân thọ C phát hiện 3 tài khoản test VTI tạo để kiểm tra trên production (動作確認 – xác nhận hoạt động) vẫn còn hoạt động và có quyền nhập hợp đồng. PM xử lý thế nào?**
① Em xác nhận 3 tài khoản đã được dùng sau thời gian xác nhận chưa, có dữ liệu test nào lẫn vào dữ liệu thật không. ② Vô hiệu hóa ngay theo thủ tục của khách, nếu có dữ liệu test lẫn vào thì phối hợp khách làm sạch. ③ Báo khách nguyên nhân và kết quả kiểm tra. ④ Phòng ngừa: thủ tục release phải có bước "tạo tài khoản xác nhận" và "xóa tài khoản xác nhận" với người kiểm, ghi vào checklist release; tài khoản xác nhận có quyền tối thiểu và hạn sử dụng.
> 📘 PMP: Close Phase checklist: dọn dẹp tạm thời (temporary access, test data) là một phần của hoàn tất giai đoạn.
> 💡 Nhật: Trên production của khách tài chính, dữ liệu test lẫn vào dữ liệu thật có thể ảnh hưởng báo cáo cho cơ quan quản lý; xử lý như sự cố, không như việc nhỏ.

**Q598. Bộ phận bảo mật của ngân hàng A yêu cầu danh sách người có quyền truy cập các môi trường kèm lý do và người duyệt, nộp trong 3 ngày. Thông tin hiện nằm rải rác ở email và chat. PM làm gì?**
① Em xác nhận format và phạm vi khách cần (môi trường, loại quyền, thời điểm). ② Tổng hợp từ hệ thống thực tế (danh sách tài khoản hiện có) chứ không chỉ từ email, đối chiếu với đơn xin để có lý do và người duyệt; tài khoản không có đơn thì đánh dấu và xử lý. ③ Nộp đúng hạn, nói rõ các điểm chưa đủ hồ sơ và kế hoạch bổ sung. ④ Từ nay dùng một sổ quản lý quyền duy nhất, cập nhật khi cấp/thu hồi, để lần sau xuất được trong vài giờ.
> 📘 PMP: Manage Project Knowledge: thông tin quản lý phải được lưu ở nơi thống nhất, truy xuất được.

**Q599. Vendor hạ tầng khác của khách bảo hiểm B và team VTI dùng chung một tài khoản admin trên server ứng dụng. Có một thay đổi cấu hình không ai nhận là mình làm, gây lỗi IT. PM xử lý thế nào?**
① Em xác nhận thay đổi qua log hệ thống (thời gian, nguồn kết nối) để tìm hiểu, không đổ lỗi khi chưa có bằng chứng. ② Khôi phục cấu hình theo thủ tục để IT tiếp tục. ③ Báo khách sự việc và đề xuất tách tài khoản cá nhân cho từng bên, quy định ai được thay đổi gì, qua đơn xin; khách là bên quyết định vì là chủ hệ thống. ④ Ghi vào 課題管理表 và theo dõi đến khi tách xong; trong thời gian chờ, mọi thao tác của VTI được ghi vào nhật ký thao tác để chứng minh khi cần.
> 📘 PMP: Manage Stakeholder Engagement giữa nhiều vendor; giải quyết bằng dữ liệu và qua chủ thể có thẩm quyền.

**Q600. Đêm 本番移行 của ngân hàng A cần 5 kỹ sư VTI thao tác song song với quyền admin, nhưng khách chỉ cấp 1 特権ID theo quy định. Lịch cutover chỉ có 8 giờ. PM xử lý thế nào?**
① Em xác nhận quy định của khách cho phép ngoại lệ không, và tính lại lịch nếu chỉ 1 người thao tác quyền admin. ② Đề xuất phương án tuân thủ: tách bước nào thật sự cần quyền admin và bước nào làm bằng quyền thường; xin khách cấp tạm nhiều 特権ID cá nhân chỉ trong đêm cutover với log và giám sát; hoặc một người thao tác admin, người khác chuẩn bị và kiểm tra. ③ Trình khách các phương án với ảnh hưởng thời gian, khách duyệt trước cutover nhiều ngày. ④ Diễn tập theo phương án đã duyệt để đo thời gian thật.
> 📘 PMP: Plan Schedule Management trong ràng buộc tuân thủ; phân tích phương án và để stakeholder có thẩm quyền quyết định trước.
> 💡 Nhật: Đừng đề cập vấn đề này lần đầu vào tuần cutover; khách Nhật cần thời gian 根回し (nemawashi – vận động trước) với bộ phận bảo mật để duyệt ngoại lệ.

## 5.9 Audit log, dữ liệu cá nhân, masking, audit bảo mật của khách

**Q601. Khi viết 基本設計書 cho hệ thống quản lý hợp đồng của khách bảo hiểm nhân thọ B, khách hỏi 監査ログ phải ghi những gì. PM đề xuất thế nào?**
Em đề xuất mỗi bản ghi tối thiểu trả lời: ai (ID người dùng, vai trò), khi nào (thời gian có múi giờ thống nhất), ở đâu (thiết bị, địa chỉ nguồn), làm gì (thao tác: xem, tạo, sửa, xóa, xuất file, đăng nhập/đăng xuất, đổi quyền), trên đối tượng nào (ID hợp đồng, ID khách hàng, không ghi nội dung nhạy cảm), kết quả (thành công/thất bại). Đặc biệt ghi các thao tác xem và xuất dữ liệu cá nhân, không chỉ thao tác ghi. Bằng chứng: bảng danh mục sự kiện được khách duyệt, test xác nhận từng sự kiện sinh log. Bẫy: ghi nội dung dữ liệu cá nhân vào chính audit log.
> 📘 PMP: Collect Requirements bao gồm yêu cầu phi chức năng (bảo mật, kiểm toán); ghi vào requirements traceability.
> 💡 Nhật: Khách bảo hiểm Nhật thường có quy định nội bộ riêng về log; hỏi tài liệu quy định đó trước khi thiết kế thay vì đề xuất từ đầu.

**Q602. Khách ngân hàng A yêu cầu 監査ログ phải giữ nhiều năm và "không ai sửa được, kể cả admin". Team đề xuất lưu vào bảng DB thường. PM xử lý thế nào?**
① Em xác nhận yêu cầu cụ thể: thời gian lưu, ai được đọc, yêu cầu chống sửa đổi (改ざん防止) ở mức nào, có quy định nội bộ hay chuẩn nào khách áp dụng. ② Chỉ ra bảng DB thường không đáp ứng vì admin DB sửa được; đề xuất phương án có thể kiểm chứng: lưu tách biệt với hệ thống ứng dụng, quyền ghi chỉ thêm, phân tách quyền quản trị log với quản trị hệ thống, có cơ chế phát hiện sửa đổi. ③ Trình phương án kèm chi phí, khách duyệt; ghi vào 方式設計書. ④ Đưa test chống sửa đổi vào ST.
> 📘 PMP: Phân tích yêu cầu phi chức năng và đánh giá phương án (alternatives analysis) trước khi chốt thiết kế.

**Q603. Tester phát hiện môi trường test của khách phi nhân thọ C đang dùng dữ liệu copy từ production, chưa được che, có tên, địa chỉ, số điện thoại người mua bảo hiểm. Team đã test trên đó 2 tuần. PM xử lý thế nào?**
① Em xác nhận ai đã copy, theo yêu cầu của ai, ai trong team đã truy cập, dữ liệu có bị xuất ra file hay エビデンス không. ② Dừng sử dụng môi trường đó, báo khách ngay vì đây là vấn đề quản lý dữ liệu cá nhân của khách, bất kể ai copy. ③ Phối hợp khách xử lý: xóa hoặc che dữ liệu, rà エビデンス và tài liệu đã tạo trong 2 tuần để xóa phần chứa dữ liệu thật. ④ Phòng ngừa: thống nhất bằng văn bản quy trình chuẩn bị test data, mọi dữ liệu từ production phải qua masking và được duyệt trước khi vào môi trường test.
> 📘 PMP: Escalate rủi ro tuân thủ ngay; PM không tự đánh giá "chưa sao" với dữ liệu cá nhân.
> 💡 Nhật: Dù khách là bên copy, vendor im lặng tiếp tục dùng sẽ bị coi là đồng trách nhiệm; báo ngay mới là cách bảo vệ cả hai bên.

**Q604. Sau khi masking dữ liệu test cho ngân hàng A bằng cách thay ngẫu nhiên số tài khoản, các bảng liên kết bị lệch, 40% case IT không chạy được. PM chọn phương án nào?**
① Em xác nhận cột nào dùng làm khóa liên kết giữa các bảng và giữa các hệ thống. ② Đổi kỹ thuật: thay thế nhất quán (cùng một giá trị gốc luôn ra cùng một giá trị che trên mọi bảng), giữ định dạng và chữ số kiểm tra nếu có; các cột chỉ hiển thị như tên, địa chỉ thì có thể thay bằng dữ liệu giả. ③ Trình khách quy tắc masking mới để duyệt, xác nhận kết quả không thể suy ngược dữ liệu thật. ④ Viết quy tắc masking thành tài liệu, có test kiểm tính toàn vẹn liên kết sau mỗi lần làm dữ liệu.
> 📘 PMP: Trade-off giữa yêu cầu bảo mật và yêu cầu kiểm thử; giải bằng phương án thỏa cả hai, có duyệt của khách.

**Q605. Review code phát hiện log ứng dụng của khách bảo hiểm B in ra tên, ngày sinh, số điện thoại người mua bảo hiểm khi có lỗi validate. Hệ thống đã chạy ở môi trường kiểm chứng 1 tháng. PM xử lý thế nào?**
① Em xác nhận phạm vi: những chỗ nào in dữ liệu cá nhân, log đã được lưu ở đâu, ai xem được, có bị chuyển ra ngoài không. ② Sửa code để chỉ ghi ID hoặc giá trị đã che; xử lý log đã sinh theo hướng dẫn của khách. ③ Báo khách sự việc, đặc biệt nếu môi trường có dữ liệu thật. ④ Phòng ngừa: quy tắc coding cấm ghi dữ liệu cá nhân vào log, hàm log chung tự che các trường nhạy cảm, đưa mục này vào checklist review code và quét tự động trong log test.
> 📘 PMP: Root cause analysis và biện pháp ở mức cơ chế (common function) thay vì chỉ sửa từng chỗ.

**Q606. Khách phi nhân thọ C thông báo sẽ audit bảo mật vendor sau 3 tuần: kiểm tra văn phòng, quy trình quản lý tài khoản, quản lý tài liệu, đào tạo. PM chuẩn bị thế nào?**
① Em xin danh mục kiểm tra hoặc phạm vi của khách để chuẩn bị đúng. ② Tự audit trước theo danh mục: kiểm thực tế văn phòng/ODC, đối chiếu danh sách tài khoản, sổ xin mang ra/mang vào, hồ sơ đào tạo, cam kết bảo mật; sửa các điểm chưa đạt trước ngày audit. ③ Chuẩn bị hồ sơ bằng chứng có tổ chức, chỉ định người trả lời từng mục, báo khách những điểm đang khắc phục thay vì che giấu. ④ Sau audit, lập kế hoạch khắc phục các phát hiện với hạn cụ thể.
> 📘 PMP: Quality audit (Manage Quality): chuẩn bị bằng tự đánh giá; phát hiện audit là đầu vào cải tiến.
> 💡 Nhật: Khách Nhật đánh giá cao khi vendor tự nói ra điểm yếu kèm kế hoạch sửa; bị phát hiện điều đã biết mà không nói thì mất điểm nặng.

**Q607. Audit bảo mật của ngân hàng A đưa ra 3 phát hiện: thiếu log ra vào phòng 1 tháng, 2 máy chưa cập nhật bản vá, đào tạo bảo mật của 4 member mới chưa có hồ sơ. Khách yêu cầu kế hoạch khắc phục trong 1 tuần. PM xử lý thế nào?**
① Em xác nhận từng phát hiện: nguyên nhân, phạm vi (chỉ 2 máy hay còn máy khác), rủi ro. ② Xử lý ngay những gì làm được: cập nhật bản vá, đào tạo và lưu hồ sơ cho 4 member. ③ Nộp kế hoạch khắc phục đúng hạn: mỗi phát hiện có nguyên nhân gốc, hành động ngay, biện pháp phòng ngừa, người phụ trách, hạn hoàn thành, bằng chứng sẽ nộp. ④ Mở rộng sang các dự án khác của công ty có cùng quy trình (横展開), báo khách kết quả khi hoàn tất.
> 📘 PMP: Corrective action và preventive action; theo dõi đến khi đóng với bằng chứng.

**Q608. Hệ thống của khách bảo hiểm nhân thọ B xử lý thông tin sức khỏe khi thẩm định hợp đồng. Khách nói đây là 要配慮個人情報 (thông tin cá nhân cần lưu ý đặc biệt), cần quản lý chặt hơn thông tin thường. PM điều chỉnh thế nào?**
① Em xác nhận với khách danh sách item thuộc nhóm này và quy định nội bộ của khách cho nhóm đó. ② Điều chỉnh trong thiết kế: giới hạn màn hình và vai trò được xem, ghi 監査ログ cho mọi lần xem, che khi hiển thị nếu không cần, không xuất ra file trừ khi được duyệt. ③ Điều chỉnh trong dự án: dữ liệu test tuyệt đối là dữ liệu giả, エビデンス không chứa item thật, giới hạn người trong team tiếp cận. ④ Đưa các yêu cầu này vào ma trận truy vết và 観点 test bảo mật.
> 📘 PMP: Tailoring kiểm soát theo mức nhạy cảm của dữ liệu; yêu cầu tuân thủ là một phần của phạm vi.
> 💡 Nhật: Ở mức nhận biết, luật bảo vệ thông tin cá nhân của Nhật có xếp riêng nhóm này; để khách (pháp chế) diễn giải quy định, vendor không tự diễn giải luật.

**Q609. Trong họp khởi động, khách ngân hàng A nói hệ thống "phải tuân thủ FISC". Team VTI không ai biết cụ thể FISC yêu cầu gì. PM làm gì?**
① Em xác nhận với khách: khách áp dụng FISC ở mức nào cho hệ thống này, khách có danh sách kiểm soát đã chuyển hóa thành yêu cầu cho vendor chưa. ② Đề nghị khách cung cấp danh sách yêu cầu cụ thể (thường do bộ phận rủi ro hệ thống của khách quản lý), vì vendor không tự diễn giải chuẩn. ③ Chuyển các yêu cầu đó thành yêu cầu phi chức năng có ID, truy vết vào thiết kế và test. ④ Cử người trong team tìm hiểu tổng quan chuẩn để trao đổi hiệu quả; ghi giả định và rủi ro nếu yêu cầu đến muộn.
> 📘 PMP: Collect Requirements và assumption log: biến yêu cầu chung chung thành yêu cầu cụ thể, đo được, có nguồn.

**Q610. Trong UAT, khách phi nhân thọ C dùng dữ liệu gần với thật. Team VTI hỗ trợ và chụp màn hình lỗi gửi về Việt Nam để điều tra, trong ảnh có tên và địa chỉ người mua bảo hiểm. PM xử lý thế nào?**
① Em xác nhận số ảnh, đã gửi qua kênh nào, lưu ở đâu, ai đã xem. ② Xóa các ảnh khỏi mọi nơi đã lưu theo hướng dẫn bảo mật, báo khách theo quy định. ③ Hướng dẫn lại cách báo lỗi UAT: che thông tin cá nhân trước khi chụp, hoặc chỉ gửi ID nội bộ và mô tả, ảnh có dữ liệu chỉ được lưu trong môi trường khách. ④ Đưa quy tắc này vào thủ tục hỗ trợ UAT và đào tạo team trước giai đoạn UAT của các dự án sau.
> 📘 PMP: Manage Communications: kênh và nội dung trao đổi phải tuân thủ yêu cầu bảo mật đã thống nhất.

**Q611. Khách bảo hiểm B hỏi: "làm sao chứng minh không ai trong team VTI xem dữ liệu khách hàng ngoài mục đích công việc?". PM trả lời và thiết kế thế nào?**
Em trả lời bằng cơ chế 3 lớp: phòng ngừa (phân quyền tối thiểu, chỉ vai trò cần mới xem được, dữ liệu test được che); phát hiện (監査ログ ghi mọi lần xem dữ liệu cá nhân, định kỳ người không thuộc team kiểm tra log theo mẫu bất thường như truy cập ngoài giờ, số lượng lớn, đối tượng không liên quan task); răn đe (cam kết bảo mật, đào tạo, xử lý vi phạm). Bằng chứng nộp khách: bảng phân quyền, báo cáo kiểm tra log định kỳ, hồ sơ đào tạo. Bẫy: có log nhưng không ai đọc; log không được kiểm tra thì không chứng minh được gì.
> 📘 PMP: Monitor Risks: kiểm soát phải có bằng chứng hoạt động thực tế, không chỉ trên giấy.
> 💡 Nhật: Khách Nhật sẽ hỏi "誰がいつ確認したか" (ai kiểm, khi nào); báo cáo kiểm log định kỳ có chữ ký trả lời đúng câu đó.

**Q612. Masking dữ liệu test của khách nhân thọ B đổi ngày sinh ngẫu nhiên, khiến tính phí theo tuổi cho kết quả khác production và 120 case ST không so sánh được với kết quả hệ cũ. PM xử lý thế nào?**
① Em xác nhận các item nào ảnh hưởng tới logic nghiệp vụ (ngày sinh, giới tính, ngày hiệu lực hợp đồng) và các item chỉ để hiển thị. ② Đề xuất quy tắc masking phân biệt: item ảnh hưởng tính toán được giữ đặc tính cần thiết (ví dụ giữ tuổi hoặc dịch ngày trong phạm vi không đổi tuổi), item định danh được thay hoàn toàn; xem lại rủi ro suy ngược khi giữ đặc tính. ③ Trình khách quy tắc để bộ phận bảo mật duyệt. ④ Làm lại dữ liệu và chạy lại 120 case; ghi quy tắc vào tài liệu chuẩn bị test data.
> 📘 PMP: Phân tích trade-off giữa yêu cầu bảo mật và tính hợp lệ của test; quyết định có sự tham gia của stakeholder bảo mật.

**Q613. 監査ログ của ngân hàng A tăng nhanh, chi phí lưu trữ vượt dự toán. Phía vận hành đề xuất giảm thời gian lưu và bỏ log thao tác xem màn hình. Bộ phận bảo mật của khách phản đối. PM xử lý thế nào?**
① Em xác nhận số liệu: dung lượng theo loại sự kiện, tốc độ tăng, chi phí, yêu cầu lưu giữ theo quy định nội bộ của khách. ② Đưa ra phương án không vi phạm yêu cầu: nén, chuyển log cũ sang kho lưu trữ chi phí thấp, loại bỏ trường dư thừa, gộp sự kiện trùng; tính chi phí từng phương án. ③ Tổ chức họp có cả vận hành và bảo mật của khách, trình phương án và ảnh hưởng; khách quyết định, không để vendor đứng về một phía. ④ Ghi quyết định, cập nhật 運用設計書 và dự báo dung lượng.
> 📘 PMP: Manage Stakeholder Engagement khi stakeholder có mục tiêu xung đột; dùng phân tích phương án để đạt đồng thuận.
> 💡 Nhật: Đề xuất bỏ log xem dữ liệu cá nhân gần như chắc chắn bị bảo mật bác; bắt đầu bằng phương án kỹ thuật giảm chi phí sẽ thuận lợi hơn.

## 5.10 Câu khó: vi phạm bảo mật, mất niềm tin, áp lực bỏ bước, member sai quy định

**Q614. Hệ thống DLP báo một member dự án khách bảo hiểm nhân thọ B gửi file Excel test data từ email công ty sang email cá nhân để "làm thêm ở nhà". File có 2.000 dòng, chưa rõ đã được masking chưa. PM xử lý thế nào?**
① Em xác nhận ngay: nội dung file (dữ liệu thật hay đã che), thời điểm gửi, file đã được mở/chuyển tiếp chưa; nói chuyện với member, không kết luận vội. ② Báo bộ phận bảo mật nội bộ trong ngày, yêu cầu member xóa file khỏi email cá nhân và thiết bị dưới sự xác nhận của bảo mật. ③ Nếu dữ liệu là của khách, báo khách theo hợp đồng và quy trình sự cố, dù dữ liệu đã che; trình bày fact, phạm vi, biện pháp. ④ Gốc rễ: áp lực công việc khiến member làm thêm ngoài giờ; xem lại khối lượng, đào tạo lại toàn team, xử lý kỷ luật theo quy định.
> 📘 PMP: Ethics và stewardship: minh bạch với stakeholder về sự cố; xử lý cả cá nhân và nguyên nhân hệ thống.
> 💡 Nhật: Báo cáo đầu tiên (第一報) nên gửi sớm dù chưa đủ thông tin, ghi rõ "đang điều tra"; khách Nhật xem trọng tốc độ báo hơn sự hoàn chỉnh.

**Q615. Trong báo cáo định kỳ gửi khách ngân hàng A, tên ngân hàng bị viết sai 1 chữ Hán. Trưởng phòng khách nói "tên công ty còn sai thì thiết kế tin sao được" và yêu cầu review lại toàn bộ 15 tài liệu đã nộp. PM xử lý thế nào?**
① Em xác nhận lỗi, xin lỗi trực tiếp và nghiêm túc, không giảm nhẹ là "chỉ 1 chữ". ② Chấp nhận yêu cầu rà soát, nhưng làm có phương pháp: kiểm tên riêng, thuật ngữ, số liệu trong 15 tài liệu bằng tool và người, báo cáo kết quả bằng số lỗi tìm thấy và đã sửa. ③ Báo khách kế hoạch rà soát và thời hạn; báo lãnh đạo VTI vì ảnh hưởng niềm tin. ④ Phòng ngừa: danh sách tên riêng chuẩn (tên công ty, bộ phận, người, sản phẩm) đưa vào kiểm tra tự động; tài liệu gửi lãnh đạo khách có thêm một lớp kiểm của BrSE.
> 📘 PMP: Manage Stakeholder Engagement: khôi phục niềm tin bằng hành động có bằng chứng, không bằng lời giải thích.
> 💡 Nhật: Sai tên công ty khách là một trong những lỗi bị coi là thất lễ nhất; xin lỗi trực tiếp (bằng lời, qua cấp phù hợp) trước khi gửi bản sửa.

**Q616. Còn 2 ngày tới hạn nộp 詳細設計書 cho khách phi nhân thọ C. Lãnh đạo VTI bảo PM bỏ bước cross-check để kịp hạn, "khách cũng sẽ review mà". PM xử lý thế nào?**
① Em xác nhận khối lượng còn lại và thời gian cross-check thực sự cần, tìm phần nào có rủi ro cao nhất. ② Đề xuất phương án thay thế: cross-check tập trung vào phần rủi ro cao (logic nghiệp vụ, phần mới), tăng người kiểm song song, tool kiểm tự động cho phần format. ③ Nếu vẫn không đủ, trình lãnh đạo và khách lựa chọn: nộp đúng hạn phần đã kiểm đủ và phần còn lại trễ 1–2 ngày, ghi rõ trạng thái; không nộp tài liệu chưa kiểm như tài liệu đã kiểm. ④ Giải thích với lãnh đạo chi phí khi khách tìm ra lỗi lớn hơn chi phí trễ ngắn.
> 📘 PMP: Cost of quality: chi phí sai hỏng bên ngoài (external failure) cao hơn chi phí phòng ngừa; quyết định trade-off phải minh bạch.
> 💡 Nhật: Với khách Nhật, "trễ có báo trước + chất lượng ổn" thường được chấp nhận hơn "đúng hạn + nhiều chỉ trích"; nhưng phải báo trước hạn, không báo vào ngày hạn.

**Q617. Một member ở ODC khách ngân hàng A lại mang điện thoại vào phòng lần thứ 2 trong 1 tháng, dù đã được nhắc nhở lần đầu. Member này đang là người chủ chốt của module thanh toán. PM xử lý thế nào?**
① Em xác nhận sự việc qua camera/biên bản, kiểm điện thoại có dùng để chụp hay ghi gì không. ② Xử lý theo quy định đã công bố, không ngoại lệ vì vai trò chủ chốt; báo bộ phận bảo mật và lãnh đạo; báo khách nếu cam kết với khách yêu cầu. ③ Tìm nguyên nhân: thói quen, lý do cá nhân (cần liên lạc gia đình), hay quy trình gửi đồ bất tiện; giải quyết nguyên nhân hợp lý (ví dụ số điện thoại cố định trong phòng). ④ Giảm rủi ro phụ thuộc một người bằng chia sẻ kiến thức module, phòng khi phải điều chuyển member.
> 📘 PMP: Manage Team: xử lý vi phạm công bằng và nhất quán; đồng thời quản lý rủi ro nguồn lực chủ chốt.

**Q618. Khách bảo hiểm B gửi email chính thức: "弊社として御社の品質意識に懸念がある" (chúng tôi lo ngại về ý thức chất lượng của quý công ty) sau nhiều chỉ trích nhỏ về chính tả, format. Khách yêu cầu kế hoạch cải thiện. PM xử lý thế nào?**
① Em xác nhận dữ liệu: tổng hợp chỉ trích theo loại, tài liệu, team, thời gian để hiểu vấn đề thật nằm ở đâu. ② Đề xuất gặp trực tiếp khách cùng lãnh đạo VTI để nhận trách nhiệm và lắng nghe kỳ vọng. ③ Nộp kế hoạch cải thiện cụ thể: nguyên nhân gốc, biện pháp (checklist, tool, quality gate, người kiểm độc lập), mốc thời gian, cách khách theo dõi kết quả trong các lần nộp tiếp theo. ④ Thực hiện và báo cáo kết quả định kỳ cho đến khi khách xác nhận đã yên tâm; không coi email trả lời là xong việc.
> 📘 PMP: Manage Stakeholder Engagement và Manage Quality: hành động khắc phục có kế hoạch, đo được, có theo dõi.
> 💡 Nhật: Email chính thức có câu "懸念" là tín hiệu nghiêm trọng, có thể ảnh hưởng hợp đồng tiếp theo; lãnh đạo VTI nên tham gia ngay, không để PM xử lý một mình.

**Q619. Một member báo mất laptop công ty trên taxi. Laptop có tài liệu thiết kế của khách phi nhân thọ C (không có dữ liệu cá nhân), ổ đĩa đã mã hóa nhưng member không chắc đã khóa màn hình. PM xử lý thế nào?**
① Em xác nhận ngay: thời điểm mất, tài liệu gì có trên máy, tình trạng mã hóa và khóa, máy đang đăng nhập những tài khoản nào. ② Hành động trong vài giờ: báo bộ phận IT/bảo mật để khóa máy từ xa nếu có thể, vô hiệu hóa phiên đăng nhập và đổi mật khẩu các tài khoản liên quan, liên lạc hãng taxi. ③ Báo khách sớm theo quy định với thông tin đã có, cập nhật khi có thêm. ④ Gốc rễ: tài liệu khách không nên nằm trên laptop mang ra ngoài; rà lại quy định lưu trữ và kiểm tra máy của toàn team.
> 📘 PMP: Implement Risk Responses theo kế hoạch ứng phó sự cố; thông tin cho stakeholder kịp thời và trung thực.

**Q620. PM phát hiện một dev đã đẩy một phần source của hệ thống ngân hàng A lên repository công khai cá nhân từ 3 tuần trước, trong đó có file cấu hình với chuỗi kết nối DB môi trường kiểm chứng. PM làm gì trước tiên?**
① Em xác nhận phạm vi: những file nào, có thông tin xác thực nào, repository đã bị người khác sao chép chưa (nếu xem được). ② Ngay lập tức: yêu cầu gỡ repository, báo bộ phận bảo mật; coi mọi thông tin xác thực trong đó là đã lộ, phối hợp khách đổi ngay. ③ Báo khách trong ngày theo quy trình sự cố, vì source là tài sản của khách và đã công khai 3 tuần. ④ Gốc rễ: quyền push ra ngoài không bị chặn, thông tin xác thực nằm trong source; chặn kỹ thuật, quét secret trước commit, đưa cấu hình nhạy cảm ra kho bí mật, xử lý member theo quy định.
> 📘 PMP: Issue escalation ngay với rủi ro đã xảy ra; corrective action kết hợp preventive action ở mức hệ thống.
> 💡 Nhật: Khách Nhật sẽ yêu cầu 再発防止策 (biện pháp chống tái diễn) ở mức tổ chức, không chấp nhận chỉ "đã nhắc nhở cá nhân".

**Q621. Khách bảo hiểm B yêu cầu nộp エビデンス cho 500 case ST trong 1 ngày để kịp họp lãnh đạo. Team mới có エビデンス đủ chuẩn cho 380 case. Một leader đề xuất "chụp nhanh lại 120 case cho đủ". PM xử lý thế nào?**
① Em xác nhận 120 case: đã chạy nhưng thiếu ảnh, hay chưa chạy. ② Nếu chạy lại trong ngày được thì chạy thật và chụp với thời gian thật; tuyệt đối không tạo ảnh không phản ánh lần chạy thật hay ghi ngày sai. ③ Báo khách trung thực ngay hôm nay: 380 case đủ bằng chứng, số case chạy lại trong ngày, phần còn lại và thời hạn; đề xuất khách dùng số thật cho họp lãnh đạo. ④ Gốc rễ là quy trình lấy エビデンス chậm so với chạy test; sửa quy trình và nói rõ với leader ranh giới giữa bổ sung đúng cách và làm giả.
> 📘 PMP: PMI Code of Ethics (honesty): không trình bày sai trạng thái dù bị áp lực thời gian.

**Q622. Một sự cố nhỏ: tài liệu có tên 3 người mua bảo hiểm bị gửi nhầm giữa hai bộ phận nội bộ của khách nhân thọ B, do lỗi chức năng xuất file VTI làm. Trưởng phòng IT bên khách đề nghị VTI "sửa lặng lẽ, không cần báo bộ phận compliance". PM xử lý thế nào?**
① Em xác nhận fact: lỗi chức năng nào, bao nhiêu dữ liệu, ai đã nhận, đã được xử lý chưa. ② Sửa lỗi theo quy trình thay đổi bình thường, kiểm tra các chức năng xuất file tương tự. ③ Không tự liên hệ compliance của khách vượt mặt đầu mối, nhưng trình bày rõ với trưởng phòng IT bằng văn bản: fact, khuyến nghị báo theo quy trình của khách, và rủi ro nếu không báo; nếu vẫn bị yêu cầu che giấu, báo lãnh đạo VTI để xử lý ở cấp hợp đồng. ④ Lưu hồ sơ đầy đủ, báo cáo sự cố nội bộ VTI.
> 📘 PMP: Ethics: không tham gia che giấu thông tin; escalate theo cấp bậc phù hợp, có hồ sơ bằng văn bản.
> 💡 Nhật: Đây là tình huống xám điển hình; giữ quan hệ với đầu mối nhưng để quyết định "báo hay không" thuộc về quy trình của khách, và vendor có bằng chứng đã khuyến nghị.

**Q623. Để tiết kiệm thời gian xin tài khoản, người phụ trách bên ngân hàng A đưa cho team VTI tài khoản và mật khẩu của chính họ để vào hệ thống kiểm chứng "trong 1 tuần thôi". PM xử lý thế nào?**
① Em xác nhận hệ thống đó có dữ liệu gì và quy định của khách về dùng tài khoản. ② Từ chối lịch sự nhưng rõ ràng: dùng tài khoản người khác làm 監査ログ ghi sai người thao tác, có thể khiến chính người phụ trách bị quy trách nhiệm. ③ Đề xuất cách thay thế: hỗ trợ khách điền đơn xin tài khoản ngay hôm nay, xin cấp nhanh với lý do cụ thể, trong lúc chờ thì làm phần việc không cần hệ thống; báo ảnh hưởng tiến độ nếu có. ④ Ghi việc này vào 課題管理表 để quy trình cấp tài khoản được cải thiện cho các lần sau.
> 📘 PMP: Bảo vệ stakeholder khỏi rủi ro họ chưa thấy là một phần của Manage Stakeholder Engagement; tuân thủ không ngoại lệ vì thuận tiện.

**Q624. Trưởng nhóm mới bên khách phi nhân thọ C review rất khắt khe: 120 chỉ trích cho tài liệu 50 trang, phần lớn về cách diễn đạt và dấu câu. Team mệt mỏi, có member nói "khách cố tình làm khó". PM xử lý thế nào?**
① Em phân loại 120 chỉ trích: lỗi thật, sở thích diễn đạt, chỉ trích mâu thuẫn với tiêu chuẩn đã thống nhất trước đó. ② Sửa ngay lỗi thật; với chỉ trích về sở thích, gặp trưởng nhóm khách để hiểu kỳ vọng và đề xuất cập nhật tiêu chuẩn tài liệu (văn phong, dấu câu) bằng văn bản để áp dụng thống nhất từ nay. ③ Nếu tiêu chuẩn mới làm tăng công đáng kể, báo khách và xử lý như thay đổi. ④ Với team: chia sẻ cách nhìn rằng đây là kỳ vọng chất lượng của khách, chuyển chỉ trích thành checklist để giảm làm lại, ghi nhận tiến bộ để giữ tinh thần.
> 📘 PMP: Manage Stakeholder Engagement với stakeholder mới; biến kỳ vọng ngầm thành tiêu chuẩn chất lượng rõ ràng.
> 💡 Nhật: Người mới phụ trách bên khách Nhật thường muốn thể hiện sự chặt chẽ; hiểu và đáp ứng kỳ vọng sớm thường biến họ thành người ủng hộ.

**Q625. Hai tháng sau 検収 dự án 請負 với khách bảo hiểm B, bộ phận vận hành của khách phát hiện 運用手順書 có 6 chỗ sai khiến một batch phải chạy lại thủ công. Khách hỏi VTI xử lý thế nào và ai chịu chi phí. PM xử lý thế nào?**
① Em xác nhận 6 chỗ sai: là lỗi của tài liệu đã nghiệm thu hay do hệ thống/quy trình thay đổi sau đó. ② Sửa ngay các lỗi thuộc trách nhiệm VTI, gửi bản sửa có đánh dấu, hỗ trợ khách xử lý ảnh hưởng. ③ Về chi phí: không tự hứa hay từ chối; báo lãnh đạo và bộ phận hợp đồng VTI để đối chiếu với điều khoản về trách nhiệm khi deliverable không phù hợp hợp đồng (契約不適合責任 – trách nhiệm không phù hợp hợp đồng) và thời hạn đã thỏa thuận, rồi trả lời khách chính thức. ④ Rà toàn bộ tài liệu vận hành đã nộp để tìm lỗi tương tự, ghi lessons learned về diễn tập 手順書.
> 📘 PMP: Control Procurements / quản lý hợp đồng: xử lý khiếu nại theo điều khoản hợp đồng, đồng thời duy trì quan hệ bằng hành động khắc phục nhanh.
> 💡 Nhật: Sửa lỗi trước, bàn chi phí sau; khách Nhật đánh giá vendor qua thái độ xử lý sau nghiệm thu, điều này ảnh hưởng trực tiếp tới dự án tiếp theo.
