# 

# 🌟 Анализ данных о звёздах (EDA)

## 📌 Описание задачи  
Целью данного проекта является **разведочный анализ данных (EDA)**, содержащих характеристики звезд. Основная задача — понять структуру данных, выявить выбросы, связи между переменными и подготовить их для дальнейшего машинного обучения.

## 📂 Датасет
Файл **`train_var_1.csv`**, содержащий информацию о звездах, был загружен и исследован. В датасете представлены следующие переменные:

| Переменная | Описание |
|------------|-----------|
| `Vmag` | Видимая величина звезды (яркость звезды, измеренная с Земли) |
| `Plx` | Параллакс (используется для измерения расстояния до звезды) |
| `e_Plx` | Погрешность измерения параллакса |
| `B-V` | Цветовой индекс (разница между яркостью в синем и видимом свете) |
| `SpType` | Спектральный тип звезды |
| `Amag` | Абсолютная величина звезды (истинная яркость звезды) |
| `TargetClass` | Класс звезды (0 или 1) |

## 📊 Выполненные задания  

### **1️⃣ Диаграмма разброса (`Vmag` vs `e_Plx`)**  
✅ Построен **scatterplot**, показывающий зависимость между видимой яркостью и погрешностью параллакса.  
📌 **Вывод:** Чем ярче звезда (`Vmag` ниже), тем меньше `e_Plx` (измерение точнее).

![Диаграмма Разброса](1.jpg)

### **2️⃣ Анализ пропущенных значений**  
✅ Проверены и **визуализированы** пропущенные значения.  
📌 **Вывод:** В датасете **нет пропусков**, что упрощает анализ.


### **3️⃣ Boxplot для всех числовых переменных**  
✅ Построены **диаграммы boxplot** для оценки выбросов.  
📌 **Вывод:** В переменных `Plx` и `e_Plx` обнаружены выбросы, возможно, из-за ошибок измерений.

![boxplot1](boxplot1.jpg)
![boxplot2](boxplot2.jpg)
![boxplot3](boxplot3.jpg)
![boxplot4](boxplot4.jpg)
![boxplot5](boxplot5.jpg)


### **4️⃣ Barplot для `TargetClass`**  
✅ Построен **график распределения классов**.  
📌 **Вывод:** **Данные сбалансированы**, классы 0 и 1 представлены примерно одинаково.

### **5️⃣ Матрица корреляции**  
✅ Построена **корреляционная матрица** для числовых переменных.  
📌 **Вывод:**  
- `Vmag` и `Amag` сильно коррелируют → оба описывают яркость.  
- `Plx` и `Vmag` имеют **слабую отрицательную корреляцию** → далекие звезды слабее видны.  
- `e_Plx` (погрешность) **не связана** с другими параметрами → ошибки измерения случайны.

### **6️⃣ Графики парных зависимостей (pairplot)**  
✅ Построены **диаграммы рассеяния** между ключевыми переменными.  
📌 **Вывод:**  
- `Vmag` и `Amag` имеют линейную связь.  
- `Plx` (расстояние) влияет на яркость, но не всегда очевидно.  
- Есть **выбросы в `Plx`**, которые могут быть аномальными объектами.

### **7️⃣ График распределения `Plx`**  
✅ Построен **гистограммный график**.  
📌 **Вывод:**  
- Большинство звезд **далекие** (`Plx` мал).  
- Есть несколько **очень близких звезд** (высокий `Plx`).

---

## 🔍 **Основные выводы**
1️⃣ В данных **нет пропущенных значений**, что удобно для машинного обучения.  
2️⃣ **Яркость (`Vmag`, `Amag`) и расстояние (`Plx`) связаны**, но есть аномалии.  
3️⃣ **Есть выбросы в `Plx` и `e_Plx`**, которые стоит изучить подробнее.  
4️⃣ **Корреляция между `Vmag` и `Amag` очень сильная**, возможно, один параметр можно исключить.  
5️⃣ **Распределение звезд по `Plx` показывает, что большинство из них находятся далеко.**  

🚀 **Этот анализ поможет лучше понять данные и подготовить их для дальнейшего моделирования!**
