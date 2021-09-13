# Algorithm


<h2>시간복잡도</h2>
<details>
  <summary><strong>시간 복잡도 VS 공간 복잡도</strong></summary>
<hr>
  <p><strong>시간 복잡도</strong> : 알고리즘을 수행하는데 연산이 몇번 이루어지는지</p>
  <p><strong>공간 복잡도</strong> : 알고리즘이 필요로하는 자원의 양</p>
<hr>
</details>
<details>
  <summary><strong>시간 복잡도는 실제 수행 시간과 어떤 관계가 있는가?</strong></summary>
<hr>
  <p>실제 수행 시간에 미치는 요소는 아주 많다. CPU의 클록 속도, 1클록에 수행할 수 있는 명령어 수, 프로그램의 메모리 접근 패턴, 운영체제와 컴파일러 버전 등..</p>
  <p>시간 복잡도는 반복문이 반복되는 횟수로 판단한다.</p>
<hr>
</details>
<details>
  <summary><strong>시간복잡도가 작은 알고리즘은 무조건 빠른가?</strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>최악의 복잡도는 나쁘지만 실제로는 자주 사용되는 알고리즘을 나열하시오</strong></summary>
<hr>
  <ol>
     <li>Quick Sort</li>
  </ol>
  <ol>
     <li>Hash</li>
  </ol>
<hr>
</details>
<details>
  <summary><strong>빅오 표기법에 대해서 설명해주세요</strong></summary>
<hr>
  <p>알고리즘의 효율성을 표기해주는 기법</p>
  <ul>
     <li>빅오(Big-O) : 최악의 경우</li>
  </ul>
  <ul>
     <li>빅오메가(big-Ω) : 최선의 경우</li>
  </ul>
  <ul>
     <li>빅세타(big-Θ) : 평균</li>
  </ul>
<hr>
</details>
<p></p>
<br>
<h2>알고리즘</h2>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/LIS%20(Longest%20Increasing%20Sequence).md">최장 증가 수열(LIS)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/LCA(Lowest%20Common%20Ancestor).md">최소 공통 조상(LCA)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/%EB%B9%84%ED%8A%B8%EB%A7%88%EC%8A%A4%ED%81%AC(BitMask).md">비트마스크(BitMask)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>Call by value, call by reference의 차이점을 설명하시오.</strong></summary>
<hr>
  <p>Call by Value는 함수를 호출할때 값을 넘겨주고, Call by Reference는 변수의 레퍼런스를 전달합니다. Call by value는 함수 내에서 값이 변경되어도 원본 값은 변경되지 않지만, Call by Reference는 원본 값도 변경된다는 특징이 있습니다.</p>
<hr>
</details>
<details>
  <summary><strong>DFS &amp; BFS</strong></summary>
<hr>
  <p><strong>DFS</strong></p>
  <ul>
     <li>다음 브랜치로 넘어가기 전에 해당 브랜치를 모두 탐색</li>
  </ul>
  <ul>
     <li>스택/재귀함수</li>
  </ul>
  <ul>
     <li>모든 경로를 방문해야할 경우</li>
  </ul>
  <ul>
     <li>시간 복잡도 : 인접행렬 O(V^2), 인접리스트 O(V+E)</li>
  </ul>
  <p><strong>BFS</strong></p>
  <ul>
     <li>인접한 노드부터 먼저 탐색</li>
  </ul>
  <ul>
     <li>큐</li>
  </ul>
  <ul>
     <li>최소 비용 구하기</li>
  </ul>
  <ul>
     <li>시간 복잡도 : 인접행렬 O(V^2), 인접리스트 O(V+E)</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>크루스칼 알고리즘과 프림 알고리즘에 대해서 설명해 주세요.</strong></summary>
<hr>
  <p><strong>크루스칼 알고리즘</strong></p>
  <ul>
     <li>간선 위주의 알고리즘</li>
  </ul>
  <ul>
     <li>정점 개수에 비해 간선이 적은 경우 사용</li>
  </ul>
  <ul>
     <li>시간 복잡도 : O(E logE)</li>
  </ul>
  <pre><code>1. 간선 오름차순 연결
