### **Phần 1: Phân tích**

Lỗi 1: mkdir Smart Farm Project

| mkdir : A positional parameter cannot be found that accepts argument 'Farm'. <br> At line:1 char:1 <br> \+ mkdir Smart Farm Project \+ \~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~     \+ CategoryInfo          : InvalidArgument: (:) \[mkdir\], ParameterBindingException     \+ FullyQualifiedErrorId : PositionalParameterNotFound,mkdir |
| :---- |

* Giải thích: Xảy ra lỗi khi sử dụng mkdir để tạo thư mục Smart Farm Project nhưng PowerShell hiểu Smart Farm Project là 3 tham số khác nhau. Nên PowerShell chỉ nhận mkdir thuộc tham số Smart và không nhận 2 tham số còn lại do PowerShell không tìm được lệnh gắn vào phù hợp. 

Lỗi 2: cd Smart Farm Project

| Set-Location : A positional parameter cannot be found that accepts argument 'Farm'. At line:1 char:1 \+ cd Smart Farm Project \+ \~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~\~     \+ CategoryInfo          : InvalidArgument: (:) \[Set-Location\], ParameterBindingException     \+ FullyQualifiedErrorId : PositionalParameterNotFound,Microsoft.PowerShell.Commands.SetLocationCommand |
| :---- |

* Giải thích: Xảy ra lỗi khi sử dụng cd để di chuyển vào thư mục Smart Farm Project nhưng PowerShell hiểu Smart Farm Project là 3 tham số khác nhau. Nên PowerShell chỉ nhận cd thuộc tham số Smart và không nhận 2 tham số còn lại do PowerShell không tìm được lệnh gắn vào phù hợp. 

### **Phần 2: Hoàn thiện** 

Sửa lại:

| mkdir “Smart Farm Project” |
| :---- |
| cd “Smart Farm Project” |

