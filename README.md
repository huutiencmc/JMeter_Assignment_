##Báo cáo kiểm thử hiệu năng bằng JMeter

-Thông tin sinh viên

-Họ tên: Nguyễn Hữu Tiến

-MSSV: 220225

-Website được kiểm thử: https://www.wikipedia.org

##Mô tả kịch bản kiểm thử

**Kịch bản 1: Cơ bản**

-Số lượng người dùng: 10 + (220225 % 10) = 15

-Hành vi: Gửi yêu cầu GET đến https://www.wikipedia.org

-Loop Count: 5

**Kịch bản 2: Tải nặng**

-Số lượng người dùng: 50 + (220225 % 20) = 55

-Ramp-up Period: 30 giây

-Hành vi: Gửi yêu cầu GET đến https://www.wikipedia.org và https://en.wikipedia.org/wiki/Help:Contents

**Kịch bản 3: Tùy chỉnh**

-Số lượng người dùng: 20 + (220225 % 15) = 25

-Thời gian chạy: 60 giây

-Hành vi: Gửi yêu cầu GET đến https://en.wikipedia.org/wiki/Main_Page và https://en.wikipedia.org/wiki/Special:Random?student_id=${StudentID}

##Kết quả kiểm thử
**Kịch bản 1:**

-Response Time trung bình: 724 ms

-Throughput: 0.02071 yêu cầu/giây

-Error Rate: 0.000%

**Kịch bản 2:**

-Response Time trung bình: 600 ms

-Throughput: 14.816 yêu cầu/giây

-Error Rate: 0.000%

**Kịch bản 3:**

-Response Time trung bình: 1258 ms

-Throughput: 0.02072 yêu cầu/giây

-Error Rate: 0.000%

##Nhận xét
-Website Wikipedia có hiệu năng ổn định, không xuất hiện lỗi trong cả ba kịch bản.

-Ở kịch bản tải nặng, hệ thống vẫn duy trì được tốc độ phản hồi khá tốt với throughput cao.

-Kịch bản tùy chỉnh có thời gian phản hồi cao hơn, có thể do tải tăng dần theo thời gian chạy.

-Nhìn chung, website có khả năng chịu tải tốt trong phạm vi kiểm thử.

