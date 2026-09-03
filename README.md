<div align="center">

# 🎮 Game Programmer

**Unity · C# · Multiplayer · Problem Solving**

기존 시스템이 왜 그렇게 동작하는지 이해하고,  
그 위에 플레이어가 새롭다고 느낄 변화를 만드는 프로그래머를 지향합니다.

[![Blog](https://img.shields.io/badge/Development_Blog-181717?style=flat-square&logo=github&logoColor=white)](https://bbie-6772.github.io/)
[![Email](https://img.shields.io/badge/Email-qldpdml12%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:qldpdml12@gmail.com)

</div>

---

# ⭐ Featured Projects

## 🟢 2d-survivor
**Unity 6 · C# · Personal Project**

직접 기획하고 게임플레이 코드를 작성하며 Unity 클라이언트의 입력·물리·전투 구조를 학습하고 있습니다.

- 이동·조준·대시·적 스폰·추적·근접 전투 구현
- 필요한 기능을 단순하게 먼저 구현하고 실제 동작에서 드러난 문제를 기준으로 구조 개선
- 구현 대안·선택 이유·감수한 비용·재검토 조건을 `docs/decisions`에 기록
- 현재 전투 이후 경험치와 성장 요소를 추가해 코어 루프를 확장 중

[![Repository](https://img.shields.io/badge/Repository-2d--survivor-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/2d-survivor)
[![Source](https://img.shields.io/badge/View-C%23_Scripts-512BD4?style=flat-square&logo=dotnet&logoColor=white)](https://github.com/bbie-6772/2d-survivor/tree/main/Assets/_Project/Scripts)
[![Decisions](https://img.shields.io/badge/View-Design_Decisions-0969DA?style=flat-square&logo=markdown&logoColor=white)](https://github.com/bbie-6772/2d-survivor/tree/main/docs/decisions)

---

## 🦆 DUCKTOPIA
**Node.js · TCP · Protobuf · Redis · Docker · AWS**

2~8인이 협력하는 생존 게임의 8인 팀 프로젝트에서 서버 개발을 담당했습니다.

- 단일 서버를 `Gateway / Lobby / Game`으로 분리하고 Redis 기반 연결 구조 구현
- Unity 클라이언트 담당자와 FSM·좌표 처리 흐름을 추적해 클라이언트-서버 동기화 문제 해결
- 조건을 바꿔가며 부하 테스트를 반복해 Game Server 한 대당 평균 약 **1,850 sessions** 확인
- 🏆 팀 프로젝트 최우수상

[![Repository](https://img.shields.io/badge/Repository-DUCKTOPIA-181717?style=flat-square&logo=github)](https://github.com/kms5064/DUCKTOPIA)

---

## 🧪 AI Development Pipeline × Slime Ranch
**Python · Unity MCP · RAG · Unity 6**

AI Agent에 구현과 디버깅을 맡기고, 사람이 게임 규칙과 완료 조건을 결정하고 결과를 검증하는 개발 방식을 실험했습니다.

- Agent별 참조 범위를 조정해 작업 카드당 Context 사용량을 약 **30K → 9K**로 감소
- 일정 확률의 돌연변이와 오염도에 따라 확률이 증가하는 게임 규칙 기획
- AI 생성 캐릭터·타일셋 결과물 선정 및 타일셋 적용 관리
- 직접 플레이 후 슬라임 스탯·돌연변이 확률을 플레이어에게 보여주는 UX 개선 제안

[![Play](https://img.shields.io/badge/▶_Play-Slime_Ranch-4CAF50?style=for-the-badge)](https://juglegame.github.io/Slime/)
[![Game](https://img.shields.io/badge/Repository-Slime_Ranch-181717?style=flat-square&logo=github)](https://github.com/JugleGame/Slime)
[![Pipeline](https://img.shields.io/badge/Repository-Game_Develop_Orchestration-412991?style=flat-square&logo=github)](https://github.com/JugleGame/Game-Develop-Orchestration)

---

<details>
<summary><b>🌐 Earlier Multiplayer Projects</b></summary>
<br>

### TCP Multiplayer Game Server
**Node.js · TCP · Protobuf**

위치 검증과 추측항법이 같은 상태를 수정하던 문제에서 상태 변경 책임을 분리하고, 위치 오차 허용치를 **10% → 5%**로 좁혀도 동기화가 유지되는 것을 확인했습니다.

[![Repository](https://img.shields.io/badge/Repository-TCP_Multiplayer-181717?style=flat-square&logo=github)](https://github.com/bbie-6772/TCP-Multi-Playgame)

### Multi Tower Defense Server
**Node.js · TCP · Protobuf**

Unity 클라이언트를 분석해 서버 로직을 구현하고, 비동기 로그인 경쟁 문제를 재현·수정한 뒤 서버와 수정된 클라이언트를 연동한 데모를 발표했습니다.

[![Server](https://img.shields.io/badge/Repository-Multi_Tower_Defense-181717?style=flat-square&logo=github)](https://github.com/nanoda1802/multi-tower-defense-server)
[![Retrospective](https://img.shields.io/badge/Project-Retrospective-0A66C2?style=flat-square&logo=githubpages)](https://bbie-6772.github.io/multi-towerdefense-project/2025/02/03/multiplay.html)

</details>

---

# 🧰 Stack

**Game** · `Unity` `C#` `Physics2D`  
**Multiplayer / Server** · `Node.js` `TCP` `Protobuf` `Redis` `Docker` `AWS`  
**AI / Tooling** · `Python` `RAG` `MCP` `PostgreSQL`  
**Currently Learning** · `C++17` `Algorithm Problem Solving`

---

# 📚 Development Notes

구현 과정에서 발견한 문제와 설계 판단, 실패한 접근과 다시 판단할 조건을 기록하고 있습니다.

[![Development Blog](https://img.shields.io/badge/Read-Development_Blog-0A66C2?style=for-the-badge&logo=githubpages&logoColor=white)](https://bbie-6772.github.io/)

<div align="center">

**Understand → Build → Validate → Improve**

</div>
