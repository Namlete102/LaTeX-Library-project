##  Bổ sung bài học dấu ngoặc 

. . . 

```latex
\big( \Big( \bigg( \Bigg( 
```

$\big( \Big( \bigg( \Bigg($ 

```latex
\big) \Big) \bigg) \Bigg) 
```

$\big) \Big) \bigg) \Bigg)$

. . . 


Khi viết tập hợp các số hữu tỉ $\mathbb{Q}$ được biểu diễn bằng cách chỉ rõ tính chất đặc trưng của mỗi phần tử: 

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}$$

Người dùng có thể thấy, tuy hai bên dấu ngoặc nhọn đã được tự động canh chỉnh bởi hai lệnh lần lượt là `\left` và `\right`, nhưng [kí hiệu]() `|` không được tự động căn chỉnh sao cho phù hợp với kích thước của phân số $\dfrac{a}{b}$. 

Để khắc phục được điều này, người dùng chỉ cần thêm lệnh 

```latex
\middle
```

vào trước dấu `|` đó. 

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$\mathbb{Q} = \left\{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0 \right\}$$

Lệnh `\middle` này chỉ được sử dụng trong việc giúp các kí hiệu nhằm mục đích phân cách . . . (?) có thể được tự động co giãn chiêu cao sao cho phù hợp, vừa vặn với kích thước với cặp dấu ngoặc bao quanh các phân số (như ở ví dụ trên), tích phân, tổng chuỗi, ma trận, căn thức, ..vv.. 

>[!WARNING]
>Lệnh `\middle` không thể được hoạt động một cách độc lập.  Để sử dụng được lệnh này, chúng cần được đặt vào trong hai lệnh là `\left` và `\right`. Nếu không, thì hệ thống sẽ báo lỗi **Extra \middle.**  

Giả sử, nếu ta bỏ hai lệnh `\left` và `\right` ở hai bên dấu ngoặc nhọn: 
 
```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0\]
\end{document}
```

(? Ảnh báo lỗi)

>[!WARNING]
> Ngay sau lệnh `\middle` là phải có các kí hiệu có khả năng co giãn với chiều cao tương ứng . . .(? với gì đó). Nếu không, hệ thống sẽ báo lỗi **Missing delimiter (. inserted).**

Nếu ta thay kí hiệu `|` bằng kí hiệu nằm ngang như $\rightarrow$ (? chắc phải làm một ví dụ mới)

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b} \middle \rightarrow a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$
\mathbb{Q} = \left\{\frac{a}{b} \middle \rightarrow a, b \in \mathbb{Z}, b \ne 0 \right\} 
$$

Việc người viết thay kí hiệu `|` bằng $\rightarrow$ ở ví dụ này không thật sự có ý nghĩa về mặt toán học, tuy vậy điều người viết muốn trình bày là ở chú ý . . .(? viết như c). 

---

## Tập hợp các kí hiệu có thể được nhập trực tiếp trên bàn phím 

```latex
+ - = ! / ( ) [ ] < > | ' : * 
```

$+ \ - \ = \ ! \ / \ ( \ ) \ [ \ ] \ < \ > \ | \ ' \ : \ *$

---

## Toán tử lượng giác 

```latex
\documentclass{article}
\begin{document}
\(\cos(x), \sin(x), \tan(x), \cot(x), ..vv..\)
\end{document}
```

$\cos(x), \ \sin(x), \ \tan(x), \ \cot(x), ..vv..$  

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/trigonometry iceberg.jpg" alt"trinogometry" width="80%" height="70%"> 
Tảng băng chìm toán tử lượng giác
</div>

---

## Toán tử hàm mũ 

```latex
\documentclass{article}
\begin{document}
\(\log(x)\)
\end{document}
```

$\log(x)$ 

Đối với một hàm cơ số $e$ mũ x ta có 

```latex
\documentclass{article}
\begin{document}
\(y = e^x\)
\end{document}
```

$y = e^x$ 

Ta thấy hằng số Euler $\mathrm{e}$ hơi nghiêng, để khắc phục điều này người dùng chỉ cần đặt hằng số đó vào lệnh `\mathrm`

