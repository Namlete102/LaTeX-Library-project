Để thay đổi kích cỡ chữ trong trang tài liệu, người dùng chỉ cần thêm thông số vào bên trong dấu ngoặc vuông `[]` ở phần khai báo lớp tài liệu (`documentclass`). 

Xem qua ví dụ đoạn mã dưới đây:

```latex
\documentclass[12pt]{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```

người dùng có thể thấy bảy đoạn văn bản [lorem ipsum]() trong trang tài liệu đều sẽ có kích cỡ chữ là 12pt.  

Thông số được thêm vào bên trong dấu ngoặc vuông đó đối với LaTeX chỉ có thể được thay đổi đối với ba kích cỡ cơ bản là 10pt, 11pt và 12pt. 

Nếu như người dùng không thêm bất kì tùy chọn thông số nào làm thay đổi kích cỡ chữ, thì hệ thống sẽ mặc định để kích cỡ chữ trong trang tài liệu là 10pt. 

```latex
\documentclass{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```
