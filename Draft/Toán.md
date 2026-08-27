
## Gói `mathtools` 


---

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

. . .  (? đang viết dang dở ở phần lecture notes)

Khi viết tập hợp các số hữu tỉ $\mathbb{Q}$ được biểu diễn bằng cách chỉ rõ tính chất đặc trưng của mỗi phần tử:  

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}$$

Người dùng có thể thấy rằng, tuy hai bên dấu ngoặc nhọn đã được . . . (? điều gì tự động căn chỉnh) tự động căn chỉnh bởi hai lệnh lần lượt là `\left` và `\right`, nhưng [kí hiệu]() `|` không được tự động co giãn sao cho phù hợp với kích thước chiều cao của phân số $\dfrac{a}{b}$.  

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

Lệnh `\middle` này chỉ được sử dụng trong việc giúp các kí hiệu nhằm mục đích phân cách . . . (?) có thể được tự động co giãn chiêu cao sao cho phù hợp, vừa vặn kích thước với cặp dấu ngoặc bao quanh các phân số (như ở ví dụ trên), tích phân, tổng chuỗi, ma trận, căn thức, ..vv.. 

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

Việc người viết thay kí hiệu `|` bằng $\rightarrow$ ở ví dụ này không thật sự có ý nghĩa về mặt toán học, tuy vậy điều người viết muốn trình bày là ở chú ý . . . (? viết như c), người dùng có thể thấy các kí hiệu nằm ngang như $\rightarrow$ sẽ bị hệ thống lỗi. (? trình bày lại) 

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

. . . (định nghĩa hàm số mũ) 
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

## Giới hạn 

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

Khi viết các phần tử bên trong ma trận là các số hữu tỉ, chẳng hạn như ở ví dụ sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\
       \frac{5}{6} & 0           & \frac{1}{6} \\
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```

$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\
       \frac{5}{6} & 0           & \frac{1}{6} \\
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$
Người dùng có thể thấy, tử số của phân số phần tử $a_{21} = \dfrac{5}{6}$ là 5, bị dính với mẫu số của phân số phần tử $a_{12} = \dfrac{5}{6}$. Và điều này cũng xảy ra tương tự ở phần tử $a_{33} = \dfrac{2}{3}$ với phần tử $a_{23} = \dfrac{2}{3}$. 

Để khắc phục được điều trên, người dùng chỉ cần viết dính liền, ngay sau dấu ngăn cách các hàng trong ma trận `\\` với dấu ngoặc vuông `[]`. 

Và bên trong dấu ngoặc vuông đó chứa thông số . . . .(? thông số gì) để co giãn hai phân tử cùng cột mà khác hàng . . .(? viết lại)

Chẳng hạn, người viết muốn . . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\[0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```


