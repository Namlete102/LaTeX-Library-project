## Giới thiệu

\+ Trong các tài liệu viết về LaTeX, người viết thấy rằng phần tham chiếu chéo thường được viết chung, đầy đủ với phần bài học đó. Chẳng hạn như, khi người dùng học về phần toán học ta sẽ được giới thiệu luôn việc người dùng tham chiếu chéo đến phương trình toán học, định lý, định nghĩa như thế nào ? Điều này tương tự với các bài học như hình ảnh, bảng, ..vv.. 

\+ Tuy vậy, trong . . .(? nhược điểm của cách trình bày đó là gì)

\+ Theo quan điểm của người viết là nên giới thiệu người dùng các vấn đề đó trước và tổng hợp các tham chiếu đó chung một bài học sau. 

\+ Cách trình bày này có vẻ sẽ gây ra khó hiểu rất nhiều với người dùng mới bắt đầu tiếp cận đến LaTeX, tuy vậy với một tài liệu mà người viết cố gắng sắp xếp và trình bày một cách tuyến tính thì điều này sẽ rất hợp lí (? hợp lí chỗ nào chỉ ra nhé). 

\+ Tham chiếu chéo là . . . .? Chúng có tác dụng gì . . . ? 

\+ Tham chiếu bao gồm: 
+ Chương, mục, .. (chapter, section, ..vv..)
+ Số trang (page)
+ Danh sách đánh số  
+ Hình ảnh 
+ Bảng 
+ Thuật toán và mã nguồn 
+ Định lý, định nghĩa, ..vv..
+ Phương trình 
+ Tài liệu tham khảo (Bib)

\+ Quy tắc đặt tên tham chiếu chéo  

---

### Tham chiếu chéo phương trình toán học:

Trong một số trường hợp, khi người dùng viết tài liệu toán học cần [tham chiếu]() từ đoạn văn bản này đến phương trình toán học ở chế độ `display math`, mà không cần phải viết lặp lại, cũng như sẽ bị tràn ra khỏi văn bản đối với các [phương trình dài]() (? của phương trình đó ở chế độ `inline math` . . . (? viết tiếp đê)) 

Để làm được điều này, trước tiên người dùng cần phải khai báo package ở bài học [liên kết thông thường]() 

```latex 
\usepackage{hyperref}
```

Tiếp theo, để tham chiếu chéo đến phương trình toán học đó, người dùng sử dụng lệnh 

```latex
\label
```

cần phải được đặt vào trong môi trường `equation`. 

Cuối cùng là lệnh

```latex
\ref{}
```

hoặc lệnh 

```latex
\eqref{}
```

được đặt ở trong đoạn văn mà người dùng mong muốn để được tham chiếu đến phương trình có lệnh `\label` tương ứng.  

> [!NOTE]  
>  Người dùng nên để lệnh `\label` ở bên cạnh `\begin{equation}`, vì . . . (? vì sao thế nhỉ ?)

. . . .(? viết ví dụ mới yéeeeeeee)

```latex
\documentclass{article} % 
\usepackage{hyperref} % . . .
\begin{document} \label{eq:1} %
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y} 
\end{equation}
. . . \ref{}
\end{document}
```

Điểm khác biệt giữa lệnh `\ref` và lệnh `\eqref`, đó là lệnh `\eqref` sẽ được hệ thống tự động thêm dấu ngoặc tròn `()` cho số thứ tự tương ứng với phương trình được tham chiếu ở đoạn văn, còn lệnh `\ref` thì không.  

```latex
\documentclass{article}
\begin{document}
\begin{equation} \label{eq:1} % . . .
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . (\ref{eq:1}) % lệnh \ref không được hệ thống tự động đóng ngoặc tròn, mà người dùng phải tự chủ động thêm vào nếu cần.    
. . . \eqref{eq:1} % lệnh \eqref được hệ thống tự động đóng ngoặc tròn, mà người dùng không cần phải tự chủ động thêm vào. 

\end{document}
```

> [!WARNING]  
>  Nếu như người dùng để nội dung bên trong dấu ngoặc nhọn `{}` của lệnh `\ref`, cũng như là lệnh `\eqref` khác với nội dung bên trong dấu ngoặc nhọn của lệnh `\label`, thì hệ thống sẽ báo lỗi `Undefined reference`. Lúc này, ở trong trang tài liệu, đoạn văn có lệnh`\ref` (hoặc lệnh `\eqref`) sẽ xuất hiện hai lần dấu chấm hỏi `??` thay vì được hiện thị số thứ tự tương ứng với lệnh `\label` của phần toán học cần được trỏ đến. 

