# Kotlin


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>자바와 코틀린 차이점</strong></span></summary>
   <hr>
   <p>코틀린 : Null에 안전</p>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>함수형 프로그래밍이란</strong></span></summary>
   <hr>
   <ul>
      <li>함수도 객체로 취급</li>
   </ul>
   <ul>
      <li>코드 간략, 재사용성 증가</li>
   </ul>
   <ul>
      <li>람다식, 고차함수, 순수함수</li>
   </ul>
   <ul>
      <li>모듈화 하므로 디버깅, 테스트 용이</li>
   </ul>
   <ul>
      <li>생산성 높다</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>코틀린 장점</strong></span></summary>
   <hr>
   <ul>
      <li>문법이 간결하다</li>
   </ul>
   <ul>
      <li>컴파일 타임에 Null을 체크하므로 Null 안전하다</li>
   </ul>
   <ul>
      <li>JVM을 기반으로 하므로 자바에서 제공하는 Collection을 그대로 사용할수있음</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>sealed class VS data class</strong></span></summary>
   <hr>
   <p><strong>sealed class</strong></p>
   <ul>
      <li>하위 클래스의 종류를 제한</li>
   </ul>
   <ul>
      <li>객체 생성 불가능</li>
   </ul>
   <ul>
      <li>하위 클래스는 class, data class, object 가능</li>
   </ul>
   <ul>
      <li>when절에서 else문 필요없음</li>
   </ul>
   <ul>
      <li>sealed의 하위 클래스들은 객체 여러개 생성 가능 → enum은 인스턴스 하나임</li>
   </ul>
   <p><strong>data class</strong></p>
   <ul>
      <li>데이터만 담기 위한 클래스</li>
   </ul>
   <ul>
      <li>getter/setter 자동 생성</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>고차함수 vs 순수함수 vs 일급객체</strong></span></summary>
   <hr>
   <p><strong>고차함수</strong></p>
   <ul>
      <li>함수를 인자로 전달받거나 함수를 반환하는 함수</li>
   </ul>
   <p><strong>순수함수</strong></p>
   <ul>
      <li>side effect 없음 : 입력이 같으면 출력이 같다</li>
   </ul>
   <p><strong>일급객체</strong></p>
   <ul>
      <li>함수의 인자로 전달 가능</li>
   </ul>
   <ul>
      <li>함수의 반환값에 사용 가능</li>
   </ul>
   <ul>
      <li>변수에 담을 수 있음</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>obejct vs companion object</strong></span></summary>
   <hr>
   <p><strong>object</strong></p>
   <ul>
      <li>클래스를 정의하면서 객체 생성</li>
   </ul>
   <ul>
      <li>상속 가능</li>
   </ul>
   <p><strong>companion object</strong></p>
   <ul>
      <li>코틀린에는 static 없다</li>
   </ul>
   <ul>
      <li>말그대로 동반 객체임</li>
   </ul>
   <ul>
      <li>클래스의 private 데이터에 접근 가능</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>lateinit VS by lazy</strong></span></summary>
   <hr>
   <p><strong>lateinit</strong></p>
   <ul>
      <li>var</li>
   </ul>
   <ul>
      <li>primitive에 사용 불가능</li>
   </ul>
   <ul>
      <li>null을 통한 초기화 불가능</li>
   </ul>
   <p><strong>by lazy</strong></p>
   <ul>
      <li>val</li>
   </ul>
   <ul>
      <li>기본 synchronized로 동작</li>
   </ul>
   <hr>
</details>
<details>
   <summary><span style="border-bottom:0.05em solid"><strong>let, apply, run, with 차이점</strong></span></summary>
   <hr>
   <hr>
</details>
