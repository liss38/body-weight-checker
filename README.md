### Общее

Использовать NativeJS, html/css(возможно UI CSS-фреймворк), в качестве хранение данных JSON-формат, данные забиваются впучную в JSON-файлы через редактор

Одна страница без раздела/роутинга, на которой при старте отображается понедельный график изменения массы, переключалка масштабов графика, чекбоксы для отображения минимальной/максимальной/средней массы(всё это отдельные слои столбиков на графике), критические минимальное и максимально-допустимое значения для контроля перегибов, возможность отобразить данные в виде списка или таблицы

В качестве отрисовки графика использовать canvas, 
масштаб графика день(самый крупный), неделя, месяц, год.

Начиная с маштаба "неделя", оценка веса поределяется тремя величинами: 
 - минимальное значение в единицу времени
 - среднее значение в единицу времени
 - максимальное значение в единицу времени

Визуально график/диаграма похож на график успещности актера в кинопоиске, либо это столбиковая диаграмма

В качестве источника данных использовать JSON-формат, на каждый год свой отдельный JSON-формата, в проекте это может быть реализовано так:
```
...
	/src/data/simple-weight-list/2020.json
	/src/data/simple-weight-list/2021.json
	/src/data/simple-weight-list/2022.json
```

Использовать данные начиная с 2020 года

В идеале(? 2021 год) сделать внешнюю публикацию и перевести на андроид-приложение(React Native)





#### API


(1)
/simple-weight-list

```
[
	{
		id: `#2020#12#1`,
		weightValue: 75.2
	}
]
```

"Простой(линейный) список замеров веса тела"

`simple-weight-list.json`

Массив из плоских объектов(POD), каждый объект имеет два поля:

`id` - уникальный ключ по маске `#<год>#<индекс_недели_года>#<индекс_дня_недели>`
`weightValue` - вес тела в килограммах, вещественное число с одним знаком после запятой




### @TODO. Прогресс реализации

**(Подготовка)**
[+] - npm init
[-] - webpack config
[-] - src-структура
[-] - src/data/simple-weight-list/2020.json занесение данных за 2020-й год


**(Черновая разработка)**
[-] - fetch(или import ?) для json'а с данными 
[-] - отображение данных просто тексто-списком в html-странице
[-] - функция подсчета минимальных/средних/максимальных значений за неделю
[-] - отображение этих значений ввиде таблицы(просто без изысков)
[-] - 
[-] - 


**(Промежуточный рефакторинг)**
[-] - 
[-] - 
[-] - 


**(Отрисовка графика)**
[-] - 
[-] - 
[-] - 


**(Чистовая разработка)**
[-] - 
[-] - 
[-] - 