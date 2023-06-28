Phân biệt UDP/TCP:

|**Tính năng**|***TCP***|***UDP***|
| :- | :- | :- |
|**Trạng thái kết nối**|Yêu cầu kết nối đã thiết lập để truyền dữ liệu (Phải ngắt kết nối sau khi đã được truyền)|<p>Không kết nối, không yêu cầu mở,</p><p>` `không duy trì hoặc chấm dứt kết nối</p>|
|**Giải trình tự dữ liệu**|Có trình tự|Không trình tự|
|**Cung cấp dữ liệu đến đích**|Đảm bảo|Không đảm bảo|
|**Truyền lại dữ liệu gói bị mất**|Truyền lại được|Không truyền lại được|
|**Kiểm tra lỗi**|Kiểm tra lỗi mở rộng và xác nhận dữ liệu|Tổng kiểm tra cơ bản|
|**Phương thức chuyển khoản**|Dữ liệu được đọc dưới dạng luồng byte, thông điệp được truyền đến ranh giới phân đoạn.|<p>Ranh giới xác định; gửi riêng lẻ và kiểm </p><p>tra tính toàn vẹn khi đến nơi.</p>|
|**Tốc độ**|Chậm hơn UDP|Faster than TCP|
|**Phát sóng**|Không hỗ trợ phát sóng|Does support Broadcasting|
|**Sử dụng tối ưu**|Được sử dụng bởi HTTPS, [HTTP](https://bkhost.vn/blog/http-va-https-la-gi/), [SMTP](https://bkhost.vn/blog/smtp-la-gi/), POP, [FTP](https://bkhost.vn/blog/ftp/), v.v.|<p>Hội nghị truyền hình, phát trực tuyến, </p><p>[DNS](https://bkhost.vn/blog/dns-la-gi/), [VoIP](https://bkhost.vn/blog/voip-la-gi/), v.v.</p>|

