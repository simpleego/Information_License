# UML

## UML이란
- 시스템 개발이나 프로젝트 아이디어를 상대방에게 효과적으로 설명하며 의사소통을 효율적이고 효과적으로 이루어지게 하기 위해 표준화된 모델링 언어이다.
- 다양한 다이어그램으로 구성되어 있는 UML은 시스템을 다양한 시각에서 볼 수 있는 뷰(view, 관점)를 제공한다.
- 설명하는 사람뿐만 아니라 설명을 듣는 사람도 서로의 의도를 쉽게 이해하고 고칠 수 있기 때문에, UML을 보며 다양한 의견과 피드백이 오고 갈 수 있다.

## UML 다이어그램의 종료
<img width="700"  alt="image" src="https://github.com/user-attachments/assets/c72f2dd9-6118-4877-8c62-5bd14fc38cdb" />

# 대표적인 UML 다이아그램 예시
<img width="700" alt="image" src="https://github.com/user-attachments/assets/cf7aa7b3-9f7a-431a-bd41-60bf737a2c84" />

## 클래스 다이어그램
> 시스템의 정적 구조를 보여주며, 클래스와 클래스 간의 관계를 표현

### 클래스 구성 요소
- 클래스
  > 공통의 속성, 메서드(오퍼레이션), 관계, 의미를 공유하는 객체 집합에 대한 기술
- 속성
  > 클래스의 구조적 특성에 이름을 붙인 것
  > 구조적 특성에 해당하는 인스턴스가 보유할 수 있는 값의 범위를 기술
  > 영문 소문자로 시작함
  > 
<img width="700" alt="image" src="https://github.com/user-attachments/assets/ac501faf-912e-4ecd-826d-f095abca49e2" />

- 메서드

<img width="909" alt="image" src="https://github.com/user-attachments/assets/40c124b0-6e2b-4f55-a881-892b9c492e72" />
<img width="700"  alt="image" src="https://github.com/user-attachments/assets/ce177864-25f5-4429-9461-7b9188f9d39c" />

### 클래스의 관계
> 객체와 클래스 사이의 관계와 표현
> 연관 관계는 의존 관계와 마찬가지로 객체를 생성하는 관계
> 그러나 연관 관계는 멤버 변수로 참조하고, 의존 관계는 메서드로 참조한다는 것이 다름

<img width="700"  alt="image" src="https://github.com/user-attachments/assets/668f45b3-4604-4dbd-a460-0cd067f8c369" />
### 🔗 클래스 간 관계  

| 관계 | 설명 | 표기 |  
|------|------|------|  
| **연관(Association)** | 한 클래스가 다른 클래스를 참조 | 실선 |  
| **집합(Aggregation)** | 전체-부분 관계, 부분은 독립적 존재 가능 | 속이 빈 마름모 |  
| **합성(Composition)** | 전체-부분 관계, 부분은 전체와 생명주기 공유 | 속이 채워진 마름모 |  
| **상속(Generalization)** | 부모-자식 관계 | 속이 빈 삼각형 화살표 |  
| **실체화(Realization)** | 인터페이스 구현 | 점선 + 속이 빈 삼각형 |  
| **의존(Dependency)** | 한 클래스가 다른 클래스에 의존 | 점선 화살표 |  

[클래스 관계 사이트 주소](https://kyoun.tistory.com/100)


## Use Case 다이아그램
> 소프트웨어 혹은 시스템의 기능과 사용자들의 관계를 나타낼 수 있는 다이어그램이다. 시스템과 사용자의 상호관계를 표현하는 다이어그램이다.

## 유스케이스 다이어그램 구성요소 : 사물(Things)
- 액터(Actor)= 사용자
- 케이스(Usecase)=서비스 또는 기능
- 관계(Relationships)
  > 액터와 유스케이스 사이의 의미 있는 상호관계를 의미함
  > 연결선의 종류에 따라 연관, 포함, 확장, 일반화 관계로 구분됨
 
<img width="700" alt="image" src="https://github.com/user-attachments/assets/3d288360-adef-4a25-8381-682e41e27626" /> 

---  
<img width="700" alt="image" src="https://github.com/user-attachments/assets/af79ade1-b900-4222-a3db-1253caaf0f73" />

### 해석 예시
액터인 ‘학생’이 유스케이스 중 ‘공부를 한다’와 연결되어 있음  
즉 ‘학생이 열람실에서 공부를 한다’로 해석됨  

<img width="700"  alt="image" src="https://github.com/user-attachments/assets/9742f97a-a8e6-4157-8552-1931dd5d9295" />

### 구내 식당 예제 유스케이스 다이아그램
<img width="700" alt="image" src="https://github.com/user-attachments/assets/c1ada122-6268-48c1-b3fc-b9698c6f5375" />

##  Sequence 다이아그램
- 시스템 세부사항들의 진행 과정과 시간적 흐름을 표현할 수 있는 다이어그램임
- 즉 팀에서 탐색한 주제에 맞게 프로젝트가 잘 진행되고 있는지 활동의 흐름을 확인할 수 있으며, 활동을 시간 순서에 따라 자세히 표현할 수 있음
- 
### 시퀀스 다이어그램(Sequence Diagram) 구성요소
❶ 액터(actor ) : 시스템을 사용하는 사람이나 외부 시스템을 의미한다.  
❷ 객체(object ) : 시스템 내에서 객체과 객체, 객체와 액터가 상호작용하는 개체를 의미한다.  
❸ 메시지(message) : 객체 간의 상호작용을 의미한다. 수평의 화살표 방향으로 진행되는 것을 의미한다.  
❹ 생명선(lifeline ) : 객체가 존재할 수 있는 시간을 의미한다. 객체가 소멸되면 생명선도 함께 소멸된다.  
❺ 활성화(activation ) : 객체가 활성화된 기간을 의미한다.

<img width="700"  alt="image" src="https://github.com/user-attachments/assets/c0e8341e-db41-493b-b23b-26f52b2dd4e4" />

### 시퀀스 다이어그램의 구성요소 : 사물(Things)
- 생명선 또는 Lifeline

<img width="700"  alt="image" src="https://github.com/user-attachments/assets/542b742c-9d00-4085-ab6c-10bdde0581e1" />

### 시퀀스 다이어그램의 구성요소 : 관계(Relationships)
- 메시지(Message)가 가장 많이 쓰임
- 이는 프로그래밍 코드의 호출(call )과 밀접한 관계가 있음

  <img width="700"  alt="image" src="https://github.com/user-attachments/assets/c43f887d-f8cf-448d-a9fe-ed107e016264" />









