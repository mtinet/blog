+++
categories = ["graph", "python"]
date = 2020-03-01T15:00:00Z
description = "파이썬으로 그래프를 그려보다."
image = "/images/pythongraph/1101_temp.png"
tags = ["python", "graph", "plt", "matplotlib", "csv"]
title = "python으로 그래프 그리기"
type = "post"
+++  

옆의 그래프는 파이썬으로 그린 그래프이다. 79년 11월 1일부터 지금까지 매년 11월 1일의 최고온도와 최저온도를 그래프로 그리는 작업을 해보았다. 

한성과학고에서 정보교과를 가르치고 있는 송석리샘이 쓴 책 '모두의 데이터분석 with 파이썬'을 참고하면 '기상자료개방포털'로부터 csv파일을 다운 받을 수 있고, 그 데이터를 기반으로 python과 matplotlib 라이브러리를 이용해 그래프로 표현할 수 있다. 

데이터(seoul.csv)파일을 먼저 열어서 가장 위쪽에 있는 쓸데 없는 부분을 헤더부분만 남기고 삭제해 준 다.

프로그램의 기본 구조는 라이브러리를 임포트한 후 데이터(seoul.csv)를 가져오고, 헤더를 데이터와 구분해준다. utf-8은 한글 엔코딩 형식을 말하는데, 보통은 utf-8을 쓰나, 맥에서는 cp949를 쓰기도 한다. 

    import csv
    import matplotlib.pyplot as plt
    
    f = open('seoul.csv', encoding = 'utf8')
    data = csv.reader(f)
    next(data)

다음으로 최고 온도, 최저 온도가 들어갈 리스트를 만들고, csv파일을 검색하여 최고 온도의 빈칸이 있는질ㄹ  최고 온도를 high 리스트에, 최저 온도를 low 리스트에 넣어준다. 

csv파일을 열어보면 알겠지만, 최고온도는 가장 오른쪽 열에 있어서 row\[-1\]을 최저온도는 오른쪽 열에서 세번째에 있어서 row\[-3\]을 쓴다. 

아래 부분은 첫번째 열에 있는 날짜의 형태가 '1979-11-01'의 형태로 만들어져 있기 때문에 '-'로 잘라서 리스트에 집어 넣고, 그 리스트의 왼쪽에서 두번째 값이 '11'인 것을 찾기 위한 코드이다. 

    row[0].split('-')[1] == '11' 

어찌됐든 날짜의 왼쪽에서 두번째 값이 11, 세번째 값이 01인 행의 오른쪽에서 첫번째(최고온도), 오른족에서 두번째(최저온도)를 각각 high 리스트, low 리스트에 넣고 high는 핫핑크로, low는 스카이블루로 그래프를 그린다. 

    import csv
    import matplotlib.pyplot as plt
    
    f = open('seoul.csv', encoding = 'utf8')
    data = csv.reader(f)
    print(next(data))
    
    
    
    high = []
    low = []
    
    for row in data :
        if row[-1] != '' and row[-2] != '' :
            if row[0].split('-')[1] == '11' and row[0].split('-')[2] == '01' :
                high.append(float(row[-1]))
                low.append(float(row[-2]))
                
    
    plt.plot(high, 'hotpink')
    plt.plot(low, 'skyblue')
    plt.show()
    
