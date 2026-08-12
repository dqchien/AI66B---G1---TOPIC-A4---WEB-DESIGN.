# CONCERTLY — Online Concert Ticketing Platform

## 1. Giới thiệu đề tài

Đề tài A4: Trang bán khóa học / vé sự kiện online, được cụ thể hóa thành website bán vé concert các nhóm nhạc.

**CONCERTLY** là website bán vé concert trực tuyến, tập trung vào trải nghiệm tìm kiếm sự kiện, lựa chọn ghế, mua vé và quản lý vé sau khi đăng nhập.

Website mô phỏng một hệ thống bán vé concert thực tế, trong đó người dùng có thể xem thông tin nghệ sĩ/sự kiện, lựa chọn vị trí trên sơ đồ chỗ ngồi, thanh toán online và nhận vé điện tử.

---

## 2. Bài toán

Vé concert là sản phẩm số có số lượng giới hạn (theo hạng ghế/khu vực), nhiều người có thể cùng đặt một vé tại một thời điểm. Hệ thống cần đảm bảo:

- Không bán trùng một ghế cho hai người, đồng thời xử lý tranh chấp khi nhiều người cùng đặt một ghế.
- Giữ chỗ tạm thời trong lúc người dùng thanh toán, tự hủy giữ chỗ nếu hết hạn.
- Quản lý đơn hàng: trạng thái chờ thanh toán / đã thanh toán / đã hủy.
- Người dùng có thể xem và quản lý các vé đã mua trong mục My Tickets sau khi đăng nhập.

---

## 3. Các tính năng chính

### 3.1. Concert Discovery

- Danh sách concert đang mở bán/sắp diễn ra.
- Tìm kiếm và lọc theo nghệ sĩ, thời gian, giá vé.
- Concert nổi bật và concert đang được quan tâm.
- Countdown đến thời điểm mở bán hoặc ngày diễn ra.

### 3.2. Concert Detail

Trang thông tin chi tiết của concert:

- Nghệ sĩ / line-up.
- Thời gian và địa điểm tổ chức.
- Thông tin về venue.
- Giá vé theo từng khu vực / hạng ghế.
- Sơ đồ sân khấu và khu vực ghế.
- Số lượng vé còn lại theo từng khu vực / hạng vé.
- Điều khoản và quy định của concert.

### 3.3. Interactive Seat Selection

Người dùng chọn ghế trực tiếp trên **sơ đồ chỗ ngồi**.

- Hiển thị khu vực VIP / A / B / C.
- Ghế đã bán không thể chọn.
- Ghế đang được người khác giữ được đánh dấu riêng.
- Hover vào ghế để xem thông tin và giá vé.
- Tổng tiền cập nhật realtime khi người dùng chọn hoặc bỏ chọn ghế.

### 3.4. Ticket Hold & Seat Conflict Prevention

Sau khi chọn ghế:

- Ghế được giữ tạm thời trong **5 phút**.
- Countdown thời gian giữ vé.
- Nếu thanh toán thành công → ghế được xác nhận và chuyển sang trạng thái Sold.
- Nếu hết thời gian → ghế tự động được trả lại và chuyển về trạng thái Available.
- Không cho phép hai người cùng xác nhận mua một ghế.

### 3.5. Mock Payment

Mô phỏng quy trình thanh toán:

`Seat Selection → Order Summary → Payment → Success`

Có thể mô phỏng các phương thức:

- Credit/Debit Card.
- E-wallet.
- Bank Transfer.

Sau khi thanh toán thành công, đơn hàng được cập nhật sang trạng thái Paid và vé được xác nhận.

Hệ thống chỉ mô phỏng quy trình thanh toán và không thực hiện giao dịch tiền thật.

### 3.6. Digital Ticket & QR Code

Sau khi thanh toán thành công:

- Tạo vé điện tử.
- Hiển thị thông tin concert, ghế và mã vé.
- Sinh **QR Code duy nhất** cho mỗi vé.
- Vé có trạng thái `Valid / Used`.
- Cho phép người dùng xem vé điện tử trong mục My Tickets.

Admin có thể sử dụng QR Code để kiểm tra và xác thực vé tại sự kiện.

### 3.7. My Tickets & Orders

Sau khi đăng nhập, người dùng có thể:

- Xem concert sắp tham dự.
- Xem vé đã mua.
- Xem QR Code.
- Xem lịch sử đơn hàng.

### 3.8. Admin Dashboard

Admin có thể:

- Quản lý concert và thông tin nghệ sĩ.
- Quản lý khu vực / ghế và số lượng vé.
- Quản lý đơn hàng và trạng thái thanh toán.
- Quản lý người dùng.
- Theo dõi số lượng vé đã bán và doanh thu.
- Xem thống kê bán vé theo concert và khu vực.

---

## 4. Các màn hình dự kiến

### User

1. **Home**
   - Concert nổi bật
   - Trending
   - Upcoming concerts

2. **Explore Concerts**
   - Search
   - Filter
   - Danh sách concert

3. **Concert Detail**
   - Thông tin concert
   - Line-up
   - Venue
   - Giá vé
   - Seat map

4. **Seat Selection**
   - Interactive seat map
   - Chọn ghế
   - Countdown giữ vé
   - Tổng tiền

5. **Checkout**
   - Thông tin vé
   - Ghế đã chọn
   - Tổng tiền
   - Phương thức thanh toán
   - Xác nhận đơn hàng
   - Payment Success
   - Mã đơn hàng
   - Link tới vé

6. **My Tickets**
   - Danh sách vé
   - QR Code
   - Thông tin concert
   - Mã vé

7. **Profile & Orders**
   - Thông tin cá nhân
   - Lịch sử đơn hàng
   - Trạng thái thanh toán

### Admin

8. **Admin Dashboard**
   - Tổng quan doanh thu
   - Vé đã bán
   - Concert đang hoạt động
   - Quản lý concert
   - Quản lý khu vực / ghế
   - Quản lý đơn hàng
   - Check-in và xác thực QR Code

---

## 5. User Flow chính

```text
Home
  ↓
Explore Concerts
  ↓
Concert Detail
  ↓
Seat Selection
  ↓
Hold Seat (5 minutes)
  ↓
Checkout
  ├─ Order Summary
  └─ Mock Payment
  ↓
Payment Success
  ↓
My Tickets
  └─ Digital Ticket + QR Code
```

### Admin Check-in Flow

```text
Admin Dashboard
  ↓
Check-in
  ↓
Enter / Scan QR Code
  ↓
Validate Ticket
  ↓
Valid → Mark as Used
```
