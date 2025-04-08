# Câu hỏi phỏng vấn về React cho Intern

## 1. Kiến thức cơ bản về React

**Interviewer**: Em có thể giải thích React là gì và tại sao nó được sử dụng rộng rãi không?

**Candidate**: Dạ, React là một thư viện JavaScript được phát triển bởi Facebook để xây dựng giao diện người dùng. React được sử dụng rộng rãi vì nó cho phép xây dựng các ứng dụng web một cách hiệu quả thông qua việc sử dụng component-based architecture. React sử dụng Virtual DOM để tối ưu hiệu suất, chỉ cập nhật những phần cần thiết của DOM thực, giúp ứng dụng chạy nhanh hơn. Ngoài ra, React có cộng đồng lớn, nhiều tài nguyên học tập và thư viện hỗ trợ phong phú.

**Interviewer**: Em có thể giải thích về Virtual DOM trong React không?

**Candidate**: Dạ, Virtual DOM là một bản sao nhẹ của DOM thực, được lưu trữ trong bộ nhớ. Khi dữ liệu thay đổi, React sẽ tạo một Virtual DOM mới và so sánh với Virtual DOM cũ để xác định những thay đổi cần thiết. Sau đó, React chỉ cập nhật những phần thay đổi trong DOM thực, thay vì cập nhật toàn bộ DOM. Cách tiếp cận này giúp tăng hiệu suất vì thao tác với DOM thực rất tốn kém, trong khi thao tác với Virtual DOM nhanh hơn nhiều.

**Interviewer**: Em có thể giải thích về JSX và tại sao nó được sử dụng trong React không?

**Candidate**: Dạ, JSX là một cú pháp mở rộng cho JavaScript, cho phép viết mã HTML trong JavaScript. JSX giúp code dễ đọc và dễ bảo trì hơn vì nó trực quan hơn so với việc sử dụng React.createElement(). Ví dụ, thay vì viết `React.createElement('div', null, 'Hello World')`, ta có thể viết `<div>Hello World</div>`. JSX được chuyển đổi thành JavaScript thông qua Babel trong quá trình build. Mặc dù JSX không bắt buộc trong React, nhưng nó được khuyến nghị sử dụng vì tính dễ đọc và dễ bảo trì.

**Interviewer**: Em có thể giải thích về Component trong React không?

**Candidate**: Dạ, Component là các khối xây dựng cơ bản của ứng dụng React. Mỗi component là một phần độc lập, có thể tái sử dụng của giao diện người dùng. Có hai loại component chính: Function Component và Class Component. Function Component là các hàm JavaScript đơn giản nhận props và trả về React elements. Class Component là các class JavaScript mở rộng từ React.Component, có thể quản lý state và lifecycle methods. Hiện nay, Function Component với Hooks được khuyến nghị sử dụng hơn vì code ngắn gọn và dễ hiểu hơn.

**Interviewer**: Em có thể giải thích về Props trong React không?

**Candidate**: Dạ, Props (Properties) là cách để truyền dữ liệu từ component cha xuống component con. Props là read-only, nghĩa là component con không thể thay đổi props mà nó nhận được. Props có thể là bất kỳ kiểu dữ liệu nào: chuỗi, số, mảng, object, thậm chí là functions. Ví dụ, ta có thể truyền props như sau: `<User name="John" age={25} />`. Trong component con, ta có thể truy cập props thông qua tham số của function component hoặc this.props trong class component.

## 2. State và Lifecycle

**Interviewer**: Em có thể giải thích về State trong React không?

**Candidate**: Dạ, State là một object chứa dữ liệu có thể thay đổi trong component. Khác với props, state có thể thay đổi và khi state thay đổi, component sẽ render lại. Trong function component, state được quản lý bằng useState hook. Ví dụ: `const [count, setCount] = useState(0)`. Trong class component, state được khởi tạo trong constructor và thay đổi bằng phương thức setState(). State nên được sử dụng cho dữ liệu thay đổi theo thời gian, như form input, danh sách động, hoặc dữ liệu phụ thuộc vào tương tác người dùng.

