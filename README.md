# CV_4
На основе ноутбука с примером из лекции (segmentation.ipynb) написать свою версию Unet (заготовка для задачи - segmentation_by_hands.ipynb) - слои должны создаваться вручную, работа ведется с датасетом oxford_iiit_pet. Глобально менять архитектуру сети нельзя. Можно добавлять слои (но только вручную), менять функции активации, функцию ошибки, размеры batch и количество эпох. Цель - добиться от нейросети из segmentation_by_hands точности не ниже, чем для нейросети из segmentation при 20 эпохах.

1.Имортируем нужные библиотеки и подгружаем датасет

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/1.jpg)

2.Загружаем и нормализуем изображения

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/2.jpg)

3.Задаем параметры для обучения модели и загружаем обучающие и тестовые изображения

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/3.jpg)

4.Класс Augment, который предназначен для аугментации (расширения) данных перед обучением модели

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/4.jpg)

5.Визуализируем случайное изображение и его маску из обучающего набора данных, чтобы получить представление о том, как выглядят данные.

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/5.jpg)

6.Определение модели U-Net для сегментации изображений

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/6.jpg)

7.Визуализация архитектуры модели в виде графа
	tf.keras.utils.plot_model(model, show_shapes=True)

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/7.jpg)

8.Создания маски сегментации из прогнозируемых масок и визуализация предсказаний модели на изображениях

![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/8.jpg)

9.Обучения модели


![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/9.jpg)

10. Реузльтат
![Image alt](https://github.com/dnlqwer/CV_4/blob/main/pic/10.jpg)

