
# TỔNG QUAN TỪNG CHƯƠNG SÁCH TRONG CUỐN LEARNING PYTHON (Author : Mark Lutz)

## Chương 5 : Numeric Types - Kiểu số
- Các kiểu dữ liệu dạng số (số nguyên, số thực, số phức).
- Các toán tử thao tác như : cộng, trừ, nhân, chia, ...
- Kiểu dữ liệu Set (cấu trúc dữ liệu lưu trữ theo dạng tập hợp) và Boolean (True và False tương ứng với 1 và 0),...
  
## Chương 7 : String Fundamentals (Cơ bản về Xâu chuỗi)
- String Basic : Trình bày tổng quan về Common String Literals And Operations (là một bảng mà trong đó tác giả liệt kê các toán tử thao tác với xâu, một số định dạng của xâu, những phương thức hữu ích thường sử dụng cho xâu) (tr191-192)

- String Literals  (tr192) : Nêu một số ví dụ về một vài định dạng của xâu trong python

- Single and Double-Quoted Strings are the Same (tr193) : Tác giả nói rằng việc bao bọc một xâu bởi nháy đơn hoặc nháy kép đều được chấp nhận trong python. Do vậy, nếu bản thân xâu chứa một ký tự nháy đơn thì hãy nên sử dụng nháy kép bao bọc bên ngoài xâu đó (hoặc nếu nếu vẫn muốn dùng nháy đơn để bao bọc thì nháy đơn bên trong xâu phải được viết dưới dạng \' để trình thông dịch không bị nhầm lẫn giữa nháy đơn ở trong xâu và những nháy đơn bao bọc xâu đó), ngược lại tương tự với trường hợp trong bản thân xâu có chứa ký tự nháy kép,...

- Escape Sequences Represent Special Characters (tr193) : Trình bày các ký hiệu đặc biệt như \n (xuống dòng mới), \r, \t (tab),...

- Raw Strings Suppress Escapes : (tr196)Khử đi sự tác động của ký tự Escape (\) nghĩa là làm cho các ký tự \n, \t,... sẽ hiện đúng "nguyên hình" trong xâu chứa nó ==> Nhờ việc thêm r ở đằng trước xâu đó như sau : r'C:\new_file' (nếu không có r ở phía trước thì trình thông dịch sẽ hiểu là C: rồi xuống dòng (do \n) rồi ew_file, còn khi có thêm r - viết tắt của raw string sẽ là cho xâu hiển thị dưới dạng nguyên gốc của nó). Cách thứ 2, ta có thể khử đi ký tự Escape như thế này : 'C:\\new_file' nghĩa là sử dụng \\ để khử đi tác dụng của ký tự escape '\'

- Triple Quotes Code Multiple Block Srings : (tr198)
  - Trình bày về công dụng của dấu nháy 3 như sau : """ ha noi """ ==> Công dụng chính là để lưu được text trên nhiều dòng khác nhau nghĩa là : bắt đầu từ """ trình thông dịch sẽ toàn bộ từng dòng,... cho tới khi nó gặp """. Chú ý : Nó sẽ quét luôn cả comment trên dòng thuộc phạm vi của nó, như vậy ta thấy được "tính quét toàn bộ dòng" của dấu nháy 3 này !!!
  
- Strings In Action (tr200) : Trình bày toàn bộ các phương thức, kỹ thuật thường sử dụng với String
  - Basic Operations (200) : Thao tác tìm độ dài len của xâu, nối xâu sử dụng toán tử +, cách thức để lặp thành nhiều xâu nhờ toán tử nhân '*' (toán tử này rất tiện), toán tử in để kiểm tra 1 ký tự (hoặc một xâu con) có nằm trong 1 xâu lớn.
  - Indexing and Slicing (201) : Các kỹ thuật indexing và slicing cụ thể như : Truy cập 1 phần tử từ index dương hoặc từ index âm (với index âm thì trình thông dịch sẽ hiểu như thế nào), cách kỹ thuật lấy ra các chuỗi con từ chuỗi cha (như s[i:j] hay s[i:j:k],..), các quy ước trong Python về index đầu tiên trong xâu (bằng 0), quy ước về các index âm, kỹ thuật đảo ngược xâu...
  
  - String Conversion Tools :  (205) Cách ép kiểu từ số Integer về Xâu nhờ phương phức str(), cách ép kiểu từ string về dạng số nhờ các phương thức int() hay float(),... Khi nối một chuỗi với một số bằng toán tử + thì ta cần phải ép kiểu số đó về dạng string trước rồi mới thực hiện nối xâu được (nếu không ép kiểu trước trình thông dịch sẽ báo lỗi) 
  
  - Character Code Conversions : (205) cách ép kiểu 1 ký tự về dạng mã ascii và ngược lại nhờ các hàm tương ứng ord(), chr()
  
  - Changing Strings : (208)
    - Một xâu string thì không thể bị sửa đổi (nghĩa là immutable sequence), ta chỉ có thể tạo đối tượng xâu mới (từ xâu hiện tại) mà không thể chỉnh sửa bản thân xâu hiện tại
	- Phương thức thay thế các ký tự trong xâu : replace()
	- Cách thức để truyền một tham số vào một xâu bằng 2 cách :
	  - Cách 1 : Sử dụng % như sau 'That is %d %s bird!' % (1, dead) ==> Sẽ hiển thị : That is 1 dead bird
	  - Cách 2 : Sử dụng phương thức format() của xâu như sau : 'That is {0} {1} bird!'.format(1, 'dead') ==> Sẽ hiển thị : That is 1 dead bird
  - Methods of Strings : (tr210) Tác giả trình bày một bảng chứa rất nhiều các phương thức thông dụng của String
  - String Method Examples : Changing Strings II (tr211)
    - Cách thay thế các ký tự trong xâu nhờ phương thức replace()
	- Cách tìm kiếm index của xâu con trong xâu lớn nhờ phương thức find()
	- Cách convert từ xâu sang list nhờ constructor : list()
	- Cách convert từ list sang xâu với tùy chọn ký tự phân cách nhờ phương thức join() (tr213)
  - Parsing Text (tr213)
    - Tách xâu con từ xâu cha (nhờ sử dụng index)
	- Tách các xâu từ xâu cha thành các xâu con chứa trong list với tùy chọn ký tự phân tách nhờ phương thức split()
  - Other Common String Methods in Action (214)
    - Cách loại bỏ ký tự trắng (thừa) ở bên trái xâu, bên phải xâu, hoặc ở 2 phía của xâu nhờ các phương thức lstrip(), rstrip() và strip()
	- Cách chuyển xâu thành chữ hoa
	- Kiểm tra xâu có bắt đầu bởi hoặc kết thúc bởi 1 xâu con nào đó nhờ phương thức endswith() và startwith()
	
  - String Format Expression : (tr216) Từ trang này trở đi (tới cuối chương) tác giả trình cách format xâu tức cách truyền giá trị vào xâu (mà lúc trước ta đã biết có 2 cách đó là sử dụng % hoặc .format()). Trong phần này tác giả sẽ trình bày kỹ càng và nâng cao hơn về 2 kỹ thuật này (cùng với 1 vài biến thể mở rộng !!!)
  
  ## Chương 8 (240): Lists and Dictionaries (2 kiểu cấu trúc dữ liệu dùng phổ biến trong Python)
  - List (tr240) : Tác giả trình bày một bảng tóm tắt các phương thức thao tác với List như : 
    - cách khởi tạo list, 
	- cách truy vấn một phần tử, l
	- lấy số lượng phần tử trong list, 
	- nối 2 list, nhân bản list nhờ toán tử *, 
	- cách sử dụng vòng lặp for để duyệt các phần tử trong list, 
	- kiểm tra một phần tử có thuộc list nhờ toán tử in, 
	- nối đuôi 1 phần tử mới vào list, mở rộng list bằng phương thức extend(), 
	- chèn phần tử vào list bằng insert(), 
	- tìm kiếm 1 phần tử trong list bằng phương thức index(), 
	- đếm số phần tử trong list bằng count(), 
	- sắp xếp các phần tử trong list bằng sort(), 
	- đảo ngược các phần tử trong list, tạo bản sao list bằng copy(), 
	- xóa toàn bộ các phần tử trong list bằng clear(), 
	- xóa một phần tử với chỉ số i trong list bằng pop() hoặc remove hoặc dùng lệnh toán tử del, ... 
	- cách sử dụng list comprehension (tạo ra list từ 1 vòng lặp for), 
	- cách sử dụng hàm map() để thực 1 hàm chỉ định nào đó trên toàn bộ phần tử của list,...
  
  - Basic List Operations : (242) 
    - Ví dụ về cách lấy số phần tử của list bằng hàm len(), 
	- cách nối 2 list bằng toán tử +, 
	- cách lặp hay nhân bản list bằng toán tử *
	
  - List Iteration and Comprehensions (242) : 
    - Ví dụ về kiểm tra 1 phần tử có thuộc trong một list, 
	- cách duyệt list sử dụng for
	- Cách sử dụng print() mà không tự động xuống dòng bằng cách thêm end=' ' ở cuối như sau : print(x, end='')
	- Cách sử dụng List Comprehension để tạo ra một list mới từ vòng lặp như sau : res=[c*4 for c in 'SPAM'] (tạo output là ['SSSS', 'PPPP', 'AAAA', 'MMMM'])
	- Ví dụ về cách sử dụng hàm append() để nối 1 phần tử vào cuối list
	- Ví dụ về cách sử dụng hàm map như sau : list(map(abs, [-1, -2, 0, 1, 2])), trong đó map sẽ áp dụng hàm abs() lên toàn bộ các phần tử trong list, rồi trả về list sau : [1, 2, 0, 1, 2] ==> Do vậy ta có thể xây dựng các hàm tùy thích rồi sử dụng hàm map() để áp hàm đã xây dựng được lên toàn bộ phần tử của list
	
  - Indexing, Slicing, and Matrixes (tr243) :
    - Cách truy vấn các phần tử trong list nhờ index
	- Cách tạo ra một ma trận 2 chiều bằng cách sử dụng lồng list trong list
	- Cách truy vấn các phần tử trong ma trận tạo được (từ việc lồng list trong list)
  - Changing Lists in Place : (244)
    - Cách sửa đổi các phần tử trong list (244-245): sửa đổi 1 phần tử, sửa đổi hay thay thế nhiều phần tử (phần này tác giả trình bày các ví dụ khá hay và linh hoạt trong cách nhìn nhận)
	- Cách nối thêm phần tử vào sau, cách mở rộng list bằng extend(), sắp xếp các phần tử trong list bằng sort() (nếu là string thì sẽ sắp xếp theo alphabet, còn nếu là số thì sắp xếp theo thứ tự)
	- Cách sắp xếp list với các phần tử có phân biệt chữ hoa hoặc không phân biệt chữ hoa (tr247)
	- Cách sắp xếp theo thứ tự giảm dần (ngược với tăng dần, chỉ cần chỉnh sửa tham số reverset=True) (tr247)
	- Tác giả trình bày thêm nhiều cách khác để có thể thực hiện sắp xếp (248)
	- (tr248-249) Cách mở rộng list bằng extend(), xóa phần tử cuối cùng của list bằng pop(), đảo ngược list bằng reverse() hoặc reversed(), cách sử dụng phương thức insert() để chèn, xóa phần tử sử dụng remove(), đếm số phần tử trong list bằng count(),...
  
  - Dictionaries (Cấu trúc dữ liệu từ điển) (tr250-252) : Tóm tắt bằng một bảng gồm các phương thức trong Dictionary
    - Cách khởi tạo dictionary rỗng, hoặc dictionary có phần tử, tạo dictionary dạng lồng nhau (tức bên trong dictionary này lại có một dictionary khác), sử dụng constructor dict() để khởi tạo dictionary, cách sử dụng hàm zip() để tạo dictionary, 
	- Cách lấy các value có key được cho, cách kiểm tra key có thuộc dictionary hay không, cách hiển thị toàn bộ key trong dictionary, cách hiển thị toàn bộ value trong dictionary, cách hiển thị các cặp (key, value)
	- Cách tạo một bản copy của dictionary
	- Cách xóa toàn bộ phần tử trong dictionary
	- Cách đếm số phần tử trong dictionary nhờ phương thức len()
	- Cách thêm một phần tử mới cho dictionary
	- cách xóa một key trong dictionary
	- Cách tạo dictionary nhờ vòng lặp for (tức sử dụng dictionary comprehension)
	
  - Basic Dictionary Operations : (tr253)
    - Cách tạo Dictionary, cách truy vấn 1 phần tử trong dictionary bằng key
	- Đếm số item trong dictionary bằng len()
	- kiểm tra 1 key có thuộc dict không nhờ toán tử in
	- cách in toàn bộ key của dictionary theo dạng list
  - Change Dictionaries in Place : (tr 254)
    - Cách sửa value của key nào đó trong dict
	- Cách xóa key trong dict bằng toán tử del
	- Cách thêm 1 cặp key-value (tức entry) vào dict
	- Cách in ra các value (giá trị) trong dictionary, cách in item (cặp key-value dạng tuple) trong dict
	- truy vấn key để trả về value tương ứng
	- Cách xóa key bằng pop
  - Mapping values to key (tr257-258)
    - Cách duyệt các cặp (key-value) trong dictionary (tr257)
  - Using dictionaries for sparse data structures : Tuple keys (tr259)
    - Cách sử dụng dictionary để lưu trữ ma trận thưa (là ma trận có ít phần tử, vì vậy người ta sẽ lưu theo dạng dictionary hơn là lưu bằng list, và chỉ cần lưu những thành phần có giá trị vào dictionary)
	- Kiểm tra một key đã tồn tại trước khi in ra value ứng với key đó (nhờ toán tử kiểm tra in, hoặc sử dụng try-except để bắt sự kiện) (tr260), hoặc lựa chọn tham số mặc định để in ra nếu key không có trong dictionary
  - Nesting in dictionaries : (260) Cách lồng các dictionary khác hoặc list làm value cho một key trong dictionary
  
  - Other Ways to Make Dictionaries : (tr262)
    - Nhắc lại 4 cách tạo dictionary 
	- Cách tạo dictionary nhờ hàm zip để hợp nhất 2 list : một list đóng vai trò chứa các key, list còn lại đóng vai trò chứa các value. Rồi ép kiểu chúng (các cặp tuple key-value sau khi được hợp nhất) bằng dict(), từ đó tạo ra dictionary với các cặp key-value tương ứng !!!
	- Tạo dictionary với cùng value cho tất cả các key (tr262)
  - Dictionary Comprehension : (tr265)
    - Trình bày các tạo từ điển nhờ vòng lặp for (tức Dictionary Comprehension)
  - Dictionary Views in 3.X : (tr266)
	- Khái niệm về View Object : được hiểu là iterable (nghĩa là tại mỗi thời điểm chỉ trả về 1 phần tử), ta không thể indexing (lấy phần tử dựa trên index) cho iterable (bởi vì iterable chỉ trả 1 phần tử tại 1 thời điểm), còn list thì trả về toàn bộ phần tử tại 1 thời điểm nên ta có thể indexing các phần tử tùy thích. Ta có thể ép kiểu iterable về dạng list nhờ ép kiểu. Bản thân iterable cũng có thể nằm trong for để được duyệt từng phần tử nằm trong nó (iterable này) bởi vì cách duyệt của for là duyệt từng phần tử trong từng thời điểm !!! 
	- Một số ví dụ về view object (hay iterable)
	- Cách duyệt các phần tử từ iterable (view object) trong for
  
  - Sort Dictionary Keys : (tr269)
    - Trình bày cách sắp xếp các phần tử trong dictionary : Hàm sort chỉ sắp xếp được đầu vào dạng list không sắp xếp được nếu đầu vào dạng iterable (tức view object), còn sorted có thể sắp xếp được bất kỳ iterable nào hay list, hoặc sử dụng sorted để truyền vào trực tiếp dictionary cần sắp xếp 
  - The has_key() method is dead in 3.X : (tr270) 
    - Phương thức has_key() (kiểm tra 1 key có nằm trong dictionary) không còn dùng trong python 3.x, mà thay vào đó người ta sử dụng toán tử in (tr270)
	
## Chương 9 : (tr275) Tuples, Files, and Everything Else : Trình bày mọi thứ liên quan tới Cấu trúc dạng Tuple, Cách sử dụng File và những thứ khác

- Tuples : (tr276) Tác giả trình bày một bảng tóm tắt về : 
  - Constructor của tuple (tức cách để khởi tạo một tuple. Kiểu tuple lồng nhau (tức bên trong tuple lại có một tuple khác). Chú ý rằng : Nếu tuple chỉ có một phần tử thì phải ghi thêm dấu phẩy vào cuối thì trình thông dịch mới hiểu được tức là (1,) còn nếu không có dấu phẩy ở cuối trình thông dịch sẽ chỉ hiểu là (1) tức chỉ hiểu là một số nguyên (chứ ko hiểu là một tuple). Cách dùng constructor để convert từ string sang tuple
  - Indexing : Cách truy cập một phần tử trong tuple sử dụng index như T[0], T[1],... nhưng nếu có nhiều tuple lồng trong tuple thì cách truy cập có viết như sau T[1][0][2] (ở đây 3 lớp tuple lồng nên ta sẽ truy cập như vậy !)
  - Slicing - Cách lấy ra (trích xuất) một tuple con từ trong một tuple gốc ==> Sử dụng T[i:j] (lấy phần tử T[i] tới T[j-1])hoặc nếu muốn linh hoạt chọn cách phần tử trong tuple mà cách đều nhau ta có thể sử dụng T[i:j:k] (tức các phần tử được chọn ra xuất phát từ chỉ số i, rồi cách đều nhau k đơn vị, và kết thúc ở 1 phần tử phía trước j tức không bao giờ có thể có T[j] trong đó)
  - Cách lấy độ dài của tuple sử dụng hàm len()
  - Cách nối 2 tuple để tạo thành tuple mới (con trỏ tham chiếu tới cùng nhớ mới) nhờ sử dụng toán tử nối +
  - Cách nhân bản/sao chép nhiều bản từ 1 tuple sử dụng toán tử nhân bản là *
  - Cách duyệt tuple : sử dụng vòng for ... in ...
  - Kiểm tra 1 phần tử có tồn tại trong tuple hay không sử dụng toán tử in
  - Tạo list từ tuple nhờ sử dụng List Comprehension ==> ??? Không biết có Tuple Comprehension ko??? Đã thử nhưng khi in ra thì nó không trả về dạng tuple mà lại chỉ trả về địa chỉ nơi lưu trữ ==> Còn nếu muốn nó hiện ra dạng tuple hay list thì phải ép kiểu ==> Tại sao khi sử dụng List Comprehension thì nó hiện ra đầy đủ, nhưng khi sử dụng Tuple Comprehension thì nó lại trả về địa chỉ (không hiện toàn bộ, có vẻ như view object hay iteration vậy)
  - Tìm index của một phần tử trong tuple sử dụng phương thức index()
  - Đếm số lần xuất hiện của một phần tử trong tuple sử dụng phương thức count()

- Tuples In Action : (tr277) Trình bày cụ thể hơn về cách sử dụng các phương thức trong Tuple
  - (tr277)Trình bày các ví dụ cụ thể về cách sử dụng các thao tác nối tuple (+), nhân bản tuple (*), và truy xuất các phần tử từ tuple,...
  - Commas and parentheses (tr277-278): Tác giả cảnh báo rằng khi muốn tạo ra một tuple gồm 1 phần tử thì ta cần phải bổ sung thêm dấu phẩy ở cuối để trình thông dịch có thể hiểu được, ví dụ như (5,) tức tuple có 1 phần tử 5. Còn đối với việc tạo tuple có nhiều hơn 1 phần tử thì điều này không cần thiết tức (5,8,10)
  - Conversion, Methods, and Immutability : (tr278) 
    - Trình bày về tính Immutability (không thể sửa đổi được) của Tuple, nghĩa là một khi tuple được tạo ra thì ta không thể nào thêm/xóa/hay sắp xếp lại các phần tử trong đó được ==> Vì vậy nếu muốn sửa đổi một tuple, ta cần phải tạo một list mới chứa các phần tử trong tuple (nhờ phép ép kiểu), sau đó thực hiện thêm/sửa/xóa/sắp xếp,... rồi lại ép kiểu list về tuple và gán lại cho con trỏ tuple ban đầu !!!
	- Tác giả trình bày các ví dụ về Tìm index của một phần tử (sd index()), Đếm số lần xuất hiện của một phần tử (sd count())
	- Một vấn đề nữa khá hay : Đó là dù tuple có tính chất Không thể sửa đổi, điều này chỉ đúng với các phần tử ở level cao nhất của tuple, nhưng không còn đúng với nội dung bên trong tuple. Nghĩa là nếu trong tuple có một phần tử dạng list như sau : t = ([1,2], 10). Rõ ràng ta không thể nào thay đổi được t[0] vì t[0] hay t[1] là những phần tử nằm ở level cao nhất trong tuple, nhưng điều đó không có nghĩa rằng ta không thể thay đổi các phần tử ở level thấp hơn, như trong ví dụ : Ta hoàn toàn có thể thay đổi t[0][0] = 100, lúc này tuple sẽ bị thay đổi là : ([100, 2]), 10) ==> Rất hay phải không ???

	- Why Lists and Tuple : (279) Phần này tác giả giải đáp về việc Tại sao có List rồi mà cần phải tạo Tuple để làm gì? Chúng ta hãy nhìn vào sự khác nhau chính giữa 2 kiểu này đó là : Tính có thể thay đổi được hay không? Với List thì luôn có thể thay đổi được các phần tử trong nó, còn đối với Tuple thì việc sửa đổi là không thể, chúng ta có thể liên tưởng tuple với các biến hằng trong các ngôn ngữ lập trình khác, nhưng tuple lại không phải là 1 biến mà nó là một đối tượng (một con trỏ tới một vùng nhớ mà không thể bị thay đổi, còn list là một con trỏ mà trỏ tới một vùng nhớ có thể thay đổi). Vậy ứng dụng của tuple là gì? Người ta sẽ sử dụng tuple làm các key trong cấu trúc Dictionary bởi đặc tính của key là phải không bị thay đổi nên việc chọn lựa tuple là hoàn toàn hợp lý. Hơn nữa khi sử dụng tuple làm key cho các item trong từ điển cũng khá linh hoạt bởi vì : tuple có khả năng chứa được nhiều giá trị ==> Rất tiện lợi !!!
	
	- Records Revisited : Named Tuples (tr280) Tác giả trình bày cách để một tuple vừa có thể truy xuất các phần tử sử dụng index, vừa có thể truy xuất các phần tử sử dụng key ==> Bằng cách sử dụng 1 thư viện có sẵn của python là collection
	
	
- Files : (tr282-283) Tác giả trình bày về một bảng tóm tắt về các thao cho việc sử dụng Files như sau
  - Cách mở một file cho việc đọc hoặc ghi (mặc định sẽ mở để đọc). Trong tên file thì thường có các ký hiệu đặc biệt như \ do vậy ta cần nên sử dụng r' ' để trình thông dịch hiểu tên file theo nghĩa thô (raw - tức những ký hiệu escape trong tên file sẽ bị vô hiệu hóa để không còn là một ký tự đặc biệt trong python nữa) 
  - Cách đọc toàn bộ file (sd input.read()), đọc N ký tự tiếp theo(input.read(N)), đọc cả một dòng (input.readline()) (một dòng được hiểu là khi nào trình thông dịch gặp ký tự xuống dòng '\n' chứ không phải gặp dấu chấm đâu nhé!), cách đọc và đưa toàn bộ dòng trong file vào một list (nghĩa là mỗi phần tử trong list sẽ chứa 1 dòng trong file)
  - Cách viết một xâu vào file (output.write(Xâu_cần_viết)), viết các dòng được lưu trong list vào 1 file (output.writelines(tên_list))
  - Cách đóng file (tức đã sử dụng xong file đó rồi) nhờ hàm close()
  - Cách đẩy dữ liệu (buffer) của output vào bộ nhớ ngoài mà không làm đóng file (output.flush()) (nghĩa là đối với file output thì khi ghi dữ liệu vào output thì trình thông dịch luôn ghi vào buffer trước, tới khi buffer đầy thì mới tiến hành đẩy vào vùng nhớ lưu file trong bộ nhớ ngoài. Còn thao tác flush() sẽ giúp ta đẩy buffer vào bộ nhớ ngoài mà không làm cho file đó bị đóng lại)
  - Cách dịch chuyển sang một vị trí mới trong file
  - Cách duyệt file theo từng dòng một 
  - Cách mở file theo kiểu mã hóa nào, ví dụ như kiểu 'utf8' hay 'latin-1' ==> Việc chọn encoding này cũng khá quan trọng!
  
- Open File : (tr283) Trình bày một ví dụ cụ thể về cách mở file với các chế độ (mode) đọc hay ghi 
- Files In Action :(tr285)
  - Ví dụ cụ thể về cách ghi 1 dòng vào file, cách đọc các dòng từ file (sd phương thức readline()) hoặc đọc toàn bộ file (bằng phương thức read())
- Storing Python Objects in Files: Conversions (tr288) : Trong phần này tác giả muốn nói đến một vấn đề khi lưu một đối tượng vào một file. Rõ ràng, giải pháp đơn giản nhất ta có thể nghĩ tới đó là : Sẽ ép kiểu đối tượng đó về dạng String, sau đó ghi vào file, sau này khi muốn lấy lại đối tượng từ file, ta sẽ đọc xâu string này và ép kiểu nó về dạng object ban đầu (nhờ hàm eval() : đây là hàm có khả năng ép kiểu string về đúng dạng object của nó). Đối với việc ép kiểu các string về dạng đối tượng thì cần sử dụng hàm eval(), còn nếu muốn ép kiểu string về dạng int, float.. thì chỉ cần sử dụng các constructor int(), float() tương ứng để ép kiểu từ các string đó !!!

- Storing Native Python Objects : pickle (tr290) Trình bày cách sử dụng thư viện pickle để lưu trực tiếp đối tượng vào file (mà không cần phải quá trình ép kiểu sang string rồi mới ghi) ==> Lúc này để ghi đối tượng vào file ta sử dụng phương thức dump() từ đối tượng của pickle, còn muốn truy xuất đối tượng từ file ta sử dụng phương thức load() của đối tượng pickle

- Storing Python Objects In JSON Format (tr291) : Cách lưu trữ một đối tượng (chắc là ám chỉ tới từ điển, vì chỉ có từ điển trong python mới có cấu trúc giống với JSON nhưng đang còn ở dạng đối tượng) về dạng JSON (JSON bản chất là string nhưng tuân theo quy tắc key-value). Sử dụng đối tượng (thư viện) json có sẵn trong python, sau đó gọi phương thức dumps() để ép kiểu đối tượng từ điển về dạng JSON, sau đó nếu muốn ép kiểu ngược trở lại từ JSON về đối tượng từ điển ta cần sử dụng phương thức loads(). Đặc biệt phần này tác giả cũng trình bày cách ghi một đối tượng vào file theo định dạng JSON !!!

- File Context Managers : (tr294) Trình bày về Bộ quản lý ngữ cảnh của file sử dụng with, nghĩa là lúc này ta không cần phải sử dụng lệnh đóng file close() hay try-finally để bắt sự kiện, bởi vì lúc này bộ quản lý ngữ cảnh file sẽ đảm nhiệm tất mọi việc đó ==> Do vậy sẽ làm cho code ngắn gọn và dễ hiểu hơn rất nhiều !!!

- Core Types Review and Summary : (tr296) Tác giả trình một bảng tóm tắt về toàn bộ các kiểu dữ liệu có trong Python như Numbers, Strings, List, Dictionaries, Tuples, Files, Sets (dạng tập hợp như {1,2,5}, và các phần tử có khả năng sửa đổi), Frozenset (cũng giống như set, nhưng các phần tử trong Frozenset không thể bị sửa đổi), bytearray

- References Versus Copies :(tr297) Trình bày về vấn đề khi có nhiều tham chiếu (con trỏ) cùng tham chiều tới một vùng nhớ nên 1 tham chiếu làm thay đổi vùng nhớ thì các tham chiếu còn lại cũng sẽ bị ảnh hưởng (do cùng trỏ tới một vùng nhớ đó) ==> Vì vậy người ta nghĩ đến việc copy (tức không cho phép tham chiếu tới cùng 1 vùng nhớ, mà sẽ tạo ra một vùng nhớ mới lưu các giá trị trong vùng nhớ thứ nhất, do vậy 2 vùng nhớ này có các giá trị giống nhau nhưng không liên quan gì tới nhau). Nhưng sau đó lại xuất hiện một vấn đề khác là : copy nông. Nghĩa là khi bên trong một list lại chứa một con trỏ (tham chiếu) vì vậy khi copy thì con trỏ này cũng sẽ bị copy theo, do vậy lúc này sẽ có 2 con trỏ cùng trỏ tới 1 vùng nhớ. Phương thức copy() là copy nông, trong python còn hỗ trợ cả copy sâu nhờ sử dụng phương thức deepcopy()(nghĩa là nó sẽ truy xuất tới vùng nhớ mà tham chiếu đó trỏ tới để copy,... cho tới khi truy xuất hết toàn bộ các tham chiếu)!

- Comparisons, Equality, and Truth : (tr300)
  - Trình bày sự khác nhau giữa toán tử == và is : Toán tử == để so sánh về giá trị, còn toán tử is để so sánh tham chiếu (xem 2 tham chiếu nào có cùng trỏ tới cùng 1 vùng nhớ không)
  - Ngoài ra tác giả cũng trình bày chi tiết về các toán tử >,==, <
  
- The Meaning Of True And False In Python (tr304) : Ý nghĩa thực sự của 2 kiểu True/False, thông thường được hiểu những đối tượng có giá trị khác không hay khác rỗng thì được hiểu là True, còn ngược lại sẽ được hiểu là False ==> Khá thoải mái

- The None Object (tr304): Nói về bản chất của đối tượng None ==> Thực chất nó chẳng tham chiếu tới cái gì cả, nó không có giá trị gì, mà chỉ là một vật giống như "bù nhìn" vậy !

- The bool type (tr305) : Nói về kiểu dữ liệu bool

- Type Objects : (tr306) : Phương thức để trả lại kiểu dữ liệu của một đối tượng là type(), Phương thức giúp kiểm tra một đối tượng có thuộc kiểu dữ liệu này không (sử dụng isinstance(đối tượng, kiểu dữ liệu) trả về True hoặc False). Bản chất thì function cũng là một kiểu dữ liệu nên cũng sẽ kiểm tra được một đối tượng có phải là kiểu dữ liệu function ko???

- Assignment Creates References, Not Copies : (tr308) Kỹ thuật copy các giá trị từ một đối tượng sử dụng L[:]
- Repetition Adds One Level Deep : Tác giả trình bày cách sử dụng toán tử nhân bản *, bản chất của toán tử này là nhân bản các tham chiếu ==> Đây là một nhược điểm ==> Từ đó tác giả đưa ra cách để khắc phục nhược điểm này ==> Khá hay 


## Chương 13 : While and For loops

## Chương 14 : Iterations and Comprehensions

## Chương 16 : Function Basic 

## Chương 23 : Module Coding Basic 

## Chương 28 : A More Realistic Example
	



	
	
  	
