# Salesforce Level-up: The bulkification blueprint

![Alt text](image.png)

지속적으로 변화하는 세일즈포스 개발 환경에서, 효율성은 이제 단순한 필요조건이 아니다. 세일즈포스의 독특한 구조 뿐만 아니라 소비자들의 다양한 요구조건에 따라, 데이터가 최적화 되어야 하기 때문에, 이 개념이 필수적으로 환경에 들어오게 된다.

# Bulkification
> 뭉텅이화

<br>
<br>
bulkification은 한국어로 번역한 그대로 테이블의 데이터를 레코드 하나하나 처리하기 보다는 하나의 묶음 단위로 처리하는 것과 동시에 작업을 병렬적으로 처리하기 때문에 많은 데이터를 가진 테이블에 대한 비약적인 퍼포먼스를 가질 수 있다.  Bulkification을 시행한다면 DML, SOQL, API 호출등의 단계를 최소화할 수 있다. 이를 통해 <b>코드의 효율성과 세일즈포스 거버넌스의 기조에 준수할 수 있는 상태를 유지케 한다. </b>

# The need for Bulkification
> Bulkification의 필요성

핵심으로 가자면, Bulkification는 단지 데이터를 묶는 행위가 아니다. 효과적인 코딩으로 한정적인 하드웨어 리소스를 사용하는 우아한 테크닉이다. 정확하면서도, 건전한 세일즈포스의 governer제한 덕준에, API 호출을 최소화하면서 많은 데이터셋에 접근할 수 있게끔 해주면서, application의 성능을 극대화 해준다. 복잡한 trigger를 다루던, 배치 프로세스를 다루던, 데이터 통합 프로세스를 따르던, Bulkification은 확장성있고 성능에 최적화를 위한 키롤을 맡은 셈이다.

# Bulkification의 근본적인 원칙

## 레코드를 묶음으로 처리하기 위해서
* 설명: 1대 1로 레코드를 다 대응하기 보다는 묶어서 대응하기 때문에, 많은 데이터셋과의 작업에서 사용하기 적합

* 장점: Bulk를 사용하면 프로그램의 작업량과 API 호출량을 크게 줄일 수 있다. 또, governer의 용량 한계에 도달하는 것을 방지할 수 있다.

## SOQL과 SML 작업 최적화
* 설명: SOQL 쿼리문이나 DML(INSERT, Update, Delete) 작업을 진행하는데 있어서 각 레코드에 1대 1로 대응하기 보다는 묶음 단위로 작업을 진행할 수 있다.

* 장점: This approach reduces the total number of database queries and DML operations that take place in a single transaction, conserving system resources and avoiding collisions with Salesforce governor limits.

https://force.land/salesforce-level-up-the-bulkification-blueprint-0fcfb39c0b18