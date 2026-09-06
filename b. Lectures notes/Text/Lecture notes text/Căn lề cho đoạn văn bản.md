Hệ thống LaTeX sẽ để căn lề mặc định cho đoạn văn bản là "[justified]()" (căn đều hai bên).  

Để có thể thay đổi căn lề cho đoạn văn bản, người dùng có thể sử dụng môi trường sau:
```latex
\begin{alignment type}
	Nội dung...
\end{alignment type}
```

Trong đó, alignment type có thể là:

<p align="left">
+ flushleft: Căn trái
</p>
<p align="right">
+ flushright: Căn phải
</p>
<p align="center">+ center: căn giữa</p>
Ngoài ra người dùng có thể đặt các lệnh sau: 

```latex
\raggedright % Căn trái
\raggedleft % Căn phải
\centering
```

vào trước các đoạn văn bản để được tùy chỉnh căn lề cho đoạn văn đó. 

. . . 