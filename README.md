# aws_instance

t4g.small -> vCPU 2, 메모리 2gb, 5Gbps Burst, EBS Burst 2,085Mbps (볼륨 16gb일시 3.33초 / 20gb일시 3.492초)
<br/>
t4g.nano -> vCPU 2, 메모리 0.5gb, 기타 스펙 동일 (3.09초)
<br/>
t2.micro -> vCPU 1, 메모리 1gb, 네트워크/EBS = Unknown (3.08초)

### T 유형 (t4g nano, micro, small)
t2.micro, 32GB, 64(x86) : 3.086초 
<br/>
t4g.nano, 16GB, arm64 : 3.09초 
<br/>
t4g.micro, 16GB, arm64: 3.277초 
<br/>
t4g.small, 16GB, arm64 : 3.32초 
<br/>
t4g.small, 20GB, arm64 : 3.492초
<br/>
<br/>

### M 유형 (m6g medium, large)
m6g.large, 16GB, arm64 : 3.081초
<br/>
m6g.medium 16GB arm64 : 3.212초
<br/>
<br/>

### 전체
m6g.large, 16GB, arm64 : 3.081초
<br/>
t2.micro, 32GB, 64(x86) : 3.086초 
<br/>
t4g.nano, 16GB, arm64 : 3.09초 
<br/>
m6g.medium 16GB arm64 : 3.212초
<br/>
t4g.micro, 16GB, arm64: 3.277초 
<br/>
t4g.small, 16GB, arm64 : 3.32초 
<br/>
t4g.small, 20GB, arm64 : 3.492초

### 성능 결과 이유
1. 프로그래밍을 멀티쓰레딩이 안되게 짰다
2. T 인스턴스는 burst 계열로, 기존엔 성능이 제한되어있지만 그 이상의 성능이 필요한 경우에 크레딧을 소모하며 더 높은 성능을 사용할 수 있다고 하는데, 코드가 요구하는 성능이 nano의 베이스라인 ~ small의 베이스라인 사이여서 nano에서만 burst가 가동되었다

<br/>
<br/>
정희수, 한다현, 허상진

