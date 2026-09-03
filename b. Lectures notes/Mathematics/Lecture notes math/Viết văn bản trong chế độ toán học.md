
Khi viết văn bản trong toán học, chẳng hạn . . . (nên viết lại thành một vấn đề ví dụ mới)

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
Văn bản trong toán học
\]
\end{document}
```

Kết quả cho ra được là các từ sẽ được hệ thống sắp in nghiêng và bị dính vào nhau

$$
Văn bản trong toán học 
$$

Để viết được văn bản trong toán học, người dùng cần sử dụng lệnh `\text{}` để ngăn cách phần toán học với phần văn bản.  

Áp dụng điều này vào lại ở ví dụ trên ta có 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
\text{Văn bản trong toán học}
\]
\end{document}
```

Kết quả lúc này sẽ khác hoàn toàn so với khi chưa thêm văn bản vào trong lệnh `\text`

$$
\text{Văn bản trong toán học}
$$

Bên cạnh việc viết văn bản vào trong toán học, một số hàm trong toán học chẳng hạn như hàm lượng giác, . . vv . . được khuyến nghị . . . (? bởi ai, điều gì) soạn thảo ở dạng phông chữ thẳng đứng . . . (viết sau) 

Chẳng hạn, khi viết công thức . . . , nếu như người dùng chỉ viết hàm $\cos$. $\sin$ thông thường như ở ví dụ sau đây

```latex
\[cos(2 \alpha) = cos^2(\alpha) - sin^2(\alpha)\]
```

thì người dùng có thể thấy, chúng sẽ bị in nghiêng khi xuất sang trang tài liệu. 

Theo phản xạ nhanh, người dùng sẽ đặt các hàm đó vào trong lệnh `\text`

```latex
\[\text{cos}(2 \alpha) = \text{cos}^2(\alpha) - \text{sin}^2(\alpha)\]
```

. . . (kết quả từ ví dụ)

Một cách khác để viết các hàm toán học như $\cos$, $\sin$  . . . như ở ví dụ trên một cách ngắn gọn hơn, người dùng chỉ cần thêm dấu `\` bên cạnh hàm đó: 

```latex
\[\cos(2 \alpha) = \cos^2(\alpha) - \sin^2(\alpha)\]
```

Với một số hàm toán học đã được LaTeX cung cấp . . ., nếu như người dùng sử dụng dấu `\` để viết cho một . . . khác thì chúng sẽ báo lỗi . . . (? gì)  

```latex
\[\nam\]
```

Người dùng có thể xem đầy đủ các hàm được LaTeX . . . (? LaTeX làm sao) tại [danh sách các kí hiệu toán học, chữ cái Hy Lạp]().  