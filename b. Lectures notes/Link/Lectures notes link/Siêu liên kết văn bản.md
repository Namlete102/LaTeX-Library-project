Để sử dụng siêu liên kết văn bản, người dùng cần phải khai báo package đã nêu ở bài học **Liên kết thông thường** trong phần soạn thảo LaTeX.

Package `hyperref` sẽ đảm nhiệm việc chuyển các **tham chiếu** trong tài liệu thành siêu liên kết.

Các thiết lập mặc định của LaTeX thường phù hợp với hầu hết người dùng. Cụ thể, nếu người dùng chỉ cần khai báo package `hyperref` là xong, mà không cần các thiết lập nào nữa khác, thì LaTeX sẽ chỉ kích hoạt ứng dụng mặc định của gói đó là siêu liên kết các tham chiếu và hiển thị các khung $\color{red}{\text{màu đỏ}}$ đối với [mục lục]() hoặc cũng có thể là [chú thích](), 

<div align="center">
    <img src="./images link/img2.1.jpg" alt="khung màu đỏ (mục lục) khi siêu liên kết văn">
</div>

<center>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>.</center>

khung $\color{cyan}{\text{màu xanh dương}}$ đối với [liên kết thông thường](), 

<div align="center">
    <img src="./images link/img2.2.jpg" alt="khung màu xanh dương (mục lục) khi siêu liên kết văn">
</div>

<center>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>.</center>

và khung $\color{green}{\text{màu xanh lá}}$ đối với [tài liệu tham khảo](), 

<div align="center">
    <img src="./images link/img2.3.jpg" alt="Khung màu xanh lá">
</div>

<center>Ảnh lụm được ở <a href="https://tex.stackexchange.com/questions/528673/what-are-the-coloured-rectangles-in-research-papers">LaTeX Stack Exchange</a>.</center>

Các khung hiện <font color="red">màu đỏ</font>, <font color="lightblue">màu xanh dương</font>, <font color="lightgreen">màu xanh lá</font> như vậy chỉ có trong tài liệu lúc người dùng vẫn còn làm việc ở trong phần soạn thảo LaTeX, giúp người dùng dễ dàng điều hướng. Các khung đó sẽ không còn xuất hiện ở trang tài liệu của người dùng khi tải về đề in. 

<div align="center">
    <img src="./images link/img2.4.jpg" alt="Khung màu sẽ biến mất khi tải tệp">
</div>

<center>Ảnh lụm được ở . . . .</center>

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

<img src="./images link/img2.5.jpg" alt="file pdf">

</div>

<center>Ảnh lụm được ở . . . .</center>

. . . (còn nữa mà chưa soạn xem thêm dưới đây:  
https://en.wikibooks.org/wiki/LaTeX/Hyperlinks#Hyperlink_and_Hypertarget) 