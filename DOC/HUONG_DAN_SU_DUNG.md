# HƯỚNG DẪN SỬ DỤNG CHƯƠNG TRÌNH TRAVELAI

## Hệ Thống Gợi Ý Du Lịch Thông Minh

---

## MỤC LỤC

1. [Giới thiệu chung](#1-giới-thiệu-chung)
2. [Yêu cầu hệ thống](#2-yêu-cầu-hệ-thống)
3. [Hướng dẫn cài đặt và khởi chạy chương trình](#3-hướng-dẫn-cài-đặt-và-khởi-chạy-chương-trình)
4. [Hướng dẫn sử dụng dành cho Người dùng](#4-hướng-dẫn-sử-dụng-dành-cho-người-dùng)
   - 4.1. [Trang chủ](#41-trang-chủ)
   - 4.2. [Đăng ký tài khoản](#42-đăng-ký-tài-khoản)
   - 4.3. [Đăng nhập](#43-đăng-nhập)
   - 4.4. [Thiết lập sở thích (Onboarding)](#44-thiết-lập-sở-thích-onboarding)
   - 4.5. [Khám phá điểm đến](#45-khám-phá-điểm-đến)
   - 4.6. [Xem bản đồ (Explore)](#46-xem-bản-đồ-explore)
   - 4.7. [Khám phá Tour du lịch](#47-khám-phá-tour-du-lịch)
   - 4.8. [Quiz Gợi ý thông minh (SmartSuggestion)](#48-quiz-gợi-ý-thông-minh-smartsuggestion)
   - 4.9. [Chat với AI](#49-chat-với-ai)
   - 4.10. [Quản lý lịch trình](#410-quản-lý-lịch-trình)
   - 4.11. [Dẫn đường thực tế (Navigation)](#411-dẫn-đường-thực-tế-navigation)
   - 4.12. [Điểm đến đã lưu](#412-điểm-đến-đã-lưu)
   - 4.13. [Quản lý tài khoản cá nhân (Profile)](#413-quản-lý-tài-khoản-cá-nhân-profile)
   - 4.14. [Bạn bè và Nhắn tin](#414-bạn-bè-và-nhắn-tin)
5. [Hướng dẫn sử dụng dành cho Quản trị viên (Admin)](#5-hướng-dẫn-sử-dụng-dành-cho-quản-trị-viên-admin)
   - 5.1. [Truy cập trang quản trị](#51-truy-cập-trang-quản-trị)
   - 5.2. [Dashboard tổng quan](#52-dashboard-tổng-quan)
   - 5.3. [Quản lý điểm đến](#53-quản-lý-điểm-đến)
   - 5.4. [Quản lý Tour](#54-quản-lý-tour)
   - 5.5. [Quản lý đánh giá](#55-quản-lý-đánh-giá)
   - 5.6. [Quản lý lịch trình](#56-quản-lý-lịch-trình)
   - 5.7. [Quản lý người dùng](#57-quản-lý-người-dùng)
   - 5.8. [Lịch sử chat AI](#58-lịch-sử-chat-ai)
6. [Các lưu ý quan trọng](#6-các-lưu-ý-quan-trọng)

---

## 1. Giới thiệu chung

**TravelAI** là một hệ thống gợi ý du lịch thông minh tại Việt Nam, sử dụng trí tuệ nhân tạo (AI) để cá nhân hóa các gợi ý điểm đến và lịch trình du lịch cho người dùng dựa trên sở thích, ngân sách và hành vi.

**Các tính năng chính của chương trình:**

- **Chat AI thông minh:** Người dùng có thể trò chuyện với AI để nhận gợi ý điểm đến, lịch trình du lịch phù hợp với sở thích cá nhân.
- **Quiz gợi ý thông minh (SmartSuggestion):** Trả lời 5 câu hỏi đơn giản, AI sẽ tự động đề xuất lịch trình phù hợp.
- **Khám phá điểm đến:** Duyệt danh sách hàng trăm điểm đến du lịch tại Việt Nam, lọc theo danh mục, mức giá, đánh giá.
- **Bản đồ tương tác:** Xem vị trí các điểm đến trên bản đồ, tìm kiếm theo khu vực.
- **Tour du lịch:** Khám phá các tour du lịch có sẵn, xem chi tiết lịch trình và lưu tour yêu thích.
- **Quản lý lịch trình cá nhân:** Tạo, chỉnh sửa, lưu lịch trình du lịch và xem trên bản đồ hành trình.
- **Dẫn đường thực tế:** Dẫn đường turn-by-turn từ vị trí hiện tại đến các điểm đến trong lịch trình.
- **Đánh giá và nhận xét:** Viết đánh giá cho các điểm đến đã đi.
- **Bạn bè và nhắn tin:** Kết nối với bạn bè, nhắn tin trực tiếp.
- **Trang quản trị (Admin):** Quản lý toàn bộ nội dung hệ thống gồm điểm đến, tour, đánh giá, người dùng, lịch sử chat.

---

## 2. Yêu cầu hệ thống

### 2.1. Phần mềm cần cài đặt trước

| Phần mềm | Phiên bản tối thiểu | Mục đích |
|-----------|---------------------|----------|
| **Node.js** | 18.0 trở lên | Chạy Backend và Frontend |
| **npm** | Đi kèm Node.js | Quản lý thư viện |
| **Trình duyệt web** | Chrome, Edge, Firefox phiên bản mới nhất | Truy cập giao diện web |

### 2.2. Tài khoản dịch vụ bên ngoài (dành cho lập trình viên triển khai)

| Dịch vụ | Mục đích |
|---------|----------|
| **MongoDB Atlas** | Cơ sở dữ liệu đám mây |
| **Cerebras AI** (Llama 3.1-8B) | Xử lý AI chat và gợi ý |
| **OpenWeatherMap** | Cung cấp thông tin thời tiết |
| **Google OAuth** (tuỳ chọn) | Đăng nhập bằng Google |

### 2.3. Cấu hình máy tính đề xuất

- Hệ điều hành: Windows 10/11, macOS hoặc Linux
- RAM: Tối thiểu 4GB (khuyến nghị 8GB)
- Ổ cứng: Tối thiểu 500MB dung lượng trống
- Kết nối Internet ổn định (để kết nối MongoDB Atlas và API AI)

---

## 3. Hướng dẫn cài đặt và khởi chạy chương trình

### Bước 1: Tải mã nguồn

Tải toàn bộ mã nguồn chương trình về máy tính. Giải nén (nếu cần) vào một thư mục, ví dụ: `D:\travelai`.

### Bước 2: Cài đặt Backend

Mở cửa sổ dòng lệnh (Command Prompt hoặc Terminal), sau đó thực hiện lần lượt:

```
cd D:\travelai\backend
npm install
```

Chờ cho đến khi quá trình cài đặt các thư viện hoàn tất (có thể mất vài phút tùy tốc độ mạng).

### Bước 3: Cấu hình biến môi trường Backend

Trong thư mục `backend`, tạo file `.env` (hoặc sao chép từ file `.env.example`). Mở file `.env` bằng trình soạn thảo văn bản và điền các thông tin sau:

```
PORT=5001
MONGODB_URI=mongodb+srv://<tên_user>:<mật_khẩu>@cluster0.xxxxx.mongodb.net/?appName=Cluster0
JWT_SECRET=<chuỗi_bí_mật_tự_đặt>
CEREBRAS_API_KEY=<API_key_Cerebras>
OPENWEATHER_API_KEY=<API_key_OpenWeather>
```

Thay thế các giá trị trong dấu `<>` bằng thông tin thật của bạn.

### Bước 4: Khởi tạo dữ liệu mẫu (tuỳ chọn)

Nếu cơ sở dữ liệu chưa có dữ liệu, chạy lệnh sau để tạo dữ liệu mẫu:

```
npm run seed:all
```

Lệnh này sẽ tạo sẵn tài khoản admin, dữ liệu điểm đến và dữ liệu ẩm thực.

### Bước 5: Khởi chạy Backend

```
npm run dev
```

Khi thấy thông báo server chạy thành công tại `http://localhost:5001`, nghĩa là Backend đã sẵn sàng.

### Bước 6: Cài đặt Frontend

Mở **một cửa sổ dòng lệnh mới** (giữ nguyên cửa sổ Backend đang chạy), sau đó:

```
cd D:\travelai\frontend
npm install
```

### Bước 7: Cấu hình biến môi trường Frontend

Trong thư mục `frontend`, tạo file `.env.local` với nội dung:

```
NEXT_PUBLIC_API_URL=http://localhost:5001/api
```

### Bước 8: Khởi chạy Frontend

```
npm run dev
```

Khi thấy thông báo server chạy tại `http://localhost:3000`, chương trình đã sẵn sàng sử dụng.

### Bước 9: Truy cập chương trình

Mở trình duyệt web và nhập địa chỉ: **http://localhost:3000**

Trang chủ TravelAI sẽ hiển thị.

---

## 4. Hướng dẫn sử dụng dành cho Người dùng

### 4.1. Trang chủ

Khi truy cập vào địa chỉ `http://localhost:3000`, người dùng sẽ thấy **trang chủ TravelAI** với các thành phần chính:

**Bước 1:** Quan sát **thanh điều hướng (Navbar)** ở phía trên cùng của trang. Thanh điều hướng chứa các mục menu:
- **Trang chủ** — Quay về trang chính
- **Tours** — Xem danh sách các tour du lịch
- **Bản Đồ** — Xem bản đồ các điểm đến
- **Điểm Đến** — Duyệt danh sách điểm đến
- **Lịch Trình** — Xem các lịch trình đã tạo
- **AI Chat** — Trò chuyện với trợ lý AI

**Bước 2:** Cuộn xuống phần **Hero** (phần giới thiệu nổi bật) để xem hình ảnh và thông điệp chào mừng của TravelAI.

**Bước 3:** Tiếp tục cuộn xuống phần **TravelShowcase** để xem các điểm đến nổi bật được giới thiệu dưới dạng ảnh lớn xoay vòng tự động.

**Bước 4:** Phần **Destinations** hiển thị danh sách các điểm đến được gợi ý. Người dùng có thể bấm vào từng điểm đến để xem chi tiết.

**Bước 5:** Phần **Footer** (cuối trang) chứa thông tin liên hệ và các liên kết hữu ích.

> **Lưu ý:** Nếu chưa đăng nhập, phía bên phải thanh điều hướng sẽ hiện hai nút: **"Đăng Nhập"** và **"Đăng Ký"**. Nếu đã đăng nhập, sẽ hiện tên người dùng và ảnh đại diện.

---

### 4.2. Đăng ký tài khoản

**Bước 1:** Tại thanh điều hướng, bấm nút **"Đăng Ký"** (nút có nền màu gradient xanh-tím).

**Bước 2:** Trang đăng ký hiện ra với tiêu đề **"Tạo tài khoản mới"**. Điền đầy đủ các thông tin:
- **Họ và tên:** Nhập họ và tên đầy đủ của bạn (ví dụ: Nguyễn Văn A).
- **Email:** Nhập địa chỉ email hợp lệ (ví dụ: nguyenvana@gmail.com).
- **Mật khẩu:** Nhập mật khẩu ít nhất 6 ký tự. Bấm biểu tượng **con mắt** bên phải ô mật khẩu để hiện/ẩn mật khẩu.
- **Xác nhận mật khẩu:** Nhập lại chính xác mật khẩu vừa tạo.

**Bước 3:** Tích chọn ô **"Tôi đồng ý với Điều khoản sử dụng và Chính sách bảo mật"**.

**Bước 4:** Bấm nút **"Đăng Ký"**.

**Bước 5:** Nếu đăng ký thành công, hệ thống sẽ tự động chuyển về trang chủ và bạn đã được đăng nhập. Nếu có lỗi (ví dụ email đã tồn tại, mật khẩu không khớp), một thông báo lỗi màu đỏ sẽ hiện ở phía trên form.

> **Cách khác:** Bạn có thể bấm nút **"Đăng ký với Google"** để đăng ký nhanh bằng tài khoản Google.

> **Lưu ý:** Nếu đã có tài khoản, bấm dòng chữ **"Đăng nhập"** ở cuối form để chuyển sang trang đăng nhập.

---

### 4.3. Đăng nhập

**Bước 1:** Tại thanh điều hướng, bấm **"Đăng Nhập"**.

**Bước 2:** Trang đăng nhập hiện ra với tiêu đề **"Chào mừng trở lại!"**. Điền thông tin:
- **Email:** Nhập email đã đăng ký.
- **Mật khẩu:** Nhập mật khẩu. Bấm biểu tượng **con mắt** để hiện/ẩn mật khẩu nếu cần.

**Bước 3:** (Tuỳ chọn) Tích chọn ô **"Ghi nhớ đăng nhập"** nếu muốn hệ thống nhớ phiên đăng nhập.

**Bước 4:** Bấm nút **"Đăng Nhập"**.

**Bước 5:** Nếu đăng nhập thành công, hệ thống chuyển về trang chủ. Tên người dùng sẽ hiện trên thanh điều hướng.

> **Cách khác:** Bấm nút **"Đăng nhập với Google"** để đăng nhập bằng tài khoản Google.

> **Nếu quên mật khẩu:** Bấm dòng chữ **"Quên mật khẩu?"** để đặt lại mật khẩu.

---

### 4.4. Thiết lập sở thích (Onboarding)

Sau khi đăng ký tài khoản mới, hệ thống có thể chuyển bạn đến trang **Onboarding** để thiết lập sở thích cá nhân. Trang này giúp AI gợi ý chính xác hơn.

**Bước 1 — Chọn phong cách du lịch:**
- Trang hiện ra câu hỏi: **"Bạn thích du lịch kiểu nào?"**
- Chọn một hoặc nhiều loại hình: Biển & Đảo, Núi & Cao nguyên, Thành phố, Di tích & Văn hóa, Nông thôn, Mạo hiểm.
- Bấm **"Tiếp tục →"** để sang bước tiếp theo.

**Bước 2 — Chọn ngân sách:**
- Câu hỏi: **"Ngân sách du lịch của bạn?"**
- Chọn một mức: Tiết kiệm (dưới 2 triệu/người), Trung bình (2-5 triệu/người), hoặc Cao cấp (trên 5 triệu/người).
- Bấm **"Tiếp tục →"**.

**Bước 3 — Chọn sở thích:**
- Câu hỏi: **"Bạn quan tâm đến điều gì?"**
- Chọn các hoạt động yêu thích: Ẩm thực, Chụp ảnh, Thiên nhiên, Mua sắm, Nightlife, Spa & Wellness, Gia đình, Lãng mạn.
- Bấm **"🚀 Bắt đầu khám phá!"** để hoàn tất.

> **Lưu ý:** Nếu không muốn thiết lập ngay, bấm **"Bỏ qua, tôi sẽ thiết lập sau"** ở cuối trang.

---

### 4.5. Khám phá điểm đến

**Bước 1:** Bấm menu **"Điểm Đến"** trên thanh điều hướng.

**Bước 2:** Trang danh sách điểm đến hiện ra. Phía trên là **thanh tìm kiếm** và các **bộ lọc**:

- **Thanh tìm kiếm:** Nhập tên điểm đến hoặc tỉnh thành (ví dụ: "Đà Nẵng", "Hội An") rồi bấm Enter hoặc biểu tượng kính lúp để tìm kiếm.

- **Lọc theo danh mục:** Bấm vào các nút danh mục để lọc:
  - 🌍 Tất cả
  - 🏖️ Biển
  - 🏔️ Núi
  - 🎡 Khu vui chơi
  - 🏮 Văn hóa
  - 📸 Địa danh
  - 🏨 Khách sạn
  - 🍜 Nhà hàng & Quán ăn
  - ☕ Quán Cafe
  - 🛍️ Chợ & Mua sắm
  - 🌾 Nông thôn
  - 🏛️ Di tích lịch sử
  - ⛩️ Chùa & Đền

- **Lọc theo mức giá:** Chọn mức giá: Tất cả mức giá, Tiết kiệm, Trung bình, hoặc Cao cấp.

**Bước 3:** Danh sách điểm đến hiện ra dưới dạng **lưới thẻ (cards)**. Mỗi thẻ hiển thị:
- Hình ảnh minh hoạ
- Tên điểm đến
- Thành phố/Tỉnh
- Danh mục (biển, núi, v.v.)
- Mức giá
- Đánh giá trung bình (số sao) và số lượt đánh giá

**Bước 4:** Bấm vào một thẻ điểm đến để xem **trang chi tiết** của điểm đến đó. Trang chi tiết bao gồm:
- Bộ sưu tập hình ảnh
- Mô tả chi tiết
- Bản đồ vị trí (hiển thị trên OpenStreetMap)
- Danh sách hoạt động có thể tham gia
- Tiện ích và ẩm thực đặc trưng
- Thời điểm tốt nhất để ghé thăm
- Các đánh giá từ người dùng khác

**Bước 5:** Tại trang chi tiết, người dùng có thể:
- **Lưu điểm đến:** Bấm biểu tượng **trái tim (❤️)** để lưu vào danh sách yêu thích.
- **Viết đánh giá:** Cuộn xuống phần đánh giá, chọn số sao (1-5), nhập tiêu đề và nội dung nhận xét, rồi bấm **"Gửi đánh giá"**.
- **Thêm vào lịch trình:** Bấm nút để thêm điểm đến vào một lịch trình du lịch.

---

### 4.6. Xem bản đồ (Explore)

**Bước 1:** Bấm menu **"Bản Đồ"** trên thanh điều hướng.

**Bước 2:** Trang bản đồ toàn màn hình hiện ra, hiển thị tất cả các điểm đến du lịch trên **bản đồ OpenStreetMap**. Mỗi điểm đến được đánh dấu bằng một **marker** (biểu tượng ghim).

**Bước 3:** Sử dụng bản đồ:
- **Phóng to/thu nhỏ:** Dùng nút **+/−** ở góc bản đồ hoặc cuộn chuột.
- **Di chuyển:** Kéo thả bản đồ bằng chuột để di chuyển đến vùng muốn xem.
- **Bấm vào marker:** Bấm vào biểu tượng ghim trên bản đồ để xem thông tin tóm tắt của điểm đến (tên, hình ảnh, đánh giá).

**Bước 4:** Sử dụng **bộ lọc danh mục** ở phía trên bản đồ để chỉ hiện các điểm đến thuộc danh mục nhất định (Biển, Núi, Khu vui chơi, v.v.).

**Bước 5:** Bấm vào thông tin popup của điểm đến để chuyển đến trang chi tiết.

---

### 4.7. Khám phá Tour du lịch

**Bước 1:** Bấm menu **"Tours"** trên thanh điều hướng.

**Bước 2:** Trang Tours hiện ra với phần **banner ảnh lớn** (TourShowcase) xoay vòng tự động giới thiệu các tour nổi bật. Bấm vào tour trên banner để xem chi tiết.

**Bước 3:** Cuộn xuống để xem **danh sách tour**. Sử dụng các bộ lọc:
- **Lọc theo danh mục:** Tất cả, Biển & Đảo, Núi rừng, Di sản, Thành phố.
- **Lọc theo mức giá:** Mọi mức giá, Tiết kiệm, Tầm trung, Cao cấp.
- **Sắp xếp:** Đánh giá cao nhất, Nhiều đánh giá, Xem nhiều nhất, Chi phí thấp nhất.

**Bước 4:** Bấm vào một tour để mở **modal chi tiết** hiển thị:
- Hình ảnh tour
- Mô tả lịch trình chi tiết
- Bản đồ các điểm đến trong tour
- Giá tham khảo
- Đánh giá từ người dùng

**Bước 5:** Trong modal chi tiết tour, người dùng có thể:
- **Lưu tour:** Bấm nút lưu (trái tim) để thêm tour vào danh sách đã lưu.
- **Xem trên bản đồ:** Chuyển sang tab bản đồ để xem vị trí các điểm đến.
- **Đánh giá tour:** Viết đánh giá và chấm điểm cho tour.

---

### 4.8. Quiz Gợi ý thông minh (SmartSuggestion)

Đây là tính năng đặc biệt giúp AI hiểu sở thích của bạn qua 5 câu hỏi nhanh và đưa ra gợi ý cá nhân hoá.

**Bước 1:** Tại trang chủ, cuộn xuống phần **"Gợi Ý Thông Minh"** (có biểu tượng ✨ Tính năng mới). Bấm nút **"🎯 Bắt đầu khám phá sở thích"**.

**Bước 2 — Câu hỏi 1: Phong cách du lịch**
- Câu hỏi: **"Bạn thích phong cách du lịch nào?"**
- Chọn một hoặc nhiều lựa chọn: Phiêu lưu, Thư giãn, Văn hóa, Ẩm thực, Thiên nhiên, Lịch sử.
- Mỗi lựa chọn được hiển thị dưới dạng thẻ có biểu tượng và mô tả ngắn. Bấm vào thẻ để chọn (thẻ đã chọn sẽ có viền tím và nền tím nhạt).
- Bấm **"Tiếp theo →"**.

**Bước 3 — Câu hỏi 2: Ngân sách**
- Câu hỏi: **"Ngân sách của bạn như thế nào?"**
- Chọn một mức: 💰 Tiết kiệm (dưới 2 triệu/người), 💵 Trung bình (2-5 triệu/người), 💎 Cao cấp (trên 5 triệu/người).
- Bấm **"Tiếp theo →"**.

**Bước 4 — Câu hỏi 3: Địa hình yêu thích**
- Câu hỏi: **"Bạn muốn đến đâu?"**
- Chọn một hoặc nhiều: 🏖️ Biển, 🏔️ Núi, 🌆 Thành phố, 🌾 Nông thôn, 🏛️ Di tích, 🍜 Ẩm thực.
- Bấm **"Tiếp theo →"**.

**Bước 5 — Câu hỏi 4: Thời gian du lịch**
- Câu hỏi: **"Bạn dự định đi bao lâu?"**
- Chọn một: 📅 1-2 ngày (cuối tuần), 🗓️ 3-5 ngày (nghỉ ngắn), 📆 6+ ngày (nghỉ dài).
- Bấm **"Tiếp theo →"**.

**Bước 6 — Câu hỏi 5: Đi cùng ai**
- Câu hỏi: **"Bạn đi cùng ai?"**
- Chọn một: 🧑 Một mình, 💑 Cặp đôi, 👨‍👩‍👧‍👦 Gia đình, 👥 Bạn bè.
- Bấm **"Xem kết quả"**.

**Bước 7 — Xem kết quả:**
- Màn hình hiện tổng hợp sở thích của bạn (phong cách, ngân sách, địa hình, thời gian, đi cùng ai).
- Bấm **"🤖 Nhận gợi ý từ AI"** để hệ thống tự động gửi thông tin sở thích đến AI Chat và nhận gợi ý lịch trình chi tiết.
- Nếu chưa đăng nhập, một hộp thoại đăng nhập/đăng ký sẽ hiện lên để bạn đăng nhập trước khi nhận gợi ý.
- (Tuỳ chọn) Bấm **"✓ Lưu vào profile"** để lưu sở thích vào tài khoản, giúp AI gợi ý tốt hơn trong tương lai.
- Bấm **"Làm lại"** nếu muốn trả lời lại.

---

### 4.9. Chat với AI

Đây là tính năng cốt lõi của TravelAI — cho phép bạn trò chuyện trực tiếp với trợ lý AI để nhận gợi ý du lịch.

**Bước 1:** Bấm menu **"AI Chat"** trên thanh điều hướng.

**Bước 2:** Giao diện chat hiện ra với 3 phần chính:
- **Thanh bên trái (Sidebar):** Hiển thị danh sách các cuộc trò chuyện trước đó (lịch sử chat). Bấm nút **"+ Cuộc hội thoại mới"** để bắt đầu cuộc chat mới.
- **Vùng chat giữa:** Hiển thị tin nhắn trao đổi giữa bạn và AI. Tin nhắn chào mừng của AI sẽ hiện đầu tiên.
- **Bản đồ bên phải (tuỳ chọn):** Khi AI gợi ý điểm đến, bản đồ sẽ tự động hiện bên phải với các điểm đánh dấu vị trí.

**Bước 3 — Nhập câu hỏi:**
- Gõ câu hỏi vào ô nhập liệu ở phía dưới. Ví dụ:
  - *"Gợi ý điểm đến biển đẹp cho gia đình"*
  - *"Lịch trình Đà Nẵng 3 ngày với ngân sách 5 triệu"*
  - *"Ăn gì ngon ở Hội An?"*
  - *"Thời điểm nào đi Phú Quốc đẹp nhất?"*
- Bấm nút **gửi** (biểu tượng mũi tên) hoặc nhấn phím **Enter**.

**Bước 4:** Ngoài ra, bạn có thể bấm vào **câu hỏi gợi ý nhanh** (quick questions) hiển thị dưới ô nhập liệu:
- 🏖️ Gợi ý điểm đến biển đẹp
- 🏔️ Du lịch Sapa cần chuẩn bị gì?
- 💰 Lịch trình Đà Nẵng 3 ngày 5 triệu
- 🍜 Ăn gì ngon ở Hội An?
- 📅 Thời điểm nào đi Phú Quốc đẹp?

**Bước 5 — Nhận phản hồi AI:**
- AI sẽ trả lời theo thời gian thực (streaming) — bạn sẽ thấy câu trả lời xuất hiện từng chút một.
- Nếu AI gợi ý các điểm đến có trong hệ thống, **thẻ điểm đến mini** sẽ hiện bên dưới tin nhắn AI, bao gồm: hình ảnh, tên, thành phố, đánh giá sao. Bấm vào thẻ để xem chi tiết điểm đến.

**Bước 6 — Sử dụng nút "Chưa biết đi đâu?":**
- Nếu bạn chưa biết muốn đi đâu, bấm nút **"Chưa biết đi đâu?"** bên dưới ô chat.
- AI sẽ hiện một **form làm rõ** (ClarifyForm) ngay trong chat với các trường:
  - **Bạn muốn đi đâu?** — Chọn vùng miền hoặc nhập tỉnh/thành phố cụ thể.
  - **Đi mấy ngày?** — Chọn hoặc nhập số ngày.
  - **Ngân sách dự kiến?** — Chọn hoặc nhập số tiền.
  - **Đi mấy người?** — Chọn hình thức (Một mình, Cặp đôi, Gia đình, Nhóm bạn) hoặc nhập số người cụ thể.
  - **Bạn thích gì?** — Chọn nhiều sở thích (Biển, Núi, Ẩm thực, Văn hóa, Nghỉ dưỡng, v.v.).
- Sau khi điền xong, bấm **"Gửi"** để AI nhận thông tin và đưa ra gợi ý phù hợp.

**Bước 7 — Lưu lịch trình từ AI:**
- Nếu AI đưa ra lịch trình chi tiết (ví dụ: lịch trình 3 ngày ở Đà Nẵng), một nút **"Lưu lịch trình"** sẽ xuất hiện bên dưới tin nhắn.
- Bấm nút đó, một hộp thoại hiện ra cho phép bạn:
  - Đặt **tiêu đề** cho lịch trình (hệ thống tự động gợi ý tiêu đề thông minh).
  - Chọn **ngày bắt đầu** và **ngày kết thúc**.
  - Chỉnh sửa **mô tả**.
- Bấm **"Lưu"** để lưu lịch trình. Sau khi lưu thành công, một thông báo hiện ở góc màn hình cho biết số điểm đến đã tự động thêm vào lịch trình, kèm nút **"🗺️ Xem bản đồ hành trình →"**.

**Bước 8 — Quản lý lịch sử chat:**
- Bấm vào cuộc trò chuyện trong danh sách bên trái để xem lại nội dung đã chat trước đó.
- Bấm biểu tượng **xoá (🗑️)** bên cạnh tên cuộc trò chuyện để xoá.
- Bấm **"+ Cuộc hội thoại mới"** để bắt đầu chủ đề mới.

> **Lưu ý:** Nếu AI phản hồi chậm hoặc bị lỗi, bấm nút **"Thử lại"** để gửi lại câu hỏi. Bấm nút **"Dừng"** nếu muốn huỷ câu hỏi đang xử lý.

---

### 4.10. Quản lý lịch trình

**Bước 1:** Bấm menu **"Lịch Trình"** trên thanh điều hướng.

**Bước 2:** Trang lịch trình hiển thị danh sách các lịch trình du lịch mà bạn đã tạo (từ AI hoặc tự tạo). Mỗi lịch trình hiện:
- Tiêu đề
- Ngày bắt đầu — ngày kết thúc
- Số lượng điểm đến
- Trạng thái (đang lên kế hoạch, đã hoàn thành, v.v.)

**Bước 3:** Bấm vào một lịch trình để xem **trang chi tiết lịch trình**. Trang này hiển thị:
- **Bản đồ hành trình (ItineraryMap):** Hiển thị tất cả điểm đến trên bản đồ với đường nối theo thứ tự.
- **Danh sách điểm đến:** Liệt kê từng điểm đến theo ngày/thứ tự, kèm ghi chú và hoạt động.
- **Thông tin chung:** Mô tả, ngày bắt đầu/kết thúc.

**Bước 4:** Tại trang chi tiết lịch trình, bạn có thể:
- **Thêm điểm đến:** Bấm nút thêm để bổ sung điểm đến vào lịch trình.
- **Chỉnh sửa:** Thay đổi thứ tự, ghi chú, ngày cho từng điểm đến.
- **Xoá:** Xoá điểm đến khỏi lịch trình hoặc xoá toàn bộ lịch trình.
- **Dẫn đường:** Bấm nút **"Dẫn đường"** để mở tính năng dẫn đường thực tế (xem mục 4.11).

---

### 4.11. Dẫn đường thực tế (Navigation)

**Bước 1:** Từ trang chi tiết lịch trình hoặc tour, bấm nút **"Dẫn đường"**.

**Bước 2:** Trang dẫn đường toàn màn hình hiện ra, hiển thị:
- **Bản đồ thời gian thực** với vị trí hiện tại của bạn (cần cấp quyền truy cập GPS cho trình duyệt).
- **Tuyến đường** từ vị trí hiện tại đến các điểm đến trong lịch trình.
- **Thông tin dẫn đường** (khoảng cách, thời gian ước tính).

**Bước 3:** Bản đồ sẽ tự động cập nhật theo vị trí GPS của bạn. Khi bạn đến gần điểm đến, hệ thống sẽ hiển thị thông báo.

**Bước 4:** Khi đã đến đích, một **overlay hoàn thành** sẽ hiện ra, cho phép bạn:
- Đánh giá điểm đến vừa ghé thăm.
- Chuyển sang điểm đến tiếp theo.

> **Lưu ý:** Tính năng dẫn đường cần trình duyệt hỗ trợ GPS (tốt nhất trên điện thoại di động). Nếu vào trực tiếp trang `/navigate` mà không có dữ liệu, hệ thống sẽ hiện thông báo hướng dẫn quay lại lịch trình.

---

### 4.12. Điểm đến đã lưu

**Bước 1:** Bấm vào **tên người dùng** trên thanh điều hướng, chọn **"❤️ Đã lưu"** từ menu xổ xuống.

**Bước 2:** Trang hiển thị danh sách các điểm đến và tour mà bạn đã lưu (bấm trái tim). Mỗi mục hiện:
- Hình ảnh
- Tên điểm đến/tour
- Vị trí
- Danh mục
- Đánh giá
- Trạng thái tour (đang lên kế hoạch, đang đi, đã hoàn thành)

**Bước 3:** Bấm vào một mục để xem chi tiết.

**Bước 4:** Bấm **nút xoá** (biểu tượng thùng rác) để bỏ mục khỏi danh sách đã lưu.

---

### 4.13. Quản lý tài khoản cá nhân (Profile)

**Bước 1:** Bấm vào **tên người dùng** trên thanh điều hướng, chọn **"👤 Tài khoản"**.

**Bước 2:** Trang profile hiện ra với các tab:

**Tab "Thông tin" (mặc định):**
- Hiển thị ảnh đại diện, tên, email.
- Thống kê: Số điểm đến đã lưu, số lịch trình, số đánh giá.
- Bấm **"Chỉnh sửa"** để chuyển sang chế độ chỉnh sửa:
  - Thay đổi **tên hiển thị**.
  - Thay đổi **ảnh đại diện**: Bấm vào ảnh đại diện để chọn ảnh mới từ máy tính.
  - Cập nhật **sở thích du lịch**:
    - Phong cách: Chọn nhiều từ Phiêu lưu, Thư giãn, Văn hóa, Ẩm thực, Thiên nhiên, Lịch sử.
    - Ngân sách: Chọn một mức (Tiết kiệm, Trung bình, Cao cấp).
    - Sở thích: Chọn nhiều từ Biển, Núi, Thành phố, Nông thôn, Di tích, Ẩm thực, Mua sắm, Chụp ảnh.
  - Bấm **"Lưu thay đổi"** để cập nhật, hoặc **"Huỷ"** để bỏ qua.

**Bước 3:** Bấm nút **"🚪 Đăng xuất"** để thoát tài khoản.

---

### 4.14. Bạn bè và Nhắn tin

**Bước 1 — Bạn bè:** Bấm vào tên người dùng trên thanh điều hướng, chọn **"👥 Bạn bè"**.
- Trang hiện danh sách bạn bè hiện tại.
- Bấm **"Thêm bạn"** để tìm kiếm và gửi lời mời kết bạn.
- Bấm vào tên bạn bè để xem thông tin hoặc bắt đầu nhắn tin.

**Bước 2 — Nhắn tin:** Bấm **"💬 Nhắn tin"** từ menu người dùng.
- Trang nhắn tin hiện danh sách các cuộc hội thoại.
- Bấm vào cuộc hội thoại để xem và gửi tin nhắn.
- Bấm **"Cuộc trò chuyện mới"** để bắt đầu nhắn tin với bạn bè.

---

## 5. Hướng dẫn sử dụng dành cho Quản trị viên (Admin)

> **Lưu ý:** Chỉ tài khoản có quyền admin mới truy cập được trang quản trị. Tài khoản admin mặc định được tạo bằng lệnh `npm run seed:admin`.

### 5.1. Truy cập trang quản trị

**Bước 1:** Đăng nhập bằng tài khoản admin.

**Bước 2:** Bấm vào **tên người dùng** trên thanh điều hướng, chọn **"⚙️ Quản trị"** từ menu xổ xuống. Mục này chỉ hiện khi tài khoản có quyền admin.

**Bước 3:** Trang quản trị hiện ra với **thanh menu bên trái** gồm các mục:

| Mục | Biểu tượng | Mô tả |
|-----|-----------|-------|
| Dashboard | 📊 | Bảng tổng quan thống kê |
| Điểm đến | 🏝️ | Quản lý danh sách điểm đến |
| Tour | 🧳 | Quản lý tour du lịch |
| Đánh giá | ⭐ | Quản lý đánh giá người dùng |
| Lịch trình | 🗺️ | Quản lý lịch trình |
| Người dùng | 👥 | Quản lý tài khoản người dùng |
| Chat history | 💬 | Xem lịch sử chat AI |

---

### 5.2. Dashboard tổng quan

**Bước 1:** Sau khi vào trang quản trị, mặc định hiển thị trang **Dashboard**.

**Bước 2:** Dashboard hiển thị các thông số thống kê:
- **Thẻ thống kê nhanh (Stat Cards):** Tổng số người dùng, tổng số điểm đến, tổng số đánh giá, tổng số lịch trình.
- **Biểu đồ tăng trưởng người dùng:** Đồ thị dạng area chart hiện số người dùng mới đăng ký theo ngày.
- **Biểu đồ đánh giá:** Số đánh giá mới theo ngày.
- **Phân bố danh mục (CategoryDonut):** Biểu đồ tròn hiện tỷ lệ điểm đến theo danh mục.
- **Phân bố rating (Rating Distribution):** Biểu đồ cột hiện số lượng đánh giá theo số sao (1-5).
- **Top điểm đến phổ biến:** Danh sách các điểm đến được xem/đánh giá nhiều nhất.

**Bước 3:** Sử dụng **bộ lọc ngày (DateRangePicker)** ở góc trên bên phải để thay đổi khoảng thời gian thống kê (7, 14, 30, 90 ngày).

**Bước 4:** Bấm vào một điểm dữ liệu trên biểu đồ để xem chi tiết (drill-down). Ví dụ, bấm vào cột ngày trên biểu đồ tăng trưởng để xem danh sách người dùng đăng ký trong ngày đó.

**Bước 5:** Sử dụng **Quick Actions** (hành động nhanh) để:
- Thêm điểm đến mới
- Xem danh sách đánh giá chờ duyệt
- Xuất báo cáo

---

### 5.3. Quản lý điểm đến

**Bước 1:** Bấm menu **"Điểm đến"** ở thanh bên trái.

**Bước 2:** Danh sách điểm đến hiện ra dưới dạng bảng, mỗi dòng gồm:
- Hình ảnh thu nhỏ
- Tên điểm đến
- Thành phố
- Danh mục
- Mức giá
- Đánh giá trung bình
- Ngày tạo

**Bước 3 — Thêm điểm đến mới:**
- Bấm nút **"+ Thêm điểm đến"**.
- Điền form: Tên, mô tả, thành phố, quốc gia, toạ độ (lat/lng), hình ảnh, danh mục, mức giá, tiện ích, hoạt động, ẩm thực đặc trưng, thời điểm tốt nhất để ghé thăm.
- Bấm **"Lưu"** để tạo.

**Bước 4 — Chỉnh sửa điểm đến:**
- Bấm biểu tượng **bút chì (✏️)** hoặc bấm vào tên điểm đến trên bảng.
- Chỉnh sửa thông tin cần thiết.
- Bấm **"Cập nhật"**.

**Bước 5 — Xoá điểm đến:**
- Bấm biểu tượng **thùng rác (🗑️)** ở cuối dòng.
- Xác nhận xoá trong hộp thoại.

---

### 5.4. Quản lý Tour

**Bước 1:** Bấm menu **"Tour"** ở thanh bên trái.

**Bước 2:** Hiển thị danh sách các tour du lịch trong hệ thống.

**Bước 3:** Thực hiện thêm, sửa, xoá tour tương tự như quản lý điểm đến (xem mục 5.3).

---

### 5.5. Quản lý đánh giá

**Bước 1:** Bấm menu **"Đánh giá"** ở thanh bên trái.

**Bước 2:** Danh sách đánh giá hiện ra, mỗi dòng gồm:
- Tên người đánh giá
- Điểm đến được đánh giá
- Số sao
- Nội dung nhận xét
- Ngày tạo

**Bước 3 — Xoá đánh giá vi phạm:**
- Bấm biểu tượng **thùng rác (🗑️)** ở dòng đánh giá cần xoá.
- Xác nhận xoá.

---

### 5.6. Quản lý lịch trình

**Bước 1:** Bấm menu **"Lịch trình"** ở thanh bên trái.

**Bước 2:** Hiển thị danh sách tất cả lịch trình của người dùng trong hệ thống. Admin có thể xem và quản lý các lịch trình.

---

### 5.7. Quản lý người dùng

**Bước 1:** Bấm menu **"Người dùng"** ở thanh bên trái.

**Bước 2:** Danh sách người dùng hiện ra, mỗi dòng gồm:
- Ảnh đại diện
- Tên
- Email
- Vai trò (user / admin)
- Ngày đăng ký

**Bước 3 — Xoá tài khoản:**
- Bấm biểu tượng **thùng rác (🗑️)** ở dòng người dùng cần xoá.
- Xác nhận xoá trong hộp thoại.

> **Lưu ý:** Hãy cẩn thận khi xoá tài khoản vì thao tác này không thể hoàn tác. Tất cả dữ liệu liên quan (lịch trình, đánh giá, lịch sử chat) của người dùng đó có thể bị ảnh hưởng.

---

### 5.8. Lịch sử chat AI

**Bước 1:** Bấm menu **"Chat history"** ở thanh bên trái.

**Bước 2:** Hiển thị danh sách tất cả cuộc trò chuyện giữa người dùng và AI, bao gồm:
- Tên người dùng
- Tiêu đề cuộc chat
- Tin nhắn cuối cùng
- Thời gian tạo

**Bước 3:** Bấm vào một cuộc chat để xem toàn bộ nội dung hội thoại.

---

## 6. Các lưu ý quan trọng

### 6.1. Về kết nối

- Chương trình yêu cầu **kết nối Internet** để hoạt động bình thường vì cơ sở dữ liệu và dịch vụ AI đều chạy trên đám mây.
- Nếu mất kết nối, một số tính năng (AI chat, tải dữ liệu điểm đến, bản đồ) sẽ không hoạt động.

### 6.2. Về hiệu suất AI

- Lần đầu gửi câu hỏi cho AI có thể mất vài giây do server cần khởi động (cold start). Các lần sau sẽ nhanh hơn.
- AI trả lời bằng tiếng Việt và được huấn luyện chuyên về du lịch Việt Nam.
- Nếu AI phản hồi quá lâu (hơn 60 giây), hệ thống sẽ tự động hiện thông báo lỗi timeout. Bấm **"Thử lại"** để gửi lại.

### 6.3. Về bảo mật

- Mật khẩu được mã hoá (hash) trước khi lưu vào cơ sở dữ liệu, đảm bảo an toàn.
- Phiên đăng nhập sử dụng JWT (JSON Web Token) có thời hạn. Nếu token hết hạn, hệ thống sẽ yêu cầu đăng nhập lại.
- Không chia sẻ thông tin đăng nhập cho người khác.

### 6.4. Về dữ liệu

- Dữ liệu điểm đến và ẩm thực được khởi tạo sẵn bằng seed script. Admin có thể thêm, sửa, xoá thêm dữ liệu qua trang quản trị.
- Lịch sử chat AI được lưu tự động khi người dùng đã đăng nhập.
- Lịch trình lưu từ AI sẽ tự động trích xuất và liên kết các điểm đến có trong cơ sở dữ liệu.

### 6.5. Về trình duyệt

- Chương trình hoạt động tốt nhất trên các trình duyệt hiện đại: Google Chrome, Microsoft Edge, Mozilla Firefox phiên bản mới nhất.
- Giao diện được thiết kế **responsive** — tương thích với cả máy tính và thiết bị di động.
- Tính năng dẫn đường (Navigation) cần quyền truy cập GPS trên trình duyệt.

### 6.6. Về port mặc định

| Dịch vụ | Địa chỉ mặc định |
|---------|------------------|
| **Frontend** (giao diện web) | http://localhost:3000 |
| **Backend** (API server) | http://localhost:5001 |
| **Swagger API Docs** | http://localhost:5001/api-docs |

---

*Tài liệu hướng dẫn sử dụng — Đồ án tốt nghiệp TravelAI*
*Hệ thống gợi ý du lịch thông minh sử dụng trí tuệ nhân tạo*
