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
