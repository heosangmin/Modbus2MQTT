# Modbus to MQTT
## 개요
- Modbus의 TCP 프로토콜로 기기에서 데이터를 읽고 MQTT에 publish하는 중계 프로그램입니다.
- 현재 Enapter사의 Electrolyser 버전 2.1을 기준으로 작성 중입니다.

## 설정 파일
### modbus-sample.properties
- MQTT 서버, Modbus 기기 정보를 입력합니다.
- 기본 경로는 `/etc/modbus-sample.properties`이지만 `Sample.java`의 `CONFIG`의 값을 변경해도 됩니다.

### EnapterElectrolyser.json
- 기기의 레지스트리 정보를 json으로 저장합니다.
- `EnapterElectrolyser.json`는 [EL21のmodbus_tcp_communication_interface](https://handbook.enapter.com/electrolyser/el21_firmware/1.8.1/modbus_tcp_communication_interface.html)의 문서로부터 변환한 데이터입니다.

## 환경
### Java
JDK1.8+

### 필수 라이브러리
- [EashModbusJava](http://easymodbustcp.net/en/) : Modbus 클라이언트
- [Jackson](https://github.com/FasterXML/jackson) : Java JSON
- [Eclipse Paho](https://www.eclipse.org/paho/) : MQTT

## 작성 현황
- 2021/10/14
    - Modbus 기기（Enapter Electrolyser）의 Holding Register, Input Register로부터 값을 읽는 기능을 작성

