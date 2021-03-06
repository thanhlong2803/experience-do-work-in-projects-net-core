




# ASP.NET Core - Dependency Injection

ASP.NET Core is designed from scratch to support Dependency Injection. ASP.NET Core injects objects of dependency classes through constructor or method by using built-in IoC container.

# What is the relationship between  Solid principle and Dependency injection (DI)? 
[https://github.com/thanhlong2803/experience-do-work-in-projects-net-core/blob/main/Know-and-understand/net-core/what-is-solid/README.md](https://github.com/thanhlong2803/experience-do-work-in-projects-net-core/blob/main/Know-and-understand/net-core/what-is-solid/README.md)
# What is dependency?
We are know and understand in solid principle (Dependency Inversion). 

 1. High-level modules should not import anything from low-level modules. Both should depend on abstractions, interface....
 2. Abstractions should not depend on detail. Details should depend on abstractions.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/depend.png)

***Class công an quá phụ thuộc vào 2 class ăn trộm chó và ăn trộm xe.(Sai nguyên tắt DI parttern và Solid principle )***




# What is built-in IoC container ?
IoC  is Inversion of control (Dependency Inverse ) and below screen:
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen1.png)
Code for screen above:
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/ban-ga-tuyen-thong.png)

***Một ngày đẹp trời nhà tiêu dùng thích sữa bò.Thì phải làm sao ko lẻ đập ra xây lại ko lẻ chèn code vào cái đúng . Khả năng ảnh hưởng hệ thống ko. sau này thêm 100 món  người tiêu dùng thích làm sau.***
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen2.png)
***Solution use interface to implement***
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen3.png)

![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen4.png)
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen5.png)
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/screen6.png)


# Type dependency Injection 
 -   **Inject thông qua phương thức khởi tạo:**  cung cấp các Dependency cho đối tượng thông qua hàm khởi tạo ( như đã thực hiện ở ví dụ trên) -  tập trung vào cách này vì thư viện .NET hỗ trợ sẵn
 -   **Inject thông qua setter:** tức các Dependency như là thuộc tính của lớp, sau đó inject bằng gán thuộc tính cho Depedency  `object.denpendency = obj;`
 -   **Inject thông qua các Interface**  - xây dựng Interface có chứa các phương thức Setter để thiết lập dependency, interface này sử dụng bởi các lớp triển khai, lớp triển khai phải định nghĩa các setter quy định trong interface


# What Dependency injection (DI) in Asp.Net core
.Net Core is provider libary using dependency injection (DI) `using Microsoft.Extensions.DependencyInjection;`

DI container: ServiceCollection là lớp triển khai giao diện IserviceCollection nó có chức năng quản lý các dịch vụ ***(đăng ký dịch vụ , tạo dịch vụ , tự động inject và các dependency của dịch vụ,.... )*** . ServiceCollection là trung tâm xử lý của kỹ thuật DI, nó là thành phần rất quan trọng trong ứng dụng ASP.net core.

 - Khởi tạo đối tượng ServiceCollection , sau đó đăng ký (lớp) các dịch vụ nào ServiceCollection.
 - Từ `ServiceCollection` phát sinh ra đối tượng `ServiceProvider`, từ đối tượng này truy vấn lấy ra các dịch vụ cụ thể khi cần
 
***ServiceLifetime***
Mỗi dịch vụ (lớp) khi đăng ký vào `ServiceCollection` thì có một đối tượng `ServiceDescriptor` chứa thông tin về dịch vụ đó, căn cứ vào ServiceDescriptor để ServiceCollection khởi tạo dịch vụ khi cần. Trong ServiceDescriptor có thuộc tính Lifetime để xác định dịch vụ tạo ra tồn tại trog bao lâu. Lifetime có kiểu `ServiceLifetime` (kiểu enum) có các giá trị cụ thể:
 

 - Scoped:  Một bản thực thi (instance) của dịch vụ (Class) được tạo ra cho mỗi phạm vi, tức tồn tại cùng với sự tồn tại của một đối tượng kiểu `ServiceScope` (đối tượng này tạo bằng cách gọi `ServiceProvider.CreateScope`, đối tượng này hủy thì dịch vụ cũng bị hủy).
 - Singleton: Duy nhất một phiên bản thực thi (instance of class) (dịch vụ) được tạo ra cho hết vòng đời của ServiceProvider
 - Transient:  Một phiên bản của dịch vụ được tạo mỗi khi được yêu cầu.

Right now, Khởi tạo ServiceCollection như sau
`var service = new ServiceCollection();`

Khi đã có đối tượng bạn có thể thực hiện các thao như đăng ký dịch vụ vào ServiceCollection (DI container) 
Nếu ta muốn lấy đối tượng thì thông qua `ServiceProvider` , Vì thông qua nó ta sẽ lấy được các dịch vụ đăng ký ``ServiceCollection``.

 - AddSingleton<ServiceType,  ImplementationType>() or  AddSingleton< ServiceType> => value change but return one data
 - AddTransient<ServiceType, ImplementationType>() => change data return order data
 - AddScope<ServiceType, ImplementationType>() => change data return order data if within scope
 
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/addsingleton.png)
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/addtransient.png)
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/addscoped.png)

