
[![로고](/public/assets/images/logo.png)](https://github.com/Important-is-Great-Youths/QuickQuestion)

# 😺 프로젝트 소개

- 날씨에 따라 다양한 테마를 가진 익명 문답 서비스
- 기획 기간 : 24.04.19 ~ 24.04.29
- 개발 기간 : 24.04.30 ~ 24.06.07

## QQ(QuickQuestion) - 팀 프로젝트(Personal Fork)
> 이 저장소는 팀 프로젝트의 개인 포크로, 포트폴리오/데모 목적입니다. 원본 저장소 및 크레딧은 Attribution & Credits에 확인부탁드립니다.

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
### 🧑‍💻 What I Built (개인 기여)

```Plain Text
* 위치 기반 useGeolocation 훅 구현 및 날씨 테마 연동
* 리스트 페이지네이션(onPageChange 콜백) + React Query 데이터 페칭 구조 설계
* Modal UI & 폼 유효성 검사(React Hook Form)
* 태그/상태 필터(미답변, 분야별)와 URL 쿼리 동기화
* Card List API 연동 및 에러/로딩 상태 개선(스켈레톤)
* 접근성/성능 개선(키보드 탐색, 이미지 최적화 등)
```
> 팀 협업 산출물 중 제가 담당/리드한 영역을 요약했습니다. 

🧑‍🤝‍🧑 Team

* 이서영: Tags, Header, Alert Modal, PwPopup, Modal Provider/Wrapper, useModal, AnswerContent(RQ), RHF 일부 적용, 람버트 등각 원추 투영법(useLonLatToXY.ts), Vercel 배포

* 김민희: useGeolocation 훅, Pagination(onPageChange), Modal UI/유효성검사, Tag 필터(미답변/분야별), CardList API 연동, RHF로 닉네임/비밀번호/답변 검증

* 김영은: 이모지 Reaction, Input UI, RHF 기반 Form Modal/버그 수정/서버 통신, Question Content(RQ) & Card 컴포넌트, 날짜/시간 훅(newDate.ts), Storybook UI 테스트

* 유미정: Button/Textarea/Footer/AnswerEmpty UI, 공통 레이아웃, Storybook, 닉네임 중복 검사, RHF 질문 등록 검증/제출, imgbb 업로드, Carousel, next/font/local, Axios URL 설정, 메시지 상수화, 로컬 스토리지 유저 확인, 답변 채택, 날씨 API 테마 전환

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

1. **미답변 필터링 기능** :  미답변 버튼을 체크하면 답변이 달리지 않은 질문들만 나오게 된다.
2. **분야 별로 필터링 기능** : 전체, 연예 등등 원하는 분야를 누르면 해당 분야의 질문만 나온다.
3. **페이지네이션 기능** : 다음, 이전 버튼을 누르면 다음 페이지로 넘어가고 숫자를 클릭하면 해당 페이지의 질문들이 나온다.

## Question Detail Page

https://github.com/Important-is-Great-Youths/QuickQuestion/assets/79896328/70ad46f6-2bff-49f3-b5cd-06680c48bec2

1. **이모지 리액션 기능** : 해당 질문에 대한 사람들의 느낌을 이모지의 형태로 알 수 있으며, 사용자 또한 이모지로 느낌을 남길 수 있다.
2. **질문 상세 파악** : 해당 질문의 분야, 작성자, 작성일, 내용, 첨부 이미지(선택)을 볼 수 있다.
3. **답변 파악** : 해당 질문에 몇 개의 답변이 등록되었는지, 그리고 등록된 답변의 답변자, 날짜, 답변자의 프로필 이미지, 그리고 답변 내용을 알 수 있다.
4. **답변 등록** : 질문자가 아닌 사용자는 답변하기 버튼으로 본인의 답변을 등록할 수 있다.
5. **답변 수정 및 삭제** : 답변자는 각 답변 별로 설정된 비밀번호(숫자 4자리)를 입력하여 해당 답변을 수정하거나 삭제할 수 있다. 단, 채택된 답변은 수정 및 삭제가 불가하다.
6. **답변 채택** : 질문자는 본인이 원하는 답변을 채택할 수 있다.

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

# 📁 Package Structure

```plain
quickquestion
├─ public
│  └─ assets
│     ├─ fonts
│     └─ images
└─ src
   ├─ apis
   ├─ app
   │  ├─ fonts
   │  ├─ layout.tsx
   │  ├─ providers.tsx
   │  ├─ questiondetail
   │  │  └─ [id]
   │  └─ questionlist
   ├─ components
   │  ├─ common
   │  │  ├─ AlertModal
   │  │  ├─ Button
   │  │  ├─ Card
   │  │  ├─ FormModal
   │  │  ├─ Head
   │  │  ├─ Header
   │  │  ├─ Input
   │  │  ├─ ModalWrapper
   │  │  ├─ NoAnswer
   │  │  ├─ Pagination
   │  │  ├─ PopUp
   │  │  ├─ Reaction
   │  │  ├─ Tags
   │  │  └─ Textarea
   │  ├─ home
   │  │  ├─ CurationCardList
   │  │  └─ QuestionForm
   │  └─ questionDetail
   │     ├─ AnswerEmpty
   │     ├─ AnswerContent
   │     ├─ ContentLayout
   │     ├─ QuestionContent
   │     └─ ReactionContent
   ├─ constants
   ├─ contexts
   ├─ hooks
   ├─ lib
   ├─ stories
   ├─ styles
   │  ├─ base
   │  ├─ main.scss
   │  ├─ mixins
   │  └─ variables
   ├─ types
   └─ utils
```

# 💾 Installation

1. Clone the repository

  ```bash
  git clone https://github.com/Important-is-Great-Youths/QuickQuestion.git
  ```

2. Install dependencies

  ```bash
  npm install
  ```

3. Start the development server

  ```bash
  npm run dev
  ```

4. Open the project in your browser

  ```bash
  http://localhost:3000
  ```

# 🎉 Special Thanks

로고 디자인 : [🍇](https://x.com/Q_O819)

# 📝 Attribution

* Upstream: https://github.com/Important-is-Great-Youths/QuickQuestion

* 본 개인 포크는 포트폴리오/데모 목적입니다.

