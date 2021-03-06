# 프론트엔드 개발과 TDD

### 기존 개발의 문제점들

- 클라이언트 측 자바스크립트를 다루는 것은 복잡하다

  - 서버쪽은 node.js 버전을 마음대로 변경할 수 있다.
  - 클라이언트 쪽은 사용자가 사용할 브라우져 버전을 강제할 수 없다.

- 자바스크립트 언어 자체의 특징

  - console.log 함수가 매우 쉽게 덮어 쓰여질 수 있다.
  - 의도된 언어 스팩이지만 개발자들이 실수할 가능성이 높다.

- 타입 

  - '1' + 1 = '11'  string 반환
  - '2' * 3 = 6 number 반환
  - 1  + '2' + 3 * 4 = '1212' string 반환

  이러한 문제를 극복하기 이해 테스트주도개발(TDD)



### 테스트 프레임웍

- Jasmine
- Jest

**.... 많은 테스트 프레임웍이 있다**

#### 자스민 프레임웍 설치

자스미은 피보탈 랩스에서 만든 BDD(Behavior Driven Development) 프레임웍크로서 자동화된 단위 테스트 도구

**단위테스트(unit test)란** 코드의 기능단위를 테스트

- 무엇이 기능인가? 결정하기 쉽지 않다.
- TDD를 다른 관점에서 바라본 BDD라는 해결책을 제시

**BDD**

- 유저 스토리 개념을 끌어드린 테스트 방법
- 예를 들어 어떤 버튼을 클릭하면 경고 창을 띄우는 유저 스토리 
  - Given : 초기 상황
  - When : 어떤 이벤트가 발생
  - Then : 후속 결과를 기대

```javascript
describe('어떤 버튼은', ()=>{
  describe('클릭했을 때', ()=>{
    it('경고창을 띄운다', ()=>{
      
    })
  })
})
```

**단위 테스트를 스팩(spec)이라고 함**

* [getting_started](https://jasmine.github.io/pages/getting_started.html)
* 두 가지 설치 방법: 스탠드어론, 노드JS 
  * 스탠드어론으로 설치 하겠음 
* 러너
  * 자스민 코드와 소스 파일, 스펙을  파일을 참조하는 html 파일 
  * setting/index.html 파일 확인 
* 헬로월드 
  * `checkout` 

  #### 자스민 2가지 설치 방법
  - 스탠드얼론 (standalone)
    - 모든 자스민 코드를 브라우저에 올리는 방법 / 간단함 / 실무에선 많이 쓰이지 않음 / 수많은 코드를 테스트 하고 자동화 하기위해선 카르마와 함께 설치
  - 카르마(karma)와 함께 설치 (자동화)