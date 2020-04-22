100 bài luyện tập xử lý ngôn ngữ tự nhiên phiên bản 2020
========================================================

Dịch từ tài liệu [言語処理100本ノック 2020](<https://nlp100.github.io/ja>) của lab Inui-Okazaki, đại học Tohoku, Nhật Bản. Người dịch: Phạm Quang Nhật Minh
(minhpqn).

## Chương 1: Bài tập khởi động

### 00. Đảo ngược xâu ký tự

Đảo ngược xâu ký tự "stressed" (theo thứ tự từ cuối xâu đến đầu xâu ký tự).

### 01. "schooled"

Tạo một xâu kí tự bằng cách nối các kí tự ở vị trí 1, 3, 5, 7 trong xâu kí tự "schooled".

### 02. "shoe" + "cold" = "schooled"

Tạo xâu kí tự "schooled" bằng cách nối các kí tự trong "shoe" và "cold" luân phiên nhau từ đầu đến cuối.

### 03. Pi

Tách câu "Now I need a drink, alcoholic of course, after the heavy lectures involving quantum mechanics." thành các từ và 
tạo ra một danh sách (list) mà mỗi thành phần của nó biểu thị số các kí tự alphabet trong từ tương ứng.

### 04. Atomic symbols

Tách câu "Hi He Lied Because Boron Could Not Oxidize Fluorine. New Nations Might Also Sign Peace Security Clause. Arthur King Can." thành các từ
và trích xuất kí tự đầu tiên của các từ ở vị trí 1, 5, 6, 7, 8, 9, 15, 16, 19 và hai kí tự đầu tiên của các từ còn lại. Tạo một mảng kết hợp (đối tượng
dạng dictionary hoặc mapping) ánh xạ từ xâu được trích xuất tới vị trí (offset ở trong câu) của từ tương ứng.

### 05. n-gram

Viết hàm sinh ra tất cả các n-gram từ một dãy cho trước (xâu kí tự hoặc danh sách). Sử dụng hàm đã viết, sinh ra word bi-gram và character bi-gram từ câu "I am an NLPer"

### 06. Tập hợp

1.  Sinh ra tập X và Y tương ứng là tập các character bi-gram từ hai xâu ký tự
    "paraparaparadise" và "paragraph".
2.  Sinh ra các tập hợp union, intersection và difference của X và Y
3.  Kiểm tra xem bi-gram 'se' có thuộc tập X và Y hay không?

### 07. Sinh ra câu từ template

Viết hàm số nhận vào 3 biến x, y, z và trả về xâu ký tự "{y} vào lúc {x} giờ là {z}", trong đó {x}, {y} và {z} thể hiện giáo trị của x, y, z.
Sinh ra kết quả với các giá trị x, y, z sau đây x="12" y="Nhiệt độ" z=22.4

### 08. Xâu mật mã

Từ các ký tự của một xâu cho trước, cài đặt hàm có tên cipher để mã hoá xâu như
sau:

- Mọi ký tự tiếng Anh ở dạng thường (lower-case characters) c được chuyển
thành ký tự có mã là (219 - [mã ký tự ASCII của c]).
- Các ký tự khác giữ nguyên.

Sử dụng hàm đã viết để mã hoá và giải mã các xâu ký tự tiếng Anh.

### 09. [Typoglycemia](<https://en.wikipedia.org/wiki/Typoglycemia>)

Viết chương trình thực hiện việc sau:

- Nhận đầu vào là một câu tiếng Anh bao gồm các word ngăn cách nhau bằng ký tự
space. 
- Với mỗi word trong câu:
    * Nếu word đó không có nhiều hơn 4 kí tự, giữ nguyên word đó
    * Nếu không,
        + Giữ nguyên kí tự đầu và kí tự cuối của word
        + Đảo thứ tự một cách ngẫu nhiên các kí tự ở những vị trí khác (ở giữa của word đó).

Cho trước một câu tiếng Anh hợp lệ, ví dụ "I couldn't believe that I could actually understand what I
was reading : the phenomenal power of the human mind .", chạy chương trình đã
viết để đưa ra kết quả.
