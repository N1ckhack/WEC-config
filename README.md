# Занятие 5

# Практическая работа №5.1 Обмен данными в домене.

1.1 Установим DFS на DC1

![Снимок экрана (176).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(176).png)

`DFS Namespases` - позволяет создавать пространство имен для фалов ресурсов

1.2 Зайдем в управление DFS и создадим новое пространство имен для сетевого пути:

![Снимок экрана (178).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(178).png)

1.3 Зададим имя целевого сервера и права доступа к сетевым ресурсам. У админов будет full-control

![Снимок экрана (179).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(179).png)

1.4 Выберем тип пространства имен. У нас будет `Domain-based namespace`

![Снимок экрана (180).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(180).png)

1.5 Готово

![Снимок экрана (181).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(181).png)

1.6 Проверяем доступность на RU-серваке

![Снимок экрана (182).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(182).png)

1.7 Создаем папку `share`. И `папки отделов внутри, + папку all_share`

![Снимок экрана (183).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(183).png)

1.8 Каждую эту папку нужно сделать сетевой. Идём в свойства папки (сделаем на примере buhg)

1.9 Вкладка sharing, пунк advanced sharing

1.10 Активируем галочку шаринга, а вконце имени сетевой папки ставим знак . После идём в permissions.

![Снимок экрана (184).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(184).png)

1.11 Выставляем права на чтение-запись для bugh-sec и удаляем группу everyone

![Снимок экрана (189).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(189).png)

1.12 Изменим права для security у папки HR. Добавим группу HR-sec и выдадим права на midify

![Снимок экрана (191).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(191).png)

![Снимок экрана (192).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(192).png)

1.13 **ВЫШЕОПИСАННЫЕ ОПЕРАЦИИ НУЖНО ПРОДЕЛАТЬ ДЛЯ ВСЕХ ПАПОК И ВСЕХ ОТДЕЛОВ**

1.14 Проверим доступ к сетевым ресурсам с PC1

![Снимок экрана (193).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(193).png)

Как видим все папки отображаются аналогично методичке.

# Практическая работа №5.2 Средства мониторинга Windows.

2.1 Добавим правило аудита для папки share

![Снимок экрана (195).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(195).png)

2.2 Отметим группу `Domain Users`

![Снимок экрана (196).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(196).png)

2.4 Выставим type= `all`, чтобы мониторить как успех, так и отказ. Нажмём кнопку show advanced permissions

![Снимок экрана (197).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(197).png)

Отметили оба пункта Delete

2.5 Правило создано для папки `share`, а так же всех её вложенных папок и файлов

Создайте в папке `all_share` папку `folder-for-delete` для тестирования генерации событий

![Снимок экрана (198).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(198).png)

Теперь удалим ее от имени `Olga`

![Снимок экрана (199).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(199).png)

2.6 Откроем журнал безопасности и отфильтруем события. Нас интересуют следующие:

4656 - проверка прав доступа к объекту

4659 - запрос файла удаления

4660 - аудит удаления объекта

4663 - над объектом была выполнена конкретная операция `(у нас удаление)`

2.7 После установки фильтра находим нужную группу событий: 

![Снимок экрана (201).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(201).png)

![Снимок экрана (203).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(203).png)

![Снимок экрана (204).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(204).png)

![Untitled](Untitled.png)

**upd [26.09] - добавил скрин события 4660, пропустил его при формировании первого отчета**

# Реализация отправки журналов

3.1 Включим сервис сборщика логов и подтвердим его автостарт `wecutil qc`

![Снимок экрана (205).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(205).png)

3.2 Настроим политику отправки журналов на logcollector. Зайдём в редактор групповой политики и создадим новую, `log_delivery`

![Снимок экрана (206).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(206).png)

3.9 Поиск не происходит среди ПК. Изменим это, добавив группу `компьютеры`

Теперь можем выполнить поиск по имени. Введем `PC1`

![Снимок экрана (212).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(212).png)

Удалим аутентифицированных пользаков и оставим только политику к пк `PC1`

![Снимок экрана (213).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(213).png)

Теперь нужно создать настройку Windows Remote Managment. Выбираем, двигаемся дальше.

![Снимок экрана (215).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(215).png)

На этом этапе нажмем на галочку возле `public` - она нам не понадобится

![Снимок экрана (216).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(216).png)

Видим успешно добавленный WinRM

![Снимок экрана (218).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(218).png)

Теперь нужно настроить путь до Log-Collector’a: `Server=http://dc1.pt.local:5985/wsman/SubscriptionManager/WEC,Refresh=60`

![Снимок экрана (210).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(210).png)

3.17 Для настройки политики нам требуется дескриптор безопасности журнала. Найдем его на `PC1` командой `wevtutil gl security`

![Снимок экрана (219).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(219).png)

3.18 Настроим доступ учеток до журнала `security` при помощи внесения параметра `O:BAG:SYD:(A;;0xf0005;;;SY)(A;;0x5;;;BA)(A;;0x1;;;S-1-5-32-573)`

![Снимок экрана (221).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(221).png)

3.20 И отдельно добавим учетную запись, которую в дальнейшем будем использовать для чтения журналов, в группу читателей журнала. Зайдём в политику локальных групп и добавим правило для локальной группы

![Снимок экрана (222).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(222).png)

Внесем `PT\Domain Admins`

![Снимок экрана (224).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(224).png)

3.24 Применяем на домен

![Снимок экрана (225).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(225).png)

3.25 Настроим прием логов на коллекторе. Пройдя в event viewer, зайдём в меню подписок и подтвердим автоматическое включение службы. Выбираем доменный компьютер, принимаем.

![Снимок экрана (226).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(226).png)

Ошибок нет!

![Снимок экрана (230).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(230).png)

![Untitled](Untitled%201.png)

3.33 Зайдём в меню Advanced, укажем для сбора УЗ администратора

![Снимок экрана (232).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(232).png)

3.35 Ошибок нет

![Untitled](Untitled%202.png)

3.36 Дадим доступ сетевой службе до чтения журнала безопасности, выполним команду на `PC1`

![Снимок экрана (234).png](%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_(234).png)

3.37 Спустя 20-25 минут начали появляться журналы

![Untitled](Untitled%203.png)

Вот так выглядит полноценный список внесенных нами изменений:

![Untitled](Untitled%204.png)

# Настройка сборщика логов при компьютерах-инициаторах

4.1 На сервере-коллекторе выполнить команду `winrm qc`, ответить согласием на оба последующих вопроса (включение службы WinRM и прослушивание порта TCP:5985 для входящих соединений от источников)

![Untitled](Untitled%205.png)

4.2 На сервере-коллекторе выполнить команду `wecutil qc`, согласиться на включение службы сборщика событий Windows.

![Untitled](Untitled%206.png)

4.3 На источниках событий следует включить службу WinRM **(реализовано политикой в пункте 3.4)** 

4.4 Создать подписку, где инициатором будут компьютеры

![Untitled](Untitled%202.png)