**Interviewer**: Em có thể giải thích về Lifecycle Methods trong React không?

**Candidate**: Dạ, Lifecycle Methods là các phương thức được gọi ở các giai đoạn khác nhau trong vòng đời của một component. Trong class component, các lifecycle methods chính bao gồm: componentDidMount() (được gọi sau khi component được render lần đầu), componentDidUpdate() (được gọi sau khi component được cập nhật), và componentWillUnmount() (được gọi trước khi component bị hủy). Trong function component, chúng ta sử dụng useEffect hook để thay thế các lifecycle methods này. useEffect có thể mô phỏng componentDidMount, componentDidUpdate, và componentWillUnmount tùy thuộc vào dependencies array.

**Interviewer**: Em có thể giải thích về useEffect hook trong React không?

**Candidate**: Dạ, useEffect là một hook cho phép thực hiện side effects trong function components. Side effects có thể là các thao tác như gọi API, đăng ký event listeners, hoặc thao tác trực tiếp với DOM. useEffect nhận hai tham số: một function (effect) và một dependencies array. Effect sẽ chạy sau mỗi lần render. Nếu dependencies array rỗng, effect chỉ chạy một lần sau lần render đầu tiên (tương tự componentDidMount). Nếu dependencies array có giá trị, effect sẽ chạy lại khi bất kỳ giá trị nào trong array thay đổi. Nếu không có dependencies array, effect sẽ chạy sau mỗi lần render. Effect có thể trả về một cleanup function, tương tự componentWillUnmount.

**Interviewer**: Em có thể giải thích về cách quản lý state phức tạp trong React không?

**Candidate**: Dạ, để quản lý state phức tạp trong React, em thường sử dụng một số phương pháp. Đầu tiên, em cố gắng chia nhỏ state thành các phần nhỏ hơn và đặt chúng ở component phù hợp nhất. Nếu state cần được chia sẻ giữa nhiều component, em có thể sử dụng state lifting (đưa state lên component cha chung). Với state phức tạp hơn, em có thể sử dụng Context API hoặc các thư viện quản lý state như Redux, MobX, hoặc Zustand. Em cũng thường sử dụng useReducer hook cho state phức tạp trong function component, tương tự như Redux reducer.

**Interviewer**: Em có thể giải thích về sự khác biệt giữa state và props không?

**Candidate**: Dạ, có một số khác biệt quan trọng giữa state và props. Props được truyền từ component cha xuống component con và là read-only (không thể thay đổi). State được quản lý bên trong component và có thể thay đổi. Khi props thay đổi, component con sẽ render lại. Khi state thay đổi, component sẽ render lại. Props thường được sử dụng để truyền dữ liệu từ component cha xuống component con, trong khi state được sử dụng để quản lý dữ liệu thay đổi theo thời gian trong component. Một component có thể nhận props từ bên ngoài nhưng không thể thay đổi chúng, trong khi nó có thể thay đổi state của chính nó.

## 3. Hooks trong React

**Interviewer**: Em có thể giải thích về useState hook trong React không?

**Candidate**: Dạ, useState là một hook cơ bản trong React cho phép thêm state vào function components. useState nhận một giá trị ban đầu và trả về một mảng gồm hai phần tử: giá trị state hiện tại và một function để cập nhật state. Ví dụ: `const [count, setCount] = useState(0)`. Khi gọi setCount, React sẽ cập nhật state và render lại component. useState có thể được sử dụng nhiều lần trong một component để quản lý nhiều state khác nhau. Lưu ý rằng khi cập nhật state dựa trên state trước đó, ta nên sử dụng function form: `setCount(prevCount => prevCount + 1)`.

**Interviewer**: Em có thể giải thích về useContext hook trong React không?

**Candidate**: Dạ, useContext là một hook cho phép sử dụng Context API trong function components. Context API được sử dụng để truyền dữ liệu qua nhiều cấp component mà không cần truyền props qua từng cấp. useContext nhận một context object (được tạo bởi React.createContext) và trả về giá trị context hiện tại. Context thường được sử dụng cho dữ liệu toàn cục như theme, ngôn ngữ, hoặc thông tin người dùng. Để sử dụng context, ta cần tạo một context provider ở component cha và sử dụng useContext ở các component con.

