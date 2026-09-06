**Lorem ipsum** là một [đoạn văn bản giả hoặc văn bản giữ chỗ](https://en.wikipedia.org/wiki/Placeholder_text "Văn bản giữ chỗ")  thường được sử dụng trong thiết kế đồ họa, xuất bản và phát triển web. 

Nó thường là một phiên bản bị thay đổi của _[De finibus bonorum et malorum](https://en.wikipedia.org/wiki/De_finibus_bonorum_et_malorum "De finibus bonorum et malorum")_, một văn bản thế kỷ thứ nhất Trước Công nguyên của chính khách và triết gia La Mã [Cicero](https://en.wikipedia.org/wiki/Cicero "Cicero") , với các từ bị thay đổi, thêm vào và loại bỏ để làm cho nó trở nên vô nghĩa và không đúng ngữ pháp tiếng Latinh. Hai từ đầu tiên là [dạng rút gọn](https://en.wikipedia.org/wiki/Clipping_\(morphology\) "Cắt tỉa (hình thái học)") của _dolorem ipsum_ ("chính là nỗi đau"). Mục đích của lorem ipsum là cho phép thiết kế bố cục trang, độc lập với nội dung văn bản sẽ được điền vào sau đó, hoặc để minh họa các phông chữ khác nhau của một kiểu chữ mà không có văn bản có ý nghĩa gây mất tập trung.[^1] (Dịch tạm là vậy)


<div align="center">
  <img src="./img lorem/lorem Ipsum.jpg" alt="lorem"> 
</div>

<center>Nguồn ảnh: <a href="https://priceonomics.com/the-history-of-lorem-ipsum/">https://priceonomics.com/the-history-of-lorem-ipsum/</a></center>

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

Lý do là bởi (? bởi vì sao . . . 1000:150 . . . lấy ở đoạn văn Lorem thứ 100)  

---
## Footnote 

[^1]: Nguồn copy: [https://en.wikipedia.org/wiki/Lorem_ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum)
