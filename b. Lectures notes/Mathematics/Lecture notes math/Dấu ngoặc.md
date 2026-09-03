
Dấu ngoặc rất phổ biến trong việc bao quát các biểu thức, toán tử trong toán học. Một số dấu ngoặc thông dụng được sử dụng, đi kèm với lệnh của chúng trong LaTeX được trình bày ở bảng dưới đây: 

|         Ký hiệu          | Tên tiếng Việt                      | Tên tiếng Anh                     | Lệnh LaTeX                                             |
| :----------------------: | :---------------------------------- | :-------------------------------- | :----------------------------------------------------- |
|         $(...)$          | Dấu ngoặc đơn                       | Parentheses (or Round brackets)   | `(...)` (nhập dấu ngoặc tròn trên bàn phím)            |
|         $[...]$          | Dấu ngoặc vuông                     | Brackets (or Square brackets)     | `[...]` (nhập dấu ngoặc vuông trên bàn phím)           |
|        $\{... \}$        | Dấu ngoặc nhọn                      | Braces (or Curly brackets)        | `\{...\}` (nhập dấu ngoặc nhọn trên bàn phím)          |
|   $\langle... \rangle$   | Dấu ngoặc nhọn góc / Ngoặc nhọn dẹt | Angle brackets                    | `\langle ... \rangle`                                  |
|     $\vert... \vert$     | Dấu trị tuyệt đối / Dấu gạch đứng   | Vertical bars (or Absolute value) | `\vert...\vert` hoặc `\|...\|` (nhập \| trên bàn phím) |
|     $\Vert... \Vert$     | Dấu chuẩn (Toán học) / Dấu gạch đôi | Double vertical bars (or Norm)    | `\Vert...\Vert` hoặc `\|\| ...\|\|`                    |
|   $\lfloor... \rfloor$   | Dấu hàm sàn / Ngoặc dưới            | Floor brackets                    | `\lfloor...\rfloor`                                    |
|    $\lceil... \rceil$    | Dấu hàm trần / Ngoặc trên           | Ceiling brackets                  | `\lceil...\rceil`                                      |
| $\ulcorner... \urcorner$ |                                     |                                   | `\ulcorner... \urcorner`                               |
|   $/...\textbackslash$   |                                     |                                   | `/...\textbackslash`                                   |

Để viết toán học ở chế độ `inline math` hoặc `display math` được bao quát bởi dấu ngoặc, người dùng chỉ cần đặt phần toán học đó vào bên trong các dấu ngoặc ở bảng trên một cách bình thường. 

Ví dụ về dấu ngoặc tròn với định lý Taylor[^1] . . . (? viết tiếp phần định lý Taylor này)

```latex
\documentclass{article}
\begin{document}
\[
f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f^{''}(a)}{2!}(x-a)^2 + \frac{f^{'''}(a)}{3!}(x-a)^3 + \dots = \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n
\]
\end{document}
```

Kết quả cho ra được sẽ là 