**Interviewer**: Em có thể giải thích về useRef hook trong React không?

**Candidate**: Dạ, useRef là một hook cho phép tạo một mutable ref object. Ref object có thuộc tính current, có thể được gán bất kỳ giá trị nào. useRef thường được sử dụng để tham chiếu đến DOM elements, nhưng nó cũng có thể được sử dụng để lưu trữ bất kỳ giá trị nào mà ta muốn giữ nguyên giữa các lần render. Khác với state, khi ref thay đổi, component không render lại. useRef thường được sử dụng để truy cập DOM elements trực tiếp, lưu trữ các giá trị trước đó, hoặc lưu trữ các ID của timers/intervals.

**Interviewer**: Em có thể giải thích về useMemo và useCallback hooks trong React không?

**Candidate**: Dạ, useMemo và useCallback là các hooks tối ưu hiệu suất trong React. useMemo được sử dụng để ghi nhớ kết quả tính toán, tránh tính toán lại không cần thiết. Ví dụ: `const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b])`. useCallback được sử dụng để ghi nhớ function, tránh tạo lại function mới sau mỗi lần render. Ví dụ: `const memoizedCallback = useCallback(() => doSomething(a, b), [a, b])`. Cả hai hooks đều nhận một dependencies array, và chỉ tính toán lại khi bất kỳ giá trị nào trong array thay đổi. Các hooks này thường được sử dụng để tối ưu hiệu suất khi truyền props xuống các component con.

**Interviewer**: Em có thể giải thích về useReducer hook trong React không?

**Candidate**: Dạ, useReducer là một hook cho phép quản lý state phức tạp trong function components, tương tự như Redux. useReducer nhận một reducer function và giá trị ban đầu, trả về state hiện tại và một dispatch function. Reducer function nhận state hiện tại và action, trả về state mới. Ví dụ: `const [state, dispatch] = useReducer(reducer, initialState)`. useReducer thường được sử dụng khi logic cập nhật state phức tạp hoặc khi state có nhiều giá trị liên quan. Nó cũng hữu ích khi ta muốn tách logic cập nhật state ra khỏi component.

## 4. Routing và Data Fetching

**Interviewer**: Em có thể giải thích về React Router không?

**Candidate**: Dạ, React Router là một thư viện phổ biến để xử lý routing trong ứng dụng React. Nó cho phép tạo single-page applications với nhiều views khác nhau. React Router sử dụng các components như BrowserRouter, Routes, Route, Link, và Navigate. BrowserRouter bọc toàn bộ ứng dụng, Routes chứa các Route components, và Route định nghĩa mapping giữa URL và component. Link được sử dụng để điều hướng giữa các routes. React Router v6 đã giới thiệu nhiều tính năng mới như nested routes, relative paths, và data loading.

**Interviewer**: Em có thể giải thích về cách fetch dữ liệu trong React không?

**Candidate**: Dạ, có nhiều cách để fetch dữ liệu trong React. Trong function components, em thường sử dụng useEffect hook kết hợp với fetch API hoặc axios. Em thường tạo một state để lưu trữ dữ liệu và một state để quản lý trạng thái loading và error. Ví dụ:

```javascript
const [data, setData] = useState(null);
const [loading, setLoading] = useState(true);
const [error, setError] = useState(null);

useEffect(() => {
    const fetchData = async () => {
        try {
            const response = await fetch("https://api.example.com/data");
            const json = await response.json();
            setData(json);
            setLoading(false);
        } catch (error) {
            setError(error);
            setLoading(false);
        }
    };

    fetchData();
}, []);
```

Em cũng có thể sử dụng các thư viện như React Query hoặc SWR để quản lý data fetching hiệu quả hơn.

**Interviewer**: Em có thể giải thích về cách xử lý lỗi trong React không?

