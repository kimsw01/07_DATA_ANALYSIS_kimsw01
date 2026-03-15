# 데이터분석 2주차 정규과제

📌데이터분석 정규과제는 매주 정해진 분량의 『*혼자 공부하는 데이터 분석 with 파이썬*』 을 읽고 학습하는 것입니다. 이번 주는 아래의 **DataAnalysis_2nd_TIL**에 나열된 분량을 읽고 공부하시면 됩니다.

아래의 문제를 풀어보며 학습 내용을 점검하세요. 문제를 해결하는 과정에서 개념을 스스로 정리하고, 필요한 경우 제시된 강의를 참고하여 보완하는 것이 좋습니다.

<!-- 강의 링크는 아래와 같습니다.
https://www.youtube.com/watch?v=s_-VvTLb3gs&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=4
https://www.youtube.com/watch?v=Il6L8OtNFpc&list=PLVsNizTWUw7FGzSRCkQrPEEe-ljVXgS7k&index=5
-->


## DataAnalysis_2nd_TIL

### 2장 데이터 수집하기
#### 01. API 사용하기
#### 02. 웹 스크래핑 사용하기


## Study Schedule

| 주차  | 공부 범위     | 완료 여부 |
| ----- | ------------- | --------- |
| 1주차 | p.24~81    | ✅         |
| 2주차 | p.84~151   | ✅         |
| 3주차 | p.154~219  | 🍽️         |
| 4주차 | p.222~279 | 🍽️         |
| 5주차 | p.282~325 | 🍽️         |
| 6주차 | p.328~379 | 🍽️         |
| 7주차 | p.382~430 | 🍽️         |

<br>

<!-- 여기까진 그대로 둬 주세요-->


# 1️⃣ 개념 정리 

## 01. API 사용하기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->

### API (Application Programming Interface)

: 두 프로그램의 대화하는 방법 (신호 체계)

- HTTP : 웹 브라우저가 요청하는 웹 페이지
- HTML : 웹 서버가 전송하는 웹 페이지 (텍스트 파일)

=> 웹 기반 API

- JSON : key와 value로 이루어진 dict와 유사한 형태
=> 문자열 다루기 : 텍스트로 전송해야함. (json.dumps())
=> 받을 때는 json.loads()

- JSON 구조의 복잡함 :

겹치는 JSON 배열이 두개 있다면, 하나의 큰 JSON 배열 안데 JSON 객체를 두 개 넣어도 됨.

- 읽기 :

read_json()

### XML

~~~
<book> # 시작 태그 (부모 노드)
 <name> 혼공 데분</name> # 하나의 요소 = 엘리먼트
 <author> 박해선</author> 
 <year> 2021</year>
 </book> # 종료 태그
~~~

- findtext() : 자신의 엘리먼트에서 찾기

## 02.웹 스크래핑 사용하기

<!-- 새롭게 배운 내용을 자유롭게 정리해주세요.-->

### 도서 쪽수 찾기

온라인 서점 데이터에 쪽 수 정보 있음. -> 서점 HTML에서 뽑아내기.

- 웹 크롤링 :

request.get()으로 검색 결과 가져오기 ->

검색결과에서 도서 상세 페이지로 연결되는 링크 URL 추출 ->

다시 request.get()으로 도서 상세페이지 가져오기 ->

도서 상세 페이지에서 쪽수 추출

### 뷰티풀수프 사용하기

크롬 개발자도구에서 태그의 요소를 가져오기 (div나 table)

- find() 메서드
- find_all() 메서드
http://www.yes24.com/Product/Search?domain=BOOK&query=9791190090018

### 웹 스크래핑 주의할 점

- 웹사이트에서 스크래핑을 허락했는가? (robots.txt)
- HTML 태그를 특정할 수 있는가?
- 페이지가 동적으로 생성되는가?
- 디자인이 자주 변경되는가?

### 데이터프레임의 행과 열 선택하기

- df.loc[] 함수 활용 
-> df.loc[:] 전부 가져오기, df.loc[:2] 2까지 가져오기 등..


# 2️⃣ 수행 인증

<!-- 교재에서 안내된 과정을 직접 실행해본 뒤, 진행 결과가 보이도록 4~6장의 스크린샷을 캡처하여 아래에 첨부해주세요.-->

![alt text](<picture/스크린샷 2026-03-16 043051.png>)
![alt text](<picture/화면 캡처 2026-03-16 044811.png>)
![alt text](<picture/화면 캡처 2026-03-16 045202.png>)
![alt text](<picture/화면 캡처 2026-03-16 045622.png>)
![alt text](<picture/화면 캡처 2026-03-16 050911.png>)

<br>
<br>

# 3️⃣ 확인 문제

## 문제 1.

> **🧚Q. 다음 중 BeautifulSoup 외에 웹 스크래핑에 사용할 수 있는 파이썬 패키지로 가장 적절한 것은 무엇인가요?**

```
1️⃣ NumPy  
2️⃣ Scrapy  
3️⃣ Matplotlib  
4️⃣ Scikit-learn  
```

```
여기에 선택한 답과 그 이유를 간단히 서술해주세요!

스크래피는 requests와 뷰티풀수프를 합쳐 놓은 것과 비슷함.
따라서 정답은 2번 Scrapy.

```



### 🎉 수고하셨습니다.
