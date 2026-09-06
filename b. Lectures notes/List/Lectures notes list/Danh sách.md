Danh sách trong LaTeX bao gồm: danh sách không có thứ tự, danh sách có thứ tự và danh sách mô tả. 
## a. Danh sách không có thứ tự: 

Đối với danh sách không có thứ tự ta có lệnh sau: 

```latex
\begin{itemize} % môi trương danh sách không có thứ tự
    \item . . . % Liệt kê 
\end{itemize}
```

Ví dụ về danh sách không có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{itemize} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{itemize}
\end{document}
```
## b. Danh sách có thứ tự: 

Danh sách có thứ tự trong LaTeX là danh sách được liệt kê theo thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự mặc định 
    \item . . . % liệt kê 
\end{enumerate}
```

Ví dụ về danh sách có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
Liệt kê các loại danh sách phổ biến trong \LaTeX{} bằng môi trường \verb|enumerate|
\begin{enumerate} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{enumerate}
\end{document}
```

Nếu người dùng muốn sử dụng các . . . (`\item`) khác với mặc định mà LaTeX đưa ra, chẳng hạn thay vì liệt kê với số thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra, người dùng cũng có thể liệt kê với số thứ tự theo kiểu chữ số La Mã là I, II, III, $\dots vv \dots$ hoặc cũng có thể được thay bằng chữ cái thường hoặc in hoa. 

Để làm được điều trên, người dùng chỉ cần thêm dấu `[]` bên cạnh `\item` của môi trường danh sách có thứ tự và đặt bên trong đó là kí hiệu mà người dùng muốn thay đổi sẽ xuất hiện ở đầu mỗi phần liệt kê của danh sách này: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự
    \item[thay đổi tại đây] . . . % liệt kê
\end{enumerate}
```

Đối với các chữ cái Hy Lạp cổ đại như $\alpha, \beta, ..vv..$ hay kí hiệu toán học (xem ở phần [toán học]()), người dùng cần đặt chúng vào bên trong một cặp dấu đô la đơn  `$...$`  và cặp dấu đô la đơn này sẽ được đặt ở bên trong dấu ngoặc vuông `[]`.

Ví dụ về danh sách có thứ tự với `\item` được kí hiệu theo chữ các Hy Lạp cổ đại về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{enumerate} 
    \item[$\alpha$] Danh sách không có thứ tự
    \item[$\beta$] Danh sách có thứ tự
    \item[$\gamma$] Danh sách mô tả
\end{enumerate}
\end{document}
```

## c. Danh sách lồng nhau:

Đối với các dang sách lồng vào nhau, người dùng chỉ cần thêm một danh sách con vào phần `\item` của môi trường danh sách cha đang sử dụng. 

Chẳng hạn ta có thể lồng danh sách có thứ tự mặc định của LaTeX vào các `item` của danh sách cha là danh sách không có thứ tự : 
```latex
\begin{itemize} % danh sách cha không có thứ tự  
    \item . . . % liệt kê
    \begin{enumerate} % danh sách con có thứ tự mặc định của LaTeX 
            \item . . . % liệt kê   
        \end{enumerate}
    \item . . . % liệt kê 
\end{itemize}
```

Ví dụ về lồng nhau . . . (? tìm ví dụ)

```latex

```

## d. Danh sách mô tả: 

Danh sách mô tả dùng để . . . 

Để tạo danh sách mô tả trong LaTeX, người dùng cần sử dụng môi trường `description` với lệnh sau: 

```latex
\begin{description} 
\item[Từ khóa 1] Mô tả hoặc giải thích cho từ khóa 1. 
\item[Từ khóa 2] Mô tả hoặc giải thích cho từ khóa 2. 
\item[Từ khóa 3] Mô tả hoặc giải thích cho từ khóa 3. 
\end{description}
```