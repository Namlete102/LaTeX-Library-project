# a. Giới thiệu 

Có viết ở phần [[About]]

---
# b. Các bài học 

## Bố cục các tệp trong dự án LaTeX: 

. . . 

---

## Cấu trúc soạn thảo của LaTeX:

. . . 

```latex
\documentclass{article}
\begin{document}
Hello \LaTeX{} !
\end{document}
```

(? Ảnh meme nào đó thú vị về  Hello LaTeX)

---

## Viết từ "TeX" và "LaTeX" trong LaTeX:

Ở ví dụ . . . của bài học . . .  người dùng có thể thấy rằng từ "LaTeX"  

Hơn nữa, trong một số tài liệu giới thiệu về LaTeX, người dùng cũng có thể thấy rằng các tác giả viết từ "TeX" và "LaTeX" rất khác so với các từ khác như trong hình ảnh minh họa (? lấy hình từ cuốn sách hay tài liệu nào đó để làm minh họa nhé) sau đây. 

. . . (hình minh họa)

Để làm được điều này, người dùng chỉ cần thêm kí tự `\` (kí tự này rất quan trọng về các bài học như [kí tự đặc biệt]()) vào trước từ TeX và cũng như là LaTeX. Cụ thể ta có lệnh đầy đủ sau đây 

```latex
\TeX{} 
\LaTeX{}
```

hoặc cũng có thể là 

```latex
\TeX\ 
\LaTeX\
```

Điểm khác biệt ở hai câu lệnh trên tuy là ở sau từ TeX và LaTeX có thêm dấu ngoặc ngọn `{}` hoặc dấu `\`, nhưng kết quả cho ra được vẫn sẽ là giống nhau. 

$$\LaTeX{}, \ \TeX{}$$

Mục đích của dấu `{}` hoặc kí tự `\` cần được thêm vào sau lệnh `\TeX`, `\LaTeX` là nhằm để hệ thống sẽ không tự động lấy mất khoảng trắng (dấu cách) khi người dùng viết tiếp câu văn ngay sau từ LaTeX đó.

Để dễ hình dung, người dùng xem qua ví dụ đoạn mã sau đây về việc nếu như người dùng không thêm dấu ngoặc hay dấu `\` vào sau  lệnh \LaTeX`

```latex
\documentclass{article} 
\usepackage[utf8]{vietnam}
\begin{document} 
\LaTeX là một trình soạn thảo văn bản tuyệt vời ! 
\end{document}
```

Người dùng có thể thấy dù người dùng có nhấn dấu cách (space) trên bàn phím bao nhiêu lần, thì từ "là" vẫn sẽ bị dính liền với từ trước của nó là từ "LaTeX" . 
 
---

## Căn lề trang tài liệu:

Chúng ta có thể thay đổi khoảng cách căn lề (margin size) bằng cách sử dụng package `geometry` hỗ trợ. Package này sẽ tự làm mọi thứ bằng lệnh:

```latex
\usepackage[option]{geometry} 
```

trong đó:

- option: là các tham số được truyền vào để thiết lập kích thước trang giấy tài liệu mà người dùng mong muốn. 

Các option phổ biến thường thấy bao gồm:

- Chọn kích thước trang giấy (page size): a4papper, a5paper, letterpaper, ..vv..
- Định lề trang (margins): margin =... (đặt tất cả các lề), top = . . . (lề trên), left = . . .(lề trái), right = . . .(lề phải), bottom = . . . (lề dưới).
- Hướng giấy (Orientation): portrait (khổ dọc), landscape (khổ ngang).

Ví dụ: Đặt tất cả các lề của trang đều bằng 1in

```latex
\usepackage[margin=1in]{geometry}
```

---
## Chú thích trong LaTeX:

Để chú thích trong LaTeX ta sử dụng kí hiệu `%`:

```latex
% chú thích 
```



--- 
## Kí tự thông thường: 

Các kí tự thông thường là các kí tự mà người dùng có thể nhập trực tiếp từ bàn phím có thể xuất sang trang tài liệu mà không cần sử dụng thêm câu lệnh gì. 

Các kí tự thông thường trong LaTeX bao gồm:
- In hoa A - Z
- In thường a - z
- Số 0 - 9
- Các kí tự ngắt nghỉ câu (?)
--- 
## Kí tự đặc biệt:

Thuật ngữ "kí tự đặc biệt" dùng để chỉ tất cả các kí hiệu ngoại trừ các chữ cái viết thường, in hoa, các chữ số và các kí tự ngắt nghỉ câu mà ta đã nhắc ở [kí tự thông thường](). 

Hơn nữa, các kí tự đặc biệt cũng là các kí tự mà người dùng đôi khi không thể nhập trực tiếp được từ bàn phím vào phần soạn thảo LaTeX. Vì một số kí hiệu đó đã được dành riêng để có chức năng phục vụ cho mục đích nào đó của LaTeX. 

Ví dụ như kí tự $\text{\%}$ dùng để [chú thích trong LaTeX](). Nếu như người dùng gõ trực tiếp dấu chú thích đó vào phần soạn thảo LaTeX, thì khi xuất ra trang tài liệu, chúng sẽ không được hiện hữu trong trang tài liệu, mà thay vào đó hệ thống chỉ hiểu kí tự $\text{\%}$ đó đang được dùng để chú thích trong phần soạn thảo.  

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}

% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}

% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle

% Nếu viết trực tiếp kí tự % , LaTeX sẽ hiểu đó là chú thích mà không xuất hiện ở trong trang tài liệu 

\end{document}
```

Điều này cũng tương tự đối với các kí tự sau $\textbackslash$, ...vv...

Hoặc đôi khi người dùng sẽ thấy nó còn báo lỗi nếu như người dùng gõ các kí tự đặc biệt đó một cách trực tiếp trong phần biên soạn như ví dụ về kí tự viết [toán học nội tuyến]() sau. 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tài liệu ---
\usepackage[english]{babel}

\begin{document}
% --- Khai báo thông tin bài viết ---
\title{Your Paper}
\author{You}
\date{\today}
% --- Hiển thị tiêu đề, tác giả, ngày tháng ---
\maketitle
% Nếu viết hai lần kí tự $ $, LaTeX sẽ hiểu là người dùng đang viết toán học nội tuyến (inline math)
$ $
% Nếu viết đơn lẻ kí tự &, LaTeX sẽ báo lỗi "Misplaced alignment tab character &".
& 
\end{document}
```

Nếu người dùng chạy đoạn mã trên trực tiếp trên Texlive.net hoặc Overleaf, chúng đều báo cùng một lỗi là "Misplaced alignment tab character &". 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.1.jpg"
         alt="Báo lỗi ở Texlive.net">
	<figcaption>Báo lỗi kí tự '&' ở Texlive.net</figcaption>
</figure>

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img5.2.jpg"
         alt="Báo lỗi ở Overleaf">
	<figcaption>Báo lỗi kí tự '&' ở Overleaf</figcaption>
</figure>

Tùy thuộc vào kí tự đặc biệt người dùng sử dụng đó mà hệ thống sẽ báo lỗi để người dùng biết nhằm khắc phục lỗi của kí tự đó. 

Để viết các kí tự đặc biệt đó xuất hiện ở trang tài liệu, người dùng cần phải thêm trước kí tự đặc biệt đó với kí tự `\`. 

Ví dụ:

```latex
\documentclass{article}
\begin{document}
% Viết kí tự đặc biệt nhờ vào dấu '\' 
\% 
\_ 
\& 
\{ 
\} 
\end{document}
```

Đối với kí tự $\textasciicircum{}$, người dùng cần phải sử dụng lệnh sau

```latex
\textasciicircum 
```

Đối với kí tự $\textbackslash$,  người dùng cần phải sử dụng lệnh sau 

```latex 
\textbackslash
```

Một số kí tự đặc biệt mà người viết khuyên người dùng có thể chỉ cần gõ một cách trực tiếp các kí tự đó thì nó vẫn sẽ xuất hiện ở trang tài liệu mà không cần phải nhớ lệnh của chúng. 

Ví dụ: 

```latex

```

Các kí tự đặc biệt ở trên được tổng hợp đầy đủ ở bảng dưới đây mà người dùng có thể tham khảo:  

(xem ở đây https://en.wikibooks.org/wiki/LaTeX/Special_Characters#Other_symbols) 

---
## Các chữ cái đặc biệt: 

Các chữ cái đặc biệt là gì ? (tìm hiểu đôi chút về lịch sử các nước sử dụng nó cũng vui hihi)

Xem tại đây: https://en.wikibooks.org/wiki/LaTeX/Special_Characters 

--- 
## Định dạng thông tin cơ bản: 

Một số thông tin cơ bản mà người dùng cần thêm vào tài liệu khi viết bài báo, ...vv..  bao gồm:
- Tiêu đề tài liệu/bài viết
- Tác giả
- Ngày/tháng/năm (hoặc cũng có thể chỉ cần tháng/năm) xuất bản 

```latex
\title{Your title}
\author{You}
\date{Day/Mouth/Year}
```

Bên trong lệnh `\date{}`, người dùng có thể điền ngày/tháng/năm ở bất kì mốc thời gian cố định nào tùy ý. 

Các thông tin khai báo cơ bản ở trên gồm tiêu đề, tác giả, ngày/tháng/năm sẽ không được xuất hiện trong trang tài liệu cho tới khi người dùng sử dụng lệnh 

```latex
\maketitle
```

được đặt ở bên trong môi trường `documents`. 

Nếu như người dùng không sử dụng lệnh `\date` hoặc 

```latex
\date{\today}
```

thì ngày/tháng/năm sẽ được LaTeX tự động cập nhật theo thời gian thực mỗi khi người biên dịch (compile) tài liệu. 

Nếu như người dùng không muốn hiển thị thông tin ngày/tháng/năm ở trong tài liệu của mình, người dùng chỉ cần bỏ trống phần thông tin bên trong lệnh `\date`. 

```latex
\date{}
```

Để hiện thị thêm thông tin (như email, nơi công tác) của tác giả, người dùng chỉ cần thêm lệnh `\thanks{}` vào ngay bên trong lệnh `\author{}`. 

```latex
\author{You\thanks{Your information}}
```

Bên trong dấu ngoặc của lệnh `\thanks` là nơi người dùng cần thêm thông tin của tác giả đó. Lúc này, tên tác giả sẽ xuất hiện dưới dạng một dấu sao nằm ở trên đầu góc trái của tên tác giả đó và nội dung thông tin được cung cấp thêm cho tác giả sẽ được hiển thị ở chân trang tài liệu đó. 

Dưới đây là ví dụ hoàn chỉnh kết hợp các yếu tố trên. 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % latex Khai báo tài liệu viết Tiếng Việt

% Khai báo thông tin tài liệu
\title{An Example of LaTeX Document} 
\author{Namlete\thanks{nguyenlenam15082007@gmail.com}} 
\date{May 30, 2026} 

\begin{document}

% Lệnh bắt buộc để hiển thị tiêu đề, tác giả, ngày tháng ra màn hình
\maketitle

Hello LaTeX! Đây là nội dung bài viết của bạn.

\end{document}
```

Nếu như người dùng muốn thông tin tác giả được hiện thị ở ngay sau phần tên tác giả, đầu tiên người dùng cần khai báo package sau

```latex
\usepackage{authblk}
```

Sau đó, người dùng sử dụng hai lệnh sau: 

```latex
\author[]{}
\affil[]{}
```

trong đó: 
+ Lệnh `\author[]{}` là nơi người dùng cần điền tên tác giả
+ Lệnh `\affil[]{}` là nơi người dùng cần điền thông tin của tác giả đó. 

