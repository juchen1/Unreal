# Unreal
I just started Unreal now!

## 언리얼 시작 첫째 날 stared date:24-08-03
with Unreal engine KR - start Unreal 2024 lesson 1

설치시 5.4버전으로 / 설치옵션에서 필요없는 거 지우기
Sample파일 받은것은 아무데나 저장가능하나 경로사 한글폴더명은 없도록
압축파일을 푼후 config, content, 실행파일만 복사붙여넣기도 가능

### View port(뷰포트)
- Mouse Left -> 전후[평행이동] 좌우[회전]
- Mouse Right -> 현 위치에서 360도 회전
- Mouse Center -> 카메라를 상하 좌우로 평행이동

- Keyboard WASD[with mouse] -> 상하좌우 이동(마치 캐릭터 처럼)
- Keyboard Q E[with mouse] -> 위 아래 이동

### Contents 이동하기(의자)
- W[이동] E[회전] R[스케일]
- X[red] Y[green] Z[blue]
- 한 축, 두축 혹은 전체 축을 선택해서 작동가능

### Contents Pivot(소파)
- 모델링 수정시 [ctrl + d]로 에셋 복제하고 시작하기
- Tool bar에서 모델링 기능 선택
- XForm에서 Edit Pivot
- 사물밑 부분을 선택희망시[center bottom 클릭]
- 이후 오브젝트를 위로 이동시킨 후 End키 누를시 바닥에 붙고
- 스케일을 늘려도 바닥에 고정된 상태에서 늘어남

### Instance 수정(벽)
- 벽을 선택한 후 - 모델링 - 모델
- plane cut으로 원하는 만큼 자르고[자른 구멍 채우기]
- Mirror로 축을 기준하여 복사하기
- Attribute로 노말 분할 메서드 페이스 설정시 주위환경과 동화
- Triangle Edit으로 벽 이동 및 수정 가능
- Shift로 추가 선택 Ctrl로 선택 제거

### Instance 복제(창문)
- 창문에 필요한 모든 오브젝트를 선택 한 후 Alt를 누르면서 복사
- 벽에서 창문만큼의 크기를 제거하기 위해서
- 모델링 모드에서 생성 박스 크기와 위치를 창문 크기에 맞게 적당히 조절(단 박스는 벽을 통과해야한다.)
- 벽과 박스를 차례대로 선택한뒤 모델에서 Boolean을 선택하여 구멍을 뚫어준다.
- 창문이 보이므로 사이즈 및 위치를 조절한다.
- 디테일에 material 엘리먼트 0 에 폴더 돋보기를 선택하여 선택한후
- 엘리먼트 2에 동그라미 안에 화살표를 클릭하여 똑같이 적용시켜 준다.

