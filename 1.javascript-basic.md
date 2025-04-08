# Câu hỏi phỏng vấn JavaScript cho Intern

## 1. Kiến thức cơ bản về JavaScript

**Interviewer**: Em hãy giải thích JavaScript là gì và tại sao nó lại quan trọng trong phát triển web?

**Candidate**: Dạ, JavaScript là một ngôn ngữ lập trình được sử dụng chủ yếu để tạo ra các tương tác động trên trang web. Em nghĩ JavaScript rất quan trọng vì nó cho phép chúng ta tạo ra các trang web có khả năng tương tác với người dùng mà không cần tải lại trang. Ví dụ như khi em click vào một nút, JavaScript có thể thay đổi nội dung trang web ngay lập tức mà không cần refresh lại trang.

**Interviewer**: Vậy em có thể kể về các kiểu dữ liệu trong JavaScript không?

**Candidate**: Dạ, trong JavaScript có 7 kiểu dữ liệu cơ bản ạ. Đầu tiên là kiểu nguyên thủy (primitive) gồm: String (chuỗi), Number (số), Boolean (true/false), Undefined (chưa được gán giá trị), Null (giá trị rỗng), Symbol (tạo ra giá trị duy nhất), và BigInt (số nguyên lớn). Ngoài ra còn có kiểu Object (đối tượng) là kiểu dữ liệu tham chiếu. Em thường hay sử dụng String, Number, Boolean và Object trong các dự án của em.

**Interviewer**: Em có thể giải thích sự khác biệt giữa var, let và const không?

**Candidate**: Dạ, em sẽ giải thích từng cái ạ. `var` là cách khai báo biến cũ nhất, có phạm vi function-scoped và có thể khai báo lại. `let` và `const` được giới thiệu từ ES6, có phạm vi block-scoped. Sự khác biệt chính là `let` có thể gán lại giá trị, còn `const` thì không. Em thường dùng `const` cho các giá trị không thay đổi và `let` cho các biến cần thay đổi giá trị.

**Interviewer**: Em có thể giải thích về hoisting trong JavaScript không?

**Candidate**: Dạ, hoisting là cơ chế trong JavaScript cho phép di chuyển khai báo biến và hàm lên trên cùng phạm vi của chúng. Với `var`, biến được hoisted và được gán giá trị `undefined`. Với `let` và `const`, biến cũng được hoisted nhưng không được khởi tạo giá trị, tạo ra "Temporal Dead Zone". Em thường cẩn thận với hoisting để tránh các lỗi không mong muốn trong code.

**Interviewer**: Em có thể giải thích về closure trong JavaScript không?

**Candidate**: Dạ, closure là một hàm có thể truy cập các biến ở phạm vi bên ngoài của nó. Em thấy closure rất hữu ích trong việc tạo ra các hàm private và quản lý state. Ví dụ như khi em làm việc với event handlers, em thường dùng closure để truy cập các biến từ component cha.

## 2. DOM và Events

**Interviewer**: Em có thể giải thích về DOM là gì không?

**Candidate**: Dạ, DOM (Document Object Model) là một cấu trúc dữ liệu đại diện cho tài liệu HTML dưới dạng cây các node. Mỗi phần tử HTML là một node trong DOM. Em thường dùng DOM để thao tác với các phần tử HTML, thêm/xóa/sửa nội dung và style của trang web.

**Interviewer**: Em có thể kể về các phương thức chính để thao tác với DOM không?

**Candidate**: Dạ, em thường dùng các phương thức như `getElementById()`, `querySelector()`, `querySelectorAll()` để lấy phần tử. Để thêm/xóa phần tử thì dùng `appendChild()`, `removeChild()`, `createElement()`. Để thay đổi nội dung thì dùng `innerHTML`, `textContent`. Em cũng hay dùng `classList` để thao tác với CSS classes.

**Interviewer**: Em có thể giải thích về event bubbling và event capturing không?

**Candidate**: Dạ, event bubbling là khi một sự kiện xảy ra trên một phần tử, nó sẽ "nổi bọt" lên các phần tử cha. Ngược lại, event capturing là khi sự kiện đi từ phần tử cha xuống phần tử con. Em thường dùng `stopPropagation()` để ngăn sự kiện lan truyền khi cần thiết.

**Interviewer**: Em có thể kể về các event listener phổ biến không?

**Candidate**: Dạ, em thường dùng các event như `click`, `submit`, `change`, `input`, `keydown`, `mouseover`, `mouseout`. Em cũng hay dùng `addEventListener()` để thêm các event handler. Em thấy quan trọng là phải nhớ remove event listener khi không cần thiết để tránh memory leak.

**Interviewer**: Em có thể giải thích về event delegation không?

**Candidate**: Dạ, event delegation là kỹ thuật lắng nghe sự kiện trên phần tử cha thay vì từng phần tử con. Em thấy nó rất hữu ích khi làm việc với nhiều phần tử động. Ví dụ như khi em làm danh sách có thể thêm/xóa items, em chỉ cần lắng nghe sự kiện trên phần tử cha.