Dấu ngoặc vuông `[]` là nơi người dùng điền `option` là số thứ tự như $1, 2, 3, \dots$  hoặc các kí hiệu toán học, chữ cái Hy Lạp khác như $\dagger, \beta , \dots$ , để liên kết tác giả với thông tin của tác giả tương ứng, 

Ta có ví dụ về điều này như sau: 

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
\usepackage{authblk}

\title{Your Paper}
\author[1]{You}
\affil[1]{Your information}
\date{}

\begin{document}
\maketitle
\end{document}
```
![](2026/IT-project/LaTeX-Library-project/1.0.0/Images/img3.1.jpg)

Người dùng cũng có thể sử dụng điều này để trình bày nhiều hơn một tác giả cộng tác tài liệu qua ví dụ sau:

```latex
\author[1]{author 1}
\author[2]{author 2}
\affil[1]{Author information 1}
\affil[2]{Author information 1}
```

![](LaTeX-Library-project-v1.0.0/images/img3.2.jpg)

--- 
## Đơn vị độ dài trong LaTeX:



---

## Lorem ipsum:

**Lorem ipsum** là một [đoạn văn bản giả hoặc văn bản giữ chỗ](https://en.wikipedia.org/wiki/Placeholder_text "Văn bản giữ chỗ")  thường được sử dụng trong thiết kế đồ họa, xuất bản và phát triển web. 

Nó thường là một phiên bản bị thay đổi của _[De finibus bonorum et malorum](https://en.wikipedia.org/wiki/De_finibus_bonorum_et_malorum "De finibus bonorum et malorum")_, một văn bản thế kỷ thứ nhất Trước Công nguyên của chính khách và triết gia La Mã [Cicero](https://en.wikipedia.org/wiki/Cicero "Cicero") , với các từ bị thay đổi, thêm vào và loại bỏ để làm cho nó trở nên vô nghĩa và không đúng ngữ pháp tiếng Latinh. Hai từ đầu tiên là [dạng rút gọn](https://en.wikipedia.org/wiki/Clipping_\(morphology\) "Cắt tỉa (hình thái học)") của _dolorem ipsum_ ("chính là nỗi đau"). Mục đích của lorem ipsum là cho phép thiết kế bố cục trang, độc lập với nội dung văn bản sẽ được điền vào sau đó, hoặc để minh họa các phông chữ khác nhau của một kiểu chữ mà không có văn bản có ý nghĩa gây mất tập trung.[^17] (Dịch tạm là vậy)

![[LaTeX-Library-project-v1.0.0/images/lorem Ipsum.jpg]]
(Nguồn ảnh: https://priceonomics.com/the-history-of-lorem-ipsum/)

Để sử dụng được đoạn văn bản giả Lorem ipsum ở trong LaTeX, trước tiên người dùng cần phải khai báo Package

```latex
\usepackage{lipsum} 
```

được đặt ở . . . (vị trí nào trong phần soạn thảo ?):

Sau đó người dùng chỉ cần đặt các lệnh sau vào phần . . . ( phần nào của soạn thảo ?)

Với lệnh 

```latex
\lipsum
```

hệ thống sẽ tự động xuất sang trang tài liệu khoảng bảy đoạn văn bản lorem ipsum mặc định.

```latex
\documentclass{article}
\begin{document}
\lipsum
\end{document}
```

Với lệnh 

```latex
\lipsum[1-150]
```

hệ thống sẽ tự động xuất sang trang tài liệu đầy đủ từ 1 đến 150  đoạn văn bản lorem ipsum mặc định. 

```latex
\documentclass{article}
\usepackage{lipsum} 
\begin{document}
\lipsum[1-150]
\end{document}
```

. . . (150 đoạn văn bản lorem khác nhau, đây cũng chính là giới hạn . . . ,  nếu như người dùng sử dụng)

```latex
\lipsum[1000]
```

thì hệ thống sẽ tự động xuất sang trang tài liệu đoạn văn Lorem thứ 100. 

Lý do là bởi 

. . . 1000:150 . . . lấy ở đoạn văn Lorem thứ 100) 


---
## Thay đổi kích cỡ chữ: 

Để thay đổi kích cỡ chữ trong trang tài liệu, người dùng chỉ cần thêm thông số vào bên trong dấu ngoặc vuông `[]` ở phần khai báo lớp tài liệu (`documentclass`). 

Xem qua ví dụ đoạn mã dưới đây:

```latex
\documentclass[12pt]{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```

người dùng có thể thấy bảy đoạn văn bản [lorem ipsum]() trong trang tài liệu đều sẽ có kích cỡ chữ là 12pt.  

Thông số được thêm vào bên trong dấu ngoặc vuông đó đối với LaTeX chỉ có thể được thay đổi đối với ba kích cỡ cơ bản là 10pt, 11pt và 12pt. 

Nếu như người dùng không thêm bất kì tùy chọn thông số nào làm thay đổi kích cỡ chữ, thì hệ thống sẽ mặc định để kích cỡ chữ trong trang tài liệu là 10pt. 

```latex
\documentclass{article}
\usepackage{lipsum} % lorem ipsum
\begin{document}
\lipsum
\end{document}
```

--- 

##  Tóm tắt bài báo: 

Trong LaTeX, các lớp tài liệu học thuật như **`article`** (bài báo) hay **`report`** (báo cáo), luôn có phần được gọi “tóm tắt”.

Để viết phần tóm tắt, người dùng cần sử dụng môi trường `abtract` với cú pháp sau. 

```latex
\begin{abstract}
    ... Nội dung tóm tắt của bạn viết tại đây ...
\end{abstract}
```

![](./images/img4.1.jpg)

Môi trường `abstract` này được đặt ngay sau lệnh `\maketitle`.

> [!WARNING]  
> Môi trường `abstract` này không thể được thực thi với các lớp tài liệu là `book`, `letter`, $\dots vv \dots$

Nếu như người dùng muốn thay đổi tiêu đề mặc định của LaTeX là "tóm tắt nội dung" (tiếng Việt) hay "abstract" (tiếng Anh), người dùng cần sử dụng lệnh sau: 

```latex
\renewcommand{\abstractname}{New Name}
```

Với lệnh này, tiêu đề ở phần tóm tắt sẽ được thay thế bằng bất kỳ từ nào khác mà người dùng cung cấp.  

Ví dụ minh họa về phần tóm tắt vào trong một tài liệu. 

```latex
\documentclass{article} 
\usepackage[utf8]{vietnam} % Khai báo tài liệu viết Tiếng Việt

% Khai báo thông tin tài liệu
\title{An Example of LaTeX Document} 
\author{Namlete} 
\date{May 30, 2026} 

\begin{document} 

% 1. Hiển thị tiêu đề, tác giả, ngày tháng bài viết 
\maketitle 

% 2. Hiển thị phần tóm tắt bài viết
\renewcommand{\abstractname}{Tóm tắt} % Thay đổi dòng "Tóm tắt nội dung" mặc định thành "Tóm tắt". 

\begin{abstract} 
    Đây là nơi bạn viết một đoạn tóm tắt ngắn gọn (khoảng 150-250 từ) 
    về mục tiêu, phương pháp và kết quả chính của bài nghiên cứu này.
\end{abstract} 

% 3. Nội dung chính của tài liệu
Hello LaTeX! 

\end{document}
```

---

## Viết tài liệu tiếng Việt 

Để viết tài liệu tiếng Việt, ta cần khai báo gói sau:

```latex
\usepackage[utf8]{vietnam}
```

Bộ encode **UTF-8** là package thông dụng để hiển thị các chữ cái Latin trong tiếng Anh, kể cả các chữ cái Hy Lạp và Việt Nam. (?)

---

## Ngắt trang

Để viết tài liệu sang một trang tài liệu mới, người dùng sử dụng lệnh sau: 

```latex
\newpage
```

---

## Xuống dòng văn bản: 

Người dùng chỉ cần nhấn phím **Enter** được nhập trên bàn phím hai lần, để làm văn bản được xuống dòng mới khi soạn thảo LaTeX. (? viết chưa rõ ý tưởng)

---

## Thụt lề đầu dòng các đoạn văn trong văn bản

Khi [xuống dòng văn bản]() trong LaTeX, hệ thống sẽ tự động thụt lề đầu dòng cho đoạn văn mới. 

Thông thường, hệ thống sẽ mặc định tự động thụt lề đầu dòng vào một khoảng 20pt. Tuy nhiên người dùng có thể tự căn chỉnh nó bằng cách thêm vào câu mở đầu lệnh có cú pháp như sau: 

```latex
\setlength{\parindent}{length}
```

trong đó:

- length: là kích thước thụt đầu dòng mà người dùng muốn khi đoạn văn xuống dòng.

Với length = 0, tất cả các đoạn văn đều trong trang tài liệu đều không được thụt lề đầu dòng. 

Kích thước thụt lề đầu dòng đoạn văn được . . . (bên đối tượng nào ?) khuyến nghị (nên thụt lề với khoảng cách là bao nhiêu khi viết tài liệu là hợp lí ?) . . . 

Nếu như người dùng muốn lựa chọn tùy ý việc để đoạn văn tiếp theo có hay không thụt đầu dòng, người dùng có thể sử dụng hai lệnh sau. Với 

```latex
\indent
```

được dùng để đoạn văn đó thụt đầu dòng. Và 

```latex
\noindent
```

được dùng để đoạn văn đó không thụt đầu dòng.

Cả hai lệnh `\indent` và `\noindent` đều phải được đặt ở trước đoạn văn mà người dùng mong muốn có hay không thụt đầu dòng. 

Kích thước thụt lề đầu dòng của lệnh `\indent` là 20pt (? viết lại chưa hiểu ý cho lắm )

---

## Khoảng cách giữa các đoạn văn trong văn bản:

Để tùy chỉnh khoảng cách giữa các đoạn, ta sử dụng lệnh

```latex
\setlength{\parskip}{#}
```

trong đó:

- \# là kích thước khoảng cách giữa các đoạn văn mà người dùng muốn khi đoạn văn xuống dòng.  

--- 

## Khoảng cách giữa các dòng trong đoạn văn:

Đầu tiên, người dùng cần phải khai báo package sau:

```latex
\usepackage{setspace}
```

Từ đây, người dùng có thể chọn một trong hai cách sau đây để thay đổi khoảng cách giữa các dòng.

**Cách 1**: Thêm những lệnh sau trước đoạn văn để thay đổi khoảng cách giữa các dòng

```latex
\singlespacing
\onehalfspacing 
\doublespacing
\setstretch{<float number>}
```

trong đó:

- `\singlespacing`: thay đổi khoảng cách giữa các dòng là bằng 1.
- `\onehalfspacing`: thay đổi khoảng cách giữa các dòng là bằng 1.5 .
- `\doublespacing`: thay đổi khoảng cách giữa các dòng là bằng 2.
- `\setstretch{<float number>}`: thay đổi được khoảng cách giữa các dòng tùy ý trong khoảng lớn hơn 1 và nhỏ hơn 2. 

**Cách 2**: Sử dụng môi trường spacing
```latex
\begin{spacing}
Văn bản
\end{spacing}
```

trong đó spacing có thể được thay thế bằng:

- `singlespace`: thay đổi khoảng cách giữa các dòng là bằng 1.
- `onehalfspace`: thay đổi khoảng cách giữa các dòng là bằng 1.5 .
- `doublespace`: thay đổi khoảng cách giữa các dòng là bằng 2.

Để thay đổi được khoảng cách giữa các dòng tùy ý trong khoảng lớn hơn 1 và nhỏ hơn 2, người dùng chỉ cần thêm bên cạnh `\begin{spacing}` là `{<float number>}`,  lúc này ta có:
```latex
\begin{spacing}{<float number>}
Khoảng cách gữa các dòng trong một đoạn văn được thay đổi bởi <float number>
\end{spacing}
```

Ví dụ sau đây . . .

---

## Căn lề cho đoạn văn bản:

Hệ thống LaTeX sẽ để căn lề mặc định cho đoạn văn bản là "[justified]()" (căn đều hai bên).  

Để có thể thay đổi căn lề cho đoạn văn bản, người dùng có thể sử dụng môi trường sau:
```latex
\begin{alignment type}
	Nội dung...
\end{alignment type}
```

Trong đó, alignment type có thể là:
<p align="left">
+ flushleft: Căn trái
</p>
<p align="right">
+ flushright: Căn phải
</p>
<p align="center">+ center: căn giữa</p>
Ngoài ra người dùng có thể đặt các lệnh sau: 

```latex
\raggedright % Căn trái
\raggedleft % Căn phải
\centering
```

vào trước các đoạn văn bản để được tùy chỉnh căn lề cho đoạn văn đó. 

. . . 

---

## In đậm, in nghiên, gạch chân chữ, chữ gạch giữa:

Đối với **in đậm**, người dùng sử dụng lệnh

```latex
\textbf{in đậm}
```

_In nghiêng_ thì sẽ là

```latex
\textit{in nghiêng}
```

Vậy vừa _**in đậm, in nghiêng**_ thì làm sao nhỉ ? Để làm được điều này, người dùng có thể lồng lệnh *in nghiêng* vào trong lệnh **in đậm** như sau 

```latex
\textbf{\textit{Vừa in đậm, vừa in nghiêng}}
```

Hoặc nếu như người dùng lồng lệnh `\textit` vào trong lệnh `\textbf`, thì kết quả cho ra được vẫn sẽ giống hệt với cách làm trên. 

Để <u>gạch chân chữ</u> (underline), người dùng sử dụng lệnh

```latex
\underline{Gạch chân chữ}
``` 

Đối với ~~chữ gạch giữa~~ (strikethrough), trước tiên người dùng cần phải khai báo package sau

```latex
\usepackage{soul}
```

sau đó để ~~chữ gạch giữa~~ người dùng sử dụng lệnh 

```latex
\st{Chữ gạch giữa}
```

. . . (Này là gì ? Có tác dụng gì ? Mục đích sử dụng ? Khi nào thì nên sử dụng ?)

```latex
\emph{}
```

Ví dụ với các đoạn văn sau 

```latex
Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .
```

Từ "khám phá" trong đoạn mã trên sẽ được *in nghiêng* so với các từ khác trong đoạn văn. 

```latex
\textit{Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .}
```

Từ "khám phá" trong đoạn mã trên sẽ không được in nghiêng so với các từ khác trong đoạn văn đang nằm trong lệnh `\textit{}` đang được *in nghiêng*. 

```latex
\textbf{Một số \emph{khám phá} vĩ đại nhất trong khoa học được thực hiện một cách tình cờ như . . .}
```

Từ "khám phá" trong đoạn mã vẫn sẽ được **in đậm** giống như các từ khác trong đoạn văn đang nằm trong lệnh `\textbf{}`, tuy vậy từ "khám phá" sẽ được *in nghiêng* so với các từ khác trong đoạn văn.  

--- 

## Màu chữ:[^8]

Đầu tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{xcolor}
```

Package ở trên chỉ cho phép người dùng sử dụng được 19 màu cơ bản theo các tên màu đã được có sẵn mà không cần phải thêm bất kỳ `options` nào trong package như hình dưới đây.

![19 màu cơ bản](./images/img1.1.jpg)

Người dùng cũng có thể sử dụng thêm các màu ngoài 19 màu cơ bản trên theo ý muốn, cũng thông qua gói `xcolor` với các `options` như sau: 

1. `dvipsnames`: tải 68 màu được đặt tên (CMYK) 

```latex
\usepackage[dvipsnames]{xcolor}
```

![68  màu CMYK](./images/img1.2.jpg)

2. `x11names`: tải 317 màu được đặt tên (RGB) 
```latex
\usepackage[x11names]{xcolor}
```
![317 màu RGB ](./images/img1.3.jpg)

Để thay đổi màu sắc chữ người dùng sử dụng lệnh sau: 

```latex
\textcolor{color}{text}
```

trong đó:
- `color`: là nơi nhập tên màu sắc cho văn bản mà người dùng muốn, với điều kiện là màu được chọn phải phù hợp với `options` mà người dùng khai báo theo những hình ở trên.
- `text`: từ hoặc văn bản bị thay đổi thành màu mà người dùng lựa chọn. 

--- 

## Màu nền trang:

Người dùng cũng có thể thay đổi [màu]() nền của toàn bộ trang tài liệu tùy thích ngoài mặc định sẵn của LaTeX là trang tài liệu có màu trắng truyền thống, bằng cách sử dụng lệnh sau:

```latex
\pagecolor{color}
```

Lệnh này được đặt ở . . . 

---

## Nhập nền cho văn bản (highlight):

Để có thể tô đậm [màu]() cho đoạn văn bản, dòng văn bản hoặc các từ khóa quan trọng trong trang tài liệu, người dùng sử dụng lệnh sau:

```latex
\colorbox{color}{text}
```


---

## Lệnh phân cấp (Sectioning commands)

Đối với các lớp tài liệu (`documentclass`) như `article`, `proc`, `report`, `book`, `beamer`, chúng đều có các lệnh phân cấp nhằm tạo [mục lục]() để sắp xếp nội dung. 

Các lệnh phân cấp này không đứng ngang hàng với nhau, mà được sắp xếp theo một thứ tự ưu tiên từ cao xuống thấp

| Tên (Việt - Anh)              | Lệnh           | Cấp độ |
| :---------------------------- | -------------- | ------ |
| Phần (Part)                   | `\part{}`      | -1     |
| Chương (Chapter)              | `\chapter{}`   | 0      |
| Mục (Section)                 | `\section`     | 1      |
| Tiểu mục (Subsection)         | `\subsection{}`| 2      |
| Tiểu tiểu mục (Subsubsection) | `\subsubsection{}` | 3|
| Paragraph (Đoạn văn (có tiêu đề))| `\paragraph{}`  |  4 |
| Subparagraph (Đoạn văn (có tiêu đề) cấp nhỏ hơn)|`\subparagraph{}`| 5|

Tùy thuộc vào `documentclass` mà người dùng đang sử dụng mà thứ tự cấp độ ở bảng trên sẽ có chút thay đổi. 

Cụ thể, lệnh `\chapter` chỉ khả dụng trong các lớp tài liệu là `report` và `book`, mà không thể được sử dụng đối với lớp tài liệu là `article`, `proc`. 

Nếu như người dùng cố gắng viết lệnh `\chapter` vào phần soạn thảo LaTeX đang ở lớp tài liệu như `article`, `proc`, thì hệ thống sẽ báo lỗi khi người dùng biên dịch sang tài liệu. (lỗi gì nhỉ ?)

Đối với lớp tài liệu là `beamer`, các lệnh `\chapter`,  `\paragraph`,  `\subparagraph` không thể được thực thi. 

Một số lớp tài liệu như `minimal`, `letter` được thiết kế cho các mục đích rất tối giản, do đó chúng loại bỏ hầu hết hoặc toàn bộ các lệnh phân cấp. (? đoạn này còn mơ hồ quá, rốt cuộc nếu bỏ hầu hết thì còn những gì ? nếu vậy thì bỏ đoạn toàn bộ các lệnh phân cấp . . .)

Các tiêu đề được viết trong các lệnh phân cấp này sẽ được hệ thống hoàn toàn tự động đánh số ở trước nó như trong ví dụ sau đây đối với lớp tài liệu là `book`: 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section{Phương pháp nghiên cứu} % Vì thuộc Chương 2 nên mục này sẽ tự động được đánh số là: 2.1 Phương pháp nghiên cứu
Đây là mục đầu tiên của chương 2.

\end{document}
```

Nếu như người dùng không muốn các tiêu đề trước nó được đánh số, người dùng chỉ cần thêm dấu `*` vào trong giữa lệnh phân cấp và dấu ngoặc nhọn `{}` của lệnh đó. 

Để dễ hình dung, ta quay lại với ví dụ ở trên. Nếu như người dùng thêm dấu `*` vào giữa lệnh `\section` và dấu ngoặc nhọn đang chứa tiêu đề là "Phương pháp nghiên cứu" 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\part{Đây là phần I}  % Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên} % Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan} % Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1} % Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2} % Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính} % Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai} % Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu} % Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

thì tiêu đề của mục "Phương pháp nghiên cứu" ở chương 2, sẽ chỉ hiển thị chữ **"Phương pháp nghiên cứu"** mà không có số `2.1` ở phía trước như trong đoạn mã trước đó. 

---


 ki## Mục lục (Table of Contents)

Để tạo mục lục trong tài liệu đối với một số lớp tài liệu có thể được sử dụng [lệnh phân cấp](), người sử dụng lệnh 

```latex
\tableofcontents 
```

được đặt bên trong môi trường `document` và ngay sau lệnh `\maketitle`.

Ta lấy lại đoạn mã ví dụ ở bài học [lệnh phân cấp]() và thêm lệnh `\tableofcontents` vào trong đoạn mã đó. 

```latex
\documentclass{book}
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents % Mục lục 

\part{Đây là phần I} 
% Lớp book mặc định đánh số Phần bằng chữ số La Mã (Phần I, Phần II,...)

\chapter{Đây là chương đầu tiên}
% Lớp book tự động thêm chữ "Chương 1" vào trước tiêu đề này

\section{Giới thiệu tổng quan}
% Sẽ được tự động đánh số là: 1.1 Giới thiệu tổng quan
Đây là nội dung của mục đầu tiên.

\subsection{Tiểu mục chi tiết 1}
% Sẽ được tự động đánh số là: 1.1.1 Tiểu mục chi tiết 1
Đây là nội dung của tiểu mục đầu tiên.

\subsection{Tiểu mục chi tiết 2}
% Sẽ được tự động đánh số là: 1.1.2 Tiểu mục chi tiết 2
Đây là nội dung của tiểu mục thứ hai.


\section{Nội dung chính}
% Sẽ được tự động đánh số là: 1.2 Nội dung chính
Đây là mục thứ hai trong Chương 1.


\chapter{Đây là chương thứ hai}
% Hệ thống tự động nhảy sang "Chương 2"

\section*{Phương pháp nghiên cứu}
% Có dấu * nên mục này sẽ KHÔNG được đánh số (Unnumbered section) và KHÔNG xuất hiện trong Mục lục.
Đây là mục đầu tiên của chương 2 nhưng không có số thứ tự phía trước.

\end{document}
```

Ta thấy các tiêu đề được đặt trong lệnh phân cấp đều hiển thị ở trong phần mục lục, chỉ riêng `\section*{Phương pháp nghiên cứu}` là không xuất hiện ở đó.  

Để thêm mục không đánh số (Unnumbered section) vào mục lục, người dùng sử dụng lệnh sau:

```latex
\addcontentsline{toc}{section}{Tiêu đề của phần}
```

. . . . (?)

Nếu như tiêu đề người dùng viết quá dài, chúng sẽ bị . . . khi xuất hiện ở phần mục lục như trong ví dụ dưới đây: 

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Để khắc phục vấn đề này, người dùng chỉ cần viết một tiêu đề gọn lại ở trong dấu ngoặc vuông `[]` . . .  Áp dụng điều này vào lại ví dụ trên:  

```latex
\documentclass{article}

% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[utf8]{vietnam}

\begin{document}

\tableofcontents

\section[Tiêu đề rút ngọn]{Tiêu đề phần nội dung này rất là dài và cần rút gọn bớt khi hiển thị trong mục lục}

\end{document}
```

Người dùng có thể thấy tiêu đề ở ví dụ . . . đã được rút ngắn, gọn gàng lại khi hiện ở phần mục lục trong trang tài liệu.   

---
## Danh sách: 

Danh sách trong LaTeX bao gồm: danh sách không có thứ tự, danh sách có thứ tự và danh sách mô tả. 
### a. Danh sách không có thứ tự: 

Đối với danh sách không có thứ tự ta có lệnh sau: 

```latex
\begin{itemize} % môi trương danh sách không có thứ tự
    \item . . . % Liệt kê 
\end{itemize}
```

Ví dụ về danh sách không có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{itemize} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{itemize}
\end{document}
```
### b. Danh sách có thứ tự: 

Danh sách có thứ tự trong LaTeX là danh sách được liệt kê theo thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự mặc định 
    \item . . . % liệt kê 
\end{enumerate}
```

Ví dụ về danh sách có thứ tự về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
Liệt kê các loại danh sách phổ biến trong \LaTeX{} bằng môi trường \verb|enumerate|
\begin{enumerate} 
    \item Danh sách không có thứ tự
    \item Danh sách có thứ tự
    \item Danh sách mô tả
\end{enumerate}
\end{document}
```

Nếu người dùng muốn sử dụng các . . . (`\item`) khác với mặc định mà LaTeX đưa ra, chẳng hạn thay vì liệt kê với số thứ tự mặc định từ 1 đến số lượng danh sách cuối cùng được đưa ra, người dùng cũng có thể liệt kê với số thứ tự theo kiểu chữ số La Mã là I, II, III, $\dots vv \dots$ hoặc cũng có thể được thay bằng chữ cái thường hoặc in hoa. 

Để làm được điều trên, người dùng chỉ cần thêm dấu `[]` bên cạnh `\item` của môi trường danh sách có thứ tự và đặt bên trong đó là kí hiệu mà người dùng muốn thay đổi sẽ xuất hiện ở đầu mỗi phần liệt kê của danh sách này: 

```latex
\begin{enumerate} % môi trường danh sách có thứ tự
    \item[thay đổi tại đây] . . . % liệt kê
\end{enumerate}
```

Đối với các chữ cái Hy Lạp cổ đại như $\alpha, \beta, ..vv..$ hay kí hiệu toán học (xem ở phần [toán học]()), người dùng cần đặt chúng vào bên trong một cặp dấu đô la đơn  `$...$`  và cặp dấu đô la đơn này sẽ được đặt ở bên trong dấu ngoặc vuông `[]`.

Ví dụ về danh sách có thứ tự với `\item` được kí hiệu theo chữ các Hy Lạp cổ đại về các loại danh sách có trong LaTeX: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}
\begin{enumerate} 
    \item[$\alpha$] Danh sách không có thứ tự
    \item[$\beta$] Danh sách có thứ tự
    \item[$\gamma$] Danh sách mô tả
\end{enumerate}
\end{document}
```

### c. Danh sách lồng nhau:

Đối với các dang sách lồng vào nhau, người dùng chỉ cần thêm một danh sách con vào phần `\item` của môi trường danh sách cha đang sử dụng. 

Chẳng hạn ta có thể lồng danh sách có thứ tự mặc định của LaTeX vào các `item` của danh sách cha là danh sách không có thứ tự : 
```latex
\begin{itemize} % danh sách cha không có thứ tự  
    \item . . . % liệt kê
    \begin{enumerate} % danh sách con có thứ tự mặc định của LaTeX 
            \item . . . % liệt kê   
        \end{enumerate}
    \item . . . % liệt kê 
\end{itemize}
```

Ví dụ về . . . 
```latex

```

### d. Danh sách mô tả: 

Danh sách mô tả dùng để . . . 

Để tạo danh sách mô tả trong LaTeX, người dùng cần sử dụng môi trường `description` với lệnh sau: 
```latex
\begin{description} 
\item[Từ khóa 1] Mô tả hoặc giải thích cho từ khóa 1. 
\item[Từ khóa 2] Mô tả hoặc giải thích cho từ khóa 2. 
\item[Từ khóa 3] Mô tả hoặc giải thích cho từ khóa 3. 
\end{description}
```

--- 

## Liên kết thông thường:

Đầu tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{hyperref}
```

Người dùng có thể thêm liên kết đến địa chỉ web vào phần soạn thảo LaTeX bằng cách **trực tiếp** hoặc **gián tiếp** sau.

### a. Chèn liên kết trực tiếp:

Sử dụng lệnh sau:

```latex
\url{<my_url>}
```

URL sẽ được hiển thị bằng phông chữ đơn cách ([monosaced font]), và nếu người dùng nhấp vào đó, trình duyệt web sẽ mở ra và trỏ đến đúng URL mà người dùng chèn vào lệnh.

Nếu như người dùng không thích để URL hiển thị với phông chữ đơn cách và muốn chúng được in với cùng kiểu chữ với phần còn lại của văn bản, người dùng có thể sử dụng lệnh sau:
```latex
\urlstyle{same}
```

Ví dụ đối với cách chèn link trực tiếp:

```latex
\documentclass{article} 
% Language setting
% Replace `english' with e.g. `spanish' to change the document language
\usepackage[english]{babel}
% Useful packages
\usepackage{hyperref} % 
\urlstyle{same} % 
% 
\title{Your Paper} 
\author{You}
\date{\today}
\begin{document}
\maketitle
\url{<https://github.com/Namlete102/LaTeX-Library-project-1.0.0>} % 
\end{document}
```

### b. Chèn liên kết gián tiếp:

Sử dụng lệnh sau:

```latex
\href{<my_url>}{description}
```

Nó sẽ hiển thị phần `description` bằng phông chữ chuẩn của tài liệu khi soạn. Khi người dùng nhấp vào phần `description` đó trên tài liệu, trình duyệt web sẽ mở ra và trỏ đến đúng URL bên trong `<my_url>` mà người dùng đã dùng để chèn vào lệnh trên.

Ví dụ:
```latex
\href{<https://github.com/Namlete/LaTeX-Library-project>}{Thư viện LaTeX}
```

Cả hai cách **trực tiếp** hoặc **gián tiếp** trên đều cùng trỏ đến trang của trình duyệt web. Nhưng với cách **trực tiếp**, thì URL sẽ được hiển thị trực tiếp ngay trên tài liệu. Trong khi cách **gián tiếp** thì URL sẽ bị ẩn, thay vào đó là chỉ hiển thị `description` mà người dùng đã chèn URL vào.

Ngoài việc có thể được sử dụng để chèn liên kết đến các trang web bằng phương pháp **gián tiếp** trên, lệnh `\href` có thể được sử dụng để cung cấp đến các **liên kết địa chỉ email**, **liên kết tệp nội bộ,** **liên kết đến bất kỳ đâu trong tệp PDF đầu ra ,v**à cũng như là **chèn liên kết thủ công (Inserting links manually).**

#### b.1. Liên kết địa chỉ email:

Sử dụng lệnh sau:
```latex
\href{mailto: <my_email>}{<my_email>}
```

Ví dụ:
```latex
\href{mailto: nguyenlenam15082007@gmail.com}{nguyenlenam15082007@gmail.com}
```

. . .

Xem lại tại đây: 
https://www.overleaf.com/learn/latex/Hyperlinks#Styles_and_colours 

--- 
## Siêu liên kết văn bản:

Để sử dụng siêu liên kết văn bản, người dùng cần phải khai báo package đã nêu ở bài học **Liên kết thông thường** trong phần soạn thảo LaTeX.

Package `hyperref` sẽ đảm nhiệm việc chuyển các **tham chiếu** trong tài liệu thành siêu liên kết.

Các thiết lập mặc định của LaTeX thường phù hợp với hầu hết người dùng. Cụ thể, nếu người dùng chỉ cần khai báo package `hyperref` là xong, mà không cần các thiết lập nào nữa khác, thì LaTeX sẽ chỉ kích hoạt ứng dụng mặc định của gói đó là siêu liên kết các tham chiếu và hiển thị các khung $\color{red}{\text{màu đỏ}}$ đối với [mục lục]() hoặc cũng có thể là [chú thích](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.1.jpg"
         alt="khung màu đỏ (mục lục) khi siêu liên kết văn">
	<figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>. </figcaption>
</figure>

khung $\color{cyan}{\text{màu xanh dương}}$ đối với [liên kết thông thường](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.2.jpg"
         alt="khung màu xanh dương (mục lục) khi siêu liên kết văn">
    <figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>. </figcaption>
</figure>

và khung $\color{green}{\text{màu xanh lá}}$ đối với [tài liệu tham khảo](), 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.3.jpg"
         alt="Khung màu xanh lá">
	<figcaption>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>.</figcaption>
</figure>

Các khung hiện <font color="red">màu đỏ</font>, <font color="lightblue">màu xanh dương</font>, <font color="lightgreen">màu xanh lá</font> như vậy chỉ có trong tài liệu lúc người dùng vẫn còn làm việc ở trong phần soạn thảo LaTeX, giúp người dùng dễ dàng điều hướng. Các khung đó sẽ không còn xuất hiện ở trang tài liệu của người dùng khi tải về đề in. 

<figure>
    <img src="LaTeX-Library-project-v1.0.0/images/img2.4.jpg"
         alt="Khung màu sẽ biến mất khi tải tệp">
	<figcaption>Ảnh lụm được ở . . . .</figcaption>
</figure>

Nhưng nếu người dùng muốn thay đổi, chẳng hạn màu sắc của đường link sẽ bị thay đổi khi di chuột qua hoặc thay đổi màu sắc của đường link $\dots vv \dots$ , thì điều này cũng hoàn toàn có thể.

Bằng cách sử dụng lệnh:

```latex
\hypersetup{
    variable_name = new_value,
}
```

trong đó:
- `variable_name`: Là thuộc tính cấu hình do gói `hyperref` định nghĩa sẵn để điều khiển cách hoạt động hoặc hiển thị của các liên kết.
- `new_value`: Là giá trị bạn muốn gán cho thuộc tính đó để thay đổi thiết lập mặc định.

Người dùng có thể truyền `variable_name = new_value` vào `\hypersetup` bao nhiêu tùy thích, tùy thuộc vào kinh nghiệm của người dùng. Nên nhớ, hãy phân tách giữa các tên biến (`variable_name`) khác nhau bằng dấu phẩy, khi người dùng sử dụng chúng để thiết lập cho siêu liên kết văn bản. 

| **`variable_name`** | **`new_value`** | **Nhận xét**                                                                                                          |
| ------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------- |
| bookmarks           | = true, false   | Hiển thị (true) hoặc ẩn (false) cửa sổ Bookmark khi hiển thị tài liệu                                                 |
| unicode             | = true, false   | Có (true) hay không (false) cho phép sử dụng kí tự không có trong ngôn ngữ gốc Latin trong phần bookmarks của Acrobat |
| pdftoolbar          | = true,false    | Hiển thị (true) hay ẩn (false) thanh công cụ của Acrobat khi xem.                                                     |
| pdfmenubar          | = true,false    | Hiển thị (true) hay ẩn (false) thanh menu của Acrobat.                                                                |
|                     |                 |                                                                                                                       |

Để giúp người dùng tùy chỉnh nhanh hơn, đi cùng với đó là kết hợp với phần tham khảo bảng trên để theo dõi. Dưới đây sẽ là đoạn mã lệnh các biến với giá trị mặc định của chúng. Sao chép đoạn này vào trang soạn thảo tài liệu LaTeX và thực hiện các thay đổi, tùy ý của người dùng. Bên cạnh các tên biến và giá trị của biến đó là kèm theo dòng giải thích ngắn gọn về ý nghĩa của chúng. 

```latex
\hypersetup {
    bookmarks = true,          % hiển thị thanh dấu trang?
    unicode = false,           % ký tự không phải Latinh trong dấu trang của Acrobat
    pdftoolbar = true,         % hiển thị thanh công cụ của Acrobat?
    pdfmenubar = true,         % hiển thị menu của Acrobat?
    pdffitwindow = false,      % cửa sổ vừa với trang khi mở
    pdfstartview = {FitH} ,     % vừa chiều rộng của trang với cửa sổ
    pdftitle = {My title} ,     % tiêu đề
    pdfauthor = {Author} ,      % tác giả
    pdfsubject = {Subject} ,    % chủ đề của tài liệu
    pdfcreator = {Creator} ,    % người tạo tài liệu
    pdfproducer = {Produce} , % nhà sản xuất tài liệu
    pdfkeywords = {keyword1, key2, key3} , % danh sách từ khóa
    pdfnewwindow =true,       % liên kết trong cửa sổ PDF mới
    colorlinks = false,        % false: liên kết được đóng khung; true: liên kết có màu
    linkcolor = red,           % màu của các liên kết nội bộ (thay đổi màu khung bằng linkbordercolor)
    citecolor = green,         % màu của các liên kết đến thư mục tham khảo
    filecolor = cyan,          % màu của các liên kết tệp
    urlcolor = magenta,         % màu của các liên kết bên ngoài
}
```

Nếu người dùng không cần tùy chỉnh quá nhiều, sau đây lại là một vài ví dụ nhỏ nhưng hữu ích về việc tùy chỉnh siêu liên kết bằng các `variable_name` một cách đơn giản, hiệu quả cao mà người dùng có thể tham khảo.

Ví dụ: Khi xuất file PDF để in, các liên kết có màu không phải là lựa chọn tốt vì chúng sẽ bị chuyển thành màu xám trong bản in cuối cùng, gây khó đọc. Bằng cách sử dụng đoạn mã sau:

```latex
\usepackage{hyperref}
\hypersetup{
	colorlinks = false,
}
```

Hoặc cũng có thể làm cho các siêu liên kết đều có màu đen:

```latex
\usepackage{hyperref}
\hypersetup{
	links = black,
}
```

Ví dụ: Các liên kết trong phần soạn thảo LaTeX được tạo ra, tùy chỉnh dựa trên định dạng tài liệu sẽ đọc ở định dạng PDF. Tệp PDF có thể được tùy chỉnh để bổ sung thêm thông tin và thay đổi cách trình xem PDF hiển thị.

```latex
\hypersetup {
    colorlinks = true,
    linkcolor = blue,
    filecolor = magenta,
    urlcolor = cyan,
    pdftitle = {Overleaf Example}, % Tiêu đề của tập tin PDF đầu ra
    pdfpagemode = FullScreen,
}
```

<div align="center">

<img src="./images/img2.5.jpg">

</div>

. . . (còn nữa mà chưa soạn xem thêm dưới đây:  
https://en.wikibooks.org/wiki/LaTeX/Hyperlinks#Hyperlink_and_Hypertarget) 

---
## Các vấn đề với đường link:[^4]


---
## Chèn ảnh: [^10]

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

## Chèn bảng

. . . 

--- 

## Chèn code:

Có hai kiểu chèn code bao gồm: `inline code` và `block code`. Trong đó: 
+ `inline code` là: 
+ `block code` là: 

### Inline code

Sử dụng lệnh sau:

```latex
\verb|. . .|
```
. . . 

---

## Chú thích (footnote) [^3]

Để chú thích ý nghĩa hoặc thông tin thêm cho một từ/cụm từ nào đó trong LaTeX, người dùng chỉ cần đặt lệnh 

```latex
\footnote{văn bản chú thích}
```

vào ngay sau từ mà người dùng cần được chú thích.  

Từ/cụm từ được chú thích sẽ xuất hiện thêm ở sau nó một chỉ số nhỏ nằm ở phía trên. Chỉ số này sẽ được hệ thống tự động thêm, cập nhật theo theo thứ tự tăng dần với các số mặc định là $1, 2, 3 \dots$, tương ứng với số lượng chú thích có trong trang tài liệu. 

Phần nội dung chú thích bên trong dấu ngoặc nhọn `{}` của lệnh `\footnote` sẽ được tự động hiển thị ở chân trang tài liệu hiện tại, có chỉ số nhỏ hiện thị ở trước phần nội dung đó sao cho tương ứng với chỉ số nhỏ hiển thị của từ/cụm từ được chú thích. 

Dưới đây là ví dụ về việc chú thích nhà vật lý Coulomb:

```latex
\documentclass[11pt]{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document} 
Phương trình toán học mô tả lực tương tác tĩnh điện giữa hai điện tích điểm trong chân không, được tìm thấy bởi nhà vật lý Coulomb\footnote{Charles-Augustin de Coulomb (1736 - 1806) là một sĩ quan, kỹ sư và nhà vật lý người Pháp, nổi tiếng với định luật mang tên ông là định luật Coulomb và ông còn được được đặt cho đơn vị SI đo điện tích (kí hiệu là C)}  
\[
F = k_e \frac{|q_1 q_2|}{r^2}
\]
\end{document}
```

> [!NOTE] 
> Người viết khuyên người dùng nên viết lệnh `\footnote` dính liền ngay sau từ cần chú thích, không nên để khoảng trắng ở giữa, vì điều này giúp chỉ số nhỏ hiển thị ở phía trên từ đó không bị nhảy hàng lỗi khi từ đó nằm ở cuối dòng văn bản. 

Trong trường hợp người dùng muốn tự quyết định chỉ số hiển thị của chú thích theo ý muốn của người, thay vì để LaTeX tự động đánh số $1, 2, 3 \dots$, người dùng có thể để `option` từ lệnh

```latex
\footnote[số thứ tự mới]{văn bản chú thích}
```

vào bên trong dấu ngoặc `[]` với bất kỳ số nguyên nào được nhập từ bàn phím. 

Áp dụng điều này vào lại ví dụ trên ta có

```latex
\documentclass[11pt]{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

% --- Các gói hỗ trợ toán học ---
\usepackage{amssymb} 
\usepackage{amsmath}

\begin{document} 

Phương trình toán học mô tả lực tương tác tĩnh điện giữa hai điện tích điểm trong chân không, được tìm thấy và chứng minh bởi nhà vật lý Coulomb\footnote[42]{Charles-Augustin de Coulomb (1736 - 1806) là nhà vật lý người Pháp, nổi tiếng với định luật mang tên ông là định luật Coulomb}: 

\[
F = k_e \frac{|q_1 q_2|}{r^2}
\]

\end{document}
```

Lúc này, trên trang tài liệu, người dùng có thể thấy rằng từ "Coulomb" lúc này mang chỉ số nhỏ hiển thị phía trên là **42**, còn ở chân trang phần nội dung chú thích của từ "Coulomb" cũng sẽ bắt đầu bằng số **42**.

<div align="center">

<img src="./images/Coulomb.jpg" alt="Coulomb">

Nhà vật lý người Pháp Charles-Augustin de Coulomb

</div>

---

## Toán học: [^5] [^7]

#### Giới thiệu:

Một trong những động lực lớn nhất thúc đẩy [Donald Knuth]() khi bắt đầu phát triển hệ thống TeX ban đầu là tạo ra một công cụ cho phép xây dựng các công thức toán học một cách đơn giản, đồng thời trông chuyên nghiệp khi in ấn. Việc ông thành công có lẽ là lý do tại sao TeX (và sau này là LaTeX) trở nên phổ biến trong cộng đồng khoa học. Việc trình bày toán học là một trong những thế mạnh lớn nhất của LaTeX. Đây cũng là một chủ đề rộng lớn do sự tồn tại của rất nhiều ký hiệu toán học.[^6] 

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

Điều này cũng tương tự, khi người dùng viết số phần trăm 

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

---

#### `inline math`, `display math`: 

. . . (? Giới thiệu) với 1+1 = 2 ở ví dụ . . . chúng được gọi là `inline math` còn nguyên lý bất định hải sơn bắc là `displaymath`. 

LaTeX cung cấp đầy đủ hai chế độ trình bày toán học chính bao gồm
+ `inline math`(**toán học nội tuyến**): được sử dụng để viết các biểu thức, kí hiệu toán học nằm trong cùng ở đoạn văn bản.
+ `display math`(**toán học hiển thị**): được sử dụng để viết các biểu thức, kí hiệu toán học không thuộc ở đoạn văn và được trình bày trên các dòng riêng biệt. 

---

##### **inline math**:

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
<img src="./images/Pythagoras.jpg" alt="Pythagoras">
<p>Triết gia và nhà toán học người Hy Lạp cổ đại xứ Samos Pythagoras</p>
</div>

---

##### **display math**:

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

<img src="LaTeX-Library-project-v1.0.0/images/Kakeya.jpg" alt="John Napier">

Ảnh được cắt từ trang 1 bài báo toán học <a src="https://drive.google.com/file/d/1dlpgd5Q5AAOsaCFQK5MGRisJNUPmgxFu/view?usp=sharing" target="_blank">"A STREAMLINED PROOF OF THE KAKEYA SET CONJECTURE IN \(\mathbb{R^3}\)</a> của ba nhà toán học <a src="https://math.mit.edu/~lguth/" target="_blank">Larry Guth</a>, <a src="https://sites.google.com/view/hongwang/home" target="_blank">Vương Hồng</a>, <a src="https://jzahl.github.io/" target="_blank">Joshua Zahl</a>

</div>

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/Guth Hong Zahl.jpg" alt="Guth Hong Zahl">

Nhà toán học Lary Guth, nhà toán học Vương Hồng và nhà toán học Joshua Zahl

</div>

Để chuyển số thứ tự đó nằm từ bên phải sang bên trái như hình . . ., người dùng chỉ cần thêm `options` 

```latex
leqno
```

ở phần khai báo lớp tài liệu (`\documentclass`). 

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

$$\log_b{xy} = \log_b{x} + \log_b{y}$$

<div align="center"> 

<img src="./images/John Napier.jpg" alt="John Napier">

Nhà toán học người Scotland John Napier

</div>

---
### Chữ cái Hy Lạp

Để viết kí hiệu, chữ cái toán học ở chế độ là `inline math`, cũng như là `display math`, người dùng chỉ cần viết chúng ở bên trong các các cặp kí hiệu, môi trường mà người viết đã trình bày ở [`inline math`, `display math`](). 

Ví dụ về . . . 

```latex
\documentclass{article}
\begin{document}
\[
(i \gamma^\mu \partial_\mu - m) \psi = 0
\]
\end{document}
```

Người dùng có thể thấy, trong phương trình tính . . . của nhà vật lý Paul Dirac, có chữ cái Hy Lạp lần lượt là $\gamma$ (đọc là gamma) và $\mu$ (đọc là mu) được dùng để . . .(? để làm gì trong phương trình đó)

$$
(i \gamma^\mu \partial_\mu - m) \psi = 0
$$

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/Paul Dirac.jpg" alt="Paul Dirac">

Nhà vật lý lý thuyết người Anh Paul DIrac

</div>

Người dùng có thể tham khảo đầy đủ ở [danh sách các kí hiệu toán học, chữ cái Hy Lạp](), nếu như người dùng chưa biết hoặc là nếu quên cách ghi các kí hiệu, chữ cái toán học đó trong lúc soạn thảo LaTeX. 

--- 

### Phông chữ toán học 

Một số yếu tố toán học cần được trình bày bằng các kiểu phông chữ khác chẳng hạn các ký tự/ký hiệu theo một kiểu nhất định, khác nhau khi trình bày toán học. [^14] (?)

Ví dụ . . .: Người dùng có thể viết kí hiệu toán học của các tập số theo kiểu chữ đậm bảng đen (?) như tập các số tự nhiên $\mathbb{N}$, tập các số nguyên $\mathbb{Z}$, tập các số thực $\mathbb{R}$, $\dots vv \dots$ 

Để viết được các kiểu phông chữ khác nhau dành cho kí hiệu toán học, trước tiên người dùng cần phải khai báo package sau: 

```latex
\usepackage{amssymb}
```

Package `amssymb` . . . (? Giới thiệu và giải thích đôi điều gói này)

Để viết được phông chữ các kí hiệu về tập số ở ví dụ . . . trên, người dùng cần để chữ cái thường được nhập trực tiếp bàn phím đó vào lệnh

```latex
\mathbb{}
```

Với kí hiệu tập số tự nhiên ta viết như sau 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amssymb}
\begin{document}
Tập hợp các số tự nhiên được kí hiệu là $\mathbb{N}$
\end{document}
```

Áp dụng tương tự điều này lại với các tập số khác. 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amssymb}
\begin{document}
Tập hợp các số mà người dùng từng được học ở phổ thông, bao gồm: 
\begin{itemize}
	\item Tập hợp các số nguyên được kí hiệu là $\mathbb{Z}$
	\item Tập hợp các số hữu tỉ được kí hiệu là $\mathbb{Q}$
	\item Tập hợp các số thực được kí hiệu là $\mathbb{R}$
	\item Tập hợp các số phức được kí hiệu là $\mathbb{C}$
\end{itemize} 
Với . . . (? giới thiệu thêm các tập số khác như H, O)
\end{document}
```

<div align="center">

<img src="./images/Setnumber.jpg" alt="Hành tím">

Ảnh lụm được ở <a href="https://www.facebook.com/photo.php?fbid=488758739928398&set=pb.100063828282373.-2207520000&type=3">Mathtasy Toán học thú vị</a>

</div>

Ví dụ . . . chỉ là một phần nhỏ trong một số [kiểu phông chữ khác nhau dành cho kí hiệu toán học]() mà người dùng có thể tham khảo thêm.

https://www.overleaf.com/learn/latex/Mathematical_fonts 

---
### Dấu ngoặc: [^1]  

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

Ví dụ về dấu ngoặc tròn với định lý Taylor[^23] . . . (? viết tiếp phần định lý Taylor này)

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

#### 1. Nguyên tắc hiển thị dấu ngoặc nhọn `\{ \}`

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

#### 2. Quy tắc tự động thay đổi kích thước (Auto-resizing)

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

#### 3. Cú pháp dấu ngoặc một bên 

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

Kết quả cho ra được vẫn sẽ tương tự với kết quả ta có được ở trên. 

<div align="center">

<img src="./images/Fibonacci.jpg" alt="Fibonacci">

Nhà toán học người Ý Fibonacci

</div>


. . . (viết tiếp ví dụ với dấu ngoặc lớn hiển thị ở bên phải mà ko có ở bên trái)

Tham khảo: https://gemini.google.com/app/4475fd095760fba9?hl=vi 

--- 

### Chỉ số trên và chỉ số dưới: 

Để viết chỉ số trên người dùng sử dụng kí hiệu `^`, còn với chỉ số dưới người dùng sử dụng kí hiệu `_` . 

Các kí hiệu chỉ số trên và chỉ số dưới được đặt ở sau kí hiệu, chữ cái toán học. (? viết chưa hợp lí lắm, cần viết lại)

Ví dụ về chỉ số trên với phương trình từ định lý cuối cùng của Fermat được chứng minh bởi nhà toán học Andrew Wiles 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
x^n + y^n = z^n, \forall x,y,z, n \in \mathbb{Z^+}, n > 2 % chỉ số trên được viết ở cạnh các ẩn số x, y, z
\]
\end{document}
```

Kết quả cho ra được sẽ là:

$$
x^n + y^n = z^n, \forall x,y,z, n \in \mathbb{Z^+}, n > 2
$$

<div align="center">

<img src="./images/Andrew Wiles.jpg" alt="Andrew Wiles">

Nhà toán học người Anh Andrew Wiles

</div>

Ví dụ về chỉ số dưới với phương trình entropy của nhà vật lý Boltzmann thể hiện mối quan hệ giữa entropy và số cách sắp xếp các nguyên tử hoặc phân tử của một hệ nhiệt động nhất định [^2]

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[S = k_b \cdot \Omega\] % chỉ số dưới được viết ở biểu thức k_b
\end{document}
```

Kết quả cho ra được sẽ là:

$$
S = k_b \cdot \Omega 
$$

<div align="center">

<img src="./images/Boltzmann.jpg" alt="Ludwig Boltzmann">

Nhà vật lý người Áo Ludwig Boltzmann

</div>

Các kí hiệu chỉ số trên và chỉ số dưới cũng có thể được kết hợp trong cùng một biểu thức $C^k_n$ (đọc là tổ hợp chập $k$ của $n$ phần tử) như ở ví dụ về công thức nhị thức Newton giúp khai triển lũy thừa bậc nguyên dương của một tổng thành tổng các đơn thức 

```latex
\documentclass{article}
\begin{document}
\[
(a + b)^n = C^k_n a^{n-k} b^k % . . .C^k_n
\]
\end{document}
```

Kết quả nhận được sẽ là 

$$
(a + b)^n = C^k_n a^{n-k} b^k
$$

<div align="center">

<img src="./images/Isaac Newton.jpg" alt="I.Newton">

Nhà vật lý người Anh Isaac Newton

</div>

Cũng ở ví dụ về công thức nhị thức Newton trên, người dùng có thể thấy để viết được biểu thức dài $n-k$ ở chỉ số trên của $a$, chúng cần được gom lại trong dấu ngoặc nhọn `{}` được đặt sau kí hiệu chỉ số trên.

Điều này cũng được áp dụng tương tự đối với chỉ số dưới. 

Ví dụ . . . với phương trình trường hấp dẫn Einstein mô tả trọng lực không phải là một lực kéo thông thường theo quan điểm vật lý cổ điển của nhà vật lý Isaac Newton, mà là hệ quả của sự uốn cong không-thời gian do khối lượng và năng lượng . . .  gây ra.  

```latex
\documentclass{article}
\begin{document}
\[
R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R + g_{\mu\nu}\Lambda = \frac{8\pi G}{c^4}T_{\mu\nu} 
\] 
\end{document}
```

$$
R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R + g_{\mu\nu}\Lambda = \frac{8\pi G}{c^4}T_{\mu\nu} 
$$

Người dùng có thể thấy, để viết được bao quát chỉ số dưới $\mu\nu$, chúng cần được viết đấy đủ vào trong dấu ngoặc nhọn `{}` ở sau kí hiệu chỉ số dưới. 

<div align="center">

<img src="./images/Albert Einstein.jpg" alt="Einstein">

Nhà vật lý người Đức Albert Einstein

</div>

---

### Khoảng cách trong chế độ toán học:  [^12]

Khi người dùng viết toán học,  . . . (nêu vấn đề)

Để điều chỉnh khoảng cách giữa các biểu thức, toán tử . . . người dùng chỉ cần thêm lệnh ở bảng sau đây 

| Lệnh LaTeX | Mô tả                                                   | Ví dụ         |
| :--------- | :------------------------------------------------------ | ------------- |
| `\quad`    | = 18 mu                                                 | $a \quad b$   |
| `\qquad`   | $= 2 \cdot$`\quad` (= 36 mu)                            | $a \qquad b$  |
| `\enskip`  | $= \frac{1}{2} \cdot$`\quad` (= 9 mu)                   | $a \enskip b$ |
| `\,`       | $= \frac{3}{18} \cdot$`\quad` (= 3 mu)                  | $a \, b$      |
| `\:`       | $= \frac{4}{18} \cdot$`\quad` (= 4 mu)                  | $a \: b$      |
| `\;`       | $= \frac{5}{18} \cdot$`\quad` (= 5 mu)                  | $a \; b$      |
| `\!`       | $= \frac{-3}{18} \cdot$`\quad` (= -3 mu)                | $a \! b$      |
| `\`        | tương đương với khoảng trắng trong văn bản thông thường | $a \ b$       |

(Bảng tham khảo từ [Overleaf](https://www.overleaf.com/learn/latex/Spacing_in_math_mode#Spaces)) 

vào ngay bên cạnh . . . (? bên cạnh gì)

Với các [toán tử quan hệ]()  

Ví dụ về khoảng cách trong chế độ toán học với . . . 

. . .

---

### Viết văn bản trong chế độ toán học:  

Khi viết văn bản trong toán học, chẳng hạn . . . (nên viết lại thành một vấn đề ví dụ mới)

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
Văn bản trong toán học
\]
\end{document}
```

Kết quả cho ra được là các từ sẽ được hệ thống sắp in nghiêng và bị dính vào nhau

$$
Văn bản trong toán học 
$$

Để viết được văn bản trong toán học, người dùng cần sử dụng lệnh `\text{}` để ngăn cách phần toán học với phần văn bản.  

Áp dụng điều này vào lại ở ví dụ trên ta có 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
\text{Văn bản trong toán học}
\]
\end{document}
```

Kết quả lúc này sẽ khác hoàn toàn so với khi chưa thêm văn bản vào trong lệnh `\text`

$$
\text{Văn bản trong toán học}
$$


Một số hàm trong toán học chẳng hạn như hàm lượng giác, . . vv . . được khuyến nghị . . . (? bởi ai, điều gì) soạn thảo ở dạng phông chữ thẳng đứng . . . (viết sau) 

Chẳng hạn, khi viết công thức . . . , nếu như người dùng chỉ viết hàm $\cos$ thông thường

```latex

```

 thì chúng sẽ bị in nghiêng khi xuất sang trang tài liệu 

. . . (kết quả từ ví dụ)

Để viết hàm $\cos$  . . ., người viết chỉ cần thêm dấu `\` bên cạnh hàm đó như . . . . 

```latex

```

Kết quả lúc này sẽ khác hẳn so với khi ta chưa thêm dấu `\` vào trước hàm $\cos$ đó. 

Điều này, còn được áp dụng với một số hàm khác, chẳng hạn như [giới hạn]() . . .

```latex

```


Với một số hàm toán học đã được LaTeX cung cấp . . ., nếu người dùng sử dụng dấu `\` để viết cho một . . . khác thì chúng sẽ báo lỗi . . . (? gì)  

```latex
\nam
```

Xem đầy đủ các hàm được LaTeX . . . tại [danh sách các kí hiệu toán học, chữ cái Hy Lạp]().  

---

### Màu trong toán học[^15] 

(? vì sao đôi khi ta cần màu trong công thức toán học) 

Để viết các kí hiệu toán học có màu, người dùng có thể sử dụng lệnh `\textcolor` ở bài học [màu chữ]() hoặc cũng có thể thay thế lệnh đó bằng lệnh mới sau

```latex
\mathcolor{color}{text}
```

Tương tự như lệnh `textcolor`, người dùng có thể sử dụng các màu mặc định hoặc khác ngoài 19 màu cơ bản như đã nêu ở bài học [màu chữ]() cho lệnh `mathcolor`  

Ví dụ . . .  với công thức Euler về mối liên hệ giữa đỉnh, cạnh, mặt của khối đa diện lồi. Cụ thể, với mọi khối đa diện lồi nào, số đỉnh trừ đi số cạnh cộng với số mặt luôn cho ra kết quả là bằng 2: [^16]

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath} % for the equation* environment
\usepackage{xcolor} % for text color 

\begin{document}

\[\mathcolor{red}{V} - \mathcolor{blue}{E} + \mathcolor{green}{F} = 2\]

trong đó: 

\begin{itemize}
    \item \textcolor{red}{V}: Số đỉnh (Vertex) của khối đa diện lồi
    \item \textcolor{blue}{E}: Số cạnh (Edge) của khối đa diện lồi
    \item \textcolor{green}{F}: Số mặt phẳng (Face) của khối đa diện lồi
\end{itemize}
\end{document}
```

$$
\textcolor{red}{V} - \textcolor{blue}{E} + \textcolor{green}{F} = 2 
$$

<div align="center">

<img src="./images/Leonhard Euler.jpg" alt="Euler">

Nhà toán học người Thụy Sĩ Leonhard Euler

</div>

---

### Viết phương trình dài: 

+ Sử dụng môi trường multline 

```latex
\begin{multline*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
- 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{multline*}
```

$$
\begin{multline*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
- 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{multline*}
$$


---

### Căn chỉnh phương trình:  

Gợi ý viết ví dụ: 
+ Thuật toán Euclid để tìm UCLN 
+ Môi trường split giúp khai triển chẳng hạn như ví dụ ở overleaf đây

```latex
\begin{split}
A & = \frac{\pi r^2}{2} \\
 & = \frac{1}{2} \pi r^2
\end{split}
```

$$
\begin{split}
A & = \frac{\pi r^2}{2} \\
 & = \frac{1}{2} \pi r^2
\end{split}
$$
+ Môi trường gather giúp khai triển các phương trình liên tiếp, căn giữa mà không cần quan tâm đến bất kỳ sự căn chỉnh nào 

```latex
\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}
```

$$
\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}
$$

--- 

### Viết nhiều phương trình toán học cùng lúc (? đặt lại tên tiêu đề)

Với việc viết một phương trình toán học, người dùng có thể sử dụng các lệnh, môi trường mà người viết đã trình bày ở hai bài học . . . một cách dễ dàng.  

Tuy vậy, trong trường hợp người dùng cần viết nhiều hơn nhiều phương trình cùng một lúc, chẳng hạn như phương trình Maxwell được trích từ tài liệu học MIT sau https://web.mit.edu/8.02t/www/802TEAL3D/visualizations/coursenotes/modules/guide13.pdf . . (? lấy mẫu ví dụ nào đó ở đâu đó để giúp người dùng hình dung ban đầu) 

Để làm được điều này, trước tiên người dùng nhớ cần phải khai báo package `amsmath`.  Nếu như người dùng không khai báo package đó, thì hệ thống sẽ báo lỗi . . .  

Sau đó, người dùng chỉ cần đặt các lệnh, môi trường . . . (? đặt gì) vào trong môi trường `subequations` 

```latex
\begin{subequations}
. . .
\end{subequations}
```

Người dùng có thể để cũng như chọn tùy ý bao nhiêu . . . (? bao nhiêu về cái gì) vào trong môi trường `subequation` đó.   

Ví dụ: (với phương trình Maxwell)

```latex
. . .  
```


---

### Tiên đề, định nghĩa, định lý, định luật, mệnh đề, bổ đề, giả thiết, bằng chứng, hệ quả, ví dụ ... :[^19]

. . .  (Giới thiệu các định nghĩa trên ở phần sau cuốn sách)   

. . .  Để sử dụng được định nghĩa, . . . . (gồm những gì nữa) trước tiên người dùng cần phải khai báo chúng vào lệnh 

```latex
\newtheorem{}{}
```

trong đó: 
+ (giải thích hai dấu ngoặc nhọn kia)
+ 

(? lệnh này được đặt ở đâu và lệnh mới này có ý nghĩa gì trong xuyên suốt LaTeX) 

Khi biên dịch sang trang tài liệu, nếu như các từ định nghĩa, định lý, ..vv.. được gõ bằng ngôn ngữ tiếng Anh thì chúng sẽ được xuất sang trang tài liệu các từ đó là tiếng Anh. 

Ví dụ với môi trường định lý về định lý  Gauss - Wantzel và môi trường định nghĩa về định nghĩa số nguyên tố Fermat trong lĩnh vực . . . của toán học, trong đó từ định lý và định nghĩa được viết bằng ngôn ngữ tiếng Anh:  

```latex
\documentclass{article}

% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng bảng mã utf8 để gõ tiếng Anh hoặc ký tự đặc biệt bình thường
\usepackage[utf8]{inputenc}

% Khai báo môi trường "Theorem" (Định lý) và "Definition" (Định nghĩa) trong tiếng Anh
\newtheorem{theorem}{Theorem}
\newtheorem{definition}{Definition}

\begin{document}

% ==========================================
% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
% ==========================================
\begin{theorem}[Gauss--Wantzel]
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
The division of a circle into $n$ equal parts using a straightedge and compass is possible if and only if
% Công thức hiển thị ở dạng khối (display math mode)
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các biến trong công thức
where $k$ is a non-negative integer and $p_1, p_2, \dots, p_t$ are distinct Fermat primes.
\end{theorem}

% ==========================================
% SECTION: ĐỊNH NGHĨA SỐ NGUYÊN TỐ FERMAT
% ==========================================
\begin{definition}[Fermat prime]
% Khai báo dạng tổng quát của số Fermat
An integer of the form 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để một số Fermat trở thành số nguyên tố Fermat
is called a Fermat prime if the output value calculated from $F_n$ is a prime number.
\end{definition}

\end{document}
```

Điều này cũng được áp dụng tương tự với tất cả với [ngôn ngữ khác](). Chẳng hạn, để viết các từ trên từ tiếng Anh sang tiếng Việt, người dùng trước tiên cần phải khai báo package [ngôn ngữ tiếng Việt ](), và sau đó người dùng chỉ cần gõ lại từ theorem (tiếng Anh) sang định lý (tiếng Việt), ..vv.. ở dấu ngoặc nhọn ngoài cùng của lệnh trên. (? Viết lại phần "...ở dấu ngoặc nhọn ngoài cùng ...") 

Quay trở lại ví dụ trên, lúc này từ định lý và định nghĩa đều được viết sang ngôn ngữ tiếng Việt 

```latex
\documentclass{article}

% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt tốt hơn trong LaTeX
\usepackage[utf8]{vietnam}

% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Việt
\newtheorem{theorem}{Định lý}
\newtheorem{definition}{Định nghĩa}

\begin{document}

% ==========================================
% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
% ==========================================
\begin{theorem}[Gauss--Wantzel]
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% ==========================================
% SECTION: ĐỊNH NGHĨA SỐ NGUYÊN TỐ FERMAT
% ==========================================
\begin{definition}[Số nguyên tố Fermat]
% Khai báo dạng tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để một số Fermat trở thành số nguyên tố Fermat
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

\end{document}
```

Người dùng cũng có thể sử dụng lệnh `\newtheorem` nhằm để tên chính định lý, định nghĩa, ..vv.. đó thay vì từ "định nghĩa", "định lý", ..vv.. thông thường như ví dụ trên. 

Cụ thể, ta có thể ghi lại "Định lý Gauss - Wantzel" thay cho "Định lý 1 (Gauss - Wantzel)". 

```latex
\newtheorem{theorem}{Định lý Gauss - Wantzel}
```

Tương tự đối với định nghĩa về số nguyên tố Fermat. 

```latex
\newtheorem{theorem}{Số nguyên tố Fermat}
```

Áp dụng điều này vào lại ví dụ . . . , lúc này ta được: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

\end{document}
```

Trong trường hợp người dùng muốn viết định lý mới, nếu như người dùng sử dụng lại môi trường theorem đã được định nghĩa ban đầu, thì ở phần tiêu đề định lý mới đó vẫn sẽ xuất hiện "Định lý Gauss - Wantzel" như ở hai định lý . . . (? Hai định lý gì nhỉ) 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% Định lý . . . 

\begin{theorem}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{theorem}

\end{document}
```

Để khắc phục được điều trên, người dùng cần phải định nghĩa một môi trường mới cho định lý. 

Cần phải đảm bảo rằng, nếu như người dùng đã định nghĩa môi trường định lý với từ "theorem" trong dấu ngoặc lệnh `\newtheorem`, thì chúng không được lặp lại lần nữa khi người dùng muốn sử dụng chúng để viết một định lý khác. 

Điều này cũng áp dụng tương tự đối với định nghĩa (definition), ..vv.. 

Nếu như người dùng định nghĩa môi trường định lý với từ **theorem** đã được sử dụng ở môi trường định lý Gauss - Wantzel, thì hệ thống sẽ báo lỗi . . .  như ở ví dụ . . . dưới đây: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{theorem}{Định lý} % từ theorem ở lệnh đây bị trùng với theorem ở lệnh trên nó. (? Viết lại cmt này)
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% - - - -

\begin{theorem}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_{n}-1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{theorem}

\end{document}
```

Từ những điều đã nêu ở trên, lúc này để viết một hay nhiều định lý mới khác mà không bị trùng lặp với định lý đã được định nghĩa ban đầu, ta chỉ cần đặt tên . . .(? gì, ở đâu) khác đi. 

Cụ thể, thay vì sử dụng đầy đủ tên gọi **theorem**, lúc này ta chỉ cần viết tắt lại thành **thm**: 

```latex
\newtheorem{thm}{Định lý}
```

và ở . . . (? ở đâu trong phần soạn thảo LaTeX)

```latex
\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
	    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}
```

Từ đây ta viết lại ví dụ . . . như sau:  

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý} 
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

\end{document}
```

Người dùng có thể áp dụng tương tự . . . (? Áp dụng tương tự điều gì) để khắc phục đoạn mã định lý "$F_5$ là hợp số" như sau:

Người dùng có thể thấy rằng, bên cạnh các  . . . (? tên định lý đó) vẫn sẽ xuất hiện số thứ tự bên cạnh. 

. . . (Để không muốn có số thứ tự bên cạnh. . . ), trước tiên người dùng cần phải khai báo package sau: 

```latex
\usepackage{amsthm} % for theorem environments
```

. . . (giải thích đôi chút gói amsthm này)  

Sau đó người dùng chỉ cần thêm dấu `*` ở sau lệnh `\newtheorem` và trước hai dấu ngoặc nhọn (? mô tả hơi chán, nên viết lại sau): 

```latex
\newtheorem*{}{}
```

Quay lại với ví dụ . . . lúc này đoạn mã có được: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} % for theorem environments

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}
\newtheorem*{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

\end{document}
```

Với bài viết chia [mục lục]() . . . ta chỉ cần thêm các lệnh . . .  tương ứng với phần tiêu đề . . .đó vào . . .

Ví dụ . . : Nếu như tiêu đề mục đang được sử dụng là lệnh `\section`, thì ta chỉ cần thêm . . . vào   

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}

\begin{document}

% . . . 
\section{Giới thiệu}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% . . . 
\section{Một số tính chất về tính nguyên tố của số Fermat}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

\end{document}
```

(? Nêu vấn đề vì sao ta lại phải phân biệt định nghĩa, định lý) 

Khai báo package: 

```latex
\usepackage{amsthm} 
```

Nhằm phân biệt được định nghĩa, định lý, ..vv.. trong trang tài liệu toán học người dùng sử dụng lệnh

```latex
\theoremstyle{stylename}
```

trong đó **stylename** gồm các kiểu cơ bản mặc định của hệ thống được tổng hợp ở bảng sau:[^20]

| stylename  | Đặc điểm và công dụng                                                                                                                                                                                 | Ví dụ                                 |
| :--------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| definition | Tiêu đề in đậm, nội dung chữ thường. Được sử dụng trong định nghĩa, điều kiện, vấn đề và đưa ra ví dụ.                                                                                                | **Định nghĩa** 1: Nội dung định nghĩa |
| plain      | Tiêu đề in đậm, nội dung in nghiêng. Được sử dụng trong các định lý, bổ đề, hệ quả, mệnh đề và giả thuyết.                                                                                            | **Định lý 2**: *Nội dung định lý*     |
| remark     | Tiêu đề in nghiêng, nội dung in thường. Được sử dụng trong nhận xét, ghi chú, chú thích (notes), tuyên bố (annotations), trường hợp (claims), lời cảm ơn (acknowledgments) và kết luận (conclusions). | *Nhận xét 3*: Nội dung nhận xét       |

Ví dụ về stylename **definition** với định nghĩa số nguyên tố Fermat 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% . . . 
\theoremstyle{definition}
\newtheorem*{definition}{Số nguyên tố Fermat}


\begin{document}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

\end{document}
```

Ví dụ về stylename **plain** với các định lý . . . 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\theoremstyle{plain}
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 


\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

\end{document}
```

Ví dụ về stylename **remark** với nhận xét về các số nguyên tố Fermat :

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amsthm}
\theoremstyle{remark} 
\newtheorem*{remark}{Nhận xét} 
\begin{document}
\begin{remark}
Fermat nhận ra 5 số Fermat đầu tiên là \(F_0 = 3, F_1 = 5; F_2 = 17, F_3 = 257, F_4 = 65537\) đều là số nguyên tố và ông đã nhận định rằng $F_n$ là số nguyên tố với mọi giá trị của $n$. Tuy nhiên, đến năm 1732, nhà toán học người Thụy Sĩ là Leohard Euler đã tìm thấy F5 là hợp số.
\end{remark}
\end{document}
```

Bằng chứng (tiếng anh là proof) là . . . 

Để viết bằng chứng trong soạn thảo LaTeX, người dùng sử dụng môi trường `proof`

```latex
\begin{proof}
. . .
\begin{proof}
```

Với môi trường `proof`, chúng đã được có trong sẵn package `amsthm` mà ta đã khai báo ở . . . (phần bài học nhân xét mà không đánh số ở trên) 

Ví dụ về môi trường `proof` với chứng minh định lý số Fermat $F_5$ là hợp số 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amsthm}
\usepackage{amssymb}
\begin{document}
\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}
\end{document}
```

