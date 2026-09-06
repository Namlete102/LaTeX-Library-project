Để tạo mục lục trong tài liệu đối với một số lớp tài liệu có thể được sử dụng [lệnh phân cấp](), người sử dụng lệnh 

```latex
\tableofcontents 
```

được đặt bên trong môi trường `document` và ngay sau lệnh `\maketitle`.

Ta lấy lại đoạn mã ví dụ ở bài học [lệnh phân cấp]() và thêm lệnh `\tableofcontents` vào trong đoạn mã đó. 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents % Mục lục 

\part{Đây là phần I} 
% Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên}
% Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan}
% Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1}
% Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2}
% Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính}
% Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai}
% Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu}
% Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

Ta thấy các tiêu đề được đặt trong lệnh phân cấp đều hiển thị ở trong phần mục lục, chỉ riêng `\section*{Phương pháp nghiên cứu}` là không xuất hiện ở đó.  

Để thêm mục không đánh số (Unnumbered section) vào mục lục, người dùng sử dụng lệnh sau:

```latex
\addcontentsline{toc}{section}{Tiêu đề của phần}
```

. . . . (?)

Nếu như tiêu đề người dùng viết quá dài, chúng sẽ bị . . . khi xuất hiện ở phần mục lục như trong ví dụ dưới đây: 

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Để khắc phục vấn đề này, người dùng chỉ cần viết một tiêu đề gọn lại ở trong dấu ngoặc vuông `[]` . . .  Áp dụng điều này vào lại ví dụ trên:  

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section[Tiêu đề rút ngọn]{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Người dùng có thể thấy tiêu đề ở ví dụ . . . đã được rút ngắn, gọn gàng lại khi hiện ở phần mục lục trong trang tài liệu.   