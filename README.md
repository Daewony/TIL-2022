# TIL-2022

## 1013 {
  + ```<i></i>
  + <i></i>```
  + i 태그는 이렇게 띄어쓰기만 해도 한칸이라고 인식을 함으로 떨어져있으니 i태그를 담는 div태그 class에 display:flex를 해주자
  + container-class를 줄이면 안에있던 모든 요소도 줄어들줄 알았는데 img는 width: 100%를 하지 않으면 그냥 사진의 크기로 나와서 div 범위를 뚫고 나오니 주의
  + list-style은 margin:0, padding: 0 를 해야한다(친구관계)
  + 왜? : 리스트의 ● 이 차지하는 padding과 margin이 존재하기 때문이다
  + 작업을 해보니 한글과 영어가 약간의 픽셀차이가 난다, 한글로 나란히 있을때랑 영어랑 한글이 나란히 있을때의 위치가 약간 차이가 난다(영어가 한글보다 왼쪽으로 이동해있음)
  + 파이썬 set 특징: 
  + 1. 중복 허용 x 
  + 2. 순서 없음 (sort()이용 못함)
}

## 1012 {
  + sort <-> sorted 차이
  + sort: 원본 정렬, 원본값을 수정
  + sorted: 복사본을 만들어서 정렬, 새로운 리스트를 만들어서 리턴, 원본값은 그대로, 정렬값 반환
}

## 1011 {
  + 미디어 쿼리
  + @media(조건) <-> @media screen and (조건) <-> @media only screen and (조건)
  + 위 각각 미디어 쿼리를 조건에 맞게 사용하는 것인데 왜 이렇게 나눠져있고 사용목적이 다른가?
  + @media only screen and (조건) 는 옛날 브라우저(미디어 쿼리를 제공 못함)가 이 미디어 쿼리를 못읽음 -> 지원 못하는 브라우저는 적용하지 못하도록 only를 사용함
  + @media (조건) = @media all and (조건), 즉 생략된 부분이다
  + @media (조건) != @media screen and (조건) 같지 않다
  + 오히려 @media (조건)은 screen & print 동시 사용가능하니 더 기능이 많다
}

## 1010 {
  + font awesome 네모 상자 오류 문제 발생
  + 1. 설정에서 본인 버전이 5인지 6인지 확인 후 6으로 변경
  + 2. CDN: https://cdnjs.com/libraries/font-awesome 으로 가서 적용
  + 3. (임시 방편) <i class="fa-brands fa-python skill"> -> (클래스에 fas, fab 추가)<i class="fas fa-brands fa-python skill"> or <i class="fab fa-brands fa-python skill"> 추가한다(버전에 따른 클래스명)

  + css 하는 도중
  + height, width  <-> margin, padding의 관계가 궁금해짐
  + 높이 설정후 padding을 적용하면 높이가 커진다.
  + 그럼 어떻게해야 쉽게 높이 설정할 수 있지?
  + box-sizing: border-box 
  + 를 적용하면 padding을 적용한 만큼 기본사이즈를 줄여서 기존 높이를 유지하게 처리해준다.
  + ex) height: 120px, padding: 15px => 총 높이: 120 + 15(위) + 15(아래) = 150px
  + ex) height: 120px, padding: 15px, box-sizing: border-box => 총 높이: 90(120-30) + 15(위) + 15(아래) = 120px, 즉 추가된 padding 만큼 기존 높이를 빼서 원하는 사이즈로 설정 가능하게 해준다.
  
}

## 1005 {
  + align-items vs align-content 차이
  + align-items는 수직축의 라인을 기준으로 아이템들이 정렬이 되고,
  + align-content는 수직축의 라인을 기준으로 (두 줄 이상 일 때만) 라인 자체가 정렬이 된다.
}



## 0921 {
  + flex-basis: 0; 으로, 기본 점유 크기를 0으로 만들어버려 결국 전체 크기를 1:2:1로 나누어 가져서, 영역 자체의 크기가 정확히 1:2:1의 비율로 설정되었습니다.
여백의 비가 아닌, 영역 자체를 원하는 비율로 분할하기를 원한다면 이렇게 flex-basis을 0으로 하면 손쉽게 처리할 수 있어요.
}



## 0919 {
  화살표 함수
  ```
  () => {}; // 는
function() {}; // 와 같다

(() => {}); // 는
(function() {})(); // 와 같다
```

}

## 0916 {
  + 헤드에 넣지않고 푸터, 즉 맨 밑으로 놓는 이유

```jsx
<script src="js/main.js"></script>
```

HTML로드가 될때 위에서 부터 순서대로 브라우저가 읽음

헤드 자리에 <script>를 넣을 시, <script>를 읽는 동안 코드 아래에 있는 html이 로드가 안된 상황임으로 **load** 나 **DOMContentLoaded** 같은 이벤트를 사용해 html 로드 후 <script> 수행

굳이?

body 의 맨 밑에 놓으면 위 같은 이벤트를 사용할 필요가 없다(이미 html 로드한 후 이다)
}

