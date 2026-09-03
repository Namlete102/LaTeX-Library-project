Viết toán học luôn là chủ đề yêu thích của tác giả, vậy nên có lẽ sẽ hợp lý nếu như tác giả vừa giới thiệu phần chủ đề toán học, cũng như là cách viết các kí hiệu toán học đó trên LaTeX thì sẽ một công đôi việc, mang đến cảm giác thú vị đến người đọc.

Trước tiên, người viết cần làm rõ cấu trúc viết . . . 

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/LoveMath.jpg">

Keep calm and love math

</div>


---

## Toán tử:  

Là gì ? Như thế nào ? Đọc như nào ?  Khi nào ? 

Các toán tử cơ bản: 

\+ Các dấu +, -, /, = có thể được nhập trực tiếp bàn phím. 
\+ Dấu $\times$ được viết ở LaTeX sẽ là 

```latex
\times
```

\+ Dấu $\cdot$ được viết ở LaTeX là 

```latex
\cdot
```

\+ Dấu $\div$ được viết ở LaTeX là 

```latex
\div
```

\+ Một số toán tử nhị phân (Binary Operators) 

```latex
\otimes, \oplus, \cup, \cap
```

$\otimes, \ \oplus, \ \cup, \ \cap$

\+ Một số toán tử quan hệ (Relation Operators)

Dấu <, > có thể được nhập trực tiếp trên bàn phím 

Dấu $\leq, \ \geq, \ \neq$

```latex
\leq, \geq, \neq
```

Dấu $\subset, \ \supset, \ \subseteq, \ \supseteq$

```latex
\subset, \supset, \subseteq, \supseteq
```

Dấu $\in, \ \notin$

```latex
\in, \notin
```

Dấu $\ \approx, \simeq, \ \cong, \ \equiv, \ \vee, \ \wedge, \ \perp$

```latex
\approx, \simeq, \cong, \equiv, \vee, \wedge, \perp
```

Dấu $\boxtimes, \Box$

```latex
\boxtimes, \Box
```

---

## Liên phân số:  [^1]

Đối với một . . . (ở bài học này chúng ta sẽ học cách viết phân số, liên phân số, ...)

\+ Phân số được định nghĩa là . . .   

Ví dụ: $0.5 = \dfrac{1}{2}$ trong đó $\dfrac{1}{2}$ chính là phân số của số thập phân hữu hạn $0.5$  

Để viết được phân số, ta sử dụng lệnh : 

```latex
\frac{tử số}{mẫu số}
```

Viết lại phần số $\dfrac{1}{2}$ bằng lệnh trên 

```latex
\(\frac{1}{2}\)
```

\+  Phân số bị thu nhỏ lại khi chúng được viết chúng ở chế độ toán học nội tuyến như ví dụ . . ., để thay đổi kích cỡ phân số đó ta chỉ cần thêm trước lệnh `\frac` bằng lệnh `\displaystyle`

```latex
\(\displaystyle \frac{1}{2}\) 
```

Một cách khác để thay đổi kích thước phân số ở chế độ toán học nội tuyến giống với lệnh `\displaystyle` đó là sử dụng lệnh

```latex
\dfrac{tử số}{phân số}
```

Để sử dụng được lệnh `\dfrac`, người dùng nhớ cần phải khai báo package `amsmath` trước đó. 


---

## Giới hạn, đạo hàm, tích phân: 

\+ Đây là một chủ đề toán học thú vị được gọi chung là giải tích . . . 

\+ Khi viết kí hiệu tổng . . .  nếu viết thông thường bằng lệnh `\sum` thì kết quả cho ra được là $\sum$ (đọc là sigma) 

\+ Để thay đổi kích thước các kí hiệu toán học khi viết toán học ở chế độ `inline math` người dùng có thể sử dụng thêm bốn lệnh ở bảng sau đây: 

| Lệnh                 | Ví dụ                     | Kết quả từ ví dụ          |
| :------------------- | ------------------------- | ------------------------- |
| `\displaystyle`      | `\displaystyle(123)`      | $\displaystyle (123)$     |
| `\textstyle`         | `\textstyle(123)`         | $\textstyle (123)$        |
| `\scriptstyle`       | `\scriptstyle(123)`       | $\scriptstyle (123)$      |
| `\scriptscriptstyle` | `\scriptscriptstyle(123)` | $\scriptscriptstyle(123)$ |