```latex
\documentclass{article}
\begin{document}
\(y = \mathrm{e}^x\)
\end{document}
```

$y = \mathrm{e}^x$

Hàm  $y = \mathrm{e}^x$ của x này còn được viết tắt lại thành $y = \exp(x)$. Để viết kí hiệu $\exp$ trong LaTeX, người dùng chỉ cần thêm vào trước nó dấu `\`. 

```latex
\documentclass{article}
\begin{document}
\(y = \exp(x)\)
\end{document}
```

$y = \exp(x)$ 

---

## Toán tử giới hạn 

```latex
\documentclass{article}
\begin{document}
\(\lim_{x \to \infty}\)
\end{document}
```

$\lim_{x \to \infty}$

Một cách viết khác

```latex
\documentclass{article}
\begin{document}
\(\lim\limits_{x \to \infty}\)
\end{document}
```

$\lim\limits_{x \to \infty}$

---

## Ma trận 

Khai báo package 

```latex
\usepackage{amsmath}
```

Các môi trường sau đây phải được đặt viết trong các lệnh và môi trường **inline math**, **display math**. 

Sử dụng môi trường `bmatrix`

```latex
\begin{bmatrix}
. . .
\end{bmatrix} 
```

Ma trận $2 \times 2$ 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 2 \\
  3 & 4
\end{bmatrix}
\]
\end{document}
```


$$
\begin{bmatrix}
1 & 2 \\
3 & 4 
\end{bmatrix}
$$

Kí hiệu `&` dùng để phân cách (? sử dụng từ khác) các phân tử bên trong ma trận. Nếu ta không sử dụng dấu `&` ở hàng đầu tiên của ma trận, nhằm 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1  2 \\
  3 & 4
\end{bmatrix}
\]
\end{document}
```

$$
\begin{bmatrix}
  1  2 \\
  3 & 4
 \end{bmatrix}
$$

Người dùng có thể thấy, phần tử đầu tiên của hàng đầu ma trận lúc này là 12 thay vì 1, còn hàng thứ hai bị bỏ trống thay vì là 2. 

Còn kí hiệu `\\` được dùng để xuống hàng mới. 
. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 2 
  3 & 4
\end{bmatrix}
\]
\end{document}
```

Đoạn mã trên cũng tương đồng với đoạn mã sau

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 23 & 4
\end{bmatrix}
\]
\end{document}
```

Kết quả hiện thị ma trận trong trang tài liệu ở hai đoạn mã trên đều là như nhau: 

$$
\begin{bmatrix}
  1 & 2 
  3 & 4
 \end{bmatrix}
$$

Lúc này ta sẽ hiểu đây là một ma trận $1 \times 3$ (hay còn được gọi là một ma trận dòng). Có phần tử thứ nhất là 1, phần tử thứ 2 là 23 và cuối cùng phần tử thứ 3 là 4.  

Một số tài liệu toán học viết các ma trận thay vì được bao quát bởi dấu ngoặc vuông, chúng lại được bao quát bởi dấu ngoặc tròn như hình dưới đây: 

(? Ảnh minh họa cho ma trận được bao quát bởi dấu ngoặc tròn)

. . . 

```latex
\begin{pmatrix}
. . .
\end{pmatrix} 
```

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{pmatrix}
  1 & 2 \\
  3 & 4
\end{pmatrix}
\]
\end{document}
```

$$
\begin{pmatrix}
  1 & 2 \\
  3 & 4
 \end{pmatrix}
$$
. . . (định thức của một ma trận) 

```latex
\begin{vmatrix}
. . .
\end{vmatrix}
```

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{vmatrix}
  1 & 2 \\
  3 & 4
\end{vmatrix}
 \]
\end{document}
```

. . . 

$$
\begin{vmatrix}
  1 & 2 \\
  3 & 4
 \end{vmatrix}
$$

. . . (ma trận chuẩn (matrix norm))

```latex
\begin{Vmatrix}
. . .
\end{Vmatrix}
```

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{Vmatrix}
  1 & 2 \\
  3 & 4
\end{Vmatrix}
 \]
\end{document}
```

. . . 

$$
\begin{Vmatrix}
  1 & 2 \\
  3 & 4
