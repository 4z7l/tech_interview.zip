# Software Engineering

<h2>객체지향</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>객체지향이 무엇인가요? 절차지향과의 차이점은 뭐죠?</strong></span></summary>
<hr>
   <p><strong>객체지향(OOP; Object Oriented Programming)
      </strong>: 현실세계를 기반해서 모델링하는 프로그래밍 기법
      - 세부모델부터 디자인하는 Bottom-UP 방식
      - 추상화, 캡슐화, 상속, 다형성
   </p>
   <ul>
      <li>장점 : 코드 재활용성 높음, 디버깅 쉬움</li>
   </ul>
   <ul>
      <li>단점 : 처리속도가 절차지향보다 느림, </li>
   </ul>
   <ul>
      <li>언어 : JAVA, Python, C#</li>
   </ul>
   <p><strong>절차지향(PP; Procedural Programming)</strong>
      : 프로시저 호출의 개념을 바탕으로 하는 프로그래밍 기법
      - 데이터와 함수를 별개로 처리함
      - 큰 기능을 작은 단위로 나누어 처리하는 Top-Down 방식
   </p>
   <ul>
      <li>장점 : 실행 속도 빠름</li>
   </ul>
   <ul>
      <li>단점 : 유지보수 어려움, 디버깅 어려움</li>
   </ul>
   <ul>
      <li>언어 : C, Portran, Basic</li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>객체지향 SOLID 원칙에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>객체지향 4가지 특징에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <h3>추상화</h3>
   <ul>
      <li>추상적인 개념에 의존해서 설계</li>
   </ul>
   <ul>
      <li>사물의 공통적인 특징을 도출함</li>
   </ul>
   <h3>캡슐화</h3>
   <ul>
      <li>실제 구현 내용을 감추는 것</li>
   </ul>
   <ul>
      <li>낮은 결합도를 유지할 수 있도록 설계하는 것</li>
   </ul>
   <ul>
      <li>정보은닉의 개념을 활용함</li>
   </ul>
   <ul>
      <li>변경이 일어나도 다른 모듈에 영향을 최소화할 수 있음</li>
   </ul>
   <h3>상속</h3>
   <ul>
      <li>이미 정의된 부모 클래스의 메소드와 속성을 자식 클래스가 물려받는 것</li>
   </ul>
   <ul>
      <li>재사용성 높아짐</li>
   </ul>
   <ul>
      <li>단점 : 부모 클래스의 변경이 어려워진다 → IS-A 관계가 성립할때만 상속함으로써 해결</li>
   </ul>
   <h3>다형성</h3>
   <ul>
      <li>오버로딩, 오버라이딩과 관련</li>
   </ul>
   <ul>
      <li>구체적으로 어떤 클래스의 객체가 참조되는 지와 무관하게 여러 형태를 받아들임으로써 프로그래밍 가능</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>대표적인 객체지향 언어에는 어떤 것들이 있나요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>함수형 프로그래밍에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>클래스, 객체, 인스턴스 차이에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <ul>
      <li><strong>클래스 </strong>: 객체를 만들어내기 위한 설계도나 틀, 연관되어 있는 메소드나 변수의 집합</li>
   </ul>
   <ul>
      <li><strong>객체 </strong>: 클래스의 인스턴스 , 구현할 대상</li>
   </ul>
   <ul>
      <li><strong>인스턴스 </strong>: 구현된 구체적인 실체, 메모리에 할당됨, 메모리에 생성한 객체</li>
   </ul>
   <p>클래스는 연관된 여러 데이터와 메소드로 이루어진 집합체를 말합니다.</p>
   <p>객체는 클래스의 구현해야할 대상을 말하고</p>
   <p>인스턴스는 메모리에 할당된 구현된 실체를 말합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>순수 추상 클래스와 인터페이스의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p><strong>추상 클래스</strong></p>
   <ul>
      <li>추상 메소드를 한 개 이상 포함한 클래스</li>
   </ul>
   <ul>
      <li>서브 클래스에게 추상 메소드의 구현을 강제함</li>
   </ul>
   <ul>
      <li><strong>기능을 확장</strong>하는 데에 목적</li>
   </ul>
   <p><strong>인터페이스</strong></p>
   <ul>
      <li>추상메소드와 변수로만 이루어짐</li>
   </ul>
   <ul>
      <li>서브 클래스에게 메소드의 원형을 알려주어 자신의 목적에 맞게 메소드를 구현할 수 있게 함</li>
   </ul>
   <p><strong>공통점</strong></p>
   <ul>
      <li>인스턴스 생성 불가능</li>
   </ul>
   <ul>
      <li>서브 클래스가 기능을 구현하도록 책임을 위임함</li>
   </ul>
   <p><strong>차이점</strong></p>
   <ul>
      <li>추상클래스는 클래스 O, 인터페이스는 클래스 X</li>
   </ul>
   <ul>
      <li>추상클래스는 다중상속 불가능, 인터페이스는 다중상속 가능</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>인터페이스는 주로 언제 사용하나요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>오버로딩과 오버라이딩의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <ul>
      <li>오버로딩 : 같은 이름을 가진 메소드를 추가하는 것</li>
   </ul>
   <ul>
      <li>오버라이딩 : 부모 클래스의 메소드를 자식 클래스가 재정의 하는 것. </li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>업캐스팅과 다운캐스팅이란?</strong></span></summary>
