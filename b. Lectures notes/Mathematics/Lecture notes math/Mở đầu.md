## Giới thiệu:

Một trong những động lực lớn nhất thúc đẩy [Donald Knuth]() khi bắt đầu phát triển hệ thống TeX ban đầu là tạo ra một công cụ cho phép xây dựng các công thức toán học một cách đơn giản, đồng thời trông chuyên nghiệp khi in ấn. Việc ông thành công có lẽ là lý do tại sao TeX (và sau này là LaTeX) trở nên phổ biến trong cộng đồng khoa học. Việc trình bày toán học là một trong những thế mạnh lớn nhất của LaTeX. Đây cũng là một chủ đề rộng lớn do sự tồn tại của rất nhiều ký hiệu toán học.[^1]

. . . . (? viết tiếp)

Đối với phép tính thông thường chẳng hạn như phép toán cộng 1+1 = 2  

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}

Phép tính 1 + 1 = 2 là một phép tính sơ khai trong lịch sử phát triển học và nghiên cứu toán học của loài người. Tuy vây, thật bất ngờ khi mãi đến thế kỉ thứ . . . các nhà toán học mới tổng quát cấu trúc đại số . . . bắt đầu từ tiên đề Peano về . . . cho đến khi hai nhà toán học Russell và Whitehead trong tác phẩm . . . xuất bản . . .ở trang . . . mới chứng minh định lý 1 + 1 = 2. 

\end{document}
```

người dùng có thể dễ dàng nhập trực tiếp toán tử (+, -), quan hệ (? dấu =, < > trong toán học được gọi thống nhất là gì nhỉ) và các số tự nhiên cơ bản (1, 2) vào trong phần soạn thảo văn LaTeX. 

(? Ảnh các nhà toán học Peano, Russell, Whitehead)

Điều này cũng tương tự, khi người dùng viết kí hiệu phần trăm 


```latex
99%  
```

các đơn vị đo lượng cơ bản như khối lượng 

```latex
70kg
```

vận tốc

```latex
5 cm/s
```

khoảng cách

```latex
10 m 
```

biến x, y, z, ..vv.., ẩn số a, b, ...vv... là các chữ cái thông thường 

```latex
y = ax + b 
```

Tập hợp các kí hiệu toán tử ... (? gồm gì nữa) có thể được gõ trực tiếp trên bàn phím, người dùng có thể xem lại bài . . . (? bài học nào trong đây) 

Tuy vậy, để người dùng có thể viết toán học ở mức độ phức tạp hơn có các [kí hiệu toán học, chữ cái Hy Lạp] . . .vv. . . thì không thể nhập được trực tiếp trên bàn phím, chẳng hạn như ví dụ sau 

```latex
Phương trình toán học từ nguyên lý bất định Heisenberg trong cơ học lượng tử . . . (? trình bày tiếp)

