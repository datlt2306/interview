# Câu hỏi phỏng vấn Thuật toán cho Intern

## 1. Kiến thức cơ bản về Thuật toán

**Interviewer**: Em hãy giải thích thuật toán là gì và tại sao nó lại quan trọng trong lập trình?

**Candidate**: Dạ, thuật toán là một tập hợp các bước có thứ tự để giải quyết một vấn đề cụ thể. Em nghĩ thuật toán rất quan trọng vì nó giúp chúng ta giải quyết vấn đề một cách hiệu quả và có hệ thống. Ví dụ như khi em cần tìm kiếm một phần tử trong mảng, em có thể dùng thuật toán tìm kiếm nhị phân thay vì tìm kiếm tuyến tính để giảm thời gian thực thi.

**Interviewer**: Em có thể giải thích về độ phức tạp thời gian và không gian của thuật toán không?

**Candidate**: Dạ, độ phức tạp thời gian đo lường thời gian thực thi của thuật toán, thường được ký hiệu bằng Big O notation như O(1), O(log n), O(n), O(n²), O(2ⁿ). Độ phức tạp không gian đo lường bộ nhớ mà thuật toán sử dụng. Em thường phân tích cả hai yếu tố này để chọn thuật toán phù hợp. Ví dụ như khi làm việc với dữ liệu lớn, em ưu tiên thuật toán có độ phức tạp thời gian thấp hơn.

**Interviewer**: Em có thể giải thích về thuật toán đệ quy không?

**Candidate**: Dạ, đệ quy là phương pháp giải quyết vấn đề bằng cách chia nhỏ vấn đề thành các vấn đề con nhỏ hơn có cùng dạng. Em thường dùng đệ quy cho các bài toán như tính giai thừa, dãy Fibonacci, hoặc duyệt cây. Em cũng biết về điều kiện dừng (base case) và cách tránh đệ quy vô hạn.

**Interviewer**: Em có thể giải thích về thuật toán sắp xếp không?

**Candidate**: Dạ, em biết về các thuật toán sắp xếp phổ biến như Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, Quick Sort, và Heap Sort. Mỗi thuật toán có ưu và nhược điểm riêng. Em thường dùng Quick Sort cho dữ liệu lớn vì độ phức tạp trung bình O(n log n), và Insertion Sort cho dữ liệu nhỏ vì nó đơn giản và hiệu quả.

**Interviewer**: Em có thể giải thích về thuật toán tìm kiếm không?

**Candidate**: Dạ, em biết về các thuật toán tìm kiếm như Linear Search và Binary Search. Linear Search có độ phức tạp O(n) và có thể dùng cho mảng không sắp xếp. Binary Search có độ phức tạp O(log n) nhưng yêu cầu mảng phải được sắp xếp. Em thường dùng Binary Search khi làm việc với dữ liệu lớn đã sắp xếp.

## 2. Cấu trúc dữ liệu cơ bản

**Interviewer**: Em có thể giải thích về mảng (Array) không?

**Candidate**: Dạ, mảng là cấu trúc dữ liệu lưu trữ các phần tử cùng kiểu dữ liệu trong bộ nhớ liên tiếp. Em thường dùng mảng khi biết trước kích thước dữ liệu. Em cũng biết về mảng động (ArrayList) cho phép thay đổi kích thước. Em thấy mảng có ưu điểm là truy cập nhanh O(1) nhưng chèn/xóa chậm O(n).

**Interviewer**: Em có thể giải thích về danh sách liên kết (Linked List) không?

**Candidate**: Dạ, danh sách liên kết là cấu trúc dữ liệu gồm các node, mỗi node chứa dữ liệu và con trỏ đến node tiếp theo. Em thường dùng nó khi cần chèn/xóa nhanh O(1). Em cũng biết về danh sách liên kết đơn, đôi, và vòng. Em thấy nhược điểm của nó là truy cập chậm O(n) và tốn bộ nhớ cho con trỏ.

**Interviewer**: Em có thể giải thích về ngăn xếp (Stack) không?

**Candidate**: Dạ, ngăn xếp là cấu trúc dữ liệu LIFO (Last In First Out). Em thường dùng nó cho các bài toán như kiểm tra dấu ngoặc, tính toán biểu thức, và quay lui (backtracking). Em cũng biết về các thao tác push, pop, peek với độ phức tạp O(1).

