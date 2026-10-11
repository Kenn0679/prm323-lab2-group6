# Persona và vấn đề

> Đề tài: **TeamUp EXE** (tên tạm) - ứng dụng giúp **mentor/giảng viên EXE** ghép sinh viên FPT chưa có nhóm vào các nhóm đang thiếu 1-2 thành viên chuyên môn, để mỗi nhóm khởi nghiệp nhỏ đạt 4-6 người thuộc nhiều ngành. AI đề xuất, mentor duyệt.

## Persona chính: Cô Lan

| Mục | Nội dung |
|---|---|
| Tên / tuổi | Lan, 38 tuổi |
| Vai trò | Giảng viên và mentor khởi nghiệp, phụ trách 3 lớp EXE (khoảng 40 sinh viên mỗi lớp, nhiều ngành: SE, AI, MKT, GD) |
| Bối cảnh hằng ngày | Dạy xen kẽ nhiều lớp, có vài phút giữa các tiết và lúc di chuyển. Là người chịu trách nhiệm cuối cùng về nhóm của lớp. |
| Mục tiêu | Mỗi nhóm có 4-6 người, đủ ngành cần cho một dự án khởi nghiệp nhỏ, không còn sinh viên "lẻ" khi chốt nhóm. |
| Pain points | (1) Mỗi lớp còn nhiều bạn chưa có nhóm, và một số nhóm thiếu 1-2 người đúng chuyên môn (ví dụ thiếu Design hoặc AI). (2) Ghép tay bằng Excel và tin nhắn, khó nhớ ai ngành nào, kỹ năng gì, rảnh bao nhiêu giờ. (3) Ghép vội thì nhóm lệch ngành, vấn đề chỉ lộ ra giữa kỳ. (4) Chỉ có vài phút mỗi lần, cần quyết định nhanh nhưng vẫn muốn hiểu lý do. |
| Thiết bị | Điện thoại Android, thường dùng một tay; wifi trường đôi lúc chập chờn. |
| Nhu cầu accessibility | Đọc ngoài hành lang sáng nên cần tương phản cao; chữ thân bài 16 sp, nút 48 dp. |

## Vấn đề (1 câu)

Mentor có sinh viên chưa có nhóm và nhóm còn thiếu chuyên môn, nhưng phải ghép thủ công qua bảng tính nên mất nhiều thời gian và dễ ghép lệch ngành.

## Giải pháp ở mức sản phẩm

AI gợi ý sinh viên nào nên vào nhóm nào dựa trên ngành, kỹ năng và lịch rảnh. Mỗi gợi ý có nhãn mức phù hợp và lý do ngắn. Mentor xem, thêm hoặc bớt thành viên, rồi mới duyệt. Chưa duyệt thì sinh viên không bị thay đổi gì.

## Tiêu chí thành công (đo được)

- Mentor **duyệt xong gợi ý AI cho một lớp trong dưới 5 phút** (từ mở lớp đến duyệt nhóm cuối).
- **Mọi nhóm sau khi duyệt có 4-6 người và ít nhất 3 ngành khác nhau.**
- Từ danh sách đề xuất, mentor **thêm hoặc đổi một thành viên và duyệt trong dưới 60 giây**.

## Giả định cần xác nhận

- Persona là giả định của nhóm. Nên hỏi nhanh 1-2 giảng viên hoặc mentor EXE để kiểm chứng pain points và ghi kết quả vào đây trước khi nộp.
- AI trong lab chỉ là thiết kế giao diện với dữ liệu mẫu, không có mô hình thật. Ghi rõ điều này trong `ai/ai-design-log.md`.
- Việc xác minh sinh viên là sinh viên FPT nằm ngoài phạm vi lab.