$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\[0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$

Nếu như người dùng viết cách dấu `\\` và `[]`: (? viết chưa rõ ý)

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\ [0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```

thì hệ thống sẽ hiểu `[]` . . . (? hiểu gì)

$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\ [0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$

. . . .

Đối với gói `amsmath` để viết ma trận ở **inline math** ta sẽ sử dụng môi trường `smallmatrix`

```latex
\begin{smallmatrix}
. . . 
\end{smallmatrix}
```

Ta cần phải thêm . . . 

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\left(\begin{smallmatrix}1 & 2 \\ 3 & 4\end{smallmatrix}\right)\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\left(\begin{smallmatrix}1 & 2 \\ 3 & 4\end{smallmatrix}\right)$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 

Cách này chỉ phù hợp với việc người dùng viết ma trận được bao quanh bởi dấu ngoặc tròn cơ bản. Trong trường hợp ma trận đó được kí hiệu là định thức, ma trận chuẩn thì . . . (? thì sao em nhỉ)

Để làm được điều này, trước tiên người dùng cần phải sử dụng gói `mathtools`.

Môi trường `bsmailmatrix`

```latex
\begin{bsmailmatrix}
. . . 
\begin{bsmailmatrix}
```

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{bsmallmatrix}1 & 2 \\ 3 & 4\end{bsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{bsmallmatrix}1 & 2 \\ 3 & 4\end{bsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `Bsmailmatrix`

```latex
\begin{Bsmailmatrix}
. . . 
\begin{Bsmailmatrix}
```

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{Bsmallmatrix}1 & 2 \\ 3 & 4\end{Bsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Bsmallmatrix}1 & 2 \\ 3 & 4\end{Bsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `vsmailmatrix` . . . 

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{vsmallmatrix}1 & 2 \\ 3 & 4\end{vsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{vsmallmatrix}1 & 2 \\ 3 & 4\end{vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `Vsmallmatrix` . . . 

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Vsmallmatrix}1 & 2 \\ 3 & 4\end{Vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Vsmallmatrix}1 & 2 \\ 3 & 4\end{Vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Ta còn có thể thay cách thủ công . . . (? ở phần giới thiệu gói `amsmath`) . . . bằng môi trường `psmailmatrix` . . .

Ví dụ: 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{psmallmatrix}1 & 2 \\ 3 & 4\end{psmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{psmallmatrix}1 & 2 \\ 3 & 4\end{psmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 

### Ma trận bổ sung 

Cho một hệ phương trình tuyến tính tổng quát . . . 

. . . (ma trận hệ số (coefficient matrix), ma trận cột ẩn số, ma trận cột hệ số tự do)

. . . (ma trận bổ sung (augmented matrix)) 

Để viết ma trận bổ sung, người dùng sẽ sử dụng gián tiếp thông qua môi trường `array`. 

Ví dụ . . . : Cho một hệ phương trình tuyến tính sau 

```latex
\begin{cases}
	x_1 + 2x_2 + 3x_3 = 4 \\[0.5em] 
	2x_1 + 3x_2 + 4x_3 = 5 \\[0.5em]
	3x_1 + 4x_2 + 5x_3 = 6
\end{cases}
```

$$
\begin{cases}
	x_1 + 2x_2 + 3x_3 = 4 \\[0.5em] 
	2x_1 + 3x_2 + 4x_3 = 5 \\[0.5em]
	3x_1 + 4x_2 + 5x_3 = 6
\end{cases}
$$

Ta viết gọn lại bằng ma trận bổ sung như sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\left[
\begin{array}{@{}ccc|c@{}}
2 & 3 & 4 & 5 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right]
\]
\end{document}
```

$$
\left[
\begin{array}{@{}ccc|c@{}}
1 & 2 & 3 & 4 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right] 
$$

Lệnh `@{}` được đặt hai bên . . . (? gì đó) trong dấu ngoặc nhọn, dùng để căn chỉnh hai dấu ngoặc vuông của ma trận bổ sung khi viết ở phần thảo LaTeX sao cho  .  .  . (? giúp chúng như thế nào)  

Nếu như người dùng không lệnh `@{}` này vào, thì lúc này ở trong trang tài liệu sẽ hiện thị một kết quả khác: 

$$
\left[
\begin{array}{ccc|c}
1 & 2 & 3 & 4 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right] 
$$

### Pp khử Gauss - Jordan 

(? . . . . Giới thiệu phương pháp khử Gauss - Jordan) 

Ví dụ . . . : Cho một hệ ba phương trình ba ẩn sau: 

```latex
\[
\begin{cases}
    x + 2y -z = 3 \\[0.5em]
    2x + 5y + z = 10 \\[0.5em] 
    3x + 6y + 2z = 15 
\end{cases}
\]
```

$$
\begin{cases}
    x + 2y -z = 3 \\[0.5em]
    2x + 5y + z = 10 \\[0.5em] 
    3x + 6y + 2z = 15 
\end{cases}
$$

Viết lại dưới dạng ma trận bổ sung ta được: 

```latex
\[
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right]
\]
```

$$
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right]
$$

Sử dụng phương pháp khử Gauss - Jordan để tìm nghiệm hệ trên: 

```latex
\[
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right] 
\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.3em] R_3 \to R_3 - 3R_1}}
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 5 & 6 
\end{array}
\right] 
\xrightarrow{R_3 \to \dfrac{1}{5}R_3} 
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\]

\[
\xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \dfrac{21}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \dfrac{17}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\]
```

$$
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right] 
\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.3em] R_3 \to R_3 - 3R_1}}
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 5 & 6 
\end{array}
\right] 
\xrightarrow{R_3 \to \dfrac{1}{5}R_3} 
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
$$

