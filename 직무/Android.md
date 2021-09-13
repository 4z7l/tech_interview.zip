# Android

<h2>안드로이드 기초</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드의 4대 컴포넌트에 대해 설명하시오</strong></span></summary>
<hr>
   <p>액티비티 : 화면을 관리하고 다양한 이벤트를 처리함</p>
   <p>서비스 : 화면에서 보이진 않지만 백그라운드 작업 수행</p>
   <p>콘텐츠 프로바이더 : 앱 간의 데이터를 공유하기 위한 인터페이스 제공</p>
   <p>브로드캐스트 리시버 : 안드로이드에서 발생하는 브로드캐스트 메시지를 처리함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드의 실행환경</strong></span></summary>
<hr>
   <p>안드로이드는 크게 4가지로 구성되어있습니다.</p>
   <p><strong>리눅스 커널, 라이브러리, 어플리케이션 프레임워크, 어플리케이션</strong>입니다.</p>
   <p><strong>리눅스 커널</strong>은 OS로 스마트폰의 메모리나 프로세스 등을 관리합니다.</p>
   <p><strong>라이브러리</strong>는 안드로이드에 있는 다양한 기능을 라이브러리를 제공하며 안드로이드 앱을 구동해주는 dalvik 가상머신을 포함합니다.</p>
   <p><strong>어플리케이션 프레임워크</strong>는 사용자의 이벤트에 따라 출력을 담당하는 환경을 제공합니다. 생명주기도 여기서 관리.</p>
   <p><strong>어플리케이션</strong>은 실제로 동작하는 앱을 말합니다.</p>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드는 다른 플랫폼에 비해 어떠한 장점이 있는가?</strong></span></summary>
<hr>
   <ul>
      <li>오픈소스이므로 안정성과 버그 수정이 빠르다</li>
   </ul>
   <ul>
      <li>자바를 주 언어로 사용하여 자바 개발자들이 쉽게 개발할 수 있음</li>
   </ul>
   <ul>
      <li>리눅스 커널을 OS로 사용하여 하드웨어에 대한 드라이버 소스가 풍부함</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Activity와 Fragment의 차이는?</strong></span></summary>
<hr>
   <ul>
      <li><strong>Activity : </strong>사용자가 원하는 대로 Activity를 변경할 수 있고, Activity가 변하면 View도 바뀐다</li>
   </ul>
   <ul>
      <li><strong>Fragment : </strong>관심사 분리를 통해 의존성을 분리하고 독립성을 키움</li>
   </ul>
   <ul>
      <li>액티비티 스택에 액티비티를 쌓아두는 것보다 프래그먼트 백스택에서 프래그먼트를 관리하는 것이 메모리 관리면에서도 효율적</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Activity의 Lifecycle에 대해 설명하시오</strong></span></summary>
<hr>
   <p>액티비티는 크게 3가지 상태가 존재합니다.</p>
   <p>먼저 <strong>running 실행 상태</strong>는 액티비티 스택의 최상위에 있으며 포커스를 가지고 있어 사용자에게 보이는 상태입니다.</p>
   <p><strong>pasued 일시 중지 상태</strong>는 사용자에게 보이기는 하지만 다른 액티비티가 위에 있어 포커스를 받지 못하는 상태입니다.</p>
   <p><strong>stopped 중지 상태</strong>는 다른 액티비티에 의해 완전히 가려져 보이지 않는 상태를 말합니다.</p>
   <p></p>
   <p>액티비티가 처음 생성되면 onCreate가 호출되고, 그 다음으로 화면에 보여지기 직전에 onStart가 호출됩니다. 사용자가 상호작용하기 직전에 onResume이 호출되면 액티비티는 running 실행 상태가 됩니다.</p>
   <p>이후 포커스를 잃는다면 onPaused가 호출되고 paused 일시 중지 상태가 됩니다.</p>
   <p>만약 다시 포커스를 갖게 되면 onResume이 호출되고 화면이 가려져 보이지 않는 상태가 된다면 onStop이 호출되어 stopped 중지 상태가 됩니다.</p>
   <p>정지 상태에서 화면이 다시 보이기 직전에 onRestart와 onStart가 차례로 호출됩니다.</p>
   <p>마지막으로 finish 메소드가 호출되어 액티비티가 소멸하기 직전에 onDestroy가 호출됩니다.</p>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Fragment의 Lifecycle에 대해 설명하시오</strong></span></summary>
<hr>
   <figure/></a></figure>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>ListView와 RecyclerView의 차이는?</strong></span></summary>
