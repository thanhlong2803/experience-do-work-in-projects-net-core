


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

# Liskov substitution principle (LSP)
Class con không nên phá vỡ các định nghĩa và hành vi của class cha.
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/overriding.png) 
 ***Tách chúng ra thành 2 interface khác nhau.***
 
 # Interface segregation principle (ISP)
 Không nên sử dụng một interface lớn cho một mục đích chung, nên tách ra thành nhiều interface nhỏ với những mục đích cụ thể.
 
 Nếu ta dồn tất cả vào 1 interface nó sẽ phình và khó maintain dư án sau này nên tách ra. Ví dụ như bên dưới sai nguyên tắc.
 
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/interface.png) 

 Ta có interface Employee chứa qa nhìu việc impliment cho nó. Chúng ta nên tách nó ra.
  ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/i_p.png) 
 
 # Dependency inversion principle (DIP)
 Module cấp cao không nên phụ thuộc vào module cấp thấp, cả 2 nên phụ thuộc vào abstraction.
 Nói một cách tóm tắt, IoC là một design pattern được tạo ra để các code tuân thủ nguyên lý Dependency Inversion. Có một vài mô hình được sử dụng để triển khai để triển khai Inversion of Control, bao gồm:

Service Locator
Events
DI (Dependency Injection)
Để hiểu rõ hơn về IoC, chúng ta có thể lấy ví dụ như sau: Giả dụ có 1 class mẹ A và hai class con B và C ( lúc này B và C sẽ được gọi là các dependencies)

Ở trong mô hình không sử dụng IoC, Class A sẽ phải khởi tạo và điều khiển hai class B và C, bất cứ thay đổi nào ở Class A cũng sẽ dẫn tới thay đổi ở Class B,C. Một thay đổi sẽ kéo theo hàng loạt các thay đổi khác, làm giảm khả năng bảo trì của code. Trong khi đó, trong mô hình sử dụng IoC, các class B và C sẽ được đưa đến độc lập so với class A thông qua bên thứ ba, do đó các class không phụ thuộc lẫn nhau mà chỉ phụ thuộc vào interface. Điều này đồng nghĩa rằng sự thay đổi ở class cấp cao không ảnh hưởng tới class cấp thấp hơn.
 
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/inversion.png) 
 
 Lớp AnTrom quá phụ thuộc vào 2 lớp con nên nguyên tắt này nói rằng ko nên để cha phụ thuộc vào con nhìu qá.
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/should_inversion.png) 
 