\end{Vmatrix}
$$


$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\
       \frac{5}{6} & 0           & \frac{1}{6} \\
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$


---

## Định thức của ma trận 

Ví dụ . . .  về công thức tính định thức tổng quát của một ma trân vuông $A$ cấp $n$ được chứng minh bởi nhà toán học Leibniz  

```latex
\documentclass{article}
\begin{document}
\[det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )\]
\end{document}
```

. . . 

$$det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )$$

Ta thấy kí hiệu "det" và "sgn" bị nghiêng. LaTeX đã định nghĩa lệnh

```latex
\det
```

dùng để viết kí hiệu định thức. 

Còn kí hiệu "sgn" phải được viết trong lệnh `\operatorname`

```latex
\operatorname{sgn}
```

Từ những điều ở trên, đoạn mã lúc này được sửa có được như sau

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right)\]
\end{document}
```

$$
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right)
$$

\+ Vết của ma trận  

```latex
\operatorname{tr}(A)
```

$\operatorname{tr}(A)$

---

## Toán tử mô-đun (thường thấy ở bài học toán đồng dư thức) 

Nếu chỉ viết `\mod`

```latex
\(a \mod b\)
```

thì 

$a \mod b$

Ta viết lại thành

```latex
\bmod
```

$a \bmod b$

```latex
x \equiv a \pmod {b}
```

$x \equiv a \pmod { b }$

---

## Viết công thức tính tổ hợp chập $k$ của của $n$ 

```latex
\[\binom{n}{k} = \frac{n!}{k!(n-k)!}\]
```

$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$
$n! = 1 \cdot 2 \cdot 3 \dots \cdot (n-2) \cdot (n-1) \cdot n$  

Khai báo package: 

```latex
\usepackage{amsmath}
```

```latex
\[\tbinom{n}{k} = \frac{n!}{k!(n-k)!}\]
```

$$\tbinom{n}{k} = \frac{n!}{k!(n-k)!}$$
Ở **inline math** thì lệnh `\binom` và `tbinom` có kích thước không khác gì nhau.  Chỉ khi sử dụng lệnh 

```latex
\dbinom
```

ở **inline math** thì sẽ thấy rõ sự khác biệt kích thước. 

$\dbinom{n}{k} = \frac{n!}{k!(n-k)!}$  

---

## Đạo hàm 



. . . 

```latex
\[\frac{\mathrm d}{\mathrm d x} \left( k g(x) \right)\]
```

$$
\frac{\mathrm d}{\mathrm d x} \left( k g(x) \right)
$$
. . . 

```latex
\[\frac{\mathrm d}{\mathrm d x} \big( k g(x) \big)\]
```

$$
\frac{\mathrm d}{\mathrm d x} \big( k g(x) \big)
$$


---

## Phân số 

Để viết phân số ta sử dụng lệnh 

```latex
\frac{a}{b}
```

Ví dụ phân số ở **inline math** 

```latex
\(\frac{1}{2}\)
```

$\frac{a}{b}$

Ví dụ phân số ở **display math** 

```latex
\[\frac{1}{2}\]
```

$$
\frac{1}{2}
$$

Khai báo package: 

```latex
\usepackage{amsmath}
```

Lệnh `\tfrac` này được dùng để thu nhỏ lại phân số khi viết phân số ở **display math**

```latex
\[\tfrac{1}{2}\]
```

$$\tfrac{1}{2}$$
Lệnh `\dfrac` này được dùng để phóng to phân số khi viết phân số ở **inline mathmath**

```latex
\(\dfrac{1}{2}\)
```

$\dfrac{1}{2}$


Để viết được hỗn số ta chỉ cần viết số nguyên đó đứng trước lệnh viết phân số: 

```latex
\[5 \frac{1}{2} = \frac{11}{2}\]
```


$$
5 \frac{1}{2} = \frac{11}{2}
$$

Một cách khác để viết phân số mà người dùng thường hay thấy ở các công thức nấu ăn (? đại loại những vấn đề như thế)

```latex
\(^1/_2\)
```

$^1/_2$ 

Người dùng có thể khai báo package 

```latex
\usepackage{xfrac}
```

rồi sau đó sử dụng lệnh 

```latex
\sfrac{}{}
```

để viết lại $^1/_2$. 

```latex
\documentclass{article}
\usepackage{xfrac} 
\begin{document}
 $\sfrac{1}{2}$ 
