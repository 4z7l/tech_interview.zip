# Network

<h2>전산 기본</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>OSI 7계층에 대해서 설명해주세요.</strong></span></summary>
<hr>
   <p>나눈 이유 : 통신이 일어나는 과정을 단계별로 알수있고, 문제가 생기면 그 단계만 수정하면 됨</p>
   <ul>
      <li><strong>물리 </strong>: 데이터 전송 ex) 리피터, 케이블, 허브</li>
   </ul>
   <ul>
      <li><strong>데이터링크 </strong>: 물리 계층으로 송수신되는 정보 관리, Mac 주소로 통신 ex) 브릿지, 스위치</li>
   </ul>
   <ul>
      <li><strong>네트워크 </strong>: 데이터를 목적지까지 전달, 라우터로 경로를 선택해 IP 지정, 경로에 따라 패킷 전달 ex) 라우터, IP</li>
   </ul>
   <ul>
      <li><strong>전송 </strong>: 통신을 활성화 ex) TCP, UDP</li>
   </ul>
   <ul>
      <li><strong>세션 </strong>: 데이터가 통신하기 위한 논리적 연결 담당 ex) API, Socket</li>
   </ul>
   <ul>
      <li><strong>표현 </strong>: 데이터 표현에 대한 독립성을 제공하고 암호화 ex) JPEG, MPEG</li>
   </ul>
   <ul>
      <li><strong>응용 </strong>: 최종 목적지, 응용프로그램과 연관하여 서비스 수행 ex) HTTP, FTP, DNS</li>
   </ul>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TCP/IP 4계층에 대해서 설명해주세요.</strong></span></summary>
<hr>
   <p>1계층 네트워크 액세스 : 물리+데이터링크, MAC주소 사용</p>
   <p>2계층 인터넷 : 네트워크, 통신 노드간의 IP패킷을 전송하는 기능과 라우팅 기능 담당</p>
   <p>3계층 전송 : 전송, 통신 노드간의 연결 제어 및 신뢰성 있는 데이터 전송 담당</p>
   <p>4계층 응용 : 세션+표현+응용, 응용 프로그램 구현</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>DNS가 무엇인가요?</strong></span></summary>
<hr>
   <p>IP주소를 문자로 표현한 주소로 바꾸는 시스템 혹은 서버</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>www.naver.com에 접속할때 일어나는 일에 대해 설명해주세요.</strong></span></summary>
<hr>
   <ol>
      <li>사용자가 브라우저에 도메인 네임(<a href="http://www.naver.xn--com%29-8040a/">www.naver.com)을</a> <strong>입력</strong>한다.</li>
   </ol>
   <ol>
      <li>사용자가 입력한 URL 주소 중에서 <strong>도메인 네임(Domain Name) 부분을 DNS 서버에서 검색</strong>하고, DNS 서버에서 해당 도메인 네임에 해당하는 <strong>IP 주소를 찾아 사용자가 입력한 URL 정보와 함께 전달</strong>한다.</li>
   </ol>
   <ol>
      <li>페이지 URL 정보와 전달받은 IP 주소는 <strong>HTTP 프로토콜을 사용하여 HTTP 요청 메시지를 생성</strong>하고, 이렇게 생성된 HTTP 요청 메시지는 <strong>TCP 프로토콜을 사용하여 인터넷을 거쳐 해당 IP 주소의 컴퓨터로 전송</strong>된다.</li>
   </ol>
   <ol>
      <li>이렇게 도착한 HTTP 요청 메시지는 HTTP 프로토콜을 사용하여 웹 페이지 URL 정보로 변환되어 <strong>웹 페이지 URL 정보에 해당하는 데이터를 검색</strong>한다.</li>
   </ol>
   <ol>
      <li>검색된 웹 페이지 데이터는 또 다시 <strong>HTTP 프로토콜을 사용하여 HTTP 응답 메시지를 생성</strong>하고 <strong>TCP 프로토콜을 사용하여 인터넷을 거쳐 원래 컴퓨터로 전송</strong>된다.</li>
   </ol>
   <ol>
      <li>도착한 <strong>HTTP 응답 메시지는 HTTP 프로토콜을 사용하여 웹 페이지 데이터로 변환</strong>되어 웹 브라우저에 의해 출력되어 사용자가 볼 수 있게 된다.</li>
   </ol>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>도메인 이름으로 실제 IP를 어떻게 찾을 수 있는지 흐름을 설명해 주세요.</strong></span></summary>
