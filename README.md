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
## 블루프린트[오브젝트에 기능을 추가하거나 상태를 변화시킬 수 있는 언리얼 엔진의 비주얼 스크립팅 언어]
## 나이아가라[방송, 영상에서 사용 가능한 고퀄리티 이펙트 제작이 가능한 언리얼 엔진의 새로운 파티클 시스템]

## 블루프린트: 환기팬 만들기
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

## 환기팽에 회전 기능 추가하기
- custom event 추가하고 SeqTick으로 이름 변경 실행 라인[노드와 노드를 연결하면 순서대로 노드를 작동시키는 선] 실행 핀[실행 라인을 연결할 수 있는 연결점
- 블레이드를 가져옴. 데이터핀[노드가 작동하는데 필요한 데이터를 주고 받을 수 있는 연결점] - rotate Get[저장된 데이터를 읽어서 불러오는 기능] Set[지정된 저장소에 원하는 데이터를 덮어 씌우는 기능] Add relative rotate
- roll pich Yaw 로우 5도씨 움직이기
- 트리거[특정 타이밍에 원하는 이벤트를 호출(실행) 리피터[지정된 구간 동안 매 프레임마다 원하는 이벤트를 호출(실행)]
- 이벤트 퀵바인더에서 검색프로퍼티 에디터에서 호출 무조건 해주기
- FanRPM 컴포넌트에 추가하기 플로트로 선택
- 클래스[오브젝트를 만들어 내기 위해 필요한 설계도, 콘테츠 브라우저에서 보이는 블루프린트는 클래스]
- 인스턴스[클래스로부터 실제로 구현된 오브젝트, 레벨, 레벨에 배치된 블루프린트는 인스턴스(오브젝트)
- 키를 추가해서 속도를 변경할 수 있다.

## 캐릭터 블루프린트 만들기
- 커스터마이징 가능한 머티리얼은 인터넷에서 가져오기(현 단계에서 하기에는 무리)
- 머티리얼[오브젝트의 표면의 시각적인 현상을 정의하는 일종의 '페인트'] / 머티리얼 인스턴스[머티리얼의 자손, 머티리얼에서 사용된 파라미터들은 머티리얼 인스턴스 에디터에서 노출되고 실시간으로 편집 가능]
- 스켈레톤메시를 가져와서 이벤트를 다 넣어주고 시퀀서로 가서 키값을 준 다음 각 캐릭터에 입력해주기

## 머티리얼과 머티리얼 인스턴스로 사라지는 효과 표현하기
- 디졸브[한 이미지에서 다른 장면으로 넘어갈 때 서서히 넘어가는 효과]
- 자연스럽게 작동하기 위해 매 프레임마다 커스텀적용하기
- Tip[머티리얼 인스턴스의 부모가 항상 머티리얼이 아니라 머티리얼 인스턴스인 경우도 있습니다. 이 경우에는 계속 '부모찾기'를 반복하시면 머티리얼에 도달할 수 있습니다.]
- 알파클립을 연결해서 붙이기
- 파라미터 이름 꼭 넣기

## 나이아가라로 사라지는 효과에 이펙트 추가하기
- 이펙트 안에 나이아가라시스템이 있음
- 표시명 복사
- 마켓에서 구매하면 거기에 있는 설명서 잘 보기
- 0에서 2000까지 갔다가 오는 것으 커브를 넣어주기 _ 알파에서 get curve입력하기

ps. 언리얼에서 사용되는 기능들은 이전 사진 편집이나 동영상 편집툴을 사용한 것과 비슷한 기능들을 합친 것과 같다. 여기에 C++까지 더한다면 확실히 내가 지금까지 해온 모든 기술을 다써야 언리얼을 할 수 있지 않을까 하는 두근거림이 있다. 
