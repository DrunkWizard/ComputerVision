# ComputerVision

## Цель работы
Разработка метода сегментации изображения неба по четырем классам,
основанного на использовании глубокой сверточной нейронной сети
## Датасет
https://github.com/CV-Application/WSISEG-Database
Изначальный датасет был расчитан на сегментацию по трем классам,
мы доработали его в программе XnView (https://www.xnview.com/en/), 
выделив еще один класс
## Инструменты
Использовали язык python, библиотеку matplotlib для визуализации результата. 
Также использовали библиотеку https://github.com/divamgupta/image-segmentation-keras,
которая реализует различные стандартные модели нейронных сетей для сегментации изображения 
и построенна на основе tensorflow и keras 
## Реалзиация
В качестве архитектуры нейронной сети была выбрана модель SegNet.
Было произведено 40 эпох обучения по 512
итераций в каждой. Суммарное время обучения сети составило приблизительно
25 часов. Среднее значение точности сегментации на тренировочной выборке
во время сороковой эпохи обучения составило 95,74%.

![График зависимости средней взвешенной точности сегментации на тренировочный выборке от номера текущей эпохи](https://github.com/DrunkWizard/ComputerVision/blob/master/График.jpg)

График зависимости средней взвешенной точности сегментации на тренировочный выборке от номера текущей эпохи
## Результаты тестирования 
| Класс         |    Accuracy   | Precision | Recall | F-score|
| ------------- | ------------- | --------- | ------ | ------ |
| Чистое небо  | 89,42%  | 94,07% | 94,76% | 94,42% |
| Облака | 88,81% | 94,46% | 93,70% | 94,08% |
| Солнце | 59,77% | 79,16% | 70,94% | 74,82% |
| Другие объекты | 98,53% | 99,17% | 99,35% | 99,26% |
|  |  |  |  |  |
| Среднее взвешенное | 92,24%  | 95,88% | 95,89% | 95,88% |
| Среднее по классам  | 84,14% | 91,71% | 89,69% | 90,64% |
