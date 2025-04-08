# Câu hỏi phỏng vấn HTML/CSS cho Intern

## 1. Kiến thức cơ bản về HTML

**Interviewer**: Em hãy giải thích HTML là gì và tại sao nó lại quan trọng trong phát triển web?

**Candidate**: Dạ, HTML (HyperText Markup Language) là ngôn ngữ đánh dấu siêu văn bản được sử dụng để tạo cấu trúc cho các trang web. Em nghĩ HTML rất quan trọng vì nó là nền tảng của mọi trang web, định nghĩa cấu trúc và nội dung. Em thấy HTML5 đã mang lại nhiều tính năng mới như semantic elements, form controls tốt hơn, và hỗ trợ multimedia tốt hơn.

**Interviewer**: Em có thể giải thích về semantic HTML không?

**Candidate**: Dạ, semantic HTML là cách sử dụng các thẻ HTML có ý nghĩa ngữ nghĩa để mô tả nội dung. Em thường dùng các thẻ như `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>` thay vì `<div>` để code có ý nghĩa hơn. Em thấy semantic HTML giúp SEO tốt hơn và cải thiện accessibility cho người dùng screen readers.

**Interviewer**: Em có thể kể về các thẻ meta quan trọng trong HTML không?

**Candidate**: Dạ, em thường dùng các thẻ meta như `<meta charset="UTF-8">` để định nghĩa encoding, `<meta name="viewport">` để responsive design, `<meta name="description">` cho SEO, và `<meta name="theme-color">` để tùy chỉnh màu sắc trên mobile browsers. Em cũng hay dùng Open Graph meta tags để tối ưu khi chia sẻ trên mạng xã hội.

**Interviewer**: Em có thể giải thích về HTML5 APIs không?

**Candidate**: Dạ, HTML5 đã giới thiệu nhiều API mới như Web Storage (localStorage, sessionStorage), Web Workers cho xử lý đa luồng, WebSocket cho giao tiếp realtime, và WebRTC cho video/audio streaming. Em thấy các API này giúp tạo ra các ứng dụng web phức tạp hơn mà không cần plugins.

**Interviewer**: Em có thể giải thích về HTML forms và validation không?

**Candidate**: Dạ, HTML5 đã thêm nhiều tính năng validation mới như `required`, `pattern`, `min`, `max`, `type="email"`, `type="tel"`. Em thường kết hợp HTML validation với JavaScript để tạo trải nghiệm người dùng tốt hơn. Em cũng hay dùng `<datalist>` để tạo dropdown với gợi ý tìm kiếm.

## 2. Kiến thức cơ bản về CSS

**Interviewer**: Em có thể giải thích về CSS là gì và các cách áp dụng CSS không?

**Candidate**: Dạ, CSS (Cascading Style Sheets) là ngôn ngữ định dạng để tạo style cho trang web. Em thường dùng 3 cách: inline CSS, internal CSS trong thẻ `<style>`, và external CSS trong file riêng. Em thích dùng external CSS vì dễ maintain và có thể tái sử dụng.

**Interviewer**: Em có thể giải thích về CSS Selectors không?

