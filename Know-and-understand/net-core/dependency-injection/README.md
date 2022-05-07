




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