vào trước lệnh `\sum` . . . kết quả cho ra được lúc này sẽ là $\displaystyle \sum$ 

\+ Một số kí hiệu khác trong bộ môn giải tích này: 

```latex
\int \oint \prod \coprod
```

$\int, \ \oint, \ \prod, \ \coprod$

$$
\sum_{i = 0}^n 
$$

\+ Đạo hàm của hàm $y = x^2$  sẽ là $y^{'} = 2x$

```latex
$y^{'}$
```

\+ Đạo hàm $y^{'} = 2x$ sẽ là $y^{''} = 2$

```latex
$y^{''}$
```

. . . 

---

## Vector, ma trận: 

(Quan trọng của phần này là cách viết phương pháp biến đổi sơ cấp) 

\+ Vector từ điểm A đến điểm B: $\overrightarrow{AB}$  

```latex
\overrightarrow{AB}
```

\+ Vector cơ sở $e$: $\vec a$

```latex
$\vec a$
```

\+ Ma trận $A$ cấp $1 \times n$ 

$$
\begin{bmatrix} 
a_{11} & a_{12} & \dots & a_{1n} 
\end{bmatrix}
$$

```latex
\[
\begin{bmatrix} 
a_{11} & a_{12} & \dots & a_{1n} 
\end{bmatrix}
\]
```

---

## Số phức:  

\+ Viết tính chất cộng hai số phức liên hợp 

$\overline{z_1} + \overline{z_2} = \overline{z_1 + z_2}$

Để viết dấu . . . ta sử dụng lệnh 

```latex 
\overline{}
```

Áp dụng điều này  . . . ta được

```latex 
\overline{z_1} + \overline{z_2} = \overline{z_1 + z_2} 
```

\+ Mũ hai số phức dạng lượng giác 
$z\cdot z = z^2 = [r \cdot (\cos(\phi) + i\sin(\phi))]^2 = r^2 \cdot (\cos(\phi)^2 + 2 \cdot \cos(\phi) \cdot i\sin(\phi) + (i\sin(\phi)^2) = r^2 \cdot (\cos(2\phi) + i \sin(2\phi))$ 
\+ Mũ $n$ số phức dạng lượng giác 

$\underbrace{z \cdot z \cdot \ldots \cdot z}_{n} = z^n = [r \cdot (\cos(\phi) + i\sin(\phi))]^n = r^n \cdot [\cos(n \phi) + i \sin (n \phi)]$

Công thức này còn được gọi là công thức De Moivre dùng để nâng một số phức dưới dạng lượng giác lên lũy thừa bậc $n$ một cách nhanh chóng.

Để viết được $\underbrace{z \cdot z \dots z}_{n}$ ta sử dụng lệnh: 
```latex
\underbrace{. . .}_{. . .}
```

trong đó: 
+  `{...}` . . .
+ `{...}` . . .

\+ Căn bậc 2 của 2 được kí hiệu là $\sqrt{2}$  

Để viết được căn bậc 2 của một số bất kì ta sử dụng lệnh 

```latex
\sqrt{}
```

Bên trong dấu ngoặc nhọn của lệnh `\sqrt` là số . . .(? viết lại)

Viết lại . . . 

```latex
\sqrt{2}
```

\+ Căn bậc 3 của 2 được kí hiệu là $\sqrt[3]{2}$

```latex
\sqrt[3]{2}
```

\+ Căn bậc $n$ của số phức 

$$
\sqrt[n]{z} = \sqrt[n]{r} \left[\cos\left(\frac{a}{n} + \frac{k2\pi}{n}\right) + i\sin\left(\frac{a}{n} + \frac{k2\pi}{n}\right) \right], \ k = \{1, 2, \dots, n\}
$$

```latex
\sqrt[n]{z} = \sqrt[n]{r} . . .
```

---
## Footnote 

[^1]:  Tham khảo từ bài tạp chí Epsilon: https://epsilonvn.github.io/archives/epsilon_vol01_2015February.pdf