### 적용하기(컴퓨터 책상 맞추기)
- 책상을 옮기고 위치크기를 조절한다. 이때 [Ctrl + `]를 클릭시 물체 기준으로 혹은 월드 기준으로 Trans tool이 변경된다.
-  본체, 모니터, 키보드, 마우스 를 생성하여 위치해두고 VR세트를 책상위에 올려놓는다.
-  어색하게 서있는 콘솔을 피직스에서 피직스 시뮬레이터 체크박스를 클릭하고 시뮬레이터 시작으로 자연스럽게 배치한 뒤
-  시뮬레이터를 실행 시킨다. 이후 위치 조정을 한뒤 콘솔을 클릭한 뒤 마우스 우클릭 후 저장을 누른다.
-  이 모든 오브젝트를 책상기준으로 이동 시키기 위해서는 전체 클릭 후 아웃라이너에서 한 폴더 안에 넣어둔뒤
-  책상을 제외한 오브젝트를 클릭후 책상 하위레벨로 설정한다.

ps.
1. 화면 및 오브젝트 이동에 익숙해지기
2. 매쉬선택에 익숙해지지 않아서 실습했던 벽이 움푹하게 파여 버렸다. 후에 수정하도록 하자.
3. 강의 내용 정리 및 깃허브에 올리기 까지 적용하기 힘듦.
   ㄴ 정리를 위해 똑같은 강의를 3번 다시 봄.



## 언리얼 시작 둘째 날 date:24-08-04

with Unreal engine KR - start Unreal 2024 lesson 2

언리얼 엔진 샘플에 가보면 엔진4로 만든 건축시각화 인테리어 렌더링이 있다.
참고 하도록해보자!

- 라이트 매스[사전에 라이트 맵을 생성하는 기술]
- 레이트레이싱[광선의 경로를 실시간 추적하여 라이팅을 구현하는 기술

### 루멘[완전한 다이내믹 글로벌 일루미네이션 및 리플렉션 시스템으로 성능과 퀄리티 양쪽을 만족시키는 언리얼 엔진5의 새로운 라이팅 시스템
- 패스트레이싱[물리적으로 정확한 글로벌 일루미네이션과 리플렉션 및 리프랙션을 적용한 라이팅 시스템
- 프로그래시브 렌더링[시간이 흐를 수록 저해상도에서 고해상도로 이미지 퀄리티가 향상되는 렌더링 방식
- 코스틱[빛의 반사광이 다른 물체에 맺히는 형상]

###  라이트를 초기값으로 변경해서 하나씩 추가해보기
창 - 레벨 - 레벨 - 새로생성 [ 항상 퍼시스턴트(최상위 레벨) 레벨을 항상 더블클릭]
아웃라이너 - Lighting[Player Start, PostProcess외 모두 제거] - post process
디테일 - 글로벌 일루미네이션 - 루멘일루미네이션 - 초기값으로 변경 
#### 에셋(오브젝트)에서 자체 발광하기 때문에 자체 발광제거
- TV[밝기 메트리얼을 복사 덮기]
- Fanbody[머티리얼을 더블클릭하여 속성으로 들어간 다음 Emissive를 200으로 변경]
- 커튼[머티리얼 글로벌 스칼라 파라미털 Value를 0.3에서 0으로
- 야외[빛이 남아있는데 이럴 때는 아웃라이너의 야외쪽을 비활성화 했다가 활성화 한다.
- 노트북[노출값 보정을 해야하는데 아웃라이너 - Post - Exposure - manual로 설정시 현실적으로 변경된다.
- 창액터 배치시 디렉셔널 라이트 배치 -> 모빌리티를 무버블로

### 스테이셔너리[라이트맵을 생성하면서 동시에 일부 속성을 실시간으로 변경하거나 캐릭터의 다이내믹 섀도를 생성
- 리얼타임캡처
- Skylight - 무버블 - 대기 산란 효과 -> 스카이 매트어스프[물리기반 마을 및 대기렌더링을 위한 컴포넌트 건드릴 것 없이 추가. 실제 대기의 특성을 라이트에 적용
디렉셔널라이트 -> 태양을 [Ctrl + L]로 설정


### 익스포텐셜 하이트포그
카메라 바로 앞이라 뿌옇게 보이는데
Value metric fog 활성화 하기 -> 시작거리를 2000(1ekd 10cm)으로 설정시 20M
Directional Light -> 10Lux -> 12만으로 설정 
Sky light가 파래지는 이유. 직사광선이 대기중 산란빛이 많아서

PostProgrcess-> Lumen clonal -> 고급 -> 스카이라이트 누수 Cloud 추가후
Asset 박스 아래 세팅에서 엔진 플러그 활성화 

위내용들을 한번에 적용시키는 방법은 SunSky를 추가

### 프리맵
- 구성된 재활용 가능한 에셋 전구 40W 8cd정도
  blueprint actor 생성 항상 컴파일 후 저장

ps.
1. 2주차는 동영상을 따라만들기도 벅찼음. - 분명 똑같이 한 것 같은데 결과값이 달랐음[후에 뭔가 빠졌다거나 놓친 부분도 있었고 영상과 다른 부분도있었음]
2. 블루프린트의 새로운 개념을 이해하고 받아들임
3. 언리얼 엔진이 얼마나 빛에대해 진심을 가졌고 노력했는지 알 수 있었음.
4. 조명때부터 놓쳤지만 이 부분은 추후 더 많은 연습이 필요하다고 느낌


## 언리얼 시작 셋째 날 date:24-08-05

with Unreal engine KR - start Unreal 2024 lesson 3

- 캐릭터 애니메이션 작업하기

### 시퀀서[언리얼 엔진의 멀티 트랙 에디터로, 시네마틱 시퀀스를 실시간으로 제작하고 미리보는 데 사용됩니다.]
 - 시간의 흐름에 따라서 캐릭터나 엑터에게 애니메이션을 주는 툴

### 필요없는 아이콘 가리
- 아이콘을 다른 곳에 두기
- 에디터 빌보드 스케일 사이즈를 줄이기[0으로 만들면 보이지 않음. 그러면 다시 찾기 힘듦]

### 시퀀서 추가하기
- 콘텐츠 브라우저에서 적당한 위치에 - 우클릭 - 시네마 - 레벨 시네마 작성후 이름 변경
- 아이콘을 레벨에 넣어둔뒤 보이지 않도록 아래로 내리기
- 시퀀서가 클릭 되어있는 상태에서 오른쪽에 레벨 시퀀스 열기 하면 기본 에디터 창이 뜸
- 블루프린트[노드기반 인터페이스로 게임플레이 요소를 만들 수 있는 언리얼 엔진의 비주얼 스크립팅 시스템. 언리얼 엔진이 제공하는 다양한 도구들의 인터페이스로도 사용
- 스켈레탈 메시[본과 본에 따라 형태가 변형되는 폴리곤의 집합으로 구성된 언리얼 엔진의 에셋. 일반적으로 캐릭터를 표현하기 위해 사용]
- 메니를 레벨에 넣기 - 매니를 클릭한 후 추가 엑터 BP_매니 클릭하기 - 스켈레톤 매쉬 아래를 지우고 오른족+를 눌러 매니 에니메이션 추가하기

- 시퀀서[언리얼 엔진에서 시네마틱 작업을 할 수 있는 툴 세트]
- 시퀀스[캐릭터가 움직일 수 있도록 본의 시간에 따른 트랜스폼 데이터를 키 값으로 저장하고 있는 에셋]
- 애니메이션 데이터들은 애니메이션 클립이라고 부르기

- 컨트롤 릭[캐릭터에 리깅 및 애니메이션 작업을 언리얼 엔진에서 할 수 있는 애니메이션 툴세트
- 리깅[캐릭터가 움직일 수 있도록 본은 생성하여 할당하고 일부 본의 움직임을 절차적으로 구현하는 과

### 단축키
- 타임라인 영역 좌우 이동[Shift+휠스크롤]
- 타임라인 범위 조절[Ctrl+휠스크롤]
- 지정된 타임라인에 재생 시작바 배치 "[", 종료바 배치 "]"
- 시퀀서 재생 / 일시정지[Space bar]
- 선택된 오브젝트의 트랜스폼 키를 생성[S]
- 선택된 트랙에 키를 생성[Enter]
- 선택된 트랙에서 이전 키 캅의 위치로 점프[,] | 다음키[.]

### 모션 캡처 폴리싱[스캔 받은 애니메이션 데이터에서 노이즈나 불필요한 키를 제거하고 미흡한 구간에 키를 수정하거나 추가하여 애니메이션 데이터를 다듬는 작업]

스냅을끄고 키를 다음 모션에 이동시키기
애니메이션 타이밍 매니와 퀸같이 캐릭터가 두명일 때 마커를 이용하여 다수의 캐릭터들 간에 싱크 맞추기
가위바위보 하는 위치에 마커 넣기 
마커 라벨에는 한국어 넣어도 됨 / 색깔 변경도 가능
마커가 이동하는 경우가 있는데 방지 하기 위해 빈칸에 잠김 누르기

- 캐릭터 저장 - BP_manny 우클릭 스포너블 클릭 스포너블[시퀀서가 애니메이션에 필요한 오브젝트를 직접 생성 / 삭제하는 모드]
- 레벨에 종속되지 않게 하기위해서 포제서블[레벨이 이미 배치된 오브젝트에 시퀀서가 애니메이션만 적용하는 모드]
- 저장[레벨과 시퀀서는 별개로 저장됨]

어도비에 Mixamo보면 많은 모션이 있음
with Skin[애니메이션과 캐릭터 메시를 모두 포함한 데이터 제공]
Without Skin[본 정보와 애니메이션 데이터만 제공]
다운받은 파일은 콘텐츠 브라우저에 적당한 위치에 폴더생성 후 넣어두기 "FBX"

애니메이션 리타기팅[동일한 스켈레톤 에셋을 비율이 크게 다를 수 있는 캐릭터 간에 애니메이션을 재사용할 수 있는 기능]
애니메이션 모션을 추가했을때 두개가 합쳐버림 펠비스[골반에 위치한 본을 일반적으로 일컫는 명칭]기준으로 합쳐버림
필요없는 모션을 섹션 잘라내기 하기 - 틈이 있는데 현재는 신경스지 않아도 문제 없음 
주의! 뷰포트에서 클릭해서 선택하면 액터 그 자체가 선택됨. 여기서는 액터가 아니라 액터의 하위에 있는 스켈레탈 메시 컴포넌트를 선택해야 하기 때문에 시퀀서에서 스켈레탈 메시 트랙을 선택한 뒤에 뷰포트에서 조작을 해야함
자물쇠 - 오토키 자연스럽게 바꿔줌
상수 보간[다음 키에서 값이 변하기 전까지 현재의 키 값이 고정된 채로 유지되는 보간방식]
애니메이션 블렌딩[서로 다른 애니메이션을 가진 애니메이션 클립을 겹치고 가중치를 조절해서 자연스럽게 모션이 연결되도록 하는 작업]
서로 겹쳐서 웨이트를 해도 괜찮지만
같은 라인에 서로 겹치면 알아서 트랜젝션[애니메이션과 애니메이션 사이에 전환이 일어나는 구간]이 일어남

거만하게 앉는 모션
오토키를 설정하고 위치조절,  초기 기본 설정 추가 해서 책상을 스포너블로 하지않고 그대로 둠
다리가 올라갈때 책상을 다리 아래로 옮겨줌 그 키를 모션 바뀌는 그 왼족 부분으로 이동
컨트롤 릭[캐릭터에 리깅 및 애니메이션 작업을 언리얼 엔진에서 할 수 있는 애니메이션 툴 키트]
레이어드 컨트롤 


## 언리얼 시작 넷째 날 date:24-08-06

with Unreal engine KR - start Unreal 2024 lesson 4

나이아가라와 블루프린트 이용하기
### 블루프린트[오브젝트에 기능을 추가하거나 상태를 변화시킬 수 있는 언리얼 엔진의 비주얼 스크립팅 언어]
### 나이아가라[방송, 영상에서 사용 가능한 고퀄리티 이펙트 제작이 가능한 언리얼 엔진의 새로운 파티클 시스템]

### 블루프린트: 환기팬 만들기
- 액터[레벨에 배치하기 위해 필요한 이동, 회전, 스케일 기능 및 기타 필요한 기능들을 지원하는 언리얼 엔진의 클래스]
- 컴포넌트[특정타입의 오브젝트를 지정할 수 있는 일종의 컨테이너 액터의 모양 뿐만 아니라 움직임, 렌더링 방식 등을 제어기능]
- 액터 생성 이름을 BP_Fan으로 설정하고 더블 클릭하여 들어가기
- 운동하는 것이 아닌 회전 하고 있다.
- 객체 지향 언어[독립된 다수의 객체를 만들고 이 객체들끼리 서로 상호작용하도록 만드는 컴퓨터 프로그래밍의 한 체계]
- 이벤트 그래프[특정 타이밍에 연결된 작업을 수행하기 위해 호출(실행) 시키는 노드]에서 움직이는 것을 컨트롤 한다.
- Archviz에서 팬의 구성품들을 클릭한 후 블루프린트에서 전체 추가하기
- 컴파일을 항상 하기
- 선택된액터로 변환하기로 해서 바꾸기
- Tip. 이번 강의와 같이 하나의 오브젝트 역할을 하는 블루프린트 액터는 컴포넌트들이 단일 루트를 가지도록 하면서 형태를 수정하거나 기능을 추가하는 등의 추가 작업시에 훨씬 효율적입니다.

### 환기팽에 회전 기능 추가하기
- custom event 추가하고 SeqTick으로 이름 변경 실행 라인[노드와 노드를 연결하면 순서대로 노드를 작동시키는 선] 실행 핀[실행 라인을 연결할 수 있는 연결점
- 블레이드를 가져옴. 데이터핀[노드가 작동하는데 필요한 데이터를 주고 받을 수 있는 연결점] - rotate Get[저장된 데이터를 읽어서 불러오는 기능] Set[지정된 저장소에 원하는 데이터를 덮어 씌우는 기능] Add relative rotate
- roll pich Yaw 로우 5도씨 움직이기
- 트리거[특정 타이밍에 원하는 이벤트를 호출(실행) 리피터[지정된 구간 동안 매 프레임마다 원하는 이벤트를 호출(실행)]
- 이벤트 퀵바인더에서 검색프로퍼티 에디터에서 호출 무조건 해주기
- FanRPM 컴포넌트에 추가하기 플로트로 선택
- 클래스[오브젝트를 만들어 내기 위해 필요한 설계도, 콘테츠 브라우저에서 보이는 블루프린트는 클래스]
- 인스턴스[클래스로부터 실제로 구현된 오브젝트, 레벨, 레벨에 배치된 블루프린트는 인스턴스(오브젝트)
- 키를 추가해서 속도를 변경할 수 있다.

### 캐릭터 블루프린트 만들기
- 커스터마이징 가능한 머티리얼은 인터넷에서 가져오기(현 단계에서 하기에는 무리)
- 머티리얼[오브젝트의 표면의 시각적인 현상을 정의하는 일종의 '페인트'] / 머티리얼 인스턴스[머티리얼의 자손, 머티리얼에서 사용된 파라미터들은 머티리얼 인스턴스 에디터에서 노출되고 실시간으로 편집 가능]
- 스켈레톤메시를 가져와서 이벤트를 다 넣어주고 시퀀서로 가서 키값을 준 다음 각 캐릭터에 입력해주기

### 머티리얼과 머티리얼 인스턴스로 사라지는 효과 표현하기
- 디졸브[한 이미지에서 다른 장면으로 넘어갈 때 서서히 넘어가는 효과]
- 자연스럽게 작동하기 위해 매 프레임마다 커스텀적용하기
- Tip[머티리얼 인스턴스의 부모가 항상 머티리얼이 아니라 머티리얼 인스턴스인 경우도 있습니다. 이 경우에는 계속 '부모찾기'를 반복하시면 머티리얼에 도달할 수 있습니다.]
- 알파클립을 연결해서 붙이기
- 파라미터 이름 꼭 넣기

### 나이아가라로 사라지는 효과에 이펙트 추가하기
- 이펙트 안에 나이아가라시스템이 있음
- 표시명 복사
- 마켓에서 구매하면 거기에 있는 설명서 잘 보기
- 0에서 2000까지 갔다가 오는 것으 커브를 넣어주기 _ 알파에서 get curve입력하기

ps. 언리얼에서 사용되는 기능들은 이전 사진 편집이나 동영상 편집툴을 사용한 것과 비슷한 기능들을 합친 것과 같다. 여기에 C++까지 더한다면 확실히 내가 지금까지 해온 모든 기술을 다써야 언리얼을 할 수 있지 않을까 하는 두근거림이 있다. 


## 언리얼 시작 다섯째 날 date:24-08-07

with Unreal engine KR - start Unreal 2024 lesson 5

영상 연출 및 렌더링 하기

### 계획하지 않았던 기능들 변경하기
- 디렉터 블루프린드[시퀀서 이벤트가 호출(실행)되면 대응하는 액터의 이벤트가 자동으로 호출(실행)되도록 기능하는 블루프린트]


### 시퀀서에서 카메라 추가하고 애니메이션 적용하기
- Cine Camera Actor[시네카메라] 실제 물리적인 카메라의 기능들을 넣어서 현실처럼 보도록
- 0, 120 키주기 각 키갑에 [, ] 로 재생 넣어주기 'F'를 누르면 자동으로 재생구간 크기를 키워줌

### 시퀀서에서 카메라 포커스 설정하기
- 트랜스폼 키를 가진 액터의 움직임을 없애려면 키들을 수정하는 것보다 하나의 키만 남기고 모두 삭제한 뒤에 남은 키를 복제하는 것이 효과적입니다.
- 120에 확대샷을 넣어주면 확되되는 영상으로 바뀜
- 초점이 맞지 않는데 포커스 셋팅에서 수동 초점거리를 변경도 가능하지만 스포이드를 클릭하고 초점 맞추고 싶은 오브젝트를 누르면 자동으로 눌려짐
- 피벗[액터의 트랜스폼(위치, 방향, 크기)에 대한 기준점]이 너무 멀경우 잘 안될수있음 그래서 디버그 초점 평면그리기 체크해서 초점이 잘 지정되었는지 확인하기
- 이후 확대할때는 초점 위치를 창문으로 변경 가능

### 시퀀서에서 카메라 추가하고 카메라 컷 설정하기
- Shot_00으로 각각 두개의 카메라를 추가하기
- 파란 아이콘이 활성화 되어있을 경우 그 샷이 보여지고 있다.
- 카메라 컷 트랙[시퀀서가 재생될 때 활성화될 카메라를 선택하는 트랙]
- 카메라컷에서 shot1 120에서는 shot2로 추가해준다.
- Ease in[움직임이 서서히 시작해서 빨라지는 것] / Ease Out[움직임이 멈출 때 서서히 감소하는 것]
- 커브에디터를 눌러서 선형보간을 클릭하면 이지 인아웃없어짐


### 시퀀서에서 카메라가 추가하고 초점 길이 조작하기
- 샷3 추가하기 285~ 425까지 재생 구간 만들어두고 샷3 추가하기
- 샷3는 퀸에게 초점을 맞추고 줌아웃 효과 넣어주기
- 천장을 뚫고 가는데 이경우 초점길이를 양족에 두고 뒤쪽에 숫자를 낮추면 점점 멀어지는 느낌을 줄수 있다.[이 때 당연히 퀸에게 포커스 초점을 걸어줘야한다]

### 미디어 트랙으로 시퀀서에 영상 추가하기
- 써드펄슨맵 열어주기
- 미디어트랙: 미디어용 레벨 사전 작업하기
- 스켈레톤 퀸을 블루프린트 퀸으로 바꿔주기
- 미디어 트랙: 무비렌더 큐로 미디어 렌더링하기
- 플러그인에서 무비렌더큐를 활성화 하기
- 최종시퀀서를 렌더링 할수 있는 기능
- 프리셋저장으로 나중에 다시 설정을 불러올 수 있음
- 랜더링 후에는 폴더에서 확인할 수 있음
- 이미지 파일을 출력하는 이유는..?

### 무비렌더 큐로 MP4 영상 렌더링하기
- 영상에서는 항상 이미지로 시작함 영상을 원할 경우 언리얼 디벨로퍼 커뮤니티에서 FFmpeg로 검색해서 어떻게 이미지를 영상으로 바꿀 수 있는지 알려줌.
- 다운받은 실행파일을 엔진에 적용시키는 방법 실행가능 경로에 엠펙이 들어있는 파일 경로를 복사해서 실행가능 경로에 붙여넣고 \ffmpeg.exe  입력 | 비디오코덱은 LIBX264 | 출력 파일 확장명은 MP4 | 오디오코덱은 AAC
- 명령줄 인코더에 소스파일 삭제하면 이미지를 삭제하고 영상이 저장됨

### 시퀀서에 미디어 추가하기
- 뷰포트 게임모드 전환[G}
- 콘텐츠 브라우저에 TV폴더 만들어주고 - 오른쪽 클릭 -  미디어 - 파일미디어 소스 클릭 - 아까 만들어둔 영상 추가하기
- 미디어플레이어 생성하기
- 미디어텍스처를 바로 레벨에 넣어두기
- 나와서 미디어 트랙을 추가한뒤에 미디어텍스터에 만든것을 추가하고 화살표를 눌러 적용하기

### 루멘의 퀄리티 높이기
- 포스트프로세스: 볼륨 파이널 개더 퀄리티 1일경우 값을 높이기 - 리얼타임일 경우 4~8사이로 두기
- 루멘씬: 루멘씬으로 보면 라이팅 퀄리티와 디테일이 인데 4가 가장 적당함
- 표면 캐시[루멘이 오브젝트에 자동으로 생성하는 표면 라이팅 정보 더 단순한 표면 캐시를 통해서 레이가 닿는 포인트의 라이트 정보를 빠르게 확인할 수 있음]  --> 벽들을 분리 하는 이유.
- 반사가 너무 클 경우 오브젝트를 클릭하고 언릿으로 볼경우 명도를 확인 할 수 있음, 여기서 명도와 채도를 줄임
- 어두운 환경: 랙트라이트 추가하고 밝은 소스텍스처를 추가하기, 이미시브라이트는 최대한 피하는 것이 좋음

- 트랙 샷이 너무 많을경우 묶어서 폴더에 넣어두기
- 무비 렌더 큐: 무비렌더큐를 열고 셋팅에들어가서 해상도를 낮추거나 커스텀 재생범위 사용누르고 시작프레임을0 끝을 10으로 설정
- 첫페이지가 퀄리티가 낮은데 이때 퀄리티를 높이려면 안티에일리어싱을 체큰해줌 오버라이드를 넌으로 변경
- 안티에일리어싱 세팅[최종 프레임 생성에 사용되는 샘플 수를 설정, 안티에일리어싱, 모션 블러, 레이 트레이싱의 노이즈 퀄리티를 높일 수 있음]
- 공간샘플링[같은 타이밍에 조금씩 위치가 어긋난 화면을 렌더링]
- 템포럴 샘플링[하나의 프레임을 정해준 수만큼 나눠서 시간차로 렌더링]
- 넌으로 설정할 시 위 두개의 샘플링을 조절할 수 있음
- 공간은 두고 템포럴을 4로 올림 웜업 렌더링에 체크하고 엔진 웜업수를 128로 입력
- 서있는 친구가 이상할 경우 0으로 설정한 시작프레임을 1로 변경
- [0프레임에서 영상을 시작할경우 애니메이션은 0이전부터 만들기]
- 렌더링할때만 8로 변경하고 싶을 때 세팅에서 콘솔 변수 들어가서 콘솔변수를 추가하기 디벨로퍼 검색에 technical guide를 검색 학습클릭 맨 위에를 클릭하고 13번 랜더링 클릭 보면 최소 퀄리티가 있음 그 아래 팁이 있음.

ps. 
1. 점점 자신감이 붙어감 많이 낯설었던 언리얼이 5강를 지나서 나도 영상을 만들어 보고 싶다라는 마음이 생김.



## 언리얼 시작 여섯째 날 date:24-08-08

with Unreal engine KR[러셀] - start Unreal 2022 lesson 1

언리얼 엔진 시작하기 [ 5.0.2버전]

###  UE5 에디터 UI소개
언리얼 4 레이아웃으로 변경가능
뷰포트 및 카메라 이동 방법
오브젝트는 액터라고함
화살표는 기즈모라고 함 
스냅기능 
#### 디테일 기능[액터에대한 모든 옵션은 디테일에 있다고 보면 됨]
- 트랜스폼 속에서 정확한 위치 이동과 드래그로 이동 및 변경 가능함

#### 콘텐츠 브라우저
- 콘텐츠 내에있는 데이터를 에셋이라고 부르기 외부데이터는 콘텐츠 브라우저에 넣어서 임포트 한뒤 사용

#### 액터배치
- 기본적으로 가지고 있는 액터를 사용할 수 있음.

#### 재생버튼을 클릭하면 실제 플에이 하는 것처럼 사용 가능 ESC버튼을 누르면 사라짐
#### 캐릭터 능력 및 기능 변경하기
- 콘텐츠 브라우저안레 블루프린트로 들어가면 
- 플레이어스타트로 캐릭터 시작 위치 지정 가능

- Props[소품]
- Materials[오브젝트의 외형을 결정]
- static mesh actor + material = 완성형 액
#### 아웃라이너 특정 액터를 검색해서 찾고 싶을때 사용 가

- 표면스냅
- End키를 누르면 바닥에 붙음
- 기즈모 위치 바꾸기[Alt + 마우스휠누르기] 임시로 사용가능
- 피벗[오브젝트의 중심]
- 모델링은 익스포트 가능하나 머티리얼은 언리얼에 고유 도구
- custom은 다른 3D 프로그램을 사용해서 임포트해도 괜찮음
- 머티리얼과 텍스처의 차이 / 표면과 질감 재질에대한 모든 것이 있다면 텍스처 머티리얼의 재료라고 보면 된다.
- 뷰포트에서 샌드위치 아이콘 클릭 고해상도 스크린으로 캡처 가

ps. 기초부터 배우니 훨씬 좋음


## 언리얼 시작 일곱째 날 date:24-08-09

with Unreal engine KR[러셀] - start Unreal 2022 lesson 2

언리얼 엔진 시작하기 [ 5.0.2버전]

### 퀵셀[Quixel] 메가스캔 에셋 다운로드 & 배치
- 브릿지를 실행 후 엑픽게임즈 아이디로 로그인
- 원하는 머티리얼을 고르고
- 퀄리티 설정[나나이트가 가장 고퀄] - 용량 확인하기
- 임시 위치는 preferences에서 경로 설정 가능[보조디스크에 설정해도 괜찮음]
- 이후 다운로드 Add를 클릭하면 콘텐츠 브라우저로 들어옴 모든 파일은 megascans하위 폴더에 저장됨
- 첫번째는 머티리얼, 두번째는 스태틱 매쉬, 이후 텍스처
- 라운로드 하지 않아도 퀵셀 브릿지에서 드래그로 바로 레벨에 넣을 수 있고 이때 저용량으로 저장되는데 후에 나나이트로 다운 받은 경우 대체가능함
-  퀵셀은 분류가 잘 되어있으니 한번 둘러보기
-  다중 선택 및 다운로드, 임포트 가능.
-  후에 저퀄로 다운 했을 경우 에셋우클릭 나나이트 활성화 해야함
-  필터를 이용하면 스태틱 매쉬만 확인 할 수 있음

### 머티리얼 내 수정하기
- saturation[채도]
- brightness[명도]
- Albedo[색깔변경가능]
- Roughness[거칠기]
- 콜리전 세팅하기[충돌데이터] / 자동 컨벤션 콜리전 / 적용
- 오차가 있는 부분은 스택틱 매쉬에들어가서 디테일부분속 콜리전/콜리전 복잡도를 가장 아래호 설정하면 오차가 줄어듦 
- 식물은 많이쓰기 때문에 퀄리티를 미디엄에서 하이사이로 하면 좋음
- 식물에는 베리에이션이 있어서 하나를 임포트해도 다양한 종류로 됨
- 플랜트 머티리얼 설정 알베도[컬러오버레이에서 명도를 조절] 러프니스[줄이면 촉촉한 느낌이나 입체(생동감)이 늘어남]
- 윈드 기능이 있는데 체크하면 오른쪽 체크박스가 또 생기는데 체크하면 식물들이 자연스럽게 움직임
- 폴리지로 플랜트 배치하기
- 선택관리에서 폴리지 모드 / 사용한 식물들이 있는데 전체 선택을 한 뒤 / 체크한뒤 / 뷰포트에서 드래그하면 식물들이 대량으로 배치가 가능함
- 삭제하려면 Shift를 누른뒤 드래그 하면 가능함
- 각 플랜트의 크기 조절은 그 아래에 관련 설정이 있음, X의 최소 최대크기를 조절 할 수 있음
- 밀도를 높이면 더 많이 넣을 수 있음.


### Q&A 
- 피직스 시뮬레이션에 체크하고 질량을 적절하게 설정하면 캐릭터가 움직이도록 밀 수 있음.
콜리젼을 복잡하게 하면 설정 안됨/
- 원근내에서 다른 3D툴들저첨 평면도 확인 가능
- 북마크[Ctrl+ 숫자키]
- 퀵셀에서다운 받은 것을 전체 선택 한 뒤 한번 로드하면은 버벅임이 덜함.
- 언리얼 공부방법 . 언리얼 온라인 러닝
- 고해상도 스크린샷 뽑는 방법 명령어 입력하기. 콘솔에서  HighResshot 3840x2160 을 입력하면 4K로 저장 가능
- 나나이트란? 폴리곤의 갯수도와 상관없이 불러올 수 있는 기술
- 식물은 현재[5.0.2]에서 나나이트를 지원하지 않는다.
- 파일 / 프로젝트 압축을 하면 다른 컴퓨터로 옮기기 쉽다.
- 조립식 모델형이 있는데 객체 규격을 단위별로 설정하고 하면 스냅으로 설정하면 쉽다.


ps. 
1. 자연환경 배경을 만드는데 큰 도움임 됨
2. Q&A에서 꿀팁이 많았음 꼭 듣고 가기!










