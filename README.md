# Neurotechnologies-Project

# АННОТАЦИЯ
  Распознавание эмоций речи является важной задачей в обработке естественного языка с многочисленными приложениями, такими как улучшение пользовательского опыта в виртуальных помощниках или повышение эффективности диагностики здоровья ума. В этой статье мы сравниваем производительность трех популярных методов машинного обучения - случайного леса (RFC), сверточной нейронной сети (CNN) и рекуррентной нейронной сети (RNN) - для распознавания эмоций речи с использованием набора данных RAVDESS. Мы реализуем и обучаем каждую модель с использованием соответствующих алгоритмов оптимизации и оцениваем их производительность с помощью различных метрик, включая точность, F1-оценку и матрицу смежности. Наши результаты показывают, что CNN и RNN превосходят RFC по общей производительности, а CNN достигает лучших результатов. Мы также наблюдаем, что модели работают по-разному на разных эмоциях, некоторые из которых легче распознавать, чем другие. Наши находки предоставляют инсайты в относительные сильные и слабые стороны этих техник для распознавания эмоций речи и указывают направления для будущих исследований.

# 1. АНАЛИЗ ПРЕДМЕТНОЙ ОБЛАСТИ
  Распознавание эмоций речи (SER) является областью обработки естественного языка (NLP), которая стремится идентифицировать и классифицировать эмоциональное состояние говорящего на основе его речи. Оно имеет широкий спектр потенциальных приложений, включая улучшение пользовательского опыта в виртуальных помощниках, повышение эффективности диагностики здоровья ума и улучшение сервиса клиента в колл-центрах.
Одним из основных вызовов в SER является неустойчивость эмоций, которая может быть влияема факторами, такими как культура, индивидуальные различия и контекст. В результате разработка надежных и точных систем SER требует использования разнообразных и представительных наборов данных, а также надежных методов машинного обучения.
Существует несколько подходов и методов, которые используются для решения существующих проблем в SER. Один из распространенных подходов - это извлечение признаков из аудиосигнала и применение алгоритмов машинного обучения (например, случайный лес, SVM и т.д.) для классификации эмоций. Эти признаки могут включать в себя прозодические признаки, такие как тон (pitch), энергия кадра (frame energy) а также спектральные признаки, такие как спектральный центроид (spectral centroid), спектральный rolloff и спектральная плоскостность (spectral flatness).
Другой подход - это использование методов машинного обучения, которые способны учиться на сырых аудиоданных или аудиоволновой форме, таких как глубокое обучение. Эти модели, такие как сверточные нейронные сети (CNN) и рекуррентные нейронные сети (RNN), способны учиться сложным шаблонам в данных и могут достичь хорошей производительности на задачах SER. Однако они требуют большого количества отмеченных данных и вычислительных ресурсов для обучения.
Другие методы, которые используются в SER, включают в себя гибридные подходы, которые сочетают несколько техник, а также техники, которые включают в себя контекстную информацию, такую как характеристики говорящего или содержание речевых слов.
В целом SER является сложной и трудной задачей, но за последние годы были сделаны значительные успехи благодаря прогрессу в области машинного обучения и наличию больших наборов данных. Будущие исследования в области SER, вероятно, будут сосредоточены на разработке более надежных и точных систем SER, а также на изучении новых приложений и сценариев использования технологии SER.

# 2. ОПРЕДЕЛЕНИЕ ЦЕЛИ И ЗАДАЧ РАБОТЫ
  Целью этого проекта является сравнение эффективности трех различных методов решения проблем в распознавании эмоций речи (SER): случайный лес (RFC), сверточная нейронная сеть (CNN) и рекуррентная нейронная сеть (RNN). Основная цель проекта - оценить относительные сильные и слабые стороны этих методов для SER и определить, какой метод лучше всего работает на данном наборе данных. Для достижения этой цели проект будет включать в себя реализацию и обучение каждого из трех методов на представительном наборе данных для SER, таком как набор данных RAVDESS, и оценку их производительности с помощью различных метрик, таких как точность, F1-оценка и матрица смежности. Результаты сравнения предоставят взгляд на эффективность различных подходов к SER и могут служить основой для будущих исследований в этой области.
Работа по этому проекту была разделена следующим образом:
•	Чинь Дык Тханг отвечал за реализацию и обучение модели случайного леса (RFC). Это будет включать в себя извлечение релевантных признаков из аудиоданных, выбор гиперпараметров и оценку производительности модели с помощью различных метрик.
•	Нгуен Тхи Ми Ту отвечал за реализацию и обучение рекуррентной нейронной сети (RNN). Это будет включать в себя проектирование и реализацию соответствующей архитектуры RNN, оптимизацию модели с помощью соответствующих техник и оценку производительности модели.
•	Ле Нгок Тхиен был ответственен за реализацию и обучение сверточной нейронной сети (CNN). Это будет включать в себя проектирование и реализацию соответствующей архитектуры CNN, оптимизацию модели с помощью соответствующих техник и оценку производительности модели.

