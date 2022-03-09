1. 시스템 프로그래밍이란?
os의 커널 및 핵심 라이브러리를 사용하여 hw와 소통하는 시스템 sw를 프로그래밍하는 것이다. 때문에 우선 os의 역할과 os에서 제공하는 시스템 콜의 종류를 파악해야 한다.

2. os란?
사용자와 hw의 중개자로 리소스 allocator, programmer controler이기도 하다.
주요 기능으로는 다양한 유저가 동시에 접속할 수 있도록하고 프로세스를 스케줄링하고 입출력 장치와의 통로를 담당한다.

3. 컴퓨터 시스템이란?
sw(application, os kernel) - architecture - hw(cpu, memory, i/o)
application은 os 위에서 동작하고 시스템 리소스를 사용할 때 시스템 콜 인터페이스를 이용해 필요한 기능을 os에 요청할 수 있다.

4. Layered Linux Structure
user
shell and commands
system-call interface to kernel
kernel interface to hw
핵심은 kernel이다.
kernel의 핵심 기능은 5가지이다.
process 관리(cpu 스케쥴링)
메모리 관리
파일 시스템 관리
디바이스 드라이버 관리
네트워크 관리
커널은 위쪽으로는 시스템콜 인터페이스, 아래쪽으로는 hw 커널 인터페이스를 제공한다.
시스템 콜 인터페이스란 유저가 커널의 영역을 활용할 수 있도록 하는 인터페이스이다.
shell, complier, interpreter를 통해 유저의 요청을 커널에 전달할 수 있다.
하드웨어 커널 인터페이스를 이용하면 하드웨어 디바이스 드라이버 등 sw를 이용하여 하드웨어를 제어할 수 있다.
요약 : os의 핵심은 kernel이고 kernel은 cpu, 메모리, 파일, 디바이스, 네트워크를 관리한다. 이러한 핵심 기능들은 유저 레벨의 프로그램에서 시스템콜을 통해 사용할 수 있다.
유저는 유저 레벨의 프로그램에서 혹은 shell, library routine을 거쳐 커널에 접근할 수 있다.

## 요약
시스템 프로그래밍이란 시스템 콜과 시스템콜을 래핑하는 쉘, 라이브러리 루틴을 이용해 애플리케이션 프로그램을 작성해 시스템 유틸리티를 사용하는 것이다.
user-system calls or library calls-oskernel-hw
> ![20220309135638](https://user-images.githubusercontent.com/96465753/157375707-88bc9a5b-421d-4113-9be1-6d224330aeaa.png)
