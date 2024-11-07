# learn.svelte.dev

Svelte를 사용해 앱을 만드는 방법을 처음부터 끝까지 다루는 대화형 튜토리얼입니다.

## 설정

이 저장소는 [pnpm](https://pnpm.io/)을 사용합니다.

## 앱 개발

먼저, `node scripts/create-common-bundle` 명령어를 실행하세요. 이 명령어는 SvelteKit 앱을 실행하는 데 필요한 모든 것을 패키징합니다 (Vite, esbuild, SvelteKit, Svelte 컴파일러 등). 이후 서버에서 이 패키지를 풀어서 SvelteKit 애플리케이션의 인스턴스를 생성하고 실행할 수 있습니다 (튜토리얼의 출력 창을 지원). 그다음 `dev` 명령어를 실행하세요:

```bash
node scripts/create-common-bundle
pnpm dev
```

프로덕션 빌드 및 로컬 실행:

```bash
pnpm build
pnpm preview
```

## 새로운 튜토리얼 만들기

튜토리얼은 `content` 폴더에 있습니다. 각 튜토리얼은 왼쪽에 표시되는 텍스트인 `README.md`와 초기 상태와 해결된 상태를 나타내는 `app-a` 및 `app-b` 폴더로 구성됩니다. 동일한 파일은 `app-b`에 생략할 수 있습니다. 파일이 `__delete`로 시작하면 `app-b`에서 삭제된 것으로 표시됩니다. 폴더 내에 `__delete`라는 파일이 있으면 해당 폴더는 `app-b`에서 삭제된 것으로 간주됩니다.

## 튜토리얼 종속성 업데이트

종속성(예: Svelte)을 업데이트하려면 루트와 `content/common`의 `package.json`에서 해당 종속성을 변경하세요. 루트에서는 `pnpm i`를 실행하여 (`pnpm-lock.yaml` 업데이트), `content/common`에서는 `npm i`를 실행하여 (`package-lock.json` 업데이트) 종속성을 반영합니다.

