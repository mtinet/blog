+++
categories = ["html"]
date = 2020-03-01T15:00:00Z
description = "홈페이지 주소가 여러개일 때 한 쪽 주소로 자동으로 이동하게 하는 방법"
image = "/images/redirect.png"
tags = ["html", " redirect"]
title = "홈페이지 리다이렉트(redirect) 하는 방법"
type = "post"

+++
  

  

  

  

  

블로그를 하거나 홈페이지가 여러개가 만들어졌을 때 이전 주소로 들어오게 되는 사람들이 혼란을 겪지 않게 하기 위해서는 '리다이렉트' 작업을 해주는게 좋다.

홈페이지에 사람들이 접속하게 되면 자동으로 index.html 파일을 열도록 설정되어 있는데, 그 파일의 <head></head> 태그 사이에 아래 코드를 추가 하면 해당 주소로 자동 리다이렉트 된다.

<meta http-equiv="refresh" content="3;url=[http://mtinet.netlify.com](http://mtinet.netlify.com "http://mtinet.netlify.com")" charset="utf-8" />

예제 코드는 다음과 같다.

    <!DOCTYPE html>
    <html>
    <head>
      <title>쥬디다무</title>                              
      <meta http-equiv="refresh" content="3;url=http://mtinet.netlify.com" charset="utf-8" />
      </head>
    <body>
      <h1>안녕하세요.</h1>
      <div>
        <p>이 페이지는 3초 후에 <a href="http://mtinet.netlify.com">http://mtinet.netlify.com</a>으로 자동 리다이렉트됩니다.</p>
      </div>
    </body>
    </html>

참고링크 : [https://www.tuwlab.com/ece/1987](https://www.tuwlab.com/ece/1987 "https://www.tuwlab.com/ece/1987")