**Candidate**: Dạ, có nhiều cách để xử lý lỗi trong React. Đối với lỗi trong quá trình render, em có thể sử dụng Error Boundary, một component đặc biệt bắt lỗi trong cây component con của nó. Đối với lỗi trong data fetching, em thường sử dụng try-catch trong async functions. Em cũng có thể sử dụng các thư viện như React Query hoặc SWR, chúng cung cấp các tính năng xử lý lỗi tích hợp. Ngoài ra, em có thể sử dụng các thư viện như react-toastify để hiển thị thông báo lỗi cho người dùng. Em luôn cố gắng cung cấp thông tin lỗi hữu ích và các tùy chọn khắc phục cho người dùng.

**Interviewer**: Em có thể giải thích về cách tối ưu hiệu suất trong React không?

**Candidate**: Dạ, có nhiều cách để tối ưu hiệu suất trong React. Đầu tiên, em sử dụng React.memo để tránh render lại không cần thiết các components. Em cũng sử dụng useMemo và useCallback để ghi nhớ các giá trị và functions. Em cố gắng tránh các tính toán nặng trong render function và sử dụng virtualization cho danh sách dài. Em cũng sử dụng code splitting và lazy loading để giảm kích thước bundle ban đầu. Ngoài ra, em sử dụng React DevTools để phân tích hiệu suất và xác định các vấn đề về render. Em cũng cố gắng tối ưu các images và assets khác.

**Interviewer**: Em có thể giải thích về cách quản lý form trong React không?

**Candidate**: Dạ, có nhiều cách để quản lý form trong React. Với form đơn giản, em có thể sử dụng controlled components, nơi giá trị của input được quản lý bởi state của React. Em cũng có thể sử dụng uncontrolled components với useRef, nhưng ít phổ biến hơn. Với form phức tạp, em thường sử dụng các thư viện như Formik hoặc React Hook Form. Các thư viện này cung cấp nhiều tính năng như validation, error handling, và form submission. Em cũng sử dụng các thư viện validation như Yup hoặc Zod để xác thực dữ liệu form. Em luôn cố gắng cung cấp phản hồi ngay lập tức cho người dùng và xử lý các trường hợp lỗi một cách thân thiện.

## 5. State Management và Testing

**Interviewer**: Em có thể giải thích về Redux không?

**Candidate**: Dạ, Redux là một thư viện quản lý state phổ biến cho ứng dụng React. Redux tuân theo kiến trúc Flux và có ba nguyên tắc chính: single source of truth (state được lưu trữ trong một store duy nhất), state là read-only (chỉ có thể thay đổi thông qua actions), và changes được thực hiện bằng pure functions (reducers). Redux sử dụng các khái niệm như actions (mô tả những gì đã xảy ra), reducers (xác định cách state thay đổi), và store (lưu trữ state). Redux Toolkit là phiên bản hiện đại của Redux, cung cấp các utilities để giảm boilerplate code.

**Interviewer**: Em có thể giải thích về cách test trong React không?

**Candidate**: Dạ, có nhiều cách để test trong React. Em thường sử dụng Jest làm test runner và React Testing Library để test components. Em viết unit tests cho các functions và components riêng lẻ, và integration tests cho các tương tác giữa các components. Em sử dụng các methods như render, screen, fireEvent, và waitFor từ React Testing Library. Em cố gắng test behavior thay vì implementation, sử dụng các queries như getByRole, getByText, và getByTestId. Em cũng sử dụng MSW (Mock Service Worker) để mock API calls trong tests. Em tin rằng testing là một phần quan trọng của quy trình phát triển, giúp đảm bảo code hoạt động đúng và dễ bảo trì.

**Interviewer**: Em có thể giải thích về Context API trong React không?

**Candidate**: Dạ, Context API là một tính năng của React cho phép truyền dữ liệu qua nhiều cấp component mà không cần truyền props qua từng cấp. Context API sử dụng các components như Provider và Consumer. Provider component nhận một value prop và cung cấp giá trị này cho tất cả các components con. Consumer component có thể truy cập giá trị này thông qua useContext hook. Context thường được sử dụng cho dữ liệu toàn cục như theme, ngôn ngữ, hoặc thông tin người dùng. Context API là một giải pháp tốt cho state management đơn giản, nhưng có thể gây ra re-renders không cần thiết nếu không được sử dụng cẩn thận.

