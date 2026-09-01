<div align="center">

# 🎮 Game Client Developer

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1200&center=true&vCenter=true&width=700&lines=Building+gameplay+with+Unity+%26+C%23;Writing+the+client+code+myself;Understand+before+automating)](https://git.io/typing-svg)

**Unity · C# · Gameplay · Problem Solving**

[![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)](https://unity.com/)
[![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://learn.microsoft.com/dotnet/csharp/)
[![Game Client](https://img.shields.io/badge/Focus-Game_Client-2EA44F?style=for-the-badge&logo=gamejolt&logoColor=white)](https://github.com/bbie-6772/2d-survivor)
[![WebGL](https://img.shields.io/badge/Target-WebGL-F16529?style=for-the-badge&logo=webgl&logoColor=white)](https://github.com/bbie-6772/2d-survivor)

[![Blog](https://img.shields.io/badge/Development_Blog-181717?style=flat-square&logo=github&logoColor=white)](https://bbie-6772.github.io/)
[![Email](https://img.shields.io/badge/Email-qldpdml12%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:qldpdml12@gmail.com)

</div>

---

## 👋 About Me

**게임이 왜 그렇게 동작하는지 이해하고, 반복되는 문제를 코드와 도구로 줄이는 개발을 좋아합니다.**

자동화와 게임 서버 개발을 통해 구조와 데이터 흐름을 다뤄왔고, 이후 Unity 클라이언트까지 범위를 넓혀 입력과 상태, 상호작용이 실제 플레이 경험으로 이어지는 과정을 직접 구현하고 있습니다.

특정 기술 하나에만 머무르기보다 **게임 클라이언트를 중심으로 서버와 개발 도구까지 연결해 이해하는 것**, 그리고 시행착오와 설계 판단을 문서로 남기는 것을 중요하게 생각합니다.

---

# 🎯 Game Client — Primary Focus

## 🟢 2d-survivor — Unity · C# · 직접 작성 중 "In Progress"

웨이브 서바이버를 만들며 Unity 클라이언트 코드를 직접 작성하고 있습니다.
필요한 기능을 가장 단순한 형태로 먼저 만들고, 실제로 동작시키며 드러나는 문제를 기준으로 구조를 고쳐나가고 있습니다.

- "PlayerMovement" / "PlayerAim" - Update와 FixedUpdate의 주기 차이로 순간 입력이 사라지는 문제를 확인하고, 입력을 읽는 책임과 물리를 적용하는 책임을 분리
- "Health" / "IDamageable" - 공격하는 쪽이 대상 타입을 몰라도 데미지를 전달하도록 분리
- "EnemySpawner" / "SpawnerBase" - 적 생성을 확장하며 abstract와 virtual, Unity 생명주기, 초기화 책임을 어떤 기준으로 나눌지 비교한 뒤 현재 규모에서 가장 단순한 쪽을 선택
- "EnemyChase" - 적이 플레이어를 추적하는 이동 처리
- "MeleeWeapon" - 근접 공격과 피격 판정
- "CameraFollow" / "DamageFlash" - 카메라 추적과 피격 피드백

현재 플레이어 이동과 공격, 화면 밖에서의 적 생성과 플레이어 추적, 피해 처리와 처치까지 동작하며 경험치와 성장 요소를 붙여 코어 루프를 완성하는 단계입니다.
적의 생성과 소멸을 매번 인스턴스화·파괴로 처리하고 있어 오브젝트 풀링 적용을 다음 과제로 두고 있습니다.

구현 과정에서 어떤 선택지를 비교했고 왜 그 방향을 골랐는지는 "docs/decisions"에 기록하고 있습니다.

[![Repository](https://img.shields.io/badge/Repository-2d--survivor-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/2d-survivor)
[![Source](https://img.shields.io/badge/View-C%23_Scripts-512BD4?style=flat-square&logo=dotnet&logoColor=white)](https://github.com/bbie-6772/2d-survivor/tree/main/Assets/_Project/Scripts)
[![Decisions](https://img.shields.io/badge/View-Design_Decisions-0969DA?style=flat-square&logo=markdown&logoColor=white)](https://github.com/bbie-6772/2d-survivor/tree/main/docs/decisions)


---

# 🌐 Server Background — Secondary Strength

서버 경험은 **게임 클라이언트를 더 넓게 이해하기 위한 배경 역량**으로 가져가고 있습니다.

<details>
<summary><b>멀티플레이 서버 경험 보기</b> — DUCKTOPIA · TCP Multiplayer</summary>
<br>

### 🦆 DUCKTOPIA

> **Node.js · TCP · Protobuf · Redis · Docker · AWS**

2~8인이 협력하는 생존 게임의 멀티플레이 서버를 개발했습니다. 다른 팀원 한 명과 역할별 서버 분리 구조를 설계하고 구현을 맡아 Gateway, Lobby, Game Server로 책임을 나눴습니다.

부하 테스트를 점진 증가 방식으로 다시 설계해 게임 수가 "99"에서 멈추는 현상을 발견했고, Redis 값이 문자열 기준으로 비교되던 문제를 수정했습니다. 이후 다시 측정해 **Game Server 한 대당 약 1,850 game sessions**이라는 기준을 얻었습니다.

**283 commits — 팀 내 최다 기여**

[![Repository](https://img.shields.io/badge/Repository-DUCKTOPIA-181717?style=flat-square&logo=github)](https://github.com/kms5064/DUCKTOPIA)
[![My Commits](https://img.shields.io/badge/My_Commits-283-2EA44F?style=flat-square&logo=github)](https://github.com/kms5064/DUCKTOPIA/commits?author=bbie-6772)

### 🌐 TCP Multiplayer Game Server

> **Node.js · TCP · Protobuf**

여러 명이 같은 공간에서 움직이는 멀티플레이 게임 서버를 직접 구현했습니다.

위치 검증과 추측항법이 같은 상태를 수정하면서 서로의 결과를 덮어쓰는 문제를 발견했습니다. 검증만 실제 위치를 확정하도록 하고 추측항법은 예측만 수행하도록 책임을 분리해, 오차 허용치를 **10%에서 5%**로 좁혀도 동기화가 흔들리지 않는 것을 확인했습니다.

이 프로젝트에서 Unity 클라이언트를 처음 분석하며 **클라이언트에서 일어나는 일을 이해해야 서버도 제대로 설계할 수 있다**는 것을 체감했고, 이후 게임 클라이언트 개발로 관심 범위를 넓혔습니다.

[![Repository](https://img.shields.io/badge/Repository-TCP--Multi--Playgame-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/TCP-Multi-Playgame)

</details>

---

# 🛠 AI & Developer Tooling

<details>
<summary><b>AI Game Development Experiments</b> — Orchestration · RAG · 검증 중심 활용</summary>
<br>

AI에게 게임 개발을 어디까지 맡길 수 있는지 확인하기 위해 개발 작업을 단계별로 나누는 Orchestration 구조와 게임 설계 지식을 검색하는 RAG 도구를 실험했습니다.

두 차례의 Unity 게임 제작 실험에서는 **게임 코드를 직접 작성하지 않고**, 어떤 명세를 어떤 범위로 구현할지 정한 뒤 생성된 결과를 검증하고 문제의 원인을 찾아 수정 방향을 요청하는 역할을 맡았습니다.

그 과정에서 코드를 직접 써보지 않으면 만들어진 구조를 충분히 이해하기 어렵고, 결국 수정 요청의 품질도 떨어진다는 한계를 경험했습니다. 그래서 현재 "2d-survivor"에서는 AI를 구현자보다 **학습과 검토를 돕는 도구**로 사용하고 코드는 직접 작성하고 있습니다.

[![Orchestration](https://img.shields.io/badge/Game_Develop-Orchestration-412991?style=flat-square&logo=github)](https://github.com/JugleGame/Game-Develop-Orchestration)
[![RAG](https://img.shields.io/badge/Game_Planning-RAG-412991?style=flat-square&logo=github)](https://github.com/JugleGame/Game-Planning-RAG)

**프로젝트 결과물** — [다음에 (플레이)](https://juglegame.github.io/project-daeum/) · 코드는 AI가 작성했으며, 명세 결정과 검증을 담당했습니다.

</details>

---

# 🧰 Tech Stack

### 🎮 Game Client — Primary

[![Unity, CSharp](https://skillicons.dev/icons?i=unity,cs&theme=dark)](https://skillicons.dev)

"Unity" · "C#" · "Input System" · "2D Physics" · "WebGL"

### 🌐 Server / Infrastructure — Secondary

[![NodeJS, Redis, Docker, AWS, PostgreSQL](https://skillicons.dev/icons?i=nodejs,redis,docker,aws,postgres&theme=dark)](https://skillicons.dev)

"TCP" · "Protobuf" · "Redis" · "Docker" · "AWS"

### 📖 Currently Learning

[![CPP, Python](https://skillicons.dev/icons?i=cpp,python&theme=dark)](https://skillicons.dev)

---

# 📊 GitHub Activity

<div align="center">

[![GitHub Profile Summary](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=bbie-6772&theme=github_dark)](https://github.com/bbie-6772)

<img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=bbie-6772&theme=github_dark" height="165" alt="GitHub stats" />
<img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=bbie-6772&theme=github_dark&utcOffset=9" height="165" alt="GitHub productive time" />

</div>

---

# 📚 Development Notes

프로젝트를 진행하면서 겪은 문제와 해결 과정, 게임 클라이언트 구현, 네트워크와 AI 활용 실험, 학습 내용을 기록하고 있습니다.

[![Development Blog](https://img.shields.io/badge/Read-Development_Blog-0A66C2?style=for-the-badge&logo=githubpages&logoColor=white)](https://bbie-6772.github.io/)

<div align="center">

**Build → Break → Understand → Build Again**

</div>
