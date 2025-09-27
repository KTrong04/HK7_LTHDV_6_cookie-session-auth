# Cookie Session Authentication

This project demonstrates how to implement authentication using **Express-session** and cookies.  
It includes features: **Register, Login, Protected Route (Profile), and Logout**.

---

## Test Results

### 1. Register
- API: `POST /register`
- Mô tả: Tạo user mới, lưu vào MongoDB.
- Kết quả:

![Register](./public/results/register.png)

#### Show in MongoDB (Users collection)
![Show Users MongoDB Register](./public/results/show_users_mongodb_register.png)

#### Show Session (MongoDB - after Register)
![Show Session Register](./public/results/show_sessionAuth_mongodb_register.png)

---

### 2. Login
- API: `POST /login`
- Mô tả: Đăng nhập với username/password đúng → tạo session và set cookie `connect.sid`.
- Kết quả:

![Login](./public/results/login.png)

#### Cookie sau khi login
![Show Cookie Login](./public/results/show_cookie_login.png)

#### Show Session (MongoDB - after Login)
![Show Session Login](./public/results/show_sessionAuth_mongodb_login.png)

---

### 3. Profile (Protected Route)
- API: `GET /profile`
- Mô tả: Truy cập tài nguyên cần xác thực bằng session cookie.
- Kết quả:

![Profile](./public/results/profile.png)

---

### 4. Logout
- API: `GET /logout`
- Mô tả: Hủy session, xóa cookie `connect.sid`.
- Kết quả:

![Logout](./public/results/logout.png)

#### Cookie sau khi logout
![Show Cookie Logout](./public/results/show_cookie_logout.png)

#### Show Session (MongoDB - after Logout)
![Show Session Logout](./public/results/show_sessionAuth_mongodb_logout.png)

---

## How to Run

1. Cài đặt dependencies:
   ```bash
   npm install
2. Chạy app
   ```bash
   node app.js
4. Server chạy tại
   ```bash
   http://localhost:3000
