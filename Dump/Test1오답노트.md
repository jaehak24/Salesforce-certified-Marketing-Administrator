# 1.  Bounced Status?
메일을 편지로 생각했을 때 배달부가 편지합에 던졌는데 들어가지 않은 케이스다. 전송 자체는 이루어졌지만, 이를 받는 Inbox에서 받아들이지 않은 상태를 말한다. 이후에 다른 메일의 링크로 접속했더라도 bouncde된 이메일을 받지 않은 상태로 해당 고객의 상태는 bounced로 남아 있는다.

# 2.  Full Permission 
admin이 사용자에게 모든 권한을 위임할 때 주어야 할 2 가지 권한은 다음과 같다.
* Marketing Cloud Administrator: Marketing Cloud Platform의 모든 특징과 기능에 대해 접속할 권한을 준다.
* Administrator: Salesforce의 모든 특징과 기능에 대해 접속 가능한 권한을 준다.

# 3. SSO(Single sign On)
SSO는 여러 개의 applications에 접속하는데에 있어서 하나의 applications에서만 접속하더라도 다른 곳에서도 접속할 수 있게 해주는 것이다. 보안을 위해서 로그인 정보는 암호화되고 이는 보안에 기여를 한다.

# 4. Einstein Email Recommendation
보안정책으로 아직 국내 산업에 들어오기는 어려움 (slack이 클라우드를 사용하는데 이를 사용하면 민감 정보들이 정책에 위반되어 국내에서 일부 기업을 제외하고는 아직 망설여하는 추세)
Einstein Email Recommendation는 Marketing Cloud의 ai 제품 중 하나로 고객의 행동 데이터를 수집하고 이에 대한 선호도 프로파일을 만들고, 이에 기반한 맞춤형 추천을 제안한다.

# 4-1 Interactive Email form Block
Salesforce email studio의 기능 중 하나로 사용자가 원하는 방식으로 이메일 보내게끔 양식을 제공해주는 기능이다.

# 4-2 Eienstein Content Selection
소비자에게 컨텐츠를 제공하는 Salesforce의 AI 모델이다. Content Builder의 기능 중 하나.

# 5 Contact Builder
data extenstions들 관의 관계를 만들어주는 기능을 하는것이 Contact Builder다.
lists, data views, data extensions, data sources 등의 관계를 맺어주는 것을 말한다.
Marketing cloud UI로 접근할 수 있으므로 API를 통해서만 접근할 수 있다는 것은 틀린 사실이다.
단독 또는 그룹으로 관계를 만들 수 있으므로 단독으로만 관계를 맺을 수 있다는 사실은 근거가 없는 정답지다.

## 6 Cloud admin이 Sales cloud Object를 동기화하고 leveraged(활용)하기 위해서 데이터를 구성하기 위해서는 어디로 가야 할까요?
Setup -> Data Management -> Synchronized Data Extenstions

오답: 
Contact Builder -> Data Sources 이 방식은 외부의 데이터를 연관짓기 위해서 찾아가는 방식이다.

Contact Builder -> Data Extensions ->Synchronized Data extensions
해당 방식은 Sales cloud Object를 편집하기 위한 탐색이지 구성하기 위한 탐색방식이 아니다.

## 7. NTO 사용자는 Parameter Manager를 사용해서 자동으로 링크를 첨부한다. NTO 사용자는 이제 이메일에 Campaign identifier를 옆에 붙이고 싶어하는데 어떤 단계에서 이를 구성해야 하는가?
1. link 
2. email 
3. Account
정답: utm_campaign 값을 구성하기 위해서는 이메일 단계에서 구성해야 한다. 

### 8. Marketing cloud admin에서 이를 켐페인 우승자를 뽑기 위해서 60%를 배제하려고 하는데 이를 위해서는 어떻게 해야 할까요?
1. No more than two paths.
2. Evaluation Period must be 72 hours
3. Run once schedule type.
4. Split activity with a percentage of 40% and 60%
5. Decision split activity with a percentage of 40% and 60%
6. Use the Random Split activity with a percentage of 40% and 60%
정답: Path Optimizer에서 구성원을 어떤 이벤트에서 배제하고 계산하려면 원하는 비율을 가지고 Random Split 기능을 사용해야 한다. 40과 60에 random split이 동시에 이루어져야 한다.

## 9. 기본 Profile center를 사용해서 일어날 수 있는 참사로서 어떤 것이 있을까요? 
> 고객이 밴리스트에 추가되어 마케팅 수신거부 리시트에 등록될 수 있다.

### 10. Marketing Cloud Connection을 완료하기 위해서 Marketing Cloud admin이 Marketing 클라우드 탭으로 탐색해서 통합을 완료하기 위해서 이동했다. 하지만, 해당 admin이 "권한 부족, 당신은 통합 마케팅 클라우드 유저로 등록되지 않았다." 라는 메시지를 받게 된다. admin은 Marketing cloud 를 위한 Appexchange admin 옵션이 활성화 된 것을 확인했다. 해당 문제를 고치기 위해서는 어떤 행동을 해야 할것인가?
1. CRM 구성에서 적절한 유저 매핑을 해야 한다.
2. 마케팅 클라우드 옵션 중 appxchange User option도 활성화 한다.
3. 앱을 통해서 연결되는 권한 허락을 얻어서 해결한다.

