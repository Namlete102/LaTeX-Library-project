Với việc viết một phương trình toán học, người dùng có thể sử dụng các lệnh, môi trường mà người viết đã trình bày ở hai bài học . . . (? hai bài học nào) một cách dễ dàng.  

Tuy vậy, trong trường hợp người dùng cần viết nhiều hơn nhiều phương trình cùng một lúc, chẳng hạn như phương trình Maxwell[^1] . . . 

Để làm được điều này, trước tiên người dùng nhớ cần phải khai báo package `amsmath`.  Nếu như người dùng không khai báo package đó, thì hệ thống sẽ báo lỗi . . .  (? lỗi gì)

Sau đó, người dùng chỉ cần đặt các lệnh, môi trường . . . (? lệnh, môi trường nào) vào bên trong môi trường `subequations` 

```latex
\begin{subequations}
. . .
\end{subequations}
```

Người dùng có thể để cũng như chọn tùy ý bao nhiêu . . . (? bao nhiêu về cái gì) vào bên trong môi trường `subequation`.   

Ví dụ: (với các phương trình Maxwell)

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

\usepackage{amsmath}

\begin{document}

\begin{subequations}
    \begin{align} 
        \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\ 
        \nabla \cdot \mathbf{B} &= 0 \\
        \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
        \nabla \times \mathbf{B} &= \mu_0 \left( \mathbf{J} + \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right)
    \end{align}
\end{subequations}

\end{document}
```

. . . (? Người dùng có thể sử dụng lệnh `\tag` để thay đổi số thứ tự phương trình tùy ý) 

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

\usepackage{amsmath}

\begin{document}

\begin{subequations}
    \begin{align} 
        \tag{1.1}
	    \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\ 
        \tag{1.2} 
        \nabla \cdot \mathbf{B} &= 0 \\
        \tag{1.3}
        \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
        \tag{1.4}
        \nabla \times \mathbf{B} &= \mu_0 \left( \mathbf{J} + \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right)
    \end{align}
\end{subequations}

\end{document}
```

--- 

## Footnote: 

[^1]:  Nguồn tham khảo từ tài liệu học MIT sau https://web.mit.edu/8.02t/www/802TEAL3D/visualizations/coursenotes/modules/guide13.pdf 
