Gợi ý viết ví dụ: 
+ Sử dụng môi trường `align` để viết thuật toán Euclid để tìm UCLN của hai số là 441 và 662. Môi trường `align` này không cần đặt vào lệnh, môi trường viết phương trình toán học. Trước đó, người dùng nhớ cần phải khai báo package `amsmath`. 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{align*}
    662 &= 414 \cdot 1 + 248 \\
    414 &= 248 \cdot 1 + 166 \\
    248 &= 166 \cdot 1 + 82 \\
    166 &= 82 \cdot 2 + 2 \\ 
    82 &= 2 \cdot 41
\end{align*}
\end{document}
```

$$
\begin{align*}
    662 &= 414 \cdot 1 + 248 \\
    414 &= 248 \cdot 1 + 166 \\
    248 &= 166 \cdot 1 + 82 \\
    166 &= 82 \cdot 2 + 2 \\ 
    82 &= 2 \cdot 41
\end{align*}
$$

>[!WARNING]
>Người dùng không được để môi trường `align*` vào trong lệnh hoặc môi trường viết toán học. Nếu không, hệ thống sẽ báo lỗi . . . (? báo lỗi gì). 

+  Môi trường gather giúp khai triển các phương trình liên tiếp, căn giữa mà không cần quan tâm đến bất kỳ sự căn chỉnh nào (? chưa biết lệnh này dùng để làm gì) 

```latex
\[\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}\]
```

$$
\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}
$$

+ Môi trường split giúp khai triển chẳng hạn như ví dụ ở overleaf đây (? thay bằng một ví dụ khác về khai triển $a^n + b^n$  và ví sao không có công thức $a^2 + b^2$ )  

```latex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\[
\begin{split}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{split}
\]

\end{document}
```

$$
\begin{split}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{split}
$$