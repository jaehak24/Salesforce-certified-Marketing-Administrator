# ChatterGroup

salesforce를 사용하게 되면 팀원들과 목표와 관련된 파일 OR 관련 정보들을 받아 볼 수 있는 그룹을 만들 수 있는데 이를 ChatterGroup이라고 부른다.

## ChatterGroup의 권한
* Public: 누구나 해당 그룹에 참여, 수정, comment를 할 수 있다.
* Private: 그룹 멤버엔 한해서만 파일 수정, 추가, comment가 가능, 그룹을 완전하게 비공개로 만들려면 그룹을 Unlist로 하면 된다. "Modify all data" 또는 "View all data" 권한을 가지는 사용자는 그룹의 posts, comments와 파일을 볼 수 있다. 
"Manage all Data" 권한을 가지는 사용자는 private group에 별도의 권한 허가 없이 참여 할 수 있고 그룹의 설정을 변경할 수 있다.

* Unlisted: "Manage all Data" 권한을 가진 사람들만 posts, comments, file을 추가 할 수 있다. 해당 그룹에는 참가 요청을 신청 할 수 없고 관리자 OR 매니저가 해당 그룹 초대를 했을 경우에만 참여를 할 수 있다. 해당 그룹에 참여하지 않는 멤버는 해당 그룹을 그룹 리스트에서 볼 수 없을 뿐만 아니라, 피드, 검색 에서도 조회 할 수 없다.

* Groups with customer: private과 unlisted 그룹 같은 경우 고객을 해당 그룹에 참여 시킬 수 있다. 고객을 그룹에서 구분시키기 위해서 Salesforce Classic의 좌측 상단의 그룹 포토를 통해서 가능하다.또한, Lightninig Experience의 그룹 헤더의 자막을 통해서 식별이 가능하다.


<img src="private with customers.png" width="400" height="200"  ></img>

