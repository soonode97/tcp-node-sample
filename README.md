# tcp-node-sample
tcp-game-training 프로젝트용 샘플 유니티코드

샘플이 있기 때문에 코드 부분만 따로 올린 상태입니다.

샘플 링크는 아래에 있습니다.

https://github.com/Ho-yeong/node5_unity_sample/tree/main


## 작업 내용

### 1. NetworkManager.cs

- 핑 패킷을 보내는 함수 정의 SendPingPacket()
- 핑 요청 시, 핑 패킷을 전달하는 핸들러 정의 HandlePingPacket()
- LocationUpdateResponse 시리얼라이징
- INIT(0) 핸들러에 따른 응답 시, locationData(마지막 위치) 받아서 GameStart() 메서드에 인자로 전달

### 2. GameManager.cs 

- GameStart() 메서드에서 플레이어 생성 전 시작 위치를 세팅하도록 함. `player.transform.position = new Vector2(x, y);`