# 학생/학부모를 위한 코로나19 모니터링 앱 개발
## 1. 개발 취지
- 코로나19 바이러스 확산에 따른 학교 개학 연기 지속 확산(20.3월)
- 20학년도 1학기 개학 지속 연기 불가에 따른 일부 개학 추진에 따라
  학부모의 자녀 등교에 대한 우려 증가
- 자녀의 등교 후 발열상태 및 활동반경 모니터링의 필요성 증가

## 2. 요구사항 파악
### (1) 학교에서 자녀의 체온상태, 활동 모습을 볼 수 있었으면 좋겠다.
- 등교 시 자녀의 체온 자동 측정
- 체온 측정 시 모습을 동영상으로 기록

### (2) 등교 후 그날의 자녀 심리적 상태가 궁금하다.
- 주어진 단어에 대한 그림을 그릴 수 있는 캔버스를 제공
- 주어진 그림을 보고 연상되는 단어를 입력할 수 있는 기능 제공
    + 그림과 단어를 통해 자녀의 심리 상태를 간접 파악함.

## 3. 개발 컨셉
### (1) 체온, 동영상 측정용 Robot 개발
- 아이들에게 친숙한 펭수 인형을 활용, 인형 하단에 주행가능한 Robot을 부착하는 형태
    + 인형 내부에 구동용 라즈베리파이 보드 + Touch Display + 웹캠 + 열감지 센서를 부착함
    + 하단 주행 Robot에는 주행 중 충격 발생 시 회피 기능 추가

### (2) 원격지에서 모니터링 가능한 앱 개발
- 로그인 후 학생/부모/관리자용 모니터링 화면 개발
    + 부모용 : 해당 자녀의 체온, 동영상, 그림보기, 단어보기 기능 제공
    + 아이용 : 자신의 체온, 동영상, 그림그리기, 단어입력하기 기능 제공
    + 관리자 : 반 전체 아동의 체온상태 모니터링 기능 제공

## 4. 개발 Tool 선정
- 프로그래밍 언어 : Python + TKinter
    + 선정이유 : 범용성, 확장성 용이. 언어 접근성 용이. UI적 구현 유리함.
- 하드웨어 : 라즈베리파이
- OS : 우분투

## 5. 팀별 업무 분장
### (1) 펭수 로봇 개발 : 
- 주행 Robot 조립 및 구동용 보드 연계
- Robot 조작 프로그램 구현

### (2) 체온 모니터링 앱 개발
- 