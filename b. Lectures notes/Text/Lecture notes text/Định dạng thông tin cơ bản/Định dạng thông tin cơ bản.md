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

<div align="center">
  <img src="./img abstract/img3.1.jpg">
</div>

Người dùng cũng có thể sử dụng điều này để trình bày nhiều hơn một tác giả cộng tác tài liệu qua ví dụ sau:

```latex
\author[1]{author 1}
\author[2]{author 2}
\affil[1]{Author information 1}
\affil[2]{Author information 1}
```

<div align="center">
  <img src="./img abstract/img3.2.jpg">
</div>


