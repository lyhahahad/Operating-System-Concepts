1. 상황.
sudo apt-get update 실행시 다음과 같은 에러 발생.
'Failed to fetch'
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

3. nameserver가 제대로 작동하는지 확인하기.
nslookup url nameserver
172.22.144.1 안된다면 8.8.8.8로 바꿔보기.