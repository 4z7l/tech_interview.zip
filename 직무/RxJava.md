# RxJava


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>Rx에서 새로운 스레드를 생성해도 되는데 왜 </strong></span><span style="border-bottom:0.05em solid"><strong><a href="http://schedulers.io/">Schedulers.io</a></strong></span><span style="border-bottom:0.05em solid"><strong>() 를 사용하는가? </strong></span></summary>
<hr>
   <p>IO 스케줄러는 필요할때마다 스레드를 생성함</p>
   <p>뉴스레드는 요청받을때마다 스레드 생성함</p>
   <p>많은 스레드가 생성되면 전체 성능에 영향 줄수있음</p>
<hr>
</details>


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>배압 현상이란?</strong></span></summary>
<hr>
   <p>생산과 소비가 불균형적일때 일어나는 현상</p>
   <p>데이터를 발행하는 속도를 소비가 못 따라감</p>
   <p>메모리가 Overflow되고 OOME 가능성</p>
<hr>
</details>


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>Observable vs Flowable</strong></span></summary>
<hr>
   <p><strong>Observable</strong></p>
   <ul>
      <li>데이터 흐름에 맞게 알림을 보냄</li>
   </ul>
   <ul>
      <li>Observer는 이를 구독해 데이터가 준비되면 반응함</li>
   </ul>
   <p><strong>Flowable</strong></p>
   <ul>
      <li>배압 현상을 제어할 수 있음</li>
   </ul>
   <ul>
      <li>일정량 이상의 데이터가 쌓이면 더이상 발행하지않음</li>
   </ul>
<hr>
</details>


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>Cold Observable vs Hot Observable</strong></span></summary>
<hr>
<hr>
</details>


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>zip merge combineLast</strong></span></summary>
<hr>
   <p>zip : 두 스트림에서의 데이터를 하나로 합쳐줌</p>
   <figure/></a></figure>
   <p>merge : 두 스트림을 하나의 스트림으로</p>
   <figure/></a></figure>
   <p>combineLast : 두 스트림의 마지막 데이터끼리 합쳐줌</p>
   <figure/></a></figure>
<hr>
</details>


<details>

   <summary><span style="border-bottom:0.05em solid"><strong>map과 flatMap 차이</strong></span></summary>
<hr>
   <figure/></a></figure>
   <p>flatMap은 Observable을 반환</p>
<hr>
</details>

<p></p>
