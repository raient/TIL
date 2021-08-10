## GitHub
- 분산 버전관리툴 Git을 지원합는 웹호스팅 서비스
- 유명 오픈 소스 프로그램들의 저장소 및 협업 장소
- 개발자의 이력관리 수단


## Git 동작원리
![Git 동작원리](\img\git 동작원리.jpg)


## Git 사용법 (local)

#### 1. git 다운로드 및 설치
    https://git-scm.com/download/win

#### 2 설치 확인 후 초기 세팅 / Github에 회원 등록
```bash
$ git --version (hyphen 기호가 2개) 
$ git config --global user.name “Bigdata Kim“ 
$ git config --global user.email bigdata@naver.com
```
#### 3.작업할 디렉토리에서 새로운 저장소를 생성 cmd 
- (예, d:\Workspace\python)
- (새로운 명령 프롬프트 앱 실행) 
    - d: cd \Workspace\python 
    
```bash
$ git init (하나의 PC에 여러 개의 저장소 생성 가능)
```

#### 4.Working Directroy에서 작업 수행 
- notepad test.txt

#### 5.파일을 Staging Area(준비 상태)로 보내기 
```bash
$ git add filename (특정 파일만 준비 상태)
$ git add .(모든 파일 준비 상태)
$ git status
```
- (통상 git add . 으로 사용) git status 로 상태 확인 가능


#### 6.파일을 확정함 
```bash
$ git commit -m “First Commit“ 
```
- (따옴표 안에 쓰고 싶은 말 쓰면 됨) git log 로 결과 확인 가능


## Github 사용법 (remote)

#### 1.GitHub에 저장소(Repository) 생성 
- 저장소(Repository)의 이름(Test)과 간단한 설명(Testing GitHub Operation)을 입력

#### 2. 브란치 이름 변경
- 기본 생성 branch 이름을 ‘master’에서 ‘main’으로 변경 
```bash 
$ git branch –M main
```

#### 3. local과 remote 연결
- 필요한 URL과 Command 복사한 후 “명령 프롬프트” 앱에서 실행 
```bash
$ git remote add origin https://github.com/ckiekim/Test.git

$ git remtoe -v (클론한 저장소의 retmoe 정보 확인)
```

#### 4.로컬에서 확정한 파일을 원격저장소에 보관하고 배포함 
```bash
$ git push -u origin main (최초 실행시) 
$ git push (이후에는 git push만 하면 됨)
```

#### 5. 원격저장소의 변경내용 가져 오기
```bash
$ git pull
```

#### 6. 원격 저장소를 새로운 로컬에 복사하기
```bash 
$ git clone https://github.com/~/project.git```
```