
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
### One mental model (remember this)
 **Discover → Crawl → Parse HTML → Render JS → Index → Recrawl → Rank**

## Frontend security best practices (e.g., XSS prevention, cookies, authentication)

## Web view (for mobile apps)