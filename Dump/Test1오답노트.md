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

# 6 Cloud admin이 Sales cloud Object를 동기화하고 leveraged(활용)하기 위해서 데이터를 구성하기 위해서는 어디로 가야 할까요?
Setup -> Data Management -> Synchronized Data Extenstions

오답: 
Contact Builder -> Data Sources 이 방식은 외부의 데이터를 연관짓기 위해서 찾아가는 방식이다.

Contact Builder -> Data Extensions ->Synchronized Data extensions
해당 방식은 Sales cloud Object를 편집하기 위한 탐색이지 구성하기 위한 탐색방식이 아니다.

# 7 





