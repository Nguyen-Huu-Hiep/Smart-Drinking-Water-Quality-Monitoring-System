# Smart Drinking Water Quality Monitoring System

## 📌 Giới thiệu
Dự án **Đo chất lượng nước uống thông minh** được thực hiện trong khuôn khổ
môn học *Cảm biến và Đo lường thông minh*, với mục tiêu thiết kế một hệ thống
đo lường nhỏ gọn, chi phí thấp nhưng có khả năng giám sát chất lượng nước
theo thời gian thực.

Hệ thống ứng dụng cảm biến, vi điều khiển ESP32 và công nghệ IoT để đo,
xử lý, hiển thị và truyền dữ liệu các thông số quan trọng của nước uống,
góp phần bảo vệ sức khỏe cộng đồng.

## 🎯 Mục tiêu
- Đo và giám sát các chỉ tiêu chất lượng nước: **TDS, EC và nhiệt độ**.
- Xử lý tín hiệu đo, bù ảnh hưởng nhiệt độ để tăng độ chính xác.
- Hiển thị dữ liệu trực quan trên **màn hình OLED**.
- Truyền dữ liệu lên nền tảng **IoT** để theo dõi từ xa.
- Phân tích và cảnh báo chất lượng nước dựa trên **tiêu chuẩn WHO**.

## 🏗️ Kiến trúc hệ thống
Hệ thống gồm các khối chức năng chính:
- **Cảm biến**: TDS Sensor V1.0, DS18B20 (nhiệt độ).
- **Bộ xử lý trung tâm**: ESP32.
- **Hiển thị cục bộ**: Màn hình OLED 0.96”.
- **Kết nối IoT**: WiFi, Web/App giám sát.
- **Khối cảnh báo**: LED / thông báo khi vượt ngưỡng cho phép.
  <img width="542" height="325" alt="image" src="https://github.com/user-attachments/assets/4becc7bf-3b53-4126-9710-e95f7030a8a7" />
Nguyên lý hoạt động:
Cảm biến → ESP32 xử lý & bù nhiệt → Hiển thị → Gửi dữ liệu IoT → Cảnh báo.

## 🧠 Thuật toán & xử lý tín hiệu
- Chuyển đổi ADC từ tín hiệu analog của cảm biến TDS.
- Bù nhiệt độ cho độ dẫn điện (EC) để tính TDS chính xác.
- Lọc nhiễu (Median / Average) nhằm ổn định giá trị đo.
- Phân loại mức độ chất lượng nước theo ngưỡng TDS.

## 🖥️ Chức năng chính
- Giám sát thời gian thực TDS và nhiệt độ nước.
- Hiển thị trực quan dữ liệu trên OLED.
- Ghi nhận và truyền dữ liệu lên nền tảng IoT.
- Cảnh báo khi chất lượng nước không đạt chuẩn.
- Hỗ trợ mở rộng thêm các cảm biến khác (pH, độ đục…).

## 🛠️ Công nghệ sử dụng
- **ESP32**
- **Cảm biến TDS Sensor V1.0**
- **Cảm biến nhiệt độ DS18B20**
- **Màn hình OLED SSD1306**
- **Arduino IDE / IoT Cloud**
- **WiFi & IoT**

  <img width="596" height="442" alt="image" src="https://github.com/user-attachments/assets/608add91-1293-4aff-97cf-6ec9847ac004" />

## 👥 Nhóm thực hiện
- **Nguyễn Hữu Hiệp**  
- **Nguyễn Minh Ngọc Huy**  
- **Lê Công Khoa**  
- **Quý Tâm Anh**

📍 Lớp: 21PFIEV2  
📍 Khoa: Khoa học Công nghệ Tiên tiến  
📍 Trường: Đại học Bách Khoa – Đại học Đà Nẵng  

## 👨‍🏫 Giảng viên hướng dẫn
**TS. Lê Quốc Huy**

## 📅 Thời gian thực hiện
Tháng 9 năm 2025

## 📚 Tiêu chuẩn & tham khảo
- WHO – Guidelines for Drinking-water Quality
- QCVN 01-1:2024/BYT
- Datasheet ESP32, DS18B20, TDS Sensor