## 3. Asynchronous JavaScript

**Interviewer**: Em có thể giải thích về callback là gì không?

**Candidate**: Dạ, callback là một hàm được truyền vào một hàm khác như một tham số và được thực thi sau khi hàm chính hoàn thành. Em thường dùng callback để xử lý các tác vụ bất đồng bộ. Tuy nhiên, em thấy callback có thể gây ra "callback hell" khi có nhiều tác vụ lồng nhau.

**Interviewer**: Em có thể giải thích về Promise không?

**Candidate**: Dạ, Promise là một đối tượng đại diện cho một tác vụ bất đồng bộ có thể hoàn thành hoặc thất bại. Em thường dùng Promise với `then()` và `catch()` để xử lý kết quả. Em cũng hay dùng `Promise.all()` khi cần chạy nhiều Promise cùng lúc.

**Interviewer**: Em có thể giải thích về async/await không?

**Candidate**: Dạ, async/await là cú pháp mới giúp code bất đồng bộ dễ đọc hơn. Em thấy nó giống như viết code đồng bộ vậy. Em thường dùng `try/catch` với async/await để xử lý lỗi. Em cũng thích dùng async/await hơn Promise vì code dễ đọc và bảo trì hơn.

**Interviewer**: Em có thể giải thích về setTimeout và setInterval không?

**Candidate**: Dạ, `setTimeout` thực thi một hàm sau một khoảng thời gian nhất định, còn `setInterval` thực thi một hàm lặp lại sau một khoảng thời gian. Em thường dùng chúng để tạo animation, delay, hoặc polling. Em cũng nhớ clear timeout/interval khi không cần thiết nữa.

**Interviewer**: Em có thể giải thích về AJAX không?

**Candidate**: Dạ, AJAX (Asynchronous JavaScript and XML) là kỹ thuật gửi và nhận dữ liệu từ server mà không cần tải lại trang. Em thường dùng `fetch` API hoặc `axios` để thực hiện AJAX requests. Em cũng hay dùng async/await với fetch để code dễ đọc hơn.

## 4. ES6+ Features

**Interviewer**: Em có thể kể về các tính năng mới trong ES6 không?

**Candidate**: Dạ, ES6 có nhiều tính năng hay như arrow functions, template literals, destructuring, spread/rest operators, classes. Em thích dùng arrow functions vì cú pháp ngắn gọn và không bị ràng buộc bởi `this`. Em cũng hay dùng destructuring để code gọn gàng hơn.

**Interviewer**: Em có thể giải thích về arrow functions không?

**Candidate**: Dạ, arrow functions là cú pháp viết hàm ngắn gọn hơn. Em thích dùng nó vì không cần từ khóa `function` và `return`. Tuy nhiên, em cũng biết là arrow functions không có `this` riêng, nên em cẩn thận khi dùng trong các phương thức của object.

**Interviewer**: Em có thể giải thích về template literals không?

**Candidate**: Dạ, template literals cho phép em viết chuỗi nhiều dòng và nhúng biểu thức vào chuỗi bằng `${}`. Em thường dùng nó để tạo HTML strings hoặc các message động. Em thấy nó dễ đọc hơn cách nối chuỗi thông thường.

**Interviewer**: Em có thể giải thích về destructuring không?

**Candidate**: Dạ, destructuring là cách lấy giá trị từ arrays hoặc objects một cách ngắn gọn. Em thường dùng nó để lấy props từ React components hoặc parameters từ functions. Em cũng hay dùng default values với destructuring.

**Interviewer**: Em có thể giải thích về spread/rest operators không?

**Candidate**: Dạ, spread operator (`...`) dùng để mở rộng arrays hoặc objects, còn rest operator dùng để gom nhóm các tham số còn lại. Em thường dùng spread để copy arrays/objects, merge objects, hoặc truyền props trong React.

## 5. Error Handling và Debugging

**Interviewer**: Em có thể giải thích về try-catch không?

**Candidate**: Dạ, try-catch dùng để bắt và xử lý lỗi trong JavaScript. Em thường dùng nó với async/await hoặc khi làm việc với các API bên ngoài. Em cũng hay log lỗi ra console để debug.

**Interviewer**: Em có thể kể về các cách debug JavaScript không?

**Candidate**: Dạ, em thường dùng `console.log()` để in ra giá trị biến. Em cũng hay dùng debugger trong DevTools, breakpoints, và console.table() để xem dữ liệu dạng bảng. Em cũng biết dùng source maps để debug code đã được minify.

**Interviewer**: Em có thể giải thích về Error objects không?

**Candidate**: Dạ, Error objects là các đối tượng đại diện cho lỗi trong JavaScript. Em thường dùng `throw new Error()` để tạo lỗi tùy chỉnh. Em cũng biết về các loại Error khác như TypeError, ReferenceError, SyntaxError.

**Interviewer**: Em có thể giải thích về window.onerror không?

**Candidate**: Dạ, window.onerror là một event handler toàn cục để bắt các lỗi chưa được xử lý. Em thường dùng nó để log lỗi về server hoặc hiển thị thông báo lỗi thân thiện với người dùng. Em cũng biết về window.onunhandledrejection để bắt lỗi Promise.

