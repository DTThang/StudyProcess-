#  Các thư mục trong linux
 
Sơ đồ thư mục hệ thống linux

![image](https://user-images.githubusercontent.com/92305335/139211765-d59d17ed-6e36-4f50-bfc7-df970d18d89a.png)

 
•	/ : 

  *	Thư mục gốc, chưa tất cả file và thư mục hệ thống

  *	Chỉ người dùng root mới có quyền ghi cho thư mục này

![image](https://user-images.githubusercontent.com/92305335/139211836-ee481bad-c4ec-4e2f-a0de-0f68949fe1bf.png)


•	/boot: 

*	Chứa linux kernel, file ảnh hỗ trợ load hệ thống
 
 ![image](https://user-images.githubusercontent.com/92305335/139211889-cb55beb4-6cfe-4788-abbb-95da20f2bf99.png)


•	/bin:

o	 Chứa các tin nhị phân hỗ trợ việc boot và thi hành lệnh  
 
•	/dev: 

o	Chứa các tập tin thiết bị phần cứng, bao gồm các thiết bị đầu cuối, thiết bị được gắn vào hệ thống. Vd: cdrom, cpu, core… 
 
•	/etc: 

  *	Chứa các file cấu hình yêu cầu bởi tất cả các chương trình

  *	/etc kiểu soát cách hệ điều hành và hệ thống hoạt động
 

•	/home: 
  *	Thư mục chính của người dùng, mỗi người dùng sẽ được tạo thư mục riêng và sử dụng
 
•	/lib, /lib64: 

  *	Thứa các file thư viện chia sẻ cho các tệp tin nhị phân nằm dưới /bin và /sbin

  *	Chứa thư viện dùng chung để khởi động hệ thống và chạy các lệnh trong hệ thống tệp gốc

 
•	/media:

  *	Thư mục chứa các mount tạm thời cho các thiết bị tháo lắp

	Vd: /media/cdrom cho CD-ROM; /media/floppy cho ổ đĩa mềm; /media/cdrecorder cho ổ đĩa ghi CD

•	/mnt

  *	Thư mục mount tạm thời nơi mà người quản trị hệ thống có thể mount các tập tin hệ thống.

•	/opt

o	Chứa các ứng dụng thêm không thuộc hệ điều hành, các thư mục ứng dụng sẽ được lưu tại /otp.

Vd: viz, java 

•	/ proc: 

  *	Chứa các thông tin về tiến trình hệ thống

  *	Các tiến trình đang chạy sẽ được lưu thông tin tại đây. 

  *	Đây là các tập tin hệ thống ảo với nội đung tài nguyên hệ thống
 
•	/root:

  *	Là thư mục của người dùng root

  *	Chỉ người dùng root mới được sử dụng thư mục này 

•	/run

  *	Chứa dữ liệu của tiến trình chạy từ khi bắt đầu đến khi kết thúc

  *	/run bao gồm tệp id và tệp khóa và một số thứ khác  


•	/sbin

  *	Giống như /bin, chứa các tập tin nhị phân và  thi hành lệnh

  *	Được dùng cho quản trị viên và bảo trì hệ thống

•	/srv

  *	Srv là viết tắt của service

  *	Sử dụng cho các dịch vụ như NTS, HTTP,…

•	/sys

  *	Chứa các file giao diện phần cứng khác nhau và các tiến trình liên quan được quản lý bởi linux kernel và các tiến trình liên quan.
 
•	/usr

  *	Chứa đựng các thư mục con có tệp chương trình , thư viện cho các file chương trình và tài liệu về chúng  
 

•	/var

  *	Chứa các file có thể thay đổi kích thước như log file, mail boxet, và spool files
 
•	/tmp

  *	Thư mục chứa các tập tin tạm được tạo bởi hệ thống và người dùng

  *	Các tập tin trong thư mục này bị xóa khi hệ thống khởi động lại.
