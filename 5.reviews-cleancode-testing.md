# Phỏng vấn về Clean Code, Làm việc nhóm và Testing

## 1. Clean Code và Coding Standards

**Interviewer**: Em có thể giải thích thế nào là clean code và tại sao nó quan trọng không?

**Candidate**: Dạ, clean code là code dễ đọc, dễ hiểu và dễ bảo trì. Nó tuân thủ các nguyên tắc và quy ước đặt tên rõ ràng, có cấu trúc tốt, và được viết một cách đơn giản. Clean code quan trọng vì nó giúp team dễ dàng làm việc cùng nhau, giảm thiểu lỗi, và tiết kiệm thời gian bảo trì trong tương lai.

**Interviewer**: Em thường làm gì để đảm bảo code của mình sạch sẽ và dễ đọc?

**Candidate**: Dạ, em thường áp dụng các nguyên tắc sau:

1. Đặt tên biến, hàm, class rõ ràng và có ý nghĩa
2. Viết comment giải thích cho code phức tạp
3. Chia nhỏ các hàm để mỗi hàm chỉ làm một việc
4. Sử dụng các quy ước code style nhất quán
5. Thường xuyên refactor code để cải thiện cấu trúc

**Interviewer**: Em có thể cho ví dụ về cách em đặt tên biến và hàm theo chuẩn clean code không?

**Candidate**: Dạ, em thường đặt tên theo các nguyên tắc sau:

1. Tên biến mô tả rõ nội dung: `userList` thay vì `list`, `totalPrice` thay vì `total`
2. Tên hàm bắt đầu bằng động từ: `calculateTotal()`, `getUserById()`, `updateProfile()`
3. Tên class là danh từ: `UserService`, `ProductController`, `OrderRepository`
4. Tên hằng số viết hoa: `MAX_RETRY_COUNT`, `DEFAULT_TIMEOUT`
5. Tên boolean bắt đầu bằng is/has/should: `isValid`, `hasPermission`, `shouldUpdate`

## 2. Làm việc nhóm và Code Review

**Interviewer**: Em đã từng tham gia code review chưa? Em thường chú ý những điểm gì khi review code?

**Candidate**: Dạ, em đã tham gia code review và thường chú ý các điểm sau:

1. Code có tuân thủ coding standards không
2. Có lỗi logic hoặc bug tiềm ẩn không
3. Có test cases đầy đủ không
4. Có thể tối ưu hoặc cải thiện gì không
5. Documentation có đầy đủ và rõ ràng không

**Interviewer**: Em làm gì khi nhận được feedback từ code review?

**Candidate**: Dạ, em thường:

1. Đọc kỹ và hiểu rõ feedback
2. Trao đổi với reviewer nếu có điểm chưa rõ
3. Sửa code theo feedback một cách c careful
4. Chạy lại tests để đảm bảo không có lỗi mới
5. Gửi lại để review tiếp nếu cần

**Interviewer**: Em làm thế nào để làm việc hiệu quả trong team?

**Candidate**: Dạ, em thường:

1. Giao tiếp rõ ràng và thường xuyên với team
2. Cập nhật tiến độ công việc đều đặn
3. Chia sẻ kiến thức và giúp đỡ đồng nghiệp
4. Tuân thủ các quy trình làm việc của team
5. Chủ động báo cáo vấn đề và đề xuất giải pháp

## 3. Testing cơ bản

**Interviewer**: Em có thể giải thích các loại testing cơ bản không?

**Candidate**: Dạ, có các loại testing cơ bản sau:

1. Unit Testing: Kiểm tra từng hàm/class riêng lẻ
2. Integration Testing: Kiểm tra tương tác giữa các thành phần
3. Functional Testing: Kiểm tra chức năng của hệ thống
4. UI Testing: Kiểm tra giao diện người dùng
5. Performance Testing: Kiểm tra hiệu năng hệ thống

**Interviewer**: Em đã viết unit test chưa? Em thường test những gì?

**Candidate**: Dạ, em đã viết unit test và thường test:

1. Các hàm xử lý logic nghiệp vụ
2. Các hàm tính toán
3. Các hàm validate dữ liệu
4. Các hàm xử lý lỗi
5. Các hàm utility

**Interviewer**: Em làm gì khi phát hiện bug trong quá trình testing?

**Candidate**: Dạ, khi phát hiện bug, em thường:

1. Ghi lại các bước để tái hiện bug
2. Phân tích nguyên nhân gây ra bug
3. Viết test case để capture bug
4. Sửa code và chạy lại tests
5. Báo cáo cho team nếu là bug nghiêm trọng

## 4. Version Control và Git

**Interviewer**: Em sử dụng Git như thế nào trong dự án?

**Candidate**: Dạ, em thường:

1. Tạo branch mới cho mỗi tính năng/bug fix
2. Commit code thường xuyên với message rõ ràng
3. Pull code mới nhất từ main branch trước khi làm việc
4. Tạo pull request để review code
5. Merge code sau khi được approve

**Interviewer**: Em làm gì khi có conflict trong Git?

**Candidate**: Dạ, khi có conflict, em thường:

