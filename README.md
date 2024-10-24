# Вот оно — счастье!

**World Happiness Report** (Доклад о мировом счастье) — ежегодная публикация, призванная оценить субъективное благополучие людей по всему миру. Доклад выпускается Sustainable Development Solutions Network (Сеть по поиску решений в области устойчивого развития), глобальной инициативой, запущенной Организацией Объединенных Наций в 2012 году.

Оценки качества жизни, полученные в ходе всемирного опроса *Gallup*, служат основой для ежегодного рейтинга счастья. Они основаны на ответах на главный вопрос об оценке качества жизни. В шкале *Cantril* респондентам предлагается представить лестницу, на которой 10 — это наилучшая возможная жизнь, а 0 — наихудшая возможная жизнь. Затем их просят оценить свою текущую жизнь по шкале от 0 до 10. Рейтинги составляются на основе репрезентативных общенациональных выборок за три года.

Также отчете используется ряд факторов для измерения счастья, включая доход, социальную поддержку, ожидаемую продолжительность жизни, свободу выбора жизненного пути, щедрость и восприятие коррупции.

## Идея проекта
Идея нашего проекта заключается в том, чтобы на основе данных, полученных в опросе 2024 года, составить различные графики, которые будут наглядно отображать информацию, а также на основе построенных графических материалов провести небольшой анализ.

Для этого мы использовали датасет, который нашла на платформе **Kaggle**.

Ссылка на датасет: https://www.kaggle.com/datasets/jainaru/world-happiness-report-2024-yearly-updated/data

## Что содержит датасет?
- `Country name`: Название страны.
- `Regional indicator`: Регион, в которых входит страна.
- `Ladder score`: Индекс счастья для каждой страны, основанный на ответах на вопрос Cantril о лестнице.
- `Upper whisker`: Максимальное значение индекса с учетом погрешности.
- `Lower whisker`: Минамальное значение индекса с учетом погрешности.
- `Log GDP per capita`: Натуральный логарифм ВВП страны на душу населения, скорректированный на паритет покупательной способности (ППС) для учета различий в стоимости жизни между странами.
- `Social support`: Среднее по стране количество бинарных ответов (либо 0, либо 1, что означает "Нет" / "Да") на вопрос о том, есть ли у вас родственники или друзья, на которых можно положиться в трудную минуту.
- `Healthy life expectancy`: Среднее количество лет, которое новорожденный младенец прожил бы в здоровом состоянии, исходя из показателей смертности и ожидаемой продолжительности жизни в разном возрасте.
- `Freedom to make life choices`: Среднее значение ответов по стране на вопрос об удовлетворенности свободой выбирать, что делать со своей жизнью.
- `Generosity`: остаток от регрессии среднего показателя по стране по ответам на вопрос о пожертвовании денег на благотворительность по отношению к ВВП на душу населения.
- `Perceptions of corruption`: Среднее значение ответов на вопросы опроса по стране о предполагаемых масштабах коррупции в правительстве и бизнесе.
- `Dystopia + residual`: Антиутопия - это воображаемая страна с наименее счастливыми людьми в мире, используемая в качестве ориентира для сравнения. Оценка "Антиутопия + остаточный балл" представляет собой комбинацию оценки "Антиутопия" и необъяснимого остаточного балла для каждой страны, гарантируя, что совокупный балл всегда положительный. Каждый из этих факторов вносит свой вклад в общий балл счастья, но остаточное значение "Антиутопия +" является эталоном, который гарантирует, что ни одна страна не получит более низкий балл, чем гипотетическая Антиутопия.

## Задачи проекта:
С помощью графиков, барплотов, круговых диаграмм и диаграмм рассеивания:
1. Узнать какие регионы мира были самыми "счастливыми", а какие самыми "несчастными" в 2024 году
2. Составить топ-10 самых "счастливых" и самых "несчастных" стран
3. Проанализировать показатели, влияющие на индекс счастья в регионах и отдельных странах
4. Узнать какое место занимает Россия по индексу счастья среди своего региона

## Результаты

В данном проекте были определены самые **"счастливые"** и самые **"несчастные"** регионы мира в 2024 году, а также проанализирован топ-10 самых "счастливых" и топ-10 самых "несчастных" стран путем изучения влияния различных факторов, таких как щедрость, восприятие коррупции и продолжительность жизни на индекс счастья. Отдельно была изучена зависимость уровня счастья от ВВП. Индекс счастья в России сравнивался с индексом в  странах Содружества Независимых Государств. Данные были визуализированы при помощи барплотов, круговых диаграмм, графиков и диаграмм рассеяния. В результате были сформированы следующие **выводы**:

1) Самые "счастливые" регионы мира - Западная Европа, Северная Америка и Австралия с Новой Зеландией, самый "несчастный" регион - Южная Азия
2) В **топ-10 самых "счастливых" стран** входят Финляндия, Дания, Исландия, Швеция, Израиль, Нидерланды, Норвегия, Люксембург, Швейцария и Австралия. В них наблюдается наиболее высокая высокая продолжительность жизни, а также высокий уровень восприятия коррупции. 
3) Чем выше ВВП на душу населения, тем выше индекс счастья
4) В **топ-10 самых "несчастных"стран** входят Эсватини, Замбия, Малави, Ботсвана, Зимбабве, Конго, Сьерра-Леоне, Лесото, Ливан и Афганистан. В них наблюдается низкая продолжительность жизни и низкий уровень восприятия коррупции.
5) Уровень щедрости в странах почти не оказывает влияния на индекс счастья
6) Среди стран Содружества Независимых Государств Россия занимает 4 место по индексу счастья после Узбекистана, Казахстана и Молдовы.

## Авторы проекта

- Кокурина Екатерина — идейный вдохновитель, специалист по использованию сложных функций
- Рыбакова Вита — дизайн-менеджер, продвинутый пользователь матплотлиба

НИУ ВШЭ, ФГиГТ, 2 курс, группа БГЕО232