<hr>
   <p><strong>RecyclerView</strong></p>
   <ul>
      <li>layout manager</li>
   </ul>
   <ul>
      <li>viewholder 패턴 강제 구현 → View의 재사용 가능</li>
   </ul>
   <ul>
      <li>oncreateviewholder새롭게 생성될때만 호출</li>
   </ul>
   <ul>
      <li>itemdecoration과 itemanimation 있음</li>
   </ul>
   <ul>
      <li>linear/grid/staggeredgrid 레이아웃매니저 있음</li>
   </ul>
   <p><strong>ListView</strong></p>
   <ul>
      <li>findviewbyid와 inflate를 연속적으로 발생시키면 메모리와 성능에 악영향 미칠수있음</li>
   </ul>
   <ul>
      <li>수직 스크롤만 가능</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>View가 그려지는 과정에 대해 설명하시오</strong></span></summary>
<hr>
   <ul>
      <li>액티비티가 포커스를 얻으면 자신의 레이아웃을 그리도록 한다</li>
   </ul>
   <ul>
      <li>액티비티에 레이아웃의 계층구조 중 루트 노드를 제공해야함</li>
   </ul>
   <ul>
      <li>레이아웃의 루트노드에서 시작해 레이아웃 트리를 따라 이동</li>
   </ul>
   <ul>
      <li>부모 뷰는 자식 뷰 이전에 그려짐</li>
   </ul>
   <ul>
      <li>자식 뷰는 전위순회 방식으로 그려짐</li>
   </ul>
   <ul>
      <li>measure, layout 단계가 있음</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Intent와 Intent filter란 무엇인가?</strong></span></summary>
<hr>
   <p><strong>Intent</strong>란 안드로이드 컴포넌트간에 통신을 하기 위한 메세지 객체이다.</p>
   <ul>
      <li>명시적 인텐트(Explicit Intent) : 시작할 컴포넌트 이름 지정</li>
   </ul>
   <ul>
      <li>암시적 인텐트(Implicit Intent) : 컴포넌트를 제외한 나머지를 지정, 사용자가 선택</li>
   </ul>
   <p>암시적 인텐트를 통해 사용자가 어떤 앱을 사용할지 선택하도록 할 때 <strong>Intent Filter</strong>가 필요하다.</p>
   <figure>
      <a href="Android%20f06bc20888314090937a13eb90920846/Untitled%204.png"><img style="width:132px" src="Android%20f06bc20888314090937a13eb90920846/Untitled%204.png"/></a>
      <figcaption>암시적 인텐트</figcaption>
   </figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>ANR이란 무엇인가?</strong></span></summary>
<hr>
   <p>앱의 UI 스레드가 너무 오랫동안 차단되면 ANR 오류가 트리거됨</p>
   <ol>
      <li>앱이 입력 이벤트나 BroadcastReceiver에 5초 이내로 응답하지 않음</li>
   </ol>
   <ol>
      <li>포그라운드에 Activity 없는데 BroadcastReceiver가 실행을 완료하지 못함</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>인플레이션이란 무엇인가?</strong></span></summary>
<hr>
   <p>자바 소스코드에서 xml의 구성요소들을 사용할 수 있게 객체로 만들어주는것</p>
   <p>메모리상에 실제로 객체화되어 앱에 보여지는 것</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Context란 무엇인가?</strong></span></summary>
<hr>
   <p>Context란 안드로이드의 컴포넌트들이 동작하기 위해 필요한 정보를 담고 있는 것이다.</p>
   <p>Context를 통해 시스템 레벨의 정보를 얻을 수 있는 메소드를 쓸 수 있다.</p>
   <p>애플리케이션 별로 리소스 및 클래스에 대한 접근은 물론 Activity의 실행, 브로드 캐스팅 및 Intent수신과 같은 애플리케이션 레벨에 대한 호출을 허용한다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드 매니페스트 파일이란 무엇인가?</strong></span></summary>
<hr>
   <p>매니페스트는 앱의 이름, 버전, 구성요소, 권한 등 앱의 실행에 있어 필요한 각종 정보들이 저장되어있는 파일이다.</p>
   <p>안드로이드 프로젝트의 최상위에 위치하고 있다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Thread, Looper, Handler에 대해 설명하시오</strong></span></summary>
<hr>
   <p>Looper와 Handler는 스레드 간 통신을 도와준다.</p>
   <p><strong>Looper</strong></p>
   <ul>
      <li>스레드 당 하나만 가질 수 있다</li>
   </ul>
   <ul>
      <li>메시지 큐가 비어있으면 아무것도 하지않고, 메시지가 들어오면 꺼내서 Handler에 전달</li>
   </ul>
   <ul>
      <li>Main 스레드는 Looper를 가지지만, 기본적으로는 Looper를 가지지않음</li>
   </ul>
   <p><strong>Handler</strong></p>
   <ul>
      <li>Message나 Runnable 객체를 처리함</li>
   </ul>
   <ul>
      <li>Thread, Looper, MessageQueue에 의존적</li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>디스플레이(display), 윈도우(window), 서피스(surface), 뷰(view), 뷰 그룹(view group), 뷰 컨테이너(view container), 레이아웃(layout)에 대해서 설명하시오.</strong></span></summary>
