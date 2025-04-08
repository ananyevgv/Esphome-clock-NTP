

# Часы с синхронизацией времени и автоматической регулировкой яркости

[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2025.3&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/


| clock-1                                                    | clock-2                                                   | clock-3                                    |
|------------------------------------------------------------|-----------------------------------------------------------|--------------------------------------------|
| ![clock-1](https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-1/1639051819484.jpg) | ![clock-2](https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-2/1639051819490.jpg) | ![clock-3](https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-3/33.jpg) |



Основная идея избавится от дополнительных устройств для измерения различных параметров, концепция все в одном устройстве в виде часов. 
В китайских часах дисплеи стоят к верх ногами, пришлось переворачивать т.к точка на часах попадала не туда.

Версия 1 
==========

Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, качества воздуха, отображение нахождения солнца над горизонтом, RF315M, интернет радио (jukebox-card).

Дисплейный модуль построен на двух TM1637 т.к. в часах стоят 7-ми сегментные 4 разрядные индикаторы с общим анодом (MAX7219 общий катод). Для подключения индикатора влажности используется незадействованный 5 и 6 разряд TM1637. Значок влажности подключен 6 разряду и DP 2-го TM1637

<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-1/1639051819484.jpg" height="300" alt="Часы">

Версия 2
==========
Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, температуры пола, PZEM AC, ИК пульт (для включения ТВ), датчик атмосферного давления + отображение нахождения солнца над горизонтом.

Дисплейный модуль построен на трех TM1637 т.к. в часах стоят 7-ми сегментные 4 разрядные индикаторы с общим анодом (MAX7219 общий катод). Значок влажности подключен к 3 разряду и DP 3-го TM1637. 

<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-2/1639051819490.jpg" height="300" alt="Часы">

Версия 3
==========

Часы с синхронизацией времени и автоматической регулировкой яркости + датчики температуры, влажности, температуры пола, датчик расхода фильтрованной воды  и температуры, ИК пульт (для включения ТВ). 

<img src="https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/clock-3/33.jpg" height="300" alt="Часы">

Дисплейный модуль построен на трех MAX7219 общий катод. Задуманы для крепления под кухонный гарнитур. 3D модель корпуса в папке clock-3.

7-ми сегментный 4 разрядный индикатор для отображения времени собран из светодиодов с использованием корпуса от индикатора от старых часов VST. Питание на каждый модуль MAX7218 не стоит включать последовательно, лучше подключать на прямую от ESP особенно "+" (можно получить разную яркость).


Wemos D1 mini pin D8  для подключения TM1637 и MAX7219 не использовать! 

На home assistant установлен адон Chrony https://github.com/hassio-addons/addon-chrony 


Будильник 
==========
используется сторонний компонент dynamic_on_time https://github.com/hostcc/esphome-component-dynamic-on-time
DF-Player, BME-680.

[Умные часы будильник](https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/smart-time.yaml)



max7219
==========

[Часы с эффектом перелистывания цифр](https://github.com/ananyevgv/Esphome-clock-NTP/blob/main/max7219.yaml)
