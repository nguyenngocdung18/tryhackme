# TRYHACKME
# 18-23/12/2023
- Rootme có một số thứ mới hơn Basic Pentest
## Basic Pentest 
- search cách truy cập smb 
- còn lại tự làm
## Root Me
- đọc write up phần nâng cao đặc quyền
# 25-30/12/2023
- Lazy Admin có 1 vài điểm mới.
## Lazy Admin
- ban đầu làm bình thường thì khi nâng cao đặc quyền không được. vẫn ở wwwdata. Đi đọc writeup mới phát hiện ra do (/bin/sh: 0: can't access tty; job control turned off)
- lúc tìm lỗi thì xem thêm được cách tạo copy bash cũng hay =)))
## Pickle Rick
- tự làm
## Simple CTF
- tự làm
# 2-6/1/2024
- Tomghost có chút lạ
## OhSINT
- xem writeup cách dùng wigle.net
- và tìm nơi anh ấy đã đi vào kỳ nghỉ nhưng blog đã không tồn tại nữa nên chỉ có thể xem qua writeup
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2219e117-fafe-4425-9c24-eb8f821d6445)
## Wgel CTF
- tự làm phần lớn
- xem writeup cách dùng (```sudo wget --use-askpass=$TF 0```) trong: 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1f419ee0-abc1-44de-978c-6078adf7214c)
## Crack the hash
- tự làm
## Brooklyn 99 
- README.md tự làm
- README2.md xem writeup (stegseek để lấy được thông tin trong ảnh)
## Cyborg
- giải xong hàm băm rồi bị chững =(( đi xem writeup
- phần nâng cao đặc quyền trong writeup nó tạo 1 user có quyền root trong passwd. làm theo nhưng mà không biết sao bị lỗi "authentication failure"
=> thấy nó thực thi backup.sh để tạo user thì nghĩ là có khi cũng lấy shell được =)) thử lại được nên chốt luôn .còn cách tạo user kia vẫn lỗi. 
## Tomghost
- đọc writeup
# 8-13/1/2024
## Agent Sudo
- tự làm
## Bounty Hacker
- tự làm
## Ignite
- đọc writeup privilege escalation
## Startup
- đọc writeup đoạn Wireshark
- hơi chưa hiểu lắm đoạn : sau khi dùng ```echo...``` để thêm vào print.sh thì mới ```cat /etc/print.sh``` (đồng thời đã ```nc -nlvp 9876``` từ trước rồi) thì đã kết nối thành công rồi :V  hơi lạ nhưng làm lại mấy lần vẫn vậy nên chắc nó có auto chạy scripts chăng =))))))
# 15-20/1/2024
## c4ptur3-th3-fl4g
- tự làm
## GamingServer
- xem writeup nâng cao đặc quyền (lxd)
## Lian_Yu
- Lúc scanning dùng gobuster với common.txt có sẵn trong linux như bình thường thì chả ra cái gì mà lab nó cứ hỏi file, dir của web là gì :)))  đi xem writeup thì thấy phải dùng từ điển "directory-list-2.3-medium.txt" (hơn 200k kết quả và 400k với extension .ticketkèm thêm =))))) lâu điên. cái này bình thường hay dùng để bruteforce mật khẩu mà ta)  mới ra được file, dir của nó...
- tìm thấy file, dir rồi thì còn lại không khó nên tự làm được 
## Anthem
- Xem writeup tên đăng nhập remote desktop ( =))) rõ ràng ở tab /umbraco/#/login dùng email đăng nhập được vào mà đăng nhập remote desktop lại không được :V hóa ra là chỉ lấy username là "SG" thôi chứ k cần cả cái email) và đoạn tìm file ẩn trên window
## Source
- Xem writeup
## EasyPeasy
- xem writeup nâng cao đặc quyền ( cat /etc/crontab)
## Archangel
-xem writeup
# 22-27/1/2024
## ColddBox: Easy
- Dùng burp suite để brute-force cái login form của wp cũng được nhưng mà đọc writeup thấy có công cụ wpscan chuyên dụng nên nó nhanh hơn =))) khá nhiều. xem cả write đoạn tìm ra cái wp-config.php để có mật khẩu của tài khoản c0ldd. 
##  Git Happens
- đọc writeup biết thêm công cụ dumper của GitTools
## Team
- xem writeup đoạn tìm openssh private key, chuyển sang user gyles, check bash_history.
## Thompson
- xem writeup dùng msfconsole lấy shell . còn lại dễ
## Overpass
- xem writeup đoạn lấy được private key. còn lại dễ
## Cat Pictures
- xem write up đoạn chạy file runme
# 29-3/2/2024
## Dav
-xem writeup đoạn nó tìm ra cái web có chứa username, password để login. còn lại dễ
## Library 
- tự làm, lâu rồi mới thấy 1 cái lab brute force mật khẩu ssh được =)))
## Plotted-TMS
- xem writeup privilege escalation.
## Tony the Tiger
- dùng cái file exploit nó cho sẵn thì không được. xem writeup kiếm cách exploit khác trên github (dùng jexboss)
# 4-9/3/2024
## Flatline
- Đọc writeup
## IDE
- xem writeup đoạn ftp :))) nó toàn . \ .. \ ... tưởng không có gì ai dè có file tên "-" sau khi ```cd ...``` =)) hơi ẩu. không check kĩ.
## Wordpress: CVE-2021-29447
- Phần I: introduce =)) gần ngang writeup rồi. không có nhiều thứ để nói
## VulnNet: Internal
- hard đội lốt easy =)))))
- xem writeup
## VulnNet: Roasted
- xem writeup
## VulnNet: Node
- đánh giá chủ quan thì nó quen hơn 2 cái VulnNet trên
- xem writeup đoạn tìm "node serialize payload" để lấy được  shell www-data =))) băn khoăn mỗi đoạn đó còn lại thì dễ
## VulnNet
- xem cách tra ra cái đường dẫn "/etc/apache2/sites-enabled/000-defdfault.conf" với đoạn sao chép các file trong /var/backups ra /tmp để có quyền giải nén file .tar.gz
## VulnNet: Active
- xem writeup 
## VulnNet: dotjar
- Cách khai thác Apache Tomcat khá giống tomghost nên cũng dễ.
- xem writeup đoạn nó tìm ra file "shadow-backup-alt.gz" trong /var/backups, còn lại lấy root thì tương tự lúc lấy web shell
## VulnNet: dotpy
- xem write kiếm được (Server-Side Template Injection)ssti exploit payload
# 18-23/3/2024
## SQL Injection
## Relevant
## Anonymous