<hr>
   <p>업캐스팅</p>
   <ul>
      <li>서브클래스의 객체가 수퍼클래스로 형변환됨</li>
   </ul>
   <ul>
      <li>수퍼클래스 변수로 서브클래스 가리킴</li>
   </ul>
   <ul>
      <li>이유 : instanceof 할 필요없이 부모타입으로 가리킬수있음, 코드 재사용성 높임</li>
   </ul>
   <p>다운캐스팅</p>
   <ul>
      <li>업캐스팅 상태를 원상태로 복구</li>
   </ul>
   <ul>
      <li>원래의 서브클래스로 복구. 명시적으로 형변환</li>
   </ul>
   <ul>
      <li>이유 : 서브클래스의 각자의 고유기능에 접근하기 위해</li>
   </ul>

<hr>
</details>

<p></p>
<p></p>
<h2>디자인 패턴</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>디자인 패턴이란 무엇인가요?</strong></span></summary>
<hr>
   <p>반복적으로 일어나는 방법론을 어떻게 풀어나갈 것인가에 대한 솔루션</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>추상 팩토리 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>생성 패턴</li>
   </ul>
   <ul>
      <li>클래스에서 실제 구현부를 정의하지 않고 팩토리 클래스에 인스턴스 생성을 요청함</li>
   </ul>
   <ul>
      <li><strong>장점</strong> : 클라이언트 코드와 구현 분리 가능, 객체 간의 일관성 증진, 구현부 쉽게 수정 가능</li>
   </ul>
   <ul>
      <li><strong>단점</strong> : 새로운 종류의 product 제공 어려움</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>싱글톤 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>생성 패턴</li>
   </ul>
   <ul>
      <li>어떤 클래스의 인스턴스는 하나임을 보장함</li>
   </ul>
   <ul>
      <li>전역적인 접근점 제공, 공통된 객체를 여러곳에서 접근해야 하는 경우</li>
   </ul>
   <ul>
      <li><strong>장점</strong> : 인스턴스로의 접근을 통제, 접근 캡슐화</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>빌더 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>생성 패턴</li>
   </ul>
   <ul>
      <li>복잡한 객체를 생성하는 클래스와 표현하는 클래스를 분리</li>
   </ul>
   <ul>
      <li>복합적인 객체를 생성하는 과정을 세밀하게 분리할 수 있음</li>
   </ul>
   <ul>
      <li>생성과 표현을 분리</li>
   </ul>
   <ul>
      <li>데이터가 늘어난다면 매번 생성자를 만들어야하는데 그러지않아도됨</li>
   </ul>
   <ul>
      <li>명시적이다</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>팩토리 메소드 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>생성 패턴</li>
   </ul>
   <ul>
      <li>어떤 객체를 생성할지 서브클래스가 결정함</li>
   </ul>
   <ul>
      <li>자신이 어떤 객체를 생성해야할지 모를 때</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>옵저버 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>행위 패턴</li>
   </ul>
   <ul>
      <li>객체의 상태 변화를 관찰해 변화가 발생하면 변화를 통지받고 자동으로 갱신될 수 있게 함</li>
   </ul>
   <ul>
      <li>분산 이벤트 핸들링 시스템에 주로 사용</li>
   </ul>
   <ul>
      <li>객체가 변경되어야하는데 얼마나 많은 객체들이 변경되어야 하는지 모를 때</li>
   </ul>
   <ul>
      <li>장점 : subject와 observer 사이에 추상적인 결합도만 존재</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>어댑터 패턴이란?</strong></span></summary>
<hr>
   <ul>
      <li>구조 패턴</li>
   </ul>
   <ul>
      <li>클래스의 인터페이스를 사용자가 기대하는 다른 인터페이스로 변환하는 패턴</li>
   </ul>
   <ul>
      <li>ex) 리사이클러뷰의 어댑터는 데이터 리스트로부터 아이템 뷰를 만들어냄</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>뷰홀더 패턴이란?</strong></span></summary>
<hr>

<hr>
</details>

<p></p>
<h2>기타</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>프레임워크와 라이브러리 차이는 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Monolitc Architecture, Micro Service Architecture에 대해 각각 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>애자일 방법론이란?</strong></span></summary>
<hr>
   <p>반복적인 개발 주기를 통해서 소프트웨어를 개발하는 방법</p>
   <p>피드백을 받아서 유동적으로 개발함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>컴파일러와 인터프리터의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p><strong>컴파일러</strong></p>
   <ul>
      <li>전체 소스코드를 훑으며 명령어를 수집하고 재구성</li>
   </ul>
   <ul>
      <li>소스코드를 기계어로 바꿈</li>
   </ul>
   <ul>
      <li>OS와 빌드 환경에 종속적</li>
   </ul>
   <p><strong>인터프리터</strong></p>
   <ul>
      <li>번역시간은 빠르지만 실행시간은 컴파일러보다는 느림</li>
   </ul>
   <ul>
      <li>소스코드를 한 줄씩 읽으며 기계어로 바꿈</li>
   </ul>
   <ul>
      <li>프로그램 수정이 간단하다</li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>1급 객체에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>char type과 string type으로 나뉘어져 있는 이유는 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>클린코드란?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TDD란?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>리눅스 시스템의 i-node에 대해서 설명해 보아라</strong></span></summary>
<hr>

<hr>
</details>
