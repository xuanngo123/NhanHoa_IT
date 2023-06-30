**1. VLAN là gì?**

**VLAN** là viết tắt của **Virtual Local Area Network** - nghĩa là **mạng LAN ảo**, là một mạng tuỳ chỉnh, được hình thành từ một hoặc nhiều mạng LAN, cho phép các nhóm thiết bị khả dụng kết nối cùng với một mạng dù không đặt cạnh nhau.

Từ đó tạo nên mạng VLAN được quản lý tương tự với mạng LAN vật lý. VLAN hay Virtual LAN giúp sử dụng tài nguyên mạng hiệu quả hơn và hữu ích khi kết nối quá nhiều thiết bị cùng một mạng.

Sơ đồ Virtual Local Area Network

Thông thường Router sẽ có vai trò là miền quảng bá. Tuy nhiên, trong mạng VLAN, thiết bị chuyển mạch Switch sẽ có chức năng tương tự tạo nên miền quảng bá. Vậy nên xét về mặt kỹ thuật, mạng VLAN được xem là một miền quảng bá được tạo ra bởi Switch.

Có thể hiểu VLAN là một kỹ thuật cho phép quản trị viên thiết lập hệ thống nhiều mạng LAN đơn trên cùng một hạ tầng hệ thống.

Mạng VLAN thường được cấu hình khi mạng máy tính của người dùng quá lớn với lượng truy cập quá nhiều. Đôi khi cũng có những trường hợp người dùng VLAN chỉ vì mạng máy tính của họ đang sử dụng mạng VLAN.

