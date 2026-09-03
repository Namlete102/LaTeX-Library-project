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