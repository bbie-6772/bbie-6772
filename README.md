<div align="center">

# 🎮 Game Client Developer

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1200&center=true&vCenter=true&width=700&lines=Building+gameplay+with+Unity+%26+C%23;Learning+the+client+through+server+experience;Understand+before+automating)](https://git.io/typing-svg)

**Gameplay · Multiplayer · Problem Solving**

[![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)](https://unity.com/)
[![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://learn.microsoft.com/dotnet/csharp/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Redis](https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white)](https://redis.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)](https://aws.amazon.com/)

[![Blog](https://img.shields.io/badge/Development_Blog-181717?style=flat-square&logo=github&logoColor=white)](https://bbie-6772.github.io/)
[![Email](https://img.shields.io/badge/Email-qldpdml12%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:qldpdml12@gmail.com)

</div>

---

## 👋 About Me

게임의 한쪽만 아는 개발자가 되지 않기 위해 **서버에서 시작해 클라이언트까지 범위를 넓혀가고 있습니다.**

Node.js 기반 멀티플레이 게임 서버를 개발하면서 클라이언트에서 일어나는 일을 알아야 서버 로직도 제대로 설계할 수 있다는 것을 경험했습니다. 현재는 **Unity와 C#으로 게임 플레이 코드를 직접 작성하며** 게임 클라이언트 구조를 공부하고 있습니다.

문제를 만났을 때 바로 기능을 덧붙이기보다 **재현 → 원인 범위 축소 → 수정 → 재검증**의 과정을 중요하게 생각합니다.

---

# 🎮 Featured Projects

## 🟢 [2d-survivor](https://github.com/bbie-6772/2d-survivor) `In Progress`

> **Unity · C# · Game Client**

Unity 클라이언트 코드를 직접 작성하며 웨이브 서바이버의 핵심 게임 플레이를 구현하고 있습니다.

- `PlayerMovement` / `PlayerAim` — 플레이어 이동과 조준
- `EnemySpawner` / `EnemyChase` — 적 생성과 추적
- `MeleeWeapon` — 근접 공격과 Hit Detection
- `Health` / `IDamageable` — 피해 처리 책임 분리
- 구현 과정의 선택과 이유를 `docs/decisions`에 기록

[![Repository](https://img.shields.io/badge/Repository-2d--survivor-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/2d-survivor)

---

## 🦆 [DUCKTOPIA](https://github.com/kms5064/DUCKTOPIA)

> **Node.js · TCP · Protobuf · Redis · Docker · AWS**

2~8인이 협력해 거점을 지키고 최종 보스를 처치하는 협동 생존 게임의 멀티플레이 서버를 개발했습니다.

**283 commits — 팀 내 최다 기여**

다른 팀원 한 명과 역할별 서버 분리 구조를 설계하고 구현을 맡아 Gateway, Lobby, Game Server로 책임을 나눴습니다. Redis를 이용해 서버 상태를 공유하고 Health Check와 진행 중인 게임 수 기반 접속 분배 구조를 구성했습니다.

부하 테스트에서는 더미 클라이언트를 점진적으로 늘리는 방식으로 테스트를 다시 설계했고, 게임 수가 `99`에서 더 이상 분배되지 않는 현상을 발견했습니다. Redis 값이 문자열 기준으로 비교되던 문제를 수정한 뒤 다시 측정해 **Game Server 한 대당 약 1,850 game sessions**이라는 기준을 얻었습니다.

[![Repository](https://img.shields.io/badge/Repository-DUCKTOPIA-181717?style=flat-square&logo=github)](https://github.com/kms5064/DUCKTOPIA)
[![My Commits](https://img.shields.io/badge/My_Commits-283-2EA44F?style=flat-square&logo=github)](https://github.com/kms5064/DUCKTOPIA/commits?author=bbie-6772)

---

## 🌐 [TCP Multiplayer Game Server](https://github.com/bbie-6772/TCP-Multi-Playgame)

> **Node.js · TCP · Protobuf**

여러 명이 같은 공간에서 움직이는 멀티플레이 게임 서버를 직접 구현했습니다.

서버의 위치 검증과 추측항법이 같은 상태를 수정하면서 서로의 결과를 덮어쓰는 문제를 발견했습니다. 검증 로직만 실제 위치를 확정하도록 하고 추측항법은 예측만 수행하도록 책임을 분리해, 오차 허용치를 **10%에서 5%**로 좁혀도 동기화가 흔들리지 않는 것을 확인했습니다.

이 프로젝트에서 Unity 클라이언트를 처음 분석하며 **클라이언트에서 일어나는 일을 이해해야 서버도 제대로 설계할 수 있다**는 것을 체감했고, 이후 게임 클라이언트 개발로 관심 범위를 넓히게 되었습니다.

[![Repository](https://img.shields.io/badge/Repository-TCP--Multi--Playgame-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/TCP-Multi-Playgame)

---

# 🛠 AI & Developer Tooling

AI에게 게임 개발을 어디까지 맡길 수 있는지 확인하기 위해 개발 작업을 단계별로 나누는 Orchestration 구조와 게임 설계 지식을 검색하는 RAG 도구를 실험했습니다.

두 차례의 Unity 게임 제작 실험에서는 **게임 코드를 직접 작성하지 않고**, 어떤 명세를 어떤 범위로 구현할지 정한 뒤 생성된 결과를 검증하고 문제의 원인을 찾아 수정 방향을 요청하는 역할을 맡았습니다.

그 과정에서 코드를 직접 써보지 않으면 만들어진 구조를 충분히 이해하기 어렵고, 결국 수정 요청의 품질도 떨어진다는 한계를 경험했습니다. 그래서 현재 `2d-survivor`에서는 AI를 구현자보다 **학습과 검토를 돕는 도구**로 사용하고 코드는 직접 작성하고 있습니다.

[![Orchestration](https://img.shields.io/badge/Game_Develop-Orchestration-412991?style=flat-square&logo=github)](https://github.com/JugleGame/Game-Develop-Orchestration)
[![RAG](https://img.shields.io/badge/Game_Planning-RAG-412991?style=flat-square&logo=github)](https://github.com/JugleGame/Game-Planning-RAG)

---

# 🧰 Tech Stack

### Game Client

[![Unity, CSharp](https://skillicons.dev/icons?i=unity,cs&theme=dark)](https://skillicons.dev)

### Multiplayer / Backend

[![NodeJS, Redis, Docker, AWS, PostgreSQL](https://skillicons.dev/icons?i=nodejs,redis,docker,aws,postgres&theme=dark)](https://skillicons.dev)

### Currently Learning

[![CPP, Python](https://skillicons.dev/icons?i=cpp,python&theme=dark)](https://skillicons.dev)

---

# 📊 GitHub Activity

<div align="center">

[![GitHub Profile Summary](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=bbie-6772&theme=github_dark)](https://github.com/bbie-6772)

[![GitHub Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=bbie-6772&theme=github-compact&hide_border=true)](https://github.com/Ashutosh00710/github-readme-activity-graph)

</div>

---

# 📚 Development Notes

프로젝트를 진행하면서 겪은 문제와 해결 과정, 게임 개발과 AI 활용 실험, 학습 내용을 기록하고 있습니다.

[![Development Blog](https://img.shields.io/badge/Read-Development_Blog-0A66C2?style=for-the-badge&logo=githubpages&logoColor=white)](https://bbie-6772.github.io/)

<div align="center">

**Build → Break → Understand → Build Again**

</div>
