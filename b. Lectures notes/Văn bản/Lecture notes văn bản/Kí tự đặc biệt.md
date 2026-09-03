Thuật ngữ "kí tự đặc biệt" dùng để chỉ tất cả các kí hiệu ngoại trừ các chữ cái viết thường, in hoa, các chữ số và các kí tự ngắt nghỉ câu mà ta đã nhắc ở [kí tự thông thường](). 

Hơn nữa, các kí tự đặc biệt cũng là các kí tự mà người dùng đôi khi không thể nhập trực tiếp được từ bàn phím vào phần soạn thảo LaTeX. Vì một số kí hiệu đó đã được dành riêng để có chức năng phục vụ cho mục đích nào đó của LaTeX. 

Ví dụ như kí tự $\text{\%}$ dùng để [chú thích trong LaTeX](). Nếu như người dùng gõ trực tiếp dấu chú thích đó vào phần soạn thảo LaTeX, thì khi xuất ra trang tài liệu, chúng sẽ không được hiện hữu trong trang tài liệu, mà thay vào đó hệ thống chỉ hiểu kí tự $\text{\%}$ đó đang được dùng để chú thích trong phần soạn thảo.  

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}

% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}

% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle

% Nếu viết trực tiếp kí tự % , LaTeX sẽ hiểu đó là chú thích mà không xuất hiện ở trong trang tài liệu 

\end{document}
```

Điều này cũng tương tự đối với các kí tự sau $\textbackslash$, ...vv...

Hoặc đôi khi người dùng sẽ thấy nó còn báo lỗi nếu như người dùng gõ các kí tự đặc biệt đó một cách trực tiếp trong phần biên soạn như ví dụ về kí tự viết [toán học nội tuyến]() sau. 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}
% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}
% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle
% Nếu viết hai lần kí tự $ $, LaTeX sẽ hiểu là người dùng đang viết toán học nội tuyến (inline math)
$ $
% Nếu viết đơn lẻ kí tự &, LaTeX sẽ báo lỗi "Misplaced alignment tab character &".
& 
\end{document}
```

Nếu người dùng chạy đoạn mã trên trực tiếp trên Texlive.net hoặc Overleaf, chúng đều báo cùng một lỗi là "Misplaced alignment tab character &". 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.1.jpg"
         alt="Báo lỗi ở Texlive.net">
	<figcaption>Báo lỗi kí tự '&' ở Texlive.net</figcaption>
</figure>

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.2.jpg"
         alt="Báo lỗi ở Overleaf">
	<figcaption>Báo lỗi kí tự '&' ở Overleaf</figcaption>
</figure>

Tùy thuộc vào kí tự đặc biệt người dùng sử dụng đó mà hệ thống sẽ báo lỗi để người dùng biết nhằm khắc phục lỗi của kí tự đó. 

Để viết các kí tự đặc biệt đó xuất hiện ở trang tài liệu, người dùng cần phải thêm trước kí tự đặc biệt đó với kí tự `\`. 

Ví dụ:

```latex
\documentclass{article}
\begin{document}
% Viết kí tự đặc biệt nhờ vào dấu '\' 
\% 
\_ 
\& 
\{ 
\} 
\end{document}
```

Đối với kí tự $\textasciicircum{}$, người dùng cần phải sử dụng lệnh sau

```latex
\textasciicircum 
```

Đối với kí tự $\textbackslash$,  người dùng cần phải sử dụng lệnh sau 

```latex 
\textbackslash
```

Một số kí tự đặc biệt mà người viết khuyên người dùng có thể chỉ cần gõ một cách trực tiếp các kí tự đó thì nó vẫn sẽ xuất hiện ở trang tài liệu mà không cần phải nhớ lệnh của chúng. 

Ví dụ: 

```latex

```

Các kí tự đặc biệt ở trên được tổng hợp đầy đủ ở bảng dưới đây mà người dùng có thể tham khảo:  

(xem ở đây https://en.wikibooks.org/wiki/LaTeX/Special_Characters#Other_symbols)  