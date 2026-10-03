Deployment
https://week5-lime.vercel.app/

Key learning
이번 주에 배운 핵심 내용 3가지
JS event를 통해 웹페이지에서 발생하는 동작이나 상태를 감지하고 각각의 상황에 맞게 원하는 대로 웹페이지를 조작하는 것을 배웠습니다.
JS form validation을 통해 사용자가 form을 통해 입력한 값이 조건을 충족하는지 검사하는 것을 배웠습니다.
object array와 DOM 변경하는 것을 통해 사용자가 입력한 정보를 저장하고 수정하고, 삭제하고, 추가하는 기능을 구현할 수 있습니다.

CRUD service
구현한 서비스 주제: 공동 todo list 관리
사용하는 데이터 Field
어떤 일정인지 일정의 이름, 어떤 종류의 일정인지(ex 학교, 교회, 동아리 등), 언제까지인지 혹은 언제인지 날짜, 입력한 사람이 누군지, 입력한 사람의 메일을 field로 다룹니다. 
Create / Read / Update / Delete 구현 방법
함수를 네 가지로 구분했습니다. 화면에 array의 내용을 출력해주는 함수, 새로운 정보르 입력받아 배열에 저장하는 함수, 
배열의 저장된 특정 정보를 삭제하는 함수, 특정 정보를 수정하는 함수, 입력받은 내용을 배열에 추가하는 함수 이렇게 네 가지의 함수를 만들고
window.addEventListener와 addEventListener에서 적절히 호출해서 사용하는 식으로 구조를 잡았습니다. 수정하는 기능을 구현하기 위해 변수를 
하나 설정해서 수정 버튼을 누르면 그 값이 바뀌게 하여 addEventListener 안에서 sunbmit 버튼을 눌렀을 때 변수의 값에 따라 수정하는 기능을 실행할지
추가하는 기능을 실행할지 구분하도록 하였습니다. 각 데이터마다 id를 부여해 수정할 때, 삭제할 때 그 id값으로 array안에서 
정보를 찾고 수정하고 삭제하도록 하였습니다.
JavaScript

이번 과제에서 사용한 주요 JavaScript 기능을 설명합니다.
querySelector() : html 요소를 자바스크립트로 가져오는 기능이고, 태그,클래스,아이디를 통해 접근할 수 있다. 
addEventListener() : 이벤트를 감지하는 역할을 한다. 마우스클릭, 키보드입력, 마우스호버 등등 
createElement() : 새로운 HTML 태그를 만들어내는 기능을 한다. 
appendChild() : 이미 만들어둔 요소나 태그를 특정 부모 요소의 자식으로 갖다가 붙이는 기능을 한다. 
Array : 여러 개의 데이터를 순서대로 하나의 변수로 묶어서 보관하는 기능을 한다. 
filter() : 배열 요소 중에 조건에 맞는 요소만 걸러서 새로운 배열을 만들어 변환한다.
confirm(): 사용자에게 팝업창을 띄우고 확인을 누르면 true, 취소를 누르면 false를 반환한다.
forEach : 배열에 있는 요소들을 하나씩 처음부터 끝까지 꺼내며 반복 작업을 수행한다.
Date.now() : 1970년부터의 시간을 현재까지 밀리초 단위의 숫자로 반환한다.
push(): 배열의 맨 뒤에 새로운 데이터를 추가하는 기능을 한다.

AI / Search Usage
li.textContent = uname.value + " - " + email.value; li의 text내용 할당할 때 입력받은 값으로 할당하는 방법이 분명 있을텐데 생각하면서 혼자 시도하다가 ai에게 물어봤습니다.
confirm도 어떻게 쓰는지 몰라서 ai에게 물어봤습니다.
todoList = todoList.filter(todo => todo.id != id) filter 사용법을 몰라서 ai에게 물어봤습니다. 
todoList = todoList.filter(function(todo) {
    return todo.id != id;
}); 같은 표현인 걸 알게 됨.
const target = todoList.find(todo => todo.id == id); find도 filter와 사용법이 거의 같다는 것도 알았습니다.
수정하는 기능을 구현할 때 이미 입력받은 radio값은 어떻게 표시할 수 있을까 고민하다가 ai에게 물어봤습니다.
const radio = document.querySelector(`input[name="information"][value="${target.dobtn}"]`); radio 태그를 불러와서
if(radio) radio.checked = true; null 값이 아니면 그때의 값으로 표시하게 할 수 있다는 것도 배웠습니다. 
forEach도 ai에게 사용법을 물어봤습니다.
push도 ai에게 사용법을 물어봤습니다.
ai에게 사용법과 예시 보여달라고 하고 제 코드에 적용 시키는 방법으로 했습니다. 
도저히 안 되겠어서 제 코드의 일부분을 보여주고 물어보기도 했는데 그럴 경우 거의 오타 문제였습니다.
그리고 css를 사용해서 디자인하려고 했었는데 bootstrap을 좀 더 익히고 싶어서 원하는 디자인을 가능하게 해주는
bootatrap 디자인이 있는지, 까먹은 class이름이 뭔지 ai에게 물어보며 했습니다.
shadow-sm, text-primary, flex-shrink-0, flex-grow-1 이런 익숙치 않은 태그들 익혔습니다.
저는 제미나이 사용했습니다.

Problem & Solution
모르는 기능을 사용해야 하는 부분이 있어서 filter, push, array 등등 위의 ai활용과 search부분에 입력한 내용에서 말한 것처럼
검색해보고 검색해봐도 모르겠으면 ai에게 좀 구체적인 예시 달라고 하고 적용해보고 그렇게 해결했습니다.

Reflection
확실히 점점 변수도 많아지고, 구조도 복잡해지고 하니 괄호 하나, 오타 하나 때문에 몇 분씩 붙잡고 있었던 게 너무 
아까웠다.. 그러면서 더 잘 배우게 되는 것 같아 뿌듯하기도 했다. 코드가 점점 길어지니 확실히 왜 디자인 따로 스크립트 따로 하는지 
절실히 느꼈다. 물론 디테일하게 디자인을 바꾸고 싶은 거는 결국에는 css를 써야 하지만, 앞으로도 bootstrap을 적극 활용하는 게 훨씬 편할 것 같다.

이번 과제를 통해 새롭게 알게 된 점 또는 궁금한 점
정성들여서 하나하나 만드는 게 정말 힘들고 시간이 많이 든다는 걸 절실히 느끼지만 그래도 이렇게 배워야 오래 남고
의미있는 것 같다. 오늘 과제를 마무리하면서 정말 이제 나도 웹페이지는 잘 만들 수 있겠다는 생각이 들었다. 완성도가
기능에서 갈리는 게 아니라 디자인에서 갈린다는 게 조금 아쉽다. 디자인도 더 열심히 한 번 공부해봐야겠다는 생각이 들었다. 
