# Data Structure

<h2>자료구조</h2>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>배열과 링크드 리스트의 차이점에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <p>배열은 메모리에 할당될 때 연속적인 데이터 공간에 할당이 됩니다.</p>
      <p>데이터에 접근할 때 random access가 가능하므로 빠르지만, 삽입 삭제 시에나 배열의 크기를 유동적으로 변하기 어렵습니다.</p>
      <p>링크드 리스트는 메모리에 할당될 때 흩어져서 저장됩니다.</p>
      <p>처음에 크기를 지정해주지 않아도되며 삽입 삭제가 빠르지만 검색시 순차접근을 통해서 접근해야하므로 느립니다.</p>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>스택과 큐에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <p><strong>스택</strong></p>
      <ul>
         <li>가장 마지막으로 들어온 자료가 먼저 나가는 후입선출(LIFO)</li>
      </ul>
      <ul>
         <li>ex) 재귀 알고리즘, 함수의 스택프레임 저장, 뒤로가기</li>
      </ul>
      <p><strong>큐</strong></p>
      <ul>
         <li>먼저 들어온 자료가 먼저 나가는 선입선출(FIFO)</li>
      </ul>
      <ul>
         <li>데이터가 들어간 순서대로 처리되어야 할 때 사용</li>
      </ul>
      <ul>
         <li>ex) BFS, 프로세스 관리, CPU 스케줄링</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>우선순위 큐에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <ul>
         <li>우선순위를 가지고 있는 큐</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>해시테이블에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <ul>
         <li>key-value를 함께 저장하는 자료구조</li>
      </ul>
      <ul>
         <li>key를 통해 value값을 얻어냄</li>
      </ul>
      <ul>
         <li>key, hash function, hash, value로 이루어짐</li>
      </ul>
      <ul>
         <li>서로 다른 키의 해시값이 동일하게 나오는 경우 해시 충돌이 일어난다</li>
      </ul>
      <p><strong>장점</strong></p>
      <ul>
         <li>적은 리소스로 많은 데이터를 효율적으로 관리 가능</li>
      </ul>
      <ul>
         <li>배열 인덱스를 사용하므로 검색, 삽입, 삭제가 빠르다</li>
      </ul>
      <p><strong>단점</strong></p>
      <ul>
         <li>충돌 발생 가능성</li>
      </ul>
      <ul>
         <li>공간 복잡도 증가</li>
      </ul>
      <ul>
         <li>들어온 순서 무시</li>
      </ul>
      <p><strong>해시 알고리즘</strong></p>
      <ul>
         <li>Chaining</li>
      </ul>
      <ul>
         <li>개방 주소법 - 선형 조사, 2차 조사, 이중 해싱</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>그래프와 트리의 차이점에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <p><strong>그래프</strong></p>
      <ul>
         <li>정점과 간선을 모아놓은 자료구조</li>
      </ul>
      <ul>
         <li>연결되어있는 객체 간의 관계 표현 가능</li>
      </ul>
      <ul>
         <li>무방향/방향 가능</li>
      </ul>
      <ul>
         <li>self-loop, cycle 가능</li>
      </ul>
      <ul>
         <li>EX) 지도, 지하철 노선도, 회로</li>
      </ul>
      <p><strong>트리</strong></p>
      <ul>
         <li>계층 구조를 가지는 그래프의 한 형태</li>
      </ul>
      <ul>
         <li>하나의 루트 노드를 가짐</li>
      </ul>
      <ul>
         <li>loop, cycle 불가능</li>
      </ul>
      <figure/></a></figure>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>최소 신장 트리에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <ul>
         <li>모든 노드를 잇는 신장 트리에서 간선의 가중치 합이 최솟값인 트리</li>
      </ul>
      <ul>
         <li>EX) 도로 건설, 전기 회로, 통신, 배관</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>힙 자료구조에 대해 설명해 주세요.</strong></span></summary>
<hr>
      <ul>
         <li>완전 이진 트리의 일종</li>
      </ul>
      <ul>
         <li>우선순위큐에 사용</li>
      </ul>
      <ul>
         <li>최댓값이나 최솟값을 빠르게 찾을 수 있음</li>
      </ul>
      <ul>
         <li>중복된 값 허용</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>힙의 삽입과 삭제는 어떻게 이루어지나요?</strong></span></summary>
<hr>
      <p><strong>삽입</strong></p>
      <ol>
         <li>마지막에 노드 추가</li>
      </ol>
      <ol>
         <li>부모와 비교 → 부모보다 크면 swap</li>
      </ol>
      <ol>
         <li>2 반복</li>
      </ol>
      <p><strong>삭제</strong></p>
      <ol>
         <li>노드 삭제</li>
      </ol>
      <ol>
         <li>마지막 노드를 부모로 가져옴</li>
      </ol>
      <ol>
         <li>부모가 자식보다 작으면 → 자식 중 큰 값과 swap</li>
      </ol>
      <ol>
         <li>3 반복</li>
      </ol>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>이진 탐색 트리에 대해 설명해 주세요.</strong></span></summary>