```latex
\documentclass{article}

\usepackage{hyperref}

\begin{document} 

\begin{equation} \label{eq:1}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . \eqref{eq:2} . . .\ref{eq:1}

\end{document}
```

Vậy nên, nội dung bên trong dấu ngoặc nhọn của lệnh `\label` và lệnh `\ref` (hoặc `\eqref`) đều phải được giống nhau. 

```latex
\documentclass{article}

\usepackage{hyperref}

\begin{document} 

\begin{equation} \label{eq:1}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . \eqref{eq:1} . . .\ref{eq:1}

\end{document}
```

> [!WARNING]  
> Nếu như người dùng để nội dung bên trong dấu ngoặc nhọn `{}` của nhiều lệnh `\label` là giống hệt nhau, thì hệ thống sẽ báo lỗi `multiply-defined labels`. 

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:1} % 
\end{equation}

\end{document}
```

>[!WARNING]
>Hơn nữa, nếu lệnh `\label` bị trùng nội dung với nhau bên trong dấu ngoặc nhọn, thì lệnh `\ref` cũng như là lệnh `\eqref` sẽ được hệ thống mặc định trỏ đến vị trí có lệnh `\label` xuất hiện gần nhất.

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:1} % 
\end{equation}

. . . \ref{eq:1} . . . 

\end{document}
```

 Vậy nên, nội dung bên trong dấu ngoặc nhọn của mỗi lệnh `\label` là phải khác nhau nhằm phân biệt các phương trình toán học.  

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:2} % 
\end{equation}

. . . \ref{eq:1} . . . 

\end{document}
```

Các chú ý trên cũng được áp dụng tương tự với các bài học tham chiếu chéo [hình ảnh](), [bảng](), ..vv..   

---
### Tham chiếu định lý, định nghĩa ..vv..: 

Để tham chiếu đến định lý, định nghĩa, trước tiên ta cần đặt lệnh 

```latex
\label{}
```

vào môi trường định nghĩa "định lý", "định nghĩa" ...vv... đó.

Để tham chiếu đến môi trường đó ta cần đặt lệnh 

```latex
\ref{}
```

vào . . . 

Ví dụ: . . .

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

% Useful packages

%  Khai báo màu đường link
\usepackage[colorlinks=true, allcolors=blue]{hyperref}

\usepackage{amsmath}
\usepackage{amsthm}

\theoremstyle{plain}
\newtheorem{theorem}{Định lý}[section]

\begin{document}

\begin{theorem}[Định lý Rolle]
    Cho hàm số $f$ liên tục trên đoạn $[a;b]$ có đạo hàm trên khoảng $(a;b)$ và $f(a) < f(b)$ khi đó tồn tại $c \in (a;b)$ sao cho $f^{'}(c) = 0$
    \label{thm:0.1}
\end{theorem}

\begin{proof}
    Xem ở đây: \url{https://artofproblemsolving.com/wiki/index.php?title=Rolle%27s_Theorem}
\end{proof}

\begin{theorem}[Định lý giá trị trung bình Lagrange]
    Cho hàm số $f$ liên tục trên đoạn $[a;b]$  có đạo hàm trên khoảng $(a;b)$ khi đó tồn tại $c \in (a;b)$ sao cho 
    \[
    f^{'}(c) = \frac{f(b) - f(a)}{b - a} 
    \]
    \label{thm:0.2}
\end{theorem}

\begin{proof}
    . . . 
\end{proof}

Như vậy, định lý \ref{thm:0.2} chính là trường hợp tổng quát của định lý \ref{thm:0.1}.

\end{document}
```

(?) Có hai vấn đề mà mình chưa giải quyết trong phần này

(1) Khi định lý bị thay đổi số thì hệ thống sẽ không được tự cập nhật dẫn đến đôi khi tham chiếu không được hợp lí. Ví dụ khi "định lý 1.1" bị thay đổi thành "định lý 1.2" thì nếu ta để `\label{1.1}` thì `\ref{1.1}` vẫn sẽ để 1.1. 

(2) Với định lý có tên dài, chẳng hạn "định lý Gauss - Wantzel" thì làm sao để `\ref` có đầy đủ tên định lý đó để tham chiếu đến tiêu đề định lý Gauss - Wantzel. 

(Ảnh Lagrange và Rolle) 

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/Theorem environments.jpg"> 

</div> 
