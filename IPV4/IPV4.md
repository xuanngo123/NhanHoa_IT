Mục lục:
1.IPV4 là gì?
2.Cấu trúc
3.tìm hiểu subnet và subnetmark
4.chia mạng 
5.ví dụ
 **1.IPV4 là gì?**

IPv4 là phiên bản IP thế hệ thứ 4, nó được sử dụng nhiều nhất hiện nay bên cạnh [IPv6](https://bkhost.vn/blog/ipv6/). Hai phiên bản IP này là yếu tố chủ chốt cho việc giao tiếp giữa các thiết bị trong mạng internet.

IPv4 được ra mắt vào năm 1981 trong phiên bản RFC 791 và đã được bộ quốc phòng Hoa Kỳ chuẩn hóa trong phiên bản MIL-STD-1777.

IPv4 được ứng dụng trong các hệ thống chuyển mạch gói. Vai trò của nó là định hướng [dữ liệu](https://bkhost.vn/blog/data-du-lieu/) truyền đi. Khi truyền đi các gói tin, giao thức này chỉ đảm bảo phần truyền tải mà không để ý đến thứ tự truyền gói tin hoặc vấn đề gói tin có đến đích hay không, có lặp lại ở máy đích hay không. Vấn đề này sẽ được giải quyết ở tầng cao hơn của hệ thống TCP/IP. Một điều mà IPv4 đảm bảo được đó là tính toàn vẹn dữ liệu bằng cách sử dụng kết quả của việc chạy thuật toán Checksum để kiểm tra.

**2.CẤU TRÚC IPV4:**

Về cấu tạo, địa chỉ IPv4 sẽ có 32 bit và được biểu diễn thành một dãy số nhị phân và chia thành 4 cụm. Mỗi cụm như vậy sẽ gọi là [octet](https://bkhost.vn/blog/octet/). Mỗi octet sẽ là 8 bit và chúng được ngăn cách bằng dấu chấm (.)

Về hình dáng, cấu trúc của một địa chỉ IPv4 sẽ gồm 4 con số ở dạng thập phân tượng trưng cho 4 cụm. Địa chỉ này gồm 2 phần là phần mạng và phần host

**3. Phân loại địa chỉ IPv4**

Dựa vào cách chọn địa chỉ mạng mà địa chỉ IP được phân thành 5 lớp A, B, C, D, E. Đặc điểm của các lớp như sau:

**Lớp A**

Địa chỉ lớp A

Địa chỉ lớp A có phần mạng là 8 bit đầu và phần host là 24 bit sau. Bit đầu tiên của phần mạng luôn là 0.

Lớp A sẽ có các địa chỉ mạng từ 1.0.0.0 đến 126.0.0.0 và mỗi mạng sẽ có 224 địa chỉ host (loại trừ địa chỉ mạng và địa chỉ broadcast).

Mạng [loopback](https://bkhost.vn/blog/loopback/) sẽ là 127.0.0.0.

**Lớp B**

Địa chỉ lớp B

Địa chỉ lớp B có phần mạng là 16 bit đầu và phần host là 16 bit sau. [2 bit](https://bkhost.vn/blog/bit-la-gi/) đầu tiên của phần mạng luôn là 1.0.

Lớp B sẽ có các địa chỉ mạng từ 128.0.0.0 đến 191.255.0.0 và mỗi mạng sẽ có 214 địa chỉ host (loại trừ địa chỉ mạng và địa chỉ broadcast).

**Lớp C**

Địa chỉ lớp C

Địa chỉ lớp C có phần mạng là 24 bit đầu và phần host là 8 bit sau. 3 bit đầu tiên của phần mạng luôn là 1.1.0.

Lớp C sẽ có các địa chỉ mạng từ 192.0.0.0 đến 223.255.255.0 và mỗi mạng sẽ có 26 địa chỉ host (loại trừ địa chỉ mạng và địa chỉ broadcast).

**Lớp D**

Các địa chỉ trong lớp D là những địa chỉ [multicast](https://bkhost.vn/blog/multicast/) bao gồm 224.0.0.0 đến 239.255.255.255.

**Lớp E**

Các địa chỉ trong lớp E có vai trò dùng để dự phòng, bao gồm những địa chỉ từ 240.0.0.0 trở đi.

- Lớp A từ 1 đến 126.
- Lớp B từ 128 đến 191.
- Lớp C từ 192 đến 223.
- Lớp D từ 224 đến 239.
- Lớp E từ 240 đến 255.

## **4.Tìm hiểu về Subnet và SubnetMark?**
Subnet mask là gì? Hiểu một cách đơn giản, Subnet là một số dạng 32 bit. Để tạo ra Subnet mask, người ta sẽ đặt host bit dưới dạng số 0 và network bit dạng số 1. Từ đó tạo ra các dãy số có dạng nhị phân là 0 và 1 để phân chia địa chỉ IP thành 2 phần, tương ứng với địa chỉ mạng và địa chỉ host. 

Địa chỉ mạng thường có số 0 và địa chỉ broadcast thường có số 255. Ngoài ra, địa chỉ IP, Subnet Mask và router sẽ có các cấu trúc riêng. Tùy từng khu vực, từng địa chỉ mà địa chỉ thể hiện sẽ có sự khác biệt. Người dùng có thể dựa vào các số này để xác định chính xác IP và route của mình.

**4.TÍNH SUBNET MARK**

Sẽ rất hữu ích nếu bạn biết cách tính subnet mask của mình. Chia địa chỉ Class C bằng phương thức nhị phân bằng cách làm theo bốn bước sau:

1. Chuyển đổi sang [hệ nhị phân](https://vietnix.vn/he-nhi-phan/).
2. Tính địa chỉ tập hợp con (subset).
3. Tìm phạm vi của host.
4. Tính tổng số tập hợp con (subset) và host trên mỗi subnet.

Chúng ta sẽ sử dụng địa chỉ Class C, lấy 5 bit từ trường Host để chia subnet (mạng con) và để lại 3 bit để xác định các máy chủ như trong hình 1 bên dưới. Có sẵn 5 bit để xác định subnet có nghĩa là chúng ta có thể có tối đa 32 (2 ^ 5) subnet khác nhau.

Cần lưu ý rằng trước đây không cho phép sử dụng subnet zero (00000 —) và all-ones subnet (11111 —). Điều này không đúng đối với cách tính hiện nay. Kể từ Bản phát hành phần mềm iOS 12.0 của Cisco, toàn bộ không gian địa chỉ bao gồm tất cả các subnet có thể được cho phép tính toán một cách rõ ràng.

Ví dụ IP thuộc subnet mới sau khi chia: địa chỉ IP 192.168.10.44, subnet mask  255.255.255.248 hoặc / 29.

**Bước 1**: Chuyển đổi sang hệ nhị phân

**Bước 2**: Tính địa chỉ subnet

Để tính Địa chỉ IP subnet, bạn cần thực hiện thao tác AND theo bit (1 + 1 = 1, 1 + 0 hoặc 0 + 1 = 0, 0 + 0 = 0) trên địa chỉ IP host và subnet mask. Kết quả là địa chỉ subnet chứa host.

**Bước 3**: Tìm Phạm vi của Host

Chúng ta đã biết rằng đối với subnet địa chỉ Class C này, chúng ta đã mượn 5 bit từ trường host. 5 bit này được sử dụng để xác định các subnet. 3 bit còn lại được sử dụng để xác định các host trong một subnet cụ thể.

Địa chỉ subnet được xác định bởi tất cả các bit 0 trong phần host của địa chỉ. Host đầu tiên trong subnet được xác định bởi tất cả các số 0 và 1. Host cuối cùng được xác định bởi tất cả các số 1 và số 0. Địa chỉ broadcast là tất cả các số 1. Bây giờ, chúng ta chuyển sang subnet tiếp theo và quá trình này được lặp lại theo cùng một cách.

Sơ đồ sau minh họa rõ ràng quá trình này:


**Bước 4**: Tính Tổng số subnet và host trên mỗi subnet

Khi biết số lượng bit của Subnet và Host, chúng ta có thể tính toán tổng số subnet có thể có và tổng số host trên mỗi subnet. Chúng ta sẽ giả định trong các tính toán của mình rằng có thể sử dụng tất cả các số 0 và các mạng con tất cả các số 1. Sơ đồ sau minh họa các bước tính:


Một số người biết cách tính toán subnet mask bằng tay, nhưng hầu hết mọi người sử dụng subnet mask calculator. Có một số loại subnet calculator. Một số calculator bao gồm nhiều chức năng hơn và có phạm vi lớn hơn, trong khi một số khác có các tiện ích cụ thể. Các công cụ này có thể cung cấp thông tin như dải IP, địa chỉ IP, subnet mask và địa chỉ mạng.

**5.CÁCHI CHI MẠNG IPV4**

Xét mạng 192.168.1.0/24 , mượn 2 bit, còn lại 6 bit host,  bước nhảy là 64. Ta có:

\-    Số subnet có thể có: 2<sup>2</sup> = 4 subnet.

\-    Số host trên mỗi subnet = 2<sup>6</sup> – 2 = 62 host.

\-    Các địa chỉ mạng sẽ có octet bị chia cắt (octet thứ 4) là bội số của 64.

\-    Liệt kê các mạng như sau:

`     `+Sub 1->      192.168.1.0/26    -> địa chỉ mạng

`                        `192.168.1.1/26    ->địa chỉ host đầu.

`             `Đến:

`            `192.168.1.62/26   ->địa chỉ host cuối.

`            `192.168.1.63/26   ->địa chỉ broadcast.

`            `---------------------------------------------

`      `+Sub 2:  

`            `192.168.1.64/26    -> địa chỉ mạng

`            `192.168.1.65/26    ->địa chỉ host đầu

`                       `Đến :

`            `192.168.1.126/26   ->địa chỉ host cuối

`            `192.168.1.127/26   ->địa chỉ broadcast.

`    `+Sub 3:

`            `---------------------------------------------

`    `+Sub 4:

`            `192.168.1.128/26    -> địa chỉ mạng

`            `192.168.1.129/26    ->địa chỉ host đầu.

`                        `….

`           `192.168.1.190/26   ->địa chỉ host cuối.

`            `192.168.1.191/26   ->địa chỉ broadcast.

`            `---------------------------------------------

`     `+Sub 5:

`            `192.168.1.192/26    -> địa chỉ mạng

`            `192.168.1.193/26    ->địa chỉ host đầu.

`                        `….

192\.168.1.254/26   ->địa chỉ host cuối.

`            `192.168.1.255/26   ->địa chỉ broadcast.



Vậy, một mạng lớp C 192.168.1.0/24 đã được chia thành 4 mạng :192.168.1.0/26, 192.168.1.64/26, 192.168.1.128/26, 192.168.1.192/26.

Subnet mask được sử dụng trong ví dụ này là 255.255.255.192

**6.VÍ DỤ IPV4:**

Để hiểu địa chỉ Ipv4 là gì có thể lấy ví dụ như sau: Giả sử ta có 1 dải số như sau: **172.16.254.1**. Dải số này có thể được dùng để đặt tên cho 1 địa chỉ Ipv4 nào đó. Có thể thấy địa chỉ Ipv4 có tổng cộng 4 số và mỗi số phải nằm trong giới hạn từ 0-255. Xem hình minh họa.

Các loại địa chỉ Ipv4: unicast, broadcast, multicast. Trong đó unicast là địa chỉ IP cho phép thiết bị gửi dữ liệu đến 1 nơi nhận duy nhất. Địa chỉ IP broadcast lại cho phép gửi dữ liệu đến các host trong 1 mạng con. Còn địa chỉ IP multicast cho phép thiết bị gửi dữ liệu đến 1 tập xác định trước các host.