<hr>
   <ul>
      <li><strong>디스플레이 </strong>: 안드로이드 단말기가 가지는 하드웨어 화면</li>
   </ul>
   <ul>
      <li><strong>윈도우 </strong>: 앱이 그림을 그릴수있는 영역</li>
   </ul>
   <ul>
      <li><strong>서피스 </strong>: 윈도우에 그림을 그릴 때 그림이 저장되는 메모리 버퍼</li>
   </ul>
   <ul>
      <li><strong>뷰 </strong>: 사용자 인터페이스를 구성하는 최상위 클래스</li>
   </ul>
   <ul>
      <li><strong>뷰 그룹</strong> : 여러개의 뷰를 포함하고 있는 뷰를 의미함</li>
   </ul>
   <ul>
      <li><strong>뷰 컨테이너</strong> : 다른 뷰를 포함하고 있는 뷰</li>
   </ul>
   <ul>
      <li><strong>레이아웃</strong> : 뷰를 윈도우에 어떻게 배치할지 정의하는 관리자</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>노티피케이션(notification)은 무엇인가?</strong></span></summary>
<hr>
   <p>안드로이드가 앱의 UI 외부에 표시하는 메시지</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>태스크(task)란 무엇인가?</strong></span></summary>
<hr>
   <p>Task란 사용자가 특정 작업을 할 때 상호작용하는 Activity의 모음이다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드의 메모리 관리 방식에 대해서 설명하시오.</strong></span></summary>
<hr>
   <p>안드로이드 런타임(ART)와 Dalvik 가상 머신은 페이징과 메모리 매핑을 통해 메모리를 관리함</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Annotation이란?</strong></span></summary>
<hr>
   <p>일종의 메타데이터</p>
   <p>컴파일/런타임 과정에서 코드를 어떻게 처리할 지 알려주는 정보</p>
   <ol>
      <li>컴파일러에게 코드 문법 에러를 체크하도록 정보 제공</li>
   </ol>
   <ol>
      <li>런타임시 특정 기능 실행하도록 정보 제공</li>
   </ol>
   <ol>
      <li>소프트웨어 개발 툴이 빌드나 배치 시 코드를 자동으로 생성할 수 있도록 정보를 제공</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>ViewPager란?</strong></span></summary>
<hr>
   <p>데이터를 페이지 단위로 표시하고, swipe를 통해 페이지를 전환할 수 있도록 만들어주는 컨테이너</p>

<hr>
</details>

<p></p>
<h2>안드로이드 심화</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>액티비티간 데이터 전달에서 임의의 클래스 객체를 바로 전달하지 못하는 이유는 무엇이고 전달하기 위해서는 어떤 처리가 필요한가?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>부모 액티비티에서 자식 액티비티의 결과 값을 받아오기 위해 어떻게 해야하는가?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>안드로이드가 리소스(resource)를 접근하는 방식에 대해서 설명하시오.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>디바이스를 회전할 때 Activity에서 일어나는 과정에 대해 설명하시오</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Singleton Pattern에 대해 설명하시오</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Viewholder Pattern이란 무엇인가?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>MVC, MVP, MVVM에 대해서 설명하시오</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>액티비티 스택에 대해 설명하시오</strong></span></summary>
<hr>

<hr>
</details>

<p></p>
<h2>안드로이드 응용</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Dependency Injection이란?</strong></span></summary>
<hr>
   <p>의존성 주입이란 외부에서 의존 객체를 주입해줘서 결합도를 줄여주는 것을 말합니다.</p>
   <p>생성자에서 주입하는 방식과 setter를 사용하는 방법이 있습니다.</p>
   <p>장점은 (1) 종속성이 감소해 변경에 대한 여파가 줄어들고, (2)재사용성이 증가하고, (3) 테스트가 용이합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Koin과 Dagger의 차이점은?</strong></span></summary>
<hr>
   <p><strong>Koin</strong></p>
   <ul>
      <li>런타임과정에 DI 주입</li>
   </ul>
   <ul>
      <li>컴파일이 빠름</li>
   </ul>
   <ul>
      <li>런타임 에러 가능</li>
   </ul>
   <ul>
      <li>Module에서 선언한 DI를 캐시에 저장하고 by inject로 캐시를 조회해서 객체를 가져옴</li>
   </ul>
   <p><strong>Dagger</strong></p>
   <ul>
      <li>Annotation을 통해 컴파일과정에 DI 주입</li>
   </ul>
   <ul>
      <li>컴파일은 느리지만 런타임에서 에러 발생하지 않음</li>
   </ul>
   <ul>
      <li>컴파일 시 오버헤드 발생</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>SharedPreferences란?</strong></span></summary>
