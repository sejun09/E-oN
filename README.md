# E-oN
## 실시간 영상처리를 이용한 자동신호 제어 시스템

### Overview
### 실시간 영상처리를 이용한 자동 신호제어 시스템 
--------------------------------------------------------------------------
## 배경 및 필요성 
 고령자, 휠체어를 이용하는 장애인들의 평균 보폭은 일반 성인의 보행속도를 기준으로 만들어진 횡단 신호의 시간이 부족한 경우가 많다. 
횡단 시간이 부족한 사람들은 제시간에 도착하기 위해 신호가 바뀌기 전 미리 출발하거나, 좌 우를 살피지 않고 안전이 확보되지 않은 상황에서 횡단을 하다 
사고가 발생하는 악순환이 발생한다. 따라서 보행속도가 느린 노약자 및 장애인들을 위한 자동신호제어 시스템을 통해 횡단보도에서 발생하는 교통사고를 
예방하고자 한다. 

 또한 신호 교차로 사고 10건 중 2건은 우회전 상황에서 발생하고 있다. 현재, 차량 운전자의 시야에서는 보행자 신호가 보이지 않고 있기 때문에 운전자가
볼 수 있는 시각적인 시스템과, 보행자가 있음을 명확하게 알려줄 시스템이 필요하다.  


## 주요 기능

1. 실시간 영상처리를 이용하여 보행자의 상황을 판단 및 횡단 신호 조절 
2. 보행자의 무리한 횡단 감지 시 위험 알림 및 무단횡단 제지
3. 운전자에게 보행자가 건너고 있음을 인지하게 해 줌 (시각적인 표현)
4. 교차로에서 우회전 시 운전자에게 보행자 신호인지, 보행자가 있는지 알려줄 시스템 

## 설계 내용 

1. 횡단보도에서의 안전
   1. openCV와 deep learning을 이용한 보행자의 상황 판단
   2. 상황에 따라 횡단 신호를 추가하고, 보행자가 안전하게 횡단할 수 있게끔 보조 
   3. 무리한 횡단 시 위험성 알림 및 제지 

2. 차량 운전자의 우회전 시 안전 
   1. 보행자신호를 운전자도 볼 수있게끔 시각적인 표현 
   2. 횡단보도에 보행자가 있음을 운전자에게 알려주는 시스템 설계    


## 시스템을 만들면서 고려해야 할 점 

1. 신호등을 제어하면서, 교통의 흐름을 방해하는 것에 대한 해결책
2. 일반 보행자가 이 시스템을 악용해서 횡단을 시도할 경우
3. 보행대기 상태에서 휠체어 or 목발 or 보행보조기를 이용하는 사람을 미리 구분
4. 횡단시간을 추가하는 것을 넘어 어떻게 보행자를 확실하게 보호할 수 있는 시스템을 만들 것인가?

### Development Environment

이 프로젝트를 하려면 어떤 개발 환경이 필요한지

---------------------------------------------------------------------------

### Build and Run

빌드와 실행은 어떻게 하면 되는지

---------------------------------------------------------------------------

### Manual

실행 후 사용 방법에 대한 내용

---------------------------------------------------------------------------

### License

라이선스 조항은 어떻게 되는지

---------------------------------------------------------------------------

### Contributing

기여하려면 어떤 조건과 방법으로 해야 하는지

---------------------------------------------------------------------------

### Known issues
![image](https://user-images.githubusercontent.com/68588772/114360011-86ea0d80-9baf-11eb-8548-9e852578411f.png)
고령자, 휠체어를 이용하는 장애인들의 평균 보행속도는 일반 성인의 보행속도보다 느리기 때문에 일반 성인의 보행속도를 기준으로 만들어진 횡단 신호의 시간이 부족할 경우가 많다.
