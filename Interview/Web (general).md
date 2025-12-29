
## How Googlebot works & how often it recrawls
### 1. How Google finds a page

- Through **links**, **sitemaps**, or **Search Console**   
- No links + no sitemap → likely never found
### 2. Crawling
- Googlebot requests the URL
- Checks:
    - `robots.txt`
    - HTTP status
    - `noindex / nofollow`
- Blocked here → never indexed
### 3. Parsing & rendering
- Reads **HTML first**
- Then (if needed) runs **JavaScript** using headless Chrome
- If content depends on JS, auth, or user action → may fail
### 4. Indexing
- Google decides:
    - Is content useful?
    - Is it duplicate?
    - Which URL is canonical?
- Crawled ≠ indexed
### 5. Recrawling (no fixed time)
- Per URL, not entire app
- Based on:
    - Importance (links, traffic)
    - Content change frequency
    - Site trust & server quality
    - Sitemap + `lastmod`
    - `Last-Modified / ETag`
**Ranges:**
- Important pages → minutes / hours
- Normal pages → days
- Low-value pages → weeks / months
### 6. React / Next.js impact
- Google crawls **URLs**
- **SSR / SSG / ISR** = best
- Client-only rendering = risky
- Google can’t see content if render fails
### 7. SEO: One mental model (remember this)
 **Discover → Crawl → Parse HTML → Render JS → Index → Recrawl → Rank**

### **8. CORS**
CORS (Cross-Origin Resource Sharing) is ==a browser security standard that lets servers explicitly allow web pages from _different_ domains (origins) to request resources==

## Frontend security best practices 
- Dont store sensitve data on localStorage
- Use **Content Security Policy (CSP)** in response header (We need help from BE.)
- Sanitization input
- Dont use dangerouslysetinnerhtml

## Web view (for mobile apps)

## Why mobile first?

## 1. **Thống kê sử dụng thiết bị**

- Hơn 60% lưu lượng truy cập web toàn cầu đến từ mobile
- Người dùng dành nhiều thời gian hơn trên điện thoại so với desktop
- Xu hướng này đang tăng mạnh hàng năm

## 2. **Ưu tiên nội dung (Content Priority)**

- Buộc bạn tập trung vào nội dung quan trọng nhất
- Loại bỏ các yếu tố không cần thiết
- Tạo trải nghiệm người dùng đơn giản, rõ ràng hơn

## 3. **Hiệu suất tốt hơn (Performance)**

- Tối ưu hóa tốc độ tải trang ngay từ đầu
- Giảm dung lượng file, hình ảnh
- Cải thiện Core Web Vitals (chỉ số quan trọng của Google)

## 4. **SEO tốt hơn**

- Google sử dụng Mobile-First Indexing (ưu tiên phiên bản mobile)
- Website mobile-friendly được xếp hạng cao hơn
- Tăng khả năng hiển thị trên kết quả tìm kiếm

## 5. **Dễ mở rộng (Progressive Enhancement)**

- Bắt đầu từ mobile đơn giản, sau đó mở rộng cho màn hình lớn
- Dễ hơn so với làm ngược lại (desktop → mobile)
- Tránh phải cắt bỏ tính năng khi thu nhỏ

## 6. **Tiết kiệm chi phí**

- Phát hiện vấn đề sớm trong quá trình phát triển
- Giảm thời gian sửa lỗi và tối ưu hóa sau này

## RESTful Methods
