# Nguồn gốc hình nhân viên (`staff.png`)

`staff.png` là atlas nhân viên của văn phòng pixel: 12 nhân vật, mỗi ô 24 × 40, 4 cột × 17 hàng dáng (đứng, chớp mắt, quay lưng, nghiêng, đi 3 hướng, ngồi bàn, gõ phím, ngồi sofa, nói, cầm cốc, ngủ gật, bị chặn, ăn mừng).

Đây là **hình phái sinh** từ bộ **Modern Rooms & People** của **HappyHustle** (https://happyhustle.itch.io/modern-rooms-people), đã căn lại, đổi màu và thêm dáng cho văn phòng. Tác giả hình gốc là HappyHustle; khung này không nhận là tác giả.

## Giấy phép gốc (nguyên văn, bản 0.2.0)

```
MODERN ROOMS & PEOPLE — ASSET LICENSE
Copyright 2026 HappyHustle

You may use and modify these assets in commercial and non-commercial games,
applications, videos and promotional materials. Credit is optional.
You may distribute the assets inside a finished project and share working files
privately with collaborators on that project.
Standalone redistribution, repackaging, resale or sublicensing of the assets,
including modified versions, as an asset collection is prohibited.
Do not claim authorship of the original artwork. Sample code has the same
project-use permission. Provided as-is, without warranty.
https://happyhustle.itch.io/
```

## Ràng buộc khi dùng khung

- Chỉ dùng `staff.png` bên trong công cụ văn phòng (`tools/office/`). Không tách ra, không chia sẻ hay đăng thành một bộ tài nguyên riêng.
- Giữ repo khung riêng tư. Nếu mở mã nguồn khung (ví dụ giấy phép MIT), phải gỡ `staff.png` và thay bằng hình tự vẽ trước khi công bố.
- Dự án tạo từ khung được giữ `staff.png` vì nó nằm trong sản phẩm hoàn chỉnh; giữ kèm file này.

## Bảng màu đồ vật

Sàn, tường và đồ vật trong `index.html` vẫn do code tự vẽ (không chép hình của pack), nhưng dùng bảng màu môi trường của cùng bộ Modern Rooms & People (`environment-palette.gpl`, hằng `HH` trong code) để cùng tông với nhân viên.

# Nguồn gốc hình thú cưng (`pets.png`)

`pets.png` là atlas mèo và corgi, quay sang trái. Hàng mèo (y 0, ô 22 × 16): 6 khung đi, ngồi, nằm ngủ. Hàng corgi (y 16, ô 28 × 20): 4 khung đi, đứng, ngồi nhìn thẳng, nằm ngủ.

- **Mèo tuxedo:** hình phái sinh từ **Cat Sprites** của **Shepardskin** (https://opengameart.org/content/cat-sprites), giấy phép **CC0 1.0** (không bắt buộc ghi công, tác giả mong được ghi tên). Mèo đen gốc được tô thêm ngực, mõm, bàn chân trắng và viền tối một điểm ảnh.
- **Corgi:** hình do AI vẽ theo yêu cầu của chủ repo (2026-10-29), cam trắng, mông hình tim, giữ đúng bố cục ô ở trên. Không lấy từ bộ hình có bản quyền nào.

Mèo (CC0) và corgi (AI vẽ) không ràng buộc phân phối, nên `pets.png` không chịu các giới hạn của `staff.png` ở trên.

# Thư viện markdown (`vendor/`)

Trang văn phòng hiện phần markdown (bảng, danh sách, chữ đậm) trong câu hỏi, mục tiêu task / sprint và gói duyệt bằng hai thư viện chép nguyên bản, không sửa, chạy được khi không có mạng:

| File | Thư viện | Phiên bản | Giấy phép | Nguồn |
|---|---|---|---|---|
| `vendor/marked.umd.js` | marked | 15.0.12 | MIT | https://github.com/markedjs/marked |
| `vendor/purify.min.js` | DOMPurify (lọc HTML trước khi chèn, chống chèn script) | 3.2.6 | Apache-2.0 hoặc MPL-2.0 | https://github.com/cure53/DOMPurify |

Nâng phiên bản: tải đúng file `lib/marked.umd.js` và `dist/purify.min.js` của bản mới, thay file, sửa bảng này.
