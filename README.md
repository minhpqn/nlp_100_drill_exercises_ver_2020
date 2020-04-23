# Table of Contents
- [Chương 1: Bài tập khởi động](#ch-ng-1-b-i-t-p-kh-i-ng)
- [Chương 2: Các lệnh cơ bản trên môi trường UNIX](#ch-ng-2-c-c-l-nh-c-b-n-tr-n-m-i-tr-ng-unix)

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

## Chương 2: Các lệnh cơ bản trên môi trường UNIX

Tệp [popular-names.txt](https://nlp100.github.io/data/popular-names.txt) là một tệp ở định dạng phân cách bằng dấu tab, lưu trữ "tên", "giới tính", "số người" và "năm sinh" của các em bé được sinh ra ở Hoa Kỳ. Viết chương trình thực hiện các xử lý sau đây. Tệp [popular-names.txt](https://nlp100.github.io/data/popular-names.txt) là đầu vào của của chương trình. Sau đó, chỉ dùng cách lệnh trong UNIX để thực hiện cùng các nhiệm vụ và xác nhận xem kết quả các lệnh UNIX đưa ra có giống với kết quả của chương trình bạn viết hay không.

### 10. Đếm số dòng trong file

Đếm số dòng trong file. Xác nhận kết quả bằng lệnh wc trong unix.

### 11. Biến đổi các ký tự tab thành space

Chuyễn mỗi ký tự tab thành ký tự space. Xác nhận kết quả bằng các lệnh
`sed`, `tr` hoặc `expand`.

### 12. Lưu cột 1 vào file col1.txt, cột 2 vào file col2.txt

Trích xuất nội dung trong cột 1, cột 2 của các dòng trong file và lưu vào các file tương ứng: `col1.txt`
và `col2.txt`. Thử thực hiện công việc với lệnh `cut` trong unix.

### 13．Trộn hai file col1.txt và col2.txt

Kết hợp nội dung trong 2 file `col1.txt` và `col2.txt` đã được tạo ra trong bài 12 để tạo thành một file mới có
nội dung giống gồm cột 1 và cột 2 trong file ban đầu và các cột cách nhau bởi ký tự tab. Sử dụng lệnh paste để thực hiện bài tập và xác nhận kết quả của chương trình bạn viết.

### 14. Trích xuất ra N hàng đầu tiên của file

Viết chương trình trích xuất ra *N* hàng đầu tiên của file. Biến số dòng lệnh là số tự nhiên *N*. Sử dụng lệnh head trong unix để thực hiện công việc.