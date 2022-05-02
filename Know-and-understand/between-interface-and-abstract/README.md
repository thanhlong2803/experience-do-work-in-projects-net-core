



# Difference between Abstract Class and Interface in C#
***1. Sự giống nhau của abstract class va interface***
 - Abstract class và Interface  đều không thể khởi tạo đối tượng từ chính nó.
 - Abstract class và interface đều được kế thừa hoặc thực thi phương thức hoặc properties từ các class dẫn xuất nó.
 - Abstract class và interface đều có thể implement từ một hoặc nhiều interface.
 - Abstract class và interface đều giúp code trở nên sáng sủa và gọn gàng , dễ bảo trì và nâng cấp.

***2. Sự giống nhau của abstract class va interface***
 
|  abstract class | Interface  |
|--|--|
| Có thể tạo được đối tượng thông qua lớp dẫn xuất | Không thể tạo được đối tượng từ nó hoặc từ lớp dẫn xuất |
|Vừa có thể kế thừa class và vừa có thể thực thi interface|Không thực kế thừa từ class, chỉ có thể thực thi từ interface
|Có thể khai báo field, const, constructor, destructor|Không được chứa phương thức định nghĩa |
|Lớp dẫn xuất khi kế thừa phải dung từ khóa override lúc định nghĩa|Không dùng từ khóa override implement|