2. 가중치 가장 작은거 선택
3. 사이클이면 무시하고 지나침
4. 2~3 반복</code></pre>
  <p><strong>프림 알고리즘</strong></p>
  <ul>
     <li>정점 위주의 알고리즘</li>
  </ul>
  <ul>
     <li>간선 개수에 비해 정점 개수가 적은 경우 사용</li>
  </ul>
  <ul>
     <li>시간 복잡도 : O(E logV)</li>
  </ul>
  <pre><code>1. 정점 선택
2. 정점에서 연결된 간선 중 가장 가중치 작은거 선택
3. 반대편이 이미 추가된 정점이면 무시
4. 2~3반복</code></pre>
<hr>
</details>
<details>
  <summary><strong>다익스트라 알고리즘에 대해서 설명해 주세요.</strong></summary>
<hr>
  <p>그래프의 최단거리를 찾기 위한 알고리즘</p>
  <p>현재까지의 최단거리를 계속 갱신</p>
<hr>
</details>
<details>
  <summary><strong>LinkedList vs ArrayList의 차이점에 대해 설명하시오</strong></summary>
<hr>
  <p><strong>ArrayList</strong></p>
  <ul>
     <li>데이터들이 순서대로 늘어선 배열의 형식</li>
  </ul>
  <ul>
     <li>Random access 가능하므로 검색 빠름</li>
  </ul>
  <ul>
     <li>삽입/삭제 느림</li>
  </ul>
  <p><strong>LinkedList</strong></p>
  <ul>
     <li>자료의 주소값으로 연결된 형식</li>
  </ul>
  <ul>
     <li>검색 느림</li>
  </ul>
  <ul>
     <li>삽입/삭제 빠름</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>인접행렬과 인접리스트에 대해 설명하시오</strong></summary>
<hr>
  <p><strong>인접행렬</strong></p>
  <ul>
     <li>이차원 배열로 표현</li>
  </ul>
  <ul>
     <li>O(V^2)</li>
  </ul>
  <ul>
     <li>두 정점 연결되어있는지 여부 → O(1)</li>
  </ul>
  <ul>
     <li>모든 노드 방문시 O(V)</li>
  </ul>
  <ul>
     <li>간선이 적다면 인접리스트 사용</li>
  </ul>
  <p><strong>인접리스트</strong></p>
  <ul>
     <li>리스트로 표현</li>
  </ul>
  <ul>
     <li>O(V+E)</li>
  </ul>
  <ul>
     <li>탐색 시 간선 개수만큼만 방문</li>
  </ul>
  <ul>
     <li>두 정점 연결되어있는지 확인 → 정점에 연결된 노드 다 방문 O(V)</li>
  </ul>
<hr>
</details>
<p></p>
<br>
<h2>정렬</h2>
<figure/></a></figure>
<details>
  <summary><strong>54321 배열이 있을 때, 어떤 정렬을 사용하면 좋을까요?</strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>랜덤으로 배치된 배열이 있을때, 어떤 정렬을 사용하면 좋을까요?</strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>자릿수가 모두 같은 수가 담긴 배열이 있을 때, 어떤 정렬을 사용하면 좋을까요?</strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>정렬을 하는 이유는 무엇인가요?</strong></summary>
<hr>
  <p>데이터를 탐색하기 위해</p>
  <p>만약 정렬이 되어있다면 이진탐색을 할 수 있음</p>
<hr>
</details>
<details>
  <summary><strong>선택 정렬(Selection Sort)</strong></summary>
<hr>
  <ul>
     <li>앞에서부터 차근차근 비교하며 정렬하는 방법</li>
  </ul>
  <ul>
     <li>불안정 정렬, 제자리 정렬</li>
  </ul>
  <ul>
     <li>시간복잡도 O(N^2)</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>삽입 정렬(Insertion Sort)</strong></summary>
<hr>
  <ul>
     <li>원소가 삽입될 자리를 찾아나가는 정렬 방식</li>
  </ul>
  <ul>
     <li>안정 정렬, 제자리 정렬</li>
  </ul>
  <ul>
     <li>최선의 경우 O(N), 평균/최악의 경우 O(N^2)</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>거품 정렬(Bubble Sort)</strong></summary>
<hr>
  <ul>
     <li>인접한 두 원소를 비교하며 정렬하는 방식</li>
  </ul>
  <ul>
     <li>시간복잡도 O(N^2)</li>
  </ul>
  <ul>
     <li>안정정렬, 제자리정렬</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/QuickSort.md">퀵 정렬(Quick Sort)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>병합 정렬(Merge Sort)</span></strong></summary>