\Delta x \cdot \Delta p \ge \frac{\hbar}{2} 
```

So với 1 + 1 = 2, 99%, 70kg, 5 cm/s, 10 m trên, việc người dùng viết trực tiếp [toán tử]() nhân ($\cdot$), [kí hiệu Hy Lạp]() $\Delta$, [quan hệ so sánh]() $\geq$, [phân số]()  $\frac{\hbar}{2}$  từ phương trình nguyên lý bất định của Heisenberg vào soạn thảo LaTeX, khi xuất sang trang tài liệu, hệ thống sẽ lập tức báo lỗi `! Missing $ inserted`. 

(? Ảnh báo lỗi) 

Hơn nữa, phương trình đó không được căn ở một dòng riêng biệt như bài báo . . . (? bài báo nào) 

(https://ntrs.nasa.gov/citations/19840008978)

Từ hai điều cơ bản trên, người dùng có thể thấy rằng, để viết được một hay hai nhiều (hệ) phương trình toán học phức tạp (? lặp từ quá nhỉ), chúng cần được đặt vào một môi trường, lệnh riêng biệt khác, để hệ thống có thể dễ dàng phân loại, xác nhận . . . (? đúng ko nhỉ ?) phân tách việc đâu là văn bản chữ thông thường, đâu là văn bản toán học, , giúp hiển thị chính xác các kí hiệu, chữ cái toán học mà người dùng mong muốn xuất hiện trên trang tài liệu, khi xuất ra từ phần soạn thảo LaTeX.  

## inline math, display math: 

. . . (? Giới thiệu) với 1+1 = 2 ở ví dụ . . . chúng được gọi là `inline math` còn nguyên lý bất định hải sơn bắc là `displaymath`. 

LaTeX cung cấp đầy đủ hai chế độ trình bày toán học chính bao gồm
+ `inline math`(**toán học nội tuyến**): được sử dụng để viết các biểu thức, kí hiệu toán học nằm trong cùng ở đoạn văn bản.
+ `display math`(**toán học hiển thị**): được sử dụng để viết các biểu thức, kí hiệu toán học không thuộc ở đoạn văn và được trình bày trên các dòng riêng biệt. 

---

###  inline math: 

Để viết toán học ở chế độ **inline math**, người dùng cần viết chúng vào bên trong một trong ba cách sau: 

1. Một cặp dấu đô la đơn:`$...$`
2. Một cặp dấu ngoặc tròn  `\(...\)`
3. Môi trường toán học (`math`)

```latex
\begin{math} 
. . . 
\end{math}
```

Điều này có nghĩa là người dùng có thể viết phương trình toán học nổi tiếng từ định lý Pytago về mối quan hệ giữa hai cạnh góc vuông và một cạnh huyền trong một tam giác vuông ở chế độ **inline math** bằng một cặp dấu đô la đơn 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pythagoras: $x^2 + y^2 =z^2$
\end{document}
```

hoặc cũng có thể là bằng một cặp dấu ngoặc tròn

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pythagoras: \(x^2 + y^2 =z^2\)
\end{document}
```

hay cũng thể là bằng môi trường `math` 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pythagoras: 
\begin{math} 
x^2 + y^2 = z^2
\end{math}
\end{document}
```

mà kết quả cho ra được đều sẽ là giống nhau: 

Phương trình định lý Pythagoras:  $x^2 + y^2 =z^2$ 

Việc lựa chọn một trong ba cách trên để viết **inline math** tùy thuộc vào sở thích, thói quen cá nhân của người dùng.  

> [!WARNING]  
> Nếu như người dùng không viết các dấu gạch dưới `_`, dấu mũ `^` và các [kí hiệu, chữ cái toán học]() khác vào một trong ba cách viết toán học ở chế độ **inline math** trên, thì hệ thống sẽ báo lỗi `! Missing $ inserted.`

