## Введение

#### Общая информация о продукте

PH/Desktop представляет собой систему, предназначенную для автоматизации работы почтовой связи. В некотором смысле её можно считать дополнением к тому программному обеспечению, которое на постоянной основе используется в почтовых отделениях. Идея проекта состоит в том, чтобы постепенно добавлять в него те функции и возможности, которых почтовым работникам может недоставать в официальном ПО.

Важно отметить, что настоящее ПО не связано с ФГУП "Почта России" и разрабатывается исключительно на добровольных началах и в свободное от основной работы время. Автор(ы) не несёт(ут) ответственности за любой ущерб, причиненный при использовании данного продукта, а также за его работу и своевременное исправление ошибок.

#### Запуск и использование оболочки

Программа устроена по принципу "одно окно - одна функция" (или в терминах программы - модуль). В ней нет главного окна и примыкающих к нему модальных окон. Каждый модуль работает в отдельном окне и все эти окна независимы.

При запуске программы появляется окно входа. Предусмотрено два режима работы: пользователь и администратор. Для входа в режим пользователя просто нажмите на соответствующую кнопку. Для администрирования системы необходимо ввести пароль.

После входа появляется функциональное окно. Для начала работы выберите требуемый модуль из меню `Функции`. Модуль загружается в *текущее* окно, при этом загруженный ранее модуль сбрасывается с потерей всех несохранённых данных. Поэтому, если вы хотите переключиться на другой модуль, не прерывая работу с текущим, создайте новое окно (`Окно` - `Новое окно`) и загрузите модуль в него.

## Модули

### Обработка мелких пакетов

Модуль предназначен для печати извещений на простые мелкие пакеты. Для ускорения работы и предотвращения ошибок предусмотрена автоматическая подстановка адреса из накопляемой базы данных, автодополнение имени, автоматическая нумерация отправлений и проверка адреса на принадлежность к участку текущего ОПС.

Работа с пакетами осуществляется путем создания списков и последующей печати извещений на отправления, добавленные в список. Списки имеют фиксированную ёмкость, поэтому предполагается разбиение входящей корреспонденции на несколько списков.

Для того, чтобы создать новый список, выберите его вид (с номером или без него) и нажмите кнопку `Создать`. Откроется экран редактирования списков, состоящий их двух частей: формы ввода данных и таблицы, содержащей информацию об отправлениях.

Форма ввода состоит из полей: имя, улица, дом, квартира. Оболочкой предусмотрена подсветка текущего поля. Для переключения между полями можно использовать мышь и клавиши <kbd>Enter</kbd> и <kbd>Tab</kbd>.

В поле `Имя` вводится ФИО адресата. При введении имени с некоторой задержкой появляются варианты автодополнения. Модуль ищет имена не только по первым буквам имени, но и по любой его части, что позволяет находить адресатов при неполном написаниии имени на адресном ярлыке.

Для навигации по выборке используйте клавиши <kbd>↑</kbd> и <kbd>↓</kbd>. Выбрав подходящее имя, нажмите <kbd>Enter</kbd>. Произойдет автоматическая подстановка адреса из базы данных. Если появившиеся данные не соответствуют адресу на ярлыке, их можно исправить вручную. Если соответствуют, нажмите кнопку `Добавить` или ещё раз нажмите <kbd>Enter</kbd>. Появится всплывающее окно для повторной проверки введённых данных. Подтвердите ввод или нажмите `Отмена` для исправления.

В случае отсутствия имени в базе данных введите его целиком для упрощения последующей навигации. Программой также предусмотрена автоподстановка названий улиц, работающая по тому же принципу, что и имя.

В случае несоответствия адреса участку отделения программа выдаст соответствующее сообщение. Такой адрес добавить в список нельзя.

Для редактирования или удаления информации из списка нажмите на имя адресата в таблице. Откроется окно редактирования, в котором можно провести данные действия. На базе данных эти изменения не отражаются. Для редактирования БД необходимо использовать средства администрирования.

По окончании ввода данных настоятельно рекомендуется сохранить список в файл при помощи кнопки `Сохранить`. По умолчанию имя файла имеет вид `packetsDD_MM.json`, где `DD` и `MM` - день и месяц сохранения соответственно.

Для печати извещений нажмите соответствующую кнопку. Появится окно, где можно просмотреть макет документа, изменить настройки принтера и печати. Если всё настроено, нажмите кнопку `Печать`. Окно не закрывается автоматически. Настоятельно рекомендуется не закрывать его до тех пор, пока печать не завершится. Продолжить работу с программой можно в другом окне.