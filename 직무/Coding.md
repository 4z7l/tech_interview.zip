# 손코딩 문제

<h2>손코딩</h2>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>재귀를 이용한 피보나치 수열</strong></span></summary>
<hr>
  <ul>
     <li>시간복잡도 : O(2^n)</li>
  </ul>
  <pre><code>int fibo(int n){
if(n&lt;2) return n;
return fibo(n-1) + fibo(n-2);
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>메모이제이션을 이용한 피보나치 수열</strong></span></summary>
<hr>
  <ul>
     <li>시간복잡도 : O(N)</li>
  </ul>
  <pre><code>int memo[MAX]={0,};

int fibo(int n){
if(memo[n]!=0) return memo[n];
if(n&lt;2) return n;
return memo[n] = fibo(n-1) + fibo(n-2);
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>동적계획법을 이용한 피보나치 수열</strong></span></summary>
<hr>
  <ul>
     <li>시간복잡도 : O(N)</li>
  </ul>
  <pre><code>int dp[MAX] = {0,};
dp[1] = 1; dp[2] = 2;
for(int i=3;i&lt;=N;i++){
dp[i] = dp[i-1] + dp[i-2];
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>재귀를 이용한 팩토리얼</strong></span></summary>
<hr>
  <pre><code>int fact(int n){
if(n==1) return 1;
return n*fact(n-1);
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>10번 동안 1~10까지 랜덤한 숫자를 출력하여 중복된 숫자가 있을 경우 true, false를 리턴</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>선택 정렬 구현</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>버블 정렬 구현</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>삽입 정렬 구현</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>퀵 정렬 구현</strong></span></summary>
<hr>
  <pre><code>void quickSort(int* arr, int left, int right)
if(left&gt;=right) return;
int pivot = left;
int i = left+ 1;
int j = right;

while (i &lt;= j) { // 엇갈릴 때까지 반복
while (i &lt;= right &amp;&amp; (array[i] &lt;= array[pivot])) i++;
while (j &gt; left &amp;&amp; (array[j] &gt;= array[pivot])) j--;

if (i &gt; j) swap(array[j], array[pivot]);
else swap(array[i], array[j]);
}
quickSort(arr, left, lt-1);
quickSort(arr, lt+1, right);
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>합병 정렬 구현</strong></span></summary>
<hr>
  <pre><code>void mergeSort(int* arr, int left, int right){
if(left&gt;=right) return;

int mid = (left + right) / 2;
mergeSort(left, mid);
mergeSort(mid+1, right);

int p1 = left;
int p2 = mid+1;
int p3 = left;
while(p1 &lt;= mid &amp;&amp; p2 &lt;= right) {
if(arr[p1] &lt; arr[p2]) temp[p3++] = arr[p1++];
else temp[p3++] = arr[p2++];
}
while(p1&lt;= mid) temp[p3++] = arr[p1++];
while(p2&lt;= right) temp[p3++] = arr[p2++];

for(int i=left; i&lt;=right;i++) arr[i] = temp[i];
}</code></pre>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>10번 동안 1~10까지 랜덤한 숫자를 출력하여 중복된 숫자가 있을 경우 true, false를 리턴하라(randomQuiz)</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>각종 정렬</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>각종 자료구조 구현해보기(Stack, Queue, HashTable, LinkedList) 등등</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>Anagram</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>문자열 안에 문자들이 고유한 문자인지 확인</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>최소공배수 최소공약수 구하기</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>[7, 3, 2, 9, 4]가 들어있는 배열을 오름차순으로 정렬해서 리턴하는 함수를 만들고 주어진 배열을 정렬하세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>factorial로 4!를 구하는 함수를 재귀를 이용해 만들어주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>배열에 0~10억까지 숫자가 있을 때 9억 6000이 몇번째 인덱스에 있는지 알려주는 함수를 만들어주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>요일 구하기/ 둠스데이 알고리즘/ 같은 요일 어떻게 찾는지</strong></span></summary>
<hr>

<hr>
</details>

<p></p>