Người dùng có thể thấy ở đoạn mã dưới đây, các dấu mũ `^` của phương trình khi không được viết vào trong chế độ **inline math** ở phần soạn thảo LaTeX 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình định lý Pytago: x^2 + y^2 = z^2 
\end{document}
```

khi xuất sang trang tài liệu, lập tức hệ thống sẽ tự động báo lỗi như đã nêu ở chú ý trên. 

(? Ảnh báo lỗi đoạn mã trên)

Chú ý trên cũng được áp dụng tương tự đối với việc người dùng viết toán học ở chế độ [display math]().

<div align="center">
	<img src="LaTeX-Library-project-v1.0.0/Toán học/images math/Pythagoras.jpg" alt="Pythagoras">
</div>
<center>Triết gia và nhà toán học người Hy Lạp cổ đại xứ Samos Pythagoras</center>

---

###  display math:

Để viết toán học ở chế độ **display math**, người dùng cần viết chúng vào bên trong một trong ba cách sau:

1. Một cặp dấu đô la kép: `$$...$$`
2. Một cặp dấu ngoặc vuông: `\[...\]`
3. Môi trường `displaymath`: 

```latex
\begin{displaymath} 
. . . 
\end{displaymath}
```

Tương tự như **inline math**, tùy thuộc vào sở thích, thói quen cá nhân của người dùng để có thể chọn một trong ba cách trên để viết toán học ở chế độ **display math**, mà vẫn đảm bảo kết quả cho ra được vẫn là giống nhau. (? Quan điểm này cũng sẽ được thay đổi chút ít khi học lập trình [marco]())

Ví dụ về việc viết toán học ở chế độ `display math` với phương trình logarithm của một tích là tổng của logarit của các thừa số. Trong đó:

+ Phương trình được viết bên trong `$$...$$`

```latex
\documentclass{article}
\begin{document} % Sử dụng cặp dấu $$ để viết phương trình logarithm
$$\log_b{xy} = \log_b{x} + \log_b{y}$$
\end{document}
```

+  Phương trình được viết bên trong `\[...\]`

```latex
\documentclass{article} % Sử dụng cặp dấu \[\] để viết phương trình logarithm
\begin{document}
\[\log_b{xy} = \log_b{x} + \log_b{y}\] 
\end{document}
```

+  Phương trình được viết bên trong môi trường `displaymath`: 

```latex
\documentclass{article}
\begin{document}
\begin{displaymath} % Sử dụng môi trường displaymath để viết phương trình logarithm
\log_b{xy} = \log_b{x} + \log_b{y}\
\end{displaymath}
\end{document}
```

Kết quả cho ra được từ ba cách trên vẫn sẽ xuất hiện ở trong trang tài liệu là 

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

Để viết các phương trình có số được đánh ở bên cạnh theo thứ tự tăng dần, nhằm về sau giúp người dùng [tham chiếu chéo phương trình] , người dùng sử môi trường `equation`

```latex
\begin{equation} 
. . . 
\end{equation}
```

Để dễ hình dung môi trường `equation`, nếu như người dùng thay các cặp dấu, môi trường `displaymath` ở ví dụ . . . bằng môi trường `equation`, thì người dùng có thể thấy rằng phương trình logarithm được đặt bên trong môi trường đó sẽ được LaTeX tự động đánh thêm một số thứ tự từ (1) đến số lượng cuối cùng . . . (? số lượng cuối cùng gì) có trong phần soạn thảo và mặc định số đó được nằm ở bên phải phần toán học đó có trong trang tài liệu.  

```latex
\documentclass{article}
\begin{document}
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
\end{document}
```

Kết quả cho ra được lúc này sẽ là: 

$$
\begin{equation}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
$$

Trong một số tài liệu toán học, đôi khi người dùng cũng thế thấy rằng số thứ tự được đánh bên cạnh phần toán học đó nằm ở bên trái thay vì bên phải mặc định như ở hình dưới đây 

<div align="center"> 

<img src="LaTeX-Library-project-v1.0.0/Toán học/images math/Kakeya.jpg" alt="Kakeya">

</div>
<center>Ảnh được cắt từ trang 1 bài báo toán học <a src="https://drive.google.com/file/d/1dlpgd5Q5AAOsaCFQK5MGRisJNUPmgxFu/view?usp=sharing" target="_blank">"A STREAMLINED PROOF OF THE KAKEYA SET CONJECTURE IN \(\mathbb{R^3}\)</a> của ba nhà toán học <a src="https://math.mit.edu/~lguth/" target="_blank">Larry Guth</a>, <a src="https://sites.google.com/view/hongwang/home" target="_blank">Vương Hồng</a>, <a src="https://jzahl.github.io/" target="_blank">Joshua Zahl</a></center>

<div align="center">
	<img src="LaTeX-Library-project-v1.0.0/Toán học/images math/Guth Hong Zahl.jpg" alt="Guth Hong Zahl">
</div>
<center>Nhà toán học Lary Guth, nhà toán học Vương Hồng và nhà toán học Joshua Zahl</center>

Để chuyển số thứ tự đó nằm từ bên phải sang bên trái như hình . . . (Số hình), người dùng chỉ cần thêm `options` 

```latex
leqno
```

ở phần khai báo lớp tài liệu (`documentclass`). 

```latex
\documentclass[leqno]{article} % 
\begin{document}
\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
\end{document}
```

Kết quả cho ra được lúc này sẽ là 

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

Nếu như người dùng không muốn xuất hiện số thứ tự bên cạnh phương trình toán học khi viết chúng bằng môi trường `equation`, thì người dùng có thể quay lại ba cách đầu tiên mà người viết đã hướng dẫn ban đầu khi viết toán học ở chế độ [`display math`](), hoặc người dùng cũng có thể sử dụng một cách mới sau.  

Trước tiên người dùng nhớ cần phải khai báo package

```latex
\usepackage{amsmath}
```

ở phần . . . (? vị trí đặt lệnh `amsmath`)

Package `amsmath` còn cung cấp cho người dùng một số tùy chọn để sắp xếp và hiển thị bố cục phương trình toán học sao cho phù hợp với tài liệu người dùng, ngay cả khi các phương trình rất dài hoặc nếu người dùng phải đưa nhiều phương trình vào cùng một dòng, để tránh việc viết phương trình có thể thiếu tính linh hoạt, dẫn đến việc chồng chéo hoặc thậm chí cắt bớt một phần phương trình khi nó quá dài [?].  

. . . (*viết sau*) https://www.overleaf.com/learn/latex/Aligning_equations_with_amsmath

Tiếp đến, người dùng chỉ cần thêm dấu `*` vào bên trong dấu ngoặc nhọn `{}` của lệnh môi trường `equation` là phương trình logarithm ở ví dụ . . . sẽ không còn xuất hiện số thứ tự bên cạnh ở trong trang tài liệu nữa:  

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{equation*} % Sử dụng môi trường equation* để viết phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation*}
\end{document}
```

