(? vì sao đôi khi ta cần màu trong công thức toán học) 

Để viết các kí hiệu toán học có màu, người dùng có thể sử dụng lệnh `\textcolor` ở bài học [màu chữ]() hoặc cũng có thể thay thế lệnh đó bằng lệnh mới sau

```latex
\mathcolor{color}{text}
```

Tương tự như lệnh `textcolor`, người dùng có thể sử dụng các màu mặc định hoặc khác ngoài 19 màu cơ bản như đã nêu ở bài học [màu chữ]() cho lệnh `mathcolor`  

Ví dụ . . .  với công thức Euler về mối liên hệ giữa đỉnh, cạnh, mặt của khối đa diện lồi. Cụ thể, với mọi khối đa diện lồi nào, số đỉnh trừ đi số cạnh cộng với số mặt luôn cho ra kết quả là bằng 2: [^1]

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath} % for the equation* environment
\usepackage{xcolor} % for text color 

\begin{document}

\[\mathcolor{red}{V} - \mathcolor{blue}{E} + \mathcolor{green}{F} = 2\]

trong đó: 

\begin{itemize}
    \item \textcolor{red}{V}: Số đỉnh (Vertex) của khối đa diện lồi
    \item \textcolor{blue}{E}: Số cạnh (Edge) của khối đa diện lồi
    \item \textcolor{green}{F}: Số mặt phẳng (Face) của khối đa diện lồi
\end{itemize}
\end{document}
```

$$
\textcolor{red}{V} - \textcolor{blue}{E} + \textcolor{green}{F} = 2 
$$

<div align="center">

<img src="./images/Leonhard Euler.jpg" alt="Euler">

Nhà toán học người Thụy Sĩ Leonhard Euler

</div> 

--- 

## Tài liệu tham khảo: 

\[1]: Tham khảo cuốn "How to Reproduce this Book Exactly with LaTeX A Self-contained Tutorial on Writing Mathematical Notes" trang 47.  

--- 

## Footnote 

[^1]: Nguồn tài liệu tham khảo phần công thức Euler ở tạp chí Pi: [https://drive.google.com/file/d/1O_QiD8GcipW0DXclsRH7HoWUsnr9pE4y/view?usp=sharing](https://drive.google.com/file/d/1O_QiD8GcipW0DXclsRH7HoWUsnr9pE4y/view?usp=sharing))[↩︎](app://obsidian.md/index.html#fnref-10-4048b0cf606cfde1)
