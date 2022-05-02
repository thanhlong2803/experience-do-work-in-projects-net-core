



# Between readonly and const #

***Difference between readonly and const keyword in C#***
 
***Explain  Readonly in The C#***
 1. Runtime
 2. The value of readonly can be changed
 3. It can not declare insde method
 4.  We can assign the value in constructor
 5. It can be used with static modifier

***Explain  Const in The C#***

 6. Compile time
 7. The value can not changed
 8. It can be declared inside method
 9. We can only assign value in decleration part
 10. Can not be used with static method


ReadOnly

 1. Trường ReadOnly có thể được khởi tạo trong declaration hoặc
   constructor.
 2. Một khi bạn khởi tạo trường aReadonly, không thể gán lại nó.
 3. Có thể sử dụng tùy chỉnh static cho trường ReadOnly
 4. Tùy chỉnh ReadOnly có thể được dùng với các kiểu tham chiếu
 5. Tùy chỉnh ReadOnly chỉ có thể được dùng cho trường instance hoặc
   static,
 6. không thể dùng từ khóa ReadOnly cho các biến trong các phương thức.
 
Const
 1. Constants mặc định sẽ là static
 2. Chúng phải có giá trị
 3. Có thể được khai báo trong functions.
 4. Được sao chép vào mỗi assembly sử dụng chúng.
 5. Có thể được sử dụng trong các thuộc tính.

