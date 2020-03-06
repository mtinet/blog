+++
categories = ["login", "kivy", "python"]
date = 2020-03-06T15:00:00Z
description = "kivy라이브러리를 이용해 GUI형태의 로그인 창 만들기"
image = "/images/스크린샷 2020-03-07 오전 12.47.54.png"
tags = ["python", "kivy", "login"]
title = "python으로 login 시스템 만들기(feat.kivy)"
type = "post"

+++
python과 kivy를 활용하면 아래 캡쳐와 같은 예쁜 로그인 페이지를 만들 수 있다. 기본 파일은 다음과 같다.

main.py : 프로그램이 동작하도록 틀을 잡아주는 파일

database.py : 로그인을 위하여 계정을 만들 때 데이터베이스에 자료를 추가하거나, 로그인을 할 때 데이터베이스의 정보를 확인해주는 파일

my.kv : 디자인을 만들어주는 파일

users.txt : 데이터베이스 파일에 의해 데이터가 저장되는 파일

계정이 있으면 로그인을 하고, 없으면 계정을 만드는 창으로 이동한다.
![](https://github.com/mtinet/blog/blob/master/exampleSite/static/images/kivy1.png?raw=true)  

계정을 만들 수 있는 창에서 계정을 만들고 서밋을 하면 자동으로 로그인 창으로 이동한다.
![](https://github.com/mtinet/blog/blob/master/exampleSite/static/images/kivy2.png?raw=true)  

로그인을 하고나면 로그인 정보를 확인할 수 있는 창을 보여준다.
![](https://github.com/mtinet/blog/blob/master/exampleSite/static/images/kivy3.png?raw=true)  

만약 로그인 정보가 바르지 않으면 정보가 잘못되었음을 보여주는 팝업을 띄운다.
![](https://github.com/mtinet/blog/blob/master/exampleSite/static/images/kivy4.png?raw=true)  

사실 kivy는 Bay Area Flagship MakerFaire에서 본 Dos Pueblos Engineering Academy 학생들이 만든 작품들의 오퍼레이팅 화면을 보고 너무 깔끔하게 만들어놔서 어떻게 만들었는지 물어봐서 알게 되었었다. 하지만, 한국으로 돌아와서 한 번 자료를 찾아보았었지만, 마땅히 구동이 잘 안되서 미뤄두다가 다시 한 번 자료를 찾아봤는데, 그 새 많은 자료들이 만들어져 있는 것을 확인할 수 있게 되었다.

kv라는 파일로 따로 화면을 구성해서 불러오기도 하고, 그냥 python파일에서 구동하기도 하는데, 어찌되었든 python으로 구현하는 GUI중에서는 가장 깔끔한 결과물을 보여주는 것 같아 소개한다.

이 예제는 아래 사이트에서 보고 테스트 해보았다.

[https://techwithtim.net/tutorials/kivy-tutorial/example-gui/](https://techwithtim.net/tutorials/kivy-tutorial/example-gui/ "https://techwithtim.net/tutorials/kivy-tutorial/example-gui/")

공식사이트는 다음과 같으며,

[https://kivy.org](https://kivy.org/ "https://kivy.org/")

기초 학습은 이곳에서 할 수 있다.

[https://kivy.org/doc/stable/guide/basic.html](https://kivy.org/doc/stable/guide/basic.html "https://kivy.org/doc/stable/guide/basic.html")

또한, kivy는 크로스 플랫폼을 지원하는데, 윈도우, 리눅수, OS X, 안드로이드, iOS, 라즈비안에도 모두 동작한다. 앱으로 구동하는 kivy의 모습은 아래 링크에서 확인할 수 있다.

[http://wiznetacademy.com/wp/?p=7026](http://wiznetacademy.com/wp/?p=7026 "http://wiznetacademy.com/wp/?p=7026")
