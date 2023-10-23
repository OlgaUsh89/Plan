# План автоматизации тестирования сценария перехода к записи и заполнению формы на обучение профессии «Тестировщик ПО»

1. Перечень автоматизируемых сценариев.

   1.1 Сценарии навигации к форме записи (предусловия).
   
   1.2 Сценарии заполнения и отправки формы
2. Перечень используемых инструментов с обоснованием выбора.
3. Перечень необходимых разрешений, данных и доступов.
4. Перечень и описание возможных рисков при автоматизации.
5. Перечень необходимых специалистов для автоматизации.
6. Интервальная оценка с учётом рисков в часах.

### 1. Перечень автоматизируемых сценариев.
#### 1.1 Сценарии навигации к форме записи (предусловия)
|ID | Название                         | Шаги    |Ожидаемый результат  |
|---|----------------------------------|---------|---------------------| 
| 1 | Переход к форме записи через раздел "Каталог курсов"  |  1. Открыть в браузере ссылку [веб-сайт Нетологии.](https://netology.ru/#/)   2. Найти на странице раздел "Каталог курсов", кликнуть на него. 3. В поисковую строку ввести "Тестировщик ПО", кликнуть в выпадающем списке на зназвание.  4. Найти на странице кнопку "Записаться" и кликнуть на нее.| Осуществлен переход на страницу c формой записи на курс|                                                                             |
| 2 | Переход к форме записи через блок "Направления обучения"| 1. Открыть в браузере ссылку [веб-сайт Нетологии.](https://netology.ru/#/)  2. Найти на странице блок "Направления обучения".  3. Кликнуть на раздел "Программирование".  4. В  выпадающем списке найти курс "Тестировщик ПО", кликнуть на него.  5. Кликнуть на странице на кнопку "Записаться".   |Осуществлен переход на страницу c формой записи на курс|                    |

#### 1.2 Сценарии заполнения и отправки формы
|ID | Название                         | Описание   | Шаги  |Ожидаемый результат    |
|---|----------------------------------|---------|---------------------|---------|
| 1 |***Позитивные сценарии:***  Ввод в форму валидных значений полей "Имя" и "Телефон" для записи на курс "Тестировщик ПО"|Валидными данными для полей ввода являются: поле "Имя" - символы кириллицы, дефис, пробел, верхний и нижний регистры. Например, Валентина. Поле "Телефон" - наличие префикса, 11 цифр. Например, +79200114499|1. Ввести в поле "Имя" валидное значение. 2. Ввести в поле "Телефон" валидное значение. 3. Кликнуть на поле "Записаться".| Появление сообщения "Ваша заявка принята. Скоро с вами свяжется наш специалист".|
| 2 |Ввод в форму валидных значений полей "Имя" и "Телефон" для получения консультации по курсу "Тестировщик ПО"|Валидными данными для полей ввода являются: поле "Имя" - символы кириллицы, дефис, пробел, верхний и нижний регистры. Например, Валентина. Поле "Телефон" - наличие префикса, 11 цифр. Например, +79200114499|1. Ввести в поле "Имя" валидное значение. 2. Ввести в поле "Телефон" валидное значение. 3. Кликнуть на поле "Получить консультацию".| Появление сообщения "Ваша заявка принята. Скоро с вами свяжется наш специалист".|
| 1 |***Негативные сценарии:*** Ввод в поле "Имя" латинских букв|Невалидное значение поля "Имя", написанное латинскими буквами. Например, Valentina|1. Ввести в поле "Имя" значение латинскими буквами. 2. Ввести в поле "Телефон" валидное значение. 3. Кликнуть на кнопку "Записаться".|Поле "Имя" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода имени."|
| 2 |Пустое поле "Имя"|Оставить поле "Имя" незаполненным |1. Оставить поле "Имя" пустым. 2. Заполнить поле "Телефон" валидным значением. 3. Кликнуть на кнопку "Записаться"|Поле "Имя" выделяется красной рамкой, под полем появляется сообщение "Поле незаполнено".|
| 3 |Ввод в поле "Имя" цифр|Невалидное значение поля "Имя", написанное цифрами. Например, 1234|1. Ввести в поле "Имя" цифры. 2. Заполнить поле "Телефон" валидным значением. 3. Кликнуть на кнопку "Записаться" |Поле "Имя" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода имени."|
| 4 |Ввод в поле "Имя" спецсимволов|Невалидное значение поля "Имя" с указанием спецсимволов. Например, Валентина$| 1. Ввести в поле "Имя" значение со спецсимволами. 2. Заполнить поле "Телефон" валидным значением. 3. Кликнуть на кнопку "Записаться" |Поле "Имя" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода имени."|
| 5 |Ввод в поле "Телефон" букв кириллицы|Невалидное значение поля "Телефон" с использованием букв кириллицы. Например, фывапро|1. Заполнить поле "Имя" валидным значением. 2. Ввести в поле "Телефон" буквы кириллицы. 3. Кликнуть на кнопку "Записаться" |Поле "Телефон" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода номера телефона."|
| 6 |Пустое поле "Телефон"|Оставить поле "Телефон" незаполненным |1. Заполнить поле "Телефон" валидным значением. 2. Оставить поле "Телефон" пустым. 3. Кликнуть на кнопку "Записаться"|Поле "Телефон" выделяется красной рамкой, под полем появляется сообщение "Поле незаполнено".|
| 7 |Ввод в поле "Телефон" значения из 10 цифр|Невалидное значение поля "Телефон" из 10 цифр. Например, +7900112234|1. Заполнить поле "Имя" валидным значением. 2. Ввести в поле "Телефон" 10 цифр. 3. Кликнуть на кнопку "Записаться" |Поле "Телефон" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода номера телефона."|
| 8 |Ввод в поле "Телефон" 11-ти нулей|Невалидное значение поля "Телефон" из 11-ти нулей. Например, +00000000000|1. Заполнить поле "Имя" валидным значением. 2. Ввести в поле "Телефон" 11 нулей. 3. Кликнуть на кнопку "Записаться" |Поле "Телефон" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода номера телефона."|
| 9 |Ввод в поле "Телефон" значения без префикса +7|Невалидное значение поля "Телефон" без префикса +7. Например, 9305558157|1. Заполнить поле "Имя" валидным значением. 2. Ввести в поле "Телефон" значение без префикса. 3. Кликнуть на кнопку "Записаться" |Поле "Телефон" выделяется красной рамкой, под полем появляется сообщение "Неверный формат ввода номера телефона."|

### 2. Перечень используемых инструментов с обоснованием выбора.
1.  IntelliJ IDEA - программное приложение, которое помогает эффективно разрабатывать программный код.
2.  Java - язык программирования, достаточно распространенный и относительно несложный.
3.  Gradle - система автоматической сборки с легкой настройкой зависимостей и преимуществом производительности.
4.  Библиотека JUnit - позволяет проверить код программы без значительных усилий и не занимает много времени.
5.  Selenide - автоматизированная система тестирования c лаконичным синтаксисом, автоматическим созданием скриншотов.
6.  Docker Compose — средство для определения и запуска приложений с несколькими контейнерами, позволяющее, запустить СУБД.
7.  Git - программа, позволяющая отслеживать любые изменения в файлах, хранить их версии и оперативно возвращаться в любое сохранённое состояние.
8.  Faker - пакет для генерации тестовых данных.
9.  Allure - самый популярный фреймворк для создания отчетов автотестирования.
   
