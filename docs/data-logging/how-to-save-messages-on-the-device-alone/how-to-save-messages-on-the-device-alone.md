---
title: 장비 단독으로 메세지 저장법
description: 장비 단독으로 메세지 저장법
keywords: [장비 단독으로 메세지 저장법]
sidebar_position: 4
sidebar_label: 장비 단독으로 메세지 저장법
---

# 장비 단독으로 메세지 저장법

### 들어가며..

이번 챕터에서는 장치를 PC에 연결하지 않고 장치 단독으로 로깅(Standalone logging)하는 방법을 알아보겠습니다.

### VehicleScape DAQ

VehicleScape DAQ는 진단과 로깅을 통합한 신호 데이터 수집 도구입니다. 독립 실행형 로깅은 SD 카드와 CoreMini 스크립팅을 지원하는 ICS 하드웨어가 필요합니다.

아래 그림과 같이 Measurement > VehicleScape DAQ를 눌러 VehicleScape DAQ를 실행합니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ](./../../assets/images/image29.png "Standalone Logging: VehicleScape DAQ")
<figcaption>Standalone Logging: VehicleScape DAQ</figcaption>
</figure>
</div>

### Database/Hardware Setup

이 탭에서는 하드웨어 설정을 관리하고, 플랫폼 데이터베이스를 선택하며, 로거 SD 카드에서 데이터를 가져오는 기능을 제공합니다.

데이터 취득을 위해 알맞은 데이터베이스(dbc, odx, a2l등)가 불러와졌는지 다시 한 번 확인합니다. \
.dbc, .ldf, .arxml 파일의 추가 방법은 [여기](./../../getting-started/database-platform-and-register-database-files/)를 참고하시기 바랍니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ(Database/Hardware Setup)](./../../assets/images/image133.png "Standalone Logging: VehicleScape DAQ(Database/Hardware Setup)")
<figcaption>Standalone Logging: VehicleScape DAQ(Database/Hardware Setup)</figcaption>
</figure>
</div>

기능에 대한 설명은 다음과 같습니다.

* DAQ Name: DAQ의 이름을 설정합니다. 이 기능을 통해 Expression Builder에서 DAQ 설정을 쉽게 변경할 수 있습니다.
* Auto Start PC DAQ: 해당 옵션을 선택할 경우 Vehicle Spy 3가 Online이 될 때 PC와 장치에서 동시에 DAQ Function을 수행합니다.

### Channels

이 탭은 원하는 신호를 설정해서 로깅할 수 있도록 하는 기능입니다. 다른 위치의 Filters 옵션과 유사합니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ(Channels))](./../../assets/images/image11.png "Standalone Logging: VehicleScape DAQ(Channels)")
<figcaption>Standalone Logging: VehicleScape DAQ(Channels)</figcaption>
</figure>
</div>

좌측 탭에서 원하는 신호를 선택하여 더블 클릭 또는 드래그 앤 드롭을 통해 우측 창으로 이동합니다.

우측 탭 상단에서 Pooling / Decimation Setup 메뉴를 통해 ISO 14229 메시지(UDS), XCP, CCP 변수를 로깅할 때 Pooling Rate를 설정할 수 있습니다.

### PC Logging

이 탭에서 Standalone Logging와 같이 실행할 PC Logging 설정을 할 수 있습니다. 자세한 설정 방법은 [링크](./../how-to-save-signals-in-the-logging-menu/)를 참조 바랍니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ(PC Logging))](./../../assets/images/image132.png "Standalone Logging: VehicleScape DAQ(PC Logging)")
<figcaption>Standalone Logging: VehicleScape DAQ(PC Logging)</figcaption>
</figure>
</div>

### Standalone Logging

이 탭에서는 PC 없이 Standalone Logging을 위해 필요한 옵션들을 설정할 수 있습니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ(Standalone Logging)](./../../assets/images/image88.jpg "Standalone Logging: VehicleScape DAQ(Standalone Logging)")
<figcaption>Standalone Logging: VehicleScape DAQ(Standalone Logging)</figcaption>
</figure>
</div>

Standalone Logging에서는 Collection을 통해 로깅의 설정을 관리할 수 있습니다. 각 Collection은 고유한 시작/정지(trigger) 설정을 가질 수 있으며, 여러 개의 로그 파일을 기록할 수 있습니다.

Collection은 + - 버튼으로 추가 제거가 가능하며 하나의 script에는 최대 16개의 Collection을 가질 수 있습니다.

Collection 내부 기능에 대한 설명은 다음과 같습니다.

* Name: 해당 로깅 설정의 이름을 설정합니다. 이 이름으로 로그 파일이 생성됩니다. 아래의 Append Time and Date to file name 옵션을 사용하면 자동으로 로깅 날짜와 시간을 파일 이름 뒤에 붙여줍니다.<br/>

* Type: 아래와 같이 세 종류의 Collection Method를 선택할 수 있습니다.

  * Message Capture: 가장 대표적인 기능입니다. 네트워크의 메시지 데이터를 수집하여 저장합니다.
  * Bus Query: 특정 시점의 데이터를 Snapshot 형태로 저장합니다. 통시적 데이터 보다는 특정 순간의 상태를 확인하고 싶을 때 사용합니다.
  * Histogram: 일정 기간 동안 특정 범위의 메시지 빈도를 측정하는데 사용합니다. 특정 이벤트의 발생 주기를 분석하는데 유리합니다.

* Message Collection Options: 두 가지의 로깅을 지원합니다.

  * Log all bus messages: 전체 혹은 특정 네트워크의 모든 메시지를 저장합니다.
  * Log only the items selected on the Channels tab: 이전 Channel 탭에서 선택한 메시지만 저장합니다.

