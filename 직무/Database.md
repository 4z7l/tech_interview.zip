# Database

<h2>데이터베이스</h2>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>키 종류</strong></span></summary>
<hr>
  <ul>
     <li>
        <strong>후보키 </strong>: 유일성과 최소성을 만족한 키
        <ul>
           <li>유일성 : 해당 키로 하나의 튜플을 식별할수있음</li>
        </ul>
        <ul>
           <li>최소성 : 꼭 필요한 속성으로만 이루어짐</li>
        </ul>
     </li>
  </ul>
  <ul>
     <li><strong>기본키 </strong>: 후보키들 중 하나, Null 가질 수 없음, 동일한 값을 가질수없음</li>
  </ul>
  <ul>
     <li><strong>대체키/보조키</strong> : 기본키를 제외한 후보키</li>
  </ul>
  <ul>
     <li><strong>외래키 </strong>: 다른 릴레이션의 속성, 참조 관계를 표현하는 데에 쓰임</li>
  </ul>
  <ul>
     <li><strong>슈퍼키 </strong>: 유일성은 만족하지만 최소성은 만족하지 못하는 키</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>JOIN에 대해서 설명해 주세요.</strong></span></summary>
<hr>
  <p>두 가지 이상의 릴레이션을 연결해서 데이터를 검색하는 기법</p>
  <p>RDBMS에서는 릴레이션끼리 관계를 가지고 있는데, 각 테이블에 저장된 데이터를 효과적으로 검색하기 위해 조인이 필요하다.</p>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>내부 조인, 외부 조인, 셀프 조인</strong></span></summary>
<hr>
  <p><strong>내부 조인(Inner Join) : </strong>가장 기본적인 조인</p>
  <figure/></a></figure>
  <ol>
     <li>동등 조인(EQUI Join) : 동등 비교(=) 사용</li>
  </ol>
  <ol>
     <li>자연 조인(Natural Join) : 동일한 컬럼명을 가진 테이블에서 모든 컬럼 비교</li>
  </ol>
  <figure/></a></figure>
  <p>3. 교차 조인(Cross Join) : 곱집합 반환, 모든 경우의 수(M*N)</p>
  <p></p>
  <p><strong>외부 조인(Outer Join)</strong> : 특정 테이블의 데이터가 모두 필요한 경우</p>
  <figure/></a></figure>
  <figure/></a></figure>
  <ol>
     <li>Left Outer Join : 좌측 테이블의 모든 결과값 포함</li>
  </ol>
  <ol>
     <li>Right Outer Join : 우측 테이블의 모든 결과값 포함</li>
  </ol>
  <p></p>
  <p><strong>셀프 조인 (Self Join)</strong> : 자기 자신과 자기 자신 결합</p>
  <figure/></a></figure>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>SQL Injection이란</strong></span></summary>
<hr>
  <p>해커에 의해 조작된 쿼리문에 DB에 그대로 전달되어 비정상적 명령을 실행시키는 공격 기법</p>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>파티셔닝과 샤딩에 대해서 설명해 주세요.</strong></span></summary>
<hr>
  <p><strong>파티셔닝</strong></p>
  <ul>
     <li>데이터를 여러 DB에 분산시키는 것</li>
  </ul>
  <ul>
     <li>X테이블의 일부 데이터는 A에, Y테이블의 일부 데이터는 B에</li>
  </ul>
  <p><strong>수평 단편화/수평 파티셔닝/샤딩</strong></p>
  <ul>
     <li>데이터를 수평으로 쪼갠다</li>
  </ul>
  <p><strong>수직 단편화/수직 파티셔닝</strong></p>
  <ul>
     <li>수직으로 칼럼을 쪼갬</li>
  </ul>
  <ul>
     <li>칼럼을 나눠서 새로운 테이블로 갖고있는 것</li>
  </ul>
  <ul>
     <li>특정 컬럼이 빈번하게 참조될때, 여러 데이터가 캐시에 올라갈수있음</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>ORM이란 무엇인가요?</strong></span></summary>
<hr>
  <p><strong>ORM (Object - Relation Mapping)</strong></p>
  <ul>
     <li>객체-관계 매핑</li>
  </ul>
  <ul>
     <li>객체지향적인 코드로 비즈니스 로직에 집중 가능</li>
  </ul>
  <ul>
     <li>객체와 RDBMS간의 매핑을 하는 것</li>
  </ul>
  <ul>
     <li>재사용 및 유지보수 용이</li>
  </ul>
  <ul>
     <li>DBMS에 대한 종속성 감소</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>NoSQL이란 무엇인가요?</strong></span></summary>