**>> Tìm hiểu: [Mạng LAN là gì](https://viettuans.vn/mang-lan-la-gi "Mạng LAN là gì")?**

**2. Phân loại VLAN gồm những loại nào?**

Hiện nay có những loại mạng VLAN nào? Dưới đây là 3 loại VLAN phổ biến nhất, cùng Việt Tuấn tìm hiểu ngay nhé.

**+ Port - based VLAN**

**+ MAC address based VLAN**

**+ Protocol - based VLAN**

**3. Ưu điểm và nhược điểm của VLAN**

**3.1. Ưu điểm của VLAN**

Thông qua cách giới hạn miền quảng bá, các trạm cuối trên một VLAN bị chặn không cho nghe hay nhận các chương trình phát sóng không dành cho nó. Thêm nữa, nếu một Router không được kết nối với VLAN, các trạm cuối của một VLAN sẽ không trao đổi/giao tiếp với trạm cuối của các VLAN khác. Với việc giới hạn các miền quảng bá trên mạng giúp giảm đáng kể lưu lượng truy cập.

Các giới hạn ảo do VLAN thiết lập chỉ có thể vượt qua được bởi các Router. Bởi vậy, quyền truy cập vào VLAN bị hạn chế thông qua việc áp dụng các biện pháp bảo mật dựa trên thiết bị định tuyến tiêu chuẩn. Ngoài ra, VLAN có thể tăng cường bảo mật bằng cách lọc gói tin. Quản trị viên mạng kiểm soát từng cổng và bất kỳ tài nguyên nào mà họ cho phép được dùng, phân tách các nhóm có dữ liệu nhạy cảm khỏi phần còn lại của mạng và hạn chế nguy cơ bị lộ thông tin mật.

VLAN giúp cải thiện hiệu quả mạng tổng thể bằng cách tạo nhóm các thiết bị giao tiếp thường xuyên nhất. VLAN cung cấp bảo mật cho các mạng lớn thông qua việc cấp quyền kiểm soát thiết bị lớn hơn. Các tổ chức lớn thường tạo VLAN với mục đích kiểm soát lưu lượng cao để phân vùng lại các thiết bị.

**3.2. Nhược điểm của VLAN**

Bên cạnh những ưu điểm nổi trội bên trên thì VLAN cũng có những hạn chế cần lưu ý, chẳng hạn như:

- Gói tin có thể bị rò rỉ giữa các VLAN.
- Để xử lý được khối công việc trong hệ thống mạng lớn, cần có thiết bị định tuyến mạnh.
- Một VLAN không thể chuyển tiếp lưu lượng mạng tới những VLAN khác.
- Khả năng tương tác là một rào cản lớn.
- Các mối đe dọa trong hệ thống đơn lẻ có thể phát tán virus khắp hệ thống mạng.
- Cấu hình VLAN phải phụ thuộc nhiều vào nhà sản xuất thiết bị mạng do tiêu chuẩn chính thức  IEEE 802.1q chưa được phê duyệt.

**4. Ứng dụng và lợi ích của VLAN**

VLAN ngày càng trở nên phổ biến và được ứng dụng rộng rãi, bởi một số lợi ích tuyệt vời mà nó mang lại:

- **Tiết kiệm băng thông của hệ thống mạng**

VLAN chia mạng cục bộ (LAN) thành nhiều phân đoạn (segment) mạng nhỏ. Khi có gói tin quảng bá (broadcast), nó sẽ truyền trong VLAN tương ứng. Do đó, việc phân đoạn VLAN giúp tối ưu băng thông của hệ thống mạng.

- **Tăng khả năng bảo mật**

Các thiết bị ở các VLAN khác nhau sẽ không thể kết nối với nhau (trừ khi trang bị Router nối giữa các VLAN). Ví dụ máy tính ở mạng VLAN kế toán không thể kết nối với các máy tính ở VLAN kỹ sư. Điều này giúp tăng cường bảo mật dữ liệu hiệu quả hơn.

- **Có tính linh động cao**

VLAN có thể dễ dàng di chuyển các thiết bị. VLAN có thể được cấu hình tĩnh hoặc động. Trong cấu hình tĩnh, người quản trị mạng sẽ cấu hình cho từng cổng của mỗi Switch. Tiếp đó, gán vào một VLAN bất kỳ. Với cấu hình động, mỗi cổng của Switch có thể tự cấu hình cho VLAN thông qua địa chỉ MAC được thiết bị kết nối vào.

- **Dễ dàng thêm / bớt máy tính vào VLAN**

Chỉ cần cấu hình cổng máy tính vào VLAN mong muốn là có thể thêm máy tính vào VLAN.

Mạng VLAN thường được ứng dụng nhiều cho các công ty có quy mô lớn với lượng truy cập [Internet](https://viettuans.vn/internet-la-gi "Internet là gì? Những điều cần biết về internet") khủng trong cùng lúc. Với những máy tính có dung lượng lớn, nhiều người truy cập vào cùng lúc, sử dụng VLAN giúp giảm tải, chia đều người dùng Internet để họ có có thể truy cập mạng nhanh chóng hơn.

**>> Tìm hiểu: [Router là gì](https://viettuans.vn/router-la-gi "Router là gì")?**

**5. Khi nào cần sử dụng VLAN?**

Khi nào cần thiết cấu hình VLAN? Mạng VLAN được sử dụng trong nhiều trường hợp, đáp ứng nhu cầu truy cập Internet lớn của người dùng. Một số trường hợp thường sử dụng VLAN như:

- Hệ thống máy tính chạy trong mạng LAN đạt hơn 200 thiết bị.
- Bên trong mạng LAN, lưu lượng quảng bá của người dùng đạt đến ngưỡng quá lớn.
- Hệ thống máy tính kết nối chậm do có quá nhiều tin quảng bá.
- Nhóm làm việc ở trên cùng một miền phát sóng và chạy chung một ứng dụng.
- Người dùng có nhu cầu nâng cao tính bảo mật dữ liệu trong quá trình làm việc nhóm.
- Người dùng có nhu cầu chuyển đổi bộ chuyển mạch đơn thành nhiều bộ chuyển mạch ảo.

**6. Sự khác nhau giữa mạng LAN và VLAN**

**Mạng LAN** hay mạng cục bộ là hệ thống mạng dùng để kết nối số lượng lớn máy tính và các thiết bị ngoại vi trong một phạm vi địa lý nhỏ. Các máy tính trong mạng LAN có thể chia sẻ tài nguyên với nhau.

Còn mạng VLAN là một mạng LAN ảo được tạo thành từ một hay nhiều mạng LAN tập hợp lại với nhau. Trong mạng VLAN, các máy tính giao tiếp/trao đổi với nhau như thể chúng được kết nối cùng miền phát sóng bất kể vị trí vật lý.

Các VLAN có thể tiết kiệm lưu lượng băng thông hơn so với mạng LAN truyền thống. **Ví dụ**: *Nếu lưu lượng phát sóng dành cho năm người dùng, họ có thể được đặt trên năm VLAN khác nhau mà lần lượt sẽ làm giảm lưu lượng truy cập*.

Ứng dụng VLAN vào các mạng LAN truyền thống giúp tối ưu chi phí vì VLAN loại bỏ nhu cầu trang bị Router đắt tiền.

Trong mạng cục bộ, Router xử lý lưu lượng truy cập đến với lượng băng thông ngày càng tăng, thời gian trễ cũng tăng theo, như vậy sẽ làm giảm hiệu suất. Đối với VLAN, hạn chế nhu cầu trang bị Router bởi VLAN có thể tạo các miền phát sóng thông qua bộ chuyển mạch thay vì bộ định tuyến.

Mạng LAN yêu cầu quản lý vật lý như là người dùng dùng thay đổi vị trí sẽ cần thiết phục hồi địa chỉ trạm mới, tái cấu hình của Router và các [**Hub**](https://viettuans.vn/hub-la-gi "https://viettuans.vn/hub-la-gi"). Sự di chuyển của người dùng trong một mạng dẫn đến phát sinh các chi phí mạng. Trong khi đó, nếu người dùng di chuyển trong mạng VLAN, thì không cần thiết phải cấu hình lại Router.

Ngoài ra, các dữ liệu phát trên VLAN an toàn hơn so với mạng LAN bởi dữ liệu nhạy cảm chỉ có thể truy cập bởi người dùng trên VLAN.

Bạn hãy theo dõi bảng so sánh LAN và VLAN dưới đây để hiểu rõ hơn:

|**Tiêu chí** |**VLAN**|**LAN**|
| :-: | :-: | :-: |
|**Khái niệm** |Là một mạng LAN ảo được tạo thành từ một hay nhiều mạng LAN.|Là một tập hợp các máy tính và thiết bị ngoại vi được kết nối trong một phạm vi địa lý nhỏ.|
|**Cách thức hoạt động**|Các gói mạng trong VLAN chỉ được gửi đến một địa chỉ Broadcast duy nhất.|Các gói mạng được Broadcast gửi tới từng thiết bị trong mạng LAN.|
|**Giao thức** |VLAN sử dụng các giao thức VTP và ISP.|LAN sử dụng giao thức FDDI|
|**Độ trễ**|Độ trễ của VLAN giảm xuống thấp hơn LAN|Độ trễ của LAN lớn hơn VLAN|
|**Chi phí**|Thấp hơn (do không cần thiết sử dụng Router)|Cao hơn (do cần trang bị Router)|
|**Hiệu suất** |VLAN mang lại hiệu suất tốt hơn so với mạng LAN |LAN mang đến hiệu suất thấp hơn so với mạng VLAN|
|**Mức độ an toàn**|VLAN an toàn hơn |LAN có mức độ an toàn kém hơn VLAN|

