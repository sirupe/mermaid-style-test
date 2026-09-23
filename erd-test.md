### a. 주석 칸 HTML span
```mermaid
erDiagram
  COUPON {
    bigint id PK
    datetime expiry_noticed_at "<span style='color:#d9480f'>신규</span>"
  }
```

### b. 컬럼명 자리에 HTML
```mermaid
erDiagram
  COUPON {
    bigint id PK
    datetime <span_style='color:#d9480f'>expiry_noticed_at</span> "신규"
  }
```

### c. 테두리만 (글자색 없음)
```mermaid
erDiagram
  COUPON {
    bigint id PK
    datetime expiry_noticed_at "신규"
  }
  classDef changed stroke:#d9480f,stroke-width:2px
  class COUPON changed
```

### d. 컬럼 글자색 CSS 선택자 시도 (themeCSS)
```mermaid
---
config:
  themeCSS: ".attributeBoxEven text, .attributeBoxOdd text {} g[id*='expiry'] text {fill:#d9480f}"
---
erDiagram
  COUPON {
    bigint id PK
    datetime expiry_noticed_at "신규"
  }
```

### e. themeCSS 로 특정 행 글자색 (nth-child)
```mermaid
---
config:
  themeCSS: "[id*='entity-COUPON'] .row-rect-odd:nth-of-type(2) + * text, text[id*='expiry_noticed_at'] {fill:#d9480f !important}"
---
erDiagram
  COUPON {
    bigint id PK
    datetime expiry_noticed_at "신규"
  }
```