## 0915 {
  CSS에서 아래의 코드를 사용하는 이유

```css
@charset 'urf-8';
```

CSS코드가 다국어 지원을 하도록 세팅해주는 구문입니다.

영문으로만 코딩한다면 반드시 필요한 것은 아닌데, CSS 코드에 혹시 들어갈지 모르는 영문이나 숫자 외의 문자를 안전하게 처리하기 위해 넣어주기도 한답니다.
}

## 0914 {
  + font-size를 vw와 rem 나누는 기준
  + 화면 크기에 따라서 글자 크기 변동의 유무로 기준
  + 화면이 커질때 글자도 커지고 싶다 : vw
  + 화면이 변해도 글자는 일정해야한다 : rem(크게만 보이기)

}

## 0913 {
  + p, h 태그 가운데 정렬: text-align: center;
  + 가로 스크롤 필요 없을 시, body { overflow-x: hidden; } 하기

}

## 0912 {
  + rem -> font-size 따라감
  + em -> 현재 추가로 적용된 font-size에 따라감

}

## 0911 {
  + 브랜치 공부 및 수정

}


## 0908 {
  + 복습 및 피드백

}

## 0907 {
  + 제작한것 복습 및 피드백

}

## 0906 {
  + 제작한것 복습 및 피드백

}

## 0814 {
  + Uncaught TypeError: Cannot read properties of undefined 오류 발생
  + JS코드엔 문제가 없었으나 함수 관련 CSS에서 ; 관련 문제발생함

}

