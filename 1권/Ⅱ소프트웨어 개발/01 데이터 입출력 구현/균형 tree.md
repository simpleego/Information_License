## AVL Tree
<img width="437" height="430" alt="image" src="https://github.com/user-attachments/assets/4fe90c76-90f9-4f0d-bebb-e9bbc4d9dfce" />

<img width="500"  alt="image" src="https://github.com/user-attachments/assets/777f75a2-246a-443b-9de5-7131035fdebb" />


## 2-3 Tree
<img width="527" height="299" alt="image" src="https://github.com/user-attachments/assets/63ee6839-c43b-4704-b9c4-0db8c6aa89af" />

(참고사이트)[https://www.geeksforgeeks.org/dsa/2-3-trees-search-and-insert/]


## Red-Black Tree
> **자가 균형 이진 탐색 트리(Self-balancing BST)**로, 삽입·삭제 시에도 트리의 균형을 유지하여 **탐색, 삽입, 삭제 모두 \(O(\log n)\)** 시간 복잡도를 보장합니다.
> 핵심은 **노드 색깔 규칙(빨강/검정)**과 **회전(Rotation)**을 통해 균형을 맞추는 것입니다.  

---

## 🌳 Red-Black Tree의 기본 원리

### 1. 정의
- **이진 탐색 트리(BST)** 의 일종  
- AVL 트리보다 **덜 엄격한 균형 조건**을 유지하지만, 연산 속도가 더 빠르고 구현이 단순합니다.

### 2. 핵심 성질 (규칙)
모든 Red-Black Tree는 다음 조건을 만족해야 합니다:

1. **모든 노드는 빨강(Red) 또는 검정(Black)**  
2. **루트 노드는 반드시 검정**  
3. **모든 리프(NIL) 노드는 검정**  
4. **빨강 노드의 자식은 반드시 검정** (즉, 빨강 노드가 연속될 수 없음)  
5. **루트에서 모든 리프까지의 경로는 동일한 개수의 검정 노드**를 포함해야 함 (Black-height 동일성)

### 3. 균형 유지 원리
- 삽입/삭제 시 규칙이 깨질 수 있음 → **회전(Rotation)**과 **색상 변경(Recoloring)** 으로 복구  
- 예시:
  - 삽입 시 빨강-빨강 충돌 발생 → 부모/삼촌 색상 변경 또는 회전 수행  
  - 삭제 시 검정 높이 불균형 발생 → 회전과 색상 조정으로 해결  

---

## 🔑 장점
- **탐색, 삽입, 삭제 모두 \(O(\log n)\)** 보장  
- AVL 트리보다 **삽입/삭제가 빠름** (균형 조건이 덜 엄격하기 때문)  
- 실제 라이브러리 구현에서 많이 사용됨 (예: Java `TreeMap`, C++ `map`/`set`)  

---

## 📊 AVL 트리 vs Red-Black 트리 비교

| 구분              | AVL 트리 | Red-Black 트리 |
|-------------------|----------|----------------|
| 균형 조건         | 매우 엄격 | 덜 엄격 |
| 탐색 성능         | 약간 더 빠름 | 로그 시간 보장 |
| 삽입/삭제 성능    | 회전 많음 | 회전 적음 |
| 구현 난이도       | 복잡함 | 상대적으로 단순 |
| 활용 예시         | 데이터베이스 인덱스 | 언어 라이브러리(Map, Set) |

---

## ⚠️ 주의할 점
- Red-Black Tree는 **탐색 성능 최적화보다는 전체 연산 균형**을 중시합니다.  
- AVL은 탐색에 더 유리하지만, 삽입/삭제가 잦은 경우 Red-Black Tree가 더 효율적입니다.  

---

👉 요약하면, **Red-Black Tree는 "빨강/검정 규칙 + 회전"으로 균형을 유지하는 트리**이며, 실무에서 가장 널리 쓰이는 균형 이진 탐색 트리입니다.  

Sources: [Velog – Red-Black Tree 개념과 동작 원리](https://velog.io/@dankj1991/Tree-Red-Black-Tree-Part1), [위키백과 – 레드-블랙 트리](https://ko.wikipedia.org/wiki/%EB%A0%88%EB%93%9C-%EB%B8%94%EB%9E%99_%ED%8A%B8%EB%A6%AC), [네이버 블로그 – Red-Black Tree 개념 및 원리](https://m.blog.naver.com/luexr/223480431474)
