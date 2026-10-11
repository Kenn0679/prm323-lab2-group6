# assets/figma/

PNG xuất từ file Figma: https://www.figma.com/design/X5WcaK4s20AYF53cvRdouV

Trạng thái file Figma (11/10/2026), 6 page đúng thứ tự:

| Page | Nội dung |
|---|---|
| 01 User Flow | Cây IA, Flow A/B/C vẽ bằng layer Figma từ `assets/flows/build_flows.py`, bảng phủ màn S1-S21 (Flow A qua S19, Flow C qua S20 và S21) |
| 02 Wireframe | W01-W21 xám, 360x800, **suy ra từ layout Final UI sau khi Stitch sinh ra** (không phải bản phác trước) |
| 03 Final UI | S01-S21 360x800, dựng từ code HTML của Stitch thành layer Figma; màu và chữ đã gắn Variables và text style |
| 04 Design System | Variables Color / Spacing / Radius, 6 text style, bảng tương phản tính từ giá trị thật, icon, ô ngành |
| 05 Components | 14 component set có variant và state (Button, Major slot, Filter chip, Fit chip, Checkbox row, Text field, Card, Team card, App bar, Navigation bar, Dialog, Loading, Empty, Error) và Snackbar |
| 06 Prototype | 3 hàng Flow A/B/C, mỗi hàng có điểm bắt đầu riêng, loading tự chuyển sau 3-4 giây, đường lỗi S19, S18, S13, S21, S17; Flow C đi qua S20 |

Ảnh PNG chưa có (chưa xuất được từ phiên làm việc này). Người phụ trách Figma xuất và bỏ vào đây:
- `s01-sign-in.png` ... `s21-add-student-no-results.png`: 21 màn Final UI, khung 360x800 (File > Export, 2x).
- `s04-after.png`, `s17-after.png`: hai màn đã sửa trong Figma (ảnh "before" ở `../stitch/mentor-v2/s04-no-team/screen.png` và `s17-discard-dialog/screen.png`).
- Ảnh chụp 6 page Figma và các section Design System, Components.
