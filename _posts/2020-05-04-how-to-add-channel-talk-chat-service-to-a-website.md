---
title: "How to add 'Channel Talk (chat service)' to a website"
categories: [Service]
tags: [Chat, Chat Service, Channel Talk]
---

## How to add 'Channel Talk (chat service)' to a website

1. Visit **Channel Talk** web site (<https://channel.io/en>).

2. **Join** the wet site
* Click the **'Join'** button at the top right of the website.
* Enter your **work email** and click the **'Try for Free'** button.
![join the Channel Talk web site](https://user-images.githubusercontent.com/32950391/81020308-84772380-8e36-11ea-825f-edeb41118bdd.JPG)

3. **Sign up**
* Enter **'Name'**, **'Password'** and **'Phone number'**.
* Click the **To the next step** button on the web page.
![sign up to Channel Talk](https://user-images.githubusercontent.com/32950391/81021991-7f1bd800-8e3a-11ea-89a2-c5ccb5547ffe.JPG)

4. Create new **Channel**.
* Enter **'Service name'** and **'Homepage URL'** and set the **'Chat theme color'**.
* Click the **To the next step** button on the web page.
![create new channel](https://user-images.githubusercontent.com/32950391/81022395-7e377600-8e3b-11ea-8a21-c9e49ed6f99e.JPG)

5. Enter **company information**.
* Enter **'Number of employees'**, **'Industry category'**, **'How did you find us?'** and **'What you want to do with Channel (duplicate)'**.
* Click the **Start Channel Talk** button on the web page.
![enter company information](https://user-images.githubusercontent.com/32950391/81030431-cc0da780-8e56-11ea-87c4-665f7641b513.JPG)

6. Get **Channel Plugin Scripts Code**.
* Click the **Own website** button on the web page.
* Copy the **code** clicking **'Copy'** button on the text area.
![own website button](https://user-images.githubusercontent.com/32950391/81031090-14c66000-8e59-11ea-8cb3-900a2d8a1b02.JPG)
![copy script code](https://user-images.githubusercontent.com/32950391/81031202-7f779b80-8e59-11ea-84a8-0ac7d0535918.JPG)

7. Insert the **code** into the home page **<body>** tag.
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

7. You can see **'chat icon'** and **'chat window'** at the bottom right of the site.
![chat icon](https://user-images.githubusercontent.com/32950391/81031773-65d75380-8e5b-11ea-81da-62b2b1e1b8ab.JPG)
![chat window](https://user-images.githubusercontent.com/32950391/81031860-c5356380-8e5b-11ea-8aba-11aef16cf4a3.JPG)
![chat start](https://user-images.githubusercontent.com/32950391/81032077-68867880-8e5c-11ea-8971-11637ca5e595.JPG)

8. On the Admin page, you'll see customer's chat. And you can respond.
![check and reply](https://user-images.githubusercontent.com/32950391/81032457-e13a0480-8e5d-11ea-9f79-a830ec60b2fb.JPG)

