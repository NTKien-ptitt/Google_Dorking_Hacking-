# Google_Dorking_Hacking-
**Google Dorking** là kỹ thuật sử dụng các toán tử tìm kiếm nâng cao của Google để tìm kiếm thông tin nhạy cảm hoặc cấu hình không được bảo mật trên các website; hacker thường dùng để thu thập dữ liệu, xác định lỗ hổng bảo mật và chuẩn bị cho các cuộc tấn công.
---
### Các quy tắc tìm kiếm trong Google Dorking (Google Hacking)

Google Dorking dựa trên các toán tử tìm kiếm nâng cao để truy xuất thông tin cụ thể từ cơ sở dữ liệu của Google. Dưới đây là các quy tắc phổ biến và ví dụ minh họa:

---

### 1. **Tìm kiếm trong trang web cụ thể**  
**Toán tử:** `site:`  
- **Mục đích:** Tìm kiếm nội dung chỉ trong một tên miền cụ thể.  
- **Ví dụ:**  
  ```
  site:example.com
  site:gov.vn "login"
  ```

---

### 2. **Tìm kiếm theo tiêu đề trang**  
**Toán tử:** `intitle:`  
- **Mục đích:** Tìm kiếm từ khóa trong tiêu đề của trang web.  
- **Ví dụ:**  
  ```
  intitle:"index of" "password"
  intitle:"login" "admin"
  ```

---

### 3. **Tìm kiếm theo URL**  
**Toán tử:** `inurl:`  
- **Mục đích:** Tìm kiếm từ khóa xuất hiện trong URL.  
- **Ví dụ:**  
  ```
  inurl:admin
  inurl:"php?id="
  ```

---

### 4. **Tìm kiếm tệp cụ thể**  
**Toán tử:** `filetype:`  
- **Mục đích:** Tìm kiếm các loại tệp cụ thể như PDF, TXT, DOC, XLS.  
- **Ví dụ:**  
  ```
  filetype:pdf "confidential"
  filetype:xls "username password"
  ```

---

### 5. **Loại trừ kết quả không mong muốn**  
**Toán tử:** `-`  
- **Mục đích:** Loại bỏ các từ khóa hoặc nội dung không mong muốn khỏi kết quả.  
- **Ví dụ:**  
  ```
  "password" -site:github.com
  intitle:"index of" -inurl:login
  ```

---

### 6. **Tìm kiếm cụm từ chính xác**  
**Toán tử:** `""` (dấu ngoặc kép)  
- **Mục đích:** Chỉ tìm kiếm các kết quả chứa cụm từ chính xác.  
- **Ví dụ:**  
  ```
  "database backup"
  "admin login"
  ```

---

### 7. **Tìm kiếm dữ liệu trên bản lưu trữ của Google**  
**Toán tử:** `cache:`  
- **Mục đích:** Truy cập phiên bản được lưu trữ trong bộ nhớ đệm của Google.  
- **Ví dụ:**  
  ```
  cache:example.com
  ```

---

### 8. **Tìm kiếm kết hợp nhiều toán tử**  
- **Ví dụ:**  
  ```
  site:edu.vn filetype:pdf "exam answers"
  intitle:"index of" "admin" filetype:txt
  site:example.com inurl:"login" "username"
  ```

---

### Ứng dụng Hacker:  
Hacker thường sử dụng Google Dorking để:  
1. Tìm thông tin nhạy cảm như danh sách tài khoản, mật khẩu, file cấu hình.
2. Khai thác thư mục công khai và dữ liệu không được bảo vệ.
3. Xác định các lỗ hổng tiềm ẩn như URL dễ bị SQL Injection (`php?id=`).

### Lưu ý:
Việc sử dụng Google Dorking cần tuân thủ pháp luật và không được xâm phạm quyền riêng tư. Các thao tác chỉ nên thực hiện trong môi trường kiểm thử có sự cho phép.