Kết quả lúc này ta nhận được giống với ba cách đầu tiên trên: 

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

Việc thêm dấu `*` vào trong dấu ngoặc nhọn của môi trường, cũng được áp dụng tương tự đối với các môi trường khác như môi trường `aligned` (xem ở bài học . . .), . . . (viết tiếp)  

**(?)** Điểm khác biệt của môi trường `equation*` và `displaymath` là gì ? Nên sử dụng chúng trong trường hợp nào ? (xem qua issues đây https://github.com/Namlete102/LaTeX-Library-project/issues/1) 

> [!WARNING]
> Khi người dùng viết toán học dù ở chế độ `inline math` hay `display math`, người dùng không được phép để các biểu thức,  toán tử, kí hiệu, chữ cái toán học có các khoảng trống ở mỗi dòng. Nếu không, thì hệ thống sẽ báo lỗi  `Missing $ inserted`

. . . . 

```latex
\documentclass{article}
\begin{document}
\[
\log_b{xy} 

= 
\log_b{x} + \log_b{y}
\]
\end{document}
```

Có thể thấy ở đoạn mã trên, nếu người dùng vô tình để khoảng trống giữa các dòng biểu thức $\log_b{xy}$  và $= \log_b{x} + \log_b{y}$, thì hệ thống sẽ lập tức báo lỗi `Missing $ inserted:  

. . . (? ảnh báo lỗi) 

Ta khắc phục lỗi ở đoạn mã ở ví dụ . . . (? đánh số ví dụ) bằng cách xóa đi khoảng trắng giữa hai biểu thức đó

```latex
\documentclass{article}
\begin{document}
\[
\log_b{xy} 
= 
\log_b{x} + \log_b{y}
\]
\end{document}
```

hoặc thêm [chú thích]() vào khoảng trống giữa hai biểu thức đó

```latex
\documentclass{article}
\begin{document}
\[
\log_b{xy} 
% Chú thích này sẽ lấp lại dòng trống
= \log_b{x} + \log_b{y}
\]
\end{document}
```

mà kết quả cho ra được đều sẽ là như sau:

$$
\log_b{xy} 
% Chú thích này sẽ lấp lại dòng trống
= \log_b{x} + \log_b{y}
$$

<div align="center"> 
	<img src="LaTeX-Library-project-v1.0.0/Toán học/images math/John Napier.jpg" alt="John Napier">
</div>
<center>Nhà toán học người Scotland John Napier</center> 

---
## Tài liệu tham khảo: 

\[1]: Nguồn tham khảo viết toán học ở Overleaf: https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Adding_math_to_LaTeX.   

\[2]:  Nguồn tham khảo lời viết này sử dụng ở Wikibook: https://en.wikibooks.org/wiki/LaTeX/Mathematics 

---
## Footnote

[^1]: [https://en.wikibooks.org/wiki/LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
