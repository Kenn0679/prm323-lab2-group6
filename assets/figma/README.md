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

## PNG đã xuất (11/10/2026, 1x)

| Thư mục | Nội dung |
|---|---|
| `01-user-flow/` | 1 ảnh toàn page 01 |
| `02-wireframe/` | W01-W21 (360x800) + `wireframe-note.png` |
| `03-final-ui/` | S01-S21 (360x800); S04 và S17 là bản đã sửa trong Figma (ảnh "before" ở `../stitch/mentor-v2/s04-no-team/screen.png` và `s17-discard-dialog/screen.png`) |
| `04-design-system/` | Page 04 |
| `05-components/` | Page 05 |
| `06-prototype/` | 31 frame A0-A11, B0-B7, C0-C10 + 4 ảnh nhãn (header, Flow A/B/C label) |

Quy ước tên file: chữ thường, dấu gạch ngang, không dấu cách (ví dụ `s04-no-team.png`, `w04-no-team.png`, `a3-s04-no-team.png`). Prototype: chữ cái A/B/C là flow, số là thứ tự frame trong flow.