**Interviewer**: Em có thể giải thích về hàng đợi (Queue) không?

**Candidate**: Dạ, hàng đợi là cấu trúc dữ liệu FIFO (First In First Out). Em thường dùng nó cho các bài toán như BFS, xử lý tác vụ, và buffer. Em cũng biết về hàng đợi ưu tiên (Priority Queue) và deque (double-ended queue). Em thấy các thao tác enqueue, dequeue có độ phức tạp O(1).

**Interviewer**: Em có thể giải thích về cây nhị phân (Binary Tree) không?

**Candidate**: Dạ, cây nhị phân là cấu trúc dữ liệu phân cấp, mỗi node có tối đa hai node con. Em thường dùng nó cho các bài toán như tìm kiếm, sắp xếp, và biểu diễn biểu thức. Em cũng biết về các cách duyệt cây: preorder, inorder, postorder, và level-order.

## 3. Thuật toán sắp xếp nâng cao

**Interviewer**: Em có thể giải thích về Merge Sort không?

**Candidate**: Dạ, Merge Sort là thuật toán sắp xếp chia để trị (divide and conquer). Em thích nó vì có độ phức tạp ổn định O(n log n) và là thuật toán sắp xếp ổn định (stable). Em cũng biết về cách tối ưu bộ nhớ và xử lý các trường hợp đặc biệt.

**Interviewer**: Em có thể giải thích về Quick Sort không?

**Candidate**: Dạ, Quick Sort cũng là thuật toán chia để trị, sử dụng pivot để chia mảng. Em thường dùng nó vì hiệu suất tốt trong thực tế. Em cũng biết về cách chọn pivot tốt và xử lý các trường hợp đặc biệt như mảng đã sắp xếp.

**Interviewer**: Em có thể giải thích về Heap Sort không?

**Candidate**: Dạ, Heap Sort sử dụng cấu trúc heap để sắp xếp. Em thích nó vì có độ phức tạp O(n log n) và sắp xếp tại chỗ (in-place). Em cũng biết về cách xây dựng heap và các thao tác heapify.

**Interviewer**: Em có thể giải thích về Counting Sort không?

**Candidate**: Dạ, Counting Sort là thuật toán sắp xếp không so sánh, phù hợp khi biết trước phạm vi giá trị. Em thường dùng nó cho dữ liệu có phạm vi nhỏ. Em cũng biết về các biến thể như Radix Sort và Bucket Sort.

**Interviewer**: Em có thể giải thích về Shell Sort không?

**Candidate**: Dạ, Shell Sort là cải tiến của Insertion Sort, sắp xếp các phần tử cách nhau một khoảng. Em thấy nó hiệu quả cho dữ liệu vừa và nhỏ. Em cũng biết về cách chọn khoảng (gap) tốt và phân tích độ phức tạp.

## 4. Thuật toán tìm kiếm nâng cao

**Interviewer**: Em có thể giải thích về thuật toán tìm kiếm nhị phân nâng cao không?

**Candidate**: Dạ, em biết về các biến thể của Binary Search như tìm phần tử đầu tiên/cuối cùng thỏa mãn điều kiện, tìm trong mảng xoay, và tìm trong khoảng. Em thường dùng nó cho các bài toán tìm kiếm trên dữ liệu đã sắp xếp.

**Interviewer**: Em có thể giải thích về thuật toán tìm kiếm theo chiều rộng (BFS) không?

**Candidate**: Dạ, BFS là thuật toán duyệt đồ thị theo từng lớp. Em thường dùng nó cho các bài toán tìm đường đi ngắn nhất và kiểm tra tính liên thông. Em cũng biết về cách cài đặt BFS bằng queue và xử lý các trường hợp đặc biệt.

**Interviewer**: Em có thể giải thích về thuật toán tìm kiếm theo chiều sâu (DFS) không?

**Candidate**: Dạ, DFS là thuật toán duyệt đồ thị theo chiều sâu. Em thường dùng nó cho các bài toán như tìm chu trình, tô màu đồ thị, và tìm thành phần liên thông. Em cũng biết về cách cài đặt DFS bằng đệ quy và stack.

