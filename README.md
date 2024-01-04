# aws_instance

정희수, 한다현, 허상진

### T 유형 (t4g nano, micro, small)
<img width="492" alt="BBE0EAC9-0E59-4FEE-BBC2-7C1FE660487E" src="https://github.com/heeeesoo/aws_instance/assets/73633272/19937fb0-2fd2-4e7c-8455-de48cae475c8">
<br/>


### M 유형 (m6g medium, large, xlarge)
![BFFAD24D-0C24-4EF6-80B4-D02E7B746EB0_4_5005_c](https://github.com/heeeesoo/aws_instance/assets/73633272/85b645e8-5857-47ae-bcdd-8b142573cccf)
<br/>


### 성능 결과 이유 추론
1. T 인스턴스는 burst 계열로, 기존엔 성능이 제한되어있지만 그 이상의 성능이 필요한 경우에 크레딧을 소모하며 더 높은 성능을 사용할 수 있다고 하는데, 코드가 요구하는 성능이 nano의 베이스라인 ~ small의 베이스라인 사이여서 nano에서만 burst가 가동되었다. 
2. 일정 성능 이상 확보하면 실행 시간은 비슷하지만 cpu 사용률은 더 낮아진다.

CPU 사용률
<br/>
<img width="187" alt="KakaoTalk_Photo_2024-01-05-08-47-32" src="https://github.com/heeeesoo/aws_instance/assets/73633272/a5000bd6-5387-4400-a515-05cabb1d6599">



<br/>
<br/>