1. Pull code mới nhất từ main branch
2. Kiểm tra các file có conflict
3. Giải quyết conflict một cách cẩn thận
4. Chạy tests để đảm bảo không có lỗi
5. Commit và push code đã sửa

## 5. Debugging và Problem Solving

**Interviewer**: Em thường làm gì khi gặp lỗi trong code?

**Candidate**: Dạ, em thường:

1. Đọc kỹ thông báo lỗi
2. Sử dụng console.log hoặc debugger để theo dõi luồng code
3. Kiểm tra input và output của các hàm
4. Tìm kiếm giải pháp trên internet
5. Hỏi đồng nghiệp nếu không tự giải quyết được

**Interviewer**: Em làm thế nào để giải quyết vấn đề phức tạp?

**Candidate**: Dạ, em thường:

1. Phân tích vấn đề thành các phần nhỏ hơn
2. Viết ra các bước cần thực hiện
3. Thử nghiệm từng giải pháp
4. Tham khảo tài liệu và kinh nghiệm của team
5. Ghi lại cách giải quyết để học hỏi

## 6. Git và GitHub nâng cao

**Interviewer**: Em có thể giải thích sự khác biệt giữa Git và GitHub không?

**Candidate**: Dạ, Git là một hệ thống quản lý phiên bản phân tán (distributed version control system) chạy trên máy local, trong khi GitHub là một dịch vụ lưu trữ code dựa trên Git, cung cấp giao diện web và nhiều tính năng bổ sung như:

1. Lưu trữ code trên cloud
2. Pull requests và code review
3. Issues tracking
4. Actions (CI/CD)
5. Wiki và documentation

**Interviewer**: Em đã sử dụng các tính năng nâng cao của Git chưa? Ví dụ như rebase, cherry-pick?

**Candidate**: Dạ, em đã sử dụng một số tính năng nâng cao của Git:

1. **Rebase**: Em dùng để cập nhật branch của mình với code mới nhất từ main branch, giúp lịch sử commit sạch sẽ hơn
2. **Cherry-pick**: Em dùng để chọn và áp dụng một commit cụ thể từ branch khác
3. **Stash**: Em dùng để lưu tạm các thay đổi chưa commit khi cần chuyển sang làm việc khác
4. **Interactive rebase**: Em dùng để sửa lại lịch sử commit trước khi push
5. **Git hooks**: Em đã cấu hình pre-commit hook để chạy linter trước khi commit

**Interviewer**: Em làm gì để quản lý các branch trong dự án lớn?

**Candidate**: Dạ, em thường áp dụng chiến lược Git Flow hoặc một biến thể của nó:

1. **main/master**: Branch chính, luôn ở trạng thái ổn định
2. **develop**: Branch phát triển, tích hợp code từ các feature branch
3. **feature/\***: Các branch cho tính năng mới
4. **bugfix/\***: Các branch cho sửa lỗi
5. **release/\***: Các branch cho chuẩn bị release

Em cũng thường xuyên xóa các branch đã merge để giữ repository sạch sẽ.

## 7. Làm việc nhóm hiệu quả

**Interviewer**: Em làm thế nào để đảm bảo code của mình không ảnh hưởng đến code của người khác trong team?

**Candidate**: Dạ, em thường:

1. Luôn pull code mới nhất trước khi bắt đầu làm việc
2. Tạo branch riêng cho mỗi tính năng/bug fix
3. Commit code thường xuyên với message rõ ràng
4. Chạy tests trước khi push code
5. Tạo pull request sớm để team có thể review và góp ý

**Interviewer**: Em làm gì khi phát hiện vấn đề trong code của đồng nghiệp?

**Candidate**: Dạ, em thường:

1. Kiểm tra kỹ vấn đề trước khi báo cáo
2. Ghi lại các bước để tái hiện vấn đề
3. Đề xuất giải pháp nếu có thể
4. Trao đổi trực tiếp với đồng nghiệp một cách tế nhị
5. Nếu cần thiết, tạo issue trên GitHub để theo dõi

**Interviewer**: Em làm thế nào để học hỏi từ code của đồng nghiệp?

**Candidate**: Dạ, em thường:

1. Review code của đồng nghiệp một cách chủ động
2. Đặt câu hỏi về các phần code mình chưa hiểu rõ
3. Tham gia các buổi code review của team
4. Đọc documentation và comments trong code
5. Thảo luận về các best practices với team

**Interviewer**: Em làm gì để cải thiện quy trình làm việc của team?

**Candidate**: Dạ, em thường:

1. Đề xuất các công cụ và quy trình mới khi thấy cần thiết
2. Chia sẻ kiến thức và kinh nghiệm với team
3. Tự động hóa các công việc lặp đi lặp lại
4. Cập nhật documentation khi có thay đổi
5. Tham gia các buổi retrospective để đóng góp ý kiến

**Interviewer**: Em làm thế nào để đảm bảo mình luôn cập nhật với các thay đổi trong dự án?

**Candidate**: Dạ, em thường:

1. Tham gia đầy đủ các cuộc họp team
2. Đọc kỹ các thông báo và updates từ team lead
3. Review các pull requests của đồng nghiệp
4. Đọc changelog và release notes
5. Thường xuyên trao đổi với đồng nghiệp về tiến độ công việc
