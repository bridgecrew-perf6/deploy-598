# 구조
/
    └ requirements.txt : 특정 환경에서 사용한 모듈들을 기술
                         환경이 구축될 때, 이 서비스 운영/개발시 사용한 필요한 모듈을
                         설치하기 위해 기술되는 파일
                         - 반드시 버전을 명시하며, 향후에 서버가 변경되도, 
                           문제없이 구동되겠끔 동일한 환경을 제공 
    └ run.py           : 서비스 메인
    └ wsgi.py          : 엔트리 포인트, 아파치서버가 바라보는 파일
    └ deploy.json      : 패브릭이 배포 작업을 하는데 필요한 상수값들을 저장한 파일
                         - 환경변수가 저장된 파일

# fabric 설치 
- pip(or conda) install fabric (x)
    => python2.7.x 버전에 맞게 설치가 된다
    => python3.x 버전에서 사용 불가
- pip(or conda) install fabric3 (o)
  
# github 사용
1. github.com 접속 후 저장소 생성
2. 로컬 PC에서 git 명령어를 이용하여 적절한 위치에 저장소를 다운로드
    - 현재 위치
        - $ cd Users/master13/OneDrive/__simoon/py_projects
    - 저장소에서 카피
        - $ git clone https://github.com/simoon136/deploy.git
    - 이미 작성된 내용을 카피해서 현재 만들어진 폴더 deploy 안으로 붙여 넣는다
        - 커밋 메시지 작성
        - 커밋 
            - 에러 : make sure you configure your 'user.name' and 'user email' in git
        - 공통 처리 : 
            $ git config --global user.name "본인이름"
                ex) $ git config --global user.name "simoon136"
            $ git config --global user.email ""
                ex) $ git config --global user.email "simoon3568@gmail.com"
