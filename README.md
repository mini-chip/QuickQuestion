[![로고](/public/assets/images/logo.png)](https://github.com/Important-is-Great-Youths/QuickQuestion)

# 😺 프로젝트 소개

- 날씨에 따라 다양한 테마를 가진 익명 문답 서비스
- 기획 기간 : 24.04.19 ~ 24.04.29
- 개발 기간 : 24.04.30 ~ 24.06.07
- 배포 : [배포링크](https://quick-question-weather.vercel.app/)

## QQ(QuickQuestion) - 팀 프로젝트(Personal Fork)

> 이 저장소는 팀 프로젝트의 개인 포크로, 포트폴리오/데모 목적입니다.

### 발단

- 기존 과제 프로젝트 [**오픈마인드**](https://github.com/Important-is-Great-Youths/openmind)의 개선의 여지가 보이는 기능을 발전시키고자 함

```Plain Text
1. 질문 시 닉네임만을 볼 수 있다는 불편한 접근성 향상
2. 트랜디하지 않은 디자인과 단순한 기능의 개선
3. 보안 기능의 부재 해결
4. 기존에 사용해보지 못한 새로운 기능의 도입
```

- **닉네임 쓰는 곳에 질문을 쓰고, 짧고 빠르게 사용할 수 있는 사이트를 만들자.**

### 결과

```Plain Text
1. 질문자의 닉네임과 질문을 함께 볼 수 있도록 수정
2. 귀여운 로고와 직관적이고 깔끔한 디자인으로 수정
3. 질문자와 답변자 닉네임과 비밀번호 설정
4. 기상청 api를 활용한 테마 자동 변동
```

### 🧑‍💻 개인 기여 (My Contributions)

#### 1. 위치 기반 날씨 테마 시스템

- **useGeolocation 커스텀 훅 구현**: 사용자 위치 정보를 가져오는 재사용 가능한 훅 개발
- **기상청 API 연동**: 실시간 날씨 데이터 fetching 및 에러 핸들링
- **테마 자동 전환 로직**: 날씨 데이터에 따른 동적 UI 테마 변경 시스템 구축

#### 2. 데이터 페칭 & 상태 관리

- **React Query 아키텍처 설계**: 서버 상태 관리 및 캐싱 전략 수립
- **페이지네이션 시스템**: `onPageChange` 콜백 기반 페이지네이션 컴포넌트 구현
- **API 연동 최적화**: Card List 데이터 페칭 구조 설계 및 리팩토링

#### 3. 폼 & 모달 UX/UI

- **React Hook Form 통합**: 폼 유효성 검사 및 에러 핸들링 구현
- **Modal 컴포넌트 개발**: 재사용 가능한 모달 UI 시스템 구축
- **사용자 입력 검증**: 실시간 유효성 검사 및 피드백 제공

#### 4. 필터링 & 검색 기능

- **태그/상태 필터 시스템**: 미답변, 분야별 필터링 로직 구현
- **URL 쿼리 동기화**: 필터 상태와 URL 파라미터 양방향 동기화
- **검색 결과 최적화**: 필터링 조건에 따른 효율적인 데이터 표시

#### 5. UX 개선 & 성능 최적화

- **로딩 상태 관리**: Skeleton UI를 활용한 로딩 인디케이터 구현
- **에러 핸들링**: 사용자 친화적인 에러 메시지 및 fallback UI
- **접근성 개선**: 키보드 네비게이션 지원 및 시맨틱 마크업
- **이미지 최적화**: Next.js Image 컴포넌트를 활용한 성능 향상

> **📌 주요 기술 스택**: TypeScript, Next.js, React Query, React Hook Form, Geolocation API, 기상청 API

# 💻Features

## Main Page

![image](https://github.com/Important-is-Great-Youths/QuickQuestion/assets/96277798/3b5a0e1c-886b-4321-bcc2-783efee3ea7c)

1. **질문 등록** : 메인 페이지에서 바로 질문을 등록할 수 있다.
2. **등록 조건 부합** : 질문을 등록할 때 필수 값을 입력하지 않거나 조건에 맞지 않는 값을 입력하면 등록할 수 없다.
3. **로컬스토리지에 저장** : 질문이 등록되면 입력한 닉네임과 비밀번호가 로컬스토리지에 저장된다.
4. **리액션 수에 따른 인기 질문** : 리액션 수가 많은 순으로 인기 질문에 나타난다.
5. **슬라이드 기능** : 인기 질문에는 총 6개가 나타나고 드래그를 하거나 화살표 버튼을 클릭하여 옆으로 넘길 수 있다.

## Question List Page

![image](https://github.com/Important-is-Great-Youths/QuickQuestion/assets/96277798/cdf15e03-6f20-480e-9cd1-2074b0fd0702)

1. **미답변 필터링 기능** : 미답변 버튼을 체크하면 답변이 달리지 않은 질문들만 나오게 된다.
2. **분야 별로 필터링 기능** : 전체, 연예 등등 원하는 분야를 누르면 해당 분야의 질문만 나온다.
3. **페이지네이션 기능** : 다음, 이전 버튼을 누르면 다음 페이지로 넘어가고 숫자를 클릭하면 해당 페이지의 질문들이 나온다.

# 🛠️ Skill Stacks

## Environment

![Git](https://img.shields.io/badge/Git-f05032.svg?&style=for-the-badge&logo=Git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717.svg?&style=for-the-badge&logo=GitHub&logoColor=white)
![VSCode](https://img.shields.io/badge/VSCode-007acc.svg?&style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000.svg?&style=for-the-badge&logo=Vercel&logoColor=white)
![Storybook](https://img.shields.io/badge/Storybook-FF4785.svg?&style=for-the-badge&logo=Storybook&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-f24e1e.svg?&style=for-the-badge&logo=Figma&logoColor=white)

## Development

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6.svg?&style=for-the-badge&logo=TypeScript&logoColor=white)
<img alt='Next.js' src='https://img.shields.io/badge/Next.js-000000.svg?&style=for-the-badge&logo=Next.js&logoColor=white'/>
![CSS_Modules](https://img.shields.io/badge/CSS_Modules-000000.svg?&style=for-the-badge&logo=cssmodules&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-cc6699.svg?&style=for-the-badge&logo=sass&logoColor=white)
![REST_api](https://img.shields.io/badge/REST_api-000.svg?&style=for-the-badge)

## Libraries

![Axios](https://img.shields.io/badge/Axios-5429e4.svg?&logo=Axios&logoColor=white&style=for-the-badge)
![ReactQuery](https://img.shields.io/badge/react_query-FF4154.svg?style=for-the-badge&logo=reactquery&logoColor=white)
![reacthookform](https://img.shields.io/badge/react_hook_form-EC5990.svg?style=for-the-badge&logo=reacthookform&logoColor=white)
![NextThemes](https://img.shields.io/badge/next_themes-000.svg?&style=for-the-badge)

---

# 🔗 Links

- **배포**: [https://quick-question-weather.vercel.app/](https://quick-question-weather.vercel.app/)
- **팀 레포지토리**: [https://github.com/Important-is-Great-Youths/QuickQuestion](https://github.com/Important-is-Great-Youths/QuickQuestion)

---

> **📝 Note**: 본 개인 포크는 포트폴리오/데모 목적입니다.
