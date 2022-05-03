# C# ref vs out
Ref and out keywords in C# are used to pass arguments  [tranh luận]  x within a method  [phương pháp]  x or function. Both indicate  [biểu thị]  x that an argument/parameter is passed by reference  [thẩm quyền giải quyết]  x. By default parameters are passed to a method by value. By using these keywords (ref and out) we can pass a parameter by reference.

# Ref Keyword in C#
The ref keyword passes arguments  [tranh luận]  x by reference. It means any changes made to this argument in the method will be reflected  [phản ánh]  x in that variable when control returns to the calling method.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/ref.png)
# Out Keyword in C#
The out keyword passes arguments by reference. This is very similar to the ref keyword.
![enter image description here](https://github.com/thanhlong2803/update-image/blob/main/image4/out.png)

# Difference between Ref and Out keywords in C#

|  ref| out  |
|--|--|
| The parameter or argument  [lý lẽ]  x must be initialized  [khởi tạo]  x first before it is passed to ref. | It is not compulsory  [bắt buộc]  x to initialize a parameter  [tham số]  x or argument  [lý lẽ]  x before it is passed to an out. |
|Passing a parameter value by Ref is useful when the called method is also needed to modify  [biến đổi]  x the pass parameter.|Declaring  [Tuyên bố]  x a parameter  [tham số]  x to an out method is useful when multiple values need to be returned from a function or method.|
|It is not compulsory  [bắt buộc]  x to initialize  [khởi tạo]  x a parameter value before using it in a calling method|A parameter value must be initialized within the calling method before its use.|
|||