**Candidate**: Dạ, em thường dùng các loại selector như element selector (p, div), class selector (.class), ID selector (#id), attribute selector ([type="text"]), và pseudo-classes (:hover, :focus). Em cũng hay dùng combinators như descendant (space), child (>), và sibling (~, +) để chọn elements.

**Interviewer**: Em có thể giải thích về CSS Box Model không?

**Candidate**: Dạ, CSS Box Model bao gồm content, padding, border, và margin. Em thường dùng `box-sizing: border-box` để tính toán kích thước element dễ dàng hơn. Em cũng biết về `box-shadow` và `border-radius` để tạo hiệu ứng visual.

**Interviewer**: Em có thể giải thích về CSS Flexbox không?

**Candidate**: Dạ, Flexbox là một layout model giúp sắp xếp elements theo một chiều. Em thường dùng `display: flex` và các properties như `justify-content`, `align-items`, `flex-direction`, `flex-wrap`. Em thấy Flexbox rất hữu ích cho responsive design và căn chỉnh elements.

**Interviewer**: Em có thể giải thích về CSS Grid không?

**Candidate**: Dạ, CSS Grid là layout model mạnh mẽ cho việc sắp xếp elements theo hai chiều. Em thường dùng `display: grid` và các properties như `grid-template-columns`, `grid-template-rows`, `grid-gap`. Em thích dùng Grid cho layouts phức tạp và responsive.

## 3. Responsive Design

**Interviewer**: Em có thể giải thích về responsive design không?

**Candidate**: Dạ, responsive design là cách thiết kế website để hiển thị tốt trên mọi thiết bị. Em thường dùng media queries, flexible images, và fluid grids. Em cũng hay dùng viewport meta tag và các đơn vị tương đối như %, em, rem, vw, vh.

**Interviewer**: Em có thể giải thích về media queries không?

**Candidate**: Dạ, media queries cho phép áp dụng CSS dựa trên các đặc điểm của thiết bị. Em thường dùng breakpoints cho mobile, tablet, và desktop. Em cũng hay dùng `min-width` và `max-width` để tạo mobile-first design.

**Interviewer**: Em có thể giải thích về CSS Grid và Flexbox trong responsive design không?

**Candidate**: Dạ, em thường kết hợp Grid và Flexbox để tạo layouts responsive. Grid cho layout tổng thể, Flexbox cho các components nhỏ hơn. Em cũng hay dùng `auto-fit` và `auto-fill` trong Grid để tạo responsive grids.

**Interviewer**: Em có thể giải thích về responsive images không?

**Candidate**: Dạ, em thường dùng `<picture>` element và `srcset` attribute để cung cấp nhiều phiên bản ảnh cho các thiết bị khác nhau. Em cũng hay dùng `object-fit` để kiểm soát cách ảnh được hiển thị trong container.

**Interviewer**: Em có thể giải thích về mobile-first design không?

**Candidate**: Dạ, mobile-first là cách tiếp cận thiết kế bắt đầu từ mobile và mở rộng lên desktop. Em thường dùng min-width media queries và thiết kế cho màn hình nhỏ trước. Em cũng chú ý đến performance và tối ưu cho mobile.

## 4. CSS Preprocessors và Postprocessors

**Interviewer**: Em có thể giải thích về CSS Preprocessors không?

**Candidate**: Dạ, CSS Preprocessors như Sass, Less, và Stylus cho phép viết CSS với các tính năng nâng cao. Em thường dùng Sass vì nó có nhiều tính năng như variables, nesting, mixins, và functions. Em cũng hay dùng @import để tổ chức code.

**Interviewer**: Em có thể giải thích về CSS Postprocessors không?

**Candidate**: Dạ, PostCSS là công cụ biến đổi CSS với plugins. Em thường dùng Autoprefixer để thêm vendor prefixes, CSS Modules để scope CSS, và PostCSS Preset Env để sử dụng các tính năng CSS mới. Em cũng hay dùng CSS-in-JS solutions như styled-components.

**Interviewer**: Em có thể giải thích về CSS Modules không?

**Candidate**: Dạ, CSS Modules là cách để scope CSS locally trong components. Em thường dùng nó trong React để tránh CSS conflicts. Em cũng biết về cách import/export CSS Modules và cách sử dụng composition.

**Interviewer**: Em có thể giải thích về CSS-in-JS không?

**Candidate**: Dạ, CSS-in-JS là cách viết CSS trong JavaScript. Em thường dùng styled-components hoặc Emotion. Em thấy nó giúp component-based styling và dynamic styles dễ dàng hơn. Em cũng biết về performance implications và cách tối ưu.

**Interviewer**: Em có thể giải thích về CSS Custom Properties không?

**Candidate**: Dạ, CSS Custom Properties (variables) cho phép định nghĩa và sử dụng các giá trị tùy chỉnh. Em thường dùng nó cho theming và responsive design. Em cũng biết về cách sử dụng trong JavaScript và fallbacks.

## 5. CSS Frameworks và Libraries

**Interviewer**: Em có thể kể về các CSS Frameworks phổ biến không?

**Candidate**: Dạ, em biết về Bootstrap, Tailwind CSS, Bulma, và Foundation. Em thường dùng Tailwind CSS vì nó utility-first và highly customizable. Em cũng biết về cách tùy chỉnh và tối ưu các frameworks này.

**Interviewer**: Em có thể giải thích về Tailwind CSS không?

**Candidate**: Dạ, Tailwind CSS là utility-first CSS framework. Em thích nó vì không cần viết CSS riêng, chỉ cần sử dụng các utility classes. Em cũng biết về cách cấu hình Tailwind và tạo custom utilities.

**Interviewer**: Em có thể giải thích về Bootstrap không?

**Candidate**: Dạ, Bootstrap là framework phổ biến với grid system, components, và utilities. Em thường dùng nó cho rapid prototyping. Em cũng biết về cách customize Bootstrap với Sass và responsive breakpoints.

**Interviewer**: Em có thể giải thích về CSS Grid Frameworks không?

**Candidate**: Dạ, em biết về CSS Grid Frameworks như CSS Grid Garden và Grid by Example. Em thường dùng chúng để học và thực hành CSS Grid. Em cũng biết về cách tạo custom grid systems.

**Interviewer**: Em có thể giải thích về CSS Animation Libraries không?

**Candidate**: Dạ, em biết về các thư viện như Animate.css, GSAP, và Motion One. Em thường dùng chúng cho complex animations. Em cũng biết về performance và cách tối ưu animations.

## 6. CSS Best Practices và Performance

**Interviewer**: Em có thể kể về các CSS Best Practices không?

**Candidate**: Dạ, em thường tuân thủ các quy tắc như BEM naming convention, CSS specificity, và DRY principle. Em cũng hay dùng CSS reset/normalize và tổ chức CSS theo components. Em thấy quan trọng là phải maintain được code.

**Interviewer**: Em có thể giải thích về CSS Specificity không?

**Candidate**: Dạ, specificity xác định quyền ưu tiên của CSS selectors. Em biết về cách tính specificity và cách sử dụng !important. Em cũng cẩn thận với specificity để tránh conflicts.

**Interviewer**: Em có thể giải thích về CSS Performance không?

**Candidate**: Dạ, em thường tối ưu bằng cách minimize CSS, sử dụng critical CSS, và tránh expensive selectors. Em cũng biết về rendering performance và cách sử dụng will-change. Em thấy quan trọng là phải measure performance.

**Interviewer**: Em có thể giải thích về CSS Architecture không?

**Candidate**: Dạ, em thường dùng các phương pháp như SMACSS, ITCSS, và Atomic Design. Em cũng biết về cách tổ chức CSS theo layers và components. Em thấy architecture giúp maintain code dễ dàng hơn.

**Interviewer**: Em có thể giải thích về CSS Testing không?

**Candidate**: Dạ, em biết về các công cụ như Stylelint, CSS Validator, và visual regression testing. Em thường dùng chúng để đảm bảo code quality. Em cũng biết về cách test responsive designs.

## 7. Advanced CSS

**Interviewer**: Em có thể giải thích về CSS Custom Properties không?

**Candidate**: Dạ, CSS Custom Properties cho phép tạo và sử dụng variables trong CSS. Em thường dùng nó cho theming và responsive design. Em cũng biết về cách sử dụng trong JavaScript và fallbacks.

**Interviewer**: Em có thể giải thích về CSS Grid Areas không?

**Candidate**: Dạ, Grid Areas cho phép đặt tên và sắp xếp grid items. Em thường dùng nó cho complex layouts. Em cũng biết về responsive grid areas và cách sử dụng với media queries.

**Interviewer**: Em có thể giải thích về CSS Shapes không?

**Candidate**: Dạ, CSS Shapes cho phép tạo các hình dạng phức tạp. Em thường dùng `clip-path` và `shape-outside`. Em cũng biết về cách tạo animations với shapes.

**Interviewer**: Em có thể giải thích về CSS Filters không?

**Candidate**: Dạ, CSS Filters cho phép áp dụng các hiệu ứng như blur, brightness, contrast. Em thường dùng nó cho hover effects và image manipulation. Em cũng biết về performance implications.

**Interviewer**: Em có thể giải thích về CSS Blend Modes không?

**Candidate**: Dạ, Blend Modes cho phép blend elements với nhau. Em thường dùng nó cho creative effects và overlays. Em cũng biết về cách sử dụng với images và text.

## 8. Modern CSS Features

**Interviewer**: Em có thể giải thích về CSS Container Queries không?

**Candidate**: Dạ, Container Queries cho phép styling dựa trên kích thước container thay vì viewport. Em thấy nó rất hữu ích cho component-based design. Em cũng biết về browser support và fallbacks.

**Interviewer**: Em có thể giải thích về CSS Cascade Layers không?

**Candidate**: Dạ, Cascade Layers cho phép kiểm soát specificity và cascade order. Em thường dùng nó để tổ chức CSS theo layers. Em cũng biết về cách sử dụng với @layer.

**Interviewer**: Em có thể giải thích về CSS Subgrid không?

**Candidate**: Dạ, Subgrid cho phép grid items kế thừa grid từ parent. Em thường dùng nó cho nested grids. Em cũng biết về browser support và alternatives.

**Interviewer**: Em có thể giải thích về CSS Logical Properties không?

**Candidate**: Dạ, Logical Properties cho phép styling dựa trên logical flow thay vì physical directions. Em thường dùng nó cho RTL support. Em cũng biết về cách sử dụng với writing modes.

**Interviewer**: Em có thể giải thích về CSS Viewport Units không?

**Candidate**: Dạ, Viewport Units (vw, vh, vmin, vmax) cho phép sizing dựa trên viewport. Em thường dùng nó cho responsive design. Em cũng biết về cách sử dụng với calc() và fallbacks.
