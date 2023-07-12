### 선택자

#### 기본 패턴

```css
selector {
  property: value;
}
```

#### 전체 선택자

```css
* {
  color: balck;
}
```

#### 태그(요소) 선택자

```css
태그명 {
  property: value;
}
```

#### CSS selector list

```css
span,
div {
  border: red 2px solid;
}
```

- ,(콤마)로 구분하며, 여러개의 일치하는 모든 선택자들에 적용

#### 클래스 선택자

```css
.class명 {
  property: value;
}
```

#### ID 선택자

```css
#id명 {
  property: value;
}
```

#### 자손 선택자

```css
li a {
  color: blue;
}
```

> - 띄어쓰기 사용
> - 콤마와 사용 주의
> - 콤마는 li, a라면 상속에 관계 없이 모든 li태그와 a태그를 선택하는것이고
> - 자손 선택자의 경우 위의 예시로 설명하자면 li태그 이하의 a태그를 선택하는것이며 이외의 a태그에는 적용되지 않는다.

#### 자식 선택자

```css
A > B {
  color: teal;
}
```

```html
<div>
  <h1 class="one">1번</h1>
  <h1 class="two">2번</h1>
  <p class="three">3번</p>
</div>
```

> - A의 자식 요소 B를 선택한다.
> - 자식 요소들 중 일치하는 것들(다수 가능)을 변경한다.
> - 위 예시에서는 div의 하위 h1태그 모두 color가 변경된다.

### 자손 선택자 vs 자식 선택자

```
- A B {}: A요소에 포함된 B요소를 선택 (자손)
- A > B {}: A요소의 직계 자식 요소인 B를 선택 (자식)
- 결론부터 말하자면 자식이 더 작은 범위
- 자식은 선택 태그 바로 아래 계층에 있는 것 (1 depth)
- 자손은 선택 태그 안에 들어가 있는 모든 것 (모든 depth)
- 즉, 자식 선택자(A>B)는 바로 아래 있는것만, 자손 선택자(A B)는 아래의 해당 태그 모두 선택
```

#### 인접 선택자 (형제)

```css
A + B {
  color: red;
}
```

> - A와 B가 같은 계층에 있을 때 A 바로 뒤에 B를 선택자로 지정
> - 아래 예제의 경우 `<h1>` 태그 바로 뒤에 있는 `<h2>` 태그 1개(2번)만 컬러를 변경시킴

```css
h1 + h2 {
  color: teal;
}
```

```html
<h1>1번</h1>
<h2>2번</h2>
<h2>3번</h2>
<h2>4번</h2>
```

#### 속성 선택자

```css
a[target="_blank"] {
  color: red;
}
```

> - 속성명으로 선택하는 선택자이며, 방법이 여러 종류이기 때문에 필요시 찾아보도록 하고 우선 위의 예시로 정리해둔다.
> - a태그에 target=”\_blank”라는 속성을 가진 요소를 선택하며, targer이 반드시 \_blank인 요소만 선택한다.
> - `<a href="#" target="_blank">link</a>` 선택
> - `<a href="#" target="_self">link</a>` 선택 안함
> - `<a href="#" target="_blankk">link</a>` 선택 안함
