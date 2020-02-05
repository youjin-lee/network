---
title: "Method of Connection"
date: 2020-02-05 14:26:28 -0400
categories: network
---

### 1. role of PC = Host(AP), role of SENSOR = Client
<div>
  <br>
  <img width="600" src = "https://user-images.githubusercontent.com/27392019/73799699-033dcf80-47fa-11ea-8e26-373eef145c5e.png">
  </br>
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
  <img width="600" src = "https://user-images.githubusercontent.com/27392019/73799696-ffaa4880-47f9-11ea-8da0-8abf71765644.png">
  </br>
</div>

 - PC가 클라이언트가 되고, Sensor가 Server(Host, AP mode) 되는 경우
 
 - **WiFi**
 1. PC가 회로 연결을 통해 바로 Sensor에 접속
 
 
 - **BLE**


--------------------------

### Decision : Method 1

[Advatage]

  - able to use internet
 
[Disadvatage]

  - more complicated than method 2.

### ect

- (python) **twisted** : tcp 경량화 프레임워크
- 주기 : 160ms + N/W
