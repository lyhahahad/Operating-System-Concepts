# shell, basic commands.<br>

1. shell : os에 접근할 수 있도록 만들어주는 인터페이스이다. 리눅스 커널은 유저가 프로그램과 인터페이싱하기 위해서 system call이라는 인터페이스를 제공하는데 system call은 function level에서의 인터페이스이기 때문에 유저가 조금 더 쉽게 명령어 기반으로 사용할 수 있도록 제공하는 것이 shell이다.<br>

shell의 기능<br>
1.다른 프로그램들을 command line으로 실행시킴.<br>
2.운영체제 안에 있는 파일, 프로세스들을 관리.<br>

2.commonly used shells<br>
 -/bin/sh     : The Bourne Shell / POSIX shell<br>
 -/bin/csh    : C shell<br>
 -/bin/tcsh   : Enhanced C Shell<br>
 -/bin/ksh    : Korn shell<br>
 -/bin/bash  : Free ksh clone<br>

기본적으로 사용하는 shell은 bash이다.<br>
shell은 사용자가 명령어를 입력하게 되면 입력 받은 command를 파싱해서 명령어를 알아낸 후 이를 실행해서 커널에 전달함.<br>