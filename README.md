# Matplotlib 라이브러리 완전 가이드북

---

## 1. Matplotlib 소개

| 항목           | 설명                                            |
|----------------|-------------------------------------------------|
| 라이브러리명    | Matplotlib                                      |
| 주요 기능      | 파이썬에서 2D 및 3D 그래프 및 시각화 도구 제공 |
| 공식 홈페이지  | [https://matplotlib.org](https://matplotlib.org) |
| 설치 명령어    | `pip install matplotlib`                        |

---

## 2. 기본 사용법

| 단계           | 코드 예시                                 | 설명                           |
|----------------|------------------------------------------|------------------------------|
| 임포트         | `import matplotlib.pyplot as plt`       | pyplot 모듈 불러오기           |
| 데이터 준비    | `x = [1,2,3]` <br> `y = [4,5,6]`        | x, y 축 데이터 준비            |
| 그래프 그리기  | `plt.plot(x, y)`                         | 기본 선 그래프 그리기          |
| 출력           | `plt.show()`                            | 그래프 화면에 표시             |

---

## 3. 주요 그래프 종류

| 그래프 종류        | 함수명            | 설명                              | 간단 예시                              |
|-------------------|-----------------|---------------------------------|-------------------------------------|
| 선 그래프         | `plt.plot()`    | 연속 데이터 시각화                | `plt.plot(x, y)`                    |
| 산점도            | `plt.scatter()` | 점으로 데이터 분포 표현          | `plt.scatter(x, y)`                 |
| 막대 그래프       | `plt.bar()`     | 범주형 데이터 막대 길이로 표현   | `plt.bar(categories, values)`       |
| 히스토그램        | `plt.hist()`    | 데이터 분포를 구간별로 표현      | `plt.hist(data, bins=10)`            |
| 원 그래프 (파이)   | `plt.pie()`     | 비율을 원 형태로 표현            | `plt.pie(sizes, labels=labels)`      |
| 박스 플롯         | `plt.boxplot()` | 데이터 분포와 이상치 시각화      | `plt.boxplot(data)`                  |

---

## 4. 그래프 꾸미기 옵션

| 옵션                 | 설명                        | 예시                             |
|----------------------|-----------------------------|--------------------------------|
| 제목 설정            | 그래프 제목 지정             | `plt.title("제목")`             |
| 축 레이블 설정       | x, y 축 이름 설정            | `plt.xlabel("X축")`<br>`plt.ylabel("Y축")` |
| 범례 표시            | 여러 데이터 구분하는 범례    | `plt.legend()`                  |
| 축 범위 지정         | x, y 축 범위 지정            | `plt.xlim(0, 10)`<br>`plt.ylim(0, 100)` |
| 선 스타일 변경       | 선 색, 두께, 모양 변경       | `plt.plot(x, y, color='red', linewidth=2, linestyle='--')` |
| 격자 표시            | 그래프 격자선 표시           | `plt.grid(True)`                |

---

## 5. 서브플롯 (여러 그래프 한 화면에)

| 방법                  | 코드 예시                               | 설명                            |
|-----------------------|----------------------------------------|-------------------------------|
| `plt.subplot()` 사용   | `plt.subplot(2,1,1)`<br>`plt.plot(x,y1)`<br>`plt.subplot(2,1,2)`<br>`plt.plot(x,y2)` | 2행 1열 서브플롯 만들기          |
| `plt.subplots()` 사용  | `fig, axs = plt.subplots(2, 2)`<br>`axs[0,0].plot(x,y)` | 2x2 격자 서브플롯 만들기         |

---

## 6. 이미지 저장하기

| 기능               | 코드 예시                   | 설명                            |
|--------------------|----------------------------|--------------------------------|
| 그래프 이미지 저장 | `plt.savefig("filename.png")` | 그래프를 PNG, JPG 등으로 저장   |

---

## 7. 3D 그래프 (추가)

| 기능                  | 코드 예시                                         | 설명                            |
|-----------------------|--------------------------------------------------|--------------------------------|
| 3D Axes 생성          | ```python<br>from mpl_toolkits.mplot3d import Axes3D<br>fig = plt.figure()<br>ax = fig.add_subplot(111, projection='3d')<br>``` | 3D 그래프 축 만들기              |
| 3D 산점도 그리기      | `ax.scatter(x, y, z)`                              | 3D 공간에 점 찍기                |
| 3D 선 그래프 그리기   | `ax.plot(x, y, z)`                                 | 3D 공간에 선 그리기              |

---

## 8. 참고 자료 및 커뮤니티

| 종류                | 링크/설명                                            |
|---------------------|----------------------------------------------------|
| 공식 문서           | [https://matplotlib.org/stable/contents.html](https://matplotlib.org/stable/contents.html) |
| 튜토리얼            | [https://matplotlib.org/stable/tutorials/index.html](https://matplotlib.org/stable/tutorials/index.html) |
| Stack Overflow      | https://stackoverflow.com/questions/tagged/matplotlib |
| 한국어 자료          | https://wikidocs.net/book/2160                      |

---

## 부록: 간단 예제 코드 모음

```python
import matplotlib.pyplot as plt

# 선 그래프
x = [1,2,3,4]
y = [10,20,25,30]
plt.plot(x,y)
plt.title("간단 선 그래프")
plt.show()

# 산점도
plt.scatter(x, y)
plt.title("산점도 예제")
plt.show()

# 막대 그래프
categories = ['A', 'B', 'C']
values = [5,7,3]
plt.bar(categories, values)
plt.title("막대 그래프 예제")
plt.show()
