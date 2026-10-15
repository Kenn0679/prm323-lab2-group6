# PRM323 Lab 2 \- Nguồn nội dung để tạo slide thuyết trình

Dùng cho công cụ ppt\-master (hugohe3/ppt\-master). Đặt file này vào projects/prm323/sources/ cùng các ảnh liệt kê ở mục 3, rồi dán câu lệnh ở mục 1 vào chat của công cụ AI.

# 1. Câu lệnh để dán vào chat

Create a 12\-slide presentation from projects/prm323/sources/slide\-source.docx. Follow the slide structure and content exactly as written in section 4 (one slide per heading, in order). Language of slide text: Vietnamese (keep app UI strings and file names in English). Style: clean and professional, white background, burnt orange \#B23E00 as the only accent colour, dark text \#1C1B18, no blue, no gradients, no stock illustrations. Maximum 6 short lines per slide; put detail in the speaker notes. Use only the facts in this document. If a value is marked TODO, leave a visible placeholder "\[TODO: ...\]" instead of inventing it. Use the image files in sources/ where section 4 names them; where an image is missing, leave an empty labelled placeholder. Do not use illustrative mockups as evidence. No need for 5\-minute demo slides; the demo is done live in Figma.

# 2. Thông tin chung (điền trước khi chạy)

| Mục | Giá trị |
| --- | --- |
| Tên ứng dụng | TeamUp EXE (mentor app) |
| Thành viên và MSSV | [TODO: điền tên và MSSV từng người] |
| Link GitHub | https://github.com/Kenn0679/prm323-lab2-group6 |
| Link Figma | https://www.figma.com/design/X5WcaK4s20AYF53cvRdouV/TeamUp-EXE---Mentor--PRM323-Lab-2-?node-id=2-6&t=VPIFaeqdEmKBzDex-1 (ai có link cũng xem được) |
| Giảng viên | [TODO] |
| Bài làm nhóm | Đã được giảng viên xác nhận [TODO: ngày xác nhận] |

# 3. Ảnh cần bỏ vào sources/ trước khi chạy

| Ảnh | Lấy ở đâu | Dùng cho |
| --- | --- | --- |
| flow-a.png, flow-b.png, flow-c.png | Có sẵn trong repo, thư mục assets/flows/ | Slide 04 |
| Ảnh Stitch lần đầu (R0, bản sinh viên) và 21 frame R9 và R10 (bản mentor) | Bạn lưu từ Stitch vào assets/stitch/ [TODO] | Slide 05 |
| Ảnh trước và sau của 3 iteration | assets/stitch/ và Figma version history [TODO] | Slide 06 |
| Ảnh wireframe, 25 màn final, các state | `assets/figma/02-wireframe/`, `03-final-ui/` (đã xuất) | Slide 08 |
| Ảnh Page 04 Design System và Page 05 Components | Xuất từ Figma [TODO] | Slide 09 |
| Ảnh prototype (3 flow, dialog overlay, loading) | Xuất hoặc chụp màn hình Figma Page 06 [TODO] | Slide 11 |

Lưu ý: không có ảnh thì để ô trống có nhãn. Tuyệt đối không dùng ảnh minh họa tự vẽ làm bằng chứng.

# 4. Nội dung từng slide

## Slide 01. Tổng quan dự án

- TeamUp EXE: ứng dụng di động cho mentor/giảng viên môn EXE
- AI gợi ý ghép sinh viên chưa có nhóm vào nhóm đang thiếu 1\-2 thành viên chuyên môn; mentor duyệt
- Đối tượng: mentor và giảng viên EXE (Cô Lan, 3 lớp, nhiều ngành SE, AI, MKT, GD)
- Người trình bày: Group 6
- Figma: https://www.figma.com/design/X5WcaK4s20AYF53cvRdouV/TeamUp-EXE---Mentor--PRM323-Lab-2-?node-id=2-6&t=VPIFaeqdEmKBzDex-1; GitHub: https://github.com/Kenn0679/prm323-lab2-group6

