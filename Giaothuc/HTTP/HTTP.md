Mục Lục 

1. Khái niệm
1. Sơ đồ hoạt động
1. URL (Uniform Resource Locator)
1. Các phương thức của giao thức HTTP (HTTP method)
1. Một số khái niệm liên quan
1. Các thành phần chính của HTTP

**1.HTTP là gì?**

HTTP (HyperText Transfer Protocol - Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW

HTTP là một giao thức ứng dụng của bộ giao thức TCP/IP (các giao thức nền tảng cho Internet).

**2. Sơ đồ hoạt động của HTTP**

HTTP hoạt động dựa trên mô hình Client – Server. Trong mô hình này, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.

HTTP là một stateless protocol. Hay nói cách khác, request hiện tại không biết những gì đã hoàn thành trong request trước đó.

HTTP cho phép tạo các yêu cầu gửi và nhận các kiểu dữ liệu, do đó cho phép xây dựng hệ thống độc lập với dữ liệu được truyển giao.

**3.Uniform Resource Locator (URL)**

Một URL (Uniform Resource Locator) được sử dụng để xác định duy nhất một tài nguyên trên Web. Một URL có cấu trúc như sau:

protocol://hostname:port/path-and-file-name

Trong một URL có 4 thành phần:

Protocol: giao thức tầng ứng dụng được sử dụng bởi client và server

Hostname: tên DNS domain

Port: Cổng TCP để server lắng nghe request từ client

Path-and-file-name: Tên và vị trí của tài nguyên yêu cầu.

**4.Một số khái niệm liên quan**

Layer 1. Network Access Layer

Network Access Layer xác định chi tiết về về cách thức dữ liệu được gửi qua mạng, bởi các thiết bị phần cứng trực tiếp giao tiếp với môi trường mạng, chẳng hạn như cáp đồng trục, cáp quang hay dây đồng xoắn đôi. Các giao thức bao gồm trong Network Access Layer là Ethernet, Token Ring, FDDI, X.25, Frame Relay ...vv

Layer 2. Internet Layer

Internet Layer đóng gói dữ liệu vào các gói dữ liệu được biết đến dưới dạng các gói tin thông giao thức Internet Protocol, chứa địa chỉ nguồn và đích (địa chỉ logic hoặc địa chỉ IP) được sử dụng để chuyển tiếp các gói tin giữa các máy chủ và qua các mạng.

Layer 3. Transport Layer

Mục đích của Transport Layer là cho phép các thiết bị trên máy chủ nguồn và đích đến trao đổi dữ liệu. Transport Layer sẽ xác định mức độ service và trạng thái của kết nối được sử dụng khi vận chuyển dữ liệu.


Layer 4. Application Layer

Các thực thể của lớp Application cung cấp các ứng dụng cho phép người dùng trao đổi dữ liệu ứng dụng qua mạng

Một số ứng dụng thường gặp của chồng giao thức TCP/IP: FTP (File Transfer Protocol), DNS

**5.Các thành phần chính của HTTP**

**-HTTP – Requests:**

**HTTP Request Method**

Cấu trúc của một HTTP Request:

- Một **Request-line** = **Phương thức** + **URI–Request** + **Phiên bản HTTP** . Giao thức HTTP định nghĩa một tập các giao thức GET, POST, HEAD, PUT ... Client có thể sử dụng một trong các phương thức đó để gửi request lên server.
- Có thể có hoặc không các trường **header**
- Một dòng trống để đánh dấu sự kết thúc của các trường **Header**

**1 số HTTP Request method thường dùng:**