$$
\xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \dfrac{21}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \dfrac{17}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
$$
Cách viết thứ hai . . . bằng cách sử dụng môi trường `align`

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{align*}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
2 & 5 & 1 & 10 \\
3 & 6 & 2 & 15 
\end{array}\right]
&\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.2em] R_3 \to R_3 - 3R_1}}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 5 & 6 
\end{array}\right] \\[1em] % xuống hàng mới 
& \xrightarrow{R_3 \to \dfrac{1}{5}R_3} % Vô hàng
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 1 & \frac{6}{5} 
\end{array}\right] \\[1em]
& \xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \frac{21}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] \\[1em]
& \xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \frac{17}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] 
\end{align*}
\end{document}
```

$$
\begin{align*}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
2 & 5 & 1 & 10 \\
3 & 6 & 2 & 15 
\end{array}\right]
&\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.2em] R_3 \to R_3 - 3R_1}}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 5 & 6 
\end{array}\right] \\[1em] % xuống hàng mới 
& \xrightarrow{R_3 \to \dfrac{1}{5}R_3} % Vô hàng
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 1 & \frac{6}{5} 
\end{array}\right] \\[1em]
& \xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \frac{21}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] \\[1em]
& \xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \frac{17}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] 
\end{align*}
$$

Vậy 

$$
(x, y, z) = \left(\frac{17}{5}, \frac{2}{5}, \frac{6}{5}\right)
$$


<div align="center">
	
<img src="./draft img/Gauss-Jordan.jpg" alt="Gauss-Jordan">

Hai nhà toán học người Đức là Carl Gauss (trái) và Wilhelm Jordan (phải) (không nền nhầm lẫn với hai nhà toán học cùng tên khác là Camille Jordan và Pascual Jordan) 

</div>


---

## Định thức của ma trận 

### Công thức LeibnizLeibniz

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

Ngoài ra, định thức của một ma trận vuông $A$ cấp $n$ còn được kí hiệu là $\det(A)$. 

Ví dụ . . .  về công thức tính định thức tổng quát của một ma trân vuông $A$ cấp $n$ được chứng minh bởi nhà toán học Leibniz  

```latex
\documentclass{article}
\begin{document}
\[det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )\]
\end{document}
```

. . . 

$$det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )$$

Ta thấy hai kí hiệu từ công thức trên là "det" và "sgn" bị nghiêng. LaTeX đã định nghĩa lệnh

```latex
\det
```

dùng để viết kí hiệu định thức. 

Còn kí hiệu "sgn", người dùng cần phải viết chúng vào trong dấu ngoặc nhọn của lệnh `\operatorname`

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

### Công thức khai triển Laplace 

Một cách khác để tính định thức đó là khai triển Laplace . . . (? không cần nói quá rõ chi tiết lý thuyết, những vẫn cần giới thiệu sơ qua)

. . . (? công thức khai triển Laplace tổng quát theo hàng)

```latex
\[
\det(A) = \sum_{1 \leq i_1 < \dots < i_k \leq k} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
\]
```

$$
\det(A) = \sum_{1 \leq i_1 < \dots < i_k \leq k} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
$$
Người dùng có thể thấy, có một khoảng trống giữa lệnh `\sum` hai bên. Vì điều kiện của phương trình quá lớn dẫn đến việc hệ thống tự động co giãn các biểu thức hai bên đầu điều kiện. (? . . . kiểm tra lại phần mô tả này)

Để khắc phục được vấn đề này, trước tiên người dùng cần phải khai báo package `mathtools`. Sau đó, người dùng chỉ cần nhóm điều kiện ở chỉ số dưới lệnh `\sum` này lại vào trong dấu ngoặc nhọn của lệnh `\mathclap`. Cụ thể: 

```latex
\mathclap{1 \leq i_1 < \dots < i_k \leq k}
```

Từ đây, ta viết lại công thức khai triển Laplace tổng quát theo theo hàng như sau: 

```latex
\[
\det(A) = \sum_{\mathclap{1 \leq i_1 < \dots < i_k \leq k}} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
\]
```

Kết quả hiện thị lúc này,  . . . (? lúc này sẽ ra làm sao)

$$
    \det(A) = \sum_{\mathclap{1 \leq i_1 < \dots < i_k \leq k}} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
$$


---

##  Vết của ma trận  

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

Lệnh `\dfrac` này được dùng để phóng to phân số khi viết phân số ở **inline math**

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

```latex
\(\mathring{A}\)
```

$\mathring{A}$ 

---

## Sai số (cũng ko hẳn)

```latex
\(a \pm b\)
```

$a \pm b$  

Hai nghiệm phân biệt của một phương trình bậc hai một ẩn, với $\Delta > 0$ 

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

? . . . (dấu dưới đây là dấu gì nhỉ)

```latex
\(a \mp b\)
```

$a \mp b$

--- 

## Các dấu chấm dài trong LaTex

Các dấu chấm này được sử dụng cả trong văn bản thông thường, lẫn trong văn bản toán học. 

| . . .            | Lệnh           |
| :--------------- | -------------- |
| a $\dots$ b      | `\dots`        |
| a $\cdots$ b     | `\cdots`       |
| a $\vdots$ b     | `\vdots`       |
| a $\ddots$ b     | `\ddots`       |

Ở bảng . . . (số bảng ...) trên, chỉ riêng dấu ba chấm "$\dots$" là không cần nhất thiết được đặt vào các lệnh và môi trường viết chế độ toán học. Còn lại là bắt buộc phải đặt chúng vào trong các lệnh, môi trường viết toán học, nếu không thì hệ thống sẽ báo lỗi **Missing $ inserted.** 

Ví dụ: 

. . . (ví dụ với hai dấu ba chấm đầu tiên) 

. . . (giới thiệu dấu $\vdots$) 

Ví dụ: Dấu $\vdots$ thường được thấy nhiều ở việc người dùng sử dụng chúng để viết một ma trận tổng quát có kích thước $m \times n$. 

. . . (ma trận tổng quát)

Ngoài ra dấu $\vdots$ còn được sử dụng để làm quan hệ chia hết giữa hai số. 

Ví dụ: Với bổ đề Euclid trong lý thuyết số  

Bổ đề Euclid: Cho  $a, b \in \mathbb{N}$ và $p \in \mathbb{P}$: 

Nếu $p \ \vdots \ (a \cdot b)$, thì $p \ \vdots \ a$ hoặc $p \ \vdots \ b$. 

Tuy vậy, đôi khi . . . thường sử dụng dấu $|$ để biểu diễn quan hệ chia hết giữa hai số. 

Đọc thêm ở . . . (? phần viết lý thuyết số cơ bản trên) 

. . . (giới thiệu dấu `\hdotsfor{n}`) 

Dấu này được sử dụng chính chỉ trong việc viết . . . (? dùng cho điều gì cơ)

. . . . (? giải thích lệnh này) 

---

## Viết văn bản trong chế độ toán học 

Đã viết một phần bên [[Lecture notes]].  

Khi người dùng viết lệnh `\text` ở sau một số hay một từ nào đó như ở ví dụ sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{vietnam}
\begin{document}
\[500 \text{quả táo} \times 100 \text{quả cam} = \text{Siuuu}^2\]
\end{document}
```