__Ghi chú trình bày: __Nêu ngay vấn đề thực tế: lớp có sinh viên chưa có nhóm, nhóm thiếu chuyên môn, ghép tay bằng Excel mất thời gian.

__Bằng chứng: __Link GitHub và Figma (README.md).

## Slide 02. Vấn đề và Persona

- Persona: Cô Lan, 38 tuổi, giảng viên và mentor phụ trách 3 lớp EXE, khoảng 40 sinh viên mỗi lớp
- Pain points: nhiều bạn chưa có nhóm; ghép tay bằng Excel và tin nhắn khó nhớ ngành, kỹ năng, lịch rảnh; ghép vội thì nhóm lệch ngành, chỉ lộ ra giữa kỳ; chỉ có vài phút mỗi lần
- Một câu vấn đề: mentor có sinh viên chưa có nhóm và nhóm còn thiếu chuyên môn, nhưng phải ghép thủ công nên mất thời gian và dễ lệch ngành
- Tiêu chí thành công: (1) duyệt xong gợi ý AI cho một lớp dưới 5 phút; (2) mọi nhóm sau duyệt có 4\-6 người và ít nhất 3 ngành; (3) thêm hoặc đổi một thành viên rồi duyệt dưới 60 giây
- Lưu ý: persona là giả định của nhóm (giả định của nhóm, chưa kiểm chứng với người dùng thật)

__Ghi chú trình bày: __Nhấn mạnh thiết bị: một tay, vài phút giữa các tiết, wifi trường chập chờn.

__Bằng chứng: __ux/persona.md

## Slide 03. Information Architecture

- 25 màn hình S1\-S25; thanh điều hướng 3 tab: Classes, Proposals, Profile
- Classes (S2) → Class detail (S3) → No team (S4), Need members (S5), Student detail (S7)
- Proposals (S9) → Proposal detail (S10) → Add member (S11) → Approve dialog (S12) / Discard dialog (S17)
- Mỗi màn thuộc ít nhất một flow (S6 Profile là tab gốc)

__Ghi chú trình bày: __Giải thích vì sao 3 tab đủ: persona Cô Lan chỉ có 3 việc chính: chọn lớp, duyệt đề xuất, xem hồ sơ.

__Bằng chứng: __ux/user\-flow.md; Figma Page 01.

## Slide 04. Ba user flow

- Flow A: duyệt gợi ý AI cho một lớp. Lỗi: email sai, mất mạng khi AI chạy (S18, nút Try again)
- Flow B: thêm thành viên vào đề xuất. Lỗi: vượt 6 người (S13, "Max 6 members")
- Flow C: AI không ghép được, mentor ghép tay. Lỗi: sinh viên đã có nhóm bị khóa (S16); hủy đề xuất bằng Discard (S17)
- Bảng flow → màn có trong user\-flow.md

__Ghi chú trình bày: __Kể một flow từ đầu đến cuối; chỉ ra đường lỗi và cách phục hồi.

__Bằng chứng: __assets/flows/flow\-a.png, flow\-b.png, flow\-c.png; bảng phủ màn trong ux/user\-flow.md.

## Slide 05. Tạo UI bằng AI (Stitch)

- Prompt gồm: người dùng (mentor), tác vụ (duyệt gợi ý AI), nền tảng (Android 360×800, Material 3), ràng buộc (chữ ≥14 sp, 1 nút chính, không từ cấm), phong cách (DESIGN.md)
- Lần đầu (R0, hướng sinh viên): 4 màn, có chữ nội bộ như "Lineup", "Roster"
- Hướng mentor (R9, 3 prompt × 6 frame): 18 frame, xuất sang Figma
- Prompt nguyên văn: ai/stitch\-prompts\-r9.md và ai/ai\-design\-log.md mục 3

__Ghi chú trình bày: __Nói rõ cách tách prompt: Stitch chỉ ra khoảng 6 frame mỗi lần, nên chia 3 prompt.

__Bằng chứng: __design/DESIGN.md; ai/ai\-design\-log.md; ảnh Stitch trong assets/stitch/ \[TODO\].

## Slide 06. Iteration và UX critique

