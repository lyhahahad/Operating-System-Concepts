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

3. shell interactive use
4. simple commands
5. frequently used commands
pwd : 현재 자신의 디렉터리 path를 보여줌
cd : change directory
cat : text file에 대한 내용을 읽어서 바로 display(standard output, 즉 터미널에 바로 출력)
chmod : file에 대한 속성(access permission)을 바꿈
vi : vi text editor을 실행
ls : 현재 디렉터리의 파일들을 나열
rm : remove
mv : move ( +2개의 option이 필요)
cp : copy (option - source file, destination file)
touch : empty file을 생성
mkdir : make directory
rmdir : remove directory
more : 터미널 창에서 나열되는 정보들이 창을 넘어갈 경우, 정보를 터미널 창에 맞도록 끊어서 출력
od : binary file 출력
ln : 파일에 대한 link를 만듦 (symbolic or hard link)
file : 해당 file에 대한 속성을 출력
passwd : password 변경
split : file을 다른 file로 분할

6. linux file system
리눅스 파일 시스템은 루트를 기반으로 한 계층적 트리구조이다. 

