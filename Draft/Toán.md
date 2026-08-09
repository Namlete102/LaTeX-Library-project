
\+ Tập hợp các kí hiệu có thể được nhập trực tiếp trên bàn phím 

```latex
+ - = ! / ( ) [ ] < > | ' : *
```

$+ \ - \ = \ ! \ / \ ( \ ) \ [ \ ] \ < \ > \ | \ ' \ : \ *$

---


\+ Toán tử lượng giác 

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

\+ Toán tử hàm mũ 

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

\+ Toán tử giới hạn 

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


\+ Định thức của ma trận 

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

Còn kí hiệu "sgn" phải được chứa trong lệnh `\operatorname`

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

\+ Toán tử mô-đun (thường thấy ở bài học toán đồng dư thức) 

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

\+ Viết công thức tính tổ hợp chập $k$ của của $n$ 

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

\+ Phân số 

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

Khai báo package: 

```latex
\usepackage{amsmath}
```

$$
\frac{1}{2}
$$
```latex
\[\tfrac{1}{2}\]
```

$$\tfrac{1}{2}$$
```latex
\(\dfrac{1}{2}\)
```

$\dfrac{1}{2}$


Một cách viết phân số khác 

```latex
\(^1/_2\)
```

$^1/_2$ 

---

\+  Tổng và tích phân 

Vào năm lớp 6 THCS (theo chương trình học Việt Nam ...), chúng ta đã quen thuộc với bài toán đếm tổng dãy từ 1 đến 100 huyền thoại mà ở đó nhà toán học người Đức Carl Gauss đã giải bằng một phương pháp thú vị . . . mà tổng tính được từ dãy đó là 5050

Nếu ta viết lại đáp án bài toán  

$$1+2+ .... + 100 = 5050$$ 
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

Viết gọn lại ta được: 

```latex
\(\displaystyle\sum_{n = 1}^{100} = 5050\)
```

$\displaystyle\sum_{n = 1}^{100} = 5050$

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

Kí hiệu tích phân: 

```latex
\int
```

$\int$

Cách viết tương tự như viết tổng. 

**inline math** (sau thay bằng mẹo tính tích phân của nhà vật lý học Richard Feynman)

```latex
\(\displaystyle\int_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
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

Một cách khác để viết tích phân. 

Trước tiên cần khai báo package `amsmath` và để tùy chọn (options) là `intlimits`

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

. . . 

```latex
\[\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)\]
```

$$
\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)
$$

. . .

$$
\int\limits_2^3 x^2 \mathrm{d}x = \left.\frac{x^3}{3}\right|^3_2 = \frac{3^3}{3} - \frac{2^3}{3} = \frac{19}{3}
$$
. . . 

$$
\frac{\mathrm d}{\mathrm d x} \left( k g(x) \right)
$$

$$
\frac{\mathrm d}{\mathrm d x} \big( k g(x) \big)
$$

--- 

\+ Đơn vị Angstrom 

$\mathring{A}$ 

---

\+ Sai số 

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

