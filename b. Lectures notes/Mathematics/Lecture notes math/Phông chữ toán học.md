## Nội dung bài học:  

Một số yếu tố toán học cần được trình bày bằng các kiểu phông chữ khác chẳng hạn các ký tự/ký hiệu theo một kiểu nhất định, khác nhau khi trình bày toán học. [^1] (?)

Ví dụ . . .: Người dùng có thể viết kí hiệu toán học của các tập số theo kiểu chữ đậm bảng đen (?) như tập các số tự nhiên $\mathbb{N}$, tập các số nguyên $\mathbb{Z}$, tập các số thực $\mathbb{R}$, $\dots vv \dots$ 

Để viết được các kiểu phông chữ khác nhau dành cho kí hiệu toán học, trước tiên người dùng cần phải khai báo package sau: 

```latex
\usepackage{amssymb}
```

Package `amssymb` . . . (? Giới thiệu và giải thích đôi điều gói này)

Để viết được phông chữ các kí hiệu về tập số ở ví dụ . . . trên, người dùng cần để chữ cái thường được nhập trực tiếp bàn phím đó vào lệnh

```latex
\mathbb{}
```

Với kí hiệu tập số tự nhiên ta viết như sau 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amssymb}
\begin{document}
Tập hợp các số tự nhiên được kí hiệu là $\mathbb{N}$
\end{document}
```

Áp dụng tương tự điều này lại với các tập số khác. 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amssymb}
\begin{document}
Tập hợp các số mà người dùng từng được học ở phổ thông, bao gồm: 
\begin{itemize}
	\item Tập hợp các số nguyên được kí hiệu là $\mathbb{Z}$
	\item Tập hợp các số hữu tỉ được kí hiệu là $\mathbb{Q}$
	\item Tập hợp các số thực được kí hiệu là $\mathbb{R}$
	\item Tập hợp các số phức được kí hiệu là $\mathbb{C}$
\end{itemize} 
Với . . . (? giới thiệu thêm các tập số khác như H, O)
\end{document}
```

<div align="center">
<img src="./images/Setnumber.jpg" alt="Hành tím">
</div>
<center>Ảnh lụm được ở <a href="https://www.facebook.com/photo.php?fbid=488758739928398&set=pb.100063828282373.-2207520000&type=3">Mathtasy Toán học thú vị</a></center>

Ví dụ . . . chỉ là một phần nhỏ trong một số [kiểu phông chữ khác nhau dành cho kí hiệu toán học]() mà người dùng có thể tham khảo thêm.

https://www.overleaf.com/learn/latex/Mathematical_fonts   

--- 
## Footnote: 

[^1]:  Tham khảo từ Overleaf: https://www.overleaf.com/learn/latex/Mathematical_fonts
