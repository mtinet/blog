+++
categories = ["한글", "kivy", "python"]
date = 2020-03-08T15:00:00Z
description = "python GUI라이브러리인 kivy에서 한글이 나오게 하는 방법"
draft = true
image = ""
tags = ["python", "kivy", "한글"]
title = "kivy 한글 폰트 설치하기"
type = "post"

+++
##### python 기본 설치 위치

C:\\Users\\**사용자 계정**\\AppData\\Local\\Programs\\Python\\Python37

##### python에서 직접 확인하는 방법

![](/images/locationCheck.png)

    $python
    
    >>> import sys
    >>> sys.executable

kivy에서 한글을 사용하기 위해 폰트를 넣어놓을 

한글폰트 갖다 놓을 위치 :  
 - 윈도우: %파이썬 설치경로%\\Lib\\site-packages\\kivy\\data\\fonts  
 - 리눅스(라즈베리파이): /usr/local/lib/python3.4/dist-packages/kivy/data/fonts  
 - 저 위치에 malgun.ttf, malgunbd.ttf 등을 갖다 놓음

##### 참조

[https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70](https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70 "https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70")

[https://allhpy35.tistory.com/23](https://allhpy35.tistory.com/23 "https://allhpy35.tistory.com/23")

[http://blog.daum.net/pg365/276](http://blog.daum.net/pg365/276 "http://blog.daum.net/pg365/276")(시리얼 포트(COM port)나 TCP/IP, UDP/IP 프로토콜로 데이터를 주고받을 수 있는 프로그램)