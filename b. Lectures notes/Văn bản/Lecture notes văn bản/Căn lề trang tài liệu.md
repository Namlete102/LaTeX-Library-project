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
