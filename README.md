수행은 92쪽까지

### 정보보호의 3요소
* 기밀성 : 적절한 권한이 있는 사용자만 접근하도록
* 가용성 : " 사용자만 변경하도록
* 무결성 : 적절한 시간에 인가된 사용자가 접근 가능하도록

### 정보보호전문가의 조건
윤리의식

### 조직 내에서 사용하는 네트워크
인트라넷
* TCP/IP, SMTP를 기반으로 구축

### 방화벽의 주요 기능
* 접근제어
* 로깅과 감사추적
* 인증
* 주소 변환
* 데이터 암호화

### 방화벽 구성 요소
* 배스천 호스트
* 스크리닝 라우터
* 단일 홈 게이트웨이
* 이중 홈 게이트웨이
* 스크린된 호스트 게이트웨이

### 침입탐지 시스템의 분류
* 데이터 근원지에 따라 분류 - 호스트 기반, 네트워크 기반
* 침입탐지 모델에 따라 분류 - 오용 침입탐지 방법, 비정상 행위 침입탐지 방법

### 침입차단 시스템
기존의 침입탐지 시스템이 탐지만 했다면 이건 연결을 끊는 등 적극적인 방어.
* 분류 - 호스트 기반, 네트워크 기반

### 기타 보안시스템
* 웹 방화벽 - 80번 포트, 443번 포트
* 스팸 차단 장비
* 통합 보안관리 시스템

### OSI 7계층
1. 물리 계층 - [비트스트림] 물리적, 전기적. 허브나 DSU
2. 데이터 링크 계층 - [프레임] 이더넷 프로토콜, 브릿지, 스위치, 통신에 MAC주소 사용
3. 네트워크 계층 - [패킷] 라우팅, 흐름 제어, 세그멘테이션, 오류 제어. ICMP, OSPF, RIP 등의 프로토콜 사용
4. 전송 계층 - [세그먼트] 패킷에 순번 부여, 전송 실패 패킷을 재전송. TCP, UDP, SSL, TLS
5. 세션 계층 - 통신을 동기화
6. 표현 계층 - 암호, 압축
7. 응용프로그램 계층 - 사용자와 프로그램 사이에 데이터 교환. HTTP, FTP

### TCPIP 4계층
1. 네트워크 인터페이스 계층
2. 인터넷 계층
3. 전송 계층
4. 응용프로그램 계층

### 이더넷 프로토콜
* 프리앰블 - 패킷이 입력되고 있음을 알리기 위한 부분. 1010101 값이 입력됨.
* 프레임 시작구분자 - 1이 입력됨.
* 목적지 MAC주소, 출발지 MAC주소
* 패킷의 최소길이는 64바이트, 최대길이는 1500바이트

### ARP
* 특정 IP를 가진 시스템의 MAC주소를 알아내기 위함
* ARP Request 패킷은 목적지 주소를 FF.FF.FF.FF.FF.FF값으로 브로드캐스팅
* 이때 해당 IP를 가진 시스템은 자신의 MAC주소를 ARP Reply 패킷으로 보냄.
* 반대로 클라이언트가 자신의 MAC주소를 알지만 IP주소를 모를 때는 RARP를 쓰지만 현재는 BOOTP 또는 DHCP를 많이 씀

### ICMP
* 수신지에 도착하지 못했을 때 - ICMP Destination Unreachable
* 시스템이 적절하지 못한 경로를 이용하거나 2개 이상의 라우터가 함께 운영될 경우 다른 라우터를 통해 통신하게 함 - ICMP Redirect
* TTL이 0이 되면 패킷을 폐기하고 - ICMP Time Exceeded
* 라우터 트래픽을 완화시키기 위해 송신 패킷의 양을 제어 - ICMP Source Quench

### TCP 특징
* 높은 신뢰성
* 가상 회선 연결 방식
* 데이터 체크섬
* 시간 초과와 재전송
* 데이터 흐름 제어

### TCP 연결 생성(3-way handshaking)
1. 클라이언트는 closed, 서버는 listen
2. SYN ->
3. <- SYN + ACK
4. ACK ->

### TCP 연결 해제
1. 클라이언트와 서버 모두 established
2. FIN ->
3. <- ACK
4. <- FIN
5. ACK ->

### UDP
* 비연결 지향형
* 네트워크 부하 감소
* 비신뢰성
* 전송된 데이터의 일부가 소실됨