\end{document}
```

---

##  Tổng và tích phân 

### Tổng 

Vào năm lớp 6 THCS (theo chương trình học Việt Nam ...), chúng ta đã quen thuộc với bài toán đếm tổng dãy từ 1 đến 100 huyền thoại mà ở đó nhà toán học người Đức Carl Gauss đã giải bằng một phương pháp thú vị . . . mà tổng tính được từ dãy đó là 5050

Nếu ta viết lại đáp án bài toán lại như sau

$$1+2+3+4+5+.... + 100 = 5050$$ 
thì sẽ rất dài. 

Kí hiệu tổng: 

```latex
\(\sum\)
```

$\sum$

được phát minh lần đầu bởi nhà toán học Euler vào năm 1755. 

. . . (? viết tiếp)

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/1.1.jpg" alt="1.1">
Nguồn: https://thomaskojar.wordpress.com/2021/05/13/history-of-math-symbols/
</div>

**inline math**

```latex
\(\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \sum_{n=1)^{100} \frac{1}{n^s}$ (kiểm tra lại lỗi sai)

$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}$

Hoặc có thể thêm lệnh 

```latex
\displaystyle
```
vào trước lệnh `\sum`

```latex
\(\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

**display math**

```latex
\[\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\]
```

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}
$$

Giả sử, cho $s = 2$, thay vào . . . ta được: 

$$
\zeta(2) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \frac{1}{1^2} + \frac{1}{2^2} + \frac{1}{3^2} + \dots
$$
. . . (đọc đầy đủ định lý ở đây https://pkg.yihui.org/bookdown/markdown-extensions-by-bookdown#theorems) 

Từ những kiến thức đã trình bày về cách viết kí hiệu tổng trên, ta viết gọn lại bài toán tổng ở đầu bài như  sau: 

```latex
\[\sum_{n = 1}^{100} = 5050\]
```

$$\sum_{n = 1}^{100} = 5050$$

### Tích phân 

Kí hiệu tích phân: 

```latex
\int
```

$\int$

Cách viết tương tự như viết tổng. 

**inline math** (sau thay bằng bài học mẹo tính tích phân của nhà vật lý học Richard Feynman)

```latex
\(\int_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\int_a^b f(x) \mathrm{d}x = F(b) - F(a)$

```latex
\(\displaystyle\int_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\displaystyle\int_a^b f(x) \mathrm{d}x = F(b) - F(a)$ 

**display math** 

$$
\int_a^b f(x) \mathrm{d}x = F(b) - F(a)
$$

Một cách khác để viết tích phân. (thật ra là rất quen thuộc)

Trước tiên cần khai báo package `amsmath` và để thêm tùy chọn (options) là `intlimits`:

```latex
\usepackage[intlimits]{amsmath}
```

**inline math** 

```latex
\(\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)$  

hoặc

```latex
\(\displaystyle\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\displaystyle\int\limits_a^bb f(x) \mathrm{d}x = F(b) - F(a)$

**display math** 

```latex
\[\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\]
```

$$
\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)
$$
Khai triển tích phân của một hàm số: 
. . . 

```latex
\[\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)\]
```

$$
\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)
$$

. . .

```latex
\[\int\limits_2^3 x^2 \mathrm{d}x = \left.\frac{x^3}{3}\right|^3_2 = \frac{3^3}{3} - \frac{2^3}{3} = \frac{19}{3}\]
```
$$
\int\limits_2^3 x^2 \mathrm{d}x = \left.\frac{x^3}{3}\right|^3_2 = \frac{3^3}{3} - \frac{2^3}{3} = \frac{19}{3}
$$

--- 

## Đơn vị Angstrom 

$\mathring{A}$ 

---

## Sai số 

```latex
\(a \pm b\)
```

$a \pm b$  

? . . . (dấu dưới đây là dấu gì nhỉ)

```latex
\(a \mp b\)
```

$a \mp b$

--- 

