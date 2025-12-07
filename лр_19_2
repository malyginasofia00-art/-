import pandas as pd
import numpy as np

# 1) Зчитування двовимірного масиву з файлу temp.txt
# Припустимо, що числа розділені пробілами
data = np.loadtxt("temp.txt", dtype=int)

# Перетворення у одновимірний масив
flat = data.flatten()

# Запис у Series
s = pd.Series(flat)

# 2) Видалення повторів
s = s.drop_duplicates().reset_index(drop=True)

# 3) Додавання 6 випадкових чисел у діапазоні [0;25]
random_numbers = np.random.randint(0, 26, size=6)
s = pd.concat([s, pd.Series(random_numbers)], ignore_index=True)

# 4) Збереження у файл fin.txt
s.to_csv("fin.txt", index=False, header=False)

print("Файл fin.txt успішно створено.")
