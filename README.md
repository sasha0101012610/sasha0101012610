- 👋 Hi, I’m @sasha0101012610
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
sasha0101012610/sasha0101012610 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import numpy as np
import matplotlib.pyplot as plt

# Задаем параметры
R1 = 200
R2 = 100
R3 = 300
C = 0.405 * 10**(-6)
L = 37 * 10**(-3)
Uo = 3

# Временной интервал
t = np.arange(0, 0.005, 0.00001)

# Вычисление значений IL(t) и Uc(t)
IL = (Uo - R1 * (Uo - 3*t))/(R1 + R3)
UC = (Uo - IL*R1)/R2

# Построение графика
plt.plot(t, IL, label='IL(t)')
plt.plot(t, UC, label='Uc(t)')
plt.xlabel('Время, с')
plt.ylabel('Значение')
plt.title('График IL(t) и Uc(t)')
plt.grid(True)
plt.legend()
plt.show()