Khi kết thúc phần chứng minh cho định lý, mệnh đề, bổ đề, ..vv.. nào đó trong toán học, chúng ta luôn kết lại bằng câu "điều phải chứng minh".  Điều này bắt nguồn từ . . . (? một chút lịch sử về việc tại sao phải có điều này)

và được viết tắt ngắn gọn lại là QED[^18] . 

Để sử dụng từ QED khi kết thúc chứng minh, người dùng sử dụng lệnh: 

```latex
\renewcommand\qedsymbol{QED}
```

được đặt ở {? ở đâu}

Từ QED trên thông thường được thay thế ngắn gọn lại bằng một [kí hiệu đặc biệt]() ô vuông trắng 

```latex
\renewcommand{\qedsymbol}{$\square$} 
```

hoặc đôi khi là một ô vuông đen 

```latex
\renewcommand\qedsymbol{$\blacksquare$}
```

Các lệnh trên đều phải được đặt trước môi trường `proof` như ở ví dụ . . . đây

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amsthm}
\usepackage{amssymb}
\begin{document}
\renewcommand\qedsymbol{QED}
\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}
\end{document}
```

Viết lại đầy đủ từ . . . (? từ đâu)

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\theoremstyle{plain}
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 
\theoremstyle{definition}
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}
\theoremstyle{remark}
\newtheorem{remark}{Nhận xét} 

\begin{document}

% . . . 
\section{Giới thiệu}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% Chứng minh định lý Gauss - Wantzel 

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}

% . . . 
\section{Một số tính chất về tính nguyên tố của số Fermat}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% Chứng minh định lý F_5 là hợp số

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}

% Định lý . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

% Chứng minh . . . . 

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof} 

\end{document}
```

