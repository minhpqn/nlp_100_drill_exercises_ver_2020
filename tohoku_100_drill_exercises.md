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

### 31. Động từ

Trích xuất tất cả các surface forms của động từ (pos=動詞).

### 32. Dạng nguyên thể của động từ (動詞の原形)

Trích xuất tất cả dạng nguyên thể của động từ (base form).

### 33.「AのB」

Trích xuất tất cả các danh từ ghép (compound nouns) gồm 2 danh từ kết nối bằng の.

### 34. Trích xuất các kết nối danh từ (noun connections hay 名詞の連接)

Trích xuất tất cả các noun connections (các danh từ đứng cạnh nhau liên tiếp). Khi trích xuất, chú ý trích xuất chuỗi danh từ matching dài nhất có thể. Ví dụ ABC trong đó A, B, C là danh từ thì phải trích xuất ABC thay vì AB.

### 35. Tần suất xuất hiện của từ

Lập trình tính tần suất xuất hiện của từ trong văn bản. Đưa ra các từ theo thứ tự giảm dần của tần suất xuất hiện.

### 36. Top 10 từ xuất hiện nhiều nhất

Vẽ đồ thị (ví dụ bar graph) của tần suất xuất hiện của 10 từ xuất hiện nhiều nhất trong văn bản.

### 37. Top 10 từ đồng xuất hiện với từ 猫

Vẽ đồ thị (ví dụ: bar plot) tần suất xuất hiện của top 10 từ đồng xuất hiện nhiều nhất với từ 猫.

### 38. Histogram

Vẽ đồ thị histogram tần suất xuất hiện của các từ. Trục ngang là tần suất xuất hiện. Trục dọc là các từ.

### 39. Luật Zipf

