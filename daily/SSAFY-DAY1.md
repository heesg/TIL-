# SSAFY-DAY1

### 파이썬 코드 작성

```PYTHON
gj.py.hphk.io

저녁메뉴

import random 
menu = ["삼겹살","치킨","피자","칼국수","빕스"]
pick = random.choice(menu)
#(주석은 나중에 참고할 때 좋다.)랜덤하게 하나를 뽑을 수 있을까?
print(pick)



저녁식사 전화번호

import random

menu = ['영암매력한우수완점','신전떡볶이 광주수완점','양동통닭','광주식당','회마켓','원조나주곰탕50년']
print(menu[0])
choice = random.choice(menu)
print(choice)

phonebook = {'영암매력한우수완점':'062-383-8118',
​            '신전떡볶이 광주수완점':'062-956-2334',
​             '양동통닭':'062-471-9277',
​             '광주식당':'062-962-8284 ',
​             '회마켓':'062-952-2026',
​             '원조나주곰탕50년':'062-951-3255'
​            }
print(phonebook[choice])



미세먼지

if dust > 100:
  print("높음")
elif dust > 50:
  print("낮음")
else:
  print("매우낮음")



로또번호 추출

import random
numbers = list(range(1,46))
print(numbers)
#numbers에 1부터 45 넣기
a = random.sample(numbers,6)
#이것은 비복원 추출 x
print(a)



웹크롤링(코스피)

import requests
from bs4 import BeautifulSoup

url = 'https://finance.naver.com/sise/'

r = requests.get(url).text
soup = BeautifulSoup(r,'html.parser')
select = soup.select_one("#KOSPI_now")
print(select.text)
#200은 매우 잘되었음을 의미 


LOTTO

import random
numbers = list(range(1,46))
print(numbers)
#numbers에 1부터 45 넣기
a = random.sample(numbers,6)
#이것은 비복원 추출 x
print(a)


광주먼지

import requests
from bs4 import BeautifulSoup
url = 'http://openapi.airkorea.or.kr/openapi/services/rest/ArpltnInforInqireSvc/getCtprvnRltmMesureDnsty?serviceKey=' + key + '&numOfRows=10&pageSize=10&pageNo=1&startPage=1&sidoName=%EA%B4%91%EC%A3%BC&ver=1.3'
request = requests.get(url).text
soup = BeautifulSoup(request,'xml')
dong = soup('item')[7]
location = dong.stationName.text
time = dong.dataTime.text
dust = int(dong.pm10Value.text)

print("{0} 기준 {1}의 미세먼지 농도는 {2}입니다.".format(time,location,dust))

```