<div align="center">
	
<img src="LaTeX-Library-project-v1.0.0/images/Fermat Gauss Wantzel.jpg" alt="Fermat Gausss Wantzel">

Nhà toán học người Pháp Fermat (trái), nhà toán học người Đức Gauss (giữa) và nhà toán học người Pháp Wantzel (phải)

</div>

---

### Các bài học toán khác 

Viết toán học luôn là chủ đề yêu thích của tác giả, vậy nên có lẽ sẽ hợp lý nếu như tác giả vừa giới thiệu phần chủ đề toán học, cũng như là cách viết các kí hiệu toán học đó trên LaTeX thì sẽ một công đôi việc, mang đến cảm giác thú vị đến người đọc.

Trước tiên, người viết cần làm rõ cấu trúc viết . . . 

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/LoveMath.jpg">

Keep calm and love math

</div>


---

#### Toán tử:  

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

#### Liên phân số:  [^13]

Đối với một . . . (ở bài học này chúng ta sẽ học cách viết phân số, liên phân số, ...)

\+ Phân số được định nghĩa là . . .   

Ví dụ: $0.5 = \frac{1}{2}$ trong đó $\frac{1}{2}$ chính là phân số của số thập phân hữu hạn $0.5$  

Để viết được phân số, ta sử dụng lệnh : 

