# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

풀베이스(FullBase) 야구팀의 2026 시즌 정보 웹사이트. 순수 정적 HTML/CSS로 구성되며, GitHub Pages로 호스팅된다.

- 라이브 URL: https://helloyeops.github.io/fullbase
- 레포: https://github.com/helloyeops/fullbase

## Architecture

빌드 도구 없이 단일 HTML 파일들로 구성된 정적 사이트. 각 페이지는 독립적인 `<style>` 블록을 포함한다.

- `index.html` — 메인 페이지. 퀵 스탯, 다음 경기(개막전), 3개 서브페이지 네비게이션 카드
- `schedule.html` — 시즌 경기 일정. 월별 그룹, 홈/원정/인터리그 색상 구분, 개막전 배지
- `roster.html` — 선수 명단. 스태프(단장/감독/기록/총무) + 선수 카드, 등번호, 회비 납부 표시
- `finance.html` — 회비 내역. 입출금 테이블, 요약 카드(총 입금/출금/잔액)

## Design Conventions

- 라이트 테마: 배경 `#f0f4f8`, 카드 `#ffffff`, 테두리 `#e2e8f0`
- 폰트: Noto Sans KR (Google Fonts import)
- 색상 체계: 홈 파란색(`#2563eb`), 원정 빨간색(`#dc2626`), 인터리그 골드(`#d97706`/`#f59e0b`), 총무 보라색(`#7c3aed`)
- 모든 서브페이지 상단에 🏠 홈 아이콘 링크
- 반응형: `@media (max-width: 640px)` 브레이크포인트

## Deployment

GitHub Pages (main 브랜치, root). push하면 자동 배포된다. 변경사항이 있으면 항상 즉시 배포한다.

```
git add . && git commit -m "메시지" && git push
```