Vẽ đồ thị với trục ngang là rank của các từ theo tần suất xuất hiện (cao đến thấp), trục dọc là tần suất xuất hiện của các từ. Vẽ đồ thị [log-log](https://en.wikipedia.org/wiki/Log%E2%80%93log_plot) để thể hiện.

## Chương 5: Dependency parsing (係り受け解析)

Thực hiện phân tích cấu trúc ngữ pháp (dependency parsing) bằng công cụ
[CaboCha](<http://taku910.github.io/cabocha/>) cho file
[neko.txt](https://nlp100.github.io/data/neko.txt) và lưu kết
quả vào file neko.txt.cabocha. Sử dụng file kết quả này làm đầu vào cho các bài
tập dưới đây.

### 40. Đọc vào kết quả dependency parsing (theo morphemes)

Cài đặt lớp Morph cho các morphemes. Lớp này có các biến thành phần (member
variables) là surface (cho surface forms của morphems), base (cho base form),
pos (cho POS tag), pos1 (cho detailed POS tag - 品詞細分類). Sau đó đọc vào kết
quả phân tích dependency parsing trong file neko.txt.cabocha. Mỗi câu sẽ bao gồm
một danh sách các Morph objects. Hiển thị danh sách các morphemes cho câu thứ 3
trong văn bản.

### 41. Đọc vào kết quả dependency parsing (theo chunks và depedency relations)

Tiếp theo bài 40, cài đặt lớp Chunk để lưu trữ các chunk (hay bunsetsu (文節)).
Lớp này có các biến thành phần là:

- morphs (để lưu trữ danh sách các Morph
objects)
- dst để lưu trữ index của chunk mà chunk hiện tại trỏ đến (chunk đích - destination)
- srcs để lưu trữ danh sách các indexes của các chunk trỏ đến chunk hiện tại.

Sau đó, đọc vào kết quả dependency parsing. Mỗi câu sẽ bao gồm danh sách của các
Chunk objects. Hiển thị nội dung text và giá trị của biến dst của các chunk trong câu
thứ 8 của file đầu vào.

Các bài tập còn lại trong chương 5 sẽ sử dụng các chương trình được tạo ra ở đây.

### 42. Hiển thị chunk nguồn (head) và chunk đích (modifier) trong các depedency relations

Hiển thị nội dung dạng text các chunk nguồn (head) và chunk đích (modifier)
trên mỗi dòng và cách nhau bởi ký tự tab. Chú ý không hiển thị các dấu
(punctuation marks) trong các chunk.

### 43. Trích xuất các dependency relations giữa các chunk chứa danh từ và các chunk chứa động từ

Trích xuất các dependency relations giữa các chunk chứa danh từ và các chunk
chứa động từ và in ra nội dung text trên mỗi dùng và các thành phần cách nhau bởi dấu cách. Tương tự như bài 42, không hiển thị các
dấu (punctuation marks) trong các chunk.

### 44. Visualize cây dependency

Visualize cây phụ thuộc của câu đã cho dưới dạng biểu đồ có hướng. Để visualize, có thể chuyển đổi cây phụ thuộc sang ngôn ngữ DOT và sử dụng Graphviz. Thêm nữa, khi visualize một đồ thị có hướng trong Python, có thể sử dụng pydot.

### 45. Trích xuất case pattern của động từ

Yêu cầu của bài tập này là tìm hiểu (investigate) về case frame trong tiếng Nhật
sử dụng dữ liệu trong file đầu vào neko.txt. Coi các động từ là vị ngữ
(predicate), các trợ từ (như が,を,...) của chunk liên kết với với động từ là các case, hãy
in ra các vị ngữ và các "case" theo định dạng cách nhau bởi ký tự tab. Output
của chương trình cần thoả mãn các điều kiện sau: 

- Ở các chunk có chứa động từ, sử dụng dạng nguyên thể của động từ trái nhất làm vị ngữ.
- Coi các trợ từ liên kết với các vị ngữ là các "case" trong case frame. 
- Nếu một vị ngữ được liên kết bởi nhiều trợ từ (chunk), in tất cả các trợ từ theo thứ tự từ điển. Các trợ từ cách nhau bởi dấu cách

Xem xét ví dụ sau: 吾輩はここで始めて人間というものを見た (câu thứ 8 trong
file neko.txt.cabocha). Câu này gồm hai động từ 始める và 見る. Nếu trong kết
quả phân tích cú pháp, động từ 始める liên kết với chunk ここで, động từ 見る
liên kết với với chunk 吾輩は và ものを, chương trình sẽ in ra:

```
始める で
見る は を
```

Lưu output của chương trình ra file, xác nhận các mục sau chỉ với các lệnh của Unix.

- Kết hợp của các vị ngữ và case phổ biển trong corpus.
- Các case patterns của các động từ する, 見る, 与える (theo thứ tự từ cao đến thấp của tần suất xuất hiện trong corpus).

### 46. Trích xuất thông tin của case pattern của động từ

Chỉnh sửa bài tập 45, trích xuất thêm các chunks mà các vị ngữ (predicate) liên
kết tới. In ra theo định dạng tab. Ngoài các điều kiện đưa ra ở bài tập 45,
output phải thoả mãn các điều kiện sau.

- Các modifier là dãy các word của các chunk liên kết tới vị ngữ (không cần phải xoá đuôi và các trợ từ).
- Trong trường hợp một predicate liên kết với nhiều chunk (bunsetsu), in ra các chunk này theo thứ tự của các trợ từ trong các chunk. Dùng ký tự space để ngăn cách giữa các chunk.

Xem xét ví dụ sau: 吾輩はここで始めて人間というものを見た (câu thứ 8 trong
file neko.txt.cabocha). Câu này gồm hai động từ 始める và 見る. Nếu trong kết
quả phân tích cú pháp, động từ 始める liên kết với chunk ここで, động từ 見る
liên kết với với chunk 吾輩は và ものを, chương trình sẽ in ra:

```
始める  で      ここで
見る    は を   吾輩は ものを
```

### 47. Mining các cấu trúc câu có động từ chức năng

(cấu trúc này có tên tiếng Nhật là 機能動詞構文)

Bài tập này tập trung vào các case frame を của các động từ, trong đó động từ có dạng liên kết サ変接続名詞. Sửa chương trình trong bài tập 46 để thoả mãn các yêu cầu sau đây.

- Bài tập này tập trung vào các bunsetsu có dạng 「サ変接続名詞+を（助詞）」 liên kết với động từ. 
- Biến đổi các vị ngữ về dạng 「サ変接続名詞+を+動詞の基本形」. Nếu trong 1 chunk có nhiều động từ, sử dụng động từ bên trái nhất.
- Trong trường hợp một vĩ ngữ có liên kết với nhiều trợ từ (chunk), in tất cả các trợ từ này theo thứ tự từ điển. Các trợ từ cách nhau bởi dấu cách.
- Trong trường hợp có nhiều chunks liên kết với một vị ngữ (predicate), in tất cả các chunk này đồng nhất với thứ tự in của các trợ từ mà nó bao gồm. Các chunk được cách nhau bởi ký tự space.

Ví dụ, cho câu sau. 「別段くるにも及ばんさと、主人は手紙に返事をする。」. Chương trình sẽ in ra kết quả sau.

```
返事をする と に は 及ばんさと 手紙に 主人は
```

Lưu kết quả của chương trình ra file, chỉ sử dụng lệnh unix để xác nhận:

- Các vị ngữ thường gặp trong corpus (danh từ liên kết sahen + động từ)
- Các vị ngữ và các case patterns thường xuất hiện trong văn bản.

### 48. Trích xuất ra dependency path từ các danh từ đến gốc

Chương trình yêu cầu trích xuất ra depedency path từ các chunk có chứa danh từ đến root của cây depedency. Các dependency path phải thoả mãn yêu cầu sau đây.

- Biểu diễn các chunk (bunsetsu) dưới dạng chuỗi của các morpheme (surface form)
- Biểu diễn liên kết giữa các bunsetsu bằng ký tự mũi tên ```->```.

Ví dụ, đầu ra cho câu ví dụ 「吾輩はここで始めて人間というものを見た」(câu thứ 8 trong file neko.txt.cabocha) như sau:

```
吾輩は -> 見た
ここで -> 始めて -> 人間という -> ものを -> 見た
人間という -> ものを -> 見た
ものを -> 見た
```

### 49. Trích xuất ra chuỗi liên kết giữa các danh từ

Trích xuất dependency path ngắn nhất liên kết giữa các cặp noun chunk. Đối với cặp
noun chunk với index tương ứng là *i* và *j* (*i* \< *j*), các dependency paths
thoả mãn các yêu cầu sau.

- Giống như bài 48, biểu diễn liên kết giữa các
bunsetsu bằng ký tự mũi tên (-\>).
- Thay các noun chunk *i*, và *j* tương ứng
thành X và Y.

Thêm nữa, các dependency path trong bài tập này có thể được diễn dịch như sau.

- Trên đường đi của noun chunk *i* tới gốc của cây, nếu tồn tại noun chunk *j*: trích xuất dependency path giữa noun chunk *i* và noun chunk *j*.
- Ngoài trường hợp nói trên, nếu đường đi của noun chunk *i* và noun chunk *j* tới gốc của cây cắt nhau ở bunsetsu *k*: In ra đường đi từ *i* tới bunsetsu ngay trước *k* và
đường đi từ bunsetsu *j* tới bunsetsu ngay trước *k*. Biểu diễn liên kết với
bunsetsu *k* bằng ký tự \|.

Ví dụ, kết quả đưa ra cho câu ví dụ
「吾輩はここで始めて人間というものを見た」(câu thứ 8 trong file
neko.txt.cabocha) như sau:

```
Xは | Yで -> 始めて -> 人間という -> ものを | 見た
Xは | Yという -> ものを | 見た
Xは | Yを | 見た
Xで -> 始めて -> Y
Xで -> 始めて -> 人間という -> Yを
Xという -> Y
```


