# 01. Login

## 프로젝트 내용
- 

## 기본 설계
- CSS를 이용해서 스타일링
- theme 파일을 만들어 색상 변수 설정
- 컴포넌화
<br>

## 설계 순서
#### 1) header 요소
- <strong>header 안에는 logo와 menu button으로 구성.</strong>
- 로고를 마크업할 때, a 속성> span 속성 > role="img"를 주어 마크업 함. 
- 찾아보니 브라우저가 텍스트 로고를 이미지로 보도록 강제하는 것은 어떤 실질적인 이점도 없다고 하지만, 현 프로젝트에서는 사실 로고가 텍스트가 아닌 이미지였지 않았을까..하는 생각이 들어 role="img" 를 부여했다. 
- 버튼 초기화 해주는 all 단축 속성 사용 [관련 문서](https://inpa.tistory.com/entry/CSS-%F0%9F%93%9A-all-%EC%86%8D%EC%84%B1-%EA%B8%B0%EB%B3%B8-%EB%94%94%EC%9E%90%EC%9D%B8-%EB%A6%AC%EC%85%8B)
```css
button{
    all: unset; 
}
```
<br>


#### 2) form 요소
- <strong>제목과 언더라인 묶음 / Name, Email, Password 컴포넌트 묶음 / 'Have an account? Signup' 묶음 / 제출 버튼 컴포넌트 순으로 구성.</strong>
- Get started 버튼을 만들때 고민한 것   
-1.1) 회원가입 폼 제출이므로 제출에 용이하도록 a태크에 "role=button"을 주는 것보다 button 태그가 더 나을 것.
-1.2) input태그에 "type=button"을 주지 않고 네이티브 마크업인 button 태그를 선택했음. [form에서 button태그를 사용하는 이유](https://developer.mozilla.org/ko/docs/Web/HTML/Element/input/button)
-2) 'Get started'이란 텍스트를 보조기기로 읽었을 때 '회원가입 폼 제출 및 다음 단계'란 의미가 다 포함될지 고민스러웠다. 그래서 aria-label 속성을 부여할까 싶었는데, 사실 가장 좋은 방법은 버튼 텍스트를 바꾸는게 아닐까 싶었다. 그래서 챗gpt에게 물어봤다. 개인적으로 Create Account가 의미를 잘 담는다고 생각해 이걸로 선택했다.
```Bash
Sign Up
Create Account
Join Now
Register
Get Started
Join Us
Become a Member
Start Your Journey
Register Now
Sign Up Today
```
<br>


#### 3) 배경 이미지 요소
- <strong>배경에 있는 글씨를 main과 sub로 나눠 구성.</strong>
<br>


#### 3) footer 요소
- <strong>home으로 이동하는 버튼과 copyright 문구로 구성.</strong>
- footer를 만들 때 고민한 것
-1) footer는 보통 구획의 작성자나 저작권 정보, 관련 문서 내용 등을 담는데 home으로 이동하는 버튼은 보다 더 중요한 역할을 하고 있기에 같이 footer 태그로 묶어도 될지 고민스러웠다. 일단은 div 태그에서 class="footer"로 작성함. 
<br>

## 구현 못한 부분
- Name, Email, Password 컴포넌트의 label 크기 없애기
- 배경 우측 반원 그래픽..
<br>

## 아쉬운 부분
- 좀 더 시맨틱한 마크업 + 접근성 고려
- 브라우저 크기에 따라 구성 달리 해봤으면 어땠을까 싶음. (배경 텍스트가 가려지는 문제를 해결하기 위해..!)


### 뒤늦게 md 작성 예시를 봤네요..! 2차부턴 지키겠습니다