**Interviewer**: Em có thể giải thích về cách quản lý state trong ứng dụng lớn không?

**Candidate**: Dạ, trong ứng dụng lớn, em thường sử dụng kết hợp nhiều phương pháp quản lý state. Đối với state cục bộ, em sử dụng useState và useReducer. Đối với state được chia sẻ giữa một số components, em sử dụng Context API. Đối với state phức tạp và toàn cục, em sử dụng Redux hoặc các thư viện tương tự. Em cũng sử dụng các thư viện như React Query hoặc SWR để quản lý server state. Em cố gắng đặt state ở component phù hợp nhất và chỉ đưa state lên khi cần thiết. Em cũng sử dụng các patterns như container/presenter để tách logic khỏi UI.

**Interviewer**: Em có thể giải thích về cách tối ưu bundle size trong React không?

**Candidate**: Dạ, có nhiều cách để tối ưu bundle size trong React. Đầu tiên, em sử dụng code splitting và lazy loading để chia nhỏ bundle thành các chunks nhỏ hơn. Em sử dụng dynamic import với React.lazy và Suspense. Em cũng sử dụng tree shaking để loại bỏ code không sử dụng. Em cố gắng sử dụng các thư viện nhẹ và chỉ import những gì cần thiết. Em sử dụng các công cụ như webpack-bundle-analyzer để phân tích bundle size. Em cũng tối ưu các assets như images và fonts. Ngoài ra, em sử dụng các techniques như minification và compression để giảm kích thước bundle.

## 6. Best Practices và Advanced Topics

**Interviewer**: Em có thể giải thích về cách tổ chức code trong dự án React không?

**Candidate**: Dạ, em thường tổ chức code theo cấu trúc feature-based hoặc domain-based. Mỗi feature hoặc domain có thư mục riêng chứa các components, hooks, utils, và tests liên quan. Em cũng có thư mục shared cho các components và utilities được sử dụng trong nhiều features. Em sử dụng các conventions như đặt tên file theo PascalCase cho components và camelCase cho utilities. Em cố gắng giữ các components nhỏ và có một trách nhiệm duy nhất. Em cũng sử dụng các patterns như container/presenter để tách logic khỏi UI. Em tin rằng cấu trúc code rõ ràng giúp dự án dễ bảo trì và mở rộng.

**Interviewer**: Em có thể giải thích về cách xử lý authentication trong React không?

**Candidate**: Dạ, có nhiều cách để xử lý authentication trong React. Em thường sử dụng JWT (JSON Web Tokens) để lưu trữ thông tin đăng nhập. Em lưu token trong localStorage hoặc httpOnly cookie. Em sử dụng Context API để cung cấp thông tin authentication cho toàn bộ ứng dụng. Em cũng sử dụng các thư viện như Auth0 hoặc Firebase Authentication để xử lý authentication. Em cố gắng bảo vệ các routes cần authentication bằng cách sử dụng PrivateRoute component. Em cũng xử lý token expiration và refresh token. Em tin rằng bảo mật là một phần quan trọng của ứng dụng web.

**Interviewer**: Em có thể giải thích về cách tối ưu SEO trong React không?

**Candidate**: Dạ, để tối ưu SEO trong React, em sử dụng các techniques khác nhau. Đầu tiên, em sử dụng React Helmet để quản lý meta tags. Em cố gắng sử dụng semantic HTML và đảm bảo cấu trúc heading hợp lý. Em sử dụng server-side rendering (SSR) hoặc static site generation (SSG) với Next.js hoặc Gatsby để cải thiện SEO. Em cũng đảm bảo ứng dụng có thể hoạt động mà không cần JavaScript (progressive enhancement). Em sử dụng các công cụ như Lighthouse để kiểm tra SEO. Em cũng đảm bảo ứng dụng có sitemap.xml và robots.txt.

