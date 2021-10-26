Tham khảo: https://www.youtube.com/playlist?list=PLdxDYNyqNPwFr4D_mktkbfn7FG_DvZmHb
1.	Giới thiệu về linux
kernel là trung tâm điều khiển chứa các mã nguồn mở để điều khiển hoạt động của toàn  bhệ thống

GUI (giao diện) và Kernel tách biệt, ít khi bị nỗi 

Phần mềm mã nguồn mở trên linux

Internet: apache, sendmail, BIND, Squuid, Wu-ftp

Data base: postgresql, mysQL

Office: Openoffice, Koffice

Graphics: GIMP
 
![image](https://user-images.githubusercontent.com/92305335/138793361-0257a5ec-f6e7-47eb-9564-5e7ba2db3549.png)
![image](https://user-images.githubusercontent.com/92305335/138793408-f5c00517-97a0-4ceb-9657-7db707335e13.png)
![image](https://user-images.githubusercontent.com/92305335/138793425-df84ad42-1c67-4f0f-94fd-82a1e38f367a.png)


 
 
các level hoạt động của hệ điều hành linux

trợ giúp sử dụng dòng lệnh: man + lệnh , man –-help

các lệnh thông dụng:

mkdir (tạo thư mục) touch(tạo file), cp (copy), rm (xóa), cat(đọc file ), vi(chỉnh sửa file ) 

lệnh cấp quyền trên file: chown, chgrp, chmod

lệnh tìm kiếm: find, locate

lệnh xem kích thước phân vùng: df, du

lệnh quản lý tiến trình, tình trạng hệ thống: ps, top, kill

lệnh quản lý mạng: service, ifup/ifdown, ping, traceroute, telnet

2.	Chuyển hướng dòng lệnh 
	redirect input: command <<filename
					   
vd sqlplus / as sysdba << EOF: 
			     
	redirect input 
			     
command > output (ls -al > /tmp/out.txt): tạo ra file /tmp/out.txt nếu chưa có, nếu có rồi sẽ bị ghi đè  
	
vd: ls -al thang > thang/lenhls ghi kết quả lệnh ls -al thang vào file thang/lenhls và ghi đè nếu file lenhls đã có  
	
command > >output (ls -al > /tmp/out.txt): tạo ra file /tmp/out.txt nếu chưa có, nếu có rồi sẽ ghi vào cuối file  
	
vd: ls -al thang >> thang/lenhls ghi kết quả lệnh ls -al thang vào file thang/lenhls và ghi vào cuối file  nếu file lenhls đã có 
	
       echo “centoss” >> /thang/lenhls : ghi lại phần văn bản vào cuối file 
	
echo là lệnh lặp lại phần văn bản mà người dùng cung cấp hoặc hiển thị giá trị của một số biến.

	Pipe: là khái niệm đưa ra output của lệnh này thành input của lệnh kia
	
Command1 | command2 ….: chạy lệnh 1, lấy kết quả lệnh 1 chạy tiếp lệnh 2 ….
	
Vd cat thang/lenhls | more : 
	
3.	Cài đặt phần mềm
	
Có 4 cách: 
	
-	Quản lý phần mềm bằng GUI software
	
 ![image](https://user-images.githubusercontent.com/92305335/138793438-6e83333a-384c-4d1b-8d33-dd9e9a4629a2.png)

-	RPM ( redhat package manager )
	
Kiểm tra cài đặt, xóa bỏ phần mềm bằng RPM
	
+ truy vẫn thông tin moi phần mềm 
	
rpm -qa |more
	
+ truy vấn các tập tin cấu hình phần mềm: 
	
rpm -qc tên phần mềm  --c: configuration
	
+ cài đặt 1 phần mềm: 
	rpm -ivh tên phần mềm 
+ cập nhâp 1 phần mềm
	rpm _Uvh tên phần mềm 
+ gỡ bỏ phần mềm
	rpm -e tên
nếu gỡ phần mềm còn phụ thuộc vào phần mềm khác thì thêm –nodeps
-	YUM – kiểm tra phần mềm 
yum check-update
	
+ Cập nhập danh sách các phần mềm được hỗ trợ 
	yum list updates

+ liệt kê các phần mềm đã được cài đăt
	yum list installed

+ liệt kê các phần mềm có thể cài đặt bằng YUM 
	yum list available

+ hiển thị các gói có thể cài đặt và đã được cài dăt
	Yum list ‘xxxx*	

+ xem thông tin: yum info httpd
	
+ tìm kiếm phần mềm: yum search tên (yum search httpd)
	
+ hiện thị các nhóm gói đã, có thể cài đặt:yum group list
	
+ cài đặt nhóm gói: yum group install “name group”	
	
+ cài đặt tự động phần mềm: yum install tên (yum install httpd)	 
	
+ kiểm tra cập nhập phiên bản: yum update, (Yum update httpd)
	
+ gỡ bỏ, xóa cache của yum: yum rm tên 
	
+ xóa cache: yum clear all
	
+ xem lịch sử lệnh cài đặt yum: yum history	
	
+Hiển thị danh sách kho dữ liệu: yum repolist all
	
+ bật 1 kho dữ liệu: yum-config-manager –enable tên
	
+ tắt 1 kho dữ liệu: yum-config-manager –disable tên	
	
	
-	Cài bằng source
	
Phần mềm được sử dụng kiểu GNU zip (.gz) hoặc Bzip2(bz2) .tar.gz or .tar.bz2
	
Giải nén: 	tar xvzf tên.tar.gz 
	
Hoặc 		tar xvjf tên.tar.bz2
	
Quy trình cài đặt: 
	
1, giải nén, chuyển đến thư mục của phần mềm source: -cd <extracted_dir_name>
	
2, chạy script configure, cần đọc file README, INSTALL để có những gì cần thiết: -./configure  //(cấu hình chi tiết)
	
3, build phần mêm soucrce bằng lệnh make: -make
	
4, cài đặt phần mềm: -make install
	
5, gỡ: make clean 
	
Make distclean
	
6, xóa thư mục source cài đặt: rm -rf < extracted_dir_name >

4.	Quản lý user. Group
	
 Thông tin về user lưu ở file /etc/passwd
	
 ![image](https://user-images.githubusercontent.com/92305335/138793486-ca406c25-846c-4bd5-9da9-ab4244e71e50.png)

Kiểm tra password của user ở file /etc/shadow
	
Kiểm tra password của group ở file /etc/gshadow

Tạo user, group
	
Danh sách user:Ls -l /home
	
Tạo người dùng mới user: useradd user
	
Tạo user với uid, với mô tả mặc định: useradd -u 412 -d /data/user1 user1
	
Tạo 1 nhóm mới:groupadd group1	

  
Kiểm tra user:cat /etc/passwd 
		Id user1
Kiểm tra group: at /etc/group	

Cấp mật khẩu cho user1: passwd user1
	
Xóa user1: userdel user1
	
Xóa group: groupdel group1	

Khóa user1: passwd -l user1
	
Mở khóa user1: passwd -u user1	

Thay đổi thư mục home của user: usermod -d /home/user1_new user1
	
Thay đổi nhóm của user: usermod -G group1 user1	
	
Đăng nhập vào user: su - user	