* Start: 로깅 시작 옵션을 선택합니다.

  * Start immediately: 장치에 스크립트를 심는 동시에 로깅을 시작합니다.
  * Start when expression is true: 우측의 조건을 만족할 때 로깅을 시작합니다. 조건은 Expression builder를 통해 수식을 정의하거나, 아래 체크 박스를 선택하여 설정할 수 있습니다.
  * Start using trigger expression: trigger 혹은 우측의 체크 박스를 만족시킬 때 로깅을 시작합니다.
  * Start every \[] seconds: 설정한 시간 마다 로깅을 시작합니다.

* Stop: 로깅 종료 옵션을 선택합니다.

  * Finish after collecting \[] messages: 정해진 메시지 수만큼 로깅을 하고 중단합니다. 우측에 해당 메시지가 들어올 경우 예상 저장 공간이 표시됩니다.
  * Finish after \[] seconds: 정해진 시간만큼 로깅을 하고 중단합니다.
  * Finish when expression is true: 우측의 수식을 만족할 경우 로깅을 중단합니다.

* Restart: 로깅 종료 후 재시작 옵션입니다.
  * Do not restart the collection when finished: 로깅 종료 후 재시작 하지 않습니다.
  * Restart the collection when finished: 로깅 종료 후 해당 Collection을 다시 시작합니다.\
    Start 조건이 걸려 있을 경우, 조건을 다시 만족해야 로깅을 시작합니다.
  * Force restart(do not wait for start expression): 로깅 종료 후 곧바로 로깅을 재시작합니다.

* Upload to Wireless neoVI: Wireless neoVI(WIVI)에 데이터를 업로드 하는 옵션입니다.  해당 옵션은 Start immediately 옵션에서는 사용하실 수 없습니다. ([WIVI란?](https://www.intrepidcs.co.kr/wireless-neovi.html))
  * WiFi / Ethernet: WiFi 혹은 Ethernet 포트를 사용하여 데이터를 업로드합니다.
  * Cellular: 별도의 [모뎀](https://intrepidcs.com/products/rad-4g/)을 통해 Cellular Network를 사용하여 데이터를 업로드합니다.
  * Upload Priority: 데이터를 업로드할 우선순위를 선택할 수 있습니다.

Standalone Logging 탭은 스크롤을 내리면 하단에 더 많은 설정이 있습니다.

<div class="text--center">

<figure>

![Standalone Logging: VehicleScape DAQ(Standalone Logging)](./../../assets/images/image91.png "Standalone Logging: VehicleScape DAQ(Standalone Logging)")
<figcaption>Standalone Logging: VehicleScape DAQ(Standalone Logging)</figcaption>
</figure>
</div>

Status Reporting: 로깅 상태를 확인할 수 있는 방법입니다.

* LEDs: 해당 옵션을 선택하면 장치에 내장된 LED를 통해 현재 로깅 상태를 보여줍니다.&#x20;
* Use neoVI MOTE to report logger statue: neoVI MOTE(별매, [링크](https://www.intrepidcs.co.kr/neovi-mote.html))를 통해 로깅 상태를 보여줍니다.
* Beep on Wakeup: 비프음을 통해 로깅을 알립니다.

Power Management  탭을 통해 장치의 sleep / wakeup 등 전원 관리 설정을 할 수 있습니다.

* Sleep
  * Never go to sleep: bus가 idle 상태여도 로깅을 중단하지 않습니다.
  * Sleep when there's no bus activity: 설정한 시간동안 메시지가 들어오지 않으면 로깅을 중단합니다.\
    Advanced 옵션을 통해 해당 옵션에서 제외할 네트워크를 선택할 수 있습니다.

* Wake
  * Normal: Sleep 상태에서 메시지가 들어왔을 때 더 천천히 동작합니다. 이 옵션은 sleep 시의 전력 소모를 줄여줍니다. 단 Wake up 시 최초의 일부 메시지는 로깅되지 않을 수 있습니다.
  * Fast: Sleep 상태의 장치가 좀 더 빠르게 깨어납니다.&#x20;
  * Enable remote wake up: 해당 옵션을 선택하면 원격으로 장치를 깨울 수 있습니다.
  * Start a new file when waking up: 해당 옵션을 선택할 경우, 장치가 Wake up 때마다 새로운 파일을 생성하여 데이터를기록합니다.

* Wireless neoVI: WIVI를 위한 옵션을 설정합니다.
  * Overall Timeout(min): WIVI에 업로드를 시도할 수 있는 최대 시간을 설정합니다.
  * Connection Timeout(min): 연결을 시도하기 위한 최대 시간을 설정합니다.
  * Voltage Cutoff(V): 로거가 데이터를 업로드 하기위한 최소 전압을 설정합니다.

옵션을 모두 선택하였으면 하단의 Generate 버튼을 통해 스크립트를 컴파일 합니다.

### CoreMini Console

Generate 버튼을 누르면 아래 그림과 같이 CoreMini Console이 실행됩니다.

<div class="text--center">

<figure>

![Standalone Logging: CoreMini Executable Generator(CoreMini Console)](./../../assets/images/image87.jpg "Standalone Logging: CoreMini Executable Generator(CoreMini Console)")
<figcaption>Standalone Logging: CoreMini Executable Generator(CoreMini Console)</figcaption>
</figure>
</div>

Target Device에 스크립트를 심기 원하는 장치를 선택 후 Storage를 선택합니다.

Send 버튼을 눌러 장치에 스크립트를 심습니다. Send가 완료되고 나면 장치는 알아서 Logging을 시작합니다.
