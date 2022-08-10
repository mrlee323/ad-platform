# 📊 광고 플랫폼 대시보드 
-------
> by. 원티드 프리온보딩 4팀 (2022.07.14~19)
> 
> 🚀🚀 [배포 보러가기](https://wanted-preonboarding-ad-platform.vercel.app/)



# 👉  학습 목표

1. 라우터를 활용하여 `sub routing`을 구현한다.
2. `chart` 라이브러리를 이용하여 라인 차트, 스택차트를 구현한다.
3. `table`을 구현한다.


# 👉   기능 요구 사항

메뉴
- 메뉴에는 각 페이지로 이동하는 탭이 포함되어 있습니다. 다른 부분은 구현하지 않아도 된다.
- 메뉴는 모바일 환경에서 480px이하 접히며 헤더에 포함되고 hamburger icon 으로 변경되며 클릭시 메뉴 탭을 볼 수 있도록 화면에 노출 된다.


헤더
- 헤더는 이미지 예시와 같이 유저 아바타와 유저이름, 설정, 알림 아이콘을 포함한다.
- 설정과 알림 아이콘은 아무기능이 없어도 무관.


대시보드
- 대시보드에는 Line chart와, stacked bar chart가 포함.
- 통합 광고 현황의 데이터를  활용하여 통합 광고 현황 컴포넌트를 개발.
- 통합 광고 현황의 드랍다운을 클릭 할 때마다 데이터가 변경.
- 주간 별 조회를 할 수 있어야 합니다. 조회 주간을 변경하면 두 개의 차트 데이터도 변경.
- Line chart의데이터는 ROAS와 클릭수 를 보여주어야함.
- 매체 현황의 데이터를 활용하여 매체 현황 컴포넌트를 개발. (chart, table)


광고 관리
- 광고 관리 페이지 상단의 드랍다운으로 전체, 현재 진행중인 광고, 종료된 광고를 filtering 해야함.
- 수정 버튼을 클릭하여 수정 할 수 있고, 광고 만들기로 생성할 수 있어야 함.

# 👉  로직 
 
### 대시보드 페이지

1. 최상단 날짜 선택하면 데이터 받아오기
2. 통합 광고 현황, 매체 현황 컴포넌트에 이전 주 데이터와 함께 내려보내기

### 통합 광고 현황

1. 상단: BoardItem, BoardList 이전 주, 현재 주차 데이터로 BoardItem 렌더링하기
2. 하단: select (Mui 사용),  받은 데이터를 filter 해서 선택된 필드에 대한 Line Chart 보여주기

### 매체 현황

1. 상단: 지표(광고비, 매출, …) 마다 각각의 회사별 비중에 따라 Bar Chart 그리기
2. 하단: Table 컴포넌트 만들어서 데이터 전달하기

### 광고 관리 페이지

1. 드롭다운에 따라 데이터를 넘겨주기
2. ManageCard, ManageList 컴포넌트 만들고 반응형 처리 구현하기, 모달 백그라운드 & 띄우기
3. 수정하기, 만들기: 수정의 경우는 넘겨받은 데이터를 띄워주고, 새로 입력된 데이터를 서버에 전달
4. 삭제하기: delete 요청

# 👉  사용법

```shell
# with yarn
# install
$ yarn install

# run
$ yarn start
```

# 👉 구현 상세
---

## 🎨 [Figma](https://www.figma.com/file/Mu4NicacSniXYsGvf8tfZh/Wanted?node-id=297%3A60)
### 대시보드
![스크린샷 2022-08-10 오전 2 22 29](https://user-images.githubusercontent.com/80194405/183717159-1150562b-bdf5-4bd2-9e60-9004bb57f137.jpg)- 
### 광고관리
![스크린샷 2022-08-10 오전 2 22 51](https://user-images.githubusercontent.com/80194405/183717270-8a8fa121-d8f9-43e4-945d-a5e25b288315.jpg)
### 모바일
![스크린샷 2022-08-10 오전 2 23 15](https://user-images.githubusercontent.com/80194405/183717414-5b514dc3-58aa-40e8-9f98-75ab340d7512.jpg)

##  📊 역할

|이름|역할|github|
|---|---|---|
|이가람|글로벌 타입 선언, 대시보드 페이지 Bar Chart제작|https://github.com/devmagrfs|
|박소영|대시보드 페이지 상단 드롭다운, BoardItem, BoardList 컴포넌트|https://github.com/soyoung931014|
|이미림|디자인 목업, 전체 레이아웃|https://github.com/mrlee323|
|서소희|초기세팅, 상태 관리 라이브러리|https://github.com/greenish0902|
|성열하|대시보드 페이지 표 제작|https://github.com/Hotsumm|
|박지훈|차트 1드롭다운|https://github.com/JiehoonPark|

## 📊 기술스택

<center><img src="https://user-images.githubusercontent.com/80194405/183722053-60f85924-9a4d-4b2a-8f71-327cb6d0c525.jpg" width="300" height="300"></center>



