$$
500 \text{quả táo} \times 100 \text{quả cam} = \text{Siuuu}^2
$$

Người dùng có thể thấy từ quả táo sẽ bị dính liền với số 500, còn từ quả cam cũng sẽ bị dính liền với số 100. Dù người dùng đã phím cách tạo khoảng trống giữa các số với lệnh `\text` tương ứng.  

Để khắc phục được điều này, người dùng chỉ cần nhấn phím cách văn bản trong lệnh `\text` so với dấu `{`  

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{vietnam}
\begin{document}
\[500 \text{ quả táo} \times 100 \text{ quả cam} = \text{Siuuu}^2\]
\end{document}
```

$$
500 \text{ quả táo} \times 100 \text{ quả cam} = \text{Siuuu}^2
$$

Chỉnh sửa lại ở phần [[Lecture notes]] phần ví dụ mở đầu. [^1]

```latex
\documentclass{letter}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm} 
\theoremstyle{definition}
\newtheorem*{definition}{Định nghĩa}
\begin{document}
\begin{definition}
    Cho \(c, d \in \mathbb{R}, c \neq d\) (thường lấy \(c=1 \ \text{và} \ d = 0\)). Hàm Dirichlet được định nghĩa bởi: 
    \[
    D(x) = 
        \begin{cases}
        c \quad nếu \ x \in \mathbb{Q}\\ 
        d \quad nếu \ x \notin \mathbb{Q} 
        \end{cases}
    \]
    và không liên tục ở mọi nơi. Hàm Dirichlet có thể được viết dưới dạng giải tích như sau:
    \[
    D(x) = \lim\limits_{m \to \infty} \lim\limits_{n \to \infty} \cos^{2n}(m! \pi x)
    \]
\end{definition}
\end{document}
```

Người dùng có thể thấy, từ "nếu" được viết vào bên trong môi trường toán học sẽ bị in nghiêng. 

. . . (Hướng dẫn sử dụng lệnh `\text`) 

```latex
\documentclass{letter}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm} 
\theoremstyle{definition}
\newtheorem*{definition}{Định nghĩa}
\begin{document}
\begin{definition}
    Cho \(c, d \in \mathbb{R}, c \neq d\) (thường lấy \(c=1 \ \text{và} \ d = 0\)). Hàm Dirichlet được định nghĩa bởi: 
    \[
    D(x) = 
        \begin{cases}
        c \quad \text{nếu} \ x \in \mathbb{Q}\\ 
        d \quad \text{nếu} \ x \notin \mathbb{Q} 
        \end{cases}
    \]
    và không liên tục ở mọi nơi. Hàm Dirichlet có thể được viết dưới dạng giải tích như sau:
    \[
    D(x) = \lim\limits_{m \to \infty} \lim\limits_{n \to \infty} \cos^{2n}(m! \pi x)
    \]
