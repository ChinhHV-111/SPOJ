# Buổi 1: Visual Code Studio & Markdown
***Tác giả: Hoàng Văn Chính D23***

- [Buổi 1: Visual Code Studio \& Markdown](#buổi-1-visual-code-studio--markdown)
  - [A. Mục tiêu](#a-mục-tiêu)
  - [B. Yêu cầu chuẩn bị (Người dạy)](#b-yêu-cầu-chuẩn-bị-người-dạy)
  - [C. Yêu cầu chuẩn bị (Người học)](#c-yêu-cầu-chuẩn-bị-người-học)
  - [D. Tiến trình bài giảng](#d-tiến-trình-bài-giảng)
    - [I. Kiểm tra tiến độ SPOJ](#i-kiểm-tra-tiến-độ-spoj)
    - [II. Visual Code Studio](#ii-visual-code-studio)
      - [1. Giới thiệu chung](#1-giới-thiệu-chung)
      - [2. Đặc điểm nổi bật](#2-đặc-điểm-nổi-bật)
        - [a. Hỗ trợ đa nền tảng](#a-hỗ-trợ-đa-nền-tảng)
        - [b. Hiệu suất cao và nhẹ](#b-hiệu-suất-cao-và-nhẹ)
        - [c. Kho tiện ích mở rộng phong phú](#c-kho-tiện-ích-mở-rộng-phong-phú)
        - [d. IntelliSense - Gợi ý mã thông minh](#d-intellisense---gợi-ý-mã-thông-minh)
        - [e. Terminal tích hợp](#e-terminal-tích-hợp)
      - [3. Sử dụng VS Code](#3-sử-dụng-vs-code)
        - [a. Một số kiến thức cơ bản](#a-một-số-kiến-thức-cơ-bản)
        - [a. IntelliSense trong VS Code](#a-intellisense-trong-vs-code)
        - [b. Một số phím tắt trong VS Code (Phần này có thể cap màn hình gửi luôn cho các em, chú ý thực hành)](#b-một-số-phím-tắt-trong-vs-code-phần-này-có-thể-cap-màn-hình-gửi-luôn-cho-các-em-chú-ý-thực-hành)
        - [c. Giới thiệu một số extension thường dùng](#c-giới-thiệu-một-số-extension-thường-dùng)
    - [III. Debug trong VS Code](#iii-debug-trong-vs-code)
    - [IV. Markdown \& GitHub cơ bản](#iv-markdown--github-cơ-bản)
      - [1. Giới thiệu Markdown](#1-giới-thiệu-markdown)
      - [2. Cú pháp cơ bản](#2-cú-pháp-cơ-bản)
        - [a. Tiêu đề](#a-tiêu-đề)
        - [b. Định dạng văn bản](#b-định-dạng-văn-bản)
        - [c. Danh sách](#c-danh-sách)
        - [d. Chèn liên kết \& hình ảnh](#d-chèn-liên-kết--hình-ảnh)
        - [e. Đoạn mã nguồn (Code Block)](#e-đoạn-mã-nguồn-code-block)
        - [f. Trích dẫn](#f-trích-dẫn)
        - [g. Bảng](#g-bảng)
      - [3. Cú pháp nâng cao](#3-cú-pháp-nâng-cao)
      - [4. GitHub](#4-github)


## A. Mục tiêu
1. Kiểm tra tiến độ SPOJ
2. Hiểu vể Visual Code Studio

## B. Yêu cầu chuẩn bị (Người dạy)
1. Đọc, nghiên cứu kĩ giáo án vì đây là giáo án mới
2. Tạm thời tránh nhắc đến snippets
3. Vì buổi này khá nặng lý thuyết dạy chính nên share màn hình từ đầu buổi, giảng đến đâu thực hành đến đấy.

## C. Yêu cầu chuẩn bị (Người học)
1. Hoàn thành >40% tiến độ SPOJ
2. Tìm hiểu và tải Visual Code Studio về máy
3. Cài đặt môi trường cho code C/C++
4. Tìm hiểu về debug trong VS Code
5. Tìm hiểu markdown và đăng ký tài khoản GitHub, sử dụng kéo thả cơ bản.

## D. Tiến trình bài giảng
### I. Kiểm tra tiến độ SPOJ
Từng em báo cáo số bài làm được, % chỉ tiêu, khó khăn gặp phải

### II. Visual Code Studio
Hướng dẫn nhanh nếu các em chưa cài được hoặc đang bị lỗi (ưu tiên cài bằng MSYS2 và thiết lập môi trường user variables): https://www.youtube.com/watch?v=Gwix4rtQpdk&t=469s
> Câu hỏi: Tại sao lại phải cài đặt MinGW và thiết lập môi trường trong environment variables để chạy file C/C++?

**Trả lời: MinGW là bộ công cụ giúp biên dịch C/C++ trên Window. Khi chạy chương trình hệ thống sẽ tìm kiếm chương trình biên dịch nằm trong biến môi trường `Path`. Vì vậy kể cả đã tải MinGW nhưng chưa dẫn vào `Path` thì Window sẽ không tìm thấy trình biên dịch và báo lỗi**

#### 1. Giới thiệu chung
Visual Studio Code (VS Code) là một trình soạn thảo mã nguồn miễn phí và mạnh mẽ do Microsoft phát triển. Nó hỗ trợ nhiều ngôn ngữ lập trình, có khả năng mở rộng với các tiện ích (extensions) và tích hợp nhiều công cụ hỗ trợ lập trình viên.

#### 2. Đặc điểm nổi bật
##### a. Hỗ trợ đa nền tảng
- Hoạt động trên Windows, macOS và Linux.
- Cung cấp khả năng đồng bộ hóa giữa các thiết bị.

##### b. Hiệu suất cao và nhẹ
- Tốc độ khởi động nhanh, không tiêu tốn quá nhiều tài nguyên hệ thống.
- Hỗ trợ mở các dự án lớn mà không bị chậm.

##### c. Kho tiện ích mở rộng phong phú
- Cho phép cài đặt nhiều extensions để hỗ trợ ngôn ngữ lập trình, công cụ debug, AI hỗ trợ code, v.v.
- Một số tiện ích phổ biến: C/C++ Extension Pack, CPH, Markdown All in One, Markdown Preview Enhanced,...

##### d. IntelliSense - Gợi ý mã thông minh
- Hỗ trợ gợi ý cú pháp thông minh giúp lập trình nhanh và chính xác hơn.
- Có thể mở rộng với các extensions chuyên biệt cho từng ngôn ngữ.

##### e. Terminal tích hợp
- Giúp chạy lệnh trực tiếp mà không cần mở terminal bên ngoài.

#### 3. Sử dụng VS Code
##### a. Một số kiến thức cơ bản
- Có thể dùng ctrl + N như DevC, code và ctrl + S để lưu file nhưng không khuyến khích lắm => nên tạo một folder để quản lý
- Có dấu chấm trắng xuất hiện ở cuối của tên file có nghĩa là có một thay đổi gì đấy chưa được lưu.
![alt text](Image/Chưa_lưu_file.png)
- Có thể tìm hiểu thêm auto save (không khuyến khích dùng lắm nếu chỉ code thuật toán).
- Chỉnh themes, size chữ (hướng dẫn qua các em tuỳ chỉnh cho phù hợp, đặc biệt là về size chữ).

##### a. IntelliSense trong VS Code
IntelliSense là một tính năng hỗ trợ lập trình viên trong VS Code. Nó giúp tự động gợi ý code, giảm thiểu lỗi cú pháp, tăng tốc độ lập trình và cải thiện năng suất làm việc.

Nhưng chỉ có một số ngôn ngữ được hỗ trợ mặc định IntelliSense trong VS Code như:
- JavaScript
- TypeScript
- JSON
- CSS, SCSS, Less
- HTML

Còn đối với các ngôn ngữ khác thì phải tự cài thêm extension (đối với C/C++ )


##### b. Một số phím tắt trong VS Code (Phần này có thể cap màn hình gửi luôn cho các em, chú ý thực hành)
- **Ctrl + /**: comment hoặc huỷ comment nhanh
- **Alt + Up/Down**: chuyển một hoặc nhiều dòng code lên hoặc xuống
- **Ctrl + Alt + Up/Down**: Chọn nhiều dòng từ tâm điểm ban đầu
- **F2**: Thay đổi tên biến nhanh. Đặt con trỏ chuột vào biến cần thay đổi và ấn F2 (chú ý không tô đậm, chỉ đặt con trỏ chuột).
- **Shift + Alt + F**: format document. Format nhanh toàn bộ file code
  - Mặc định thì sẽ sắp xếp dấu `{` theo kiểu `Allman` (`{` xuống dòng mới)
  - Nếu muốn đổi thành kiểu `Attach` (`{` cùng một dòng với câu lệnh)
  - Thì tìm hiểu thêm về clang-format

##### c. Giới thiệu một số extension thường dùng
- C/C++ Extension Pack
- CPH (nói luôn về file input, output)
![alt text](Image/Input_Output.png)
- Markdown All in One
- Markdown Preview Enhanced
- ...

### III. Debug trong VS Code


### IV. Markdown & GitHub cơ bản
- Hướng dẫn viết markdown cơ bản: https://www.youtube.com/watch?v=zunwTq3QC-Q&t=958s&ab_channel=CodeLearnShare
- Sử lỗi không gõ được tiếng Việt trong file markdown: https://www.youtube.com/watch?v=tTheRJ9R1cY&ab_channel=EnglishandDeveloper%28ENADEV%29
#### 1. Giới thiệu Markdown
- Markdown là gì? (Ngôn ngữ đánh dấu đơn giản giúp soạn thảo văn bản nhanh chóng và dễ đọc. Cực kỳ tiện lợi để soạn các tài liệu kỹ thuật)
- Ứng dụng của Markdown:
  - Viết tài liệu kỹ thuật, blog.
  - Soạn thảo ghi chú và bài viết khoa học.
- Các công cụ phổ biến hỗ trợ Markdown: VS Code, Typora, Obsidian, GitHub.

#### 2. Cú pháp cơ bản
##### a. Tiêu đề
- `# Tiêu đề cấp 1`
- `## Tiêu đề cấp 2`
- `### Tiêu đề cấp 3`

##### b. Định dạng văn bản
- **Chữ đậm**: `**chữ đậm**`
- *Chữ nghiêng*: `*chữ nghiêng*`
- ~~Chữ gạch ngang~~: `~~chữ gạch ngang~~`

##### c. Danh sách
- **Danh sách không thứ tự**:
  ```markdown
  - Mục 1
  - Mục 2
  - Mục 3
  ```
- **Danh sách có thứ tự**:
  ```markdown
  1. Bước 1
  2. Bước 2
  3. Bước 3
  ```

##### d. Chèn liên kết & hình ảnh
Dùng ctrl + shift + p

##### e. Đoạn mã nguồn (Code Block)
- Inline Code: `` `code` ``
- Code Block:
  ```python
  print("Hello, World!")
  ```

##### f. Trích dẫn
```markdown
> Đây là một đoạn trích dẫn.
```

##### g. Bảng
```markdown
| Cột 1  | Cột 2  | Cột 3  |
| ------ | ------ | ------ |
| Hàng 1 | Hàng 2 | Hàng 3 |
```

#### 3. Cú pháp nâng cao
- **Table of content**
- **Task List**:
  ```markdown
  - [x] Hoàn thành bài tập 1
  - [ ] Hoàn thành bài tập 2
  ```
  - [x] Hoàn thành bài tập 1
  - [ ] Hoàn thành bài tập 2
- **Biểu thức toán học (Dùng latex, chỉ cần giới thiệu qua vì tạm thời chưa cần)**:
  ```markdown
  $$E = mc^2$$
  ```
  $$E = mc^2$$

#### 4. GitHub 
- Hướng dẫn tại repo tài liệu
- Hướng dẫn up, remove tài liệu bằng UI và kéo thả file.