**Interviewer**: Em có thể giải thích về cách xử lý internationalization trong React không?

**Candidate**: Dạ, để xử lý internationalization trong React, em thường sử dụng các thư viện như react-i18next hoặc react-intl. Các thư viện này cung cấp các utilities để quản lý translations và định dạng ngày tháng, số, và tiền tệ theo locale. Em lưu trữ translations trong các file JSON hoặc YAML. Em sử dụng Context API để cung cấp locale cho toàn bộ ứng dụng. Em cũng xử lý các vấn đề như RTL (right-to-left) layout cho các ngôn ngữ như Arabic. Em tin rằng internationalization là một phần quan trọng của ứng dụng web toàn cầu.

**Interviewer**: Em có thể giải thích về cách tối ưu accessibility trong React không?

**Candidate**: Dạ, để tối ưu accessibility trong React, em tuân thủ các guidelines của WCAG (Web Content Accessibility Guidelines). Em sử dụng semantic HTML và ARIA attributes khi cần thiết. Em đảm bảo ứng dụng có thể hoạt động bằng bàn phím và screen readers. Em cố gắng cung cấp đủ contrast và text alternatives cho images. Em sử dụng các components như FocusTrap và SkipLink để cải thiện keyboard navigation. Em cũng sử dụng các công cụ như axe-core để kiểm tra accessibility. Em tin rằng accessibility không chỉ là một yêu cầu pháp lý mà còn là một phần quan trọng của trải nghiệm người dùng.

## 7. React Query và Data Management

**Interviewer**: Em có thể giải thích về React Query và tại sao nó được sử dụng rộng rãi không?

**Candidate**: Dạ, React Query là một thư viện quản lý state và data fetching cho React applications. Nó được sử dụng rộng rãi vì cung cấp nhiều tính năng mạnh mẽ như caching, background updates, và optimistic updates. React Query giúp quản lý server state một cách hiệu quả, tự động xử lý các trường hợp loading, error, và stale data. Nó cũng cung cấp các hooks như useQuery và useMutation để đơn giản hóa việc fetch và cập nhật dữ liệu. React Query giúp giảm boilerplate code và cải thiện trải nghiệm người dùng thông qua việc tự động cập nhật dữ liệu.

**Interviewer**: Em có thể giải thích về cách sử dụng useQuery hook trong React Query không?

**Candidate**: Dạ, useQuery là một hook cơ bản trong React Query để fetch dữ liệu. Hook này nhận một query key và một query function, trả về một object chứa data, isLoading, error, và các trạng thái khác. Ví dụ:

```javascript
const { data, isLoading, error } = useQuery("todos", fetchTodos);
```

Trong đó 'todos' là query key và fetchTodos là function để fetch dữ liệu. useQuery tự động xử lý caching, refetching, và error handling. Em cũng có thể cấu hình các options như staleTime, cacheTime, và refetchOnWindowFocus để tùy chỉnh behavior của query. Nếu cần fetch dữ liệu với parameters, em có thể sử dụng query key array: `useQuery(['todo', id], () => fetchTodo(id))`.

**Interviewer**: Em có thể giải thích về cách sử dụng useMutation hook trong React Query không?

**Candidate**: Dạ, useMutation được sử dụng để thực hiện các thao tác thay đổi dữ liệu như POST, PUT, DELETE. Hook này nhận một mutation function và trả về một object chứa mutate function và các trạng thái như isLoading, error. Ví dụ:

```javascript
const mutation = useMutation(addTodo, {
    onSuccess: () => {
        // Invalidate and refetch
        queryClient.invalidateQueries("todos");
    },
});
```

Em có thể gọi mutation bằng cách sử dụng mutate function: `mutation.mutate(newTodo)`. useMutation cung cấp các callbacks như onSuccess, onError, và onSettled để xử lý các trường hợp khác nhau. Em cũng có thể sử dụng optimistic updates để cập nhật UI ngay lập tức trước khi server phản hồi.

**Interviewer**: Em có thể giải thích về cách quản lý cache trong React Query không?