```latex
\frac{tử số}{mẫu số}
```

Viết lại phần số $\frac{1}{2}$ bằng lệnh trên 

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

#### Giới hạn, đạo hàm, tích phân: 

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

#### Vector, ma trận: 

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

#### Số phức:  

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

### Danh sách các kí hiệu toán học, chữ cái Hy Lạp[^22]

Tham khảo trang 70 tài liệu đây: **Một tài liệu ngắn gọn giới thiệu về LATEX 2ε - hay LATEX 2ε trong 155 phút**,  https://www.cmor-faculty.rice.edu/~heinken/latex/symbols.pdf, https://www.cmor-faculty.rice.edu/~heinken/latex/symbols.pdf, cũng như là **LaTeX Formal Methods Reference**  https://www.cs.put.poznan.pl/ksiek/latexmath.html#id2

#### Các dấu trọng âm trong chế độ soạn thảo toán học: 

| Lệnh        | Kí hiệu     | Lệnh        | Kí hiệu     | Lệnh          | Kí hiệu       | Lệnh            | Kí hiệu         |
| :---------- | ----------- | ----------- | ----------- | ------------- | ------------- | --------------- | --------------- |
| `\hat{a}`   | $\hat{a}$   | `\check{a}` | $\check{a}$ | `\tilde{a}`   | $\tilde{a}$   | `\acute{a}`     | $\acute{a}$     |
| `\grave{a}` | $\grave{a}$ | `\dot{a}`   | $\dot{a}$   | `\ddot{a}`    | $\ddot{a}$    | `\breve{a}`     | $\breve{a}$     |
| `\bar{a}`   | $\bar{a}$   | `\vec{a}`   | $\vec{a}$   | `\widehat{A}` | $\widehat{A}$ | `\widetilde{A}` | $\widetilde{A}$ |

