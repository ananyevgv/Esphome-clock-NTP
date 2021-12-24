Часы с синхронизацией времени и автоматической регулировкой яркости
========================

<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/cloc-f.jpg" height="300" alt="Часы">
<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clok-t.jpg" height="300" alt="Обратная сторона">
<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/dat.jpg" height="500" alt="Срин датчиков">   

Основная идея избавится от дополнительных устройст для измерения различных параметров, концепция все в одном устройстве в виде часов. 
На фото clok2. В китайских часах дисплеи стоят кверх ногами, пришлось переворачивать т.к точка на часах попадала не туда.

Версия 1 
==========

Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, качества воздуха. В планах добавить RF передатчик (в пути).
Дисплейный модуль построен на двух TM1637 т.к. в часах стоят 7-ми сегментные индикаторы с обшим анодом (MAX7218 общий катод). Для подключения индикатора влажности используется незадействованый 5 и 6 сегмент TM1637. Значек влажности подключен 6 сегменту и DP 2-го TM1637

Версия 2
==========
Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, температуры пола, PZEM AC, ИК пульт (для включения ТВ), датчик давления.
Дисплейный модуль построен на трех TM1637 т.к. в часах стоят 7-ми сегментные индикаторы с обшим анодом (MAX7218 общий катод). Значек влажности подключен к 3 сегменту и DP 3-го TM1637. 

Версия 3
==========
Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, температуры пола, датчик расхода фильтрованой воды  и температуры, ИК пульт (для включения ТВ) + Opentherm  для управления котлом. Дисплейный модуль построен на трех MAX7218 общий катод. Задуманы для крепления под кухонный гарнитур. 3D модель корпуса в папке clock-3. Дисплей собран из светодиодов с исполъзованием корпуса от дисплея от старых часов VST. (Часы в процессе отладки).


Wemos D1 mini pin D8  для подключения TM1637 и MAX7218 не использовать! 


Сылки на компоненты
========================

https://aliexpress.ru/item/1005002292394381.html (часы которые переделывал)

https://aliexpress.ru/item/32649468489.html (esp8266)

https://aliexpress.ru/item/32846977179.html (шилд)

https://aliexpress.ru/item/32910027894.html (шилд2)

https://aliexpress.ru/item/1005001391696335.html (AC-DC)

https://aliexpress.ru/item/32805933184.html (TM1638)

https://aliexpress.ru/item/4000055635431.html (AHT10)

https://aliexpress.ru/item/4000587263111.html (BH1750)

https://aliexpress.ru/item/4000252589302.html (RJ-12)

https://aliexpress.ru/item/32861772061.html (IR)
