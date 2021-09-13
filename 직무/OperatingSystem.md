# Operating System

<h2>프로세스</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>프로세스와 스레드의 차이는 무엇인가요? </strong></span></summary>
<hr>
   <p>프로세스는 컴퓨터에서 실행중인 프로그램을 말하고 고유한 공간과 자원을 할당 받아 사용합니다.  반면 스레드는 프로세스 안에서 실행되는 여러 흐름의 단위로 프로세스 내의 자원을 공유하고 고유한 stack만을 각자 할당 받습니다. </p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">멀티 스레드 vs 멀티 프로세스</span></strong></summary>
<hr>
   <p>멀티 스레드는 멀티 프로세스보다 적은 메모리 공간을 차지하고 Context Switching이 빠르다는 장점이 있지만, 오류로 인해 하나의 스레드가 종료되면 전체 스레드가 종료될 수 있다는 점과 동기화 문제를 가지고 있다. </p>
   <p>반면, 멀티 프로세싱 방식은 하나의 프로세스가 죽더라도 다른 프로세스에는 영향을 끼치지 않고 정상적으로 수행된다는 장점이 있지만, 멀티 스레드보다 많은 메모리 공간과 CPU 시간을 차지한다는 단점이 존재한다. 이 두 가지는 동시에 여러 작업을 수행한다는 점에서 같지만 적용해야 하는 시스템에 따라 적합/부적합이 구분된다. 따라서 대상 시스템의 특징에 따라 적합한 동작 방식을 선택하고 적용해야 한다</p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">스택을 스레드마다 독립적으로 할당하는 이유는 무엇인가요?</span></strong></summary>
<hr>
   <p>스택은 함수 호출시 전달되는 인자, 복귀 주소값 및 함수 내에서 선언하는 변수 등을 저장하기 위해 사용되는 메모리 공간입니다. 스택 메모리 공간이 독립적이라는 것은 독립적인 함수 호출이 가능함을 의미하고 이는 독립적인 실행 흐름이 추가된다는 것이다. 따라서 스레드의 정의에 따라 독립적인 실행 흐름을 추가하기 위한 최소 조건으로 독립된 스택을 할당하는 것이다.</p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">PC 레지스터를 스레드마다 독립적으로 할당하는 이유는 뭘까?</span></strong></summary>
<hr>
   <p>PC 값은 스레드가 명령어의 어디까지 수행했는지를 나타내게 된다. 스레드는 CPU를 할당받았다가 스케줄러에 의해 다시 선점당한다. 그렇기 때문에 명령어가 연속적으로 수행되지 못하고 어느 부분까지 수행했는지 기억할 필요가 있다. 따라서 PC 레지스터를 독립적으로 할당한다.</p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">멀티 프로세스 대신 멀티 스레드를 사용하는 이유는?</span></strong></summary>
<hr>
   <figure/></a></figure>
   <ul>
      <li>프로그램을 여러 개 키는 것보다 하나의 프로그램 안에서 여러 작업을 해결하는 것이 더욱 효율적이기 때문이다.</li>
   </ul>
   <ul>
      <li><span style="border-bottom:0.05em solid">프로세스를 생성하여 자원을 할당하는 시스템 콜이 줄어들어 자원을 효율적으로 관리할 수 있다</span><strong>.</strong></li>
   </ul>
   <ul>
      <li><span style="border-bottom:0.05em solid">Context Switching시, 캐시 메모리를 비울 필요가 없기 때문에 비용이 적고 더 빠르다</span>.-&gt; 스레드는 Stack 영역만 초기화하면 되기 때문이다.</li>
   </ul>
   <ul>
      <li>스레드는 프로세스 내의 메모리를 공유하기 때문에 <span style="border-bottom:0.05em solid">데이터 전달이 간단하므로 IPC에 비해 비용이 적고 더 빠르다</span>. -&gt; 스레드는 프로세스의 Stack 영역을 제외한 모든 메모리를 공유하기 때문이다.</li>
   </ul>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">컨텍스트 스위칭(Context Switching)이란 무엇인가요?</span></strong></summary>
<hr>
   <p>여러 프로세스를 처리해야 하는 상황에서 현재 진행중인 Task(프로세스, 스레드)의 상태를 PCB에 저장하고 다음에 진행할 Task의 상태값을 읽어 적용하는 과정을 말한다.</p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">컨텍스트 스위칭의 과정</span></strong></summary>
<hr>
   <ul>
      <li>Task의 대부분 정보는 Register에 저장되고 PCB로 관리된다.</li>
   </ul>
   <ul>
      <li>현재 실행하고 있는 Task의 PCB 정보를 저장한다.</li>
   </ul>
   <ul>
      <li>다음 실행할 Task의 PCB 정보를 읽어 Register에 적재하고 CPU가 이전에 진행했던 과정을 연속적으로 수행할 수 있다.</li>
   </ul>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">교착상태(Dead Lock)란 무엇인가?</span></strong></summary>
