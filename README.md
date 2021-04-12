# E-oN
## 실시간 영상처리를 이용한 자동신호 제어 시스템

### Overview
### 실시간 영상처리를 이용한 자동 신호제어 시스템 
--------------------------------------------------------------------------
#### 배경 및 필요성 
 고령자, 휠체어를 이용하는 장애인들의 평균 보폭은 일반 성인의 보행속도를 기준으로 만들어진 횡단 신호의 시간이 부족한 경우가 많다. 
횡단 시간이 부족한 사람들은 제시간에 도착하기 위해 신호가 바뀌기 전 미리 출발하거나, 좌 우를 살피지 않고 안전이 확보되지 않은 상황에서 횡단을 하다 
사고가 발생하는 악순환이 발생한다. 따라서 보행속도가 느린 노약자 및 장애인들을 위한 자동신호제어 시스템을 통해 횡단보도에서 발생하는 교통사고를 
예방하고자 한다. 

 또한 신호 교차로 사고 10건 중 2건은 우회전 상황에서 발생하고 있다. 현재, 차량 운전자의 시야에서는 보행자 신호가 보이지 않고 있기 때문에 운전자가
볼 수 있는 시각적인 시스템과, 보행자가 있음을 명확하게 알려줄 시스템이 필요하다.  


#### 주요 기능

1. 실시간 영상처리를 이용하여 보행자의 상황을 판단 및 횡단 신호 조절 
2. 보행자의 무리한 횡단 감지 시 위험 알림 및 무단횡단 제지
3. 운전자에게 보행자가 건너고 있음을 인지하게 해 줌 (시각적인 표현)
4. 교차로에서 우회전 시 운전자에게 보행자 신호인지, 보행자가 있는지 알려줄 시스템 

#### 설계 내용 

1. 횡단보도에서의 안전
   1. openCV와 deep learning을 이용한 보행자의 상황 판단
   2. 상황에 따라 횡단 신호를 추가하고, 보행자가 안전하게 횡단할 수 있게끔 보조 
   3. 무리한 횡단 시 위험성 알림 및 제지 

2. 차량 운전자의 우회전 시 안전 
   1. 보행자신호를 운전자도 볼 수있게끔 시각적인 표현 
   2. 횡단보도에 보행자가 있음을 운전자에게 알려주는 시스템 설계    


#### 시스템을 만들면서 고려해야 할 점 

1. 신호등을 제어하면서, 교통의 흐름을 방해하는 것에 대한 해결책
   - 신호 주기를 최대한 짧게 하는 알고리즘 구현하여 적용
2. 일반 보행자가 이 시스템을 악용해서 횡단을 시도할 경우
   - 판단 기준 설립 후, 기준을 넘는 보행자 발생 시 경찰에게 영상과 함께 신고 기능
3. 보행대기 상태에서 휠체어 or 목발 or 보행보조기를 이용하는 사람을 미리 구분
   - 휠체어, 목발, 보행보조기 객체를 구분하여 보행자 객체에게 속성 적용
4. 횡단시간을 추가하는 것을 넘어 어떻게 보행자를 확실하게 보호할 수 있는 시스템을 만들 것인가?


--------------------------------------------------------------------------

### Development Environment

##### 1. Git & Git Hub
다수의 팀원 간 협업이 필요한 프로젝트 이므로, 분산버전관리시스템(DVCS)인 Git과 웹 호스팅서비스인 Git Hub를 이용해 프로젝트의 분업과 수정을 용이하게 하고, 진행상황을 공유한다.

##### 2. Open CV
실시간 이미지 프로세싱 중심의 라이브러리인 Open CV를 이용하여 보행자 객체를 추출한다.

##### 3. Deep Learning
Open CV만으로 추출되지 않는 형태의 보행자는 Deep Learning을 통해 보완하여 추출한다.

##### 4. Visual Studio
프로젝트의 메인코드는 Visual Studio의 Python을 이용해 작성한다. 필요하다면 C, C++, Java등도 사용한다.

---------------------------------------------------------------------------

### Build and Run
##### 1. Arduino IDE
아두이노를 사용하기 위해 전용 IDE를 설치하고, 빌드 및 실행한다.

##### 2. Visual Studio / Eclipse
전용 IDE를 필요로 하지 않는 코드에 대해서는 비쥬얼 스튜디오 혹은 이클립스를 이용해 빌드 및 실행한다.

---------------------------------------------------------------------------

### Manual

실행 후 사용 방법에 대한 내용
# manual
## Process
보행자 진입 시도 시
1. 보행자 진입
2. 운전자 신호등에 보행자 신호 켜짐
3. 객체에 따른 보행자 진입 시간 조절
4. 보행자 신호등에 추가된 시간 알림
보행자 진입 X
1. 보행자 없는것을 인식
2. 보행자 신호 시간을 최적 시간으로 줄여 차량의 지연 시간 줄임
---------------------------------------------------------------------------

### License

라이선스 조항은 어떻게 되는지

Copyright <2021> <COPYRIGHT HOLDER>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---------------------------------------------------------------------------

### Contributing
1. sejun0926@naver.com로 메일 보내주세요!
2. issue를 사용해주셔도 좋습니다!

---------------------------------------------------------------------------

### Known issues
![image](https://user-images.githubusercontent.com/68588772/114360011-86ea0d80-9baf-11eb-8548-9e852578411f.png)
1. 고령자, 휠체어를 이용하는 장애인들의 평균 보행속도는 일반 성인의 보행속도보다 느리기 때문에 일반 성인의 보행속도를 기준으로 만들어진 횡단 신호의 시간이 부족할 경우가 많다.

![image](https://user-images.githubusercontent.com/68588772/114361995-cc0f3f00-9bb1-11eb-8760-668373ebfc78.png)

2. 신호 교차로 사고 10건 중 2건은 우회전 상황에서 발생하고 있다. 현재, 차량 운전자의 시야에서는 보행자 신호가 보이지 않고 있기 때문에 사고가 발생한다. 지난달에도 화물차와 래미콘이 우회전을 하던 중에 아이를 발견하지 못해서 사고가 발생하였다.
