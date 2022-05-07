

 
# What is Inversion of control ?
***Nguyên lý lập trình Ioc (Inversion of control) ?***
Khái nhiệm về nguyên lý lập trình inversion of control (IoC) và các mô hình triển khai từ IoC như ***Service Locator , Denpendency Injection*** 

Nguyên lý Inversion of Control là nguyên lý thiết kế trong công nghệ phần mềm trong đó các thành phần nó dựa vào để làm việc bị đảo ngược.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/ioc.png)
Triển khai nguyên lý IoC thường thực hiện bởi các Framework theo từng loại ngôn ngữ lập trình, các mô hình lập trình (pattern) triển khai từ IoC như:

- Service Locator
- Events
- DI (Dependency Inject)

![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/nguyenlyioc.png)

# Mô hình Dependency Inject - DI
Dependency injection (DI) là một mô hình triển khai từ nguyên lý IoC, là một kỹ thuật trong lập trình trong đó một đối tượng cung cấp những phụ thuộc (dependency - là đối tượng, dịch vụ, chức năng) của đối tượng khác. Injection - Bơm vào (tiêm vào) ám chỉ một phụ thuộc (đối tượng, dịch vụ) đưa vào đối tượng để đối tượng sử dụng nó.