$$
f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f^{''}(a)}{2!}(x-a)^2 + \frac{f^{'''}(a)}{3!}(x-a)^3 + \dots = \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n
$$


<div align="center">

<img src="./images/Brooks Taylor.jpg" alt="Taylor">

Nhà toán học người Anh Brooks Taylor

</div>

Bên cạnh đó, người dùng cần lưu tâm đến một số lưu ý quan trọng sau đây khi sử dụng dấu ngoặc trong LaTeX.  

---

## 1. Nguyên tắc hiển thị dấu ngoặc nhọn `\{ \}`

Trong cú pháp của LaTeX, dấu ngoặc nhọn `{}` được mặc định nhằm sử dụng để nhóm các tham số hoặc tập lệnh lại với nhau. 

. . . 

Nếu như người dùng viết trực tiếp chúng vào phần soạn thảo LaTeX, thì dấu ngoặc nhọn đó sẽ không được hiển thị trực tiếp khi người dùng xuất bản trang tài liệu, vì hệ thống sẽ không thể phân biệt được . . . (? vì sao thế nhỉ)   

Để dễ hình dung, người dùng hãy xem qua ví dụ sau đây với tích Descartes của hai tập hợp $A$ và $B$, kí hiệu là $A \times B$ là tập hợp của các cặp $(a,b)$ trong đó $a \in A$, $b \in B$ theo thứ tự $a$ trước, $b$ sau:

```latex
\documentclass{article}
\begin{document}
\[
A \times B = { (a,b)|a \in A, b \in B }
\]
\end{document}
```

Kết quả cho ra được sẽ là 

$$A \times B = { (a,b)|a \in A, b \in B }$$

Người dùng có thể thấy, dấu ngoặc nhọn sẽ không xuất hiện nhằm bao quát thành một tập hợp. (? viết lại đoạn "nhằm bao quát thành ...")

Do đó, để hiển thị được dấu ngoặc nhọn trong trang tài liệu, người dùng bắt buộc cần phải thêm dấu gạch chéo ngược `\`, mà người viết đã đề cập ở bài học [kí tự đặc biệt]() vào ngay trước chúng.

```latex
\documentclass{article}
\begin{document}
\[
A \times B = \{(a,b)|a \in A, b \in B\}
\]
\end{document}
```

Kết quả nhận được từ ví dụ trên lúc này sẽ là: 

$$
A \times B = \{(a,b) | a \in A, b \in B\}
$$

<div align="center">

<img src="./images/Rene Descartes.jpg" alt="Descartes">

Nhà toán học và triết gia người Pháp René Descartes

</div>

---

## 2. Quy tắc tự động thay đổi kích thước (Auto-resizing)

Nếu phương trình toán học có các biểu thức được chứa bên trong dấu ngoặc là [phân số]() ($\frac{a}{b}$), [tích phân]()($\int$), [số mũ]() ($a^x$) . . . vv. . . (? như thế nào đó so với dấu các dấu ngoặc), các dấu ngoặc thông thường sẽ bị quá nhỏ và mất cân đối như ở ví dụ về phương trình Friedmann thứ nhất . . .  : 

```latex
\documentclass{article}
\usepackage{amsmath} 
\begin{document}
% . . . 
\[ 
\text{H}^2 = (\frac{\dot{a}}{a})^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\] 
\end{document}
```

Kết quả lúc này cho ra được sẽ là: 

$$
\text{H}^2 = (\frac{\dot{a}}{a})^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
$$

Người dùng có thể thấy, dấu ngoặc tròn `()` ở mỗi bên phân số $\dfrac{\dot{a}}{a}$ không được tự điều chỉnh kích thước sao cho phù hợp với kích thước của phân số đó. 

Để dấu ngoặc có thể tự động co giãn và bao quát trọn vẹn đều hai bên theo chiều cao của phần công thức bên trong, người dùng hãy thêm lệnh `\left` và `\right` vào ngay trước mỗi bên của dấu ngoặc tương ứng. Trong đó, lệnh `\left` phải được viết trước lệnh `\right`. 

Để người dùng dễ hình dung, người viết giả sử rằng người dùng muốn dấu ngoặc nhọn được tự động co giãn đều hai bên . Người dùng cần phải đặt lệnh `\left` vào trước dấu `{`, rồi sau đó mới đến lệnh `\right` vào trước dấu `}`, trong đó lệnh `\left` viết trước lệnh `\right` :  

```latex
\left{ . . . \right}
```

Hai lệnh `\left`, `\right` chỉ có thể được sử dụng ở bên trong lệnh và môi trường viết toán học. 

```latex
\[\left{ . . . \right}\]
```

Áp dụng các điều trên vào lại ví dụ . . ., ta được :

```latex
\documentclass{article}
\usepackage{amsmath} % 
\begin{document}
\[ 
\text{H}^2 
= \left ( \frac{\dot{a}}{a} \right)^2 % . . .
= \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
\end{document}
```

Kết quả cho ra được lúc này sẽ là: 

$$
\text{H}^2 = \left( \frac{\dot{a}}{a} \right)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
$$

>[!WARNING]
>Nếu như người dùng đã viết lệnh `\left` mà thiếu lệnh `\right`, thì hệ thống LaTeX sẽ báo lỗi **Missing \right. inserted.** 

Giả sử, người dùng viết thiếu lệnh `\right` vào trước dấu `)`: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[ 
\text{H}^2 
= \left( \frac{\dot{a}}{a})^2 %  
= \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
\end{document}
```

(? . . . Ảnh báo lỗi)

>[!WARNING]
>Nếu như người dùng đã viết lệnh `\right` mà viết thiếu lệnh `\left`, thì hệ thống LaTeX sẽ báo lỗi **Extra \right** 

Giả sử người dùng viết thiếu lệnh `\left` vào trước dấu `)`: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[ 
\text{H}^2 
= ( \frac{\dot{a}}{a})^2 \right) %  
= \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
\end{document}
```

(? . . . Ảnh báo lỗi)

>[!WARNING]
>Nếu như người dùng cố ý hoán đổi vị trí xuất hiện trước sau của hai lệnh `\left` và `\right`, nghĩa là lệnh `\right` được viết trước lệnh `\left`, thì hệ thống sẽ báo hai lỗi là **Missing \right inserted** và **Extra \right** cùng lúc. 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[ 
\text{H}^2 
= \right( \frac{\dot{a}}{a} \left)^2  % 
= \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
\end{document}
```

(? . . . Ảnh báo lỗi) 

Vì hệ thống lúc này đang hiểu lệnh `\right` ở dòng . . . đang thiếu lệnh `\left` nên sẽ báo lỗi ở chú ý . . .. Còn lệnh `\left` ở dòng . . .  đang thiếu lệnh `\right` nên hệ thống sẽ báo lỗi ở chú ý . . . .

Các chú ý trên cũng được áp dụng tương tự với tất cả các dấu ngoặc khác. 

Một cách khác để chỉnh các dấu ngoặc,  bằng các lệnh thủ công sau: 

```latex
\big \Big \bigg \Bigg
```
. . .  

```latex
\[
\text{H}^2 = \bigg( \frac{\dot{a}}{a} \bigg)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
\]
```

Kết quả lúc này nhận được cũng sẽ tương tự với việc người dùng sử dụng hai lệnh `\left` và `\right` lần lượt vào trước mỗi bên dấu ngoặc tròn `()` của phân số $\dfrac{\dot{a}}{a}$: 

$$
\text{H}^2 = \Big( \frac{\dot{a}}{a} \Big)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}
$$

Nhược điểm của cách này nằm ở việc người dùng . . . .(? nhược điểm của cách này là gì ? vì sao ?). Tuy vậy, các lệnh `\big`, `\Big`, `\biggg`, `\Bigg` rất hữu ích trong việc người dùng sử dụng chúng để canh chỉnh dấu ngoặc trong khi viết . . . (? viết gì) vào trong kí hiệu [đạo hàm](), . . . có thể thay thế rất tốt hai lệnh `\left` và `\right`.  

<div align="center">

<img src="./images/Friedmann.jpg" alt="Friedmann">

Nhà vũ trụ học và nhà toán học người Nga Alexander Friedmann

</div>



---

## 3. Cú pháp dấu ngoặc một bên 

Trong nhiều trường hợp viết toán học như biểu diễn hệ phương trình, điều kiện xét hàm số,  $\dots vv \dots$ , người dùng sẽ cần một dấu ngoặc lớn mở ở bên trái nhưng lại không có ở bên phải. 

Hoặc ngược lại là người dùng sẽ cần một dấu ngoặc lớn mở ở bên phải nhưng lại không có ở bên trái như khi gom nhiều điều kiện giả thiết độc lập trong chứng minh hình học/đại số để suy ra một kết luận chung, hoặc khi định nghĩa hàm số phân nhánh theo chiều ngược $\dots vv \dots$

Để xử lý cấu trúc này, người dùng vẫn sẽ dùng cặp lệnh `\left` và `\right`, nhưng ở phía không cần hiển thị dấu ngoặc nhọn, người dùng hãy thay ký hiệu dấu ngoặc bằng một dấu chấm `.` 

Trường hợp 1 với việc hiển thị dấu ngoặc lớn mở ở bên trái nhưng không có ở bên phải ta có:

```latex
\left \{
. . . 
\right.
```

Trường hợp 2 với việc hiển thị dấu ngoặc lớn mở ở bên phải nhưng không có ở bên trái ta có:

```latex
\left.
. . .
\right \}
```

Và bên trong lệnh của cả hai trường hợp đó, người dùng cần thêm môi trường `matrix` sau

```latex
\begin{matrix} 
. . . 
\end{matrix}
```

Ví dụ . . .  với dãy số Fibonacci được xác định bởi hệ thức truy hồi tuyến tính 

```latex
\documentclass{article}
\begin{document}
\[
\left\{
    \begin{matrix}
		u_1 = 1 \\ 
		u_2 = 1 \\ 
		u_{n} = u_{n-1} + u_{n-2}, \ \forall n \geq 3  
    \end{matrix}
\right.
\]
\end{document}
```

Kết quả cho ra được sẽ chỉ xuất hiện một dấu ngoặc nhọn lớn duy nhất che phủ ở bên trái của .  .  .

$$
\left\{
    \begin{matrix}
		u_1 = 1 \\ 
		u_2 = 1 \\ 
		u_{n} = u_{n-1} + u_{n-2}, \ \forall n \geq 3  
    \end{matrix}
\right.
$$

Hoặc người dùng cũng có thể sử dụng môi trường `cases` sau:

```latex
\begin{cases}
. . .
\end{cases}
```

Trước đó, người dùng nhớ hãy khai báo package `amsmath`, thì mới sử dụng được môi trường `cases`.  

Viết lại ví dụ . . . trên bằng môi trường `cases`: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{cases} % không cần phải thêm môi trường matrix 
	u_1 = 1 \\ 
	u_2 = 1 \\ 
	u_{n+1} = u_n + u_{n-1}, \forall n \geq 2  
\end{cases}
\]
\end{document}
```

Kết quả cho ra được vẫn sẽ tương tự với kết quả ta có được ở trên (? viết lỗi nhóe). 

$$
\begin{cases} % không cần phải thêm môi trường matrix 
	u_1 = 1 \\ 
	u_2 = 1 \\ 
	u_{n+1} = u_n + u_{n-1}, \forall n \geq 2  
\end{cases}
$$

<div align="center">

<img src="./images/Fibonacci.jpg" alt="Fibonacci">

Nhà toán học người Ý Fibonacci

</div>

. . . (viết tiếp ví dụ với dấu ngoặc lớn hiển thị ở bên phải mà ko có ở bên trái) 

Tham khảo: https://gemini.google.com/app/4475fd095760fba9?hl=vi   

--- 

## Tài liệu tham khảo: 

\[1]:  Nguồn tham khảo viết ở Overleaf: https://www.overleaf.com/learn/latex/Brackets_and_Parentheses  

---

## Footnote: 

[^1]: Công thức tham khảo từ: https://mathworld.wolfram.com/TaylorSeries.html 
