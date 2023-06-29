` `**Phân tích bản tin DHCP bằng Wireshark**

<a name="user-content-4.1"></a>**4.1. Chuẩn bị**

- Sử dụng máy Window đã cài đặt Wireshark.
- Release địa chỉ IP đang sử dụng bằng cách gõ các lệnh sau trong cmd:

\> ipconfig release

\> ipconfig renew 

Hoặc đơn giản là tắt card mạng đi bật lại.

- Capture gói tin trên card đang sử dụng mạng. Lọc các bản tin theo giao thức BOOTP (do DHCP là phần mở rộng cải tiến từ BOOTP nên để lọc DHCP ta vẫn phải lọc gói BOOTP) như sau:

<a name="user-content-4.2"></a>**4.2. Phân tích**

- **DHCP DISCOVER:**

Ban đầu khi máy chưa được cấu hình, máy sẽ gửi bản tin DHCP DISCOVER để yêu cầu DHCP server cấp cho một địa chỉ IP:

Thông tin phần giao thức DHCP:

- **DHCP OFFER**:

Bản tin DHCP OFFER gửi về từ server cung cấp IP 172.16.79.203 và một số thông tin cho client:

- **DHCP REQUEST**: Client gửi request yêu cầu được cấp IP 172.16.79.203 lại cho server và yêu cầu cung cấp thêm một số thông tin trong phần Options:


- **DHCP ACK**: Server gửi ACK về cho client chấp nhận việc client đã được sử dụng IP 172.16.79.203 và các thông số mà client yêu cầu:



