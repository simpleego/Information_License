#  SQL TCL 명령어(Commit, Rollback, Savepoint)

<img width="735" height="380" alt="image" src="https://github.com/user-attachments/assets/f5b5e45b-e5ed-48ba-83f9-41f99cf73038" />

<img width="381" height="452" alt="image" src="https://github.com/user-attachments/assets/1768c5e7-f22e-4c6b-a0dc-61618dbdcd98" />

## 시나리오 기반 설명
- **commit / savepoint / rollback**

---

# 🎬 시나리오: “게임에서 캐릭터 꾸미기”

jong이 RPG 게임에서 캐릭터를 꾸미고 있다고 상상해보자.

- 옷 바꾸고  
- 무기 바꾸고  
- 머리 스타일 바꾸고  
- 능력치 찍고  

이런 걸 막 하고 있는 상황이야.

---

# 🟢 1. **SAVEPOINT = 중간 저장**

게임에서 “중간 저장” 버튼을 눌러서  
**지금 상태를 잠깐 저장해두는 것**과 같아.

예시:

> “지금 캐릭터 머리 스타일이 마음에 드네.  
> 혹시 나중에 망치면 여기로 돌아오자.”  
> → **SAVEPOINT 생성**

즉,  
**큰 저장(commit) 말고, 잠깐 체크포인트를 찍어두는 것**이 savepoint야.

---

# 🔵 2. **COMMIT = 최종 저장**

게임에서 “전체 저장”을 눌러서  
**지금까지 한 모든 변경을 완전히 확정하는 것**이 commit이야.

예시:

> “오케이, 지금 캐릭터 완전 마음에 들어.  
> 이 상태로 게임 계속 진행하자!”  
> → **COMMIT**

commit을 하면  
이전 savepoint는 더 이상 필요 없고,  
지금 상태가 공식 저장본이 되는 거지.

---

# 🔴 3. **ROLLBACK = 되돌리기**

게임에서 “되돌리기”를 눌러서  
**저장해둔 시점으로 돌아가는 것**이 rollback이야.

예시:

> “헉… 갑옷 바꿨더니 너무 이상해졌네.  
> 아까 저장해둔 상태로 돌아가자.”  
> → **ROLLBACK TO SAVEPOINT**

또는

> “아예 오늘 한 모든 변경을 취소하고 싶다.”  
> → **ROLLBACK (전체 되돌리기)**

---

# 🎯 한 줄 요약

| 명령어 | 일상적 의미 | 시나리오 예시 |
|--------|-------------|----------------|
| **SAVEPOINT** | 중간 저장 | “머리 스타일 마음에 드니까 여기 저장해두자” |
| **COMMIT** | 최종 저장 | “지금 캐릭터 완벽해! 이걸로 확정” |
| **ROLLBACK** | 되돌리기 | “방금 한 변경 망했어. 저장한 지점으로 돌아가자” |

---

# 😊 jong이 이해하기 쉽게 다시 정리하면

- **savepoint**는 “잠깐 체크포인트 찍기”  
- **commit**은 “이제 진짜로 저장!”  
- **rollback**은 “저장해둔 시점으로 되돌리기”

---
