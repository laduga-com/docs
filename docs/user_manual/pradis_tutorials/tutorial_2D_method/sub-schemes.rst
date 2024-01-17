Методические указания по работе с Подсхемами
============================================

Программный комплекс для автоматизации моделирования нестационарных процессов
в механических системах и системах иной физической природы

Оглавление
-----------

Подсхемы – механизм в ПК PRADIS, который позволяет моделировать
любую иерархию любой сложности.

Рассмотрим на примере.
Создадим проект subScheme в папке DINAMA/examples/.
Создадим подсхему (рисунок 1)

.. image:: media/sub-schemes1.png
      :width: 5in
      :height: 3in

| Рисунок 1. Подсхема
| Компоненты TrapeziumSource и Lag1 берем из модуля Signals, а индикатор V, порт подсхемы P и блок Data из модуля base.

Зададим свойства компонента DISP (рисунок 2)

.. image:: media/sub-schemes2.png
      :width: 4in
      :height: 2in

Рисунок 2. Свойства компонента DISP

Зададим свойства компонента TrapeziumSource (рисунок 3)

.. image:: media/sub-schemes3.png
      :width: 5in
      :height: 3in

| Рисунок 3. Свойства компонента TrapeziumSource
| Продолжительность цикла CT – это параметр, который нужно будет рассчитывать. CT = D + FT + HT + BT. Так как все слагаемые, кроме D, равны 1, блок | Data будет выглядеть как на рисунке 4

.. image:: media/sub-schemes4.png
      :width: 5in
      :height: 3in

| Рисунок 4. Параметр C
| Сохраняем этот файл под названием generator.sch в нашем проекте
| subSheme (рисунок 5):

.. image:: media/sub-schemes5.png
      :width: 5in
      :height: 3in

Рисунок 5. Сохранение файла generator.sch

| Активный уровень VH и Начальная задержка D – это параметры, которые нужно добавить в подсхему. 
| Для этого переходим с помощью ПКМ в режим
| «Изменить обозначение схемы» (рисунок 6) или F9.

.. image:: media/sub-schemes6.png
      :width: 5in
      :height: 3in

Рисунок 6. Переход в режим «Изменить обозначение схемы»

После перехода в режим изменения обозначения подсхемы на экране будет следующее (рисунок 7)

.. image:: media/sub-schemes7.png
      :width: 5in
      :height: 3in

Рисунок 7. Изменение обозначения подсхемы

Для добавления необходимых параметров двойным нажатием ЛКМ на названии SUB открываем изменение свойств модуля (рисунок 8)

.. image:: media/sub-schemes8.png
      :width: 5in
      :height: 3in

Рисунок 8. Изменение свойств модуля SUB

С помощью нижних полей добавляем необходимые параметры (рисунок 9)

.. image:: media/sub-schemes9.png
      :width: 5in
      :height: 3in

Рисунок 9. Добавление необходимых параметров

Далее нарисуем иконку. Используем компонент Стрелка из модуля рисунки окна «Компоненты» (рисунок 10, 11)

.. image:: media/sub-schemes10.png
      :width: 5in
      :height: 3in

Рисунок 10. Компонент стрелка в модуле «рисунки»

.. image:: media/sub-schemes11.png
      :width: 5in
      :height: 3in

Рисунок 11. Использование стрелки для прорисовки иконки

Сохраняем и возвращаемся в предыдущий режим через ПКМ (рисунок 12)

.. image:: media/sub-schemes12.png
      :width: 5in
      :height: 3in

Рисунок 12. Переход в предыдущий режим

Далее создадим большую схему. Для этого создаем новый файл с названием big_scheme.sch (рисунок 13)

.. image:: media/sub-schemes13.png
      :width: 5in
      :height: 3in

Рисунок 13. Создание файла big_scheme.sch

В модуле base окна «Компоненты» выберем компонент Подсхема и поместим на рабочем поле (рисунок 14)

.. image:: media/sub-schemes14.png
      :width: 5in
      :height: 3in

.. image:: media/sub-schemes15.png
      :width: 5in
      :height: 3in

Рисунок 14. Компонент «Подсхема»

В свойствах компонента через кнопку просмотр выбираем generator.sch (рисунок 15)

.. image:: media/sub-schemes16.png
      :width: 5in
      :height: 3in

Рисунок 15. Добавление созданной подсхемы
| На рабочем поле появится генератор, который был только что создан с теми свойствами, которые были заданы (рисунок 16)

.. image:: media/sub-schemes17.png
      :width: 5in
      :height: 3in

| Рисунок 16. Генератор с заданными свойствами
| Далее на рабочее поле добавим второй генератор, зададим им параметры.
| Также добавим 2 блока DISP и блок Dynamic (рисунок 17)

.. image:: media/sub-schemes18.png
      :width: 5in
      :height: 3in

Рисунок 17. Добавление необходимых блоков на рабочее поле

.. image:: media/sub-schemes19.png
      :width: 5in
      :height: 3in

Рисунок 18. Свойства DISP1  

.. image:: media/sub-schemes20.png
      :width: 5in
      :height: 3in

| Рисунок 19. Свойства DISP2  
| В блоке Dynamic меняем свойсво end и свойство prttime (рисунок 20)

.. image:: media/sub-schemes21.png
      :width: 5in
      :height: 3in

.. image:: media/sub-schemes22.png
      :width: 5in
      :height: 3in

Рисунок 20. Параметры решателя

.. image:: media/sub-schemes23.png
      :width: 5in
      :height: 3in

Сохраняем и нажимаем моделировать (рисунок 21,22)

.. image:: media/sub-schemes24.png
      :width: 5in
      :height: 3in

Рисунок 21. График для подсхемы 1

.. image:: media/sub-schemes25.png
      :width: 5in
      :height: 3in

| Рисунок 22. График для подсхемы 2
| Очевидно, что график для подсхемы 2 (рисунок 22) сдвинут на единицу относительно графика для подсхемы 1 (рисунок 21).
| Теперь представим большую схему как подсхему. Изменим ее как на рисунке 23

.. image:: media/sub-schemes26.png
      :width: 5in
      :height: 3in

| Рисунок 23. Схема big_scheme.sch с сумматором
| Создадим файл новой схемы и сохраним под названием scheme.sch (рисунок 24)

.. image:: media/sub-schemes27.png
      :width: 5in
      :height: 3in

| Рисунок 24. Сохранение файла scheme.sch
| Добавляем компонент Подсхема и в свойствах указываем big_scheme.sch (рисунок 25)

.. image:: media/sub-schemes28.png
      :width: 5in
      :height: 3in

.. image:: media/sub-schemes29.png
      :width: 5in
      :height: 3in

| Рисунок 25. Компонент SUB1 и его свойства
| Также добавляем индикатор, блок DISP и блок Dynamic (рисунок 26)

.. image:: media/sub-schemes30.png
      :width: 5in
      :height: 3in

Рисунок 26. Добавление необходимых компонентов

.. image:: media/sub-schemes31.png
      :width: 5in
      :height: 3in

Рисунок 27. Свойства DISP

.. image:: media/sub-schemes22.png
      :width: 5in
      :height: 3in

.. image:: media/sub-schemes22.png
      :width: 5in
      :height: 3in

Рисунок 28. Свойства Dynamic

.. image:: media/sub-schemes23.png
      :width: 5in
      :height: 3in

Сохраняем и нажимаем моделировать


.. image:: media/sub-schemes32.png
      :width: 5in
      :height: 3in

| Рисунок 29. Результат
| Видно, что на графике получилась сумма графиков, которые изображены на рисунках 21 и 22.

