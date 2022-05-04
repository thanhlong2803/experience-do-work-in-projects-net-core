


# What is solid principle in the C#?

# ```S``` is single responsibility principle
Mỗi một class chỉ nên đảm nhận một trọng trách, và chỉ nên có một lý do duy nhất để thay đổi. Trong quá trình làm việc dân dev hay muốn 1 class mà có thể sài cho nhìu chức năng, đời không đẹp như mơ khách hàng lun thay đổi, Họ sẽ change liên tục làm cái class mình bị phình hoặc nó gồng cho chức năng khác.Nên single responsibility  khuyên rằng 1 class nên đảm nhiệm 1 chức năng thui.

For example :
Let me create a class Employee include Firsname, Lastname and Fullname.I have create a class InsertInEmployee inheritance form Employee, but I have again create Report  method in insertInEmployee , If write code add report method wrong single responsibility principle.


  ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/single-responsility.png)
Can you fix it to true with Single responsibility.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/delive-class.png)
