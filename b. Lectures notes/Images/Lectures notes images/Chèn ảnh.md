LaTeX không thể tự quản lý hình ảnh, vì vậy đầu tiên chúng ta cần sử dụng gói graphicx. Để sử dụng nó, người dùng cần thêm lệnh sau vào phần mở đầu:[^9]

```latex
\usepackage{graphicx}
```

. . . . 

```latex
\includegraphics[...]{...}
```

trong đó: 
+ Dấu ngoặc nhọn `{}` là nơi chứa hình ảnh mà người dùng muốn chèn vào tài liệu
+ Dấu ngoặc vuông `[]` là nơi mà người dùng tùy chọn (`option`) thay đổi kích thước của ảnh được chèn vào tài liệu.  
. . . 

Để canh ảnh phải hoặc trái ở lệnh `includegraphics` 

môi trường hình ảnh 

```latex
\begin{figure}[t]
\centering
\includegraphics[...]{...}
\caption{}
\label{}
\end{figure}
```

Người dùng có thể để lệnh `\caption` lên trước lệnh `\includegraphics` trong môi trường `figure` nếu muốn ghi caption trước hình ảnh 

```latex
\begin{figure}[t]
\centering
\caption{}
\includegraphics[...]{...}
\label{}
\end{figure}
```

. . . 

Để chèn nhiều hình ảnh vào cùng trong trang tài liệu, đầu tiên người dùng cần khai báo package sau:

```latex
\usepackage{subcaption}
```

sau đó người dùng sử dụng môi trường 

```latex
\begin{subfigure}{0.5\textwidth}
\includegraphics[width=0.9\linewidth, height=6cm]{mesh}
\caption{Caption 2}
\label{fig:subim2}
\end{subfigure}
```
được chèn vào trong môi trường `figure`. 

Mỗi một môi trường `subfigure` trong môi trường `figure` là một hình ảnh, ghi chú, canh chỉnh trái, phải ban đầu riêng biệt. 

. . . 

Hình ảnh được bao quanh bởi văn bản 

```latex
\begin{wrapfigure}{l}{0.25\textwidth}
    \centering
    \includegraphics[width=0.25\textwidth]{contour}
    \caption{Caption}
\end{wrapfigure}
```

Nhãn ở lệnh `label{}` trong môi trường `figure` cũng như môi trường `wrapfigure` và tham chiếu chéo đến hình ảnh bằng lệnh `\ref{}` . . . 

Với việc các caption được ghi ở lệnh `caption` trong các môi trường chèn hình ảnh trên, tài liệu LaTeX có khả năng tự động tạo danh sách hình ảnh nhờ vào lệnh sau:  

```latex
\listoffigures
```

. . .

---

## Tài liệu tham khảo: 

\[1]: Nguồn tham khảo viết chèn hình ảnh ở Overleaf bao gồm: https://www.overleaf.com/learn/latex/Inserting_Images%23Positioning#Introduction; https://www.overleaf.com/learn/latex/Positioning_images_and_tables