# 3. ВЫБОР МЕТОДОВ И ТЕХНОЛОГИЙ ДЛЯ РЕАЛИЗАЦИИ ПРОЕКТА
## 3.1 Набор данных
  Мы выбрали набор данных RAVDESS для обучения и оценки моделей. Райерсонская аудиовизуальная база данных эмоционального речевого и певческого материала (RAVDESS) широко используется в исследованиях по распознаванию эмоций речи. Она состоит из коллекции аудио- и видеозаписей актеров, говорящих и поющих в различных эмоциональных состояниях, включая нейтральное, счастливое, грустное, злое, страшное и отвращение.
Набор данных RAVDESS был создан, чтобы предоставить разнообразный и представительный набор данных для изучения эмоциональной речи и пения. Он включает в себя 1440 записей, с каждой записью длительностью приблизительно 10 секунд. Записи равномерно сбалансированы по различным эмоциям и полу актеров, с каждой эмоцией, представленной 24 актерами каждого пола. 
Набор данных RAVDESS широко используется в исследованиях по распознаванию эмоций речи и был найден полезным эталоном для оценки производительности различных алгоритмов машинного обучения на этой задаче. Он также использовался в различных других исследовательских проектах, в том числе связанных с синтезом речи и распознаванием речи.

## 3.2 Случайный лес 
  Мы изучили использование классификатора случайных лесов для распознавания эмоций (SER) на наборе данных RAVDESS.
Одним из основных вызовов при использовании этого метода было идентификация и извлечение соответствующих функций из речи. Чтобы решить эту проблему, мы использовали пакет librosa для извлечения соответствующих функций из аудиозаписей, включая: MFCCs, spectral rolloff, zero-crossing rate, spectral centroid.
Модель случайного леса была реализована на Python с использованием библиотеки Scikit-Learn. Поскольку мы выполняли задачу классификации, мы использовали класс классификатора случайного леса, который написан как RandomForestClassifier в библиотеке ensemble Scikit-Learn.

## 3.3 RNN
  В качестве второго классификатора была реализована рекуррентная сеть LSTM. Это разновидность рекуррентных нейронных сетей (RNN), способная обучаться долгосрочным зависимостям, особенно в задачах предсказания последовательностей. Это позволяет им изучать образцы и отношения, которые могут охватывать несколько шагов времени, что полезно для задач, таких как распознавание эмоций, где контекст и продолжительность аудио могут быть важными факторами при определении эмоции, которую выражает спикер.

## 3.4 CNN
  В качестве окончательного классификатора в этом проекте была использована сверточная нейронная сеть (CNN). Сверточные нейронные сети (CNN) являются типом глубокого обучения, который часто используется для классификации изображений и других задач, связанных с данными, имеющими сетчатую структуру, такими как спектрограммы аудио. CNN успешно решают многие задачи распознавания эмоций, в том числе те, которые используют набор данных RAVDESS.
Чтобы использовать CNN для распознавания эмоций на наборе данных RAVDESS, мы сначала использовали пакет librosa для предварительной обработки аудиоданных. Конкретно, мы использовали librosa, чтобы извлечь волновые формы, спектрограммы и другие спектральные признаки из аудио, которые затем могут быть использованы в качестве входа для CNN. 

## 3.5 Метрики оценки
  Эффективность вышеуказанных методов была оценена с помощью различных метрик, включая точность (accuracy), F1-оценку (F1-score) и матрицу смешения (cònusion matrix). Эти метрики позволили нам оценить общую эффективность методов и сравнить их производительность друг с другом и с базовыми моделями.
Точность (Accuracy) - эта метрика измеряет общую способность модели правильно определять эмоцию, выраженную в речи. Это самая распространенная метрика для оценки SER, потому что она помогает оценить производительность модели, сравнивая предсказания с истинными метками.
F1-оценку (F1-score)  - эта метрика учитывает точность и полноту и помогает оценить точность и эффективность модели. Она также может использоваться для определения того, какая модель превзошла другую, рассчитывая их веса модели
Матрица ошибок (Confusion Matrix) - это помогает более точно понять работу модели. Она разбивает точность модели на фактические и предсказанные метки, что позволяет нам визуально понять работу модели. Это может помочь выявить слабые стороны модели, которые можно улучшить.

