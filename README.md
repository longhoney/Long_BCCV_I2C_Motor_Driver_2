# Long_BCCV_I2C_Motor_Driver_2
1. Thêm các thư viện cơ bản, hình ảnh và chương trình mẫu
2. Đặt câu hỏi định hướng
    - Nhánh điều khiển: (MASTER) [Uno] <<< I2C >>> (SLAVE) [STC8 <<< PWM >>> L9110] <<< Power >>> DC Motor
    - Ta cần viết chương trình theo đúng tính năng của MKE-M17: Slave nhận lệnh từ Master và điều khiển động cơ. Tôi dần nhận ra khi đang khảo sát kiểu truyền nhận
    - Chương trình Master truyền lệnh đã có sẵn trong thư mục chương trình mẫu của Thư viện Makerlabvn_I2C_Motor_Driver
3. Tạo thư viện Makerlabvn_SimpleMotor_LONG
    - Đổi tên đối tượng L298 4pin -> L9110
    - Bổ sung lệnh cấu hình chân ENA, ENB dạng OUTPUT
    - Tắt 2 lệnh cal_speed(speedA, speedB) trong 2 hàm car_fw() và car_bw()
    - Tổng hợp tại [Google Sheet](https://docs.google.com/spreadsheets/d/1pauv_eXI9WxPK2DNi59jDcf7WH-pYOTJTPTRPNfatLw/edit?usp=sharing)
    - Chờ thử lại với [MKE Creator V2](https://hshop.vn/mach-makeredu-creator-arduino-uno-compatible)