<hr>
   <p>교착 상태는 자원을 여러 곳에서 사용하려고 할 때 발생하는 문제이다.</p>
   <p>서로 원하는 자원이 상대방에게 할당되어 있어 두 프러세스가 무한정 wait 상태에 빠지게 되는 상황.</p>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">교착상태가 발생하기 위한 조건은?</span></strong></summary>
<hr>
   <p>4가지 중 하나라도 성립하지 않으면 데드락은 발생하지 않습니다.</p>
   <ol>
      <li><strong>상호 배제(Mutual exclusion) : </strong>자원은 한번에 한 프로세스만 사용할 수 있음</li>
   </ol>
   <ol>
      <li><strong>점유 대기(Hold and wait) : </strong>최소한 하나의 자원을 점유하고 있으면서 다른 프로세스에 할당되어 사용하고 있는 자원을 추가로 점유하기 위해 대기하는 프로세스가 존재해야 함</li>
   </ol>
   <ol>
      <li><strong>비선점(No preemption) : </strong>다른 프로세스에 할당된 자원은 사용이 끝날 때까지 강제로 빼앗을 수 없음</li>
   </ol>
   <ol>
      <li><strong>순환 대기(Circular wait) : </strong>프로세스의 집합에서 순환 형태로 자원을 대기하고 있어야 함</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>교착상태의 해결법은 무엇인가요?</strong></span></summary>
