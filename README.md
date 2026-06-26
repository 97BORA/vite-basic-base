# vite-basic-base / 20260627

Vite + React + TypeScript 기본 프로젝트에서 불필요한 예제 코드와 기본 assets를 정리한 베이스 프로젝트입니다.

학습용으로 만든 프로젝트이며, 새 React TypeScript 프로젝트를 시작할 때 바로 사용할 수 있는 최소 기본 상태를 목표로 합니다.

## Tech Stack

- Vite
- React
- TypeScript
- Tailwind CSS v4
- ESLint
- Prettier
- Vitest
- Testing Library
- Husky
- lint-staged
- GitHub Actions
- Node.js 22

## What was cleaned up

- Vite 기본 예제 UI 정리
- 불필요한 CSS 정리
- 사용하지 않는 이미지 assets 제거
- public 기본 아이콘 제거
- `App.tsx`를 최소 구조로 정리
- `main.tsx` import 구조 정리
- `index.css`는 Tailwind CSS import만 유지

## Project Setup

### Node.js version

이 프로젝트는 Node.js 22 기준으로 사용합니다.

명령어: `nvm use`

`.nvmrc` 파일에 Node.js 버전이 지정되어 있습니다.

`.nvmrc` 내용: `22`

## Install

명령어: `npm install`

CI / 협업 환경에서는 아래 명령어를 사용할 수 있습니다.

명령어: `npm ci`

## Development

명령어: `npm run dev`

## Build

명령어: `npm run build`

## Preview

명령어: `npm run preview`

## Check

전체 검사를 실행합니다.

명령어: `npm run check`

위 명령어는 아래 작업을 순서대로 실행합니다.

1. `npm run typecheck`
2. `npm run lint`
3. `npm run test:run`
4. `npm run format:check`

## Scripts

| Command                 | Description                        |
| ----------------------- | ---------------------------------- |
| `npm run dev`           | 개발 서버 실행                     |
| `npm run build`         | TypeScript 검사 후 프로덕션 빌드   |
| `npm run preview`       | 빌드 결과 미리보기                 |
| `npm run lint`          | ESLint 검사                        |
| `npm run format`        | Prettier로 코드 포맷               |
| `npm run format:check`  | Prettier 포맷 확인                 |
| `npm run typecheck`     | TypeScript 타입 검사               |
| `npm run test`          | Vitest watch 모드 실행             |
| `npm run test:run`      | Vitest 테스트 1회 실행             |
| `npm run test:ui`       | Vitest UI 실행                     |
| `npm run test:coverage` | 테스트 커버리지 확인               |
| `npm run check`         | 타입 검사, 린트, 테스트, 포맷 확인 |

## Git Hook

커밋 전에 Husky와 lint-staged가 실행됩니다.

`.husky/pre-commit` 내용: `npx lint-staged`

lint-staged는 staged 파일에 대해 ESLint와 Prettier를 실행합니다.

## Folder Structure

- `vite-basic-base/`

    - `.github/`
    - `.husky/`
    - `.vscode/`
    - `public/`
    - `src/`
    - `.editorconfig`
    - `.env.example`
    - `.gitignore`
    - `.nvmrc`
    - `.prettierignore`
    - `.prettierrc`
    - `eslint.config.js`
    - `index.html`
    - `package.json`
    - `tsconfig.json`
    - `tsconfig.app.json`
    - `tsconfig.node.json`
    - `vite.config.ts`
    - `vitest.config.ts`

## Notes

- `node_modules/`는 Git에 올리지 않습니다.
- `dist/`는 `npm run build`로 생성되는 빌드 결과물이므로 Git에 올리지 않습니다.
- 프로젝트를 받은 뒤에는 `npm install` 또는 `npm ci`를 실행합니다.
- 개발 서버는 `npm run dev`로 실행합니다.
