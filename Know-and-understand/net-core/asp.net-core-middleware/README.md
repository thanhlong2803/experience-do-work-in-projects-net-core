


 
# Giới thiệu về MiddleWare / Pipeline, áp dụng trong ASP.NET CORE

Một Middleware là một module code nó yêu cầu gởi đến request và trả về response.
- Nhận một HTTP Request gửi đến và phát sinh ra HTTP Response trả về
- Nhận một HTTP Request gửi đến, thi hành một số tác vụ có thể chuyển xong chuyển đến một middleware khác.
- Nhận HTTP Response sữa nó và chuyển đến một middleware khác
# PipeLine
Trong ứng dụng ASP.net Core các middleware kết nối lại với nhau thành một xích , Client website and mobile send http request chúng ta xử lý nó hoặc chuyển nó qua cho middleware tiếp theo hoặc nó trả về cho Http response. Chuổi middleware.
Các middleware như là các dịch vụ nhỏ, đăng ký vào ứng dụng bằng cách sử dụng đối tượng `IApplicationBuilder` 

Trong ứng dụng  `ASP.NET  CORE`, có sẵn một một loạt Middleware hoặc có thể xây dựng thêm để đưa vào một pipeline, luồng xử lý HttpRequest và trả về HttpResponse. Việc thêm Middleware vào pipeline được thực hiện ở phương thức Configure của lớp Startup. Các middleware trong pipeline xử lý các HTTP Message đều có dạng - nhận đầu vào là tham số kiểu `HttpContext`  (có chứa HttpRequest và HttpRespone), thi hành code, sau đó chuyển đến cho middleware tiếp theo.

For Example:
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/customewiddle.png)
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/errormiddleware.png)
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/put_middleware_asp_core.png)
