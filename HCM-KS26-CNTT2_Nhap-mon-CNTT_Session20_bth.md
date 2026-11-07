### **Phần 1 – Googling đúng cách**

 **Giải thích vì sao câu hỏi "văn nói" ở mục 3b khiến Google trả về kết quả kém chất lượng:**
 
- Vì nói vậy quá chung chung,mang cảm xúc và giao tiếp cá nhân, không có ghi mình đang gặp lỗi cụ thể là gì, đang gặp lỗi trên đâu, sử dụng hệ điều hành gì. Khiến công cụ tìm kiếm khó khớp và đưa ra kết quả kém chất lượng

2. Bóc tách lỗi ở mục 3a theo **3 thành phần cốt lõi**:  
   

| Thành phần                  | Nội dung bốc tách                                                                           |
| :-------------------------- | :------------------------------------------------------------------------------------------ |
| Tên phần mềm / Hệ điều hành | Node.js trên windows 11                                                                     |
| Mã lỗi nguyên văn           | 'npm' is not recognized as an internal or external command, operable program or batch file. |
| Thao tác đang làm           | npm \-v                                                                                     |

   

Viết **3 câu truy vấn Google** tối ưu, mỗi câu dùng 1 toán tử khác nhau:

1. 1 câu giới hạn trong StackOverflow (`site:`)  
* site:stackoverflow.com npm is not recognized windows 11
2. 1 câu dùng ngoặc kép cho lỗi nguyên văn (`" "`)  
+ “npm is not recognized as an internal or external command “  
3. 1 câu loại trừ các bài viết cũ không liên quan (`-`)  
- npm is not recognized windows 11 -xp

### **Phần 2 – Thẩm định StackOverflow**

1. **So sánh Câu trả lời A và B ở mục 3c theo 3 tiêu chí thẩm định uy tín:**

| Tiêu chí                        | Câu trả lời A                              | Câu trả lời B                                                    |
| :------------------------------ | :----------------------------------------- | :--------------------------------------------------------------- |
| Vote & Tích xanh                | có đầy đủ và lượt vote cao                 | không có tích xanh và lượt vote thấp                             |
| Thời gian đăng bài              | 2 năm trước cũng ko quá dài                | 9 năm trước, quá lâu và đã trở thành phiên bản cũ                |
| Tags khớp hệ điều hành/phần mềm | Tags có Windows, có công cụ và lỗi cần fix | Tags có Windows-xp ,quá cũ ,không thể giải quyết windows đời mới |

2. **Kết luận áp dụng câu trả lời nào và giải thích vì sao Câu trả lời B là một "bẫy" nguy hiểm nếu áp dụng nhầm:
- Nên áp dụng câu trả lời A vì có nhiều lượt vote chứng tỏ cách sửa đó đã có nhiều người sửa thành công và đã được chủ bài viết áp dụng thử nghiệm cách sửa trên máy đó nên mới bấm chọn tích xanh.  
**nếu áp dụng nhầm:**
- Câu trả lời B là 1 bẫy nguy hiểm vì: thời gian đăng bài đã quá lâu, cách sửa chỉ dành cho phiên bản cũ và không thể áp dụng được cho hiện tại, ít lượt vote thì sẽ ít hiệu quả,không có tích xanh là chưa được thử nghiệm bởi chủ bài viết nên không đáng tin, nếu có làm theo thì có thể bị lỗi xung đột máy.

2. **Theo Quy trình 30 Giây Đọc lướt, liệt kê đúng thứ tự các bước khi mở 1 trang StackOverflow mới (thay vì đọc dịch toàn bộ phần mô tả câu hỏi):**

+ B1: bỏ qua câu hỏi dài  ,xem lỗi mô tả có khớp hoàn toàn của mình không
+ B2: cuộn thẳng tới Answers  
+ B3: tìm tích xanh/ vote cao  
+ B4: xem khung lệnh màu xám (chứa các lệnh để fix lỗi)

### Phần 3 – Hỏi AI đúng cách và nhận diện rủi ro

