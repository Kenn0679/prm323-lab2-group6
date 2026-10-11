# Screen spec (ý định thiết kế)

Mỗi màn: mục đích, nội dung, flow sử dụng. Số S trùng `ux/user-flow.md` và tên frame trong Figma.

| Màn | Tên | Flow | Mục đích | Nội dung |
|---|---|---|---|---|
| S1 | Sign in | A | Mentor vào app chỉ bằng email (không có bước mã). | Tiêu đề "Sign in", dòng "Build balanced teams", ô Email (placeholder you@gmail.com), nút Continue. |
| S2 | My classes | A | Chọn lớp cần ghép nhóm. | 3 thẻ lớp (Class A/B/C): số sinh viên và 2 dòng trạng thái (số SV chưa có nhóm, số nhóm thiếu người hoặc 'All matched'). |
| S3 | Class detail | A, C | Xem tình hình lớp và bắt đầu ghép bằng AI. | Ba số (students, without team, need members), hai hàng điều hướng (Students without team, Teams needing members), nút Match with AI. |
| S4 | No team | A | Xem sinh viên chưa có nhóm. | Chip lọc ngành (All, SE, AI, MKT, GD), 5 hàng sinh viên (avatar chữ cái, tên, ngành và kỳ), nút Match with AI. |
| S5 | Need members | C | Xem nhóm đang thiếu ngành. | 3 thẻ nhóm (Tutor Match, GreenLoop, FinLite): hàng ngành 5 ô 40dp và dòng 'Needs ...'; nút Match with AI. |
| S6 | Profile | (tab) | Xem thông tin mentor và đăng xuất. | Avatar chữ LN, tên Lan Nguyen, 'Mentor, 3 classes', hàng Notifications (switch), hàng Language, nút Sign out. |
| S7 | Student detail | B | Xem hồ sơ sinh viên trước khi thêm vào nhóm. | Avatar, tên, 'MKT, S5', chip 'No team', Skills (3 chip), Availability (12 h/week), nút Add to team. |
| S8 | AI matching | A, C | Chờ AI ghép. | Vòng tiến trình, 'Finding teammates', 'Class A, 12 students', nút Cancel. |
| S9 | Proposals | A, B | Xem các nhóm AI đề xuất. | 3 thẻ đề xuất: tên nhóm, hàng ngành (ô đầy + ô đề xuất có dấu +), chip 'Strong fit' hoặc 'Good fit'. Tab Proposals có badge '3'. |
| S10 | Proposal detail | A, B, C | Xem lý do và quyết định duyệt hay bỏ. | Hàng ngành 48dp, chip fit, mục Why (2 dòng), New member (Minh Anh, GD + Add member), Members (4 hàng), nút Approve và Discard. |
| S11 | Add member | B | Chọn sinh viên thêm vào nhóm. | 'Tutor Match, 5 of 6', chip lọc ngành, 4 hàng có checkbox, nút Add. |
| S12 | Approve dialog | A, B, C | Xác nhận duyệt nhóm. | 'Approve team?', 'Students will be notified.', Cancel, Approve. |
| S13 | Add member - Error | B | Báo vượt 6 người. | Như S11 với 'Tutor Match, 6 of 6', 2 hàng được chọn, dòng lỗi 'Max 6 members' kèm biểu tượng, nút Add bị khóa. |
| S14 | Proposals - All matched | A, B, C | Báo đã ghép xong. | Biểu tượng check, 'All matched', nút View teams, snackbar 'Approved' + Undo. |
| S15 | No match | C | Báo AI không tìm được sinh viên phù hợp. | Biểu tượng cảnh báo, 'No Design student found', nút Add manually, nút See teams. |
| S16 | Add student | C | Ghép tay. | Ô tìm kiếm, chip lọc, 3 hàng chọn được, 1 hàng 'Khoa Tran' bị khóa với chip 'In a team', nút Add. |
| S17 | Discard dialog | C | Xác nhận bỏ đề xuất. | 'Discard proposal?', 'AI will not suggest it again.', Cancel, Discard (đỏ). |
| S18 | Offline | A | Báo mất mạng khi AI chạy. | Biểu tượng offline, "You're offline", nút Try again. |
| S19 | Sign in - error | A | Báo email sai. | Như S1 nhưng ô Email có chữ `lan@gmail`, viền đỏ 2dp, biểu tượng lỗi, dòng "Enter a valid email" kèm biểu tượng, nút Continue. |
| S20 | Proposal detail - hand-built | C | Duyệt nhóm do mentor tự ghép. | FinLite, hàng ngành 5 ô đầy 48dp, chip "Added by you", New member (Lan Vo, AI + nút Change), Members (4 hàng), nút Approve, chữ Discard (đỏ). |
| S21 | Add student - no results | C | Báo tìm không ra sinh viên. | Ô tìm "Zed" có nút xóa, chip lọc ngành, biểu tượng search-off, "No student found", nút Clear search. |

## Trạng thái cần có theo màn

| Màn | Trạng thái |
|---|---|
| S1 Sign in | default; error (email sai); loading (nút đang gửi). |
| S2 My classes | populated; loading (skeleton thẻ); empty (chưa có lớp); error (offline). |
| S3 Class detail | populated; loading; error. |
| S4 No team | populated; loading; empty (không còn SV: chuyển S14); error. |
| S5 Need members | populated; loading; empty. |
| S6 Profile | populated. |
| S7 Student detail | populated; loading. |
| S8 AI matching | loading (màn này là loading); error (mất mạng: S18). |
| S9 Proposals | populated; empty (S14); loading. |
| S10 Proposal detail | populated; loading; error. |
| S11 Add member | populated; error (S13: vượt 6). |
| S12 Approve dialog | default. |
| S13 Add member - Error | error. |
| S14 Proposals - All matched | empty; snackbar 5 giây. |
| S15 No match | empty. |
| S16 Add student | populated; empty (không có kết quả); error (hàng đã có nhóm bị khóa). |
| S17 Discard dialog | default. |
| S18 Offline | error. |
| S19 Sign in - error | error. |
| S20 Proposal detail - hand-built | populated; loading; error. |
| S21 Add student - no results | empty (không có kết quả). |

## Ghi chú

- Sinh viên không có giao diện riêng, chỉ là dữ liệu.
- AI trong lab là thiết kế giao diện với dữ liệu mẫu, không có mô hình thật.
- Mọi chữ trên màn lấy đúng theo prompt trong `ai/ai-design-log.md`.
- Ngoại lệ: Stitch thêm vài dòng chữ ngoài prompt. Đã xóa trong Figma (11/10/2026) những dòng có số liệu hoặc không có trong dữ liệu mẫu: S5 dòng "Active search lists, 3 teams seeking", "x / 5 filled", "n slots open" và ô ghi chú cuối trang; S18 thẻ "Signal lost". Giữ lại các câu mô tả ngắn: S3 thẻ "Automated grouping" kèm một câu giải thích; S14 và S15 một câu mô tả dưới tiêu đề (không chứa số liệu, nhóm chấp nhận).
