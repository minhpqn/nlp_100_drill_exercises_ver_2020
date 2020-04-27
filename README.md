<a class="mk-toclify" id="table-of-contents"></a>

# Table of Contents
- [Chương 1: Bài tập khởi động](#ch-ng-1-b-i-t-p-kh-i-ng)
- [Chương 2: Các lệnh cơ bản trên môi trường UNIX](#ch-ng-2-c-c-l-nh-c-b-n-tr-n-m-i-tr-ng-unix)
- [Chương 3: Biểu thức chính quy (Regular Expressions)](#ch-ng-3-bi-u-th-c-ch-nh-quy-regular-expressions)
- [Chương 4: Morphological Analysis trong tiếng Nhật (形態素解析)](#ch-ng-4-morphological-analysis-trong-ti-ng-nh-t)

100 bài luyện tập xử lý ngôn ngữ tự nhiên phiên bản 2020
========================================================

Dịch từ tài liệu [言語処理100本ノック 2020](<https://nlp100.github.io/ja>) của lab Inui-Okazaki, đại học Tohoku, Nhật Bản. Người dịch: Phạm Quang Nhật Minh
(minhpqn).

<a class="mk-toclify" id="ch-ng-1-b-i-t-p-kh-i-ng"></a>
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

<a class="mk-toclify" id="ch-ng-2-c-c-l-nh-c-b-n-tr-n-m-i-tr-ng-unix"></a>
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
nội dung giống gồm cột 1 và cột 2 trong file ban đầu và các cột cách nhau bởi ký tự tab. Sử dụng lệnh `paste` để thực hiện bài tập và xác nhận kết quả của chương trình bạn viết.

### 14. Trích xuất ra N hàng đầu tiên của file

Viết chương trình trích xuất ra *N* hàng đầu tiên của file. Biến số dòng lệnh là số tự nhiên *N*. Sử dụng lệnh `head` trong unix để thực hiện công việc.

### 15. Trích xuất ra N hàng cuối cùng của file

Viết chương trình trích xuất ra *N* hàng cuối cùng của file. Chương trình nhận đầu vào từ dòng lệnh là số tự nhiên *N*. Sử dụng lệnh `tail` trong unix để thực hiện công việc.

### 16. Chia file thành N phần

Nhận một số tự nhiên *N* từ đối số của dòng lệnh và chia file đầu vào thành *N* phần tại các ranh giới của các dòng (line boundaries). Xác nhận lại kết quả bằng lệnh `split` trong UNIX.

### 17. Các xâu phân biệt trong cột đầu tiên

Tìm các xâu phân biệt (một tập hợp các xâu) của cột đầu tiên của file. Xác nhận lại kết quả bằng cách dùng lệnh `cut`, `sort` và `uniq`.

### 18. Sắp xếp các dòng theo thứ tự tăng dần của cột thứ 3

Sắp xếp các dòng theo thứ tự tăng dần của các số trong cột thứ 3 (sắp xếp các dòng nhưng không thay đổi nội dung của trong mỗi dòng). Xác nhận lại kết quả với lệnh `sort`.

### 19. Sắp xếp theo tần suất xuất hiện

Đưa ra tần suất xuất hiện của các giá trị trong cột 1; sắp xếp các giá trị trong
cột 1 theo thứ tự từ cao đến thấp của tần suất xuất hiện.Xác nhận lại kết quả bằng việc dùng các lệnh `cut`,
`uniq`, `sort`.

<a class="mk-toclify" id="ch-ng-3-bi-u-th-c-ch-nh-quy-regular-expressions"></a>
## Chương 3: Biểu thức chính quy (Regular Expressions)

Tệp [enwiki-country.json.gz](https://nlp100.github.io/data/enwiki-country.json.gz) lưu trữ các bài viết Wikipedia ở định dạng:

- Mỗi dòng lưu trữ một bài viết Wikipedia ở định dạng JSON.
- Mỗi tài liệu JSON có các cặp khóa-giá trị:
    * Tiêu đề của bài viết là giá trị ứng với khóa "title".
    * Phần nội dung của bài viết là giá trị ứng với khóa "text".
- Toàn bộ tập tin được nén bởi gzip.

Viết mã thực hiện các công việc sau.

### 20. Đọc vào dữ liệu JSON

Đọc các tài liệu JSON, trích xuất và hiển thị nội dung của bài viết về United Kingdom. Sử dụng các nội dung của tài liệu được trích xuất này để thực hiện các nhiệm vụ trong các bài tập từ 21-29.

### 21. Trích xuất các dòng có chứa tên đề mục

Trong các tài liệu, trích xuất các dòng có chứa tên đề mục (category name).

### 22. Trích xuất các tên đề mục

Trích xuất tên đề mục của trong các tài liệu. Trong bài tập này, cần trích xuất
chính xác các tên đề mục chứ không phải dòng chứa tên đề mục.

### 23. Cấu trúc của các Section

Hiển thị tên của các section và level của các section trong các tài liệu
Wikipedia (Ví dụ với section == Section Name ==" thì level bằng 1)

### 24. Trích xuất các liên kết file

Trích xuất toàn bộ các liên kết đến các media files trong tài liệu.

### 25. Infobox

Trích xuất tên trường và giá trị của chúng trong Infobox "country" và lưu trữ chúng trong một đối tượng từ điển (dictionary).

### 26. Loại bỏ các emphasis markups

Trong khi làm các xử lý ở bài tập 25, xoá các MediaWiki emphasis markup (italic, bold,
both) trong giá trị của các trường và biến đổi thành plain text. Xem thêm tại [Help:Cheatsheet](https://en.wikipedia.org/wiki/Help:Cheatsheet).

### 27. Xóa bỏ các Internal Links

Bên cạnh những xử lý trong bài tập 26, hãy xóa những liên kết trong từ các giá trị của các trường. Xem thêm tại [Help:Cheatsheet](https://en.wikipedia.org/wiki/Help:Cheatsheet).

### 28. Xoá các markup trong văn bản

Ngoài các xử lý ở bài 27, hãy xoá các Media markup trong các giá trị của các trường ở Infobox càng nhiều càng tốt
và in ra các thông tin cơ bản về quốc gia ở dạng plaintext.

### 29. Lấy ra các URL của quốc kỳ

Lấy URL của quốc gia bằng cách sử dụng kết quả phân tích của Infobox. (Gợi ý: chuyển đổi tham chiếu file thành URL bằng cách gọi [imageinfo](<https://www.mediawiki.org/wiki/API:Imageinfo>) trong [MediaWiki API](https://www.mediawiki.org/wiki/API:Main_page))

<a class="mk-toclify" id="ch-ng-4-morphological-analysis-trong-ti-ng-nh-t"></a>
## Chương 4: Morphological Analysis trong tiếng Nhật (形態素解析)

Dùng [MeCab](http://taku910.github.io/mecab) để phân tích hình thái cho nội dung text của cuốn tiểu thuyết "Tôi là một con mèo" ([neko.txt](https://nlp100.github.io/data/neko.txt)) tác giả Soseki Natsume, và lưu kết quả vào file neko.txt.mecab. Sử dụng file kết quả để thực hiện các công việc ở các bài tập dưới đây.

Đối với các bài tập 37, 38, 39, có thể sử dụng các phần mềm
[matplitlib](<http://matplotlib.org/>) hoặc
[Gnuplot](<http://www.gnuplot.info/>).


### 30. Đọc vào kết quả morphological analysis

Viết chương trình đọc vào kết quả morphological analysis (file neko.txt.mecab).

Yêu cầu: Với mỗi morpheme, lưu các thông tin: 表層形 (surface form), 基本形
(base form), 品詞 (pos), 品詞細分類1 (pos1) bằng cấu trúc dữ liệu hash map với
các key tương ứng là: surface, base, pos, pos1. Lưu trữ mỗi câu bằng danh sách
của các morpheme. Trong các bài tập còn lại trong chương 4, hãy sử dụng cách tổ
chức dữ liệu trong bài này.