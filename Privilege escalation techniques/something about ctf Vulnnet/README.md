# CTF Vulnnet làm ở 4-9(T3-2024)
###  ```find / -type f -user server-management -exec ls -l {} + 2>/dev/null```

=> Lệnh này sẽ tìm kiếm tất cả các tệp trên hệ thống (bắt đầu từ thư mục gốc "/") mà có chủ sở hữu là "server-management", và sau đó hiển thị thông tin chi tiết về các tệp đó bằng lệnh ls -l. Kết quả của lệnh sẽ được in ra màn hình.

+ ```find``` Lệnh tìm kiếm trên hệ thống tệp và thư mục.
+ ```/``` Thư mục gốc để bắt đầu tìm kiếm.
+ ```-type f``` Chỉ tìm kiếm các tệp, không phải thư mục.
+ ```-u server-management``` Chỉ tìm kiếm các tệp có chủ sở hữu là "server-management".
+ ```-exec ls -l {} +``` Khi tìm thấy các tệp, thực thi lệnh ls -l trên chúng để hiển thị thông tin chi tiết.
+ ```2>/dev/null``` Chuyển hướng mọi thông báo lỗi (stderr) sang thiết bị /dev/null, nghĩa là ẩn bỏ bất kỳ lỗi nào xuất hiện trong quá trình tìm kiếm.
+ việc sử dụng ```2>/dev/null``` có thể che giấu thông báo lỗi tiềm ẩn và làm mất đi khả năng phát hiện lỗi trong quá trình tìm kiếm. Điều này có thể hữu ích trong một số trường hợp nhưng cũng đáng lưu ý.
### ```smbclient -L \\\\IP\\```

=> Lệnh này được sử dụng để liệt kê các tài nguyên được chia sẻ trên một máy chủ SMB (Server Message Block) 

+ ```smbclient``` Công cụ dòng lệnh được sử dụng để tương tác với máy chủ SMB.
+ ```-L``` Tùy chọn để yêu cầu liệt kê các tài nguyên chia sẻ trên máy chủ.
+ ```\\\\IP\\``` Địa chỉ IP của máy chủ SMB được truy cập. Ký tự " \ " được lặp lại để tránh hiểu lầm với các ký tự thoát.
### ```showmount -e IP```
=> Lệnh ```showmount``` được sử dụng để hiển thị các thư mục được chia sẻ trên một máy chủ NFS (Network File System) từ một máy tính Linux hoặc Unix khác

### ```mount -t nfs IP:/opt/conf ./files```
=>  Lệnh mount trong trường hợp này được sử dụng để gắn (mount) một thư mục được chia sẻ từ một máy chủ NFS (Network File System) vào hệ thống tệp cục bộ của bạn. Thư mục /opt/conf trên máy chủ NFS sẽ được gắn vào thư mục files trên hệ thống tệp cục bộ của bạn, cho phép bạn truy cập và làm việc với các tệp trong thư mục chia sẻ đó như thể chúng đang ở trên máy tính của bạn.
+ ```-t nfs``` Tùy chọn này chỉ định loại hệ thống tệp là NFS, nói rõ rằng bạn đang gắn một thư mục từ một máy chủ NFS.
### ```redis-cli -h IP -a "password"```
=> Lệnh này sử dụng công cụ dòng lệnh redis-cli để kết nối đến một máy chủ Redis cụ thể

### ```rsync -av rsync://rsync-connect@IP/files```
=> Lệnh này sẽ sao chép dữ liệu từ máy chủ rsync có địa chỉ IP là IP, sử dụng tên người dùng là rsync-connect, từ thư mục hoặc tệp files, và đồng bộ hóa nó với thư mục hiện tại trên máy tính của bạn.

+ ```-av``` Tùy chọn này kích hoạt chế độ verbose (hiển thị thông tin chi tiết về quá trình sao chép) và giữ quyền và thuộc tính của các tệp (bao gồm cả thư mục) như ban đầu.
+ ```rsync://rsync-connect@IP/files``` Đây là nguồn dữ liệu mà bạn muốn sao chép. Đường dẫn này có thể là một máy chủ rsync (rsync://), sau đó là tên người dùng (rsync-connect@), địa chỉ IP của máy chủ (IP), và đường dẫn đến thư mục hoặc tệp cụ thể (files).
### ```ssh-keygen -t rsa```
=> Lệnh ssh-keygen được sử dụng để tạo cặp khóa công khai và khóa riêng tư để sử dụng cho việc xác thực SSH.
+ ```ssh-keygen``` Công cụ dòng lệnh được sử dụng để tạo khóa SSH.
+ ```-t rsa``` Tùy chọn này xác định loại khóa sẽ được tạo. Trong trường hợp này, -t rsa yêu cầu tạo một cặp khóa RSA.

Khóa riêng tư (id_rsa): Đây là tệp chứa khóa riêng tư. 
Khóa công khai (id_rsa.pub): Đây là tệp chứa khóa công khai.
### ```ss -tulw```
=> Lệnh "ss" (Socket Statistics) được sử dụng để hiển thị thông tin về các kết nối mạng, các port được lắng nghe và các socket trên hệ thống.
+ ss: Là công cụ dòng lệnh để hiển thị thông tin về các kết nối mạng và các socket trên hệ thống.
+ ```-tulw``` Là các tùy chọn được sử dụng để lọc và hiển thị thông tin cụ thể:
+ -t: Hiển thị thông tin về các kết nối TCP.
+ -u: Hiển thị thông tin về các kết nối UDP.
+ -l: Chỉ hiển thị các cổng (port) mà hệ thống đang lắng nghe (listen).
+ -w: Hiển thị thông tin chi tiết về mỗi kết nối.
### ```impacket```
+ ```impacket-lookupsid``` là một công cụ trong bộ công cụ Impacket được sử dụng để truy vấn và lấy SID (Security Identifier) của người dùng hoặc nhóm từ máy chủ Windows trong mạng.
+ ```impacket-secretsdump``` là một công cụ trong bộ công cụ Impacket được sử dụng để trích xuất các bí mật và thông tin quan trọng từ máy chủ Windows trong mạng.
+ ```impacket-wmiexec``` là một công cụ trong bộ công cụ Impacket được sử dụng để thực hiện thực thi mã từ xa thông qua WMI (Windows Management Instrumentation) trên các máy tính Windows trong mạng.
### ```smbmap```
+ ```smbmap``` là một công cụ dòng lệnh được sử dụng để thực hiện quét và tìm kiếm các tài nguyên chia sẻ trên một máy chủ SMB (Server Message Block) trong mạng
### ```responder -I tun1  -wd```
=> Lệnh bạn đã cung cấp là một lệnh sử dụng công cụ Responder để lắng nghe và phản ứng với các yêu cầu LLMNR (Link-Local Multicast Name Resolution), một giao thức được sử dụng để giải quyết tên máy chủ trong mạng nội bộ. 
### Server-Side Template Injection payload
=>  kỹ thuật tấn công phổ biến được sử dụng để khai thác lỗ hổng trong các hệ thống sử dụng template engine (bộ máy dựng mẫu) để tạo và hiển thị nội dung trên máy chủ. Kỹ thuật này cho phép kẻ tấn công chèn các câu lệnh hay mã JavaScript vào trong các mẫu server-side (phía máy chủ) và thực thi chúng trên máy chủ.