<hr>
  <p><strong>NoSQL</strong></p>
  <ul>
     <li>RDBMS와 달리 다른 형태의 데이터 저장</li>
  </ul>
  <ul>
     <li>데이터 간의 관계 저장하지않음</li>
  </ul>
  <ul>
     <li>고정되지않은 테이블 스키마</li>
  </ul>
  <p><strong>장점</strong></p>
  <ul>
     <li>유연함, 언제든지 저장된 데이터를 조정하고 새로운 필드를 추가할수있음</li>
  </ul>
  <ul>
     <li>데이터는 애플리케이션이 필요로 하는 형식으로 저장됨</li>
  </ul>
  <p><strong>단점</strong></p>
  <ul>
     <li>중복을 계속 업데이트해야 함</li>
  </ul>
  <ul>
     <li>데이터 구조 결정을 미루게 될 수 있음</li>
  </ul>
  <ul>
     <li>수정 시 중복된 모든 컬렉션에서 수행해야함</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>스키마란 무엇인가요?</strong></span></summary>
<hr>
  <p>DB의 구조와 제약조건에 관해 명세를 기술한 것</p>
  <figure/></a></figure>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>View란 무엇인가요?</strong></span></summary>
<hr>
  <ul>
     <li>가상테이블</li>
  </ul>
  <ul>
     <li>보안관리, 편의, 수행속도 향상</li>
  </ul>
  <ul>
     <li>저장장치 내에 물리적으로 존재하지는 않음 </li>
  </ul>
  <ul>
     <li>필요한 데이터만 뷰로 정의할수있음</li>
  </ul>
  <ul>
     <li>독립적 인덱스 불가능, CRUD에 제약이 있음</li>
  </ul>

<hr>
</details>
<p></p>
<h2>정규화</h2>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>이상 현상에 대해서 설명해 주세요.</strong></span></summary>
<hr>
  <p>데이터의 중복으로 인한 부작용을 말합니다</p>
  <ol>
     <li><strong>삽입 이상 : </strong>데이터를 삽입하는 데 필요없는 속성도 함께 추가해야함</li>
  </ol>
  <ol>
     <li><strong>갱신 이상 : </strong>데이터를 갱신한 이후 일관성이 위반됨</li>
  </ol>
  <ol>
     <li><strong>삭제 이상 : </strong>데이터를 삭제하는 데 의도하지 않은 것이 함께 삭제됨, 정보 손실이 일어남</li>
  </ol>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>정규화에 대해서 설명해 주세요.</strong></span></summary>
<hr>
  <p><strong>정규화</strong>란 RDBMS에서 중복을 최소화하기 위해 데이터를 분해하는 작업을 말합니다.</p>
  <p>정규화를 함으로써 이상현상을 방지할 수 있다는 장점이 있고, 릴레이션 간의 연산이 많아질 수 있다는 단점이 있습니다.</p>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>반정규화란?</strong></span></summary>
<hr>
  <p><strong>반정규화</strong>는 성능 향상을 위해 중복,통합을 하는 기법이다.</p>
  <p>조인으로 인한 성능 저하가 예상되는 경우 반정규화를 실행한다.</p>
  <p>반정규화를 과도하게 적용하면 무결성이 깨질수있다.</p>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>정규화의 종류에 대해서 말해보세요.</strong></span></summary>
<hr>
  <p><strong>제 1 정규형</strong> : 도메인이 <strong>원</strong>자값만을 포함함</p>
  <p><strong>제 2 정규형</strong> : <strong>완</strong>전 함수적 종속</p>
  <p><strong>제 3 정규형</strong> : 기본키에 대해 <strong>이</strong>행적 종속 제거</p>
  <p><strong>BCNF 정규형</strong> : 모든 결정키가 <strong>후</strong>보키</p>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>함수적 종속성이란 무엇인가요?</strong></span></summary>
<hr>
  <p><code>X → Y</code> : 릴레이션 R에서 <strong>X값을 알면 Y를 알 수 있고, X 값에 의해 Y값이 달라질 때</strong>, Y는 X에 함수적 종속이다.</p>

<hr>
</details>
<p></p>
<h2>인덱스</h2>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>인덱스란 무엇인가요? 어떻게 동작 하나요?</strong></span></summary>
<hr>
  <p><strong>인덱스</strong></p>
  <ul>
     <li>RDBMS에서 검색 연산의 속도를 높이기 위한 방법</li>
  </ul>
  <ul>
     <li>항상 정렬된 상태를 유지하므로 탐색이 빠르다</li>
  </ul>
  <ul>
     <li>데이터 삽입/삭제/수정 시에는 추가적인 작업이 필요하므로 실행 속도가 느려진다.</li>
  </ul>
  <ul>
     <li>저장 성능을 희생하고 데이터 읽기 속도를 높이는 기능</li>
  </ul>
  <p><strong>인덱스 자료구조</strong></p>
  <ul>
     <li>B+- Tree : 일반적으로 사용됨</li>
  </ul>
  <ul>
     <li>Hash : 해시 값을 계산해 검색하므로 빠르나 부분 검색을 할 수 없음</li>
  </ul>
  <p><strong>인덱스를 사용하면 좋은 경우</strong></p>
  <ul>
     <li>where 절에서 자주 사용되는 Column</li>
  </ul>
  <ul>
     <li>외래키에 사용되는 Column</li>
  </ul>
  <ul>
     <li>Join에 자주 사용되는 Column</li>
  </ul>
  <p><strong>인덱스를 피해야 하는 경우</strong></p>
  <ul>
     <li>데이터의 중복도가 높은 Column</li>
  </ul>
  <ul>
     <li>삽입, 삭제, 수정 연산이 자주 일어나는 Column</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>인덱스의 알고리즘에는 어떤 것들이 있나요?</strong></span></summary>
