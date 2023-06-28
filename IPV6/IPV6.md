## ﻿**Mục Lục :**

## **1.Giới thiệu** 

## **2. Cấu trúc:**
## **3. Địa chỉ Unicast**
## **4. Địa chỉ Multicast**
## **5. Địa chỉ Anycast**
**6. Các địa chỉ IPv6 đặc biệt**
##
## **-------------------------------------------**

**1.IPV6:**

Địa chỉ IPv6 (Internet protocol version 6) là thế hệ địa chỉ Internet phiên bản mới được thiết kế để thay thế cho phiên bản địa chỉ IPv4 trong hoạt động Internet. Địa chỉ IPv4 có chiều dài 32 bít, biểu diễn dưới dạng các cụm số thập phân phân cách bởi dấu chấm, ví dụ 203.119.9.0. IPv4 là phiên bản địa chỉ Internet đầu tiên, đồng hành với việc phát triển như vũ bão của hoạt động Internet trong hơn hai thập kỷ. Với 32 bit [chiều dài](https://vi.wikipedia.org/wiki/Chi%E1%BB%81u_d%C3%A0i "Chiều dài"), không gian IPv4 gồm khoảng 4 tỉ địa chỉ cho hoạt động mạng toàn cầu.

**2.Cấu trúc IPv6:**

Trong IPV6, thay vì sử dụng một địa chỉ nguồn và đích là 32bit để cung cấp khoảng 4.294.967.296 (232) địa chỉ  như IPv4, địa chỉ IPv6 có chiều dài 128bit, do đó độ dài của IP sẽ lớn hơn,tương đương với việc số địa chỉ được tạo ra từ bội số 128bit sẽ lớn hơn rất nhiều ,có thể lên đến 3.4x1038 địa chỉ.Ngoài ra,có một vài sự khác nhau trong cách biểu diễn địa chỉ của IPv6, một địa chỉ IPv6 thường được viết thành 8 nhóm, mỗi nhóm gồm có 4 số hex và mỗi nhóm được tách biệt với nhau bằng dấu “:”. Ví dụ sau thể hiện điều này 2001:0f68:0000:0000:0000:0000:1986:69af.

**Cấu trúc IPv6 gồm 2 phần:**

- Payload: là sự kết hợp của Extension và PDU.Thông thường có thể lên tới 65535 byte.PDU thường bao gồm header của giao thức tầng cao và độ dài của nó, còn Extension là những thông tin liên quan đến dịch vụ kèm theo trong IPv6 được chuyển tới một trường khác và nó có thể có hoặc không.
- IPv6 Header: là thành phần luôn phải có trong một gói tin IPv6 và cố định 40 bytes

`           `- Version: 4 bits giúp xác định phiên bản của giao thức.

`           `- Traffic class: 8 bits giúp xác định loại lưu lượng.

`           `- Flow label: 20 bits giá mỗi luồng dữ liệu.

`           `- Payload length: 16 bits (số dương).Giúp xác định kích thước phần tải theo sau IPv6 Header.

`           `- Next-Header: 8 bits giúp xác định Header tiếp theo trong gói  tin.

`           `- Hop Limit: 8 bits (số dương). Qua mỗi node, giá trị này giảm 1 đơn vị ( giảm đến 0 thì gói bị loại bỏ).

`           `- Source address: 128 bits mang địa chỉ IPv6 nguồn của gói tin.

**3.Địa chỉ Unicast:**

Trong chế độ địa chỉ unicast, máy chủ được xác định duy nhất trong một phân đoạn mạng. Gói IPv6 chứa cả địa chỉ IP nguồn và đích. Giao diện máy chủ được trang bị một địa chỉ IP duy nhất trong phân khúc mạng đó. Khi bộ chuyển mạch mạng hoặc bộ định tuyến nhận được gói IP unicast thì nó được gửi đến một máy chủ duy nhất.

Địa chỉ unicast gồm có 4 loại khác nhau :

- Global Unicast Address
- Link-Local Address
- Site-Local Address
- Unique-Local 

**4.Địa chỉ Multicast**

Chế độ Multicast IPv6 giống như của IPv4. Gói tin được gửi đến nhiều node với một địa chỉ multicast đặc biệt. Tất cả các node quan tâm đến thông tin phát multicast đó, trước tiên cần tham gia nhóm multicast .Toàn bộ các node tham gia nhóm đều sẽ nhận được gói phát multicast này và xử lý nó, trong khi các node khác không quan tâm đến gói phát multicast đó thì bỏ qua.

Địa chỉ multicast cũng có các phạm vi: global, site-local, link-local ngoài ra multicast còn có thêm 2 phạm vi mới đó là organization-local và node-local. Một node IPv6 có thể được gắn rất nhiều địa chỉ.

- Organization-local: được sử dụng trong phạm vi một tổ chức với một số site.
- Node-local: chỉ có tính tương ứng trong phạm vi một node

**5.Địa chỉ Anycast**

IPv6 đã giới thiệu một loại địa chỉ mới, được gọi là địa chỉ Anycast.Trong chế độ địa chỉ này, nhiều Hosts được gán cùng một địa chỉ IP Anycast. Khi một node muốn liên lạc với một node được trang bị địa chỉ IP Anycast, nó sẽ gửi một tin nhắn Unicast.Tin nhắn này sẽ không được gửi đến tất cả các node trong nhóm giống như Multicast mà với sự trợ giúp của cơ chế định tuyến, thông điệp Unicast đó được gửi đến node gần nhất trong nhóm với người gửi(tính theo thủ tục định tuyến) .

**6.Các địa chỉ IPv6 đặc biệt**

| |IPv6 Address|Meaning|
| - | - | - |
|0:0:0:0:0:0:0:0/128|::/128|Địa chỉ không xác định|
|0:0:0:0:0:0:0:0|::/0|Tuyến đường mặc định|
|0:0:0:0:0:0:0:1/128|::1/128|Địa chỉ Loopback|

Địa chỉ Multicast dành riêng cho giao thức định tuyến

|IPv6 Address|Giao thức định tuyến|
| - | - |
|FF02 : : 5|OSPFv3|
|FF02 : : 6|OSPFv3 Designated Routers|
|FF02 : : 9|RIPng|
|FF02 : : A|EIGRP|

