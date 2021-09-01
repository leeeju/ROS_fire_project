
안녕하세요? 저는 군용 드론 제작을 희망하는 개발자 지망생입니다,
감시장비 운용 경력을 살려 감시용 드론의 제작을 희망합니다.

본 프로젝트는 대전 인력개발원의 [ROS 기반 자율주행 드론 개발자 과정]을 통하여 수료한 프로젝트 입니다.


# 프로젝트 이름 : 화재탐지 드론
# 프로젝트 수행 기간 : 2021. 07. 01 ~ 09. 08

사용 기술 요약 : Open_CV와 머신러닝(cascade)을 활용한 객체 감지 기술 입니다.

project 요약 설명 : 신고를 받은 드론이 화재지점으로 날아가 순찰 모드를 활성화 시키고 화재를 탐지시 경고 알람과 문자(좌표)를 사용자에게 보내줍니다.
                   사진은 실시간 으로 켑쳐되어 컴퓨터에 저장 되고 초기진화 시도를 위한 소화탄을 낙하 후 복귀합니다.

개발환경 : Ubuntu 18.04 , R.O.S_melodic

시뮬레이션 환경 : Gazebo
                      
더 많은 관련 사진은 좌측 상단의 < lssues > 를 참고 해 주세요.

자세한 내용은 안의 보고서와 youtube를 참고해주세요.

YuTube -- > "https://www.youtube.com/channel/UCLSgng38L1zVYUgOHEe1yOg/videos"

# 필요성
전세계적으로 화재의 피해가 급증하고 있다. 2021년 그리스, 터키, 이탈리아, 알제리 등에서는 산불이 발생하여 매우 큰 재산과 인명의 피해를 입혔고, 그리스 에비아 섬은 8월 3일날 발생한 화재로 서울시 면적의 80%에 달하는 면적이 불탔다. 터키 안탈리아주에서 시작된 불은 해당 지역에 평년보다 8배 넓은 지역을 불태우기도 했다(노예진, “’특파원보고 세계는지금’기후변화로 인한 섭씨 50도의 폭염...최악의 산불”; “화마가 덮친 남유럽, 통제불능 기후변화”). 전문가들은 그 주요한 원인 중 하나로 기후변화를 꼽고 있다. 즉, 일시적인 것이 아니라 지속적으로 우리가 마주하고 대처해야 할 재난 중 하나가 바로 화재라는 것이다.

![q](https://user-images.githubusercontent.com/84003327/131607812-e5cb0372-b17c-485b-8bdb-13fd8c974523.png)

이처럼 막대한 재산 및 인명 피해를 발생시키는 화재사건을 초기에 진압하기 위하여 협소 공간 및 위험 지역에 빠르게 접근하며 화재를 식별하고 더불어 초기진화 시도를 위한 소화탄 낙하를 시도 함으로 대현 화재의 발생을 막는 효과를 가져올 것입니다. 

또한 드론의 활용분야는 수색(51%), 재난 및 화재 모니터링(35%), 운송(14%) 순으로 가장 많이 이용되는 것으로 나타났다. 첫째, 수색 연구분야에서는 인력을 통한 수색업무에 비해 드론을 활용하는 것이 시간, 비용 등의 측면에서 효율적인것으로 나타났다. 둘째, 재난 및 화재 모니터링분야에서는 드론을 통해 화재 현장을 실시간으로 분석함으로써 신속한 재난현장파악에 도움이 되는 것으로 확인되었다. 셋째, 운송분야의 연구에서는 구조 물품과 구호 용품, 비상 의약품 등을 빠른 시간에 운반하여 응급 상황에서의 골든타임을 확보할 수 있는 것으로 판단 됩니다.


# 사용 알고리즘
![ff](https://user-images.githubusercontent.com/84003327/131608391-6c4307f9-928f-4680-8425-be5165bc3eac.png)

드론은 목표지점으로의 이동을 위한 G.P.S코드가 있습니다. 위성을 통해 제공받은 G.P.S 정보를 바탕으로 드론이 이동하여야 하는 지점을 특정할 수 있습니다. 저희 팀에서는 많은 실험을 통하여 이동간 오차 범위와 속도 등의 최적의 컨트롤 값을 얻을 수 있었습니다. 

또한 드론이 탐색, 정렬간 북쪽을 바라보도록 설정하였는데 이를 통해 드론의 위치도 지도상의 정확한 사방위를 쉽게 파악할 수 있게 되었습니다.

또한 cv_bridge를 사용 하여 R.O.S환경에서 Open_CV를 사용할 수 있게 만들었으며, 코드에cascade Data를접목시켜 화재인식의 대한 성능을 향상 시켰습니다.

cascade Data란? 화면상의 오브젝트를 사용자가 지정한 것으로 특정지어 컴퓨터가 학습 후 추적 할 수 있게 만든 .xml 파일로 Open_CV에서 물체를 추적하는데 사용되는 기본적인 데이터입니다.


# 결과 화면
![img_fire](https://user-images.githubusercontent.com/84003327/131607360-730ae13d-a02d-4515-8e73-5fca24717e04.png)

![m4](https://user-images.githubusercontent.com/84003327/131608551-e0af671f-dca0-4183-b1b2-aa9ae668827e.png)



감사합니다. 

my e-mail : 02stu4@gmail.com




