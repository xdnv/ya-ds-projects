# Проект: Защита персональных данных клиентов

*Цель: Разработать алгоритм преобразования данных клиентов страховой компании с сохранением качества обучения моделей.*
Нужно защитить данные клиентов страховой компании «Хоть потоп».
Разработайте такой метод преобразования данных, чтобы по ним было сложно восстановить персональную информацию. Обоснуйте корректность его работы.

Нужно защитить данные, чтобы при преобразовании качество моделей машинного обучения не ухудшилось. Подбирать наилучшую модель не требуется.

*Учебная задача: научиться...*
1. использовать линейное преобразование данных в машинном обучении;
2. использовать метрику качества модели R2.

## Программа исследования
- Данные загружены;
- проведён предварительный анализ и предобработка;
- провести теоретические выкладки преобразования данных;
- подтвердить их на практике;

## Результаты
- Пропуски в данных не выявлены
- Удалены 153 дубликата строк (3% от выборки)
- Преобразован тип данных фактора "Возраст" в целочисленный
- Распределения факторов соответствуют их физическому смыслу, выбросы не выявлены
- Значимые корреляции между факторами не выявлены
- С помощью аппарата линейной алгебры обоснован ответ на вопрос по умножению данных на обратимую матрицу.
- Определён алгоритм такого умножения и проверки качества моделей до и после кодирования данных:
	- Умножение обучающих факторов X на случайно сгенерированную обратимую квадратную матрицу P. Размерность обратимой матрицы определяется числом факторов, в текущем случае это 4х4.
	- По исходным и закодированным с помошью умножения на матрицу P данным обучается модель линейной регрессии и оценивается её качество с помощью метрики R2.
	- Метрики R2 в обоих случаях должны пренебрежимо различаться или быть равны.
	- Алгоритм проверен на практике, теоретические оценки подтвержедны на практике.

Итоговый вывод: кодирование данных с помощью умножения на обратимую матрицу не снижает предсказательные возможности модели линейной регрессии и может быть использовано в работе.

## Стек и применённые подходы
* pandas, matplotlib, seaborn, sklearn