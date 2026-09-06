Đầu tiên người dùng cần phải khai báo package sau:

```latex
\usepackage{xcolor}
```

Package ở trên chỉ cho phép người dùng sử dụng được 19 màu cơ bản theo các tên màu đã được có sẵn mà không cần phải thêm bất kỳ `options` nào trong package như hình dưới đây.

![19 màu cơ bản](./img%20color%20text/img1.1.jpg)

Người dùng cũng có thể sử dụng thêm các màu ngoài 19 màu cơ bản trên theo ý muốn, cũng thông qua gói `xcolor` với các `options` như sau:

1. `dvipsnames`: tải 68 màu được đặt tên (CMYK)

```latex
\usepackage[dvipsnames]{xcolor}
```

![68  màu CMYK](./img%20color%20text/img1.2.jpg)

2. `x11names`: tải 317 màu được đặt tên (RGB)

```latex
\usepackage[x11names]{xcolor}
```

![317 màu RGB](./img%20color%20text/img1.3.jpg)

Để thay đổi màu sắc chữ người dùng sử dụng lệnh sau:

```latex
\textcolor{color}{text}
```

trong đó:

- `color`: là nơi nhập tên màu sắc cho văn bản mà người dùng muốn, với điều kiện là màu được chọn phải phù hợp với `options` mà người dùng khai báo theo những hình ở trên.
- `text`: từ hoặc văn bản bị thay đổi thành màu mà người dùng lựa chọn. 

--- 

## Tài liệu tham khảo: 

\[1]: Nguồn ảnh màu LaTeX: [https://tex.stackexchange.com/questions/659029/colour-packages-beyond-xcolor](https://tex.stackexchange.com/questions/659029/colour-packages-beyond-xcolor)