#### td

> - 단일 셀
> - 빈칸을 사용해서 칸을 맞출수도 있음

#### tr

> - table row
> - 1 tr === 1행, 예를들어 tr>td\*3이면 1row, 3columns의 꼴

#### th

> - table header
> - 헤더를 하나로 만들것이 아니라면,열의 개수에 맞춰서 헤더를 생성하면 될듯함

#### rowspan

> - 가로(행) 너비(크기)

#### colspan

> - 세로(열) 너비(크기)

#### form

> - 텍스트 입력란, 비밀번호 입력란, 버튼 및 체크박스 등 여러 개별 폼 컨트롤을 품는 컨테이너라고 생각하자
> - form의 action속성이 폼이 제출되었을 때 데이터를 보낼 위치와 시간등을 지정함

#### input

> - 빈태그, 입력창
> - type = checkbox => 복수 선택 가능 (모두 체크할 수도, 안할 수도 있음)
> - type = radio => 하나만 선택 가능 (묶음 내에서는 name 속성값이 동일해야함)
> - value 속성: 화면에 노출되지는 않으나, 폼 제출 시 값으로 전송됨, 즉 제출 시 서버에 전송되는 값(value)

##### input의 name 속성

> - 만약 form action이 '/path' 이고 그 안의 input의 name이 'userName' 일 경우 input 창에 이름을 넣고 폼 제출시에는 "/path?userName=안태욱"와 같은 링크로 데이터가 제출됨
> - 즉, /formAction?name(key)=inputContent(value)의 형식, 하지만 만약 value 속성이 있으면 /name=value로 제출됨
> - name이 여러개 제출 됬을 경우에는 &로 구분지어 이어짐
> - 이런식이라면 password같은 경우 url에 보이게 되는 문제가 생길 수 있는데, 이것은 추후 HTTP 요청에서 다시 다룰 예정
> - radio속성을 사용하기 위해 묶을 경우에는 name 속성이 모두 동일해야함

##### input의 raido 속성

> - input의 id와 label의 for의 값을 동일하게 지정하여 연결
> - 실제 제출되는 값은 value 속성이므로 필수로 지정해주어야함

#### label

> - label 요소는 실제로 특정한 입력 값이나, form 컨트롤 및 텍스트와 연결되어 있다.
> - 스크린 리더가 읽어주기도 한다.
> - 클릭 시 직접적으로 연결된 input 태그에 접근 할 수 있게도 한다.
> - input의 id와 label의 for의 값을 동일하게 지정하여 연결

#### button

> - form 안에 있으면 기본값(submit)으로 해당 폼을 제출
> - form 밖에 있으면 아무 행동도 하지 않음
> - form 안에 있더라도 type="button" 속성 사용 시 폼을 제출하지 않고 버튼으로만 기능함

#### 유효성 검사

> - required: 공백일시 제출 불가
> - minlength: 최소 글자 체크
> - maxlength: 최대 글자 체크
> - 정규 표현식을 사용한 유효성 감사는 추후에 학습 예정