- Iteration 1 (R3): chú thích dưới ô vai trò đè chữ → bỏ chú thích
- Iteration 2 (R4): thanh trên cùng và chip thừa không nhất quán → app bar thống nhất, giảm chữ
- Iteration 3 (R6): ô email yêu cầu tên miền edu không còn dùng → email bất kỳ
- Iteration 4 (R7): palette có tông xanh dương, thẻ so với nền chỉ 1.07:1 → palette cam, xanh lá, viền thẻ rõ
- Iteration 5 (R9→Figma): S4 có chữ Stitch tự thêm; S17 nền sai → sửa S4 và S17
- Findings tiêu biểu (≥5, gắn màn): S4 chữ bịa; S17 màn nền sai; S9 badge 10 sp; S2/S12/S13 cao hơn 800 dp; tên layer dài; viền thẻ 1.48:1

__Ghi chú trình bày: __Chọn 1 iteration để kể: vấn đề → prompt hoặc sửa → trước/sau.

__Bằng chứng: __ai/ai\-design\-log.md mục 7; ai/ai\-critique\-1.md; ai/ai\-critique\-2.md; ảnh trước/sau \[TODO\].

## Slide 07. Quyết định thiết kế

- Giữ: AI chỉ đề xuất, mentor duyệt (có nhãn mức phù hợp và lý do ngắn)
- Sửa: bỏ chú thích dưới ô vai trò vì đè chữ ở 360 dp
- Từ chối: dùng cam FPT \#F37021 cho nút (chữ trắng chỉ 2.9:1); chỉ dùng cho logo
- Từ chối/sửa: bỏ màu xanh dương, bỏ trường MSSV và email edu
- Mỗi quyết định gắn với một thay đổi trong Figma (ví dụ: S4 và S17 được sửa trong Figma; S13 đổi thành "Tutor Match, 6 of 6")

__Ghi chú trình bày: __Chuẩn bị trả lời câu "AI đề xuất nào bạn đã từ chối và vì sao?".

__Bằng chứng: __design/design\-decisions.md; ai/ai\-design\-log.md mục 6.

## Slide 08. Wireframe và Final UI

- Wireframe thấp (Figma Page 02) so với 25 màn final (Page 03, 360×800)
- Một nút chính mỗi màn, hàng ngành 40/48 dp làm điểm nhấn
- State: loading (S8), empty (S14 All matched), error (S13, S18), dialog (S12, S17)

__Ghi chú trình bày: __Chỉ ra phân cấp thị giác: tiêu đề, danh sách, nút chính.

__Bằng chứng: __Figma Page 02 và 03; ảnh trong assets/figma/ (đã xuất).

## Slide 09. Design System và Components

- Token màu: primary \#B23E00, primary\-container \#FFE2D2, tertiary \#1B6B3C, error \#B3261E, surface \#FFFFFF, on\-surface \#1C1B18
- Chữ: Be Vietnam Pro; 6 style (24/20/16/16/14/14 sp)
- Spacing 4/8/16/24/32; radius 8/12/16/full; elevation phẳng, chỉ dialog và snackbar có bóng
- 9 component: Button, Text field, Card, Navigation, App bar, Dialog, Loading, Empty, Error, đều có state
- Token dùng qua Figma Variables (0 màu thô trên 25 màn Final UI)

__Ghi chú trình bày: __Trả lời được: màn nào tự đổi khi đổi màu primary (mọi màn dùng biến).

__Bằng chứng: __design/DESIGN.md; Figma Page 04 và 05.

## Slide 10. Accessibility và Responsive

- Chữ thường ≥4.5:1: on\-surface/surface 17.22; on\-primary/primary 5.86; error/error\-container 5.14
- Control ≥3:1: outline/surface 4.61; viền ô đề xuất 4.76; viền thẻ 1.48 (ngoại lệ, chỉ phân tách)
- Touch target ≥48 dp; chữ ≥14 sp; không chỉ dùng màu để báo trạng thái
- Kiểm ở 360 dp và 412 dp: 360 dp đạt (21 frame 360×800, 0 chữ dưới 14 sp); 412 dp chưa kiểm
- Màn rộng ≥600 dp: NavigationRail và master\-detail (chỉ đặc tả)

