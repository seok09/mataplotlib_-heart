import matplotlib.pyplot as plt
import numpy as np

# 파라메트릭 변수 t 생성
t = np.linspace(0, 2 * np.pi, 1000)

# 하트 방정식 좌표 계산
x = 16 * np.sin(t)**3
y = 13 * np.cos(t) - 5 * np.cos(2*t) - 2 * np.cos(3*t) - np.cos(4*t)

# 그래프 그리기
plt.figure(figsize=(6,6))
plt.plot(x, y, color='red', linewidth=2)
plt.fill(x, y, color='pink', alpha=0.6)  # 하트 내부 색 채우기

plt.axis('off')  # 축 숨기기
plt.title("❤️ 하트 모양 그래프", fontsize=16)
plt.show()
