Version 3
1) Tải về — lưu ý quan trọng
  
  Tải đủ tất cả các phần (part1, part2, part3, ...) — nếu thiếu 1 phần thì không thể giải nén được.
  
  **Đặt tất cả các phần vào một cùng một thư mục trên máy tính (không cần sắp xếp thứ tự bằng tay).
  
  Không đổi tên các file phần — giữ nguyên tên do WinRAR dùng tên để nhận thứ tự.

2) Cách giải nén bằng WinRAR (Windows) — cách dễ nhất

  Mở thư mục chứa tất cả các .part*.rar.
  
  Chuột phải vào HotelBookingSystem.part1.rar → chọn Extract Here (Giải nén ở đây) hoặc Extract to HotelBookingSystem/ (Giải vào thư mục con).
  
  WinRAR tự động đọc part1 rồi tìm và nối các phần part2, part3, ... để tạo lại file gốc và giải nén nội dung.
  
  Hoàn tất — bạn sẽ thấy file/ thư mục gốc như trước khi chia.
  
  Chỉ cần mở part1 — không cần mở từng phần riêng lẻ.

3) Người nhận phục hồi (Restore)

  Người nhận mở SSMS và:
  
  Nhấn chuột phải vào Databases → Restore Database...
  
  Chọn Device, duyệt đến file .bak.
  
  Đặt tên database (hoặc để mặc định).
  
  Nhấn OK để khôi phục.

4) # Hướng dẫn chạy Project ASP.NET Core MVC (Database First) trên Visual Studio 2022 💜

  Dự án này được xây dựng bằng **ASP.NET Core MVC** theo mô hình **Database First (First Data)** — nghĩa là cơ sở dữ liệu (database) được tạo sẵn trong SQL Server, sau đó sinh code (Model và DbContext) bằng lệnh Scaffold.
  
  ---
  
  ## 🧰 Yêu cầu
  - **Visual Studio 2022 (logo tím)**  
  - **.NET SDK** phù hợp với project (xem `TargetFramework` trong file `.csproj`, ví dụ `net8.0`)
  - **SQL Server / SQL Server Express** (để kết nối database)
  
  ---
  
  ## 🚀 Các bước chạy project
  
  ### 1️⃣ Giải nén & mở project
  - Giải nén file ZIP vào thư mục **không có dấu tiếng Việt** hoặc **khoảng trắng**.  
    👉 Ví dụ: `C:\Projects\MyMvcApp`
  - Mở **Visual Studio 2022** → **File → Open → Project/Solution** → chọn file `.sln`.
  
  ---
  
  ### 2️⃣ Restore NuGet Packages
  Visual Studio thường tự động restore khi mở project.  
  Nếu không:
  - Mở **Tools → NuGet Package Manager → Package Manager Console**  
    Nhập lệnh:
    ```powershell
    Update-Package -reinstall
    ```
    Hoặc mở **Terminal** và chạy:
    ```bash
    dotnet restore
    ```
  
  ---
  
  ### 3️⃣ Cấu hình chuỗi kết nối (Connection String)
  Mở file `appsettings.json`, chỉnh lại cho phù hợp với SQL Server trên máy bạn:
  
  ```json
  "ConnectionStrings": {
    "DefaultConnection": "Server=.;Database=MyMvcAppDb;Trusted_Connection=True;"
  }
  ```
  
  Nếu bạn dùng SQL Server Express, hãy sửa thành:
  
  ```json
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost\\SQLEXPRESS;Database=MyMvcAppDb;Trusted_Connection=True;"
  }
  ```
  
  > 💡 Đảm bảo database (ví dụ `MyMvcAppDb`) đã tồn tại trong SQL Server.
  
  ---
  
  ### 4️⃣ (Tuỳ chọn) Sinh lại code từ database bằng Scaffold
  Chỉ thực hiện nếu bạn muốn sinh lại Models/DbContext từ database:
  
  ```powershell
  Scaffold-DbContext "Server=.;Database=MyMvcAppDb;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models
  ```
  
  ---
  
  ### 5️⃣ Build & chạy project
  - Vào menu **Build → Build Solution (Ctrl+Shift+B)** để biên dịch.  
  - Sau đó nhấn **F5** (chạy có debug) hoặc **Ctrl+F5** (chạy không debug).  
  - Visual Studio sẽ tự mở trình duyệt tại địa chỉ:  
    👉 `https://localhost:xxxx` (port tự động thay đổi)
  
  ---
  
  
  ✅ **Sau khi làm đủ các bước trên, bạn có thể chạy project ASP.NET Core MVC (Database First) trên Visual Studio 2022 mà không cần scaffold lại.**