**Interviewer**: Em có thể giải thích về thuật toán Dijkstra không?

**Candidate**: Dạ, Dijkstra là thuật toán tìm đường đi ngắn nhất từ một đỉnh đến các đỉnh khác trong đồ thị có trọng số không âm. Em thường dùng nó cho các bài toán về lộ trình và tối ưu hóa. Em cũng biết về cách cài đặt hiệu quả bằng priority queue.

**Interviewer**: Em có thể giải thích về thuật toán A\* không?

**Candidate**: Dạ, A\* là thuật toán tìm đường đi ngắn nhất kết hợp giữa Dijkstra và heuristic. Em thường dùng nó cho các bài toán tìm đường trong game và robot. Em cũng biết về cách chọn heuristic tốt và tối ưu hiệu suất.

## 5. Thuật toán xử lý chuỗi

**Interviewer**: Em có thể giải thích về thuật toán KMP (Knuth-Morris-Pratt) không?

**Candidate**: Dạ, KMP là thuật toán tìm kiếm chuỗi con hiệu quả với độ phức tạp O(m+n). Em thường dùng nó cho các bài toán tìm kiếm pattern trong text lớn. Em cũng biết về cách xây dựng bảng LPS (Longest Proper Prefix which is also Suffix).

**Interviewer**: Em có thể giải thích về thuật toán Rabin-Karp không?

**Candidate**: Dạ, Rabin-Karp là thuật toán tìm kiếm chuỗi con sử dụng hashing. Em thích nó vì có thể mở rộng cho tìm kiếm nhiều pattern. Em cũng biết về cách chọn hash function tốt và xử lý collision.

**Interviewer**: Em có thể giải thích về thuật toán Boyer-Moore không?

**Candidate**: Dạ, Boyer-Moore là thuật toán tìm kiếm chuỗi con hiệu quả cho text lớn. Em thường dùng nó khi pattern dài. Em cũng biết về các quy tắc bad character và good suffix.

**Interviewer**: Em có thể giải thích về thuật toán Z không?

**Candidate**: Dạ, thuật toán Z tìm độ dài prefix dài nhất của mỗi vị trí trong chuỗi. Em thường dùng nó cho các bài toán về chuỗi con và palindrome. Em cũng biết về cách cài đặt hiệu quả và ứng dụng.

**Interviewer**: Em có thể giải thích về thuật toán Manacher không?

**Candidate**: Dạ, Manacher là thuật toán tìm palindrome dài nhất trong chuỗi với độ phức tạp O(n). Em thường dùng nó cho các bài toán về palindrome. Em cũng biết về cách xử lý chuỗi và tính toán bán kính palindrome.

## 6. Thuật toán quy hoạch động

**Interviewer**: Em có thể giải thích về quy hoạch động (Dynamic Programming) không?

**Candidate**: Dạ, quy hoạch động là phương pháp giải quyết bài toán bằng cách chia nhỏ thành các bài toán con và lưu kết quả. Em thường dùng nó cho các bài toán tối ưu hóa. Em cũng biết về top-down (memoization) và bottom-up (tabulation).

**Interviewer**: Em có thể giải thích về bài toán cái túi (Knapsack) không?

**Candidate**: Dạ, bài toán cái túi là bài toán tối ưu hóa chọn các vật phẩm để tối đa giá trị với ràng buộc về trọng lượng. Em thường dùng quy hoạch động để giải. Em cũng biết về các biến thể như 0-1 Knapsack và Unbounded Knapsack.

**Interviewer**: Em có thể giải thích về bài toán dãy con tăng dài nhất (LIS) không?

**Candidate**: Dạ, LIS là bài toán tìm dãy con tăng dài nhất trong một dãy số. Em thường dùng quy hoạch động với độ phức tạp O(n²) hoặc O(n log n). Em cũng biết về cách tối ưu và mở rộng cho các biến thể.

**Interviewer**: Em có thể giải thích về bài toán nhân ma trận (Matrix Chain Multiplication) không?

**Candidate**: Dạ, bài toán này tìm cách nhân ma trận với số phép nhân tối thiểu. Em thường dùng quy hoạch động với độ phức tạp O(n³). Em cũng biết về cách xây dựng bảng và truy vết kết quả.

