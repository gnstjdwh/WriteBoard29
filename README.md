# 발견 문제점
## 1. '조회' /board/view.do 에서 에러 발생

> **원인** : view.jsp 에서 DTO 의 property 를 잘못 기재.

```java
${list[0].regdate} ==> ${list[0].regDateTime}
```

## 2. '수정' 시 내용이 삭제되는 증상 발생
> **원인** : update.jsp 에서 parameter name 에 오타

```html
<text name="contnet"> => <text name="content">
```