**Interviewer**: Em có thể giải thích về source maps không?

**Candidate**: Dạ, source maps là file map giữa code đã được minify và code gốc. Em thường dùng nó trong development để debug code dễ dàng hơn. Em cũng biết cấu hình source maps trong webpack hoặc các bundler khác.

## 6. Best Practices và Performance

**Interviewer**: Em có thể kể về các best practices trong JavaScript không?

**Candidate**: Dạ, em thường tuân thủ các quy tắc như sử dụng const/let thay vì var, viết code có thể đọc được, đặt tên biến/hàm có ý nghĩa, comment code khi cần thiết. Em cũng hay dùng ESLint để đảm bảo code chất lượng.

**Interviewer**: Em có thể giải thích về cách tối ưu performance trong JavaScript không?

**Candidate**: Dạ, em thường tối ưu bằng cách tránh vòng lặp lồng nhau, sử dụng caching, lazy loading, debounce/throttle cho các event handlers. Em cũng biết về memory leaks và cách tránh chúng.

**Interviewer**: Em có thể giải thích về garbage collection không?

**Candidate**: Dạ, garbage collection là cơ chế tự động giải phóng bộ nhớ không còn được sử dụng. Em biết về reference counting và mark-and-sweep algorithm. Em cũng cẩn thận với memory leaks từ closures và event listeners.

**Interviewer**: Em có thể giải thích về debounce và throttle không?

**Candidate**: Dạ, debounce trì hoãn việc thực thi hàm cho đến khi người dùng ngừng thực hiện hành động, còn throttle giới hạn số lần hàm được gọi trong một khoảng thời gian. Em thường dùng chúng cho các event như scroll, resize, input.

**Interviewer**: Em có thể giải thích về code splitting không?

**Candidate**: Dạ, code splitting là kỹ thuật chia nhỏ bundle thành các chunks nhỏ hơn. Em thường dùng dynamic import() hoặc React.lazy() để lazy load components. Em cũng biết cấu hình code splitting trong webpack.

## 7. Testing và Debugging

**Interviewer**: Em có thể kể về các loại testing trong JavaScript không?

**Candidate**: Dạ, em biết về unit testing, integration testing, và end-to-end testing. Em thường dùng Jest cho unit testing và React Testing Library cho component testing. Em cũng biết viết test cases và sử dụng các assertion methods.

**Interviewer**: Em có thể giải thích về Jest không?

**Candidate**: Dạ, Jest là một testing framework phổ biến cho JavaScript. Em thường dùng nó để viết unit tests, mock functions, và test async code. Em cũng biết về test coverage và cách đọc báo cáo coverage.

**Interviewer**: Em có thể giải thích về mocking trong testing không?

**Candidate**: Dạ, mocking là kỹ thuật tạo ra các phiên bản giả của dependencies để test. Em thường dùng Jest.mock() để mock modules, functions, hoặc API calls. Em cũng biết về spyOn để theo dõi method calls.

**Interviewer**: Em có thể giải thích về test coverage không?

**Candidate**: Dạ, test coverage đo lường phần code được test. Em thường dùng Jest với Istanbul để tạo báo cáo coverage. Em cũng biết về các loại coverage như statement, branch, function, và line coverage.

**Interviewer**: Em có thể giải thích về debugging tools không?

**Candidate**: Dạ, em thường dùng Chrome DevTools để debug. Em biết về các tab như Elements, Console, Sources, Network. Em cũng hay dùng breakpoints, watch expressions, và call stack để debug.

## 8. Security

**Interviewer**: Em có thể kể về các vấn đề bảo mật phổ biến trong JavaScript không?

**Candidate**: Dạ, em biết về XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery), và SQL Injection. Em thường escape user input, sử dụng HTTPS, và validate dữ liệu để phòng chống các tấn công này.

**Interviewer**: Em có thể giải thích về XSS không?

**Candidate**: Dạ, XSS là lỗ hổng cho phép attacker chèn mã JavaScript độc hại vào trang web. Em thường dùng các thư viện như DOMPurify để sanitize input, và tránh sử dụng innerHTML với user input.

**Interviewer**: Em có thể giải thích về CORS không?

**Candidate**: Dạ, CORS (Cross-Origin Resource Sharing) là cơ chế cho phép truy cập tài nguyên từ domain khác. Em biết về các headers như Access-Control-Allow-Origin và cách cấu hình CORS trên server.

**Interviewer**: Em có thể giải thích về Content Security Policy không?

**Candidate**: Dạ, CSP là một lớp bảo mật bổ sung giúp ngăn chặn XSS và các tấn công khác. Em biết về các directives như default-src, script-src, và cách cấu hình CSP trong HTTP headers.

**Interviewer**: Em có thể giải thích về cách bảo vệ API endpoints không?

**Candidate**: Dạ, em thường sử dụng authentication (JWT), rate limiting, và input validation để bảo vệ API. Em cũng biết về HTTPS và cách xử lý sensitive data an toàn.
