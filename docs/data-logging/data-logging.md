---
title: 데이터 로깅
description: 데이터 로깅
keywords: [데이터 로깅]
sidebar_position: 4
sidebar_label: 데이터 로깅
---

# 데이터 로깅

### 들어가며..

데이터 로깅은 장치가 연결된 네트워크에서 주고받는 메시지와 신호를 저장하는 가장 기본적이고 많이 사용되는 기능입니다. 이 페이지에서는 데이터 통신 라인에서 나오는 메시지와 신호를 저장하는 방법에 대해 소개합니다.&#x20;

### 데이터 로깅 방식

데이터 로깅은 크게 메시지 단위 저장과 시그널 단위 저장의 두 가지 방식으로 나눌 수 있습니다.

* 메시지 단위 저장: CAN 메시지와 관련된 정보를 모두 저장합니다.
* 시그널 단위 저장: 디코딩된 시그널 값을 저장합니다.

메시지 단위 저장은 시그널 단위 저장을 포함하므로, 메시지 단위로 저장한 파일을 시그널 단위 저장 형식으로 변환이 가능합니다. 반대로, 시그널 단위로 저장된 파일은 메시지 단위로 변환할 수 없습니다.

### 데이터 로깅 방법

데이터 로깅에는 총 5가지 방법이 있습니다

* [Messages 창의 Save 버튼을 통한 데이터 로깅](./save-data-in-the-messages-menu/)
* [Measurement > Logging 메뉴를 통한 데이터 로깅](./how-to-save-signals-in-the-logging-menu/)
* [Script and Automation > Function Block 메뉴의 Capture 기능을 통한 데이터 로깅](./capture-function-block/)
* [장비 단독 데이터 로깅](./how-to-save-messages-on-the-device-alone/)
* [Data Cache를 사용한 로깅](./logging-using-data-cache/)

각 방법에 대해 다음 장부터 순차대로 알아보겠습니다.