<hr>
   <p><strong>Recursive Query를 통해 접근 : Local DNS 서버 -&gt; Root DNS 서버 -&gt; com DNS 서버 -&gt; naver.com DNS 서버</strong></p>
   <ol>
      <li>로컬 DNS서버에 해당 url이 등록되어있는지 확인</li>
   </ol>
   <ol>
      <li>루트 DNS서버에 문의 후 최상위 도메인 .com이 등록된 네임 서버의 IP주소 전달</li>
   </ol>
   <ol>
      <li>로컬 DNS서버는 com DNS 서버에 해당 url을 문의함. 로컬 DNS서버에 naver.com DNS 서버의 IP 주소 알려줌</li>
   </ol>
   <ol>
      <li>naver..com에 해당 url 문의함. 로컬 DNS는 IP 주소를 받을수있음</li>
   </ol>
   <figure/></a></figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>유니캐스트, 멀티캐스트, 브로드캐스트란?</strong></span></summary>
<hr>
   <p>유니캐스트 : 특정 대상과 1:1 통신</p>
   <p>멀티캐스트 : 특정 다수와 1:N 통신</p>
   <p>브로드캐스트 : 네트워크에 있는 모든 대상과 통신</p>
   <p></p>

<hr>
</details>

<p></p>
<h2>TCP/UDP</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TCP와 UDP의 차이에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <p><strong>TCP</strong></p>
   <ul>
      <li>신뢰성 있는 데이터 전송을 지원하는 연결 지향형 프로토콜</li>
   </ul>
   <ul>
      <li>흐름제어, 혼잡제어, 오류제어 지원</li>
   </ul>
   <ul>
      <li>연결 설정시 3 way handshake를, 연결 해제시 4 way handshake 진행</li>
   </ul>
   <ul>
      <li>UDP보다 속도가 느리다</li>
   </ul>
   <ul>
      <li><strong>EX)</strong> 웹 http 통신, 이메일, 파일 전송</li>
   </ul>
   <p><strong>UDP</strong></p>
   <ul>
      <li>데이터를 데이터그램 단위로 처리하는 프로토콜</li>
   </ul>
   <ul>
      <li>신뢰성 낮음</li>
   </ul>
   <ul>
      <li>속도가 빠르고 부하가 적다</li>
   </ul>
   <ul>
      <li><strong>EX)</strong> Real Time Protocol(RTP), Multicast, DNS</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TCP 헤더에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>MTU가 무엇인가요?</strong></span></summary>
<hr>
   <p><strong>Maximum Transmission Unit</strong></p>
   <ul>
      <li>패킷이나 프레임의 최대 크기</li>
   </ul>
   <ul>
      <li>데이터의 크기가 크다면 단편화해야함</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>3-way hand shake, 4-way hand shake 흐름에 대해서 설명해주세요.</strong></span></summary>
