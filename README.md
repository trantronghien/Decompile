# Sơ Lượt về quá trình biên dịch và thực thi file android 

![practice-of-android-reverse-engineering-7-728](https://cloud.githubusercontent.com/assets/13708331/24585044/34f168e8-17ab-11e7-9780-12235c205cd5.jpg)

![001](https://cloud.githubusercontent.com/assets/13708331/24585046/37018474-17ab-11e7-93ae-3a4a29413023.png)

 ### khi dịch ngược ta thường thấy smali vậy smali là gì ?
 * Đây là nơi chưa toàn bộ cấu trúc dữ liệu của ứng dụng. Bên trong mục này có chứa rất nhiều file .smali khác. tất cả những gì file apk có thể kết nối được đều liên quan đến mục này. ***ai muốn hack ứng dụng hay trò chơi đều nằm ở đây.***
ngoài ra còn có các thư mục khác như: bin, src, zml, data... tùy theo mỗi file apk ( ứng dụng hay game mà nhà sản xuất viết ra).


###  Dalvik Virtual Machine  ?
+ máy ảo trên nền tảng Java cho các ứng dụng chạy được

### file deodexed ?
+ là file có chứa bộ nhớ đệm (cache) dùng bởi máy ảo Dalvik Virtual Machine (được gọi là Dalvik-cache) và được nằm trong file apk
+ deodexed có chức năng gì? Khi hệ điều hành Android khởi chạy, Davlik-cache trong máy ảo Davlik sử dụng các file .odex cho phép hệ điều hành biết trước những gì ứng dụng sẽ chạy, và do đó tăng tốc quá trình khởi động.

### file .odex , .dex(Dalvik Executable)  ?  
+ là định dạng được công cụ dx trong Android SDK biên dịch từ tất cả các file .class của java.
+ bởi vì mã nguồn java được biên dịch thành các tập tin .class chứa các mã nhị phân Java. </br>
Máy ảo Java có thể đọc được các tập tin .class nhưng Máy ảo Dalvik của android không đọc được các tập tin nhị phân Java này, một tập tin .dex chứa tổng hợp của nhiều lớp.
Tập tin dex này sẽ được dùng để chạy trên máy ảo Dalvik. 

### quá trình biên dịch 
![600_20-1index2](https://cloud.githubusercontent.com/assets/13708331/24585243/e1ba40c8-17af-11e7-8137-9b4fc1ea2cbd.jpg)

### quá trình dịch ngược 
![reverse-engineering-android-apps-10-638](https://cloud.githubusercontent.com/assets/13708331/24585249/31189e62-17b0-11e7-8e03-c2bd85a8e3fd.jpg)

![001](https://cloud.githubusercontent.com/assets/13708331/24585328/d0a80872-17b1-11e7-94e1-4231c2082f73.png)
