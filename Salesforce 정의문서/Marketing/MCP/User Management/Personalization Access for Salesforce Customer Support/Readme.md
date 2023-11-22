# Personalization Access for Salesforce Customer Support
고객의 데이터에 접근할 때 admin은 이에 대해서 높은 잣대를 가지고 권한을 부여 해야 한다. 이 파트에서 배우는 것은 고객 데이터를 접근하는 여러 권한에 대해서 알아볼 예정이다.

admin이 사용작에게 권하을 줄 때 권한에 대한 유효 기간을 설정할 수 있다. 유효기간을 설정하면, 해당 유효기간에 지났을 경우 권한은 소멸되며 이에 대한 갱신을 admin한테 재요청해야 한다.

## 권한을 부여하는 인터페이스
지원 팀에게 권한을 제공해서 admin의 업무를 도울 수 있다. 권한을 주기 위해서는 다음과 같은 권한이 필요하다.

> Administrator permission

이 권한을 가지고 있다면 다음과 같이 절차를 진행하면 된다.

1. 왼쪽의 메인 네비게이션 파트에서, <b>Security &rightarrow; Grant Access</b>
로 이동한다.

2. 지원 팀의 계정을 선택해 <br>
&nbsp;&nbsp;&nbsp;2-1 days, week, month, year를 입력해 해당 권한의 유효기간을 설정한다.<br>
&nbsp;&nbsp;&nbsp;2-2 권한을 승인한 시점부터 카운트 다운은 시작된다.

3. click Grant

## 직원 개인에게 권한을 제공하는 인터페이스
1. 직원에게 권한을 주어 구성, 지원, 전략 수립을 하는데 협업을 진행할 수 있다. 직원의 권한 또한, support와 마찬가지로 기한과 역할을 기준에 따라 부여 할 수 있다.

권한을 주기 위해서는 
> Administrator permission

1. 메인 내비게이션에서 Security &rightarrow; Grant access
2. 추가를 하려는 직원의 아이디를 선택하고 <b>add Success Manager</b>를 사용한다.
3. 액세스를 필요로 하는 각 직원의 이메일을 기입한다.
4. 권한의 유효기간이 지나면 최대 1년까지 연장할 기한을 추가로 입력한다.
5. 계정의 권한 하에, account admin을 선택해 계정에 대한 모든 개입을 할 수 있는 권한을 부여하거나 특정 dataset을 조회할 수 있게끔 설정한다.