<hr>
   <h3>3 way handshake</h3>
   <ul>
      <li>TCP/IP 프로토콜을 사용해 통신을 진행할떄, 두 종단간 정확한 데이터 전송 보장하기 위해 연결을 설정</li>
   </ul>
   <ul>
      <li>SYN(Synchronize Sequence Number)</li>
   </ul>
   <ul>
      <li>ACK(Acknowledgement)</li>
   </ul>
   <ol>
      <li><strong><mark class="highlight-yellow_background">클라이언트</mark></strong> → <strong><mark class="highlight-purple_background">서버</mark></strong> : <mark class="highlight-red">서버 접속 요청 </mark><mark class="highlight-red"><strong>SYN 패킷</strong></mark> 보냄</li>
   </ol>
   <ol>
      <li><strong><mark class="highlight-purple_background">서버</mark></strong> → <strong><mark class="highlight-yellow_background">클라이언트</mark></strong> : <mark class="highlight-orange">요청 수락 응답 </mark><mark class="highlight-orange"><strong>ACK 패킷</strong></mark>과 <mark class="highlight-teal">포트 열어달라는 </mark><strong><mark class="highlight-teal">SYN 패킷</mark></strong> 보냄</li>
   </ol>
   <ol>
      <li><strong><mark class="highlight-yellow_background">클라이언트</mark></strong> → <strong><mark class="highlight-purple_background">서버</mark></strong> : <mark class="highlight-blue">확인 응답으로 </mark><mark class="highlight-blue"><strong>ACK 패킷</strong></mark> 보냄</li>
   </ol>
   <ul>
      <li>
         <details>
            <summary>사진</summary>
<hr>
            <figure/></a></figure>
         </details>
      </li>
   </ul>
   <h3>4 way handshake</h3>
   <ul>
      <li>연결 설정 해제함</li>
   </ul>
   <ol>
      <li><strong><mark class="highlight-yellow_background">클라이언트</mark></strong>→ <strong><mark class="highlight-purple_background">서버</mark></strong> : <mark class="highlight-red">연결 해제하겠다는 </mark><strong><mark class="highlight-red">FIN 패킷</mark></strong> 보냄</li>
   </ol>
   <ol>
      <li><strong><mark class="highlight-purple_background">서버</mark></strong> → <strong><mark class="highlight-yellow_background">클라이언트</mark></strong> : <mark class="highlight-orange">응답으로</mark><strong><mark class="highlight-orange"> ACK 패킷</mark></strong> 보냄</li>
   </ol>
   <ol>
      <li><strong><mark class="highlight-purple_background">서버</mark></strong> → <strong><mark class="highlight-yellow_background">클라이언트</mark></strong>: 처리해야할 모든 통신 끝내고 <mark class="highlight-teal">연결 종료하겠다는 </mark><strong><mark class="highlight-teal">FIN 패킷</mark></strong> 보냄</li>
   </ol>
   <ol>
      <li><strong><mark class="highlight-yellow_background">클라이언트</mark></strong>→ <strong><mark class="highlight-purple_background">서버</mark></strong> : <mark class="highlight-blue">확인 응답으로 </mark><strong><mark class="highlight-blue">ACK 패킷</mark></strong> 보냄</li>
   </ol>
   <ul>
      <li>
         <details>
            <summary>사진</summary>
<hr>
            <figure/></a></figure>
         </details>
      </li>
   </ul>

<hr>
</details>

<p></p>
<h2>HTTP</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP 프로토콜에 대해서 아는대로 말해주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP와 HTTPS 의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p>HTTP는 인터넷 상에서 클라이언트와 서버가 자원을 주고받기 위한 통신규약인데, 텍스트로 자원을 주고받기 때문에 네트워크를 가로챈다면 내용이 유출되는 보안 이슈가 발생할 수 있습니다.</p>
   <p>이를 해결하는 것이 HTTPS입니다.</p>
   <p>HTTPS에 SSL 프로토콜을 사용해 정보를 암호화하는데, 메모리나 리소스를 더 많이 쓸 수 있다는 특징이 있습니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTPS가 동작하는 방식에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP Method 종류 및 역할</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP 1.0과 1.1의 차이는 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP2와 그 특징에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP 헤더의 구조에 대해서 설명해 주세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>keep-alive 헤더에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <p>HTTP는 매번 연결을 끊고 새로 생성함</p>
   <p>HTTP 1.1부터는 Keep/alive를 지원</p>
   <p>특정 시간까지는 access가 없더라도 기다리고 연결된 상태를 유지함, 이미 열려있는 곳에 요청</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>HTTP GET과 POST의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p>GET : 정보 요청, body에 담지않고 쿼리로 전송</p>
   <p>POST : 데이터를 body에 담아서 리소스를 생성하거나 변경</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>쿠키와 세션에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <p>쿠키 : 클라이언트의 웹 브라우저가 지정하는 메모리/하드디스크</p>
   <p>세션 : 서버의 메모리에 저장</p>