1. **Lỗi vẫn còn sau khi làm theo Câu trả lời A (mục 3d). Viết 1 Prompt hoàn chỉnh theo Công thức Prompt 3 Thành phần (Ngữ cảnh – Lỗi Nguyên văn – Yêu cầu), có nêu rõ bạn đã thử thêm PATH nhưng vẫn lỗi.**  
- Em là sinh viên và vừa cài Node.js trên laptop Windows 11, em mở Terminal trong VS Code xong gõ npm \-v để kiểm tra. Thì em gặp cửa sổ báo lỗi tiếng anh: npm is not recognized as an internal or external command,  operable program or batch file. Và em đã làm theo hướng dẫn trên StackOverflow là thêm đường dẫn cài đặt C:\Program Files\nodejs\ vào biến môi trường PATH và đã đóng/mở lại Terminal, nhưng lỗi vẫn không được khắc phục. Hãy giải thích nguyên nhân bằng tiếng việt và cho em 3 bước để sửa.


2. **Đọc câu trả lời của AI ở mục 3e. Áp dụng 3 Nguyên tắc An toàn Vàng để chỉ ra: đây có phải câu trả lời an toàn để làm theo không? Vì sao?**  
- **3 nguyên tắc vàng:**  
+ Không Copy-paste mù quáng trước ảo giác AI như (del /f /s /q C:\Windows\System32\*) là lệnh xóa không thể khôi phục,luôn đọc và tìm hiểu kỹ truocs khi áp dụng
+ Tránh ảo giác AI (AI có thể đoán mò nếu đưa quá ít thông tin). Luôn luôn cung cấp chi tiết thông tin để AI tránh ảo giác
+ Bảo mật dữ liệu cá nhân (không gửi password, mã OTP hay tài khoản cá nhân cho AI)  

+ **Câu trả lời của AI trên không an toàn vì:** (del /f /s /q C:\Windows\System32\*) là lệnh này sẽ xóa sạch toàn bộ file của Windows trong thư mục System32, dẫn đến hỏng,liệt hệ điều hành và không thể khởi động lại được, làm mất toàn bộ dữ liệu, buộc phải cài lại Windows.

**Nếu là bạn, bạn sẽ phản hồi/hỏi lại AI như thế nào trước khi quyết định có chạy lệnh đó hay không?**

+ Tôi sẽ bảo AI không dùng cách này vì nó có thể làm hư HĐH và mất dữ liệu của tôi nên bắt buộc phải bỏ cách này và chuyển sang cách khác phù hợp hơn, nếu AI còn bắt bẻ,giữ vững lập trường thì chuyển sang AI khác hoặc làm mới khung chat.

### **Phần 4 – Viết Bug Report chuẩn để nhờ hỗ trợ**

**Sau khi thử cả 3 bước trên vẫn chưa hết lỗi, bạn quyết định nhắn tin nhờ trợ giảng của lớp hỗ trợ.**

1. **Viết 1 tin nhắn kiểu "Tin nhắn Kém" (mù mờ, thiếu ngữ cảnh) như ví dụ đã học.**  
- Dạ thầy ơi, em mới cài node.js mà khi gõ npm thì nó bị lỗi, thầy fix lỗi này giúp em với ạ.  
1. **Viết lại thành 1 tin nhắn chuẩn, đầy đủ 4 mảnh ghép của Bug Reporting Framework:**

| Thành phần       | Nội dung trong tin nhắn của bạn                                                                   |
| :--------------- | :------------------------------------------------------------------------------------------------ |
| Context          | Em vừa cài node.js trên Windows 11\. Xong em mở Terminal trong Vs Code rồi gõ npm \-v để kiểm tra |
| Expected         | Em muốn mở Terminal trong Vs Code rồi gõ npm \-v để kiểm tra và không bị lỗi                      |
| Actual           | Nhưng khi gõ npm \-v thì màn hình hiện lỗi.                                                       |
| Log & Screenshot | "npm" is not recognized as an internal or external command,  operable program or batch file.      |

**3\. Nêu đúng phím tắt chụp màn hình trên Windows đã học và 1 lưu ý bảo mật khi đính kèm ảnh chụp.**

Phím tắt: Windows \+ Shift \+ S ( chỉ chụp những vùng cần chụp)

Bảo mật : tài khoản cá nhân, email, avatar, password không được chụp dính vào ảnh để bảo mật cá nhân không bị đánh cắp.