**Candidate**: Dạ, React Query cung cấp một hệ thống cache mạnh mẽ. Cache được quản lý dựa trên query key, và mỗi query key có thể có nhiều phiên bản dữ liệu khác nhau. Em có thể cấu hình staleTime để xác định thời gian dữ liệu được coi là fresh, và cacheTime để xác định thời gian dữ liệu được lưu trong cache. Em có thể invalidate cache bằng cách sử dụng queryClient.invalidateQueries(). React Query cũng hỗ trợ background refetching, tự động cập nhật dữ liệu khi window được focus hoặc network được reconnect. Em cũng có thể sử dụng prefetching để tải trước dữ liệu cho các routes sắp được truy cập.

**Interviewer**: Em có thể giải thích về cách xử lý error và loading states trong React Query không?

**Candidate**: Dạ, React Query cung cấp các trạng thái loading và error cho mỗi query và mutation. Em có thể sử dụng isLoading để kiểm tra trạng thái loading ban đầu, và isFetching để kiểm tra trạng thái loading cho các lần refetch. Đối với error handling, em có thể sử dụng error object, chứa thông tin chi tiết về lỗi. Em cũng có thể sử dụng các callbacks như onError để xử lý lỗi một cách toàn cục. React Query cũng cung cấp retry logic, cho phép tự động thử lại các queries thất bại. Em có thể cấu hình số lần retry và retry delay. Ngoài ra, em có thể sử dụng React Query DevTools để debug và theo dõi trạng thái của các queries và mutations.

## 8. Advanced React Hooks

**Interviewer**: Em có thể giải thích về custom hooks trong React không?

**Candidate**: Dạ, custom hooks là các functions bắt đầu bằng "use" cho phép tái sử dụng logic giữa các components. Custom hooks giúp tách logic phức tạp ra khỏi components, làm cho code dễ đọc và dễ bảo trì hơn. Ví dụ, em có thể tạo một custom hook để xử lý form logic:

```javascript
function useForm(initialValues) {
    const [values, setValues] = useState(initialValues);
    const [errors, setErrors] = useState({});

    const handleChange = (e) => {
        const { name, value } = e.target;
        setValues({ ...values, [name]: value });
    };

    const handleSubmit = (e) => {
        e.preventDefault();
        // Validation logic
        return values;
    };

    return { values, errors, handleChange, handleSubmit };
}
```

Sau đó em có thể sử dụng hook này trong nhiều components khác nhau. Custom hooks tuân theo các quy tắc của Hooks, chỉ có thể được gọi ở top level của function components hoặc custom hooks khác.

**Interviewer**: Em có thể giải thích về useLayoutEffect hook trong React không?

**Candidate**: Dạ, useLayoutEffect tương tự như useEffect, nhưng nó chạy đồng bộ ngay sau khi React thực hiện tất cả các thay đổi DOM, trước khi trình duyệt vẽ màn hình. Điều này có nghĩa là useLayoutEffect sẽ chạy trước khi người dùng nhìn thấy bất kỳ thay đổi nào trên màn hình. useLayoutEffect thường được sử dụng khi em cần đo lường DOM nodes hoặc thực hiện các thay đổi DOM cần thiết trước khi vẽ màn hình, như tránh hiệu ứng nhấp nháy. Ví dụ:

```javascript
function Tooltip({ children, position }) {
    const tooltipRef = useRef(null);

    useLayoutEffect(() => {
        if (tooltipRef.current) {
            const { top, left } = position;
            tooltipRef.current.style.top = `${top}px`;
            tooltipRef.current.style.left = `${left}px`;
        }
    }, [position]);

    return <div ref={tooltipRef}>{children}</div>;
}
```

Tuy nhiên, em nên sử dụng useEffect khi có thể, vì useLayoutEffect có thể chặn trình duyệt vẽ màn hình, gây ra hiệu suất kém.

**Interviewer**: Em có thể giải thích về useImperativeHandle hook trong React không?

**Candidate**: Dạ, useImperativeHandle là một hook cho phép tùy chỉnh giá trị được trả về từ ref. Hook này thường được sử dụng kết hợp với forwardRef để tùy chỉnh các methods và properties được expose ra bên ngoài từ một component con. Ví dụ:

