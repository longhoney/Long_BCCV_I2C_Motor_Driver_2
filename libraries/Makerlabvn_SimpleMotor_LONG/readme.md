KHảo sát lại cách điều khiển động cơ (19/05/2026)
================
### Quy ước

1. Thông số tốc độ: **0-100%** --> analogWrite() 0-255
2. Thông số chiều quay thuận: **1** = Quay thuận chiều kim đồng hồ - xe đi tới. -->  digitalWrite(IN2,1); digitalWrite(IN1,0)
3. Thông số chiều quay ngược: **0** = Quay ngược chiều kim đồng hồ - xe đi lùi. --> digitalWrite(IN2,0); digitalWrite(IN1,1)

<img width="974" height="469" alt="Image" src="https://github.com/user-attachments/assets/973f00b8-4a2d-416e-be78-ed209678afe1" />

4. Dựa theo chú thích trên các mẫu driver phổ biến: Kênh A là motor bên trái, kênh B là motor bên phải
5. Quy ước cho MKE-Creator
<img width="1050" height="752" alt="Image" src="https://github.com/user-attachments/assets/32d34036-e4d2-4065-9a71-0eac56f71a4f" />

5. Quy ước cho L298

<img width="1056" height="484" alt="Image" src="https://github.com/user-attachments/assets/644791eb-c5ec-4065-8ea7-f3c9f8a78b27" />

6. Quy ước cho L9110

<img width="795" height="498" alt="Image" src="https://github.com/user-attachments/assets/48573e5f-2d96-4f1a-9e2b-1a0795e475a8" />

## Hàm điều khiển motor

> Điều khiển độc lập từng motor của từng kênh A hoặc B.

|Hàm|Chức năng|
|---|---------|
|**<span style="color:#E47128">motorA_fw(`speed`)**|Điều khiển motor A quay thuận.<br>- *speed:* tốc độ quay (0% ~ 100%).
|**<span style="color:#E47128">motorA_bw(`speed`)**|Điều khiển motor A quay ngược.<br>- *speed:* tốc độ quay (0% ~ 100%).
|**<span style="color:#E47128">motorA_stop()**|Điều khiển motor A dừng lại.
|-|-|
|**<span style="color:#E47128">motorB_fw(`speed`)**|Điều khiển motor B quay thuận.<br>- *speed:* tốc độ quay (0% ~ 100%).
|**<span style="color:#E47128">motorB_bw(`speed`)**|Điều khiển motor B quay ngược.<br>- *speed:* tốc độ quay (0% ~ 100%).
|**<span style="color:#E47128">motorB_stop()**|Điều khiển motor B dừng lại.

## Hàm điều khiển xe

> Điều khiển kết hợp 2 kênh A & B.

|Hàm|Chức năng|
|---|---------|
|**<span style="color:#E47128">car_fw(`speedA`, `speedB`)**|Điều khiển xe đi tới.<br>- *speedA:* tốc độ quay bánh Trái (0% ~ 100%).<br>- *speedA:* tốc độ quay bánh Phải (0% ~ 100%).
|**<span style="color:#E47128">car_bw(`speedA`, `speedB`)**|Điều khiển xe đi lùi.<br>- *speedA:* tốc độ quay bánh Trái (0% ~ 100%).<br>- *speedA:* tốc độ quay bánh Phải (0% ~ 100%).
|-|-|
|**<span style="color:#E47128">car_rotateL(`speed`)**|Điều khiển xe xoay trái.<br>- *speed:* tốc độ xe (0% ~ 100%).
|**<span style="color:#E47128">car_rotateR(`speed`)**|Điều khiển xe xoay phải.<br>- *speed:* tốc độ xe (0% ~ 100%).
|-|-|
|**<span style="color:#E47128">car_stop()**|Điều khiển xe dừng lại.

So sánh với thư viện: https://docs.google.com/spreadsheets/d/1pauv_eXI9WxPK2DNi59jDcf7WH-pYOTJTPTRPNfatLw/edit?usp=sharing
