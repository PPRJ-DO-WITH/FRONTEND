## 역할 분담 예시

### 팀원 1: 로그인 시스템 및 공통 컴포넌트
- 로그인/회원가입 페이지 UI 개발
   UI 개발(입력필드, 버튼)

- 공통 컴포넌트(Button, Modal 등)
   공통 레이아웃 컴포넌트:
   헤더, 푸터, 사이드바 개발.


### 팀원 2: 대시보드 및 API 연동
- 대시보드 페이지 UI 개발
- API 연동 및 데이터 처리
- React Router를 사용한 페이지 전환 설정



components 폴더는 재사용 가능한 작은 단위의 UI 요소를 관리합니다.
이곳의 컴포넌트는 특정 페이지에 국한되지 않고, 여러 페이지에서 공통으로 사용될 수 있습니다.
1.1 기본 역할
-UI의 작은 블록: 버튼, 카드, 모달 등.
-재사용 가능한 컴포넌트: 프로젝트 전반에서 사용할 수 있는 공통 요소.
-프리젠테이셔널 컴포넌트: 상태 관리가 없고, 단순히 데이터를 받아 화면에 표시.

1.2 폴더구조
components/
├── Button/
│   ├── Button.js          # 버튼 컴포넌트
│   └── Button.module.css  # 버튼 스타일
├── Card/
│   ├── Card.js            # 카드 컴포넌트
│   └── Card.module.css    # 카드 스타일
├── Modal/
│   ├── Modal.js           # 모달 컴포넌트
│   └── Modal.module.css   # 모달 스타일
└── Header/
    ├── Header.js          # 헤더 컴포넌트
    └── Header.module.css  # 헤더 스타일




pages 폴더는 각각의 페이지를 구성하는 루트 컴포넌트를 관리합니다.
이곳의 컴포넌트는 페이지 단위로 큰 구조를 정의하고, 필요한 하위 컴포넌트를 조합합니다.

2.1 기본 역할
-라우팅에 연결된 컴포넌트: 페이지가 URL에 따라 렌더링될 수 있도록 설정.
-상태 관리와 데이터 처리: API 호출, 상태 관리 등 페이지 단위의 작업 수행.
-하위 컴포넌트를 조합: components에서 만든 공통 컴포넌트를 조합하여 페이지를 구성.

2.2 폴더구조
pages/
├── Home/
│   ├── Home.js            # 홈 페이지
│   └── Home.module.css    # 홈 페이지 스타일
├── About/
│   ├── About.js           # About 페이지
│   └── About.module.css   # About 스타일
├── Login/
│   ├── Login.js           # 로그인 페이지
│   └── Login.module.css   # 로그인 스타일
└── Dashboard/
    ├── Dashboard.js       # 대시보드 페이지
    └── Dashboard.module.css # 대시보드 스타일