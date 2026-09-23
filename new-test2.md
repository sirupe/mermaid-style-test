### e. 클래스 라벨에 KaTeX
```mermaid
classDiagram
  class Notifier["CouponExpiryNotifier $$\color{#d9480f}{new}$$"]
```

### f. 클래스 메서드에 KaTeX
```mermaid
classDiagram
  class CouponRepository {
    +findById(long id) Coupon
    +markNoticed(long id) $$\color{#d9480f}{new}$$
  }
```

### g. 클래스 note에 HTML
```mermaid
classDiagram
  class CouponRepository {
    +findById(long id) Coupon
    +markNoticed(long id)
  }
  note for CouponRepository "<span style='color:#d9480f'>new</span> markNoticed()"
```

### h. 클래스 라벨에 마크다운 문자열
```mermaid
classDiagram
  class Notifier["`CouponExpiryNotifier **new**`"]
```
