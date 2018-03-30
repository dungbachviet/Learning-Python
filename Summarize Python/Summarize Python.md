# TỔNG HỢP CÁC KIẾN THỨC VỀ PYTHON

### Ghi chú : 
- Tài liệu này mình sẽ khai thác chủ yếu từ trên Documentation tại trang chủ Python 3.6.3
- Đây sẽ là nguồn tài liệu tổng hợp, liệt kê các kiến thức hay tư tưởng được sử dụng trong ngôn ngữ Python, từ đó sẽ giúp người đọc dễ dàng trong việc tra cứu, tổng hợp kiến thức, tiện lợi hơn trong quá trình ôn thi cuối kỳ
- Có hai link sau bạn có thể tham khảo : 
  - Tutorial trên trang chủ Python : https://docs.python.org/3/tutorial/
  - Thư viện chuẩn và chính thức trên trang chủ Python : https://docs.python.org/3/library/index.html#library-index
  
  ==> Mỗi link sẽ có một ưu điềm riêng : Nếu như trang tutorial diễn giải các kiến thức từ cơ bản tới nâng cao từng khái niệm và tư tưởng, thì link thư viện chính thức sẽ là một nguồn tổng hợp các function, data structures,… giúp người học tiện tra cứu các hàm, hay các cấu trúc dữ liệu cần sử dụng
  
  - Cuối cùng là một trang hỏi đáp với những câu hỏi hay các thắc mắc với tần suất cao nhất sẽ được tổng hợp và trả lời ngay tại trang này : https://docs.python.org/3/faq/programming.html .Trong quá trình programming, chúng ta thường vướng phải rất nhiều các lỗi, bug, hay không biết được rằng tư tưởng của một ngôn ngữ khác khi được lập trình trên python thì sẽ được code như thế nào? Do đó, đây hứa hẹn sẽ một page vô cùng bổ ích, chúng ta hãy cùng nhau khai thác nó nhé!!!

## 1.	 Giới  thiệu khái quát về Python :
### 1.1.	Comment trong Python :
-	Trong Python, họ sử dụng ký hiệu ‘#’ trước dòng cần comment. Ký hiệu này sẽ có hiệu lực comment trong phạm vi một dòng. Trình thông dịch của Python sẽ không thông dịch dòng đó (vì nó nhận thấy có một ký hiệu comment ‘#’ ở phía trước dòng này)
-	Việc comment giúp cho mã nguồn trở nên rõ ràng và dễ hiểu đối với con người hay cụ thể với các lập trình viên. Giúp cho quá trình maintaining (bảo trì), hay upgrade (nâng cấp) phần mềm trở nên dễ dàng và đơn giản hơn bao giờ hết

### 1.2.	Numbers trong Python
-	Trong Python có các phép toán như : +, - , *, /, % như các ngôn ngữ lập trình thông thường. Trình thông dịch của Python khá thông minh trong việc đoán định kiểu dữ liệu của một số bất kỳ. Nó sẽ dựa vào đâu vậy? Nó sẽ dựa vào : dấu chấm động có nghĩa là : có hai kiểu dữ liệu quan trọng nhất đó là int và float, nếu trong số đó có dấu chấm động thì trình thông dịch sẽ tự hiểu số đó mang kiểu float và ngược lại, nếu không có dấu chấm động thì số đó hiển nhiên phải là kiểu int
-	Điều kỳ lạ trong phép chia / trong Python : Nếu như trong các ngôn ngữ khác, nếu sử dụng 2 hạng tử là 2 số nguyên trong phép chia này thì kết quả trả về phải được làm tròn theo kiểu integer phải không? Nhưng trong python, điều này không xảy ra, có nghĩa là : Nó sẽ trả về kết quả chính xác mà không hề làm tròn : 17/3 = 5.666666666666667. Còn tại đây nếu ta muốn làm tròn kết quả thì mình biết 2 cách : 
  - Cách 1 : Sử dụng int(17/3), ở đây nó giống như việc ép kiểu dữ liệu thông thường. Thử nghiệm : print(type(int(17/3)))  Output : <class 'int'>
  - Cách 2 : Sử dụng 17//3 = 5, ở đây chúng ta đã sử dụng 2 dấu ‘/’. Để kiểm tra ta thử in : print(type(17//3))  Output : <class 'int'>. Cũng đơn giản phải không nào???
-	Trong python tất nhiên cũng sẽ có bảng ưu tiên thứ tự thực hiện phép toán như các ngôn ngữ lập trình khác. Nhưng các bảng thứ tự ưu tiên phép toán này chỉ mang tính hình thức và ít ai có thể nhớ hết được, mà chỉ xem qua để hiểu. Vậy bằng cách nào họ có thể linh hoạt trong việc sử dụng các biểu thức toán học một cách đúng đắn khi mà họ không hề nhớ được thứ tự ưu tiên trong bảng quy tắc trên, ngay tại đây mình đang muốn nhắc đến: Sự kỳ diệu của dấu ngoặc đơn ( ). Với việc sử dụng dấu ngoặc đơn, chúng ta có thể linh hoạt và thoải mái để đưa các biểu thức quan trọng và cần phải được tính trước vào bên trong các ngoặc đơn này. Trình thông dịch sẽ hiểu được điều này, và sẽ thực hiện biểu thức với sự ưu tiên biểu thức trong ngoặc hơn cả. Nếu có nhiều ngoặc đơn, nó sẽ thực hiện các ngoặc đơn ở sâu nhất trước, và các ngoặc đơn từ trái qua phải.

-	Do Python sử dụng trình thông dịch, nên các biến khi được gán lần đầu tiên thì nó tự động lưu biến đó vào vùng nhớ (Các biến ban đầu không cần phải được khai báo trước. Điều này khá tiện và đơn giản). Nếu như một biến chưa được gán lần nào từ trước tới giờ ( có nghĩa là nó chưa được nằm trong bộ nhớ), thì nếu lập trình viên gọi biến đó ra, hiển nhiên trình thông dịch sẽ báo lỗi !!! Điều này là vô cùng dễ hiểu.

