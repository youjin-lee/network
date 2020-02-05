---
title: "Method of Connection"
date: 2020-02-05 14:26:28 -0400
categories: network
---

### 1. role of PC = Host(AP), role of SENSOR = Client
<div>
  <br>
  </br>
  <img width="600" src = "https://user-images.githubusercontent.com/27392019/73799699-033dcf80-47fa-11ea-8e26-373eef145c5e.png">
</div>
 
 - PC가 서버(Host)가 되고, Sensor가 클라이언트가 되는 경우
 
 - **WiFi**
 1. Sensor에서 Port number 등을 공유기를 경유하여 PC에 전달 
 2. PC에서 Sensor가 접근할 수 있도록 TCP 서버 정보(AP:Access Point)를 공유기를 경유하여 제공
 3. Sensor에서 PC로 연결 (과정1,2는 서버 등록 과정에서만 필요)
 
 - **BLE**


---------------------------

### 2. role of PC = Client, role of SENSOR = Host(AP)
<div>
  <br> 
  </br>
  <img width="600" src = "https://user-images.githubusercontent.com/27392019/73799696-ffaa4880-47f9-11ea-8da0-8abf71765644.png">
 </div>

 - PC가 클라이언트가 되고, Sensor가 Server(Host, AP mode) 되는 경우
 
 - **WiFi**
 1. PC가 회로 연결을 통해 바로 Sensor에 접속
 
 - **BLE**
 
### :cherry_blossom: Decision : Method 1

<Advatage>
  - able to use internet
 
<Disadvatage>
  - more complicated than method 2.

### ect
- (python) **twisted** : tcp 경량화 프레임워크
- 주기 : 160ms + N/W

---

## :cacutus: TCP 서버/클라이언트 구조

PC에서 사용되는 대표적인 웹 클라이언트인 인터넷 익스플로러는 사용자가 입력한 주소를 참조하여 접속 대기 중인 웹 서버에 접속한 후, HTTP를 이용하여 요청 메시지를 보낸다. 웹 서버는 이 데이터를 분석한 후 HTTP를 이용하여 응답 메시지를 다시 보낸다. 익스플로러는 웹 서버가 보낸 데이터를 받아 화면에 표시한다. HTTP는 TCP에 기반한 프로토콜이므로 웹 서버/클라이언트는 대표적인 TCP 서버/클라이언트 애플리케이션이라고 할 수 있다.

### TCP 서버/클라이언트 동작 방식

1. 서버는 먼저 실행하여 클라이언트가 접속하기를 기다린다(**listen**).
2. 클라이언트가 서버에 접속(**connect**)하여 데이터를 보낸다(**send**).
3. 서버는 클라이언트 접속을 수용(**accept**)하고, 클라이언트가 보낸 데이터를 받아서(**recv**) 처리한다.
4. 서버는 처리한 데이터를 클라이언트에 보낸다(**send**).
5. 클라이언트는 서버가 보낸 데이터를 받아서(**recv**) 자신의 목적에 맞게 사용한다.

​```python
def print_hi(name):
  print("hello", name)
print_hi('Tom')
​```
