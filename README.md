# BookingKS
📌 Giới thiệu

  Đây là một Single Page Application (SPA) quản lý và đặt phòng khách sạn, xây dựng hoàn toàn bằng HTML, CSS, JavaScript (không sử dụng framework backend).
Ứng dụng chạy trực tiếp trên trình duyệt, dữ liệu lưu bằng LocalStorage.

🚀 Chức năng chính

🔑 Xác thực & Phân quyền: Đăng nhập/Đăng ký, phân quyền theo vai trò:

  Admin: Toàn quyền (người dùng, phòng, dịch vụ, booking, thanh toán).

  Manager/Staff: Quản lý phòng, dịch vụ, đơn đặt, thanh toán.

  Customer: Đặt phòng, xem & quản lý đơn đặt của mình.

🏨 Quản lý phòng: CRUD phòng, loại phòng, tình trạng (Available, Maintenance…).

🛎️ Quản lý dịch vụ: CRUD dịch vụ bổ sung (Spa, Giặt ủi…).

📅 Đặt phòng trực tuyến: Chọn ngày, loại phòng, số khách, dịch vụ kèm theo.

📂 Quản lý booking: Xác nhận, hủy, check-in/out.

💳 Quản lý thanh toán: Tích hợp thanh toán demo.

📊 Dashboard: Thống kê phòng trống, đơn đặt, thanh toán pending.

🎨 Giao diện đẹp: Thiết kế hiện đại, responsive.

📁 Cấu trúc dự án
├── index.html   # Giao diện chính
├── style.css    # Toàn bộ CSS
└── script.js    # Logic ứng dụng (CRUD, Auth, Booking...)

🛠️ Công nghệ sử dụng

HTML5

CSS3 (Flexbox, Grid, Responsive Design)

JavaScript (ES6)

LocalStorage (lưu dữ liệu)

👤 Tài khoản Demo

Admin: admin@hotel.com / admin123

Manager: manager@hotel.com / manager123

Staff: staff@hotel.com / staff123

Khách hàng: customer@email.com / 123456

▶️ Cách chạy

Clone/Download dự án về máy.

Mở file index.html bằng trình duyệt (Chrome/Edge/Firefox).

Đăng nhập bằng tài khoản demo hoặc Đăng ký tài khoản mới.

Sử dụng các chức năng:

Khách hàng: đặt phòng, xem đơn của tôi.

Nhân viên/Quản lý: quản lý phòng, dịch vụ, booking, thanh toán.

Admin: quản lý tất cả bao gồm người dùng.

💡 Lưu ý

Đây là phiên bản demo frontend-only, chưa kết nối CSDL thực tế.

Dữ liệu được lưu trên LocalStorage, sẽ mất khi xóa cache trình duyệt.

📷 Giao diện minh họa

Màn hình đăng nhập

Dashboard với thống kê

Booking form

Quản lý phòng & dịch vụ

Quản lý người dùng (Admin)
