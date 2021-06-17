# termsStudy
### Web Basic   
#### 호스팅 (서비스): 
* 정의: 서버 컴퓨터의 전체 또는 일정 공간을 이용할 수 있또록 임대해 주는 서비스를 말한다.   
* 호스팅 종류   
* 1. 웹 호스팅 : 서버 컴퓨터의 일부 공간을 임대해 주는 서비스   
* 2. 서버 호스팅: 반적으로 서버 컴퓨터 전체를 임대하는 서비스를 뜻하나 (종류에 따라 부분 임대도 그 뜻에 포함된다)  
* 2-a) VPS 가상 서버 호스팅: 가상 서버 하나를 단독으로 호스팅 하는 방식 
* 2-b) VDS 가상 전용 서버 호스팅 : VPS 는 공유 코어가 제공 되나, VDS는 단일 코어가 제공되는 차이
# Book Review -쉽게 배우는 운영체제
## CH1. OS 개요 
#### OS 정의
* __정의__: 하드웨어를 관리 조정 하고, 사용자에게 편리한 인터페이스 환경을 제공하는 소프트웨어 이다.  
* __펌웨어__: OS는 하드웨어 존재로 정의되기 때문에 펌웨어라고도 한다  
* __하드웨어__ : 전기적 신호에 의해 기능 수행이 가능한 컴퓨터의 (물리적) 부품을 일컫는다.  
* __하드웨어__ : OS 관리 차원에서, 하드웨어를 자원으로 일컫는다. (하드웨어 = 자원 = 장치 )     
* __인터페이스__ : 두 기기 사이의 시그널 송수신 접점, 경계면   
* __인터페이스__ : 자원, OS, 사용자간의 송수신 가교 영역.   
* __인터페이스__ : 사용자는 OS에서 제공하는 인터페이스를 통해서만 자원을 사용할 수 있다.   
#### OS 필요성 
* 자원의 효율적인 관리와 컴퓨터의 성능 향상을 위해 필요하다  
#### OS 역할 
* __자원관리__ : 응용 프로그램에 자원을 적절히 배분하고, 회수한다.
* __자원보호__ : 컴퓨터 내의 많은 자원을 미숙한 사용자, 악의적인 사용자로 부터 보호한다. 
* __하드웨어 인터페이스 제공__ : 다양한 종류의 하드웨어 장치와 연결하기 위해 OS가 제공하는 인터페이스. OS에서 드라이버 설치 자동   
* __장치드라이버__ : 장치 마다 OS와 소통하기 위해 따로 인터페이스를 제공 하거나 연결해야 할때, 별도의 장치 드라이버를 설치한다. 
* __사용자 인터페이스 제공__: 사용자가 운영체제를 편리하게 사용하도록 지원한다. 
* __MS-DOS__ : 과거 OS 중 하나로, 사용자 인터페이스로 키보드만 제공 한다. 
* __GUI__ : Graphic User Interface, 마우스+ 키보드를 제공한다. 
* __Touch Screen__ : 화면 터치만으로도 사용자와 신호를 주고 받을 수 있는 인터페이스를 제공한다 

#### OS 목표 
* __효율성__ : 자원 관리 [OS가 사용하는 코드를 최적화] 
* __안정성__ : 자원 보호
* __확장성__ : 하드웨어 인터페이스 제공 [하드웨어 제작의 편리성을 고려해야 한다]
* __편리성__ : 사용자 인터페이스 제공

#### OS 역사 
|연도|컴퓨터|주요장치|특징|
|:--:|:--:|:--:|:--:|
|1940|에니악|진공관+전선|진공관으로 0,1 구현|
|1950|일괄처리시스템|천공카드리더+라인 프린터|OS등장|
|1950|일괄처리장치|IC,천공카드리더+라인 프린터|OS등장|

* __일괄처리 시스템__: 프로그램 중간에 사용자가 데이터를 입력 수정 하는것이 불가 
* autoexec.bat : 윈도우OS 부팅시 읽어 들이는 파일로 OS 시작할때 한꺼번에 처리해야 할 작업을 모아 놓은 것 
* __대화형 시스템__ : 키보드 와 모니터의 출연으로 사용자의 입력값을 중간에 확인하며 프로그래밍이 가능하게 되었다. 
* CPU 집중작업: 일괄처리시스템 처럼 프로그램이 실행되는 동안에 입출력이 불가능해 대부분의 작업이 CPU만을 사용한다. (ex 수학 계산) 
* 입출력 집중작업: 대화형시스템 처럼 프로그램이 실행되는 동안에 입출력이 가능하기 떄문에 생겨났다.  (ex 동영상)
* __시분할 시스템__: 다중프로그래밍 시스템에서 CPU 사용 시간을 아주 잘게 쪼개어 여러 작업에 나누어 주는 시스템  
* 다중프로그래밍 시스템 : CPU에서 여러 작업을 동시에 실행하는 것 
* 타임 슬라이스 : 쪼개진 CPU 사용 시간 한 조각 (타임 퀀텀)
* __실시간 시스템__: 시분할시스템에서 특정 작업이 일정 시간에 끝나는 것을 보장하지 못한다. 이를 보장하는 것이 실시간시스템
* 경성 실시간 : 지정한 응답 시간을 정확히 지키는 시스템 
* 연성 실시간 : 융통성 있는 시스템 
* __다중 사용자 시스템__: 여러 사람이 동시에 작업할 수 있는 시스템 
* __분산 시스템__: 네트 웨크상에 분산되어 있는 여러 컴퓨터로 작업을 처리하고 그 결과를 상호 교환하도록 구성한 시스템 
* __클라이언트/서버 시스템__: 시스템에 참가하는 모든 컴퓨터의 지위가 동일한 분산 시스템과 달리 요청 과 응답 이중 구조로 나눠진 시스템 
* 웹 시스템 : 전형적인 클라/서버 시스템 구조 
* 클라/서버 시스템 문제점 : 서버 과부하 (수 많은 동시 요청)
* 데몬 : 서버가 멈추지 않고 계속 작동하며 요청을 처리하는 작업을 돕는 프로그램 
* 웹데몬: 아파치 톰캣, IIS등 
* __P2P 시스템__: peer to peer 로 서버를 거치지 않고 사용자를 직접 연결하는 시스템 (mp3 공유, 냅스터)
* P2P시스템 작동원리: 같은 파일을 여러 사용자로 부터 나누어 받는다. 
* 불법소프트웨어: 저작권 문제로 P2P 시스템은 발전하지 못함
* 메세지소프트웨어: 사용자간에 직접 채팅하고 데이터를 주고 받음 P2P 시스템으로 발전 (사용자 인증등- 서버가 존재)  
* 완전P2P: 서버가 없는 시스템(비트코인, 블록체인)  
* __그리드 시스템__ : 필요한 컴퓨팅 자원을 구매하여 사용하는 컴퓨팅 환경 
* 작동원리: 분산 시스템 중 하나로, 다른 기종의 컴퓨터를 묶어 대용량의 컴퓨터 풀을 구성해 원겨지와 연결한다. 
* 그리드 딜리버리: 웹 하드 서비스에서 주로 사용, 파일을 내려받은 이력이 있는 컴퓨터로 부터 몰래 데이터를 빼와 전달하는 방식 
