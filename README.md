=====================

##10. 구성요소 상세 설계##
---------------------

: --:1) 단말기 : 초기에 지도를 다운로드 받습니다(설치 시). 첫 화면에 나의 위치를 지도에 띄우고 목적지를 입력받도록 합니다. 

2) gps모듈 : 위성으로부터 나의 위치를 gps수신기를 통하여 입력 받습니다. 입력 받은 위치를 첫 화면 지도상에 표기합니다. 이 때 지도상에 표기하는 모듈도 구동이 됩니다.

3) 알고리즘A 모듈(?)1. 버스 모듈 : 버스 회사 서버로부터 버스들의 정보를 받는 모듈이 필요합니다. 출발지출부터 가장 가까운 정류장의 위치를 찾아내며 그 정류장에서 목적지로 가는 가장 빠른 버스를 탐색합니다. 그러나 여기서 버스를 기다리는 시간과 운행 시간의 합을 더하여서 시간이 가장 적게 걸리는 코스를 우선적으로 출력해 냅니다.

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%98.PNG)



2. 출력 모듈 : 이 때 출발지로부터 목적지까지 버스의 코스를 추적하여 선으로 이어주는 즉 코스를 출력해주는 모듈이 필요합니다.

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%982.PNG)


4) NFC/QR코드 모듈 : 정류소에 달려있는 NFC송신칩을 통하여 버스 정보를 나의 핸드폰으로 보냅니다. 일반적으로 우리가 사용하는 NFC를 구동하게 하는 모듈이 필요하되 그 기능으로 실시간 버스 정보를 더 정확하게 받을 수 있습니다.

5) 알고리줌B 모듈
  1. 알고리즘A와 비교 : 알고리즘 A를 통하여 출력된 코스와 현제 NFC를 찍었을 때 시간상으로 맞다면 그대로 두지만 버스를 놓쳤다거나 더 빨리 도착하여서 다른 버스를 탈 수 있게 되었다면 다시 알고리즘A를 돌립니다.
  2. 알람 모듈 : 일정 시간이 지나서 원래 탑승해야 했던 버스를 놓치게 된다면 알람 모듈이 새로운 데이터를 받아 새로운 경로를 출력한다는 알림을 해줍니다.

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%983.PNG)

##10. 시스템 구현에 필요한 기술&구현 환경##

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%984.PNG)

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%985.PNG)

![picture](https://github.com/dlatpwjd26/planets/blob/master/%EC%BA%A1%EC%B2%986.PNG)
