# Personalization Permission
> MCP를 사용하기 위해서는 Marketing Cloud에서 Personalization에 접근할 수 있게끔 권한을 허락 해 주어야 한다. 또 MCP를 운영하기 위해서는 MCP 유저들에게 역할을 부여해야 한다. Marketing Cloud 유저가 Personalization에 접속하는 순간 유저의 계정을 자동으로 만들어준다. 이후, admin은 해당 유저들에게 역할에 따라, role을 부여해서 dataset 접근에 대한 권한을 차별적으로 부여해야 한다.

Personalization 권란에는 다음과 같이 3가지 권한이 존재한다.
1. Marketing  Cloud Administrator: Personalization이나 Marketing cloud에 접속하거나 사용하는 유저들에게 권한을 설정할 수 있는 권한을 가지고 있음
2. Personalization User: Personalization admin이 권한을 주기 전까진 DataSet에 접근할 수 있는 권한을 가지고 있지 않지만 Marketing Cloud에서 Personalization 탭을 통해 접근이 가능하다.
3. Personalization Administrator: Marketing cloud admin 처럼 Maketing cloud 전체 유저에 대한 권한을 설정 할 수 없지만 Personalization에 접근하는 유저에 대해서는 권한을 설정할 수 있다.

## User Data Changes
> MCP가 접목된 유저의 서비스를 운영하는 소비자들은 당연히도, 자신들의 정보를 제한하고, 변형하고, 삭제를 요청할 수 있는 권리가 있다. 이에 대한 수신 동의를 진행했을 경우 MCP 유저는 Personlization의 REST API를 통해 token 교환 방식으로 데이터를 수정하거나 교환할 수 있다.

## SFTP Users and Files
> FTP 사이트를 사용한다면 사용자는 데이터를 전송하고 수신하는 과정을 보안이 설정된 환경에서 자동으로 송수신할 수 있다. SFTP 신뢰도 조회나 생성, 파일을 Personalization에서 편집할 수 있다.


## Two-Factor Authentication
> SAML을 사용하지 않는다면, 추가적인 보안 레이러를 기존의 보안에 덧씌어 Personalization을 보호할 수 있다.

