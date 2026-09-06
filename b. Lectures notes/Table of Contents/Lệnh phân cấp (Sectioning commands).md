Đối với các lớp tài liệu (`documentclass`) như `article`, `proc`, `report`, `book`, `beamer`, chúng đều có các lệnh phân cấp nhằm tạo [mục lục]() để sắp xếp nội dung. 

Các lệnh phân cấp này không đứng ngang hàng với nhau, mà được sắp xếp theo một thứ tự ưu tiên từ cao xuống thấp

| Tên (Việt - Anh)              | Lệnh           | Cấp độ |
| :---------------------------- | -------------- | ------ |
| Phần (Part)                   | `\part{}`      | -1     |
| Chương (Chapter)              | `\chapter{}`   | 0      |
| Mục (Section)                 | `\section`     | 1      |
| Tiểu mục (Subsection)         | `\subsection{}`| 2      |
| Tiểu tiểu mục (Subsubsection) | `\subsubsection{}` | 3|
| Paragraph (Đoạn văn (có tiêu đề))| `\paragraph{}`  |  4 |
| Subparagraph (Đoạn văn (có tiêu đề) cấp nhỏ hơn)|`\subparagraph{}`| 5|

Tùy thuộc vào `documentclass` mà người dùng đang sử dụng mà thứ tự cấp độ ở bảng trên sẽ có chút thay đổi. 

Cụ thể, lệnh `\chapter` chỉ khả dụng trong các lớp tài liệu là `report` và `book`, mà không thể được sử dụng đối với lớp tài liệu là `article`, `proc`. 

Nếu như người dùng cố gắng viết lệnh `\chapter` vào phần soạn thảo LaTeX đang ở lớp tài liệu như `article`, `proc`, thì hệ thống sẽ báo lỗi khi người dùng biên dịch sang tài liệu. (lỗi gì nhỉ ?)

Đối với lớp tài liệu là `beamer`, các lệnh `\chapter`,  `\paragraph`,  `\subparagraph` không thể được thực thi. 

Một số lớp tài liệu như `minimal`, `letter` được thiết kế cho các mục đích rất tối giản, do đó chúng loại bỏ hầu hết hoặc toàn bộ các lệnh phân cấp. (? đoạn này còn mơ hồ quá, rốt cuộc nếu bỏ hầu hết thì còn những gì ? nếu vậy thì bỏ đoạn toàn bộ các lệnh phân cấp . . .)

Các tiêu đề được viết trong các lệnh phân cấp này sẽ được hệ thống hoàn toàn tự động đánh số ở trước nó như trong ví dụ sau đây đối với lớp tài liệu là `book`: 

```latex 
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section{Phương pháp nghiên cứu} % Vì thuộc Chương 2 nên mục này sẽ tự động được đánh số là: 2.1 Phương pháp nghiên cứu
Đây là mục đầu tiên của chương 2.

\end{document}
```

Nếu như người dùng không muốn các tiêu đề trước nó được đánh số, người dùng chỉ cần thêm dấu `*` vào trong giữa lệnh phân cấp và dấu ngoặc nhọn `{}` của lệnh đó. 

Để dễ hình dung, ta quay lại với ví dụ ở trên. Nếu như người dùng thêm dấu `*` vào giữa lệnh `\section` và dấu ngoặc nhọn đang chứa tiêu đề là "Phương pháp nghiên cứu" 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu} % Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

thì tiêu đề của mục "Phương pháp nghiên cứu" ở chương 2, sẽ chỉ hiển thị chữ **"Phương pháp nghiên cứu"** mà không có số `2.1` ở phía trước như trong đoạn mã trước đó. 
