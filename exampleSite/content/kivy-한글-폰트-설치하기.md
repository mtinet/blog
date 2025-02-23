+++
categories = ["programming"]
date = 2020-03-08T15:00:00Z
description = "python GUI라이브러리인 kivy에서 한글이 나오게 하는 방법"
image = "/images/kivykor/kivyKorean.png"
tags = ["python", "kivy", "한글", "윈도우"]
title = "kivy 한글 폰트 설치하기"
type = "post"

+++
##### python 기본 설치 위치

C:\\Users\\**사용자 계정**\\AppData\\Local\\Programs\\Python\\Python37

##### python에서 직접 설치 위치를 확인하는 방법

![](/images/kivykor/locationCheck.png)

    $python
    
    >>> import sys
    >>> sys.executable

##### 폰트파일 저장 위치

kivy에서 한글을 사용하기 위해 폰트를 넣어놓을

한글폰트 갖다 놓을 위치는 운영체제 별로 다음과 같다.

\-윈도우: %파이썬 설치경로%\\Lib\\site-packages\\kivy\\data\\fonts

\-리눅스(라즈베리파이): /usr/local/lib/python3.4/dist-packages/kivy/data/fonts

이 위치에 malgun.ttf, malgunbd.ttf 등의 폰트 파일을 갖다 놓는다.

##### 예제

    from kivy.app import App
    from kivy.uix.button import Button
    
    class TestApp(App):
        def build(self):
            fontName = "fonts/NanumGothic.ttf"
            return Button(text='안녕하세요 \nKivy입니다.',font_name=fontName)
    
    if __name__ == '__main__':
        TestApp().run()

##### 배포

그나저나 pyinstaller를 설치하고 배포를 좀 해볼까 했더니만.... 테스트 파일은 잘 만들어지는데, kivy가 들어가 있는 파일은 아래와 같은 오류가 난다.

![](/images/kivykor/disterror.png)

검색을 하다가 좀 더 아시는 분인 것 같아 물어봐놓은 상태..ㅠㅠ

[https://hongku.tistory.com/338](https://hongku.tistory.com/338 "https://hongku.tistory.com/338")

##### 참조

[https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70](https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70 "https://gist.github.com/edp1096/16e978a531acf23157e16b21a1e95e70")

[https://allhpy35.tistory.com/23](https://allhpy35.tistory.com/23 "https://allhpy35.tistory.com/23")

[http://blog.daum.net/pg365/276](http://blog.daum.net/pg365/276 "http://blog.daum.net/pg365/276")(시리얼 포트(COM port)나 TCP/IP, UDP/IP 프로토콜로 데이터를 주고받을 수 있는 프로그램)
