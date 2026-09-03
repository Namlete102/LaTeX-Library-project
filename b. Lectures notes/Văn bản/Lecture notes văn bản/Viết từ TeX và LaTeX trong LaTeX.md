
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