## 0814 {
  + min-width와 max-width의 차이
  + min-width(최소 width)가 1000px, 즉 1000px 이상인 경우에 적용되는 코드이고
  ```
  @media (min-width: 1000px) {
    body {
      background: gold;
    }
  }
  ```  
  + max-width(최대 width)가 1000px, 즉 1000px 이하인 경우에 적용되는 코드지요.
  ```
  @media (max-width: 1000px) {
    body {
      background: gold;
    }
  }
  ````
 + min-width를 사용하는 경우
 <br/> 스마트폰 등 가장 작은 사이즈에서의 레이아웃을 기본으로 하고, 점차 확장되어가는 형태로 CSS를 작성합니다.

 + max-width를 사용하는 경우
 <br/> 데스크탑용의 가장 큰 화면 사이즈의 레이아웃을 기본으로 하고, 점차 축소하는 형태로 CSS를 작성합니다.
 
}


## 0809 {
  + 빗방울이 떨어지는 것처럼 파동이 퍼지는 느낌으로 만들 순 없을까?
  + 너의 이름은 영상 처럼 곡선으로 선 이동 표현해보자
}

}

## 0722 {
  + Grid를 하기 전에 grid 영역 생각하기 => CSS 셀이 어떻게 나누어져있는지 생각하기
  + 카드 리스트는 grid로 만드는게 더 좋다.
  + < Grid 방법 2가지 >
  + 1. grid-column, grid-row 으로 각 라인의 번호를 이용해서 각 영역을 지정하기
  + 2. grid-template-areas 속성으로 각 영역에 이름을 지정해서 배치하기
 
}


## 0720 {
  + 카드 반대방향으로 넘기는 기능 구현 및 hover 추가
 
}

## 0719 {
  + 카드 반대방향으로 넘기는 기능 구현 및 hover 추가
 
}

## 0713 {
  + 카드 넘칠때 넘기는 기능 구현, 넘치지 않을때 비활성화 구현
 
}

## 0712 {
  + 카드 넘칠때 넘기는 기능 구현, 넘치지 않을때 비활성화 구현
 
}


## 0709 {
  + 클릭해서 스크롤 위로 가는 기능 구현
 
}

## 0706 {
 + 클릭해서 스크롤 위로 가는 기능 만들기
 
}

## 0705 {
 + 이벤트
 + 이벤트 생성 및 삭제
 + 
}

## 0704 { 
 +  < Create 해당 메서드 >
 +  document.createElement(element) : HTML 요소 생성
 +  document.appendChild(element) : HTML 요소 추가
 +  
 +  < Delete 해당 메서드 >
 +  document.removeChild(element) : HTML 요소 삭제
 +  document.replaceChild(new, old) : HTML 요소 대체
 +  
 +  < HTML 요소 탐색 >
 +  element.parentNode : 부모 요소
 +  element.nextElementSibling : 현재 요소의 다음 형제 요소
 +  element.previousElementSibling : 현재 요소의 이전 형제 요소
 +  element.children : 자식 요소들 (배열 형태)
}

## 0630 {
 +  CRUD
 +  < Read 해당 메서드(HTML) >
 +  document.getElementById(id) : id 로 찾기
 +  document.getElementsByTagName(name) : 태그로 찾기(배열로 리턴)
 +  document.getElementsByClassName(name) : class이름으로 찾기(배열로 리턴)
 +  document.querySelector(css_selector) : CSS Selector로 찾기(첫번째 요소만)
 +  document.querySelectorAll(css_selector) : CSS Selector로 찾기(모든 요소 찾음 -> 배열로 리턴)

 + < Update 해당 (HTML) >
 + < 프로퍼티 >
 + element.innerText = new html content : 요소 내용 확인/수정하기(태그 미포함)
 + element.innerHTML = new html content : 요소 내용 확인/수정하기(태그 포함)
 + element.attribute = new value : 요소의 attribute 값 수정하기
 + element.style.property = new style : 요소의 CSS 프로퍼티 값 수정하기
 + < 메서드 >
 + element.setAttribute(attribute, value) : 요소의 attribute 값 설정하기


-----------

+ align-items : 세로 방향 정렬
+ justify-items : 가로 방향 정렬
+ align-content : 아이템 그룹 세로 정렬
+ align-self : 개별 아이템 세로 정렬
+ justify-self : 개별 아이템 가로 정렬
+ place-self : 위 두개 단축 속성
}

## 0629 {
 + DOM(Document Object Model) : 
 + DOM + CSSOM => Render tree 생성
 
 + <script></script> 
 + </body> // /body 태그 직전에 script 태크로 코드 파일 형태로 추가하기
 
 + window 와 BOM(Nrowser Object Model)
 + window.alert() => alert() 
 + 생략이 가능하다.
 
 + BOM 의 주요 객체
 + console.log(navigator.userAgent); // 브라우저 정보
 + console.log(navigator.platform); // 운영체제 정보
 + console.log(location.href); // 현재 URL 정보
 
 
 ---------------
 gird-auto-flow : 자동 배치
 
 
}

## 0628 {
 + Promise 객체 : 비동기 작업 수행을 해당 함수를 동기적으로 작업 수행하도록 함
 + then : 순차적으로 동기적으로 이어주는 실행 프로퍼티? success 케이스, error 케이스로 설정 가능
 + catch : 
 
 + Promise의 3가지 상태 : 대기, 이행, 실패
  
 + chaining & return
 + finally
 + Promise.all
 + Promise.race
 
 ---------
 # CSS
 
 + grid-template-areas : 영역 이름으로 그리드 정의,
 + 영역을 직관적으로 배치 가능! (IE 안됨 ㅠ)
 
 
 
}

## 0627 {
 + 동기: 순차적으로 해결된 후에 다음으로 넘어감
 + 비동기: 순차적이지만 해결되지 않아도 다음으로 넘어가서 먼저 실행시킬 수 있음
 
 + Grid의 item 크기 및 위치 조정
 + grid-column: 1 / 3;
 + grid-row: 1 / 2;
}

## 0615 {
 filter, map 개념 인지하기
}


## 0604 {
 클래스는 new 로 생성, 생성자 함수, 상속, 
}

## 0602
{
 객체는 거의 리터럴 방식으로 생성한다
}

## 0531
{
 오늘부터 다시 잡자, 습관부터 다시 잡자
}

## 0530
{
 오늘부터 다시 잡자, 습관부터 다시 잡자
}

## 0515
{
 top, z-index과의 관계 => 위에 모달이 다 덮어져 있어서 클릭을 못하는 상황
 모달이 top으로 header 크기만큼 공간이 생기면 클릭이 가능해짐(아래로 내려감)
 혹은 header 나 icon이 덮은 부위보다 높은 z-index 설정
 width vs max-width
 max-width는 언제부터 적용되는 건가?
}

## 0503
{
  -CSS
  position의 기능 차이
  relative
  absolute
}


## 0403
{
  + 동기적: 어떤 작업을 요청했을 때 그 작업이 종료될때 까지 기다린 후 다음 작업을 수행하는 방식
  + 비동기적: 어떤 작업을 요청했을 때 그 작업이 종료될때 까지 기다리지 않고 다른 작업을 하고 있다가, 요청했던 작업이 종료되면 그에 대한 추가 작업을 수행하는 방식
}

## 0317
{
  ios::sync_with_stdio(false)
}

## 0314
{
  우선순위 큐 vs 큐
}


## 0312
{
  어떤 프론트 엔드가 되고싶은가?
}

## 0206
{
  최대힙 -> 큰수대로 그래프를 만듦 ex) 7 5 3
  최대힙 * -1  => 작은수대로 그래프를 만들수 있게됨 ex) -3 -5 -7  => 출력할때 마이너스하면 
  ```
    cin.tie(0);
    cout.tie(0);
    std::ios::sync_with_stdio(false);
  ```
  scanf VS cin 뭐가 효율이 좋을까?
  
}

## 0110
{
  이진트리의 특징
  왼쪽 자식 노드: 부모 노드 * 2
  오른쪽 자식 노드: 부모 노드 * 2 + 1
}

## 0104
{
  HTML
  section, article, div의 차이란?
  1. 내용이 독립적이고 스스로 설 수 있는 내용이라면 article 사용
  2. 내용이 서로 관계가 있다면 section
  3. 의미적으로 관계가 없다면 div를 사용. (div는 오직 내용을 묶는 역할)
  내용 출처: https://aboooks.tistory.com/346
}
