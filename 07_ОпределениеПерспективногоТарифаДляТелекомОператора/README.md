# Проект: Определение перспективного тарифа для телеком-компании

*Цель: Провести предварительный анализ поведения клиентов двух тарифов для определения наиболее выгодного для компании.*
Заказчиком предоставлены данные 500 пользователей «Мегалайна»: кто они, откуда, каким тарифом пользуются, сколько звонков и сообщений каждый отправил за 2018 год.

*Учебная задача: научиться...*
1. проводить статистический анализ, проверять статистические гипотезы;

## Программа исследования
- Все таблицы были успешно загружены, в данных нет пропусков и искажений
- Данные по пропущенным звонкам и нулевым сессиям данных соответсвуют методической сути явления и не требуют дополнительной обработки.
- В таблицы с данными по звонкам и интернет-траффику добавлена колонка с месяцем - требуется на последующих этапах.
- Проведено округление длительности звонков и интернет-траффика в большую сторону по логике тарифов.
- Для каждого пользователя вычислены:
	количество сделанных звонков и израсходованных минут разговора по месяцам;
	количество отправленных сообщений по месяцам;
	объем израсходованного интернет-трафика по месяцам;
	помесячная выручка с каждого пользователя.
- По каждому из тарифов:
	Построена гистрграмма дохода на пользователя
	Построены гистограммы распределения длительности звонков за месяц и боксплот активности пользователей по месяцам.
	Построены гистограммы распределения объёма интернет-траффика за месяц и боксплот интернет-активности пользователей по месяцам.
	Проверены статистические гипотезы о равенстве средней выручки между тарифами и между Москвой и регионами.

## Результаты
Проверены статистические гипотезы:
1. *Средняя выручка пользователей тарифов «Ультра» и «Смарт» различаются.*

	- Заёмщики без детей возвращают кредиты в срок на 1,5% чаще остальных.
	- Заёмщики с 3 детьми чуть более ответсвенны, чем с 1,2 и 4 детьми.
	- Выборка заёмщиков с 5 детьми слишком мала чтобы делать выводы.
	- В целом, заёмщики с детьми возвращают кредиты хуже чем заёмщики без детей.

2. *Средняя выручка пользователей из Москвы отличается от выручки пользователей из других регионов.*
	Данная гипотеза не подтверждается. В Москве медианное значение выше примерно на 160 рублей, но это различие статистически не значимо.

Общие выводы:
- Тариф "Смарт" привлекает более суетных и экономных людей, которые в итоге плятят больше ожидаемого. Эта категория пользователей эмоциональна, более склонна к смене тарифов и операторов, её необъодимо постянно привлекать и удерживать разными "фишками".
- Тариф "Ультра" привлекает платёжеспособных пользователей, предпочитающих предсказуемость и стабильность. Они не высчитывают копеечные выгоды. Данную категорию пользователей важно удерживать и не создавать для них стрессовые ситуации.
- Пользователей тарифа "Ультра" в два раза меньше, но они менее суетны и приносят соизмеримый объём выручки.

## Стек и применённые подходы
* pandas, seaborn, matplotlib, numpy, scipy