#### Các chữ cái Hy Lạp viết thường 


![](LaTeX-Library-project-v1.0.0/images/img6.1.jpg)

(trang chú trang 57 từ tài liệu **Một tài liệu ngắn gọn giới thiệu về LATEX 2ε - hay LATEX 2ε trong 155 phút** 

| Lệnh     | Kí hiệu  | Lệnh        | Kí hiệu     | Lệnh     | Kí hiệu  | Lệnh       | Kí hiệu    |
| :------- | -------- | ----------- | ----------- | -------- | -------- | ---------- | ---------- |
| `\alpha` | $\alpha$ | `\theta`    | $\theta$    | `o`      | $o$      | `\upsilon` | $\upsilon$ |
| `\beta`  | $\beta$  | `\vartheta` | $\vartheta$ | `\pi`    | $\pi$    | `\phi`     | $\phi$     |
| `\gamma` | $\gamma$ | `\iota`     | $\iota$     | `\varpi` | $\varpi$ | `\varphi`  | $\varphi$  |
| `\delta` | $\delta$ | `\kappa`    | $\kappa$    | `\rho`   | $\rho$   | `\chi`     | $\chi$     |
|          |          |             |             |          |          |            |            |

. . . 


---

## Chèn tài liệu tham khảo: 



---

## Tham chiếu chéo:  

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

Trong một số trường hợp, khi người dùng viết tài liệu toán học cần [tham chiếu]() từ đoạn văn bản này đến phương trình toán học ở chế độ `display math`, mà không cần phải viết lặp lại, cũng như sẽ bị tràn ra khỏi văn bản đối với các [phương trình dài]() (? của phương trình đó ở chế độ `inline math` . . . (? viết tiếp đê)    

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

---
# c. Các bài học bên lề khác 

Đây là những bài học mở rộng khác liên quan đến LaTeX. 

## Viết mã LaTeX sao cho đẹp và sạch ? 

---

# d. Footnote 

[^1]: Nguồn tham khảo viết ở Overleaf: https://www.overleaf.com/learn/latex/Brackets_and_Parentheses 

[^2]: https://en.wikipedia.org/wiki/Boltzmann%27s_entropy_formula

[^3]: Nguồn tham khảo viết chú thích ở Overleaf: https://www.overleaf.com/learn/latex/Footnotes)

[^4]: Nguồn tham khảo viết các vấn đề siêu liên kết ở Overleaf: https://en.wikibooks.org/wiki/LaTeX/Hyperlinks#Troubleshooting

[^5]: Nguồn tham khảo viết toán học ở Overleaf: https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Adding_math_to_LaTeX. 

[^6]: https://en.wikibooks.org/wiki/LaTeX/Mathematics

[^7]: Nguồn tham khảo lời viết này sử dụng ở Wikibook: https://en.wikibooks.org/wiki/LaTeX/Mathematics

[^8]: Nguồn ảnh màu LaTeX: https://tex.stackexchange.com/questions/659029/colour-packages-beyond-xcolor 

[^9]: Nguồn tham khảo viết chèn hình ảnh ở Overleaf bao gồm: https://www.overleaf.com/learn/latex/Inserting_Images%23Positioning#Introduction; https://www.overleaf.com/learn/latex/Positioning_images_and_tables

[^10]: Nguồn tham khảo tử Overleaf: https://www.overleaf.com/learn/latex/Inserting_Images%23Positioning

[^12]: Tham khảo từ bài học Overleaf: https://www.overleaf.com/learn/latex/Spacing_in_math_mode

[^13]: Tham khảo từ bài tạp chí Epsilon: https://epsilonvn.github.io/archives/epsilon_vol01_2015February.pdf

[^14]: Tham khảo từ Overleaf: https://www.overleaf.com/learn/latex/Mathematical_fonts

[^15]: Tham khảo cuốn "How to Reproduce this Book Exactly with LaTeX A Self-contained Tutorial on Writing Mathematical Notes" trang 47. 

[^16]: Nguồn tài liệu tham khảo phần công thức Euler ở tạp chí Pi: https://drive.google.com/file/d/1O_QiD8GcipW0DXclsRH7HoWUsnr9pE4y/view?usp=sharing)

[^17]: Nguồn copy: https://en.wikipedia.org/wiki/Lorem_ipsum 

[^18]: Không nên nhầm lẫn với định nghĩa QED ở các lĩnh vực khác: https://en.wikipedia.org/wiki/QED

[^19]: Tham khảo viết từ: https://paulwintz.com/mathematical-writing/theorem-like-environments-in-latex/ và bài viết về "Số Fermat" của các tác giả 

[^20]: Nguồn viết: https://www.overleaf.com/learn/latex/Theorems_and_proofs#Reference_guide + https://en.wikibooks.org/wiki/LaTeX/Theorems#Theorem_styles

[^21]: Nguồn tham khảo viết: https://mathworld.wolfram.com/BezoutsTheorem.html

[^22]: Tham khảo và chỉnh sửa từ: https://sg.mirrors.cicku.me/ctan/info/symbols/comprehensive/symbols-a4.pdf

[^23]: Công thức tham khảo từ: https://mathworld.wolfram.com/TaylorSeries.html 
