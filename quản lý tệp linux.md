# 1. Các thư mục trong linux
 
Sơ đồ thư mục hệ thống linux


 
•	/ : 

o	Thư mục gốc, chưa tất cả file và thư mục hệ thống

o	Chỉ người dùng root mới có quyền ghi cho thư mục này

•	/boot: 

o	Chứa linux kernel, file ảnh hỗ trợ load hệ thống
 
•	/bin:

o	 Chứa các tin nhị phân hỗ trợ việc boot và thi hành lệnh  
 
•	/dev: 

o	Chứa các tập tin thiết bị phần cứng, bao gồm các thiết bị đầu cuối, thiết bị được gắn vào hệ thống. Vd: cdrom, cpu, core… 
 
•	/etc: 

o	Chứa các file cấu hình yêu cầu bởi tất cả các chương trình

o	/etc kiểu soát cách hệ điều hành và hệ thống hoạt động
 

•	/home: 
o	Thư mục chính của người dùng, mỗi người dùng sẽ được tạo thư mục riêng và sử dụng
 
•	/lib, /lib64: 

o	Thứa các file thư viện chia sẻ cho các tệp tin nhị phân nằm dưới /bin và /sbin

o	Chứa thư viện dùng chung để khởi động hệ thống và chạy các lệnh trong hệ thống tệp gốc

 
•	/media:

o	Thư mục chứa các mount tạm thời cho các thiết bị tháo lắp

	Vd: /media/cdrom cho CD-ROM; /media/floppy cho ổ đĩa mềm; /media/cdrecorder cho ổ đĩa ghi CD

•	/mnt

o	Thư mục mount tạm thời nơi mà người quản trị hệ thống có thể mount các tập tin hệ thống.

•	/opt

o	Chứa các ứng dụng thêm không thuộc hệ điều hành, các thư mục ứng dụng sẽ được lưu tại /otp.

Vd: viz, java 

•	/ proc: 

o	Chứa các thông tin về tiến trình hệ thống

o	Các tiến trình đang chạy sẽ được lưu thông tin tại đây. 

o	Đây là các tập tin hệ thống ảo với nội đung tài nguyên hệ thống
 
•	/root:

o	Là thư mục của người dùng root

o	Chỉ người dùng root mới được sử dụng thư mục này 

•	/run

o	Chứa dữ liệu của tiến trình chạy từ khi bắt đầu đến khi kết thúc

o	/run bao gồm tệp id và tệp khóa và một số thứ khác  


•	/sbin

o	Giống như /bin, chứa các tập tin nhị phân và  thi hành lệnh

o	Được dùng cho quản trị viên và bảo trì hệ thống

•	/srv

o	Srv là viết tắt của service

o	Sử dụng cho các dịch vụ như NTS, HTTP,…

•	/sys

o	Chứa các file giao diện phần cứng khác nhau và các tiến trình liên quan được quản lý bởi linux kernel và các tiến trình liên quan.
 
•	/usr

o	Chứa đựng các thư mục con có tệp chương trình , thư viện cho các file chương trình và tài liệu về chúng  
 

•	/var

o	Chứa các file có thể thay đổi kích thước như log file, mail boxet, và spool files
 
•	/tmp

o	Thư mục chứa các tập tin tạm được tạo bởi hệ thống và người dùng

o	Các tập tin trong thư mục này bị xóa khi hệ thống khởi động lại.
