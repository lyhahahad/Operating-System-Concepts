# summary
![20220311105823](https://user-images.githubusercontent.com/96465753/157787457-268fdf5d-67f5-45bf-b4bd-c2ba316b9ee5.png) <br>
1. 상황.
sudo apt-get update 실행시 다음과 같은 에러 발생.
'Temporary failure resolving 'url''
우선 sudo apt-get update는 모든 소스에서 패키지 정보를 다운로드합니다.<br>
/etc/apt/sources.list 파일 및 /etc/apt/sources.list.d/ 디렉토리에 있는 기타 파일에 종종 정의되는 소스<br>
update를 실행하면 인터넷을 통해 패키지 정보를 다운로드합니다.

2. 도메인 주소 찾아가는 방법<br>
로컬 캐시 조회 -> etc/hosts 조회->dns조회
dns는 etc/resolv.conf에 있는 주소를 통해 조회한다.<br>
위의 내용과 정리해서보면 update는 sources.list에 있는 패키지 정보를 resolv.conf에 있는 dns 주소를 통해 조회하고 다운로드한다.<br>

resolv.conf 조회 결과<br>
#[network]<br>
#generateResolvConf = false<br>
nameserver 172.22.144.1<br>
nameserver는 url주소를 ip주고로 변화해주는 일을 하는 서버이다.
만약 이부분에서 문제가 생긴다면 이부분을 바꿔주어야 한다.

3. nameserver가 제대로 작동하는지 확인하기.<br>
nslookup url nameserver<br>
172.22.144.1 안된다면 8.8.8.8로 바꿔보기.<br>

name server란?<br>
DNS란 도메인 네임 시스템의 약자로 URL을 특정 서버 IP에 맴핑해준다. 이를 NAMESERVER라고 부르기도 한다. nameserver가 해당 주소에 대한 ip정보를 갖고 있지 않을 때 에러가 발생할 수 있다.<br>
이때 대형 dns 서비스 업체의 dns를 사용하면 해결할 수 있다. ex)8.8.8.8(Google)<br>

