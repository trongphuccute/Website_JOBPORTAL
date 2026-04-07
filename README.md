

#  JobPortal - Hệ Thống Tuyển Dụng Trực Tuyến

**JobPortal** là một nền tảng Web hiện đại kết nối ứng viên và nhà tuyển dụng, giúp tối ưu hóa quy trình tìm kiếm việc làm và quản lý nhân sự. Dự án được xây dựng trên nền tảng Django vững chắc với kiến trúc bảo mật và khả năng mở rộng cao.

-----

##  1. Công Nghệ Sử Dụng (Tech Stack)

Hệ thống kết hợp các công nghệ phổ biến để đảm bảo hiệu suất và tính ổn định:

| Thành phần | Công nghệ |
| :--- | :--- |
| **Backend** |  Python Framework |
| **Frontend** |  HTML, CSS, JAVASCRIPT   |
| **Database** | PostgreSQL |
| **Architecture**| MVT (Model-View-Template) & Client-Server |

-----

## 2. Kiến Trúc Hệ Thống (Architecture)

Dự án tuân thủ luồng dữ liệu chặt chẽ từ giao diện đến cơ sở dữ liệu:

```text
[ Browser ] <--> [ Frontend (HTML/JS/Bootstrap) ] 
                            ↓↑ (Fetch API/HTTP)
                    [ Django Views (Logic) ]
                            ↓↑ (ORM)
                    [ Django Models (Data) ]
                            ↓↑
                    [ PostgreSQL Database ]
```

**Các Module Cốt Lõi:**

  * `accounts`: Quản lý người dùng và xác thực.
  * `jobs`: Quản lý thông tin công ty và tin tuyển dụng.
  * `applications`: Xử lý quy trình ứng tuyển và quản lý CV.

-----

## 3. Tính Năng Chính (System Requirements)

Hệ thống phân quyền rõ ràng cho 4 nhóm đối tượng:

  * **Ứng viên (Job Seeker):** Tạo Profile, Upload CV, Tìm kiếm việc làm, Ứng tuyển & Lưu tin.
  * **Nhà tuyển dụng (Employer):** Quản lý trang công ty, Đăng tin (CRUD), Quản lý danh sách ứng viên.
  * **Quản trị viên (Admin):** Quản lý người dùng, kiểm duyệt tin đăng.
  * **Khách (Guest):** Xem tin tuyển dụng và tìm kiếm cơ bản.

-----

## 4. Hướng Dẫn Cài Đặt (Installation)

Dành cho các thành viên mới tham gia dự án:

1.  **Clone Repo:** `git clone <repository_url>`
2.  **Khởi tạo môi trường:**
    ```bash
    python -m venv venv
    # Windows: venv\Scripts\activate | Mac/Linux: source venv/bin/activate
    pip install -r requirements.txt
    ```
3.  **Cấu hình Database:**
    ```bash
    python manage.py migrate
    python manage.py runserver
    ```

-----

## 5. Quy Chuẩn Đóng Góp (Contributing)

Để giữ code luôn sạch và dễ quản lý, vui lòng tuân thủ:

### **Quy tắc Commit:**

  * `feat: ...` (Tính năng mới)
  * `fix: ...` (Sửa lỗi)
  * `refactor: ...` (Cải thiện code)

### **Quy trình làm việc (Git Workflow):**

1.  Nhánh `main` dùng cho Production.
2.  Nhánh `develop` dùng cho phát triển chung.
3.  Nhánh `feature/*` cho từng tính năng riêng lẻ.

-----

## 6. Quy Trình Phát Triển (Development Workflow)

Khi phát triển một tính năng (Ví dụ: **Ứng tuyển**), hãy thực hiện theo thứ tự:

1.  **Model:** Định nghĩa bảng `applications` trong Database.
2.  **Migration:** Cập nhật schema database.
3.  **View:** Xử lý logic kiểm tra điều kiện ứng tuyển.
4.  **Template/JS:** Xây dựng giao diện và gọi API gửi dữ liệu.
5.  **Test:** Kiểm tra luồng dữ liệu từ UI xuống DB và phản hồi người dùng.

-----

## 7. Bảo Mật & Hiệu Năng

  * **Bảo mật:** Tích hợp CSRF Protection, Password Hashing mặc định của Django.
  * **Hiệu năng:** Tối ưu hóa truy vấn ORM, đảm bảo thời gian phản hồi \< 3s.
  * **UI/UX:** Giao diện Responsive hoạt động tốt trên mọi kích thước màn hình.

-----

 *Dự án được phát triển bởi nhóm JobPortal. Chúc bạn có những trải nghiệm tuyệt vời khi sử dụng hệ thống\!*
