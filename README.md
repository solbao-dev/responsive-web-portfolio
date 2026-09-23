# Responsive Web Portfolio

> A responsive portfolio built from scratch with Vanilla HTML, CSS, and JavaScript.  
> 프레임워크 없이 Vanilla HTML·CSS·JavaScript로 직접 구현한 반응형 웹 포트폴리오입니다.

**CODYSSEY · Tool Learning | AI 도구 학습**  
`HTML5` `CSS3` `JavaScript` `GitHub API` `Responsive Web` `GitHub Pages`

## Overview | 프로젝트 소개

The goal was to understand the browser interaction cycle — **user event → state change → DOM update** — without React, Vue, jQuery, Bootstrap, or other UI frameworks.

React 같은 프레임워크를 사용하기 전에 브라우저의 기본 동작인 **사용자 이벤트 → 상태 변경 → DOM 업데이트**를 직접 구현하며 프론트엔드의 기초 원리를 이해하는 것을 목표로 했습니다.

반응형 레이아웃, 다크모드 상태 유지, GitHub API 연동, 폼 검증, 프로젝트 필터링과 다양한 UI 상태를 브라우저 기본 기술만으로 구현했습니다.

## Core Features | 주요 기능

- Mobile-first responsive layout | 모바일 퍼스트 반응형 레이아웃
- Dark mode + `localStorage` persistence | 다크모드 설정 저장·복원
- Responsive navigation & hamburger menu | 반응형 내비게이션
- Intersection Observer animations | 스크롤 등장 애니메이션
- Contact-form validation | 폼 유효성 검사와 필드별 오류 표시
- GitHub REST API with `fetch` / `async-await` | GitHub 저장소 API 연동
- Loading / success / error / empty states | 로딩·성공·오류·빈 상태 UI 분리
- Repository filtering | 언어별 프로젝트 필터링
- Hero typing effect | 타이핑 효과

## Tech Stack | 기술

| Area | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | CSS3, Flexbox, Grid, Custom Properties |
| Script | Vanilla JavaScript ES6+ |
| Browser APIs | Fetch API, Intersection Observer, localStorage |
| Integration | GitHub REST API |
| Deployment | GitHub Pages |

## State → Rendering | 상태와 렌더링

| Event | State change | UI result |
|---|---|---|
| Theme toggle | `data-theme` + localStorage | 전체 테마 변경 |
| GitHub API request | loading → success/error/empty | Projects 영역 상태 변경 |
| Form input | validation state | 필드별 오류 피드백 |
| Language filter | `activeLang` | 프로젝트 카드 재렌더링 |

## Structure | 구조

```text
responsive-web-portfolio/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
└── README.md
```

## Run Locally | 로컬 실행

```bash
git clone https://github.com/solbao-dev/responsive-web-portfolio.git
cd responsive-web-portfolio
```

VS Code에서 프로젝트를 열고 Live Server로 `index.html`을 실행합니다. GitHub 사용자명은 `js/main.js`의 `CONFIG.githubUsername`에서 설정할 수 있습니다.

## Live Demo | 배포

https://solbao-dev.github.io/responsive-web-portfolio/

## Screenshots | 실행 화면

| Desktop | Mobile | Dark Mode |
|---|---|---|
| ![Desktop](images/desktop.png) | ![Mobile](images/mobile.png) | ![Dark Mode](images/darkmode.png) |

## Known Limitations | 현재 한계

- Unauthenticated GitHub API requests are rate-limited. | 인증 없는 GitHub API 요청은 호출 제한이 있습니다.
- The contact form validates input but does not send email to a backend. | Contact 폼은 입력 검증까지 구현되어 있으며 실제 이메일 전송 백엔드는 연결하지 않았습니다.

## What I Learned | 배운 점

Building without a framework made the abstractions behind modern frontend tools visible: DOM updates, UI state, browser APIs, persistence, responsive layout, and error handling.

프레임워크 없이 직접 구현하면서 현대 프론트엔드 프레임워크가 대신 처리해주는 **DOM 업데이트, 상태 관리, 브라우저 API, 데이터 유지, 반응형 레이아웃과 오류 상태 처리**를 기초부터 이해할 수 있었습니다. 성공 화면뿐 아니라 로딩·빈 상태·실패 상황까지 사용자 경험의 일부로 설계해야 한다는 점도 배웠습니다.

---

Part of my **CODYSSEY Tool Learning | 코디세이 AI 도구 학습** journey.