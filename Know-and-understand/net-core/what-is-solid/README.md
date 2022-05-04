


# What is solid principle in the C#?

# ```S``` is single responsibility principle
Mỗi một class chỉ nên đảm nhận một trọng trách, và chỉ nên có một lý do duy nhất để thay đổi. Trong quá trình làm việc dân dev hay muốn 1 class mà có thể sài cho nhìu chức năng, đời không đẹp như mơ khách hàng lun thay đổi, Họ sẽ change liên tục làm cái class mình bị phình hoặc nó gồng cho chức năng khác.Nên single responsibility  khuyên rằng 1 class nên đảm nhiệm 1 chức năng thui.

For example :
Let me create a class Employee include Firsname, Lastname and Fullname.I have create a class InsertInEmployee inheritance form Employee, but I have again create Report  method in insertInEmployee , If write code add report method wrong single responsibility principle.


  ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/single-responsility.png)
Can you fix it to true with Single responsibility.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/delive-class.png)

# Open closed principle (OCP)

***Các thành phần thoả mãn nguyên tắc Open-Closed sẽ có hai tính chất:***
 - “Open for extension”: khi cần thêm tính năng mới, ta kế thừa và mở rộng module/class có sẵn để đáp ứng yêu cầu của chương trình.
 
 - “Closed for modification”: không nên thay code của một module hoặc class có sẵn, vì nó sẽ ảnh hưởng tới tính đúng đắn của chương trình.

For Example:
**Closed for modification** : Giải thích chổ này ta có method trong 1 là getFullName(){ return name } sài 100 chổ lấy tên fullname này vì khách hàng ko bít khi nào nó change.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/close.png)


Một ngày đẹp trời khách hàm thêm tính năng đụng chạm vào hàm getEmployeeId().Quá trình làm nó mún thêm chức năng trả về string. Nếu ta đổi kiểu int qua string rất nhiều hàm bị ảnh hưởng nên khuyên nên tạo 1 class kế thừa để xây dựng cho chức năng khác.

![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/close-custom.png)

# Open closed principle (OCP)

