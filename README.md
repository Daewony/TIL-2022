# TIL-2022

## 0708 {
 + 
 
}

## 0707 {
 + 
 
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


## 0702 {

}

## 0701 {

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

## 0626 {
 
}

## 0616 {
 
}

## 0615 {
 filter, map 개념 인지하기
}

## 0613 {
 
}

## 0610 {
 
}

## 0608 {
 
}


## 0607 {
 
}

## 0606 {
 
}

## 0605 {
 
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
1
}

## 0515
{
 top, z-index과의 관계 => 위에 모달이 다 덮어져 있어서 클릭을 못하는 상황
 모달이 top으로 header 크기만큼 공간이 생기면 클릭이 가능해짐(아래로 내려감)
 혹은 header 나 icon이 덮은 부위보다 높은 z-index 설정
 width vs max-width
 max-width는 언제부터 적용되는 건가?
}

## 0513
{
 
}

## 0509
{
 
}

## 0505
{
 
}

## 0503
{
  -CSS
  position의 기능 차이
  relative
  absolute
}


## 0429
{
  
}

## 0427
{
  
}

## 0424
{
  
}

## 0421
{
  
}

## 0420
{
  
}

## 0418
{
  
}

## 0416
{
  
}

## 0414
{
  
}

## 0413
{
  
}


## 0412
{
  
}

## 0408
{
  .
}

## 0407
{
  .
}

## 0404
{
  
}


## 0403
{
  + 동기적: 어떤 작업을 요청했을 때 그 작업이 종료될때 까지 기다린 후 다음 작업을 수행하는 방식
  + 비동기적: 어떤 작업을 요청했을 때 그 작업이 종료될때 까지 기다리지 않고 다른 작업을 하고 있다가, 요청했던 작업이 종료되면 그에 대한 추가 작업을 수행하는 방식
}


## 0401
{
  
}

## 0330
{
  
}


## 0325
{
  
}

## 0324
{
  
}

## 0323
{
  
}


## 0322
{
  
}

## 0318
{
  
}

## 0317
{
  ios::sync_with_stdio(false)
}

## 0316
{
  
}


## 0315
{
  
}

## 0314
{
  우선순위 큐 vs 큐
}


## 0312
{
  어떤 프론트 엔드가 되고싶은가?
}

## 0310
{

}

## 0309
{

}

## 0308
{

}

## 0307
{

}

## 0306
{

}

## 0305
{

}

## 0304
{

}

## 0303
{

}

## 0302
{

}

## 0301
{

}

## 0227
{

}

## 0226
{

}

## 0223
{

}


## 0222
{

}


## 0221
{

}


## 0220
{

}

## 0218
{

}

## 0217
{

}

## 0216
{

}

## 0215
{

}


## 0214
{

}


## 0213
{

}


## 0211
{

}


## 0211
{

}
## 0211
{

}

## 0210 
{

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

## 0205
{

}

## 0204
{

}

## 0201
{

}

## 0130
{

}

## 0129
{

}

## 0126
{

}

## 0125
{

}

## 0121
{

}

## 0120
{

}

## 0119
{

}

## 0116
{

}


## 0114
{

}

## 0113
{

}

## 0111
{

}

## 0110
{
  이진트리의 특징
  왼쪽 자식 노드: 부모 노드 * 2
  오른쪽 자식 노드: 부모 노드 * 2 + 1
}

## 0109
{

}

## 0108
{

}

## 0107
{

}

## 0106
{

}


## 0105
{

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

## 0103 
{
  소설 잼따
}

## 0101 
{
  z
}
