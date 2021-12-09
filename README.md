# DingDone : Fire Detecting Autonomous Drone

<img src="https://user-images.githubusercontent.com/70934572/145342654-716af606-1b4f-486d-861b-c42913437a2b.png" width="300" >


### BanBanBank Organization

https://github.com/Ewha-BanBanBank


### 프로젝트 레포지토리 정리

https://github.com/Ewha-BanBanBank/DingDone_Start/tree/main/Path%20Planning : Path Planning repository

https://github.com/Ewha-BanBanBank/DingDone_Start/tree/main/Object%20Detection : Object Detection repository

https://github.com/Ewha-BanBanBank/DingDone_Start/tree/main/Classification : Classification repository



### 프로젝트의 목적

산림청에 따르면 2020년 산불로 인한 피해액은 1581억원이고, 서울시 중구 크기만큼의 면적이 피해를 받는다. 
또한 경사도가 높고 풍속이 높을수록 화재 확산 속도가 증가하고, 산의 경우 두 경우에 해당하는 지형이므로 산불의 확산속도는 다른 화재보다 훨씬 빠르다. 
따라서 화재의 초기 진압 및 대처가 중요하고, 초기 진압을 빠르게 하려면 화재를 빨리 발견하는 것이 제일 중요하지만 기존의 소방 시스템은 신고를 받으면 화재 진압을 위해 출동하므로 화재를 빨리 진압하기 매우 어렵고 대형 산불로 이어지기 쉽다. 

이를 막기 위해서는 산불 발생 유무를 신고에 의존하지 않고 산불을 빨리 감지할 수 있어야 한다. 
신고에 의존하지 않고 CCTV를 통해 산불 발생 유무를 미리 발견할 수는 있겠지만 모든 CCTV를 사람이 항상 보고 있을 수도 없고, CCTV가 사각지대 없이 모든 곳에 설치되어 있지 않기 때문에 이 역시 초기 진압하기에는 한계가 있다.
따라서 항상 감시하여 빨리 화재를 탐지하고 진압할 수 있는 서비스 제공이 필요하다. 

우리 팀의 자율주행 산불 탐지 드론은 24시간 사람의 세부적인 조종없이 주행이 가능하고 산불을 드론과 컴퓨터에서 2번 인식하여 산불을 정확하게 인식하고, 감지한 산불의 위치를 소방서로 전송하여 빠른 화재 진압을 가능하게 한다.




### 프로젝트 시나리오

1. 자율주행 도중 산불인식 : 드론이 산 근처를 자율주행을 하며 산불 발생 유무를 Object Detection을 통해 확인 
2. 영상전송 : 드론에서 산불을 인식하면 드론이 산불이 발생한 곳 주변으로 경로를 수정하여 화재 영상을 촬영하여 실시간으로 컴퓨터에 영상을 전송
3. 산불인식(이중) 및 드론 위치파악 : 드론에게 받은 영상에서 Classification을 통해 산불이 발생하였는지 정확하게 판단하고 산불이 발생한 위치를 파악
4. 산불위치 및 영상 전송 : 산불이 발생한 위치와 산불 발생 영상을 실시간으로 사용자의 어플리케이션에 전송
5. 산불 발생 영상 및 위치 확인 : 사용자는 어플리케이션을 통해 산불 발생 영상과 산불이 발생한 위치를 확인



### 프로젝트 예상 아키텍처

<img src="https://user-images.githubusercontent.com/70934572/145341167-3612f1b3-9759-4f48-a208-f872169dad0e.png" width="600" >