<hr>
  <ul>
     <li>분할정복을 이용한 방식</li>
  </ul>
  <ul>
     <li>데이터를 분할하여 분할된 여러개의 부분집합을 하나의 정렬된 집합으로 병합하여 진행</li>
  </ul>
  <ul>
     <li>안정정렬</li>
  </ul>
  <ul>
     <li>
        시간 복잡도
        <ul>
           <li>분할 : n개 원소를 두개로 분할 → O(logN)</li>
        </ul>
        <ul>
           <li>병합 : 최대 n번의 비교연산 → O(N)</li>
        </ul>
        <ul>
           <li>총 시간복잡도 = O(NlogN)</li>
        </ul>
     </li>
  </ul>
  <ul>
     <li>
        공간 복잡도 : n개에 데이터에 대해 정렬된 데이터를 저장할 추가적인 공간 필요
        <figure id="0f714e49-aaf1-4db6-bf58-6377f98522e5">
           <a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/MergeSort.md" class="bookmark source">
              <div class="bookmark-info">
                 <div class="bookmark-text">
                    <div class="bookmark-title">gyoogle/tech-interview-for-developer</div>
                    <div class="bookmark-description">머지 소트(Merge Sort) 합병 정렬이라고도 부르며, 분할 정복 방법을 통해 구현 큰 문제를 작은 문제 단위로 쪼개면서 해결해나가는 방식 빠른 정렬로 분류되며, 퀵소트와 함께 많이 언급되는 정렬 방식이다.</div>
                 </div>
                 <div class="bookmark-href"><img src="https://github.com/favicon.ico" class="icon bookmark-icon"/>https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/MergeSort.md</div>
              </div>
           </a>
        </figure>
     </li>
  </ul>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/HeapSort.md">힙 정렬(Heap Sort)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/Sort_Radix.md">기수 정렬(Radix Sort)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong><a href="https://github.com/gyoogle/tech-interview-for-developer/blob/master/Algorithm/Sort_Counting.md">계수 정렬(Count Sort)</a></strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>이분 탐색(Binary Search)</strong></summary>
<hr>
  <p>탐색 범위를 두 부분으로 나누며 탐색함</p>
  <ul>
     <li>전체 탐색 O(N)</li>
  </ul>
  <ul>
     <li>이분 탐색 O(logN)</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>언제 불안정정렬 쓰면 안될까?</strong></summary>
<hr>
  <p>기존의 정렬은 유지해야할때</p>
  <p>A,B 쌍인데 B는 이미 정렬상태로 입력됨. 안정정렬쓰면 좋지만 불안정정렬쓰면 기존의 정렬 깨짐</p>
<hr>
</details>
<details>
  <summary><strong>언어 기본제공 정렬은 어떻게 구현되어 있을까?</strong></summary>
<hr>
<hr>
</details>
<p></p>
<p></p>
<br>
<h2>Recursive Function / DnC / DP</h2>
<details>
  <summary><strong>Tail Recursion</strong></summary>
<hr>
<hr>
</details>
<details>
  <summary><strong>분할정복에 대해 설명하고 그 예시를 드시오</strong></summary>
<hr>
  <p>큰 문제를 작은 문제로 나눠서 작은 문제를 해결해 합치면서 해를 구하는 것</p>
  <ol>
     <li>Merge Sort / Quick Sort</li>
  </ol>
  <ol>
     <li>이분 탐색</li>
  </ol>
<hr>
</details>
<details>
  <summary><strong>Dynamic Programming가 무엇이고 왜 어떻게 사용하는가?</strong></summary>
<hr>
  <ul>
     <li>복잡한 문제를 간단한 여러개로 나누어 푸는 것</li>
  </ul>
  <ul>
     <li>한 가지 문제에 대해 한 번만 품</li>
  </ul>
  <ul>
     <li>같은 문제는 항상 정답이 같다</li>
  </ul>
<hr>
</details>
<details>
  <summary><strong>Memoization 에 대해 설명하시오</strong></summary>
<hr>
  <p>한 번 계산한 것은 저장해두고 재활용함</p>
<hr>
</details>
<p></p>
