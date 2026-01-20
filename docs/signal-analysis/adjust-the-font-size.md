---
title: 실시간 신호 그래프 보기
description: 실시간 신호 그래프 보기
keywords: [실시간 신호 그래프 보기]
sidebar_position: 2
sidebar_label: 실시간 신호 그래프 보기
---

# 실시간 신호 그래프 보기

### 들어가며..

이번 챕터에서는 실시간으로 업데이트되는 신호값들을 그래프로 볼 수 있는 방법에 대해 소개합니다.&#x20;

### Signal Plot

아래 그림과 같이 Measurement > Signal Plot으로 이동합니다.

<div class="text--center">

<figure>

![Measurement > Signal Plot](./../assets/images/image102.png "Measurement > Signal Plot")
<figcaption>Measurement > Signal Plot</figcaption>
</figure>
</div>

Signal Plot 창은 아래 그림과 같습니다.

<div class="text--center">

<figure>

![Signal Plot: Overview](./../assets/images/image156.png "Signal Plot: Overview")
<figcaption>Signal Plot: Overview</figcaption>
</figure>
</div>

이전 [Signal List 창](./../view-real-time-signal-values/)에서 설명한 내용과 같이 Signal Group을 통해 시그널을 관리할 수 있습니다.

\+ 버튼을 통해 새로운 Signal Group을 만들고, - 버튼을 통해 삭제합니다. Default 쪽의 드랍다운 메뉴로 현재 선택된 시그널을 ..하고 Select Signals를 통해 해당 그룹의 시그널을 추가/제거합니다. Logging 버튼을 눌러 Measurement > Logging 창으로 이동할 수 있습니다.

좌측 시그널 옆의 체크박스를 통해 그래프로 표시할 시그널을 선택할 수 있습니다. 그룹 전체를 선택할수도 그룹 내의 특정 시그널만 선택할수도 있습니다.

우측은 그래프가 표시되는 창입니다. 아래 그림을 통해 자세한 기능을 알아보겠습니다.

<div class="text--center">

<figure>

![Signal Plot: Graph](./../assets/images/image124.png "Signal Plot: Graph")
<figcaption>Signal Plot: Graph</figcaption>
</figure>
</div>

상단 붉은 박스의 좌측 버튼부터 설명드리겠습니다.

<img src={require('../assets/images/image65.png').default} alt="data" className="inline-img"/> Resume All(Tracking): 기본적으로 체크되어있습니다. 최신 데이터를 자동으로 스크롤하여 표시합니다.

<img src={require('../assets/images/image64.png').default} alt="data" className="inline-img"/> Pause All(Tracking): 그래프의 자동 스크롤을 멈추고 화면의 데이터를 검토할 수 있습니다.

<img src={require('../assets/images/image69.png').default} alt="data" className="inline-img"/> Sroll (Axes): 이 버튼을 눌러 축 위에서 마우스를 눌러 드래그 하면 축을 이동할 수 있습니다.

<img src={require('../assets/images/image68.png').default} alt="data" className="inline-img"/> Zoom (Axes): 이 버튼을 눌러 축 위에서 마우스를 눌러 드래그 하면 축을 확대/축소할 수 있습니다.

<img src={require('../assets/images/image61.png').default} alt="data" className="inline-img"/> Zoom Out All Axes: 이 버튼을 눌러 X축과 Y 축 모두 축소합니다.

<img src={require('../assets/images/image59.png').default} alt="data" className="inline-img"/> Zoom In All Axes: 이 버튼을 눌러 X축과 Y 축 모두 확대합니다.

<img src={require('../assets/images/image62.png').default} alt="data" className="inline-img"/> Zoom Box: 이 버튼을 누르고 그래프 위에서 마우스로 확대하고 싶은 영역을 드래그 하면 해당 영역만 확대하여 보여줍니다.

<img src={require('../assets/images/image82.png').default} alt="data" className="inline-img"/> Cursor: 커서를 활성화 하는 버튼입니다. 해당 커서는 현재의 시그널 값을 보여줍니다.

<img src={require('../assets/images/image81.png').default} alt="data" className="inline-img"/> Properties: 그래프의 속성을 변경할 수 있는 속성 창을 엽니다.

<img src={require('../assets/images/image81.png').default} alt="data" className="inline-img"/> Copy to Clipboard: 이 버튼을 눌러 그래프를 이미지로 복사합니다. 복사된 이미지는 그림판 등 다양한 프로그램에 붙여넣기 할 수 있습니다.&#x20;

<img src={require('../assets/images/image84.png').default} alt="data" className="inline-img"/> Save to File: 이 버튼을 눌러 해당 차트를 .jpg, .bmp 등 그림 파일로 저장할 수 있습니다.

<img src={require('../assets/images/image85.png').default} alt="data" className="inline-img"/> Print: 이 버튼을 눌러 해당 차트를 프린트합니다.

<img src={require('../assets/images/image77.png').default} alt="data" className="inline-img"/>: 커서 모드를 변경합니다. 커서가 어떤 정보를 보여줄지 선택할 수 있는 기능입니다.

<img src={require('../assets/images/image80.png').default} alt="data" className="inline-img"/>: 그래프에서 사용할 X축 간격을 초 단위로 설정할 수 있습니다.

자주 사용되는 기능으로 아래 그림과 같이 그래프 Y축에 마우스 우클릭을 하면
Zoom to Fit 버튼이 있습니다. 해당 버튼을 눌러 그래프의 Y축 Span을 맞출 수 있습니다.

<div class="text--center">

<figure>

![Signal Plot: Zoom to Fit](./../assets/images/image14.png "Signal Plot: Zoom to Fit")
<figcaption>Signal Plot: Zoom to Fit</figcaption>
</figure>
</div>

또한 Properties 메뉴를 통해 그래프의 속성을 변경할 수 있습니다. Channels 탭에서는 그래프에 표시되는 선의 속성을 설정하실 수 있습니다.&#x20;

<div class="text--center">

<figure>

![Signal Plot: Properties(Channels)](./../assets/images/image32.png "Signal Plot: Properties(Channels)")
<figcaption>Signal Plot: Properties(Channels)</figcaption>
</figure>
</div>

또한 Axes 탭에서는 그래프의 축에 대한 속성을설정하실 수 있습니다.

<div class="text--center">

<figure>

![Signal Plot: Properties(Axes)](./../assets/images/image75.png "Signal Plot: Properties(Axes)")
<figcaption>Signal Plot: Properties(Axes)</figcaption>
</figure>
</div>


Plot 탭에서는 그래프의 축에 대한 속성을설정하실 수 있습니다.

Stack Y Axes 버튼을 통해 그래프를 쌓아서 볼 수 있는 기능을 지원하며, 그래프의 배경 색상, 기본 폰트의 색상 등 다양한 설정을 할 수 있습니다.


<div class="text--center">

<figure>

![Signal Plot: Properties(Plot)](./../assets/images/image134.png "Signal Plot: Properties(Plot)")
<figcaption>Signal Plot: Properties(Plot)</figcaption>
</figure>
</div>


모든 설정은 아래 Preview 창을 통해 변경 내용을 확인할 수 있습니다. 

설정을 모두 마치면, Ok 버튼을 눌러 다시 Signal Plot 창으로 돌아올 수 있습니다.
