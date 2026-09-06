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

Khoảng cách thụt lề đầu dòng của lệnh `\indent` mặc định là 20pt (? viết chưa được rõ cho lắm) 
