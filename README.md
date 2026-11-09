# Issue Tracker Standalone

[English below](#english)

**이슈트래커 데이터를 이 컴퓨터에만 저장합니다.** 이슈·문서·첨부파일은 내 컴퓨터 안에만 있고 외부 서버로 올라가지 않습니다. AI 에이전트를 빼면 인터넷에 연결되어 있지 않아도 모두 쓸 수 있습니다.

이슈트래커 데스크톱의 추가기능입니다. 서버를 따로 두지 않고, 가입이나 로그인 화면 없이 혼자 씁니다.

## 설치

1. 이슈트래커 데스크톱을 설치합니다.
2. 앱의 서버 선택 화면에서 **단독버전 설치**를 누르면 단독버전 탭이 열립니다.
3. **최신 버전 받기**를 누릅니다.
4. 이름과 조직 이름을 입력하고 **시작**을 누르면 서버 목록에 **내 컴퓨터** 항목이 생깁니다.

패키지는 앱이 이 저장소의 최신 릴리스에서 받아 서명을 확인한 뒤 설치합니다. 이 저장소의 파일을 직접 내려받을 필요는 없습니다.

## 데이터

- 데이터는 앱 데이터 폴더 아래 `standalone/` 에 저장됩니다. macOS 는 `~/Library/Application Support/kr.typostudio.issue-tracker/standalone/` 입니다.
- 서버는 `127.0.0.1` 에서만 열리며 다른 컴퓨터에서 접속할 수 없습니다.
- 단독버전 페이지에서 패키지만 지우거나(데이터는 남고, 다시 설치하면 이어서 씁니다) 데이터만 지워 초기화할 수 있습니다. 백업은 이 폴더를 복사하면 됩니다(앱을 끈 상태에서).

### 인터넷을 쓰는 경우

이슈트래커 데이터는 아래 어느 경우에도 앱이 외부 서버로 저장하지 않습니다. 글꼴을 포함해 화면에 필요한 파일은 패키지에 들어 있습니다.

- **AI 에이전트**를 실행하면, 작업에 필요한 내용이 사용자가 고른 AI 서비스로 전달됩니다. 에이전트를 쓰지 않으면 전달되지 않습니다.
- 앱과 추가기능의 **업데이트 확인**. 연결되어 있지 않으면 조용히 건너뜁니다.

그 밖에 공휴일 가져오기나 사용자가 직접 등록한 웹훅처럼, 사용자가 실행하거나 설정한 기능은 그 대상에 연결합니다.

## 지원 환경

macOS (Apple Silicon), Windows (x64, ARM 은 에뮬레이션으로 실행).

## 포함된 소프트웨어

Node.js, PostgreSQL(embedded-postgres) 과 npm 패키지가 함께 배포되며, 각각의 라이선스는 패키지 안의 `node/LICENSE`, `server/node_modules/@embedded-postgres/*/LICENSE.md`, 각 모듈의 라이선스 파일을 따릅니다. 글꼴 Pretendard, Outfit, JetBrains Mono 는 SIL Open Font License 1.1 이며 라이선스 전문은 `web/fonts/licenses/` 에 있습니다. 이슈트래커 자체의 라이선스는 `LICENSE`(PolyForm Internal Use 1.0.0)입니다.

---

<a id="english"></a>

# English

**Your issue tracker data is stored only on this computer.** Issues, documents and attachments stay on your machine and are not uploaded to any server. Apart from AI agents, everything works without an internet connection.

An add-on for Issue Tracker Desktop, for using it on your own with no server, sign-up or login screen.

## Install

1. Install Issue Tracker Desktop.
2. On the server picker, click **Install Standalone**. The Standalone tab opens.
3. Click **Get the latest version**.
4. Enter your name and organization name, then click **Start**. A **My Computer** entry appears in the server list.

The app downloads the package from the latest release here and verifies its signature. You don't need to download these files yourself.

## Your data

- Stored under `standalone/` in the app's data folder. On macOS: `~/Library/Application Support/kr.typostudio.issue-tracker/standalone/`.
- The server listens on `127.0.0.1` only and can't be reached from other computers.
- On the Standalone page you can delete just the package (the data stays and comes back when you reinstall) or delete just the data to reset. To back up, copy this folder while the app is closed.

### When the internet is used

The app never stores your issue tracker data on an outside server. Everything the screen needs, fonts included, ships in the package.

- **AI agents**: when you run one, what it needs for the task is sent to the AI service you chose. Nothing is sent if you don't use agents.
- **Update checks** for the app and this add-on. With no connection they are quietly skipped.

Beyond these, features you run or configure yourself, such as importing public holidays or a webhook you register, connect to their own targets.

## Platforms

macOS (Apple Silicon) and Windows (x64; ARM runs it under emulation).

## Included software

Node.js, PostgreSQL (embedded-postgres) and npm packages ship with this add-on under their own licenses: `node/LICENSE`, `server/node_modules/@embedded-postgres/*/LICENSE.md`, and each module's license file. The Pretendard, Outfit and JetBrains Mono fonts are under the SIL Open Font License 1.1, with the full text in `web/fonts/licenses/`. Issue Tracker itself is under `LICENSE` (PolyForm Internal Use 1.0.0).
