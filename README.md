# Xây Dựng Website Gợi Ý Lịch Trình Du Lịch Thông Minh

Ứng dụng web full-stack hỗ trợ tư vấn du lịch Việt Nam bằng trí tuệ nhân tạo. Người dùng có thể chat với AI để được gợi ý lịch trình, điểm đến, đặc sản theo từng vùng miền (Bắc – Trung – Nam – Tây Nguyên), lên kế hoạch chuyến đi và quản lý hành trình cá nhân.

---

## Cấu trúc thư mục

```
├── docs/               # Tài liệu đồ án tốt nghiệp
│   ├── DOANTOTNGHIEP3.docx
│   ├── DOANTOTNGHIEP3.pdf
│   ├── 4 (Poster).pdf
│   └── Hướng dẫn sử dụng chương trình, chạy demo .pdf
├── src/
│   ├── backend/        # API server (Express.js + MongoDB)
│   └── frontend/       # Giao diện người dùng (Next.js 16)
└── README.md
```

---

## Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| Backend | Node.js, Express.js, Mongoose, Socket.IO |
| Frontend | Next.js 16, React 19, Tailwind CSS 4, Leaflet |
| Cơ sở dữ liệu | MongoDB |
| AI | NVIDIA API — `stepfun-ai/step-3.7-flash` |
| Xác thực | JWT, Google OAuth |

---

## Tính năng chính

- **Chat AI tư vấn du lịch** — gợi ý điểm đến, lịch trình, đặc sản theo vùng miền; AI chỉ gợi ý dựa trên dữ liệu thực từ database
- **Lập kế hoạch hành trình** — tự động tạo và lưu itinerary từ cuộc trò chuyện với AI
- **Bản đồ tương tác** — xem điểm đến và hành trình trên bản đồ (Leaflet)
- **Khám phá điểm đến** — tìm kiếm, lọc theo tỉnh/vùng, xem đánh giá
- **Đặc sản địa phương** — tra cứu ẩm thực theo từng tỉnh
- **Hệ thống bạn bè & chia sẻ** — kết bạn, chia sẻ hành trình
- **Thời tiết thực tế** — tích hợp thông tin thời tiết theo điểm đến
- **Quản trị viên** — dashboard quản lý người dùng, điểm đến, nội dung

---

## Yêu cầu hệ thống

- Node.js >= 18
- MongoDB >= 6
- npm >= 9

---

## Cài đặt và chạy

### 1. Clone repository

```bash
git clone <repository-url>
cd travelai
```

### 2. Cấu hình Backend

```bash
cd src/backend
npm install
```

Tạo file `.env` từ `.env.example`:

```bash
cp .env.example .env
```

Chỉnh sửa `.env` với các giá trị thực tế:

```env
PORT=5001
MONGODB_URI=mongodb://localhost:27017/travelai
JWT_SECRET=your_jwt_secret
NVIDIA_API_KEY=your_nvidia_api_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

### 3. Cấu hình Frontend

```bash
cd src/frontend
npm install
```

Tạo file `.env.local`:

```env
NEXT_PUBLIC_API_URL=http://localhost:5001
```

### 4. Khởi chạy dự án

Mở 2 terminal riêng biệt:

**Terminal 1 — Backend:**
```bash
cd src/backend
npm run dev
# Server chạy tại http://localhost:5001
```

**Terminal 2 — Frontend:**
```bash
cd src/frontend
npm run dev
# Ứng dụng chạy tại http://localhost:3000
```

### 5. Seed dữ liệu mẫu (tùy chọn)

```bash
cd src/backend
npm run seed:all
```

---

## Thông tin đồ án

**Trường Đại học Trà Vinh**
Trường Kỹ thuật và Công nghệ — Khoa Công nghệ Thông tin

| | |
|---|---|
| **Sinh viên thực hiện** | Nguyễn Đình Tuấn Khoa |
| **MSSV** | 110122094 |
| **Lớp** | DA22TTD |
| **Giáo viên hướng dẫn** | TS. Đoàn Phước Miền |
| **Năm** | 2026 |
