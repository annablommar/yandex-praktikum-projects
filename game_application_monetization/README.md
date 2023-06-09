# Анализ и монетизация игрового приложения Космические братья

## Данные
В наличии были следующие данные:

Информация о действиях, совершенных в игре:
* Время события;
* Одно из трёх событий:
* Объект построен,
* Первый уровень завершён,
* Проект завершён;
* Один из трёх типов здания:
* Сборочный цех,
* Космопорт,
* Исследовательский центр;
* Идентификатор пользователя;
* Тип реализованного проекта;

Информация с расходами:
* День, в который был совершен клик по объявлению
* Источник трафика
* Стоимость кликов

Информация об источнике привлечения пользователей:
* Идентификатор пользователя
* Источник, откуда пришёл пользователь, установивший приложение

## Задача
Сформировать модель монетизации игрового приложения, помочь бизнесу выбрать оптимальный момент для запуска рекламы, зная расходы на продвижение игры и доходы от показа рекламы равные 0,07. Реклама может быть показана на экране в момент выбора типа объекта для постройки (сборочный цех, космопорт или исследовательский центр), возможен полный или частичный показ рекламы при постройке какого-либо объекта из трех возможных.

## Используемые библиотеки	
pandas
datetime
scipy
plotly

## Выводы
* Чтобы пользователь смог немного втянуться в игру до того, как ему начнут показывать рекламу, и при этом создатели игры не ушли за точку безубыточности и не терпели убытки, будем снимать 1 показ с первой постройки assembly_shop каждым привлеченным игроком, при этом прибыль составит 403
* По количеству построек больше всего было построено космопортов, затем сборочных цехов, и меньше всего исследовательских центров
* Все привлеченные пользователи построили сборочный цех, меньше всего пользователей построило исследовательский центр
* Большее количество игроков завершило первый уровень победой над врагом (3951 пользователей) по сравнению с завершением проекта постройки (1866 пользователей)
* Отвергаем гипотезу о том, что нет различий между средним временем прохождения первого уровня пользователями, которые заканчивают уровень через реализацию проекта, и пользователями, которые заканчивают уровень победой над другим игроком.
* Больше всего пользователей, закончивших первый уровень, пришло из yandex_direct и instagram_new_adverts. В целом такая же градация по каналам наблюдается в разбивки по всем привлеченным пользователям
* Не можем отвергнуть гипотезу о том, что нет различий между средним количеством зданий, построенных пользователями, закончившими первый уровень и привлеченными из канала yandex direct, и средним количеством зданий, построенных пользователями, закончившими первый уровень и привлеченными из канала instagram_new_adverts.