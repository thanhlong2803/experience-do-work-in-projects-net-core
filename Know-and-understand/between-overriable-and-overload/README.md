


# Between ```Overriding (Ghi đè phương thức)``` and ```Overloading (Nạp chồng phương thức)``` #

***What is Overriding  in the C# ?***
    The overriding modifier is required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event.
    An override method provider a new implementtation of the method inherited from a base class.
    You cannot override a non-virtual or static method. The overridden base method must be ```virtual, abstract, or override```.
    You cannot use the new, static, or virtual modifiers to modify an override method.```compile time```
    
    For Example 
 ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/overriding.png)
 
 ***What is Overloading  in the C# ?***
 Overloading là một kĩ thuật cho phép trong cùng một class có thể có nhiều phương thức cùng tên nhưng khác nhau về số lượng tham số hoặc kiểu dữ liệu tham số ```runtime```
 
  ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/overloading.png)
  
  
  # Compare overriding and overloading 
   
  ![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/compare-overriding-overloading.png)
