
# Google Dorking Hacking
### 1. [Các quy tắc tìm kiếm trong Google Dorking (Google Hacking)](#các-quy-tắc-tìm-kiếm-trong-google-dorking-google-hacking)

  - [1. Tìm kiếm trong trang web cụ thể](#1-tìm-kiếm-trong-trang-web-cụ-thể)
  - [2. Tìm kiếm theo tiêu đề trang](#2-tìm-kiếm-theo-tiêu-đề-trang)
  - [3. Tìm kiếm theo URL](#3-tìm-kiếm-theo-url)
  - [4. Tìm kiếm tệp cụ thể](#4-tìm-kiếm-tệp-cụ-thể)
  - [5. Loại trừ kết quả không mong muốn](#5-loại-trừ-kết-quả-không-mong-muốn)
  - [6. Tìm kiếm cụm từ chính xác](#6-tìm-kiếm-cụm-từ-chính-xác)
  - [7. Tìm kiếm dữ liệu trên bản lưu trữ của Google](#7-tìm-kiếm-dữ-liệu-trên-bản-lưu-trữ-của-google)
  - [8. Tìm kiếm kết hợp nhiều toán tử](#8-tìm-kiếm-kết-hợp-nhiều-toán-tử)
### 2. [Cách sử dụng](#cách-sử-dụng)
### 3. [Các ví dụ kết hợp](#các-ví-dụ-kết-hợp)
### 4. [Mục đích sử dụng](#mục-đích-sử-dụng)
### 5. [Mục đích xấu (nếu không được phép)](#mục-đích-xấu-nếu-không-được-phép)

####################
# [Lưu ý](#lưu-ý)  #
####################
---
### Example: site:com.cn intitle:"index of" "username.txt"
**Google Dorking** là kỹ thuật sử dụng các toán tử tìm kiếm nâng cao của Google để tìm kiếm thông tin nhạy cảm hoặc cấu hình không được bảo mật trên các website; hacker thường dùng để thu thập dữ liệu, xác định lỗ hổng bảo mật và chuẩn bị cho các cuộc tấn công.

---
### Các quy tắc tìm kiếm trong Google Dorking (Google Hacking)

Google Dorking dựa trên các toán tử tìm kiếm nâng cao để truy xuất thông tin cụ thể từ cơ sở dữ liệu của Google và kết hợp toán tử (a)^(a)|(A). 
Dưới đây là các quy tắc phổ biến và ví dụ minh họa:

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

**`intext:`** là một toán tử tìm kiếm nâng cao trong Google Dorking, dùng để tìm kiếm **các từ khóa xuất hiện trong nội dung của trang web** (body text). Nó đảm bảo rằng kết quả trả về phải có chứa từ khóa trong nội dung văn bản, không chỉ trong tiêu đề hay URL.

---

### Cách sử dụng:
- **Cú pháp:**  
  ```
  intext:<từ khóa>
  ```
- **Ví dụ:**  
  ```
  intext:"password"
  ```
  Kết quả sẽ là các trang web có chứa từ "password" trong nội dung của chúng.

---

### Các ví dụ kết hợp:
1. **Tìm thông tin nhạy cảm cụ thể:**  
   ```
   intext:"username" intext:"password"
   ```
   Tìm các trang web có cả từ "username" và "password" trong nội dung.

2. **Tìm kiếm các thông tin liên quan đến cấu hình AWS:**  
   ```
   intext:"aws_access_key_id" intext:"aws_secret_access_key"
   ```
   Tìm các trang có chứa thông tin khóa truy cập AWS.

3. **Tìm kiếm tài liệu hoặc mã nguồn:**  
   ```
   intext:"BEGIN RSA PRIVATE KEY"
   ```
   Tìm các trang có chứa khóa RSA riêng tư (thường bị lộ do cấu hình sai).

4. **Kết hợp với các toán tử khác:**  
   ```
   site:github.com intext:"password"
   ```
   Chỉ tìm các trang trên GitHub có chứa từ "password" trong nội dung.

---

### Mục đích sử dụng:
- **Hợp pháp:**  
  - Tìm tài liệu kỹ thuật hoặc thông tin công khai cần thiết.
  - Kiểm tra bảo mật của hệ thống (như thông tin bị lộ qua nội dung công khai).

---
# Mục đích xấu (nếu không được phép):**  
  - Tìm thông tin nhạy cảm như mật khẩu, khóa API, hoặc dữ liệu bảo mật khác trong các trang công khai và không được pháp.

---

# Lưu ý 
## Việc sử dụng `Google_Dorking_Hacking-` để tìm kiếm thông tin nhạy cảm cần tuân thủ pháp luật. Hành vi khai thác hoặc sử dụng trái phép có thể bị xem là vi phạm pháp luật.