# 4. ПРОЕКТИРОВАНИЕ, РАЗРАБОТКА И ИССЛЕДОВАНИЕ
## 4.1 Подготовка данных
  Набор данных RAVDESS состоит из 1440 аудиофайлов в формате .wav. Аудиофайлы являются 16-разрядными, моно, 44,1 кГц .wav-файлами и содержат записи актеров, говорящих в различных эмоциональных состояниях. Набор данных равномерно сбалансирован между различными эмоциями нейтрального, счастливого, грустного, сердитого, боязливого и отвращения и полом актеров, с каждой эмоцией, представленной 24 актерами каждого пола. Аудиофайлы разбиты на 24 папки, "Actor_01", "Actor_02" и т. д. Каждая из них содержит 60 аудиофайлов. А вот так выглядят идентификаторы имен файлов, представленные на официальном сайте RAVDESS:
![image](https://user-images.githubusercontent.com/30606342/226106861-97f32d91-19c0-4a10-86a3-1deec24aec2c.png)
Поскольку все данные были упакованы, и формат имени файла аудио, необходимо выполнить несколько дополнительных шагов разбора.
Все состояния эмоций имеют 192 файла, за исключением нейтральных, которых всего 96. Это несбалансированность классов учитывалась при реализации алгоритмов RFC, RNN и CNN.

![image](https://user-images.githubusercontent.com/30606342/226106871-8c9014c8-4777-41e5-a0e2-996063a5376d.png)

  В этом проекте мы не вдавались в подробное изучение процесса выбора признаков, чтобы определить, какие признаки будут наиболее эффективными для нашего набора данных. 
  
  Вместо этого мы просто извлекли пять признаков для нашего анализа:
•	Zero Crossing Rate 
•	Chroma_stft 
•	MFCC 
•	MelSpectogram 
•	Spectral constrat

  Для оценки производительности наших моделей мы разделили данные на две части: набор данных для обучения и тестовый набор данных. Тестовый набор данных составляет 20% от общего количества данных и используется для оценки способности моделей обобщать на невидимые данные.
Для улучшения производительности глубокоучительных алгоритмов, таких как CNN и RNN, на нашем небольшом наборе данных для обучения, мы использовали технику называемую аугментация данных. Аугментация данных включает в себя создание новых синтетических наборов данных с помощью небольших изменений в исходном наборе данных. В качестве переменных для аудио данных эти изменения могут включать в себя добавление шума, сдвиг во времени, изменение высоты и скорости, и т. д. Цель аугментации данных - сделать модель более устойчивой и способной обобщать новые данные, учитывая неизменность к этому типу изменений. Путем аугментации наших тренировочных данных мы смогли улучшить производительность наших глубоконейронных моделей на задаче классификации.

![image](https://user-images.githubusercontent.com/30606342/226106895-61837408-eb5e-413f-a19f-64b6571b929a.png)

  В этом исследовании мы сравнили производительность трех методов распознавания эмоций речи на наборе данных RAVDESS: классификатор леса случайных деревьев (RFC), сверточная нейронная сеть (CNN) и рекуррентная нейронная сеть (RNN) с ячейками длинно-краткосрочной памяти (LSTM).
В этом исследовании мы сравнили эффективность трех методов для распознавания эмоций речи на наборе данных RAVDESS: случайный лес (RFC), сверточная нейронная сеть (CNN) и рекуррентная нейронная сеть (RNN) с ячейками длительно-краткосрочной памяти (LSTM). Результаты сравнения показали, что CNN имеет самую высокую точность со значением 0,66, за ней на небольшом расстоянии следует RNN с точностью 0,65. Разница в точности между CNN и RNN незначительна, что указывает на то, что оба метода хорошо справляются с этой задачей. Случайный лес имеет самую низкую точность со значением 0,61.

![image](https://user-images.githubusercontent.com/30606342/226106925-a2ea9a5e-6ce4-42f1-800b-78fa6e1ec04d.png)

  По показателю F1-score макросреднего значения у CNN был наивысший результат - 0,65, за ним следовал RNN с результатом 0,62 и классификатор случайного леса с результатом 0,58. Это указывает на то, что CNN удалось достичь хорошего сбалансированного соотношения между точностью и полнотой, и поэтому сумел сделать более точные прогнозы в целом. Удивительно то, что даже несмотря на то, что «neural» данные об эмоциях несбалансированы, CNN все еще обучена предсказывать эмоции так хорошо, что мы можем увидеть это, взглянув на матрицу ошибок.

  Эти результаты указывают на то, что алгоритмы глубокого обучения могут превосходить традиционные методы машинного обучения при распознавании эмоций в речи, хотя разница незначительна. Однако стоит отметить, что относительная эффективность различных алгоритмов может зависеть от различных факторов, таких как специфические характеристики набора данных и сложность задачи. Общий вывод такой: алгоритмы глубокого обучения не всегда существенно превосходят алгоритмы машинного обучения, но если размер выборки достаточен, то методы глубокого обучения могут иметь преимущество.