**Interviewer**: Em có thể giải thích về bài toán đường đi ngắn nhất (Shortest Path) không?

**Candidate**: Dạ, em biết về các thuật toán như Dijkstra, Bellman-Ford, và Floyd-Warshall. Em thường dùng quy hoạch động cho Floyd-Warshall với độ phức tạp O(n³). Em cũng biết về cách xử lý các trường hợp đặc biệt như chu trình âm.

## 7. Thuật toán tham lam (Greedy)

**Interviewer**: Em có thể giải thích về thuật toán tham lam không?

**Candidate**: Dạ, thuật toán tham lam là phương pháp giải quyết bài toán bằng cách chọn lựa tối ưu cục bộ tại mỗi bước. Em thường dùng nó cho các bài toán tối ưu hóa. Em cũng biết về cách chứng minh tính đúng đắn của thuật toán tham lam.

**Interviewer**: Em có thể giải thích về bài toán sắp xếp công việc (Job Scheduling) không?

**Candidate**: Dạ, bài toán này tìm cách sắp xếp các công việc để tối đa lợi ích. Em thường dùng thuật toán tham lam với độ phức tạp O(n log n). Em cũng biết về các biến thể như sắp xếp theo deadline và sắp xếp với nhiều máy.

**Interviewer**: Em có thể giải thích về bài toán mã Huffman không?

**Candidate**: Dạ, mã Huffman là phương pháp nén dữ liệu sử dụng cây nhị phân. Em thường dùng thuật toán tham lam để xây dựng cây Huffman. Em cũng biết về cách mã hóa và giải mã.

**Interviewer**: Em có thể giải thích về bài toán tìm cây khung nhỏ nhất (Minimum Spanning Tree) không?

**Candidate**: Dạ, em biết về các thuật toán như Kruskal và Prim. Em thường dùng thuật toán tham lam với độ phức tạp O(E log V). Em cũng biết về cách cài đặt hiệu quả bằng Disjoint Set.

**Interviewer**: Em có thể giải thích về bài toán đổi tiền (Coin Change) không?

**Candidate**: Dạ, bài toán này tìm cách đổi tiền với số đồng xu tối thiểu. Em thường dùng thuật toán tham lam cho trường hợp đặc biệt và quy hoạch động cho trường hợp tổng quát. Em cũng biết về cách xử lý các trường hợp không có nghiệm.

## 8. Thuật toán xử lý đồ thị

**Interviewer**: Em có thể giải thích về thuật toán tìm thành phần liên thông mạnh (SCC) không?

**Candidate**: Dạ, em biết về thuật toán Kosaraju sử dụng DFS hai lần. Em thường dùng nó cho các bài toán về đồ thị có hướng. Em cũng biết về cách cài đặt hiệu quả và ứng dụng.

**Interviewer**: Em có thể giải thích về thuật toán tìm cầu và khớp (Articulation Points and Bridges) không?

**Candidate**: Dạ, em biết về thuật toán Tarjan sử dụng DFS. Em thường dùng nó cho các bài toán về độ tin cậy của mạng. Em cũng biết về cách cài đặt và xử lý các trường hợp đặc biệt.

**Interviewer**: Em có thể giải thích về thuật toán tìm chu trình Euler không?

**Candidate**: Dạ, em biết về thuật toán Fleury và Hierholzer. Em thường dùng nó cho các bài toán về đường đi Hamilton. Em cũng biết về điều kiện tồn tại chu trình Euler và cách xử lý đồ thị vô hướng/hữu hướng.

**Interviewer**: Em có thể giải thích về thuật toán tìm cặp ghép cực đại (Maximum Bipartite Matching) không?

**Candidate**: Dạ, em biết về thuật toán Hungary và Ford-Fulkerson. Em thường dùng nó cho các bài toán về phân công công việc. Em cũng biết về cách cài đặt hiệu quả và mở rộng cho các biến thể.

**Interviewer**: Em có thể giải thích về thuật toán tìm luồng cực đại (Maximum Flow) không?

**Candidate**: Dạ, em biết về các thuật toán như Ford-Fulkerson, Edmonds-Karp, và Dinic. Em thường dùng nó cho các bài toán về tối ưu hóa luồng. Em cũng biết về cách cài đặt hiệu quả và ứng dụng.
