# ip_lec24
Лабораторная 24. Responsive

1. В редакторе Sublime Text 3 создайте файл responsive-24-1.html со
следующим содержанием:
<!doctype html>
<html>
<head>
<title>Hello world!</title>
</head>
<body>
<p>Hello world!</p>
</body>
</html>

2. Откройте файл responsive-24-1.html в Google Chrome для мобильного
устройства. Увидим, что наша страница отобразится очень мелко.
Как видно, текст слишком мелкий для чтения, есть куча пустого
пространства, и для того, чтобы прочесть этот текст, нам нужно его
увеличивать приближением.

Проблема мобильных браузеров
При сравнении мобильных и десктопных браузеров наиболее очевидное различие — размер
экрана. Мобильные браузеры по-умолчанию отображают сайты, созданные для обычных
десктопных браузеров, гораздо хуже, чем могли бы: либо путем уменьшения масштаба, делая
текст и другой контент слишком мелким и нечитаемым (как в нашем варианте), либо
отображая лишь небольшую часть сайта, которая умещается на экране.
Если подумать логически, то в этом есть смысл: мобильный браузер видит страницу и
предполагает, что она создана для десктопной версии браузера, что верно для подавляющего
числа сайтов. Исходя из этого, этот браузер задает странице ширину 980px (Safari iPhone) и
пытается оптимально уместить ее на экране смартфона, отобразив в максимально
уменьшенном масштабе. Обычно ширина сайтов примерно такой и является, поэтому открыв
среднестатистическую веб-страницу на мобильном устройстве, она растянется на всю свою
ширину, но меньше в 2-3 раза своего оригинального размера.
Поэтому, если мы хотим оптимизировать сайт для смартфонов, этот вариант не катит. Нужно
каким-нибудь образом сообщить браузеру, что наша страница предназначена для
отображения на мобильных устройствах и задать правила для правильного поведения
области просмотра.
И вот как раз для этого мы и будем использовать мета-тег viewport, который был введен
компанией Apple и как обычно скопирован остальными.

3. Добавить в файл responsive-24-1.html следующий тег:
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
  
Задав мета-тегу viewport значение “device-width”, мы говорим браузеру,
что ширина области просмотра равняется ширине этого устройства, а не
стандартной ширине в 980px, как он может предполагать по-умолчанию. На
большом количестве смартфонов ширина экрана равняется 320px (в портретном
режиме). Можно задать самостоятельно ширину в 320px, что даст тот же
результат, но на некоторых смартфонах ширина экрана может быть другой,
поэтому самый оптимальный вариант — использовать device-width.

4. Откройте файл responsive-24-1.html в Google Chrome для мобильного
устройства. Увидим, что наша страница отобразится хорошо.

6. В редакторе Sublime Text 3 создайте файл responsive-24-2.html со
следующим содержанием:

<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Responsive Layout</title>
<style>
/********** Base styles **********/
* {
box-sizing: border-box;
}
h1 {
margin-bottom: 15px;
}
p {
border: 1px solid black;
background-color: #A52A2A;
width: 90%;
height: 150px;
margin-right: auto;
margin-left: auto;
font-family: Helvetica;
color: white;
}
/* Simple Responsive Framework. */
.row {
width: 100%;
}
/********** Large devices only **********/
@media (min-width: 1200px) {
.col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-
lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
float: left;
border: 1px solid green;
}
.col-lg-1 {
width: 8.33%;
}
.col-lg-2 {
width: 16.66%;
}
.col-lg-3 {
width: 25%;
}
.col-lg-4 {
width: 33.33%;
}
.col-lg-5 {
width: 41.66%;
}
.col-lg-6 {
width: 50%;
}
.col-lg-7 {
width: 58.33%;
}
.col-lg-8 {
width: 66.66%;
}
.col-lg-9 {
width: 74.99%;
}
.col-lg-10 {
width: 83.33%;
}
.col-lg-11 {
width: 91.66%;
}
.col-lg-12 {
width: 100%;
}
}
/********** Medium devices only **********/
@media (min-width: 950px) and (max-width: 1199px) {
.col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-
md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
float: left;
border: 1px solid green;
}
.col-md-1 {
width: 8.33%;
}
.col-md-2 {
width: 16.66%;
}
.col-md-3 {
width: 25%;
}
.col-md-4 {
width: 33.33%;
}
.col-md-5 {
width: 41.66%;
}
.col-md-6 {
width: 50%;
}
.col-md-7 {
width: 58.33%;
}
.col-md-8 {
width: 66.66%;
}
.col-md-9 {
width: 74.99%;
}
.col-md-10 {
width: 83.33%;
}
.col-md-11 {
width: 91.66%;
}
.col-md-12 {
width: 100%;
}
}
</style>
</head>
<body>
<h1>Responsive Layout</h1>
<div class="row">
<div class="col-lg-3 col-md-6"><p>Шаг 1</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 2 Это здорово!</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 3</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 4</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 5 Это здорово!</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 6</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 7</p></div>
<div class="col-lg-3 col-md-6"><p>Шаг 8</p></div>
</div>
</body>
</html>

6. Откройте файл responsive-24-1.html в Google Chrome для мобильного
устройства. Увидим, что страница не отображается одним столбцом.

8. Добавить в файл responsive-24-2.html следующий тег:
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
  
8. Откройте файл responsive-24-1.html в Google Chrome для мобильного
устройства. Увидим, что страница отображается одним столбцом.