<hr>
      <ul>
         <li>이진 트리(탐색이 O(logN)) + 연결리스트(삽입,삭제가 O(1))</li>
      </ul>
      <ul>
         <li>왼쪽 자식에는 부모보다 작은 값</li>
      </ul>
      <ul>
         <li>오른쪽 자식에는 부모보다 큰 값으로 이루어짐</li>
      </ul>
      <ul>
         <li>순회시에는 중위순회를 사용</li>
      </ul>
      <ul>
         <li>중복이 없어야함</li>
      </ul>
      <ul>
         <li>균등 트리인 경우 O(logN), 편향 트리인 경우 O(N)</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>포화(Perfect) 이진트리, 완전(Complete) 이진트리, 정(Full) 이진트리의 차이점에 대해 각각 설명해주세요.</strong></span></summary>
<hr>
      <ul>
         <li><strong>포화이진트리 </strong>: 리프노드를 제외한 모든 노드가 두개의 자식을 가지고 있는 트리</li>
      </ul>
      <ul>
         <li><strong>완전이진트리</strong> : 왼쪽부터 차근차근 채워진 이진트리</li>
      </ul>
      <ul>
         <li><strong>정이진트리/적정이진트리</strong> : 노드들이 자식을 0개 혹은 2개만 가지고 있는 이진트리</li>
      </ul>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>레드 블랙 트리에 대해 설명해주세요.</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>레드 블랙 트리의 삽입과 삭제 과정에 대해서 말해보세요.</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>AVL에 대해 설명해주세요.</strong></span></summary>
<hr>
      <p>자식들의 좌우 높이차이가 1을 넘지않는 BST</p>
      <p>높이 O(logN)</p>
      <p>탐색, 삽입, 삭제 O(logN)</p>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>B-Tree와 B+Tree에 대해서 설명해 주세요.</strong></span></summary>
<hr>
      <h3>B-Tree</h3>
      <ul>
         <li>하나의 노드에 데이터가 여러개</li>
      </ul>
      <ul>
         <li>한 노드에 최대 M개의 데이터 저장할수 있으면 M차 B-Tree</li>
      </ul>
      <ul>
         <li>M이 짝수냐 홀수냐에 따라 알고리즘이 다름</li>
      </ul>
      <ul>
         <li>자식 노드가 2개 이상 가능</li>
      </ul>
      <ul>
         <li>키 중복 없음</li>
      </ul>
      <p><strong>규칙</strong></p>
      <ol>
         <li>노드의 데이터 수가 N이면 자식의 수는 N+1이다.</li>
      </ol>
      <ol>
         <li>노드의 데이터는 정렬된 상태이다</li>
      </ol>
      <ol>
         <li>데이터는 중복될 수 없다.</li>
      </ol>
      <figure/></a></figure>
      <p></p>
      <h3>B+Tree</h3>
      <ul>
         <li>노드에 key만 담아두고, leaf 노드에 key와 data 저장</li>
      </ul>
      <ul>
         <li>모든 값을 leaf에 있고, 나머지는 데이터를 위한 방향성을 제공</li>
      </ul>
      <ul>
         <li>리프 노드끼리 Linked List로 연결되어있음</li>
      </ul>
      <ul>
         <li>하나의 노드에 많은 key를 담을 수 있으므로 트리의 높이는 더 낮아짐(cache hit을 높임)</li>
      </ul>
      <ul>
         <li>키 중복 가능</li>
      </ul>
      <ul>
         <li>리프 노드에서 선형 탐색</li>
      </ul>
      <figure/></a></figure>
<hr>
</details>
<p></p>
<h2>String / Long Data</h2>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>String Comparison Complexity에서 시간 복잡도가 최악인 경우는? 발생할 확률은?</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>String Comparison Complexity를 개선할 수 있는 방법은? (길이비교, 해시)</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>substr(), length(), indexOf() 를 직접 구현해보자</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>비교기반 자료구조/탐색알고리즘에 적용하면 생기는 문제점과 해결책 (hash / graph)</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>String Literal과 언어에서 String의 구현방법</strong></span></summary>
<hr>
<hr>
</details>

<details>
      <summary><span style="border-bottom:0.05em solid"><strong>Substring Problem의 종류와 원리를 설명하시오</strong></span></summary>
<hr>
      <ol>
         <li>Brute Force</li>
      </ol>
      <ol>
         <li>KMP</li>
      </ol>
      <ol>
         <li>Rabin-Karp</li>
      </ol>
<hr>
</details>