\end{definition}
\end{document}
```

<div align="center">
	
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/Dirichlet.jpg">

Nhà toán học người Đức Johann Peter Gustav Lejeune Dirichlet

</div>



--- 

## In đậm chữ cái Hy Lạp

Để in đậm chữ cái Hy Lạp, trước tiên người dùng cần phải khai báo gói `bm`

```latex
\usepackage{bm}
```

Sau đó, người dùng chỉ cần viết các chữ cái Hy Lạp vào trong dấu ngoặc nhọn của lệnh `\bm`. 

```latex
\bm
```

Lệnh này chỉ được sử dụng bên trong lệnh, môi trường viết toán học. 

Ví dụ: . . . 

```latex
\(\bm{\alpha}\)
```

Nếu như người dùng không thích khai báo package, mà muốn sử dụng một lệnh duy nhất để in đậm các chữ cái Hy Lạp, thì sử dụng qua lệnh: 

```latex
\boldsymbol{}
```

Ví dụ: . . . 

```latex
\(\boldsymbol{\alpha}\)
```

---

## Một số phông chữ trong toán học 

Phông chữ toán học thông thường: 

```latex
\[ABC \ abc \ 123\]
```

$$ABC \ abc \ 123$$

Để các chữ cái toán học không bị in nghiêng như trên sử dụng lệnh `\mathrm`: 

```latex
\[\mathrm{ABC} \ \mathrm{abc} \ 123\]
```

$$\mathrm{ABC} \ \mathrm{abc} \ 123$$

Để các số được in nghiêng ta sử dụng lệnh `\mathit`: 

```latex
\[\mathit{ABC} \ \mathit{abc} \ \mathit{123}\]
```

$$\mathit{ABC} \ \mathit{abc} \ \mathit{123}$$

Để in đậm các cái toán học ta sử dụng lệnh `\mathbf`: 

```latex
\[\mathbf{ABC} \ \mathbf{abc} \ \mathbf{123}\]
```

$$\mathbf{ABC} \ \mathbf{abc} \ \mathbf{123}$$

Để . . . 

```latex
\[\mathsf{ABC} \ \mathsf{abc} \ \mathsf{123}\]
```

$$\mathsf{ABC} \ \mathsf{abc} \ \mathsf{123}$$

Để . . 

```latex
\[\mathtt{ABC} \ \mathtt{abc} \ \mathtt{123}\]
```

$$\mathtt{ABC} \ \mathtt{abc} \ \mathtt{123}$$

Để . . .

```latex
\[\mathcal{ABCDEF}\]
```

$$
\mathcal{ABCDEF}
$$
Để viết các tập số như tập tự nhiên $\mathbb{N}$, ..vv.. rước tiên ta cần phải khai báo package là `amssymb` hoặc `amsfonts`. Sau đó sử dụng lệnh `\mathbb`:  

```latex
\[\mathbb{NPZQRC}\]
```

$$
\mathbb{NPZQRC}
$$

Để viết các tập số như tập tự nhiên $\mathbb{N}$, ..vv.. rước tiên ta cần phải khai báo package là `amssymb` hoặc `amsfonts`. Sau đó sử dụng lệnh `\mathfrak`: 

```latex
\[\mathfrak{ABC} \ \mathfrak{abc} \ \mathfrak{123}\]
```

$$\mathfrak{ABC} \ \mathfrak{abc} \ \mathfrak{123}$$

Để . . ., trước tiên ta cần phải khai báo package là `mathrsfs`. Sau đó sử dụng lệnh `\mathscr`: 

```latex
\[\mathscr{ABCDEF}\] 
```

$$
\mathscr{ABCDEF} 
$$
--- 

## Viết phương trình theo mục lục (đặt tiêu đề lại)

Câu hỏi 1: Đối với chỉ riêng **section**. 

Trước tiên, người dùng cần phải khai báo package `amsmath`, sau đó chỉ cần chèn lệnh

```latex
\numberwithin{}{}
```

ở trước môi trường `equation`, . . . (? còn môi trường nào nữa ko)

```latex

```

Câu hỏi 2: Đối với việc có cả subsection bên trong cả section.  



--- 

## Chưa phân loại (tổng hợp đại trước)

Nơi đây chứa tạp nhám các loại toán học, sau đó mới phân loại sau. 

Tổng hợp tại đây: https://www.overleaf.com/read/cvrzxtfnpxvk#5bc02f 

---

[^1]: Tài liệu tham khảo hàm Dirichlet: https://mathworld.wolfram.com/DirichletFunction.html