```javascript
const FancyInput = forwardRef((props, ref) => {
    const inputRef = useRef();

    useImperativeHandle(ref, () => ({
        focus: () => {
            inputRef.current.focus();
        },
        clear: () => {
            inputRef.current.value = "";
        },
    }));

    return <input ref={inputRef} />;
});
```

Trong ví dụ này, component cha chỉ có thể truy cập các methods focus() và clear() thông qua ref, thay vì toàn bộ DOM node. useImperativeHandle giúp giảm thiểu việc expose quá nhiều implementation details ra bên ngoài, tuân theo nguyên tắc encapsulation.

**Interviewer**: Em có thể giải thích về useDebugValue hook trong React không?

**Candidate**: Dạ, useDebugValue là một hook đơn giản giúp hiển thị label cho custom hooks trong React DevTools. Hook này chỉ hoạt động trong React DevTools và không ảnh hưởng đến logic của ứng dụng. Ví dụ:

```javascript
function useWindowSize() {
    const [size, setSize] = useState({
        width: window.innerWidth,
        height: window.innerHeight,
    });

    useEffect(() => {
        const handleResize = () => {
            setSize({
                width: window.innerWidth,
                height: window.innerHeight,
            });
        };

        window.addEventListener("resize", handleResize);
        return () => window.removeEventListener("resize", handleResize);
    }, []);

    useDebugValue(`Window size: ${size.width}x${size.height}`);

    return size;
}
```

Khi sử dụng hook này trong React DevTools, em sẽ thấy label "Window size: 1920x1080" (hoặc kích thước hiện tại) bên cạnh hook, giúp dễ dàng debug và hiểu giá trị của hook.

**Interviewer**: Em có thể giải thích về cách tạo và sử dụng compound hooks trong React không?

**Candidate**: Dạ, compound hooks là một pattern cho phép tạo các hooks phức tạp bằng cách kết hợp nhiều hooks đơn giản. Pattern này giúp tái sử dụng logic và tạo ra các APIs linh hoạt. Ví dụ, em có thể tạo một compound hook để quản lý form với validation:

```javascript
function useFormField(initialValue = "") {
    const [value, setValue] = useState(initialValue);
    const [touched, setTouched] = useState(false);
    const [error, setError] = useState("");

    const handleChange = (e) => {
        setValue(e.target.value);
        setTouched(true);
    };

    const validate = (validator) => {
        if (touched) {
            setError(validator(value));
        }
        return !error;
    };

    return {
        value,
        touched,
        error,
        handleChange,
        validate,
    };
}

function useForm(fields) {
    const formFields = {};

    Object.keys(fields).forEach((fieldName) => {
        formFields[fieldName] = useFormField(fields[fieldName]);
    });

    const isValid = () => {
        return Object.values(formFields).every((field) => !field.error);
    };

    const getValues = () => {
        const values = {};
        Object.keys(formFields).forEach((fieldName) => {
            values[fieldName] = formFields[fieldName].value;
        });
        return values;
    };

    return {
        fields: formFields,
        isValid,
        getValues,
    };
}
```

Sau đó em có thể sử dụng compound hook này như sau:

```javascript
function LoginForm() {
    const { fields, isValid, getValues } = useForm({
        email: "",
        password: "",
    });

    const handleSubmit = (e) => {
        e.preventDefault();
        if (isValid()) {
            console.log(getValues());
        }
    };

    return (
        <form onSubmit={handleSubmit}>
            <input value={fields.email.value} onChange={fields.email.handleChange} />
            {fields.email.error && <span>{fields.email.error}</span>}

            <input
                type="password"
                value={fields.password.value}
                onChange={fields.password.handleChange}
            />
            {fields.password.error && <span>{fields.password.error}</span>}

            <button type="submit">Login</button>
        </form>
    );
}
```

Pattern này giúp tạo ra các hooks có tính module hóa cao, dễ tái sử dụng và dễ mở rộng.
