---
title: "웹사이트에 채널톡 (채팅창) 추가하는 방법"
categories: [Service]
tags: [Chat, Chat Service, Channel Talk, 채팅, 채널톡]
---

## 웹사이트에 채널톡 (채팅창) 추가하는 방법

1. **채널톡** 웹사이트 (<https://channel.io/ko>)를 방문하십시오.

2. 웹사이트 **가입**
* 웹사이트 우측 상단의 **‘시작하기’** 버튼을 클릭하십시오.
* **업무용 이메일**을 입력하고 **14일 무료체험시작** 버튼을 클릭하십시오.
![채널톡 시작하기](https://user-images.githubusercontent.com/32950391/81033206-b00f0380-8e60-11ea-89bf-527ea8e59d07.JPG)

3. **관리자 계정 가입하기**
* **'이름'**, **'비밀번호'** and **'휴대폰 번호'**를 입력하십시오.
* **‘다음 단계로’** 버튼을 클릭하십시오.
![관리자 계정 가입하기](https://user-images.githubusercontent.com/32950391/81033412-94f0c380-8e61-11ea-8541-2715c2a642ac.JPG)

4. 새 **채널** 만들기.
* **'서비스명'**, **'홈페이지 주소'**와 **'채팅 테마 색상'**을 입력하십시오.
* **‘다음 단계로’** 버튼을 클릭하십시오.
![새 채널 만들기](https://user-images.githubusercontent.com/32950391/81033580-23654500-8e62-11ea-9de4-d00c0be1656b.JPG)

5. **회사 정보** 입력.
* **'직원수'**, **'업종 카테고리'**, **'채널 가입 경로'**와 **'채널로 하고 싶은 것 (중복가능)'**을 선택하십시오.
* **‘채널톡 시작하기’** 버튼을 클릭하십시오.
![회사정보 입력](https://user-images.githubusercontent.com/32950391/81033910-52c88180-8e63-11ea-963e-ba5a0b0f9036.JPG)

6. **채널 플러그인 스크립트 코드** 생성
* **‘자체 제작 웹사이트’** 버튼을 클릭하십시오.
* 텍스트 입력칸의 **코드**를 **'복사하기'** 버튼을 클릭하여 복사하십시오.
![자체 제작 웹사이트](https://user-images.githubusercontent.com/32950391/81034087-0598df80-8e64-11ea-9a79-4d673e2e330f.JPG)
![코드 복사하기](https://user-images.githubusercontent.com/32950391/81034100-0f224780-8e64-11ea-9d61-47f9a2b50b7e.JPG)

7. **코드**를 홈페이지 HTML의 **<body>** 태그에 붙여넣기 하십시오.
```
<!-- Channel Plugin Scripts -->
<script>
  (function() {
    var w = window;
    if (w.ChannelIO) {
      return (window.console.error || window.console.log || function(){})('ChannelIO script included twice.');
    }
    var d = window.document;
    var ch = function() {
      ch.c(arguments);
    };
    ch.q = [];
    ch.c = function(args) {
      ch.q.push(args);
    };
    w.ChannelIO = ch;
    function l() {
      if (w.ChannelIOInitialized) {
        return;
      }
      w.ChannelIOInitialized = true;
      var s = document.createElement('script');
      s.type = 'text/javascript';
      s.async = true;
      s.src = 'https://cdn.channel.io/plugin/ch-plugin-web.js';
      s.charset = 'UTF-8';
      var x = document.getElementsByTagName('script')[0];
      x.parentNode.insertBefore(s, x);
    }
    if (document.readyState === 'complete') {
      l();
    } else if (window.attachEvent) {
      window.attachEvent('onload', l);
    } else {
      window.addEventListener('DOMContentLoaded', l, false);
      window.addEventListener('load', l, false);
    }
  })();
  ChannelIO('boot', {
    "pluginKey": "470a6072-0777-449e-92bb-2197de06728e"
  });
</script>
<!-- End Channel Plugin -->
```

7. **채팅 아이콘**과 **채팅 윈도우**를 웹사이트 우측 하단에서 볼 수 있습니다.
![chat icon](https://user-images.githubusercontent.com/32950391/81031773-65d75380-8e5b-11ea-81da-62b2b1e1b8ab.JPG)
![chat window](https://user-images.githubusercontent.com/32950391/81031860-c5356380-8e5b-11ea-8aba-11aef16cf4a3.JPG)
![chat start](https://user-images.githubusercontent.com/32950391/81032077-68867880-8e5c-11ea-8971-11637ca5e595.JPG)

8. 관리자 페이지에서 고객의 채팅내용을 볼 수 있고 응답할 수 있습니다.
8. On the Admin page, you'll see customer's chat. And you can respond.
![check and reply](https://user-images.githubusercontent.com/32950391/81032457-e13a0480-8e5d-11ea-9f79-a830ec60b2fb.JPG)
![관리자 페이지](https://user-images.githubusercontent.com/32950391/81034443-32012b80-8e65-11ea-84c9-916ef9aad906.JPG)

