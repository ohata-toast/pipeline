## Dev Tools > Pipeline > 콘솔 사용 가이드 > 배포 대상 모니터

### 배포 대상 모니터링

Pipeline으로 배포하여 생성된 결과물들을 **배포 대상 모니터링** 메뉴에서 확인 할 수 있습니다.

## 배포 대상

**배포 대상 모니터링**에서 **배포 대상**은 Pipeline으로 Kubernetes에 배포한 워크로드를 확인 할 수 있는 페이지 입니다.
![deploy-target-monitoring-guide-01.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-01.png)
배포한 워크로드의 모든 목록과 워크로드 이름 및 해당 워크로드에 속한 파드의 수와 상태가 노출됩니다.
검색어 입력 후 검색 버튼 클릭시 입력한 문자열로 배포 대상을 검색합니다.
배포 대상 테이블에서 **배포 대상 이름**을 클릭하면 선택한 배포 대상에 속한 워크로드들을 확인 할 수 있는 페이지로 이동합니다.

![deploy-target-monitoring-guide-02.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-02.png)
선택한 배포 대상 클러스터의 네임스페이스 중 Pipeline으로 배포한 워크로드들의 네임스페이스가 노출됩니다.
검색어 입력 후 검색 버튼 클릭시 입력한 문자열로 네임스페이스를 검색합니다.
네임스페이스 선택시 선택한 네임스페이스에 속한 워크로드 목록이 노출됩니다.

![deploy-target-monitoring-guide-03.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-03.png)
워크로드에 속한 파드의 갯수와 현재 동작중인 파드가 %로 표시됩니다. 워크로드 선택시 선택한 워크로드의 파드의 목록이 나타나며 동작 상태를 왼쪽의 점의 색으로 확인 할 수 있습니다.
선택한 워크로드 및 파드의 기본정보가 오른쪽에 노출됩니다.


왼쪽 점의 색에 따른 파드의 상태

| 색깔 | 상태   |
| --- |------|
| 초록 | 실행중  |
| 빨강 | 정지   |



![deploy-target-monitoring-guide-04.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-04.png)
파드를 선택한 경우 콘솔 로그 및 연결된 서비스의 정보도 확인 할 수 있습니다.
파드 중 서비스와 연결된 파드의 경우 우측에 보이는 로드밸런서 아이콘이 생성됩니다. 로드밸런서 아이콘 선택시 **네트 워크**탭으로 이동합니다.

**배포 대상 모니터링**에서 서비스와 연결된 워크로드를 확인하기 위해서는 Manifest에서 셀렉터를 지정하는것이 아니라 'traffic.spinnaker.io/load-balancers' 어노테이션을 추가하여야 확인 하실 수 있습니다.

![deploy-target-monitoring-guide-08.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-08.png)

## 네트 워크

**배포 대상 모니터링**에서 **네트 워크**는 Pipeline으로 Kubernetes에 배포한 서비스를 확인 할 수 있는 페이지입니다.

![deploy-target-monitoring-guide-05.png]( ..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-05.png)
배포한 서비스들의 모든 목록과 서비스에 연결된 파드의 수 및 상태가 노출됩니다.
검색어 입력 후 검색 버튼 클릭시 입력한 문자열로 배포 대상을 검색합니다.
배포 대상 테이블에서 **배포 대상 이름**을 클릭하면 네임스페이스 선택 페이지로 이동합니다.

![deploy-target-monitoring-guide-06.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-06.png)

선택한 배포 대상 클러스터의 네임스페이스 중 Pipeline으로 배포한 서비스들의 네임스페이스가 노출됩니다.
검색어 입력 후 검색 버튼 클릭시 입력한 문자열로 네임스페이스를 검색합니다.
네임스페이스 선택시 선택한 네임스페이스에 속한 서비스들의 목록이 노출됩니다.

![deploy-target-monitoring-guide-07.png](..%2Fimages%2F2023-06-27%2Fdeploy-target-monitoring-guide-07.png)

서비스를 선택하면 서비스에 속한 워크로드 목록이 노출됩니다. 워크로드 선택시 선택한 워크로드의 정보가 **배포 대상**탭에서와 같이 오른쪽에 노출됩니다. 