<hr>
  <ol>
     <li><strong>B Tree 인덱스 알고리즘</strong> : 칼럼의 값을 변형하지 않고 원래의 값으로 인덱싱, 등호 뿐만 아니라 부등호 연산에도 적용 가능</li>
  </ol>
  <ol>
     <li><strong>Hash 인덱스 알고리즘</strong> : 해시값을 이용해 인덱싱</li>
  </ol>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>Table Full Scan과 Index Range Scan 을 설명해주세요.</strong></span></summary>
<hr>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>클러스터드 인덱스와 비클러스터드 인덱스란 무엇인가?</strong></span></summary>
<hr>
  <p><strong>클러스터드 인덱스</strong></p>
  <ul>
     <li>테이블당 하나만 생성 가능</li>
  </ul>
  <ul>
     <li>인덱스로 지정한 열에 맞춰 자동 정렬</li>
  </ul>
  <p><strong>비클러스터드 인덱스</strong></p>
  <ul>
     <li>테이블당 여러개 생성 가능</li>
  </ul>

<hr>
</details>
<p></p>
<h2>트랜잭션</h2>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>트랜잭션이란 무엇인가요? 4가지 원칙을 포함해서 설명해 주세요.</strong></span></summary>
<hr>
  <p><strong>트랜잭션</strong> : 데이터베이스의 상태를 변경시키는 작업의 단위</p>
  <p><strong>4가지 특징 ACID</strong></p>
  <ul>
     <li>Atomicity(원자성) : 트랜잭션의 연산은 모두 반영되어야하며, 하나라도 실패하면 모두 취소되어야한다.</li>
  </ul>
  <ul>
     <li>Consistency(일관성) : 트랜잭션을 성공하면 언제나 일관성있는 데이터베이스 상태로 변화한다.</li>
  </ul>
  <ul>
     <li>Isolation(독립성, 격리성) : 둘 이상의 트랜잭션이 동시에 수행되는 경우 다른 트랜잭션의 연산에 끼어들수없다.</li>
  </ul>
  <ul>
     <li>Durability(지속성) : 완료된 트랜잭션은 영구적으로 반영되어야한다.</li>
  </ul>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>트랜잭션의 격리 수준과 각 수준에서 발생할 수 있는 문제들에 대해 말해보세요.</strong></span></summary>
<hr>
  <p><strong>트랜잭션 격리 수준(Isolation level)</strong></p>
  <p>: 트랜잭션에서 일관성 없는 데이터를 허용하는 수준</p>
  <ol>
     <li><strong>레벨 0 - Read Uncommitted
        </strong>트랜잭션에 처리중이거나, 아직 Commit되지 않은 데이터를 다른 트랜잭션이 읽는 것을 허용함
     </li>
  </ol>
  <ol>
     <li><strong>레벨 1 - Read Committed
        </strong>Commit이 이루어진 트랜잭션만 조회 가능
     </li>
  </ol>
  <ol>
     <li><strong>레벨 2 - Repeatable Read
        </strong>트랜잭션이 범위 내에서 조회한 데이터 내용이 항상 동일함을 보장함
        다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 수정 불가능
     </li>
  </ol>
  <ol>
     <li><strong>레벨 3 - Serializable
        </strong>다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 수정 및 입력 불가능
     </li>
  </ol>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>공유 락과 배타 락의 차이는 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>데드락이란 무엇이며, 어떻게 발생할까요?</strong></span></summary>
<hr>

<hr>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>Commit과 Rollback이란 무엇인가요?</strong></span></summary>
<hr>
  <p><strong>Commit</strong></p>
  <ul>
     <li>모든 작업을 정상적으로 처리하겠다고 확정하는 명령</li>
  </ul>
  <ul>
     <li>실제 DB에 저장</li>
  </ul>
  <ul>
     <li>Commit 수행 후 하나의 트랜잭션을 종료하게 됨</li>
  </ul>
  <p><strong>Rollback</strong></p>
  <ul>
     <li>작업 중 문제가 발생하면 변경사항을 취소하고 트랜잭션을 종료함</li>
  </ul>
  <ul>
     <li>이전 commit까지만 복구함</li>
  </ul>
  <p><strong>장점</strong></p>
  <ul>
     <li>데이터 무결성 보장</li>
  </ul>

<hr>
</details>