-	Ngoài các kiểu dữ liệu int hay float, trong Python còn sử dụng các kiểu dữ liệu 
+ Decimal (https://docs.python.org/3/library/decimal.html#decimal.Decimal ) 
+ Fraction (https://docs.python.org/3/library/fractions.html#fractions.Fraction )
+ Số thực : Complex Number (https://docs.python.org/3/library/stdtypes.html#typesnumeric )

-	Ngay sau đây, chúng ta sẽ cùng nhau khám phá một số hàm và phép toán cơ bản nhất áp dụng cho kiểu số trong Python : 

#### CÁC PHÉP TOÁN BOOLEAN : 

- Khác với C hay Java, Python không sử dụng các phép toán &&, || hay ! mà thay vào đó, nó sẽ sử dụng các phép toán ở dạng chữ : and, or, not. Có một điều cần phải chú ý : Kết quả của các phép toán này sẽ trả về : True, False (bắt buộc phải ghi hoa ký tự đầu). Nhân tiện bên trong mục này, mình muốn được đề cập luôn tới các phép so sánh trong Python : <, <=, >, >=, ==, !=, is (dùng với toán hạng là đối tượng object), is not (dùng với toán hạng là đối tượng object)

- Vậy thông thường chúng ta sử dụng các phép toán Boolean này trong những hoàn cảnh nào? Theo kinh nghiệm của mình ở các ngôn ngữ lập trình khác, mình thường xuyên sử dụng chúng trong các biểu thức điều kiện trong các if, while hay for,… Vậy bên trong biểu thức điều kiện, ngoài việc sử dụng các biểu thức dạng boolean theo kiểu True/False, thì ta có thể chỉ đặt một số thực, số nguyên bên trong biểu thức liệu trình thông dịch có thể hiểu được ko??? Đối với C/C++ thì if(5), if(-1), if(5==5) đều tương đương với if(true), còn if(0) được hiểu là if(false). Còn đối với Java, trình biên dịch của nó chặt chẽ hơn, nghĩa là nó không cho phép chỉ mình các số thực bên trong biểu thức điều kiện, mà bên trong biểu thức đó phải chỉ chứa các biểu thức Boolean, nếu không nó sẽ báo lỗi cú pháp. Còn đối với Python thì sao? Mình đã test thử và nhận thấy rằng : Python “rộng mở” và “dễ dãi” giống hệt C, tức nó cho phép các số thực, số nguyên đứng một mình trong các biểu thức điều kiện !

+ Có một điều ta để ý thấy : Đó là mọi kiểu dữ liệu trong Python từ int, float, … đều được hiểu là các class. Tức Python không có phân tách kiểu dữ liệu nguyên thủy hay trừu tượng như trong java mà nó coi tất cả mọi thứ đều là đối tượng. Có một điều khiến mình vẫn còn thắc mắc, đó là : ngoài các toán tử so sánh mà Python đã định nghĩa như mình đã liệt kê trên kia, mình phát hiện thấy : Họ còn định nghĩa cả các hàm như __ eq __ (self, object) (so sánh bằng), __ lt __ (selt, object) (so sánh kém),… Tại sao khi có những toán tử so sánh rồi mà còn phải mất công để xây dựng thêm những hàm như thế này để làm gì??? Mọi người có để ý thấy rằng : trong tham số truyền vào ở những hàm trên, nó có kiểu là object. Điều này là hiển nhiên, bởi vì mọi thứ trong Python đều được coi là một object. Mình đã làm một test sau : x = 10 sau đó print(x.__ eq __ (10)) ==> Output : true. Như vậy hàm thực hiện thành công! Chợt sau đó, mình tự hỏi : Nếu truyền vào một đối số có kiểu dữ liệu khác kiểu của biến đang cần được so sánh thì sao? Tức x = 10; y = 10.0; print(x. __ eq __ (y)) ==> Bạn thử đoán xem output sẽ trả về cái gì? Output : NotImplemented . Thật bất ngờ phải không? Dựa vào những dữ kiện này, dường như mình có thể tự suy diễn theo hướng sau : 

  - Thứ nhất, các hàm __ lt __ (gt, object) __, hay __ gt __ (self, object),.. đều là các hàm được xây dựng theo từng lớp. Lớp int hay lớp float đều có những hàm này. Nhưng mỗi hàm bên trong mỗi lớp sẽ được cài đặt theo những cách cụ thể và riêng biệt. Ví dụ : hàm __ lt __ (gt, object) __ trong class ‘int’ để chỉ so sánh nhỏ hơn với các số kiểu int, nên khi ta truyền vào đó một số kiểu ‘float’ thì nó sẽ báo : NotImplemented có nghĩa là cách thức để so sánh hai số int và float thì chưa được cài đặt (hay chưa được nạp chồng) bên trong class ‘int’. Còn class ‘float’ thì sao? Class này được cài đặt tốt hơn một chút, tức nó có khả năng so sánh được các số khác kiểu, tức so sánh một số float và một số int.

  ==> Như vậy, ta có thể chốt lại rằng : Các hàm trên là phụ thuộc theo từng lớp (theo từng cách các lớp có nạp chồng đầy đủ không???)

  - Thứ hai, khi chúng ta nhìn tham số được truyền vào trong các hàm trên, ta nhận thấy kiểu dữ liệu là object. Điều này khiến mình liên tưởng rất nhiều tới lớp object trong Java, lớp object là một lớp cha, lớp tổng của tất cả mọi lớp khác trong java. Nên có lẽ cũng giống với tư tưởng này, trong Python có thể cũng có một lớp kiểu như lớp Object này để khai báo hay chứa các phương thức so sánh cơ bản nhất như trên. Còn đối với từng lớp còn như lớp int hay lớp float, chúng có thể override các phương thức này từ lớp cha, hoặc nạp chồng gì đó. Sau này khi chúng ta xây dựng các class và muốn so sánh các đối tượng trong cùng một class hay các đối tượng ở các class khác nhau, khi đó ta cần thiết phải cài đặt các hàm hay phương thức cho việc định nghĩa việc so sánh các kiểu dữ liệu đó. Bởi vì, mỗi class sẽ được đặc trưng bởi dữ liệu riêng nên nó cần phải có sự cài đặt các phương thức riêng giúp chuyên biệt tính toán đối với bộ dữ liệu riêng này (đó là lý lại cho việc cần phải xây dựng hay định nghĩa lại các phương thức cho các toán tử tính toán. Chúng ta cũng có thể kế thừa phương thức nào đó từ các class cha, hoặc override (ghi đè), nạp chồng các phương thức giúp chúng trở nên linh hoạt, cụ thể và đa năng hơn) 

####	CÁC PHÉP TOÁN INT, FLOAT, COMPLEX
-	Mình vừa nhận ra một điều, đó là : các phương thức ép kiểu như int(5.0) hay float() hay complex() (ép kiểu cho số phức, ví dụ : print(complex(5,6))  Output sẽ là : (5+6j) (it is so interesting, isn’t it?). Nguồn gốc chức năng ban đầu của nó không phải là để ép kiểu, mà đó là các phương thức constructor của các class (như int, float, complex,…). Như vậy, khi ta khai báo : x = int(5) có nghĩa rằng ta tạo ra một đối tượng của lớp ‘int’, nhưng vì do x = int(5.0) cũng tạo ra một đối tượng cho lớp ‘int’ (do trong phương thức constructor của lớp int đã tính toán và phòng ngừa những tình huống như thế này nên họ đã có thêm những đoạn code xử lý giúp chuyển về kiểu int). Chính vì những công dụng này, nên chúng ta thường sử dụng luôn các constructor làm hàm ép kiểu !!! (Một công giúp tiện lợi đôi việc -_-)

-	Các phép toán : Ngoài các phép toán cơ bản như : + - * / %. Mình xin trình bày thêm một vài phép toán khác : 
  - ‘//’ phép toán chia lấy phần nguyên (làm tròn về số nguyên lớn nhất nhưng nhỏ hơn giá trị gốc tức phần floor)
  - ‘-x’ : tức đảo ngược dấu của một số 
  - abs(x) : Đây là hàm tìm giá trị tuyệt đối của một số
  - int(x), float(x), complex(real, imagine) : Đều là các hàm ép kiểu như mình đã trình bày phía trên
  - divmod(x, y) : Sẽ trả về một bộ (tuple) dạng (div_result, mod_result) chứa đồng thời phần thương (dạng int) và phần dư của phép chia. Cách sử dụng nó thực sự rất linh hoạt, mình đã thử test : 
  
	```python
	x = 17 
	y = 3
	a,b = divmod(x, y)# hứng dữ liệu bằng a,b
	(c,d) = divmod(x,y)# hứng dữ liệu bằng tuple
	[e, f] = divmod(x,y)# hứng dữ liệu bằng list
	k = divmod(x,y)# hứng dữ liệu bằng biến k
	print(divmod(x, y))
	print(a,b)// 5 2
	print(c,d)// 5 2
	print(e, f) // 5 2
	print(k) // (5 2) tức k vẫn là tuple
	print(k[0], k[1]) // 5 2
	```

  ==> Ví dụ trên có thể được giải thích như sau : Mặc dù hàm divmod(x,y) trả về dạng tuple. Nhưng cũng sẽ tùy thuộc vào kiểu hay cấu trúc của biến hứng dữ liệu mà trình thông dịch sẽ hiểu và ghép khớp dữ liệu cho từng biến nhận một cách phù hợp và đúng đắn
  
  - Hàm pow(x,y) hoặc x**y : đều có ý nghĩa x lũy thừa y (x^y)
  
  - Trong Python có một thư viện dành riêng cho các công thức toán học: Đó là thư viện math, để sử dụng được thư viện này ta chỉ cần thêm dòng code sau ở những dòng đầu của mã nguồn giúp import thư viện đó vào chương trình của chúng ta :  import math .Trong thư viện này có rất nhiều hàm bổ ích (bạn gõ math. rồi Ctrl + space để xem cụ thể tất cả các hàm mà thư viện này hỗ trợ), chẳng hạn : sin(), cos(), exp(), log(), fabs(), floor(), ceil()… và rất nhiều !
  
  - Hàm math.trunc(x) : với x là số thực, hàm giúp loại bỏ phần thập phân và đưa về kiểu số nguyên (tức nó ép kiểu luôn, đã test thử bằng hàm type())
  
  - Hàm round(x[,n]) : x là một số thực, n là một giá trị tùy chọn chỉ định số chữ số thập phân bên trong số thực x (nếu không có n, thì giá trị x sẽ được làm tròn theo cách hiểu : 5.45 bị làm tròn xuống 5.0, còn 5.55 hay 5.5 được làm tròn lên 6)
  
  - Hàm type(x), x có thể là một biến, một số, một list,…Hàm này vô cùng quan trọng bởi vì nó giúp ta kiểm tra được kiểu dữ liệu thực sự của một biến

####	CÁC PHÉP TOÁN VỚI BIT

+ Đối với các thao tác trên bit, chúng ta có một vài các toán tử thao tác cơ bản, như :& (and bit), | (or bit), ^ (xor bit), << (dịch trái), >> (dịch phải), ~ (not bit)
+ Có một sự lưu ý : Dịch trái bit cho một số tương đương với hành động nhân số đó với pow(2,n) (tức 2^n) (với không kiểm tra overflow). Dịch phải n bit cho một số tương đương với việc chia số đó cho pow(2,n) (với không kiểm tra overflow) 
+ Class ‘int’ cũng hỗ trợ rất nhiều các phương thức xử lý bit : ví dụ int.bit_length() tức trả về số bit của của một số nguyên nào đó 

```python
x = -37
print(bin(-37))# -0b100101, trả về dạng bit
print(x.bit_length()) # 6, trả về số bit
```

## 1.3.	Các kiểu dữ liệu lưu trữ chuỗi nhiều phần tử
### 1.3.1.	Các phương thức chung xử lý chuỗi các phần tử
*Ghi chú các ký hiệu sẽ được sử dụng phía dưới đây : s, t là các chuỗi các phần tử có cùng kiểu dữ liệu; n, i, j, k là các số nguyên; x là một đối tượng (mọi thứ trong Python đều là các đối tượng, nên chúng ta cũng không cần lo lắng hay băn khoăn về x)*

-	x in s : Kiểm tra một đối tượng (phần tử) có thuộc vào danh sách s không? Trả về True nếu nó có mặt trong s, trả về False nếu x không có mặt trong s
Ví dụ : 
```python
s = [1, 2, 3, 4, 5]
x = 1
y = 100
print(x in s)# True
print(y in s)# False
```

-	x not in s : Ngược lại với biểu thức phía trên. Nếu không tìm thấy sẽ trả về True, ngược lại nếu tìm thấy sẽ trả False
-	s + t : Nối danh sách s với danh sách t và trả về một danh sách mới được nối từ 2 danh sách trên
Ví dụ : 
```python
s = [1, 2, 3, 4, 5]
t = [6, 7]
z = s + t
print(z)# [1, 2, 3, 4, 5, 6, 7]
```
hoặc
```python
s = (1, 2, 3, 4, 5)
t = (6, 7)
z = s + t
print(z) # (1, 2, 3, 4, 5, 6, 7)
```

-	s * n hoặc n * s : Tạo ra n bản copy của danh sách s.
-	s[i] : Trả lại phần tử tại index i của danh sách
-	s[i:j] : Trả lại danh sách từ phần tử s[i] đến phần tử s[j-1] (tức không tính tới j) được trích từ danh sách ban đầu s.
-	s[i:j:k] : Biểu thức này cũng tương tự như biểu thức trên, nhưng ở đây có thêm giá trị k. Vậy k để làm gì? Bình thường s[i:j] sẽ trả lại danh sách các phần tử cách đều nhau 1 index. Như vậy, để linh hoạt khi muốn trả lại danh sách mà cách nhau k index thì cần phải sử dụng thêm tham số k này!
-	len(s) : Trả lại độ dài của danh sách s
Ví dụ : 
```python
s = (1, 2, 3, 4, 5)
print(len(s))# 5, số phần tử bên trong danh sách(tuple)
```
-	min(s), max(s) : Trả lại lần lượt phần tử nhỏ nhất và lớn nhất trong danh sách s
-	s.index(x[, i[, j]]) : Trả về index của phần tử trùng đầu tiên trong danh sách xét từ index i đến index j. Nếu không có j thì nó sẽ so khớp từ index i đến index cuối cùng của danh sách. Nếu không có cả i và j thì nó sẽ so khớp toàn bộ các phần tử trong danh sách. Có một điểm cần lưu ý : Nếu tìm thấy thì nó sẽ trả về index cần tìm. Còn nếu không tìm thấy thì nó sẽ xuất ra lỗi không tìm thấy phần tử trong danh sách ra màn hình. Như vậy, khi xuất hiện lỗi khiến cho những lệnh phía sau không thể được hiện tiếp được. Vì vậy ta cần phải có một giải pháp phòng tránh lỗi? Trước khi lấy index trong một danh sách ta cần phải kiểm tra trước phần tử đó có thực sự tồn tại bên trong danh sách này không bằng cách : if(x in s), nếu trả về True thì mới tiến hành tìm index. Tại thời điểm hiện tại mình cũng chưa biết là có cách nào để bắt được ngoại lệ hay ko??? (Ghi chú : các dấu ngoặc vuông ở đây mang ý nghĩa rằng : sự xuất hiện của các biểu thức ngoặc vuông là tùy chọn (tức có thể không có)) 

Ví dụ : 
```python
s = (1, 2, 3, 4, 5)
print(s.index(3))# 2, trả về index của phần tử khớp
```
hoặc 
```python
s = (1, 2, 3, 4, 5)
print(s.index(100))
ValueError: tuple.index(x): x not in tuple
```

-	s.count(x) : Đếm tổng số lần xuất hiện của phần tử có giá trị x bên trong danh sách s

####	MỘT SỐ SỰ PHÂN TÍCH VỀ CÁC PHƯƠNG THỨC/BIỂU THỨC:
-	Ví dụ 1 :
```python
print("gg" in "ggabc")# True
```
-	Ví dụ 2 : Giải thích ví dụ sau 
```python
lists = [[]] * 3
print(lists)# [[], [], []]
lists[0].append(3)
print(lists)# [[3], [3], [3]]
```

- Nhìn vào ví dụ trên, ta nhận thấy khi thực hiện append một phần tử vào lists[0] thì khiến cho các lists[1], lists[2] cũng bị append theo. Tại sao lại như vậy? Điều này, thật mất tự nhiên và gây khó chịu đối với Lập trình viên. Hiện tượng trên có thể được giải thích như sau : 
  + Ta sẽ bắt đầu đi từ [[]] có ý nghĩa gì : cặp ngoăc vuông bên trong cùng là một list rỗng không chứa bất kỳ một phần tử nào cả (tức nếu ta gọi  phần tử index = 0 của nó, trình thông dịch sẽ báo lỗi ngay lập tức. Điều này chứng minh được cặp ngoặc vuông bên trong cùng là một list rỗng thực sự). Vậy còn cặp ngoặc vuông bao bọc ngoài cùng có ý nghĩa gì? Nó cũng là một list và bên trong nó chỉ có một phần tử duy nhất, đó chính là phần từ list rỗng đã phân tích ở trên (Test thử : Tại cặp ngoặc vuông ngoài cùng này, nếu ta gọi tới phần tử có index = 0 thì nó sẽ trả lại phần tử list rỗng [ ])
  
  +[[]] * 3  Vậy biểu thức này tiếp tục mang ý nghĩa gì? Phép nhân thực hiện quá trình nhân bản 3 lần cặp ngoặc vuông CON (bên trong cặp ngoặc vuông cha). Nghĩa là sau khi nhân nó sẽ có dạng :  [[ ], [ ], [ ] ]. Nhưng có điều đặc biệt ở đây, người ta nó rằng nếu có phép nhân ở đằng sau một list thì nó sẽ nhân bản để tạo ra 3 tham chiếu (chứ không phải ba bản sao phân biệt). 3 tham chiếu này cũng giống như 3 con trỏ, nó cùng trỏ tới cùng 1 đối tượng gốc trong bộ nhớ, nếu một tham chiếu tiến hành thay đổi cùng nhớ thì các tham chiếu khác cũng sẽ bị ảnh hưởng (bởi vì vùng nhớ cả 3 tham chiếu trỏ đến là vùng nhớ CHUNG của cả ba). Ở đây, lists[0], lists[1], lists[2] là 3 tham chiếu cùng trỏ tới 1 vùng nhớ (đối tượng). Nên khi bất kỳ một trong 3 tham chiếu này thực hiện .append(3) thì khiến cho các ngoặc vuông con (các list con) còn lại đều bị ảnh hưởng. Như vậy, chúng ta đã có thể hiểu được bản chất của đoạn code trên !!! Còn giải pháp giúp tạo một danh sách chứa các phần tử độc lập mình sẽ trình bày trong các ví dụ tiếp theo
  
  + Có một điều sau mình muốn được mở rộng thêm : Khi tạo dựng một danh sách, cụ thể là một list. Nếu chúng ta muốn chèn thêm vào list một phần tử thì cần phải làm như thế nào? Nguyên nhân bởi vì list hiện tại mới được khởi tạo, chưa hề có bất kỳ phần tử nào, nên việc gọi s[0] = 100 thì sẽ bị báo lỗi bởi vì index = 0 cũng chưa hề được tồn tại. Vậy làm sao để nói cho trình thông dịch hiều được rằng : chúng ta đang muốn chèn thêm một phần tử vào cuối danh sách. Giải pháp : Hãy sử dụng hàm append() để chèn một phần tử vào cuối danh sách. Vậy khi muốn chèn một phần tử vào đầu danh sách thì sao? Tức mọi lúc đều phải chèn vào đầu danh sách, kể cả từ lúc list ban đầu còn chưa có bất kỳ một phần tử nào cả??? Liệu có hàm đó không? Tất nhiên sẽ có, đó là phương thức insert(0,value) của đối tượng list. Ở đây, tham số đầu tiên là vị trí index cần chèn, còn value là giá trị cần chèn vào. Do ta luôn muốn chèn vào đầu của danh sách nên ta đặt index cần chèn = 0. (Do you have any questions?)
  
-	Ví dụ 3 :
```python
lists = [[] for i in range(3)]
print(lists)# [[], [], []]
lists[0].append(3)
lists[1].append(5)
lists[2].append(7)
print(lists)# [[3], [5], [7]]
```
  + Từ ví dụ trên chúng ta có thể rút ra một cách để tạo ra một danh sách (list) mà các list con bên trong nó đều độc lập với nhau (tức mỗi list để trỏ tới một đối tượng (hay vùng nhớ) riêng biệt). Tại sao trong ví dụ này lại có thể làm được điều đó??? Hãy để ý và tỉnh táo để nhận thấy rằng ở trong ví dụ này họ không sử dụng phép nhân *, bởi vì phép * chính là căn nguyên nguồn gốc tạo ra các tham chiếu cùng trỏ tới một đối tượng. Khi không sử dụng phép nhân nữa thì mọi thứ sẽ trở nên bình thường và độc lập. Còn đây là một cách khá hay và khá lạ trong việc xây dựng list : [[] for i in range(3)] . Ở đây họ sử dụng hàm range(3) để tạo ra một list [0, 1, 2], vòng for sẽ có tác dụng duyệt qua từng phần tử trong range, nhưng ở đây nó không quan tâm tới giá trị của các phần tử trong range, mà nó chỉ quan tâm tới số lần duyệt tới hết các phần tử bên trong list. Do có 3 phần tử nên vòng for cần duyệt 3 lần, mỗi lần duyệt bạn có để ý thấy rằng nó sẽ tạo ra một list con [ ], sau ba lần thì nó sẽ tạo ra 3 list con [ ], [ ], [ ]. Nhưng 3 list con này sẽ nằm ở bên trong cái gì? Tất nhiên là nó phải có một cái gì đó để đựng, thứ để đựng 3 list con chính là list cha. Điều này giải thích tại sao lại có một list cha ngoài cùng bao bọc cả mẩu code chứa vòng for. Như vậy, tới đây chúng ta đã có thể hiểu được cách sinh ra một list cha có sức chứa nhiều list con !!!
  
  + Tiếp theo đó, chỉ đơn giản là các phương thức append() của từng đối tượng list con, giúp chèn một phần tử vào cuối các list con đó (Còn nếu chúng ta muốn chèn vào đầu list con, thì hãy lưu tâm tới phương thức insert(index, value) với index đặt bằng 0 nhé!)  

-	Ví dụ 4 : Một cách giúp tạo list chứa nhiều phần tử con độc lập : 

```python
A = [None] * 3
print(A)# [None, None, None]

for i in range(3):
    A[i] = [None] * 2
print(A)# [[None, None], [None, None], [None, None]]

```

  + Tại sao ví dụ này, họ cũng sử dụng phép nhân nhưng họ vẫn tạo ra được một mảng chứa các list con độc lập. Chúng ta hãy cùng nhau phân tích để tìm ra nguyên nhân nhé ! Đầu tiên, từ [None] * 3 , họ đang làm gì vậy? Tương tự ví dụ trên, họ đang nhân bản 3 lần phần tử con None. Sau khi nhân bản, ta thu được [None, None, None] . Lúc này, mình có cảm thấy e dè không khi mà nếu các None này có thể tham chiếu tới nhau??? Và None này là gì vậy? Trước tiên mình xin được trả lời rằng, None cũng là một giá trị nhưng không có giá trị, nó gần giống với Null trong ngôn ngữ lập trình Java, C. Vậy None bên trong list trên dùng để làm gì? Hiểu một cách quan thì None giống như một vật “không có giá trị”, nhưng nó vẫn là một vật, vẫn tồn tại trên thế gian này. Vì thế, khi ta truy cập vào list trên tại các index = 0 hay 1 hay 2 thì nó đều truy xuất được và trả về None. Việc sử dụng [None] ưu điểm hơn khi chỉ sử dụng [ ] là ở chỗ : None là tồn tại nên ta có thể truy xuất được vào phần tử 0, còn list [ ] chẳng có gì cả vì thế khi truy xuất vào index 0 trình thông dịch sẽ báo lỗi. Vậy có thể để các None tham chiếu tới cùng một object không? Tất nhiên là không, bởi vì None không phải là đối tượng, chỉ là một giá trị “thô” bình thường (giống như kiểu dữ liệu nguyên thủy trong Java vậy). Do vậy mà các None này sau khi nhân bản sẽ độc lập hoàn toàn với nhau!!! (Còn list là đối tượng nên mới có khả năng tham chiếu, vì vậy sau khi bị nhân bản thì các list con mới cùng trỏ tới 1 vùng nhớ)
  
  + Tiếp theo đó, tác giả sử dụng một vòng for, vòng for này sẽ có tác dụng để thay thế mỗi None thành [None] * 2 tức [None, None]. Như vậy sau vòng for này chúng ta sẽ thu được : [[None, None], [None, None], [None, None]] . Mình xin nói thêm, do ở đây sử dụng None nên chúng ta mới có thể truy cập được vào index như : A[i]  .Còn nếu sử dụng các list rỗng thì chắc chỉ còn cách sử dụng phương thức append() hay insert() gì đó!!!


-	Ví dụ 5 : Một cách khác tạo mảng chứa các list con độc lập nhưng ngắn gọn và xúc tích hơn nhiều : 

```python
w, h = 2, 3
A = [[None] * w for i in range(h)]
print(A)# [[None, None], [None, None], [None, None]]
```

  + Với sự phân tích từ những ví dụ trên, mình nghĩa tại đây chúng ta có thể dễ dàng suy luận một cách tương tự nhé! Mình chỉ note thêm một chút ở dòng đầu tiên khi tác giả sử dụng phép gán đồng thời cho cả 2 biến w = 2 và h = 3. Đây chính là tiện tính năng có trong Python, chúng ta nên ghi nhớ và sử dụng linh hoạt nó!( Ứng dụng nó trong các phép hoán đổi giá trị nhanh chóng hơn nhiều so với hàm swap trong C hay Java)

### 1.3.2.	Các phương thức dùng cho các danh sách có tính mutable (tức có khả năng update, thêm, xóa … như kiểu list) (Còn tuple thì ngược lại, nó không cho phép update, thêm, xóa; mà chỉ được đọc và truy xuất. Giá trị của tuple chỉ được khởi tạo duy nhất ở lần đầu tiên)

+ s[i:j] = t : thay thế đoạn danh sách chứa các phần tử có chỉ số từ i tới (j-1) bởi một danh sách khác t
Ví dụ :
```python 
l = [1,2,3,4,5]
l[0:2] = [10, 11, 12, 13, 14]
print(l)# [10, 11, 12, 13, 14, 3, 4, 5]
```
 
+ s[i:j:k] = t : Gán những phần tử từ list t vào những vị trí (cách đều k tương ứng) trong mảng s

+ del s[i:j] : Giống với cách s[i:j] = [ ], tức xóa các phần tử trong danh sách có chỉ số từ i đến (j-1). Chú ý đối với việc xóa một phần tử trong list, ví dụ muốn xóa phần tử có index = 1 ta cần làm như sau s[1:2]=[] (còn nếu làm theo kiểu s[1]=[] thì đây không là thao tác xóa mà là thao tác thay phần tử này bởi list rỗng []), còn nếu sử dụng cách xóa bằng del thì có thể del s[i] hoặc del s[i:j] hoặc del s[i:j:k] đều được !!!
Ví dụ : 
```python 
l = [1,2,3,4,5]
del l[0:2] # hoặc sử dụng l[0:2] = []
print(l)# [3, 4, 5]
```
+ del s[i:j:k] : Một công thức linh hoạt hơn công thức trên có sử dụng thêm bước nhảy k để tùy chọn các phần tử cách nhau những quãng đều với độ dài quãng bằng k

+ s.append(x) : Chèn x vào cuối list. Đã trình bày nhiều ở phía trên!

+ s.clear() : Xóa tất cả các phần tử bên trong danh sách s. Giống với thao tác del s[:], hay s[:] = [ ]

+ s.copy() : Tạo ra một bản sao của danh sách s. Bản sao này với bản gốc là phân biệt và độc lập, tức trỏ tới các đối tượng hay vùng nhớ khác nhau, chỉ là chúng có cùng giống nhau các giá trị bên trong danh sách. Nhưng ở đây mình chợt nhận ra một vấn đề tương tự như trong C hay Java, đó là hiện tượng “copy nông” (copy không sâu). Hiện tượng này được lý giải như sau : Bình thường danh sách bản chất chính là đối tượng, nếu như bên trong đối tượng này chỉ toàn chứa các phần tử nguyên thủy thì hành động copy này sẽ tạo một các danh sách mới (bản sao) hoàn toàn độc lập (tức thay đổi phần tử con bên trong danh sách này không hề ảnh hưởng tới các phần tử con bên trong danh sách còn lại). Vậy vấn đề ở đây là gì? Đó là : Nếu như bên trong list cần copy, có một phần tử con nào đó lại là một danh sách (tức cũng là một đối tượng) thì sao??? Lúc này hành động nhân bản các phần tử con sẽ vô hình chung nhân bản luôn để tạo ra 2 tham chiếu của list con cùng trỏ tới 1 cùng nhớ. Nó giống với vấn đề khi copy đối tượng của lớp, nhưng bên trong lớp đó có tồn tại dữ liệu riêng cũng là một kiểu đối tượng (hay con trỏ). Đây gọi là hiện tượng copy nông? Trong java đã có những phương thức giúp copy sâu, tức đi vào sâu nhất có thể của list, tới khi gặp được các phần tử không còn là một đối tượng mà là các “phần tử nguyên thủy”.
  + Ví dụ của copy nông gây ra sai sót khiến thay đổi hàng loạt như sau : 

  ```python
  l = [[1, 2]]
  k = l.copy()
  print(l,k)# [[1, 2]] [[1, 2]]
  l[0][0] = 100 # [[100, 2]] [[100, 2]]
  print(l,k)
  ```

+ s.extend(t) hoặc s += t : Giúp mở rộng danh sách s với toàn bộ nội dung của danh sách t. Biểu thức này cũng tương đương với : s[len(s):len(s)] = t. Mình đã test thử và kết quả thành công như mong muốn!
Ví dụ : 
```python
s = [1,2,3]
# s.extend([4, 5])
# s += [4, 5]
s[len(s):len(s)] = [4, 5]
print(s)# [1, 2, 3, 4, 5]
```

+ s *= n : Nhân bản s lên n lần rồi chèn vào cuối bản thân s
Ví dụ :
```python
l = [1,2,3]
l *= 2
print(l)# [1, 2, 3, 1, 2, 3]
```

-	s.pop([i]) : Trả về giá trị của phần tử ở vị trí index = i, sau đó xóa luôn phần tử này ra khỏi danh sách

-	s.remove(x) : Xóa phần tử đầu tiên trong danh sách mà khớp với x

-	s.reverse() : Đảo ngược tất cả các phần tử bên trong danh sách s

Ví dụ : 
```python
s = [1,2,3]
s.reverse()
print(s)# [3, 2, 1]
```

### 1.3.3.	List trong Python : 
- List là một kiểu danh sách mutable (có thể cập nhật và thay đổi) trong Python. Nó được dùng để lưu các phần tử đồng nhất (có cùng kiểu dữ liệu))
- List là một class trong Python. Mỗi đối tượng của list có thể được khởi tạo theo những cách sau : 
  - Sử dụng ngoặc vuông rỗng : [ ] để khởi tạo list rỗng
  
  - [a, b, c] khởi tạo list chứa các phần tử. Các phần tử này được cách nhau bởi dấu phẩy
  
  - Sử dụng List Comprehension để khởi tạo list : [f(x) for x in iterable], trong đó iterable như là một danh sách, vòng for sẽ lấy từng phần tử bên trong danh sách đó, còn f(x) có nghĩa là một công thức bất kỳ : ví dụ 2*x + 3, thì với mỗi x có được, nó sẽ tính toán dựa trên công thức này. Thu được kết quả và đưa dần vào list!
  
  - sử dụng constructor : list() hoặc list(iterable). Hàm này cũng được như dụng như một hàm ép kiểu về dạng list. 
  Ví dụ : 
```python
	print(list([1,2,3]))# [1, 2, 3]
	print(list((1,2,3)))# [1, 2, 3]
	print(list('abc')) # ['a', 'b', 'c']
```

### 1.3.4.	Tuples 
- Là một kiểu danh sách có tính chất immutable (tức không phép cập nhật các phần tử, chỉ có thể đọc và truy xuất các phần tử)
- Là một class trong Python với các cách khởi tạo như sau : 
  + Sử dụng ( ) để khởi tạo một tuple rỗng
  + (a, ) để khởi tạo tuple có 1 phần tử duy nhất. Tại sao lại cần dấu phẩy? Bởi vì để trình thông dịch tránh nhầm lẫn với 1 biểu thức trong ngoặc như (5) chẳng hạn
  + (a, b, c) : Khi tuple có nhiều phần tử thì các phần tử phải cách nhau bởi dấu phẩy
  + Sử dụng các hàm contructor để khởi tạo như tuple() hay tuple(iterable)
  
Ví dụ : 
```python
print(tuple("abc"))# ('a', 'b', 'c')
print(tuple([1,2,3]))# (1, 2, 3)
print(tuple((1,2,3)))# (1, 2, 3)
```

==> Từ bài này, ta có thể tham khảo thêm kiến thức về enumerate tại link này : https://docs.python.org/3/library/functions.html#enumerate. Từ đó hiểu thêm về enumerate và hàm field (hàm này chỉ được sử dụng bên trong một function, nếu đặt bên ngoài một function trình thông dịch sẽ báo lỗi. Hàm này để tạo ra các dạng (key, value) thì phải???)

### 1.3.5.	Range
- Sử dụng để tạo ra một chuỗi các số, chuỗi này có tính chất immutable (tức có thể cập nhật các phần tử). Nó được sử dụng phổ biến trong các vòng lặp for trong việc duyệt các phần tử
- Đây là một class. Nó được thể hiện ở hai dạng chính : 
  + range(stop) : Tạo ra một danh sách chứa các số từ 0 tới (stop-1)
  + range(start, stop[, step]) : Tạo ra một danh sách các số từ start tới (stop-1). Còn step để cho biết bước nhảy- khoảng cách giữa các index của phần tử trong danh sách
  
Ví dụ :
```python
print(list(range(10)))# [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(list(range(0, 30, 5)))# [0, 5, 10, 15, 20, 25]
print(list(range(0, 10, 3)))# [0, 3, 6, 9]
print(list(range(0, -10, -1)))# [0, -1, -2, -3, -4, -5, -6, -7, -8, -9]
print(list(range(0)))# []
print(list(range(1, 0)))# []
```

Ngoài ra có một ví dụ này khá hay về range :

```python
r = range(10) 
print(r[:5])# range(0, 5)
print(list(r[:5]))# [0, 1, 2, 3, 4]
print(r.index(1))# 1
print(r[9])# 9
print(r[-1])# 9, kỳ diệu khi cũng trả về phần tử cuối cùng
```

### 1.3.6.	String trong Python : (Tìm hiểu sau)
### 1.3.7.	Set trong Python
- Đối tượng set là một tập hợp các đối tượng phân biệt và không có thứ tự. Nó thường được sử dụng trong việc xóa các phần tử lặp, tính toán các thao tác toán học như : giao, hợp, trừ tập hợp, …
- Set không hỗ trợ : truy xuất index (indexing) hoặc slicing(duyệt/tách một phần của danh sách),…
- Set hỗ trợ : x in set, len(set), for x in set
- Có 2 kiều dữ liệu cho dạng set : set và frozenset
  + set : có tính chất mutable (có thể update danh sách). Do tính chất mutable nên nó không có giá trị hash (giá trị băm), và không thể được sử dụng làm key cho từ điển
  + frozenset : có tính chất immutable (không thể cập nhật), vì vậy nó có giá trị hash và có thể được sử dụng như các key trong từ điển
  + Khởi tạo set và hình dạng của set : {1,2,3} hoặc {‘a’, ‘b’, ‘c’}, hoặc sử dụng các hàm constructor set([iterable]) hoặc frozenset([iterable])
- Các phương thức của Set : (tìm hiểu sau)

### 1.3.8.	Dict trong Python

### Note Quá trình làm project : 
  -	Khi thực hiện thao tác với Ma trận thì ta nên sử dụng thư viện numpy. Tức chuyển từ 1 list sang dạng array của numpy bằng np.array(list, kiểu dữ liệu)
  -	Đối với array trong numpy, giả sử nó đang là ma trận mà ta muốn truy xuất riêng các cột hoặc các hàng trong ma trận đó, ta làm như sau : a[1:5][2:4] để truy xuất các hàng từ 1 đến hàng 4 (= 5-1) và từ cột 2 tới cột 3 (= 4 – 1). Còn khi cần sử dụng bước nhảy thì ta làm như sau : a[1:5:2][2:4]
  -	Khi ta muốn nhân các ma trận, vector : Ở đây là nhân một cách thực sự thì ta cần phải sử dụng đến phương thức .dot(…). Ví dụ : a.dot(b). Còn khi muốn chia thì ta tiến hành nhân nghịch đảo thôi. Để tìm ma trận nghịch đảo của một ma trận thì ta sử dụng np.linalg.pinv(a) : Đây là cách tìm ma trận giả nghịch đảo (tức nó vẫn trả khi ma trận đó suy biến), hoặc sử dụng np.linalg.inv(a) để tìm ma trận nghịch đảo của a (ở trường hợp này thì có khả năng xảy ra suy biến )  ??? Hãy so sánh 2 hàm trên !!!
  -	Còn khi muốn nhân hay chia từng phần tử của ma trận (vector) này với từng phần tử của ma trận (vector) kia thì một cách đơn giản ta chỉ việc sử dụng các toán tử * hay / bình thường (nó đã hiểu)!!! Hoặc sử dụng phương thức __imul()__. Nhưng hình như họ không có __idiv__ tức rõ ràng trong documentation thì có phương thức này như lại không có tham số??? Why???
  -	Khi muốn tính max, min của từng cột hoặc theo từng hàm của ma trận, ta chỉ việc sử dụng các hàm np.max, np.min tương ứng. Hãy ghi nhớ ta cần phải chỉ ra số chiều tương ứng : Tức là nếu muốn tìm min theo cột thì chiều là 0, còn muốn tìm min theo các hàng thì chiều (axis) bằng 1 
  -	Hàm reshape trong thư viện numpy : np.reshape(ma_trận, các_chiều). Trong đó, ở các_chiều : nó có thể là kiểu tuple hoặc int.
    + Nếu -1 : Tức nó sẽ tạo thành 1 hàng duy nhất. Nếu ta muốn tạo nó lấy lượt lượt các phần tử theo từng dòng của ma trận thì ta cần phải có 1 tham số thứ 3 là order = ‘C’ (theo kiểu C), hoặc lấy từng phần tử trên từng cột thì order=’F’ (Fortran)
	
    + Nếu ta muốn tạo ra các ma trận có kích thước khác thì ta sử dụng tuple (2, 3) tức lúc này ta muốn ma trận mới sẽ có 2 hàng và 3 cột. Chú ý : các con số này khi nhân với nhau phải bằng đúng với số phần tử hiện có trong ma trận ban đầu
  -	Cách sắp xếp các phần tử trong numpy : Trong numpy chỉ hỗ trợ phương thức sắp xếp theo kiểu tăng dần, ví dụ : np.sort(ma_trận, axis, kind, order). Trong đó  : 
    + axis: Chỉ ra chiều nào mà ta đang muốn sắp xếp. Nó có vẻ hơi ngược một chút, nhưng thực ra lại khá hợp lý. Chúng ta còn nhớ khi tìm shape của một ma trận thì nó trả về 2 giá trị (số hàng, số cột), tức shape[0] = số hàng, còn shape[1] = số cột. Bây giờ nếu axis = 0 tức là ta muốn lấy kích thước của số hàng, vì phải biết kích thước của hàng nên ta sẽ biết được mỗi cột có bao nhiêu phần tử  Do đó sắp xếp từng cột. Còn khi axis = 1, tức ta biết được số cột của ma trận đó, đồng nghĩa với việc ta biết mỗi hàng có bao nhiêu phần tử, do đó ta sẽ sắp xếp theo từng hàng. Nếu axis = -1 thì nó sẽ lấy chiều cuối cùng (được trả về trong lệnh .shape), tức nó trả về số cột và vì thế nó sẽ sắp xếp theo từng hàng. Còn nếu axis = None thì nó sẽ đưa hết các hàng vào một dòng rồi mới sắp xếp tăng dần, sau đó sử dụng hàm reshape ở trên để trả lại ma trận ban đầu nhưng đã được sắp xếp (hàm reshape có tham số chỉ định ‘C’ hay ‘F’ (Fortran) khá hay!!)
    + Còn kind là việc ta sẽ sử dụng giải thuật nào để sắp xếp : ví dụ :’mergesort’, ‘quicksort’, …
    + Còn order :????
  -	Do trong numpy không hỗ sắp xếp giảm dần vì thế có một cách để ta sắp xếp giảm dần. Đó là sắp xếp tất cả các phần tử trên cùng một dòng bằng cách đạt tham số axis = None. Lúc này nó trả về một dãy số tăng dần, lúc này ta muốn trả về giảm dần thì sử dụng a[::-1], tức nó sẽ trả về theo chiều ngược lại. Tiếp theo ta sẽ sử dụng hàm reshape để hợp nhất nó lại 1 một ma trận ban đầu nhưng đã được sắp xếp giảm dần !!!
  
Những dòng trên cũng chưa chính xác bởi vì đối với ma trận khi được làm như trên thì nó sẽ xảy ra tình trạng hỗn loạn các phần từ trong ma trận. Trong khi mục tiêu của ta chỉ sắp xếp giảm dần theo cột hoặc theo hàng, vậy thì giải pháp là gì ? Hoặc là cũng sắp sắp xếp từng hàng hoặc từng cột rồi copy lại, hoặc là sắp xếp cả ma trận thì copy sang một ma trận mới theo thứ tự ngược lại
