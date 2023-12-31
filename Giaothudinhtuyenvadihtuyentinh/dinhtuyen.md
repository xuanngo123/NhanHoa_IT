﻿- Đinh tuyến là gì? Tại sao cần định tuyến?
- Phân loại định tuyến
- Các giao thức định tuyến động căn bản
- Thực hành định tuyến tĩnh
![đg](https://github.com/xuanngo123/NhanHoa_IT/assets/97582215/c0046d73-9a5b-4c89-8456-dd4e56b7d561)
##1. Định tuyến là gì ?

Trong ngành mạng máy tính, định tuyến (tiếng Anh: routing hay routeing) là quá trình chọn lựa các đường đi trên một mạng máy tính để gửi dữ liệu qua đó. Việc định tuyến được thực hiện cho nhiều loại mạng, trong đó có mạng điện thoại, liên mạng, Internet, mạng giao thông.

***Tại sao cần giao thức định tuyến:***

Trong một mạng rất lớn có rất nhiều router như mạng Internet, việc cập nhật bảng định tuyến bằng tay là không thể, vì vậy cần phải có giao thức định tuyến, giao thức định tuyến thực hiện các công việc sau:

- Chọn đường dẫn tốt nhất cho các gói tin
- Cung cấp các tiến trình để chia sẻ thông tin định tuyến
- Cho phép router liên lạc với các router khác để update và duy trì bảng định

##2. Phân loại định tuyến

Có nhiều tiêu chí để phân loại các giao thức định tuyến khác nhau. Định tuyến được phân chia thành 2 loại cơ bản:

- **Định tuyến tĩnh**: Việc xây dựng bảng định tuyến của router được thực hiện bằng tay bởi người quản trị.
- **Định tuyến động**: Việc xây dựng và duy trì trạng thái của bảng định tuyến được thực hiện tự động bởi router. Việc chọn đường đi được tuân thủ theo 2 thuật toán cơ bản:
- Distance vector: Chọn đường đi theo hướng và khoảng cách tới đích.
- Link State: Chọn đường đi ngắn nhất dựa vào cấu trúc của toàn bộ mạng theo trạng thái của các đường liên kết mạng.

###2.1 Định tuyến tĩnh

Định tuyến tĩnh là quá trình router thực hiện chuyển gói dữ liệu tới địa chỉ mạng đích dựa vào địa chỉ IP đích của gói dữ liệu. Để chuyển được gói dữ liệu đến đúng đích thì router phải học thông tin về đường đi tới các mạng khác. Thông tin về đường đi tới các mạng khác sẽ được người quản trị cấu hình cho router. Khi cấu trúc mạng thay đổi, người quản trị mạng phải tự thay đổi bảng định tuyến của router.

Kỹ thuật định tuyến tĩnh đơn giản, dễ thực hiện, ít hao tốn tài nguyên mạng và CPU xử lý trên router (do không phải trao đổi thông tin định tuyến và không phải tính toán định tuyến). Tuy nhiên kỹ thuật này không hội tụ với các thay đổi diễn ra trên mạng và không thích hợp với những mạng có quy mô lớn (khi đó số lượng route quá lớn, không thể khai báo bằng tay được).

- Ưu điểm:
- Sử dụng ít bandwidth hơn định tuyến động.
- Không tiêu tốn tài nguyên để tính toán và phân tích gói tin định tuyến.
- Nhược điểm:
- Không có khả năng tự động cập nhật đường đi.
- Phải cấu hình thủ công khi mạng có sự thay đổi.
- Phù hợp với mạng nhỏ, rất khó triển khai trên mạng lớn.
- Một số tình huống bắt buộc dùng định tuyến tĩnh:
- Đường truyền có băng thông thấp
- Người quản trị mạng cần kiểm soát các kết nối.
- Kết nối dùng định tuyến tĩnh là đường dự phòng cho đường kết nối dùng giao thức định tuyến động.
- Chỉ có một đường duy nhất đi ra mạng bên ngoài (mạng stub).
- Router có ít tài nguyên và không thể chạy một giao thức định tuyến động.
- Người quản trị mạng cần kiểm soát bảng định tuyến và cho phép các giao thức classful và classless.

**Giao thức định tuyến** khác với **giao thức được định tuyến** cả về chức năng và nhiệm vụ .

***Giao thức định tuyến*** được sử dụng để giao tiếp giữa các router với nhau.

***Giao thức định tuyến*** cho phép router này chia sẻ các thông tin định tuyến mà nó biết cho các router khác .Từ đó ,các router có thể xây dựng và bảo trì bảng định tuyến của nó.

Sau đây là một số ***giao thức định tuyến***:

- Rouing information Protocol(RIP)
  - Là giao thức định tuyến theo vectơ khoảng cách
  - Sử dụng số lượng hop(router) để làm thông số chọn đường đi
  - Nếu số lượng hop để tới đích lớn hơn 15 thì gói dữ liệu sẽ bị huỷ bỏ
  - Cập nhật theo định kỳ mặc định là 30 giây IGRP
- Interior Gateway Routing Protocol(IGRP) là giao thức được phát triển độc quyền bởi Cisco .Sau đây là một số đặc điểm mạnh của IGRP:
- Là giao thức định tuyến theo vectơ khoảng cách
- Sử dụng băng thông ,tải ,độ trễ và độ tin cậy củ số lựa chọn đường đi
- Cập nhật theo định kỳ mặc định là 90 giây
- Enhanced Inteior Gateway Routing Protocol(EIGRP) là giao thức định tuyến nâng cao theo vectơ khoảng cách ,và là giao thức độc quyền của Ciso.Sau đây là các đặc điểm chính của EIGRP:
- Là giao thức định tuyến nâng cao theo vectơ khoảng cách
- Có chia tải
- Có các ưu điểm của đinh tuyến vector theo khoảng cách và định tuyến theo trạng thái đường liên kết
- Sử dụng thuật toán DUAL (Diffused Update Algorithm)để tính toán chọn đường tốt nhất. Cập nhật theo định kỳ mặc định là 90 gây hoặc cập nhật khi có thay đổi về cấu trúc mạng.
- Open Shortest Path First(OSPF) là giao thức đình tuyến theo trạng thái đường liên kết .Sau đây là các đặc điểm chính của OSPF :
- Là giao thức định tuyến theo trạng thái đường liên kết
- Được định nghĩa trong RFC 2328
- Sử dụng thuật toán SPF để tính toán chọn đường đi tốt nhất
- Chỉ cập nhật khi cấu trúc mạng có thay đổi

Còn, ***giao thức được định tuyến*** thì được sử dung để định hướng cho dữ lieu người dùng. Một giao thức định tuyến sẽ cung cấp về đầy đủ thông tin về địa chỉ lớp mạng để gói dữ lieu có thể truyền đi từ host này đến host khác dựa trên cấu trúc địa chỉ đó.

