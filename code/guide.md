# Guide 

--- 

## File Structure 

### 웹페이지 구성시 준비사항 
1. 기본자료 
  - 변수 선언 : 색상 / font 
  - @mixin 세팅 : font작업 세팅, size, 이미지 설정 ... 
  - reset, common : 회사의 기본 가이드 작업을 위한 기반/ 초기 세팅

2. 작성 : 코드를 의미있게 작성하는  습관

3. id는 안티패턴?? → html 에서 id 속성은 기본의미가 "유일한 값", "label에서 input과 연동", "anker의 역할(찾아갈 수 있게 해줌)로 연동됨" 등 이므로... 그 의미에 맞게 id를 사용해야함

4. css에서 선택자 사용시 3단계까지만 유효 
(cf. scss의 nesting 기법에서도 3단계까지만 중첩해서 작성, 아니면 @at-root을 활용!)
    
  ```css
    // css 
    #wrap {
    	margin: auto;
    	> div {width: 100%;}
    	@at-root .box {height: 300px;}
    }
    
    // ----------------------------
    
    /* scss */ 
    #wrap {margin: auto;}
    #wrap > div {width: 100%;}
    .box {height: 300px;} 
  ```
5. 이름 부여시
  a. id 설정: **camelCase**
  b. class 설정:** snake_case **
  c. name 설정: id 이름과 동일하지만 구분형식(**double__Under__Score**)으로 `_` 를 두개 연속 삽입 
  d. naming 방식: `BEM` (**block element modifier**) 
    → 여기서 **element**는 **요소** 
      e.g. html에서는 \<div>\<ul>, js는 [1, 2, 3, 4,] ... 
      즉, **의미를 갖는 최소한의 단위**를 의미! 
      e.g.
          level 구성: `Box -> area -> inner -> part -> content -> detail`
      e.g. 
          hungarian notation(헝가리안) 구성: js 에서 DOM 선택자 사용시 
  e. 상태 처리 (class 첨부): 
    1. 마우스 올린 상태 :  e.g. **mouse**
    2. 선택 (체크) 된 상태: **select** 
    3. focus처리 상태: **focus** 
    4. 자료가 나타나있는 상태 : **on**
    5. error 표시: **err**
    6. success 표시: **suc** 
    7. warning 표시 : **warn**
    8. 기타 상태 체크 (대표 예시): **act**, **run**, **pause**

<br />
<br />

### Directory 구성:
- 📂  아이콘은 폴더를 의미하며,  첨부된 형태는 폴더명이며 고정이름
- 🗂  아이콘은 폴더를 의미하며, 사용이름 또는 한글이름의 폴더는 임의로 변경가능
- 📕  아이콘은 파일을 의미하며, 일부 아이콘 없이 이름으로 처리한 형태도 존재
- 📜  아이콘은 파일을 의미하며, 사용자가 임의로 변경 가능
- 파일명 앞에 '_' 붙은 형태는 암묵적 파일의 의미로 해석 → 변환 X

<br />
<br />

<!-- ### File Naming 기법 -->
--- 