<hr>
</details>

<p></p>
<h2>웹</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>www.google.com에 접속할때 일어나는 일</strong></span></summary>
<hr>
   <figure/></a></figure>
   <ol>
      <li>www.google.com을 브라우저 주소창에 친다.</li>
   </ol>
   <ol>
      <li>
         브라우저는 캐싱된 DNS 기록을 통해 www.google.com에 대응되는 IP 주소가 있는지 확인한다.
         <ul>
            <li>브라우저 캐시 확인</li>
         </ul>
         <ul>
            <li>OS 캐시 확인</li>
         </ul>
         <ul>
            <li>라우터 캐시 확인</li>
         </ul>
         <ul>
            <li>ISP 캐시 확인</li>
         </ul>
      </li>
   </ol>
   <ol>
      <li>요청한 URL이 캐시에 없으면 ISP의 DNS 서버가 www.google.com을 호스팅하고 있는 서버의 IP 주소를 찾기 위해 DNS query를 날림</li>
   </ol>
   <ol>
      <li>브라우저가 IP 주소를 받으면 서버와 TCP 연결을 한다. (3 way handshaking)</li>
   </ol>
   <ol>
      <li>TCP 연결이 완료되면 브라우저가 웹 서버에 HTTP 요청을 한다. GET 요청을 통해 www.google.com의 웹페이지를 요구한다.</li>
   </ol>
   <ol>
      <li>서버가 요청을 처리하고 response를 생성한다.</li>
   </ol>
   <ol>
      <li>서버가 HTTP response를 보낸다.</li>
   </ol>
   <ol>
      <li>브라우저가 HTML content를 보여준다.</li>
   </ol>
   <figure id="5f8023b0-d80e-4762-bb2e-84dc5770fd6c">
      <a href="https://devjin-blog.com/what-happen-browser-search/" class="bookmark source">
         <div class="bookmark-info">
            <div class="bookmark-text">
               <div class="bookmark-title">[번역] Browser에 www.google.com을 검색하면 어떤 일이 일어날까?</div>
               <div class="bookmark-description">개발자라면 인터넷이 어떻게 작동을 하고 정보들이 어떻게 주고 받아지는지 기본적으로 이해하는 것이 필요하다고 생각해서 공부할 겸 미디움 블로그를 번역했다. ** 내용 조금 수정 및 추가한 부분 있음 검색할 것이 있어서 www.google.com 에 접속을 하려고 할 때 웹페이지가 어떻게 불러와지는지 순서대로 설명을 하려고 한다. DNS(Doman Name System)은 URL들의 이름과 IP주소를 저장하고 있는 데이터베이스이다.</div>
            </div>
            <div class="bookmark-href"><img src="data:;base64,iVBORw0KGgo=" class="icon bookmark-icon"/>https://devjin-blog.com/what-happen-browser-search/</div>
         </div>
         <img src="https://devjin-blog.com/static/thumbnail-5bbdfc7ac4f8769dd921dd2a7dafc151.jpg" class="bookmark-image"/>
      </a>
   </figure>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>웹브라우저에서 서버로 요청했을 때, 흐름을 설명해주세요.</strong></span></summary>
