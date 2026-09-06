
Trong LaTeX, các lớp tài liệu học thuật như **`article`** (bài báo) hay **`report`** (báo cáo), luôn có phần được gọi “tóm tắt”.

Để viết phần tóm tắt, người dùng cần sử dụng môi trường `abtract` với cú pháp sau. 

```latex
\begin{abstract}
    ... Nội dung tóm tắt của bạn viết tại đây ...
\end{abstract}
```

<div align="center">
    <img src="./img abstract/img4.1.jpg"> 
</div>

Môi trường `abstract` này được đặt ngay sau lệnh `\maketitle`.

> [!WARNING]  
> Môi trường `abstract` này không thể được thực thi với các lớp tài liệu là `book`, `letter`, $\dots vv \dots$

Nếu như người dùng muốn thay đổi tiêu đề mặc định của LaTeX là "tóm tắt nội dung" (tiếng Việt) hay "abstract" (tiếng Anh), người dùng cần sử dụng lệnh sau: 

```latex
\renewcommand{\abstractname}{New Name}
```

Với lệnh này, tiêu đề ở phần tóm tắt sẽ được thay thế bằng bất kỳ từ nào khác mà người dùng cung cấp.  

Ví dụ minh họa về phần tóm tắt vào trong một tài liệu. 

```latex
\documentclass{article} 
\usepackage[utf8]{vietnam} % Khai báo tài liệu viết Tiếng Việt

% Khai báo thông tin tài liệu
\title{An Example of LaTeX Document} 
\author{Namlete} 
\date{May 30, 2026} 

\begin{document} 

% 1. Hiển thị tiêu đề, tác giả, ngày tháng bài viết 
\maketitle 

% 2. Hiển thị phần tóm tắt bài viết
\renewcommand{\abstractname}{Tóm tắt} % Thay đổi dòng "Tóm tắt nội dung" mặc định thành "Tóm tắt". 

\begin{abstract} 
    Đây là nơi bạn viết một đoạn tóm tắt ngắn gọn (khoảng 150-250 từ) 
    về mục tiêu, phương pháp và kết quả chính của bài nghiên cứu này.
\end{abstract} 

% 3. Nội dung chính của tài liệu
Hello LaTeX! 

\end{document}
```

(? Ảnh)
