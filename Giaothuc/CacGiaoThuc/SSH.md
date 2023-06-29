**SSH là gì?**

SSH, hay Secure (Socket) Shell, là một giao thức mạng cung cấp cho người dùng (đặc biệt là các QTV mạng) cách truy cập an toàn vào một máy tính qua một mạng không được bảo mật. Bên cạnh đó, SSH cũng cung cấp nhiều bộ tiện ích để triển khai giao thức SSH. Secure Shell là một giao thức cung cấp khả năng xác thực [password ](https://vietnix.vn/password-la-gi/)mạnh mẽ, cùng với khả năng giao tiếp dữ liệu được mã hóa giữa hai máy tính kết nối với nhau qua một mạng mở như Internet. Bên cạnh đó, SSH cũng được sử dụng phổ biến bởi các QTV mạng để quản lý hệ thống và ứng dụng từ xa. Từ đó cho phép đăng nhập vào các máy tính khác qua mạng và thực hiện các tác vụ cơ bản như thực thi lệnh, di chuyển file,…

SSH bao gồm cả giao thức mạng lẫn một bộ tiện ích để triển khai giao thức đó. SSH sử dụng mô hình client-server, kết nối một ứng dụng Secure Shell client (nơi session được hiển thị) với một SSH server (nơi session chạy). Triển khai SSH thường hỗ trợ cả các giao thức ứng dụng, dùng cho giả lập terminal hay truyền file. Ngoài ra, SSH cũng có thể được dùng để tạo các tunnel bảo mật cho nhiều giao thức ứng dụng. Chẳng hạn như để chạy các phiên đồ họa X Windows System từ xa. Một SSH server theo mặc định sẽ nghe trên cổng TCP 22.

SSH là gì?

**Giao thức SSH hoạt động như thế nào?**

Secure Shell được tạo ra để thay thế các chương tình giả lập terminal hoặc chương trình đăng nhập không an toàn như Telnet, rlogin (remote login) hay rsh (remote shell). Bên cạnh đó, SSH cũng hỗ trợ các chức năng tương tự như đăng nhập và chạy các terminal session trên hệ thống ở xa. SSH cũng thay thế các chương trình truyền file như FTP (File Transfer Protocol) hay rcp (remote copy).

**>> [FTP là gì?](https://vietnix.vn/ftp-la-gi/)**

Chức năng đơn giản nhất của SSH là kết nối đến một host ở xa cho một phiên terminal, bằng lệnh như sau:

ssh server.example.org

Qua lệnh này, client sẽ kết nối đến một server có tên server.example.com bằng user ID là UserName. Nếu đây là lần kết nối đầu tiên giữa host và server, người dùng sẽ được thông báo về public key fingerprint của host ở xa và nhắc người dùng kết nối:

The authenticity of host 'sample.ssh.com' cannot be established.

DSA key fingerprint is 

01:23:45:67:89:ab:cd:ef:ff:fe:dc:ba:98:76:54:32:10.

Are you sure you want to continue connecting (yes/no)?

Nếu chọn yes, phiên sẽ được tiếp tục và host key được lưu trữ trong file known\_hosts của hệ thống cục bộ. Đây là một file ẩn và được lưu trữ mặc định trong một directory ẩn tên là /.ssh/known\_hosts, trong home directory của người dùng. Sau đó, client có thể kết nối trực tiếp đến server đó lần nữa mà không cần phê duyệt; host key sẽ xác thực kết nối.

**Chức năng của giao thức SSH**

Sau khi biết được giao thức SSH là gì và hoạt động như thế nào? Chắc hẳn bạn đang thắc mắc về các chức năng của SSH key. Thì, SSH hỗ trợ các chức năng sau đây:

- Truy cập từ xa an toàn vào các hệ thống hay thiết bị mạng có hỗ trợ SSH cho người dùng và các quá trình tự động khác.
- Hỗ trợ phiên chuyển file an toàn
- Tự động truyền file an toàn.
- Thực thi lệnh an toàn trên các máy hay hệ thống từ xa.
- Quản lý an toàn các thành phần cơ sở hạ tầng mạng.

SSH có thể được sử dụng để enable các terminal session và nên được dùng thay thế cho các chương trình Telnet có độ bảo mật kém hơn. Ngoài ra, SSH cũng thường được dùng trong các script và nhiều phần mềm khác để cho phép các chương trình, hệ thống truy cập an toàn từ xa vào các tài nguyên khác.

**Ứng dụng của SSH là gì?**

- SSH có mặt trong mọi [datacenter](https://vietnix.vn/datacenter-la-gi/) và được đi kèm mặc định trong mọi server Unix, Linux và Mac. Các kết nối SSH hiện đang được ứng dụng để bảo mật nhiều loại giao tiếp khác nhau giữa một máy cục bộ và một host từ xa. Trong đó bao gồm cả quyền truy cập an toàn từ xa vào các tài nguyên, thực thi lệnh từ xa hay chuyển các bản patch, bản cập nhật phần mềm,… Bên cạnh khả năng tạo ra các kênh an toàn cho máy cục bộ và máy ở xa, SSH cũng dùng để quản lý router, phần cứng của server, các nền tảng ảo hóa, hệ điều hành, và có trong các ứng dụng quản lý và truyền file,…
- Secure Shell được dùng để kết nối đến các [server](https://vietnix.vn/server-la-gi/), thực hiện các thay đổi, upload,… bằng các công cụ hay thông qua terminal. Bên cạnh đó, các SSH key cũng được dùng để tự động truy cập vào server, chủ yếu được ứng dụng trong các script, hệ thống backup hay các công cụ quản lý cấu hình,…
- SSH được thiết kế với mục đích đề cao sự thuận tiện và khả năng làm việc xuyên ranh giới giữ các tổ chức, do đó SSH key cung cấp một single sign-on (SSO – đăng nhập một lần) để người dùng có thể nhanh chóng chuyển qua lại giữa các tài khoản mà không cần tốn thời gian nhập password.
- Hơn nữa, SSH không chỉ xác thực qua một kết nối được mã hóa, mà mọi SSH traffic đều được mã hóa; cho dù người dùng đang truyền file, duyệt web hay chạy lệnh, mọi tác vụ của họ đều được bảo mật tuyệt đối.
- Ta có thể sử dụng SSH với một user ID thông thường và password làm thông tin xác thực, tuy nhiên SSH chủ yếu dựa vào các public key pair để xác thực các host với nhau. Người dùng cá nhân vẫn phải sử dụng user ID và password – hoặc các phương pháp xác thực khác – để có thể kết nối đến host từ xa, tuy nhiên máy cục bộ và máy từ xa sẽ xác thực riêng biệt với nhau. Việc này được thực hiện bằng cách tạo một public key pair duy nhất cho từng host trong quá tình giao tiếp. Mỗi session yêu cầu có hai public key pair: một key pair dùng để xác thực máy từ xa với máy cục bộ, và bộ key pair có nhiệm vụ ngược lại.

**Khi nào nên sử dụng SSH**

SSH hoạt động ở tầng thứ 4 trong mô hình TCP/IP. Nó cho phép tương tác giữa máy chủ và máy khách, sử dụng cơ chế mã hoá nhằm ngăn chặn các hiện tượng nghe trộm, đánh cắp thông tin trên đường truyền. Đây là điều mà các giao thức trước đây như telnet, rlogin không đáp ứng được.

**>> [TCP/IP là gì?](https://vietnix.vn/tcp-ip-la-gi/)**

**Ưu điểm của SSH**

SSH cho phép mã hóa dữ liệu để những kẻ tấn công không thể đánh cắp thông tin người dùng và mật khẩu của bạn. SSH cũng cho phép tạo các giao thức truyền dữ liệu khác như FTP. Dưới đây là danh sách những điều cụ thể mà SSH bảo vệ bạn.

- IP source routing
- Giả mạo DNS
- Nghe lén dữ liệu được truyền
- Giả mạo địa chỉ IP
- Thao túng dữ liệu trên routers

**Một số vấn đề bảo mật của SSH**

Tuy nhiên, SSH cũng có một số lỗ hổng bảo mật nhất định mà các doanh nghiệp nên chú ý. Cụ thể, các key được lưu trữ trên hệ thống client có thể tích tụ dần theo thời gian, vì vậy cần có được cách quản lý host key hiệu quả, đặc biệt là với những nhân viên IT – những người cần truy cập vào các server từ xa để quản lý. Ngoài ra, dữ liệu được lưu trong file SSH known\_file có thể dùng để lấy quyền truy cập đã được xác thực vào hệ thống từ xa. Do đó, các doanh nghiệp cần có một quy trình tiêu chuẩn để duy trì quyền kiểm soát các file này.

Bên cạnh đó, các developer cũng cần cẩn thận khi kết hợp các lệnh hay hàm SSH với nhau trong script hoặc các loại chương trình khác. Mặc dù ta có thể đưa ra lệnh SSH chứa user ID và password để xác thực người dùng của máy cục bộ với một tài khoản trên host từ xa, nhưng việc này sẽ làm lộ thông tin xác thực cho những kẻ tấn công để truy cập vào mã nguồn.

Shellshock, một lỗ hổng bảo mật trong Bash command processor, có thể được thực thi qua SSH nhưng nó là một lỗ hổng trong Bash chứ không phải trong SSH. Mối đe dọa lớn nhất đối với SSH chính là khả năng quản lý key không tốt. Nếu không tạo, xoay vòng và loại bỏ key SSH tập trung thích hợp, các tổ chức hoàn toàn có thể mất quyền kiểm soát những người có quyền truy cập vào  tài nguyên, đặc biệt là khi SSH được sử dụng trong các quy trình app-to-app tự động.

**Các kỹ thuật mã hóa khác**

Ưu điểm của SSH so với các giao thức cũ là khả năng mã hóa và truyền tải dữ liệu một cách an toàn giữ host và client.
Có 3 cách để mã hóa khi sử dụng SSH

- Symmetrical encryption.
- Asymmetrical encrytion.
- Hashing.

Bây giờ chúng ta sẽ tìm hiểu cách thức mã hóa của từng loại.

**Symmetrical encryption là gì?**

Symmetrical encryption là loại mã hóa trong đó chỉ có một khóa (**secret key**) được sử dụng để vừa mã hóa vừa giải mã thông tin ở cả trên host và client. Các thực thể giao tiếp thông qua mã hóa đối xứng phải trao đổi khóa để nó có thể được sử dụng trong quá trình giải mã. Phương pháp mã hóa này khác với asymmetrical encrytion sử dụng một cặp khóa, một khóa công khai (public key) và một khóa riêng tư (private key) được sử dụng để mã hóa và giải mã tin nhắn.

Symmetrical encrytion

Bằng cách sử dụng các thuật toán Symmetrical encryption, dữ liệu được chuyển đổi sang dạng không thể hiểu được bởi bất kỳ ai không có khóa bí mật (secret key) để giải mã nó. Khi người nhận sở hữu khóa có tin nhắn, thuật toán sẽ đảo ngược hành động của nó để tin nhắn được trả về dạng ban đầu và dễ hiểu. Khóa bí mật mà cả người gửi và người nhận đều sử dụng có thể là một mật khẩu / mã cụ thể hoặc nó có thể là chuỗi ký tự hoặc số ngẫu nhiên đã được tạo bởi trình tạo số ngẫu nhiên an toàn (RNG). Đối với mã hóa cấp ngân hàng, các khóa đối xứng phải được tạo bằng RNG được chứng nhận theo tiêu chuẩn ngành, chẳng hạn như FIPS 140-2.

Có hai loại thuật toán Symmetrical encryption:

- Block algorithms: Tập hợp của các bit được mã hóa trong các khối dữ liệu điện tử với việc sử dụng một khóa bí mật. Khi dữ liệu đang được mã hóa, hệ thống giữ dữ liệu trong bộ nhớ của nó đến khi các khối hoàn chỉnh.
- Stream algorithms: Dữ liệu được mã hóa khi truyền trực tuyến thay vì được giữ lại trong bộ nhớ của hệ thống.

**Asymmetrical encrytion là gì**

Asymmetrical encrytion còn được gọi là public-key cryptography, là một quá trình sử dụng một cặp khóa liên quan – một khóa công khai (public key) và một khóa riêng (private key) – để mã hóa và giải mã một tin nhắn và bảo vệ nó khỏi bị truy cập hoặc sử dụng trái phép. Khóa công khai là một khóa mật mã có thể được sử dụng bởi bất kỳ người nào để mã hóa một tin nhắn sao cho nó chỉ có thể được giải mã bởi người nhận dự kiến bằng khóa riêng của họ. Khóa riêng tư – còn được gọi là khóa bí mật – chỉ được chia sẻ với người khởi tạo khóa.

Asymmetrical encrytion

Nhiều giao thức dựa trên Asymmetrical encrytion, bao gồm giao thức bảo mật lớp truyền tải (TLS) và giao thức lớp cổng bảo mật (SSL), giúp cho HTTPS khả thi. Quá trình mã hóa cũng được sử dụng trong các chương trình phần mềm – chẳng hạn như trình duyệt – cần thiết lập kết nối an toàn qua mạng không an toàn như Internet hoặc cần xác thực chữ ký số.

Tăng cường bảo mật dữ liệu là lợi ích chính của Asymmetrical encrytion. Đây là quy trình mã hóa an toàn nhất vì người dùng không bao giờ bị yêu cầu tiết lộ hoặc chia sẻ khóa riêng tư của họ, do đó giảm nguy cơ tội phạm mạng phát hiện ra khóa cá nhân của người dùng trong quá trình truyền.

**Hashing là gì?**

Trong khi encryption là một quy trình gồm hai bước được sử dụng để mã hóa và sau đó giải mã một tin nhắn, Hashing sẽ cô đọng một tin nhắn thành một giá trị có độ dài cố định không thể thay đổi được hay còn gọi là hàm băm. Hai trong số các thuật toán Hashing phổ biến nhất trong network là MD5 và SHA-1.

Hashing

Trong SSH, các giá trị Hash chủ yếu được sử dụng để kiểm tra tính toàn vẹn của dữ liệu (dữ liệu không bị sửa đổi một cách vô tình hay cố ý) và để xác minh tính xác thực của giao tiếp. Việc sử dụng chính của các giá trị Hash trong SSH là với HMAC (Hashed Message Authentication Code). HMAC sử dụng các giá trị Hash để tạo mã HMAC. Chúng được sử dụng để đảm bảo rằng văn bản tin nhắn nhận được là nguyên vẹn và không bị sửa đổi.

**Các bản phân phối của SSH**

Các bản phân phối của SSH là gì?

Phần mềm SSH rất phổ biến hiện nay. Nó đi kèm với hầu hết các bản phân phối [**Linux**](https://vietnix.vn/linux-la-gi/), Macintosh OS X, [**Sun Solaris**](https://en.wikipedia.org/wiki/Oracle_Solaris), OpenBSD và hầu như tất cả các hệ điều hành lấy cảm hứng từ Unix khác. Microsoft Windows có rất nhiều client và server SSH, cả miễn phí và thương mại. Bạn thậm chí có thể tìm thấy nó cho PalmOS, Commodore Amiga và hầu hết các nền tảng khác.

Nhiều client SSH được lấy từ các chương trình Unix cũ được gọi là r-commands r: Rv (remote shell), rlogin (đăng nhập từ xa) và RCp (sao chép từ xa). Trong thực tế, đối với nhiều mục đích, các client SSH là các thay thế cho r-commands, vì vậy nếu bạn vẫn đang sử dụng chúng, hãy chuyển sang SSH ngay lập tức! r-commands cũ không nổi tiếng là không an toàn.

[PuTTY](https://vietnix.vn/putty/) là một triển khai mã nguồn mở của SSH, được viết với mục đích ban đầu là chỉ chạy trên Windows, nhưng hiện nay nó đã có mặt trên nhiều HĐH khác như macOS hay Unix/BSD. PuTTY từ lâu đã là một trong những lựa chọn hàng đầu để triển khai SSH trên hệ thống Windows.

Hầu hết các triển khai của SSH đều bao gồm 3 tiện ích: slogin (secure login), ssh và scp (secure copy), đây là những phiên bản được cải tiến khả năng bảo mật so với những công cụ tiền nhiệm có trong Unix: rlogin, rsh và rcp. SSH sử dụng mật mã public key để xác thực máy tính từ xa, và cho phép máy tính từ xa xác thực người dùng nếu cần thiết.

**So sánh SSH và Telnet**

[Telnet là gì:](https://vietnix.vn/telnet-la-gi/) Telnet là một trong những giao thức ứng dụng Internet lâu đời nhất, cùng với FTP. Telnet được sử dụng để khởi tạo và duy trì các phiên giả lập terminal trên một host ở xa.

SSH và Telnet có những sự tương đồng nhất định về mặt chức năng, tuy nhiên điểm khác biệt lớn nhất là SSH sử dụng mật mã public key để xác thực terminal session, đồng thời mã hóa các lệnh và đầu ra của phiên.

Mặt khác, Telnet chủ yếu dùng cho giả lập terminal, còn SSH thì dùng để giả lập terminal – tương tự như rlogin command – cũng như để gửi các lệnh từ xa bằng rsh, truyền file bằng SFTP và tunnel nhiều ứng dụng khác.

|**SSH**|**Telnet**|
| :-: | :-: |
|Chạy trên port 22|Chạy trên port 23|
|Giao thức rất an toàn|Giao thức không an toàn|
|Mã hóa bằng Public Key|Truyền bằng văn bản thuần túy|
|Phù hợp với Public Network|Phù hợp với Private Network|
|Tất cả hệ điều hành|Linux/Windows|

**So sánh SSH và SSL/TLS**

SSH và TLS/SSH

Giao thức TLS (Transport Layer Security) cập nhật giao thức SSL để cung cấp bảo mật cho việc truyền mạng ở lớp truyền dẫn (transport layer). Giao thức SSH cũng hoạt động ở trong hoặc trên transport layer, nhưng hai giao thức này không hoàn toàn giống nhau.

Dù cả hai giao thức đều dựa vào các public/private key pair để xác thực host, nhưng theo TLS, chỉ server mới được xác thực bằng key pair. Còn SSH dùng một key pair riêng biệt để xác thực từng kết nối: một key pair cho kết nối từ máy cục bộ đến máy ở xa, và key pair còn lại sẽ xác thực ngược lại.

Ngoài ra, TLS cho phép mã hóa các kết nối mà không cần xác thực, hoặc được xác thực mà không cần mã hóa; còn SSH sẽ mã hóa và xác thực mọi kết nối.

Bên cạnh đó, SSH cũng cung cấp cho các chuyên gia IT và infosec một cơ chế an toàn để quản lý SSH client từ xa. Thay vì yêu cầu xác thực password để khởi tạo kết nối giữa client và server, SSH tự xác thực kết nối giữa các thiết bị. Do đó, các nhân viên IT có thể kết nối với hệ thống từ xa và sửa đổi cấu hình SSH, chẳng hạn như thêm hoặc xóa các key pair của host trong file known\_hosts.

**Một số câu lệnh SSH**

SSH có một số triển khai từ command line hoặc thực thi ở trong script. Nếu chạy một lệnh SSH mà không có các đối số (như host đích hay user ID) sẽ trả về một danh sách các tham số của lệnh SSH cùng với các option.

Dạng cơ bản nhất của lệnh SSH là gọi chương trình và tên của host đích hay địa chỉ IP:

ssh server.example.org

Lệnh này sẽ kết nối với đích server.example.org; sau đó host đích sẽ phản hồi bằng yêu cầu nhập password cho user ID mà client đang chạy. Đôi khi, user ID cho host từ xa sẽ khác, nên lệnh cần phải được gửi bằng user ID của host từ xa như sau:

ssh remote\_host\_userID@server.example.org

Ngoài ra, SSH cũng có thể được sử dụng từ trong command line để gửi ra một lệnh trên host từ xa rồi thoát:

ssh example.org ls

Lệnh này sẽ thực hiện lệnh ls trong Unix, liệt kê tất cả nội dung của thư mục hiện tại trên host từ xa. Qua đó ta có thể thấy SSH có thể được dùng để thực hiện nhiều lệnh khác nhau trên một host từ xa. Chẳng hạn như lệnh khởi tạo một server instance, cho phép máy từ xa truy cập vào một file hay tài nguyên nào đó, sau đó terminate server sau khi truy cập vào file.

Bên cạnh ssh executable thì SSH còn có một số lệnh khác có thể dùng trong command line để thực hiện một số chức năng bổ sung như:

– sshd khởi tạo SSH server để đợi request kết nối SSH đến và enable các hệ thống được ủy quyền để kết nối đến local host.

– ssh-keygen là một chương trình tạo các key pair xác thực mới cho SSH dùng để tự động hóa các đăng nhập, triển khai SSO hay xác thực host.

– ssh-copy-id là chương trình dùng để copy, cài đặt và cấu hình SSH key trên một server để thứ động hóa các đăng nhập không password và SSO.

– ssh-agent là một chương trình trợ giúp, theo dõi các key nhận dạng và passphrases của chúng, từ đó SSH có thể lấy mã khóa mã hóa và cho phép người dùng sử dụng các key nhận dạng (identity key) khác nhau mà không cần nhập loại password hay passphrase.

– ssh-add được sử dụng để thêm key vào các SSH authentication agent, được dùng với ssh-agent để triển khai SSO bằng SSH.

– scp là một chương trình sao chép file giữa các máy tính và là một phiên bản an toàn hơn của rcp.

– sftp cũng là một chương trình cho phép sao chép file giữa các máy tính, là một phiên bản an toàn hơn của ftp. SFTP đang ngày càng trở thành cơ chế được yêu thích để chia sẻ file qua internet, thay thế cả FTP lẫn FTP/S – giao thức sử dụng FTP qua một SSL/TLS tunnel.

**SSH Tunneling**

Trong bài viết SSh là gì? Vietnix xin bổ sung thêm cho bạn về SSH tunneling hay còn được gọi là SSH port fowarding (chuyển tiếp cổng SSH), là một kỹ thuật cho phép người dùng mở một tunnel an toàn giữa local host và remote host.

SSH tunneling cho phép chuyển hướng lưu lượng mạng đến một cổng/địa chỉ IP khác để các ứng dụng trên local host có thể truy cập trực tiếp đến các remote host. Đích đến có thể nằm trên remote host SSH hay bất kỳ remote host nào khác.

SSH tunnel là một công cụ mạnh mẽ cho các admin IT, tuy nhiên những kẻ tấn công cũng có thể lợi dụng SSH tunnel để chuyển firewall mà không bị phát hiện. Vì vậy, các doanh nghiệp cần sử dụng những công cụ cho phép ngăn chặn các SSH tunnel trái phép thông qua firewall.

Trên đây là những thông tin về SSH mà chúng tôi đem lại. Hy vọng với những kiến thức này sẽ đem lại cho bạn một cái nhìn mới mẻ hơn về SSH.

[
](https://vietnix.vn/web-hosting/)