### 11. ip warming: 고객에게 마케팅 메일을 보내는 양을 점진적으로 늘리는 것을 말한다. 고객에게 점진적으로 보내는 연락의 양을 늘리는 것으로서 해당 고객에 대한 노출을 늘려 공유하는 정보를 늘리는 것이다.

# 12. transactional email
> 고객과의 주고받음이 있는 이메일을 지칭하는 말로, 고객의 ID를 찾아가는 과정이라던가, 이벤트에서의 당첨을 통한 응답 확인 등이 있다.

# 13. App exchange
>Salesforce에서 활용할 수 있는 앱들을 설치할 수 있는 마켓 스토어

# 14. MFA(Multiple Factor Authentication)
고객에게 암호 이외의 추가 정보를 입력하도록 요구하는 다중 단계 로그인 과정이라고 생각하면 됩니다. 예를 들어 비밀번호를 통한 로그인 이후 지문 인식을 통해서 사용자의 생체 정보를 추가로 인증 과정에 추가하는 방식을 우리는 MFA를 적용한 사례라고 할 수 있습니다.


### Journey Builder란?

고객 라이프 사이클을 관리하는 Marketing cloud의 기능. 즉, 고객이 브랜드에 대한 충성도를 고려, 구매, 사용 및 유지할 때 거치는 단계입니다. 

Journey builder는 마케터가 고객의 요구, 욕구 및 선호도, 인구 통계 및 행동을 기반으로 단계마다 상호 작용을 사용자 지정할 수 있도록 설계되었습니다.

> 고객이 생활하는데 있어서 이게 필요한 상황이구나를 먼저 파악해, 메시지를 보낸다거나 광고를 보여주는 등 상호작용을 하는 기능. 어떻게 게인마다 적절한 타이밍에 문구나 광고를 보여줄 수 있는 지 궁금한데 세일즈 포스는 이를 가능케 한다.

### features of salesforce

### 1. 다른 마케팅 클라우드와 통합되어 중복된 경험이 발생하지 않도록 조절
> Journey Builder는 Salesforce의 Sales Cloud와 Service Cloud와 통합되어 고객의 경험을 원할하게 만들고 모든 시스템의 정보가 다른 시스템과 공유되도록 합니다. 이러한 데이터 연계를 통해서 고객이 경험하는 마케팅 솔류션들이 중복되지 않고 헛되지 않게 도와줄 수 있음

### 2. 고객과의 일대일 마케팅으로 고객 맞춤형 서비스 및 관리를 할 수 있음

Joureny Builde의 접근 방식은 일대일 마케팅이라고도 하며 고객과의 개인화 된 상호 작용을 강조하는 CRM 전략으로, 고객 충성도를 높이고 마케팅 수익을 높일 수 있습니다. Journey Builder의 자동화를 통해 대규모 고객 기반을 위한 개인화된 관계를 더 쉽게 개발할 수 있습니다.

## Journey Builder Entry source
Salesforce 마케팅에서 고객의 journey를 시작은 Entry source를 통해서 시작된다. 이 Entry source는 다음과 같이 7개의 요소 중 하나이다.

> 1. Data Extension
> 2. API Event
> 3. Audience
> 4. CloudPage
> 5. Inbound Chat
> 6. Salesforce Data
> 7. Event


</br>

![Alt text](image.png)


### Data Extension
각 고객들의 아이디와 세부 정보들을 담은 테이블이라고 생각하면 좋을 것 같다. 다음 엑셀에세 보이듯이 journey든 email studio든 해당 테이블의 값들을 토대로 작업을 진행한다.

![Alt text](image-1.png)

### Data Extension 저장 위치
>Marketing cloud 내 테이블에 저장된 경우 Data extenstion을 Entry source로 사용 가능

### Data extenstion 특징
> 유연하게 사용이 가능하며 마케터가 가장 일반적으로 사용하는 진입 소스 중 하나
> Data extension Filter를 사용하며 Journey에 있는 연락처 중 일부에게만 notification 내지는 상호작용을 하거나, 전체에게 전송 가능
통제 가능
> 'Automation Studio'나 'MobileConnect'에서도 Data extension 사용 가능
- Restrictions: 실시간으로 반응해서 전송하는 것은 불가능
(ex> 비밀번호 찾기, 양식 제출, 영수증 전송 등)


### API Events
1. 저장 위치: 다른 플랫폼이나 시스템에 저장된 데이터를 기반으로 사용
2. 특징
* quick real-time trigger sends(실시간으로 즉각 전송)를 위해 만들어짐
* 제한사항: API가 한번에 하나의 레코드만 보낼 수 있기 때문에 일괄 전송은 불가능

예제>
* 이벤트에 당첨된 고객들에게 쿠폰을 전송하는 기능은 X
* 구매를 완료한 고객에게 영수증 발송 O


### Salesforce data
1. 저장 위치: Salesforce Sales Cloud 또는 Service Cloud CRM에서 생성 또는 수정된 레코드를 기반으로 수신 목록을 생성하는데 사용
2. 3가지 Entry Source Options
* 


### Cloud Page

salesforce에서 자체적으로 만들 수 있는 <U>노코딩 페이지 개발도구</U>다. 아트 리소스만 가지고 있다면 간단한 페이지를 만들 수 있다고 생각하면 된다.

![Alt text](image-2.png)
처음에 이해한 내용은 이러한 퀵 팝업만 만들 수 있다고 생각했지만...

![Alt text](image-3.png)
다음과 같이 전체 페이지도 개발 가능하다.