<hr>
   <ul>
      <li>키-값 쌍이 포함된 파일을 가리킴</li>
   </ul>
   <ul>
      <li>데이터를 파일로 저장하므로 앱을 삭제하면 데이터도 삭제됨</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>DiffUtil이란?</strong></span></summary>
<hr>
   <p>두 목록 간의 차이점을 찾고 업데이트되어야 할 목록을 반환함</p>
   <p>추가 및 제거 작업할 아이템을 찾기위해 O(n) 소요</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>직렬화와 역직렬화란?</strong></span></summary>
<hr>
   <p><strong>직렬화</strong></p>
   <ul>
      <li>객체를 연속적인 데이터로 변형해 전송 가능한 형태로 만드는것</li>
   </ul>
   <ul>
      <li>JVM 메모리에 상주되어있는 객체를 바이트 형태로 변환</li>
   </ul>
   <p><strong>역직렬화</strong></p>
   <ul>
      <li>직렬화된 파일을 다시 객체의 형태로 만드는것</li>
   </ul>
   <ul>
      <li>직렬화된 바이트 형태의 데이터를 객체로 변환해 JVM으로 상주시킴</li>
   </ul>
   <p><strong>직렬화해야하는 이유</strong></p>
   <ul>
      <li>디스크에 저장하거나 통신에는 value type만 가능하고 reference타입은 불가능</li>
   </ul>
   <ul>
      <li>PC마다 사용하고 있는 메모리 주소는 다르다.</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Immutable이란?</strong></span></summary>
<hr>
   <p>값을 변경할 수 없는 것</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Image Loading 라이브러리에는 어떤 것이 있는가?</strong></span></summary>
<hr>
   <p><strong>Glide</strong></p>
   <ul>
      <li>화질이 더 안좋음</li>
   </ul>
   <ul>
      <li>메모리 덜 씀</li>
   </ul>
   <p><strong>Picasso</strong></p>
   <ul>
      <li>화질 좋음</li>
   </ul>
   <ul>
      <li>메모리 더 씀</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Android Ktx이란?</strong></span></summary>
<hr>
   <ul>
      <li>코틀린 개발용 확장 라이브러리</li>
   </ul>
   <ul>
      <li>확장함수, 람다, 이름이 지정된 매개변수, 코루틴 등 지원</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>데이터바인딩이란?</strong></span></summary>
<hr>
   <p><strong>데이터바인딩</strong></p>
   <ul>
      <li>데이터를 결합시켜 동기화하는 방식</li>
   </ul>
   <p><strong>안드로이드 데이터바인딩 라이브러리</strong></p>
   <ul>
      <li>UI 컴포넌트와 데이터를 programmatic하게 연결하지 않고, 선언형으로 결합하도록 도와줌</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>GSON이란?</strong></span></summary>
<hr>
   <p>JSON과 JAVA 사이의 직렬화와 역직렬화를 도와주는 라이브러리</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Retrofit과 Okhttp란?</strong></span></summary>
<hr>
   <p><strong>Retrofit</strong></p>
   <ul>
      <li>Type-safe한 HttpClient 라이브러리</li>
   </ul>
   <ul>
      <li>Type-safe : 네트워크로부터 전달된 데이터를 우리 프로그램에서 필요한 형태의 객체로 받을 수 있음</li>
   </ul>
   <ul>
      <li>보통 Http 요청을 위해서는 <strong>연결, 캐싱, 재시도, 스레딩, 응답 분석, 오류 처리</strong> 등을 해야하는데, 라이브러리는 이것들을 알아서 해줌</li>
   </ul>
   <p><strong>OkHttp</strong></p>
   <ul>
      <li>REST API와 HTTP통신을 간편하게 구현할 수 있도록 도와주는 라이브러리</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>Volley와 Retrofit의 차이는?</strong></span></summary>
<hr>
   <p><strong>Volley</strong></p>
   <ul>
      <li>용량이 작고 빠른 실행 속도</li>
   </ul>
   <ul>
      <li>동시 네트워크 연결</li>
   </ul>
   <ul>
      <li>요청 우선순위 지원</li>
   </ul>
   <ul>
      <li>JSON Object나 Array 반환</li>
   </ul>
   <p><strong>Retrofit</strong></p>
   <ul>
      <li>속도가 빠르다</li>
   </ul>
   <p></p>
   <figure/></a></figure>

<hr>
</details>