<hr>
   <p>웹 브라우저가 URL해석-&gt;URL이 문법맞으면 Punycode encoding을 url의 host부분에 적용-&gt; HSTS (HTTP Strict Transport Security 목록 로드해서 체크 -&gt;DNS 확인-&gt; ARP로 IP/MAC 확인 -&gt;TCP 통신을 통해 Socket을 열고 .HTTP 프로토콜로 요청 -&gt; HTTP 서버가 응답 -&gt;  웹 브라우저가 그린다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>CORS란 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>웹 서버와 웹 어플리케이션 서버(WAS)의 차이는 무엇인가요?</strong></span></summary>
<hr>
   <p><strong>웹 서버</strong></p>
   <ul>
      <li>항상 동일한 데이터를 주는 정적 콘텐츠를 제공</li>
   </ul>
   <ul>
      <li>동적 콘텐츠 제공을 위해 WAS에 클라이언트의 요청을 보내고 결과를 전달</li>
   </ul>
   <ul>
      <li>정적 콘텐츠만 처리해 서버 부담을 줄임</li>
   </ul>
   <p><strong>웹 어플리케이션 서버(WAS)</strong></p>
   <ul>
      <li>동적인 컨텐츠를 제공</li>
   </ul>
   <ul>
      <li>DB 접속/트랜잭션 관리/비즈니스 로직 수행</li>
   </ul>
   <ul>
      <li>요청에 맞는 콘텐츠를 제공하기 위해 필요함, 단순한 정적 콘텐츠는 웹 서버에 맡겨 부하를 줄임</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>REST API에 대해서 설명해 주세요.</strong></span></summary>
<hr>
   <p>HTTP를 통해 자원을 주고 받을 때 HTTP URI를 통해 자원을 명시하고 HTTP Method를 통해 자원의 CRUD를 수행하는 것을 말합니다.</p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>REST ful</strong></span></summary>
<hr>
   <p>REST의 원리를 따르는 시스템을 말합니다. </p>
   <p>RESTful하지 못한 경우로는 (1) CRUD 기능을 POST로만 처리하는 경우나 (2) URI에 resource, id 외의 정보가 들어가는 경우입니다. </p>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>API Gateway란 무엇인가요?</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>API Gateway가 다운되면 모든 API를 사용 못할지도 모르는데, 어떤 방안을 마련해야 할까요?</strong></span></summary>
<hr>

<hr>
</details>

<p></p>
<h2>기타</h2>

<details>
   <summary><span style="border-bottom:0.05em solid"><strong>nagle 알고리즘에 대해 설명하세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TLS에 패킷 프토토콜의 대해 설명하세요</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>TLS</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>네트워크 Layer 라우팅 알고리즘</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>SNI 필드 차단</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>흐름제어 / 혼잡제어 / 오류제어</strong></span></summary>
<hr>
   <p><strong>흐름제어</strong>는 송신측과 수신측 사이의 데이터 처리 속도 차이를 해결하기 위한 기법입니다.</p>
   <p><strong>혼잡제어</strong>는 송신측의 데이터 전달과 처리 속도 차이를 해결하는 기법입니다.</p>
   <p><strong>오류제어</strong>는 패킷이 잘못 전달됐을 경우 패킷을 재전송하는 등 오류를 복구하는 기법입니다.</p>
   <p></p>
   <p><strong>흐름제어</strong></p>
   <ul>
      <li>송신측과 수신측 사이의 데이터 처리 속도 차이(흐름)를 해결하기 위한 기법</li>
   </ul>
   <ul>
      <li>송신측의 패킷 전송량 제어해서 수신측의 버퍼 오버플로우 방지</li>
   </ul>
   <p></p>
   <p><strong>오류제어</strong></p>
   <ul>
      <li>오류 검출과 재전송</li>
   </ul>
   <ul>
      <li>프레임이 손상되었거나 손실되면 재전송해서 오류 복구</li>
   </ul>
   <p></p>
   <p><strong>혼잡제어</strong></p>
   <ul>
      <li>송신측의 데이터 전달과 데이터 처리 속도를 해결하기 위한 기법</li>
   </ul>
   <ul>
      <li>네트워크 혼잡 제어를 피하기 위해 데이터의 전송 속도  제어</li>
   </ul>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>로드 밸런서 / 로드 밸런싱은 무엇인지 설명하세요.</strong></span></summary>
<hr>

<hr>
</details>


<details>
   <summary><span style="border-bottom:0.05em solid"><strong>WebRTC</strong></span></summary>
<hr>
   <p>어플리케이션(최근에는 Android 및 IOS도 지원) 및 사이트들이 별도의 소프트웨어 없이 음성, 영상 미디어 혹은 텍스트, 파일 같은 데이터를 브라우져끼리 주고 받을 수 있게 만든 기술</p>

<hr>
</details>

<p></p>
</div>
