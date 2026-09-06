Đầu tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{hyperref}
```

Người dùng có thể thêm liên kết đến địa chỉ web vào phần soạn thảo LaTeX bằng cách **trực tiếp** hoặc **gián tiếp** sau.

## a. Chèn liên kết trực tiếp:

Sử dụng lệnh sau:

```latex
\url{<my_url>}
```

URL sẽ được hiển thị bằng phông chữ đơn cách ([monosaced font]), và nếu người dùng nhấp vào đó, trình duyệt web sẽ mở ra và trỏ đến đúng URL mà người dùng chèn vào lệnh.

Nếu như người dùng không thích để URL hiển thị với phông chữ đơn cách và muốn chúng được in với cùng kiểu chữ với phần còn lại của văn bản, người dùng có thể sử dụng lệnh sau:

```latex 
\urlstyle{same}
```

Ví dụ đối với cách chèn link trực tiếp:

```latex
\documentclass{article} 
% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
% Useful packages
\usepackage{hyperref} % 
\urlstyle{same} % 
% 
\title{Your Paper} 
\author{You}
\date{\today}
\begin{document}
\maketitle
\url{<https://github.com/Namlete102/LaTeX-Library-project-1.0.0>} % 
\end{document}
```

## b. Chèn liên kết gián tiếp:

Sử dụng lệnh sau:

```latex
\href{<my_url>}{description}
```

Nó sẽ hiển thị phần `description` bằng phông chữ chuẩn của tài liệu khi soạn. Khi người dùng nhấp vào phần `description` đó trên tài liệu, trình duyệt web sẽ mở ra và trỏ đến đúng URL bên trong `<my_url>` mà người dùng đã dùng để chèn vào lệnh trên.

Ví dụ:
```latex
\href{<https://github.com/Namlete/LaTeX-Library-project>}{Thư viện LaTeX}
```

Cả hai cách **trực tiếp** hoặc **gián tiếp** trên đều cùng trỏ đến trang của trình duyệt web. Nhưng với cách **trực tiếp**, thì URL sẽ được hiển thị trực tiếp ngay trên tài liệu. Trong khi cách **gián tiếp** thì URL sẽ bị ẩn, thay vào đó là chỉ hiển thị `description` mà người dùng đã chèn URL vào.

Ngoài việc có thể được sử dụng để chèn liên kết đến các trang web bằng phương pháp **gián tiếp** trên, lệnh `\href` có thể được sử dụng để cung cấp đến các **liên kết địa chỉ email**, **liên kết tệp nội bộ,** **liên kết đến bất kỳ đâu trong tệp PDF đầu ra ,v**à cũng như là **chèn liên kết thủ công (Inserting links manually).**

### b.1. Liên kết địa chỉ email:

Sử dụng lệnh sau:
```latex
\href{mailto: <my_email>}{<my_email>}
```

Ví dụ:
```latex
\href{mailto: nguyenlenam15082007@gmail.com}{nguyenlenam15082007@gmail.com}
```

. . .

Xem lại tại đây: 
https://www.overleaf.com/learn/latex/Hyperlinks#Styles_and_colours 