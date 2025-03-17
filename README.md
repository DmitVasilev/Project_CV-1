# <font size = 5 color = #00FF00> <center>PROJECT CV-1. Угадай знаменитость</center></font> 



##  <font color = #9ACD32> Содержание </font>

[1. Введение]()   
[2. Описание задачи]()   
[3. Описание данных]()   
[4. Результат]()                  
[5. Выводы]()                                        
[6. Контакты]()

### <font color = #9ACD32> 1. Введение </font>

В данном проекте решается задача построения пятиклассового класификатора для распознавания лиц спикеров гипотетической IT-конференции по изображениям с использованием предобученных сетей.

:arrow_up:[к содержанию]() 


###  <font color = #9ACD32>2. Описание задачи</font>

**Бизнес-задача:** необходимо реализовать модель нейронной сети способную по изображению лица определить одного из спикеров гипотетической IT-конференции (Билл Гейтс, Илон Маск, Джефф Безосс, Марк Цукерберг, Стив Джобс) с использованием предобученных моделей.

**Техническая задача:**  
   + Скачать и загрузить датасет.
   + Отрисовать один батч загруженных данных.
   + Выбрать предобученную модель.
   * Обучить многоклассовый классификатор, используя выбранную модель.
   + Визуализировать предсказания модели.
   + Описать полученные результаты в текстовой ячейке ноутбука.

**Основные цели проекта:**
1. Решить задачу многоклассовой классификации с использованием принципа переноса обучения (accuracy > 0.85 на валидационной выборке).
2. Отработать навыки визуализация данных и полученных предсказаний модели.

:arrow_up:[к содержанию]()  

###  <font color = #9ACD32>3. Описание данных</font>

В проекте используется учебный [датасет](https://drive.google.com/file/d/120xqh0mYtYZ1Qh7vr-XFzjPbSKivLJjA/view?usp=sharing). В нем содержится 3 тысяч цветных изображений лиц в тренировочной и 914 в валидационной выборках.
              
:arrow_up:[к содержанию]()                 

###  <font color = #9ACD32>4. Результат</font>

 + Ноутбук с решением поставленной задачи: [Project_CV_1.ipynb]();            
 + Работа выполнена с использованием **Python версии 3.12.3**. Необходимые для воспроизводимости кода зависисмости приведены в файле requirements.txt: [requirements.txt](). 
                        
:arrow_up:[к содержанию]()             


###  <font color = #9ACD32>5. Выводы</font>

Проведена загрузка и аугментация данных с использованием DataLoader. Выполнена визуализация батчей изображений для обучающей и валидационной выборки. В качестве предобученной модели использована модель ResNet34. Реализованы варианты модели классификатора основанной на:
   + полностью переобученной модели ResNet34, использующей веса предобученной модели в качестве начальных значений;
   + файн-тюнинге предобученной модели ResNet34;
   + сочетании файн-тюнинга предобученной модели и переобучения последних слоев сверточного блока сети.               
Визуализрованы процесс обучения моделей и результаты их предсказаний на валидационной выборке.            
Требуемое значение точности > 0.85 на валидационной выборке достигнуто для первого и последнего варианта модели. Лучшая точность на валидационной выборке достигается на полностью переобученной модели использующей предобученные веса в качестве начальных значений. Точность данной модели составляет 0.99. Сочетание файн-тюнинга предобученной модели и переобучения последних слоев сверточного блока сети на представленных данных снижает точность на валидационной выборке до 0.97, но сокращает время обучения модели примено на 20%.

:arrow_up:[к содержанию]() 


###  <font color = #9ACD32>6. Контакты</font>
Для обратной связи можно воспользоваться почтой: vasilevdma@mail.ru

:arrow_up:[к содержанию]() 