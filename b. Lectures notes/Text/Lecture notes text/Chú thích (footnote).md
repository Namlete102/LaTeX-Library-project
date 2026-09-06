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

## Tài liệu tham khảo: 

\[1]: Nguồn tham khảo viết chú thích ở Overleaf: [https://www.overleaf.com/learn/latex/Footnotes](https://www.overleaf.com/learn/latex/Footnotes) 