__Ghi chú trình bày: __Nói rõ mục nào đã đo, mục nào còn TODO.

__Bằng chứng: __design/design\-decisions.md (checklist).

## Slide 11. Prototype tương tác

- 3 flow bấm được từ điểm bắt đầu đến kết thúc, không ngõ cụt (đã kiểm bằng script: mọi màn của từng flow tới được từ điểm bắt đầu)
- Dialog dạng overlay: S12 Approve và S17 Discard
- Loading → kết quả: S8 AI matching → S9 Proposals hoặc S15 No match
- Back quay đúng màn trước

__Ghi chú trình bày: __Demo trực tiếp trong Figma, không dùng ảnh tĩnh.

__Bằng chứng: __Figma Page 06.

## Slide 12. Flutter Handoff và tổng kết

- Mỗi màn có 6 mục: layout, components, states, interactions, navigation, constraints (25 màn)
- Hai bảng: token → Flutter (ColorScheme, TextTheme, hằng số) và component → widget (FilledButton, TextFormField, NavigationBar, AlertDialog…)
- Màn rộng ≥600 dp mô tả trong handoff
- Hạn chế: AI ghép nhóm chỉ là thiết kế giao diện với dữ liệu mẫu, không có mô hình thật; lỗi kích thước từ Stitch đã sửa trong Figma (21 frame 360×800)
- Cảm ơn và Q&A

__Ghi chú trình bày: __Trả lời được: một dev Flutter lạ dựng S12 từ handoff thế nào.

__Bằng chứng: __handoff/flutter\-handoff.md; GitHub.

# 5. Gợi ý trả lời Q&A (bản nháp dựa trên tài liệu của repo; đọc lại và sửa theo ý mình trước khi trình bày)

- Nhu cầu persona nào quyết định cấu trúc điều hướng? Cô Lan dùng một tay, vài phút giữa các tiết và chỉ có ba việc: chọn lớp, duyệt đề xuất, xem hồ sơ. Nên có ba tab dưới cùng (Classes, Proposals, Profile) và các màn con đẩy lên trên tab.
- Flow nào dễ lỗi nhất và người dùng phục hồi ra sao? Flow A, vì phụ thuộc mạng khi AI chạy. Mất mạng thì hiện S18 "You're offline" với nút Try again chạy lại phép ghép (S8); email sai thì S19 báo lỗi dưới ô và mentor nhập lại.
- AI đề xuất nào bạn đã từ chối và vì sao? Từ chối cam FPT #F37021 cho nút vì chữ trắng chỉ 2.9:1 (chỉ dùng cho logo); bỏ tông xanh dương; bỏ trường MSSV và email edu; bỏ chú thích dưới ô vai trò vì đè chữ ở 360 dp.
- Ba iteration xử lý ba vấn đề UX khác nhau ra sao? R3: chú thích đè chữ (H8) nên bỏ chú thích. R4: app bar không nhất quán (H4) nên thống nhất và giảm chữ. R6: email yêu cầu tên miền edu không còn đúng thực tế nên nhận email bất kỳ.
- Màn nào tự đổi khi đổi token màu primary hoặc spacing? Màu: cả 25 màn Final UI, vì mọi fill và stroke đã gắn Variables (kiểm bằng script: 0 màu thô). Spacing và radius: chủ yếu các component ở Page 05; Final UI dựng từ code Stitch dùng số cố định.
- Làm sao bạn kiểm tra layout còn dùng được ở 412 dp? Trả lời thật: chưa kiểm trong Figma. Component ở Page 05 dùng Auto Layout nên co giãn được; việc cần làm là đổi khung Final UI sang 412 dp và xem lại các màn có hàng ngành 5 ô.
- Dev Flutter lạ dựng màn và state từ handoff thế nào? Mỗi màn có 6 mục (layout, components, states, interactions, navigation, constraints) cùng hai bảng token → Flutter và component → widget. Ví dụ S12: showDialog(AlertDialog) mở từ S10, Approve là FilledButton, Cancel là TextButton.