<hr>
   <ol>
      <li>
         <strong>예방(prevention)</strong>
         <p>교착 상태 발생 조건 중 하나를 제거하면서 해결한다 (자원 낭비 엄청 심함)</p>
         <ul>
            <li>상호배제 부정 : 여러 프로세스가 공유 자원 사용</li>
         </ul>
         <ul>
            <li>점유대기 부정 : 프로세스 실행전 모든 자원을 할당</li>
         </ul>
         <ul>
            <li>비선점 부정 : 자원 점유 중인 프로세스가 다른 자원을 요구할 때 가진 자원 반납</li>
         </ul>
         <ul>
            <li>순환대기 부정 : 자원에 고유번호 할당 후 순서대로 자원 요구</li>
         </ul>
      </li>
   </ol>
   <ol>
      <li>
         <strong>회피(avoidance) - </strong>교착 상태 발생 시 피해나가는 방법
         <p>은행원 알고리즘(Banker&#x27;s Algorithm)
         <div class="indented">
            <p>은행에서 모든 고객의 요구가 충족되도록 현금을 할당하는데서 유래함</p>
            <p>프로세스가 자원을 요구할 때, 시스템은 자원을 할당한 후에도 안정 상태로 남아있으면 자원할당, 아니면 할당을 거부하고 다른 프로세스 들이 자원을 해지할때까지 대기하는 방법</p>
         </div>
         </p>
      </li>
   </ol>
   <ol>
      <li>
         <strong>탐지(Detection) &amp; 회복</strong>
         <p>은행원 알고리즘과 유사한 방식 vs 자원 할당 그래프를 통해 교착 상태를 탐지함</p>
         <p>자원 요청 시, 탐지 알고리즘을 실행시켜 그에 대한 오버헤드 발생함</p>
      </li>
   </ol>
   <ol>
      <li>
         <strong>회복(Recovery) - </strong>교착 상태 일으킨 프로세스를 종료하거나, 할당된 자원을 해제시켜 회복시키는 방법
         <p><strong>프로세스 종료 방법</strong></p>
         <ul>
            <li>교착 상태의 프로세스를 모두 중지</li>
         </ul>
         <ul>
            <li>교착 상태가 제거될 때까지 하나씩 프로세스 중지</li>
         </ul>
         <p><strong>자원 선점 방법</strong></p>
         <ul>
            <li>교착 상태의 프로세스가 점유하고 있는 자원을 선점해 다른 프로세스에게 할당 (해당 프로세스 일시정지 시킴)</li>
         </ul>
         <ul>
            <li>우선 순위가 낮은 프로세스나 수행 횟수 적은 프로세스 위주로 프로세스 자원 선점</li>
         </ul>
      </li>
   </ol>
   <ol>
      <li><strong>무시</strong></li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>회피 기법인 은행원 알고리즘이 뭔지 설명해보세요.</strong></span></summary>
<hr>
   <p>은행원 알고리즘은 은행에서 현금을 할당하는 것에서 유래한 알고리즘입니다.</p>
   <p>프로세스가 자원을 요구할때 자원을 할당한 후에도 안정 상태이면 자원을 할당하고, 그렇지 않으면 다른 자원이 해제될때까지 대기했다가 자원을 할당합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>은행원 알고리즘의 단점</strong></span></summary>
<hr>
   <ul>
      <li>할당할 수 있는 자원수가 일정 해야함</li>
   </ul>
   <ul>
      <li>항상 불안전 상태를 방지해야 하므로 <strong>자원 이용도가 낮다</strong></li>
   </ul>
   <ul>
      <li><strong>최대 자원 요구량</strong>을 미리 알아야 한다.</li>
   </ul>
   <ul>
      <li>프로세스들은 유한한 시간 안에 자원을 반납해야 한다.</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>기아상태를 설명하는 식사하는 철학자 문제에 대해 설명해보세요.</strong></span></summary>
<hr>
   <ol>
      <li>일정 시간 생각을 한다.</li>
   </ol>
   <ol>
      <li>왼쪽 포크가 사용 가능해질 때까지 대기한다. 만약 사용 가능하다면 집어든다.</li>
   </ol>
   <ol>
      <li>오른쪽 포크가 사용 가능해질 때까지 대기한다. 만약 사용 가능하다면 집어든다.</li>
   </ol>
   <ol>
      <li>양쪽의 포크를 잡으면 일정 시간만큼 식사를 한다.</li>
   </ol>
   <ol>
      <li>오른쪽 포크를 내려놓는다.</li>
   </ol>
   <ol>
      <li>왼쪽 포크를 내려놓는다.</li>
   </ol>
   <ol>
      <li>다시 1번으로 돌아간다.</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>철학자 문제 교착상태 조건 성립 조건</strong></span></summary>
<hr>
   <p><strong>상호 배제 -&gt; </strong>젓가락은 한 번에 한 철학자만 사용할 수 있습니다.</p>
   <p><strong>점유와 대기 -&gt;</strong> 왼쪽 젓가락을 점유하면서 오른쪽 젓가락을 대기합니다.</p>
   <p><strong>비선점 -&gt; </strong>이미 누군가가 집어 든 젓가락을 강제로 뺏을 수 없습니다.</p>
   <p><strong>환형 대기 -&gt; </strong>모든 철학자들이 오른쪽에 앉은 철학자가 젓가락을 놓기를 기다립니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>식사하는 철학자 문제 해결책</strong></span></summary>
<hr>
   <ol>
      <li>모두 젓가락을 내려두고 랜덤시간동안 기다린 다음 식사 (기아현상이 발생할 수 있는 가능성이 남아 있음)</li>
   </ol>
   <ol>
      <li>
         뮤텍스 - <mark class="highlight-gray">(화장실이 하나밖에 없는 식당)</mark>
         <p>공유된 자원의 데이터를 여러 쓰레드가 접근하는 것을 막는 것</p>
         <p>식사할 수 있는 상황을 하나의 key로 관리</p>
         <p>오직 하나의 쓰레드만이 동일한 시점에 뮤텍스를 얻어 임계 영역(Critical Section)에 들어올 수 있다. 그리고 오직 이 쓰레드만이 임계 영역에서 나갈 때 뮤텍스를 해제할 수 있다.</p>
         <p>Critical Section을 가진 쓰레드들의 Running tme이 서로 겹치지 않게 각각 단독으로 실행되게 하는 기술</p>
      </li>
   </ol>
   <ol>
      <li>
         세마포어 -<mark class="highlight-gray"> (화장실이 여러개인 식당)</mark>
         <p>공유된 자원의 데이터를 여러 프로세스가 접근하는 것을 막는 것</p>
         <p>Signaling mechanism. 현재 공유자원에 접근할 수 있는 쓰레드, 프로세스의 수를 나타내는 값을 두어 상호배제를 달성하는 기법</p>
         <p>락을 걸지 않은 쓰레드도 Signal을 보내 락을 해제할 수 있다는</p>
      </li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Mutex vs Semaphore</strong></span></summary>
<hr>
   <p>세마포어와 뮤텍스는 동기화 문제를 해결하기 위한 방법입니다. 여러 프로세스가 공유자원에 접근할때, 한 프로세스가 크리티컬 섹션에서 수행중이라면 다른 프로세스는 자신의 크리티컬 섹션에 들어가지 못하게 해야합니다.</p>
   <p><strong>세마포어</strong>에는 P연산과 V연산이 있습니다. P연산은 자원을 할당하는 연산이고 V연산은 자원을 해제하는 연산입니다. 크리티컬 섹션에 들어가기 전 세마포어를 통해 자원에 접근가능한지 확인을 하며 동기화문제를 해결합니다. 공유 자원에 프로세스들이 최대 허용치만큼 접근할 수 있음</p>
   <p><strong>뮤텍스</strong>는 이진 세마포어의 일종으로 자원에 lock을 걸면서 동기화 문제를 해결합니다. <strong>상호 배제</strong> 개념을 이용하며 크리티컬 섹션을 가진 스레드들이 각각 단독으로 실행되게 하는 기술입니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>임계구역이란?</strong></span></summary>
<hr>
   <p>여러 프로세스가 데이터를 공유하며 수행될 때, 각 프로세스에서 공유 데이터를 접근하는 프로그램 코드 부분</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>경쟁 상태(Race Condition)란 무엇인가요?</strong></span></summary>
<hr>
   <p>두 개 이상의 프로세스가 공통 자원을 병행적으로(concurrently) 읽거나 쓰는 동작을 할 때, 공용 데이터에 대한 접근이 어떤 순서에 따라 이루어졌는지에 따라 그 실행 결과가 같지 않고 달라지는 상황</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>경쟁상태가 발생하는 경우</strong></span></summary>
<hr>
   <ol>
      <li>
         <strong>커널 작업을 수행하는 중에 인터럽트 발생</strong>
         <ul>
            <li>문제점 : 커널모드에서 데이터를 로드하여 작업을 수행하다가 인터럽트가 발생하여 같은 데이터를 조작하는 경우</li>
         </ul>
         <ul>
            <li>해결법 : 커널모드에서 작업을 수행하는 동안, 인터럽트를 disable 시켜 CPU 제어권을 가져가지 못하도록 한다.</li>
         </ul>
      </li>
   </ol>
   <ol>
      <li>
         <strong>프로세스가 &#x27;System Call&#x27;을 하여 커널 모드로 진입하여 작업을 수행하는 도중 문맥 교환이 발생할 때</strong>
         <ul>
            <li>문제점 : 프로세스1이 커널모드에서 데이터를 조작하는 도중, 시간이 초과되어 CPU 제어권이 프로세스2로 넘어가 같은 데이터를 조작하는 경우 ( 프로세스2가 작업에 반영되지 않음 )</li>
         </ul>
         <ul>
            <li>해결법 : 프로세스가 커널모드에서 작업을 하는 경우 시간이 초과되어도 CPU 제어권이 다른 프로세스에게 넘어가지 않도록 함</li>
         </ul>
      </li>
   </ol>
   <ol>
      <li>
         <strong>멀티 프로세서 환경에서 공유 메모리 내의 커널 데이터에 접근할 때</strong>
         <ul>
            <li>문제점 : 멀티 프로세서 환경에서 2개의 CPU가 동시에 커널 내부의 공유 데이터에 접근하여 조작하는 경우</li>
         </ul>
         <ul>
            <li>해결법 : 커널 내부에 있는 각 공유 데이터에 접근할 때마다, 그 데이터에 대한 lock/unlock을 하는 방법</li>
         </ul>
      </li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>경쟁상태를 방지하기 위한 해결법의 충족 조건</strong></span></summary>
<hr>
   <ul>
      <li>
         Mutual Exclusion (상호 배제)
         <ul>
            <li>어떤 프로세스 가 임계 영역을 수행 중이면 다른 모든 프로세스들은 그 임계 영역에 들어가면 안된다.</li>
         </ul>
      </li>
   </ul>
   <ul>
      <li>
         Progress
         <ul>
            <li>아무도 임계 영역에 있지 않은 상태에서 임계 영역에 들어가려는 프로세스가 있으면 들어가게 해주어야 한다. ( livelock 방지 )</li>
         </ul>
      </li>
   </ul>
   <ul>
      <li>
         Bounded Waiting
         <ul>
            <li>프로세스가 임계 영역에 들어가려고 요청한 후부터 다른 프로세스들이 임계 영역에 들어가는 횟수에 한계가 있어야 한다 ( starvation 방지 )</li>
         </ul>
      </li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>경쟁상태 해결방법은 무엇이 있나요?</strong></span></summary>
<hr>
   <ol>
      <li>상호배제</li>
   </ol>
   <ol>
      <li>
         동기화
         <ul>
            <li>세마포어</li>
         </ul>
         <ul>
            <li>모니터</li>
         </ul>
         <ul>
            <li>락</li>
         </ul>
      </li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>프로세스 혹은 스레드의 동기화란 무엇인가요?</strong></span></summary>
<hr>
   <p>동기화란 병렬적으로 수행되는 작업들에 대해 자원 접근 순서를 정해 서로가 알고있는 정보가 일치하도록 하는 것</p>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">사용자 수준의 스레드와 커널 수준의 스레드의 차이는 무엇인가요?</span></strong></summary>
<hr>
   <p><strong>커널 수준 스레드</strong></p>
   <ul>
      <li>스레드를 생성하고 스케줄링하는 주체가 커널</li>
   </ul>
   <ul>
      <li>장점 : 커널이 직접 제공해주므로 안정성과 다양한 기능 제공</li>
   </ul>
   <ul>
      <li>단점 : 유저 모드에서 커널 모드로의 전환이 빈번함</li>
   </ul>
   <p><strong>사용자 수준 스레드</strong></p>
   <ul>
      <li>스레드 기능을 제공하는 라이브러리를 이용하므로 커널에 의존하지 않음</li>
   </ul>
   <ul>
      <li>장점 : 커널이 스레드를 모르기때문에 모드 간의 전환이 없고 성능 이득 발생</li>
   </ul>
   <ul>
      <li>단점 : 하나의 스레드가 커널에 블로킹되면 프로세스 전체가 블로킹됨</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>CPU 스케줄링이란 무엇인가요?</strong></span></summary>
<hr>
   <p>CPU 스케줄링이란 CPU를 배정하는 것을 말한다.</p>
   <ul>
      <li>오버헤드, 기아현상, 소요시간, 반환시간, 대기시간 낮추기</li>
   </ul>
   <ul>
      <li>처리량, 사용률, 응답 시간 높이기</li>
   </ul>
   <ul>
      <li>선점 스케줄링 : OS가 CPU의 사용권을 빼앗을 수 있음</li>
   </ul>
   <ul>
      <li>비선점 스케줄링 : CPU를 빼앗을 수 없음</li>
   </ul>

<hr>
</details>


<details>
   <summary><strong><span style="border-bottom:0.05em solid">프로세스 스케줄러에는 어떤 것들이 있나요?</span></strong></summary>
<hr>
   <ul>
      <li>장기 스케줄러 : 어떤 프로세스를 ready queue에 보낼지, 시분할 시스템에서는 잘 안둠</li>
   </ul>
   <ul>
      <li>단기 스케줄러 : 어떤 프로세스를 실행시킬지</li>
   </ul>
   <ul>
      <li>중기 스케줄러 : 메모리에 공간이 부족한 경우 어떤 프로세스를 swap out할지</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>CPU 스케줄링의 성능 척도에는 어떤 것들이 있나요?</strong></span></summary>
<hr>
   <ul>
      <li>CPU Utilization(이용률) : 전체 시간 중 CPU가 놀지 않고 일한 시간, 이용률이 높을수록 좋음</li>
   </ul>
   <ul>
      <li>Throughput(처리량) : 단위 시간당 처리량, CPU가 얼마나 많은 일을 했는가, 높을수록 좋음</li>
   </ul>
   <ul>
      <li>Turnaround Time(소요시간, 반환시간) : CPU 사용한 시간 + 기다린 시간, 짧을수록 좋음</li>
   </ul>
   <ul>
      <li>Waiting Time(대기시간) : 프로세스가 Ready Queue에서 기다린 전체 시간의 합, 짧을수록 좋음</li>
   </ul>
   <ul>
      <li>Response Time(응답시간) : 프로세스가 Ready Queue에 들어가서 최초로 CPU 얻기까지의 시간, 짧을수록 좋음</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>CPU 스케줄링 방법에는 대표적으로 어떤 것들이 있나요?</strong></span></summary>
<hr>
   <p><strong>선점 스케줄링</strong></p>
   <ul>
      <li>우선순위 스케줄링 : 우선순위가 높은 순서대로 처리</li>
   </ul>
   <ul>
      <li>Round Robin : 동일한 시간의 time quantum만큼 할당</li>
   </ul>
   <ul>
      <li>Multilevel Queue : 작업을 여러 종류의 큐로 나누어 큐마다 다른 time quantum 할당</li>
   </ul>
   <ul>
      <li>Multilevel-feedback Queue : Multilevel에서 time quantum을 채우면 다음 level로 내려감</li>
   </ul>
   <p><strong>비선점 스케줄링</strong></p>
   <ul>
      <li>FCFS : 큐에 도착한 순서대로 CPU 할당</li>
   </ul>
   <ul>
      <li>SJF : 수행시간이 짧은 것 부터 CPU 할당</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>동기와 비동기, 블로킹과 넌블로킹의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p>동기/비동기 - 작업 주체 여러개</p>
   <p>블로킹/논블로킹 - 작업이 여러개</p>
   <p></p>
   <p>동기 : 시작과 종료를 동시에 하거나, 하나가 끝나면 다른 하나가 시작하는 경우</p>
   <p>비동기 : 별도의 시작/종료를 가짐</p>
   <p>블로킹 : 작업을 하다가 다른 작업이 완료될때까지 기다렸다가 다시 수행</p>
   <p>넌블로킹 : 다른 작업과 관련없이 자기 작업 계속함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>IPC란 무엇인가요?</strong></span></summary>
<hr>
   <p>IPC는 Inter-Process Communication의 약자로 프로세스간 통신을 의미합니다. 프로세스는 커널이 제공하는 IPC 설비를 이용해 프로세스간 통신을 할 수 있습니다. </p>
   <p>IPC설비의 종류는 여섯 가지가 있습니다. </p>
   <p>첫번째는, PIPE (익명 파이프) 입니다. PIPE는 두 프로세스간 파이프를 연결해서 통신을 하는 방식입니다. 여기서 한 프로세스는 쓰기만 가능하고 다른 프로세스는 읽기만 가능하다는 특징이 있습니다. 한쪽 방향으로만 통신이 가능하기 때문에 반이중 통신이라고 부르기도 합니다. PIPE는 간단하게 사용할 수 있다는 장점이 있습니다.</p>
   <p>두번째는, Named PIPE (FIFO) 입니다. PIPE는 통신하는 프로세스가 명확할 경우 사용하는 반면, Named PIPE는 전혀 모르는 사이의 프로세스들의 통신에 사용합니다. 익명 PIPE는 부모가 동일한 프로세스들 사이에서만 통신이 가능하지만 Named PIPE는 부모 프로세스에 상관없이 프로세스들 사이의 통신을 할 수 있다는 점이 특징입니다. 이는 프로세스 통신을 위해 mkfifo함수를 이용해 파일을 생성하기 때문에 가능합니다. 하지만, 익명 PIPE와 동일하게 동시에 읽기/쓰기가 불가능 합니다. 이는 두개의 파일을 읽기전용, 쓰기전용으로 만들어서 해결할 수 있습니다. 전이중 통신을 위해서는 두 개의 fifo 파일을 만들어서 사용해야 합니다.</p>
   <p>세번째는, 메세지 큐 입니다. 메세지 큐는 선입선출의 형태로 통신이 이루어지는 점에서 Named PIPE와 동일합니다. 차이점은 Named PIPE가 데이터의 흐름이라면 메세지 큐는 메모리 공간이라는 점입니다. 이는 여러개의 프로세스가 메세지 큐의 데이터에 접근할 수 있음을 의미합니다.</p>
   <p>네번째는, 공유메모리 입니다. 앞서 PIPE, Named PIPE, 메세지 큐가 통신을 이용해 데이터를 주고받는다면, 공유메모리는 프로세스간 메모리 영역을 공유해서 사용할 수 있도록 지원합니다. 프로세스가 공유 메모리 할당을 커널에 요청하면 커널은 해당 프로세스에 메모리 공간을 할당해줍니다. 이후 어떤 프로세스건 해당 메모리영역에 접근할 수 있습니다. 공유 메모리는 곧바로 메모리에 접근할 수 있기 때문에 IPC 방식 중 속도가 제일 빠릅니다.</p>
   <p>다섯번째는, 메모리 맵 입니다. 메모리 맵은 공유 메모리와 메모리를 공유한다는 점은 동일합니다. 하지만, 현재 열려져 있는 파일을 공유하는 점에서 차이가 있습니다. 열린 파일이 메모리에 올라가있으면 다른 프로세스가 해당 파일을 사용할 때 또다시 파일을 열지않고 공유한 상태로 사용하는 것이 더 효율적입니다.</p>
   <p>여섯번째는, 소켓입니다. 소켓은 소켓을 만들어 통신하는 방법입니다. 소켓 통신은 데이터 교환을 위해 양쪽 PC에서 각각 임의의 포트를 정하고 해당 포트 간의 대화를 통해 데이터를 주고받는 방식입니다. 이 때 각각 PC의 프로세스는 임의의 PORT를 맡아 데이터를 송수신 합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>fork()란 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>child process와 zombi process에 대해 설명해 보시오. (고아/좀비)</strong></span></summary>
<hr>
   <p>자식 프로세스 : fork로 자식프로세스를 만든 상태. 부모의 데이터,힙,스택, PCB 복사</p>
   <p>좀비 프로세스 : 프로세스가 종료됐는데 메모리상에 정보가 남아있는 상태, 부모가 wait로 보고받지 못함</p>
   <p>고아 프로세스 : 부모 프로세스가 먼저 종료돼서 부모 프로세스를 잃은 프로세스, init이 자식프로세스 회수함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>인터럽트란 무엇인가요?</strong></span></summary>
<hr>
   <p>인터럽트란 프로세스 실행 중에 예외상황이 발생하여 처리가 필요한 경우 CPU에게 알려 처리할 수 있도록 하는 것을 말합니다. </p>
   <p>폴링은 대상을 주기적으로 감시하여 상황이 발생하면 해당 루틴을 처리합니다.</p>
   <p>인터럽트란 CPU가 프로그램을 실행하고 있는 도중에 입출력 요청 또는 예외상황을 처리해야 하면 실행하던 프로그램을 멈추고 CPU가 해당 작업을 처리하도록 하는 것을 말합니다. 인터럽트는 하드웨어 인터럽트와 소프트웨어 인터럽트로 구성되어 있습니다. 하드웨어 인터럽트는 하드웨어 기기가 인터럽트를 요청하는 것이고 소프트웨어 인터럽트는 예외처리, 시스템 콜이 발생하는 상황에서 실행됩니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>시스템 콜이란 무엇인가요?</strong></span></summary>
<hr>
   <p>시스템 콜은 사용자나 응용 프로그램이 커널에서 제공하는 기능을 사용하기 위한 인터페이스 입니다. 운영체제는 커널이 제공하는 서비스를 시스템콜을 이용해 제한함으로써 컴퓨터 자원을 보호합니다.</p>
   <p>예시로는 프로세스 생성/종료나 I/O작업 등이 있습니다. (fork, exec, exit, wait)</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>전통적인 동기화 문제에는 어떤 것들이 있나요?</strong></span></summary>
<hr>
   <p><strong>1. Bounded- Buffer Problem</strong></p>
   <p><strong>2. Readers and Writers Problem</strong></p>
   <p><strong>3. Dining Philosophers Problem</strong></p>

<hr>
</details>

<p></p>
<p></p>
<h2>메모리</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>프로세스에 할당되는 메모리의 각 영역에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <ul>
      <li>코드 : 실행할 명령어 저장</li>
   </ul>
   <ul>
      <li>데이터 : 프로그램에 필요한 전역변수나 정적변수 저장</li>
   </ul>
   <ul>
      <li>스택 : 함수 호출에 필요한 스택 프레임 저장</li>
   </ul>
   <ul>
      <li>힙 : 사용자가 관리하는 공간으로 메모리가 동적으로 할당되고 해제됨, JAVA에서는 GC가 메모리를 알아서 해제해줌</li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>메모리 구조의 순서가 어떻게 되는가? CPU에서 가까운 순으로 말해보시오.</strong></span></summary>
<hr>
   <p>레지스터, 캐시, 주기억장치, 보조기억장치 순서입니다.</p>
   <p>CPU는 프로그램 실행 시 먼저 레지스터에 필요한 데이터가 있는지 확인합니다.</p>
   <p>레지스터에 필요한 데이터가 존재하지 않는다면 캐시를, 캐시에도 없다면 주기억장치를, 주기억장치에도 없다면 보조기억장치를 확인하며 필요한 데이터를 적재합니다.</p>
   <p>https://popcorntree.tistory.com/68</a></p>
   <figure/></a></figure>
   <ul>
      <li><strong>레지스터</strong> : CPU 내에 존재하는 메모리로 빠르고 작다.</li>
   </ul>
   <ul>
      <li><strong>캐시</strong> : CPU와 주기억장치 사이에서 중간 저장소 역할을 함. Locality 특성 이용</li>
   </ul>
   <ul>
      <li><strong>주기억장치</strong> : 현재 수행되는 프로그램과 데이터 저장</li>
   </ul>
   <ul>
      <li><strong>보조기억장치</strong> : 용량이 크나 느리다.</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>페이지와 세그멘테이션에 대해서 설명해 보시오.</strong></span></summary>
<hr>
   <p>메모리를 관리 기법 중 불연속 메모리 관리 기법입니다.
      페이징은 외부단편화와 압축 작업을 해결하기 위한 방법으로, 페이지라는 고정 크기로 logical memory를 분리하고, 페이지와 같은 크기의 프레임으로 physical memory를 분리합니다. 페이징을 사용하면 외부 단편화를 해결한다는 장점이 있지만 내부단편화는 여전히 존재합니다.
   </p>
   <p>세그멘테이션은 페이징과는 달리 서로 다른 크기의 논리적 단위인 세그먼트로 메모리를 분리합니다. 세그멘테이션을 사용하면 세그먼트들이 메모리에 할당되고 해제되는 과정에서 외부단편화가 발생합니다. 하지만 세그먼트는 메모리를 의미 단위로 나누기 때문에 보호와 공유에서 효율적입니다.</p>
   <p><strong>메모리 관리 기법</strong></p>
   <ul>
      <li>연속 메모리 관리 : 고정 분할(내부단편화), 동적 분할(외부단편화)</li>
   </ul>
   <ul>
      <li>불연속 메모리 관리 : 페이징, 세그멘테이션</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>외부 단편화란? 내부 단편화란?</strong></span></summary>
<hr>
   <p><strong>내부 단편화</strong>란 프로세스가 사용하는 메모리 공간 중 남는 부분이 발생하는 현상입니다.</p>
   <p><strong>외부 단편화</strong>란 physical memory 사이에 사용하지 못하는 공간이 생기는 현상을 말합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>메모리의 First Fit, Best Fit, Worst Fit에 대해서 설명해 보시오.</strong></span></summary>
<hr>
   <ol>
      <li>First fit : 메모리의 처음부터 검사해서 크기가 충분한 첫번째 메모리에 할당</li>
   </ol>
   <ol>
      <li>Next fit : 마지막으로 참조한 메모리 공간에서부터 탐색을 시작해 공간을 찾음</li>
   </ol>
   <ol>
      <li>Best fit : 모든 메모리 공간을 검사해서 내부 단편화를 최소화하는 공간에 할당</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>페이지 교체 알고리즘 종류에는 어떤 것들이 있나요?</strong></span></summary>
<hr>
   <p>OPT : 최적 교체. 앞으로 가장 오랫동안 사용하지 않을 페이지 교체 (실현 가능성 희박)</p>
   <p>FIFO : 메모리가 할당된 순서대로 페이지를 교체</p>
   <p>LRU : 최근에 가장 오랫동안 사용하지 않은 페이지를 교체</p>
   <p>LFU : 사용 빈도가 가장 적은 페이지를 교체</p>
   <p>NUR : 최근에 사용하지 않은 페이지를 교체</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>가상 메모리(Virtual Memory)란?</strong></span></summary>
<hr>
   <p>메모리에 로드된, 실행중인 프로세스가 메모리가 아닌 가상의 공간을 참조해 마치 커다란 물리 메모리를 갖는 것처럼 사용할 수 있게 해주는 기법</p>
   <p>프로그램에 실제 메모리 주소가 아닌 가상 메모리 주소를 할당하는 방법</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Demand Paging이란?</strong></span></summary>
<hr>
   <p>현재 필요한 부분만 메모리에 적재하는 것</p>
   <p>페이지가 올라와있는지 구별시에는 유효-무효 비트를 사용함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>가상 메모리를 사용할 시 장단점은?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Cache Memory의 역할은 무엇인가</strong></span></summary>
<hr>
   <p>캐시 메모리는 CPU와 메모리 사이의 속도 차이를 완화하기 위한 역할을 합니다. 캐시는 메모리의 데이터를 미리 가져와 저장해두는 임시 장소로 앞으로 사용될 것으로 예상되는 데이터를 미리 저장해 놓습니다. </p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Caching Locality와 Cache Hit Ratio에 대해 설명하시오</strong></span></summary>
<hr>
   <p><strong>캐시 적중률</strong>은 CPU가 사용할 데이터를 캐시에서 탐색 했을 때, 원하는 데이터가 캐시에 존재할 확률을 의미합니다. </p>
   <p><strong>캐시 적중률</strong>을 높이기 위해서는 캐시 메모리의 크기를 늘리는 방법과 앞으로 많이 사용될 데이터를 캐시에 저장하는 방법이 있습니다. </p>
   <p>앞으로 많이 사용될 데이터를 저장하기 위해서는 <strong>캐시 지역성</strong>을 이용할 수 있습니다. 캐시 지역성은 현재 사용하고 있는 메모리 위치에서 가까운 데이터를 사용할 확률이 높다는 개념입니다. 따라서, 현재 접근하고 있는 메모리 근처의 값들을 캐시에 저장해놓는다면 캐시 적중률을 높일 수 있습니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Call Stack에 대해 설명하시오</strong></span></summary>
<hr>
   <p>컴퓨터 프로그램에서 현재 실행 중인 서브루틴에 관한 정보를 저장하는 스택 자료구조</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Heap 메모리는 무엇이고 사용하는 이유는 무엇인가</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Heap과 Stack의 장단점 비교 (속도, 크기 등)</strong></span></summary>
<hr>
   <p><strong>스택</strong> : 빠르다, 스택 크기 제한</p>
   <p><strong>힙</strong> : 메모리 크기 제한 없음, 메모리를 직접 관리해야함, 상대적으로 느림</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Memory Corruption이란?</strong></span></summary>
<hr>
   <p>버그로 인한 메모리 오염, 예상되지 않은 메모리 값 변경 등에 의해 일어남</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Heap Corruption에 대해 설명하시오</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>거짓 공유에 대해 설명하시오</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>DMA란?</strong></span></summary>
<hr>
   <p>CPU를 대신하여 I/O장치와 Memory사이의 데이터전송을 담당하는 장치</p>
   <p>주변장치(하드디스크, 그래픽카드)들이 메모리에 직접 접근하여 읽거나 쓰도록 하는 기능</p>
   <p>CPU의 개입 없이 I/O장치와 기억장치 사이의 데이터를 전송할수있음</p>
   <p>인터럽트 발생 횟수 최소화하여 성능 높임</p>

<hr>
</details>
