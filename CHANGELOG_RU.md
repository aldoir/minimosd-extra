v813:
* Рамка HUD может выключаться
* РАДАР обзавелся "следом" в 3 точки, требует свежего шрифта
* значения RSSI 2 байта - убрано ограничение в 255

v816:

* Трансляция MAVlink в телеметрию Walkera на выход (для DEVO RX705/RX707 receivers) работает!
* поддержка CleanFlight/MWII протокола (не тестировано)
* поддержка диалекта MAVlink от AutoQuad   (не тестировано)
* поддержка новых режимов APM_Plane (quad-plane)
* новые параметры на экране Настройки (Setup)
* дальнейшая оптимизация места чтобы это все впихнуть :)

v817:

* отфильтрованы сообщения с наземной станции, транслируемые версиями Plane 3.4+ и Copter 3.3+
* автоматическое определение скорости последовательного порта!

v818

* исправлен баг с отображением батареи
* исправлен баг с масштабом времени
* восстановлена загрузка шрифтов (поломаная автоопределением скорости порта)

* подпроект Character_Updater теперь использует те же вспомогательные файлы и может использоваться,  также он отображает загруженный шрифт
* Скорость SPI уменьшена для предотвращения глюков при загрузке шрифтов

v820

* bugfixes
* Charecter Updater HEX

v821
* починено отображение режима NTSC в конфигураторе
* лучшая синхронизация протоколов UAVtalk & mwii - не проглатывается стартовый символ
* прерывание PWM_IN разрешено только если используется

v822 
* исправлено отображение самолетных режимов

v823
* добавлен флаг "Альтернативный режим" ко всем панелям
* Панели WindSpeed, Airspeed и Groundspeed в Альтернативном режиме отображают скорость в м/с вместо км/ч
* новый чарсет для отображения m/s


v824
* новая схема расчета высоты

v825

* Отображение сообщений MAVlink!

v826

* MAVlink message двигается на экране если не влезает целиком


v827

* новый парсер tLog, который знает его формат и не позволяет OSD терять синхронизацию
* thread-safe статус в конфигураторе
* оптимизировано время цикла
* оптимизирован расход памяти
* удалены "show battery percentage" галка и флаг - теперь этот режим задается независимо для каждого экрана в свойствах панели
* сенсоры для отображения произвольных значений в произвольном формате
* новые предупреждения о сработке GeoFence

v828

* сенсоры могут работать в режиме PWM
* некоторая оптимизация ресурсов

v829

* Высота может сбрасываться в 0 при арминге
* новая логика отображения панели результатов полета

v830

* исправлен баг с отображением рамки горизонта (HUD frame)
* исправлена зависимость от загрузчика библиотеки SingleSerial

v831

* переключение экранов в режиме "по кругу" может делаться только один раз

v832

* исправлен баг с вертикальной скоростью в m/s

v834

* исправлен баг с результатами полета
* исправлено расположение панели heading
* панель heading может иметь иконку
* скролл сообщения mavlink может быть отключен
* исправлено расположение панели time
* двоеточие времени сделано мигающим

v835
* мигание двоеточия времени может быть отключено
* действительно исправлено расположение панели time

v836
* поддержка протокола телеметрии LTM (untested)

v837
* чистка кода, пересборка с другими ключами компиляции
* исправлен баг с панелью Message


v838

* отфильтровываются сообщения MAVlink от подвеса
* Конфигуратор может подать поток телеметрии на OSD с любого COM-порта
* исправлен странный баг с самопроизвольным движением  курсора на экране настройки


v839
* исправлена вертикальная скорость, сломаная в v838

v840
* Обойден баг компилятора, приводивший к "No data"
* исправлен вид panTune 
* некоторые красивости в panEff
* полностью исправлен баг panSetup
* естественный ход времени в плеере TLOG
* исправлен баг конфигуратора с несохранением флага альтернативной функции


v841
* Предупреждение "No GPS fix!" отображается только при наличии GPS


v842
* один хороший человек из команды GCC подсказал два "секретных" (не упомянутых в GCC --help) флага оптимизации, что освободило  ~1Kbyte памяти!
* благодаря этому добавлены 2-й, 3-й и 4-й флаги для каждой панели
* благодаря этому все настройки авиагоризонта перемещены в флаги панели Horizon, и могут быть настроены поэкранно
* изменена логика показа результатов полета для самолета
* все расстояния могут быть больше чем 99км
* Панель gps координат может отображать только дробную часть координат
* исправлено залипание экрана на больших скоростях данных
* Удалена панель GPS2, вместо нее у панели GPS сделан флаг "Показывать в строке" ("Display in row")


v843
* RSSI от 3DR модема может использоваться как источинк RSSI
* дополнительные значения в результатах полета - ток и скорости подъема/снижения
* поддержка аппаратов без GPS: панели высоты и скорости работают и без GPS
* Результаты полета отображаются на экране "no input data" - например для использования OSD на наземной станции


v844
* новая панель  HDOP
* новая панель "channel status" - 5 позиций


v845
* исправлен баг в панели ChannelStatus
* CT очищает сообщение через 10 секунд

v846

* Шкала ("иконка") панели компаса (panRose) может располагаться снизу
* Сама панель panRose может быть четного размера дабы центрироваться относительно авиагоризонта. Требует загрузки шрифта 2.4.1.4. 
 Пожертвованы символы @, ~, `

v847
* исправлено несоответствие с конфигуратором в режиме NTSC
* удален знак % из panRSSI в конфигураторе
* добавлена возможность исключить MAVlink при сборке
* все файлы телеметрийных протоколов перемещены в папку 'protocols'
* исправлен размер панели для всех расстояний
* исправлена иконка GPS для модулей с поддержкой RTK


v848
* исправлен баг с отсутствием галки у панели BatteryPercent

v849
* новая панель Шкала "channel scale" - графическое представление панели Статус Канала

v850
* новая панель "Channel value" которая отображает значение для выбранного канала

v851
* панель "Channel scale" обзавелась возможностью работать в расширенном диапазоне PWM (thanks to Tonyyng)


v582
* панель "Channel status" тоже может работать с расширенным диапазоном PWM
* обновление экрана перенесено в процедуру обработки прерывания и теперь полностью избавлено от "снега"
* первая попытка поддержки строк в EEPROM
* первая попытка поддержки конфигурации через MAVlink
* 852a - fixed bug with flickering panels

v853
* Строки работают! И панель Channel State использует первые 5 из них

v854
* попытка восстановления зависшей MAX7456

v855
* запись конфигурации через MAVlink теперь работает! Но только на старших версиях ArduPilot которые транслируют команды с наземной станции на выход

v856
* исправлен баг с видимостью свойств панели

v857
* исправлен баг с выбором панели в конфигураторе
* комплиментарный фильтр панели panEff изменен с 1/10 на 1/100
* попытка изменить поведение горизонта для больших кренов (>70grad)
* мелкие изменения

v858
* исправлено несколько ошибок в конфигураторе
* поддержка локализации! Файл lang.txt в каталоге с EXE-файлом
* поддержка переключения экранов по времени (не тестировалось)
* файл default.osd загружается при запуске если есть
* исправлен баг с реверсным RSSI
* Исправлено поведение Горизонта при больших кренах
* Панель Результаты полета (Flight Data) выключается не по времени а по движению стика газа или переключению экрана ОСД
* Увеличена ширина панели Real Heading 
* Флеш-память проверяется после записи! Нет больше багов, вызванных некорректной записью во флеш
* ILS теперь позволяет заходить на полосу с противоположной стороны
* исправлен баг в ILS с неверным размером горизонта
* ILS: если посадочные маркеры не видны то отображается стрелка нужного направления поворота
* некоторые оптимизации размера чтобы все это впихнуть :)


v859
* работает UAVtalk!

v860
* MAVLink не теряет синхронизацию при ошибках CRC

v861
* исправление багов

v862
* исправлено зависание экрана настройки
* исправлено поведение без приемника на UAVtalk
* испралено направление стиков экрана настройки
* исправлена настройка сенсоров

v863
* проект перешел на отдельные бинарники на каждый протокол, так что теперь имена файлов выглядят как  MinimOsd_Extra_Uni.{версия}DV-{протокол}-{тип сборки}.hex
* реверсировано направление ветра
* исправлена panEff
* добавлен максимум скорости ветра в панель результатов полета (Flight Data)
* некоторая оптимизация

v864
* определяет зависшие потоки данных и пытается (если подключен TX) запрашивать их снова 

v865
* запрашивает нужные потоки данных на правильных скоростях для текущей скорости COM-порта
* определяет переполнение потока данных и пытается (если подключен TX) запрашивать их снова на меньшей скорости
* мелкие исправления

v866
* реверс направления ветра в конфигураторе
* исправлен баг с панелью Warnings
* оптимизация использования стека

v867
* реверс крена в горизонте - Russian HUD

v868
* исправлено множество багов в последних изменениях

v869
* поддержка режимов коптера Brake и Throw 

v870
* неизвестные режимы показываются номером а не мусором на экране

v871
* исправлено время полета

v872
* добавлено отображение определенной скорости порта

v873
* флаг 'Russian HUD' сделан независимым по экранам
* координаты в панели результатов полета "Flight Data" могут отображаться второй колонкой
* добавлена возможность отображать знак "%" для RSSI

v874
* починена работа флагов Russian HUD 

v875
* UAVtalk снова работает!
* исправлен баг с переполнением в panRose
* исправлено поведение горизонта на больших тангажах
* удалены последние остатки работы нескольких протоколов одновременно

v876
* UAVtalk использует высоту по барометру при отсутствии GPS
* исправлен подсчет времени полета
* исправлен режим RussianHUD на стартовом экране

v877
* новая панель Power, отображающая среднюю потребляемую мощность (сглаживание комплиментарным фильтром 1:10)
* в панель результатов полета добавлен максимум мощности
* унификация комплиментарных фильтров
* пройденное расстояние не растет при отсутствии данных

v878
* версия компилятора уменьшена до 4.8.1 что позволило избавиться от множества багов, вызваных компилятором
* исправлено поведение обнаружения переполнения потока MAVLink

v879
* исправлены напряжение и высота для UAVtalk
* добавлена температура (по барометру) для UAVtalk
* если MAX7456 теряет кадровую синхронизацию и перестает выдавать прерывания то OSD переключается в старый режим обновления по таймеру - снег на 
экране таки лучше чем полная остановка отображения.
* генерация PWM производится в кадровом прерывании

v880
* попытка получить емкость батареи через UAVTalk и вычислить % остатка
* слегка изменен порядок реинициализации MAX7456


v881
* панель efficiency может показывать только mah/km
* 'rhfy "flight data" с результатами полета может быть отключен
* некоторая чистка кода
* Режим "connect to COM-port" в конфигураторе теперь двухсторонний
* попытка оживить работу с протоколом MSP (MWII Cleanflight Betaflight INAV) - делаются запросы нужных данных

v882
* исправлено округление в UAVtalk

v883
* исправлено зависание OSD при больших углах тангажа
* в конфигураторе, в режиме "connect to COM port" можно задать скорость порта
* Протокол MWII работает!

v884
* исправлен режим NTSC в конфигураторе
* напряжение со второй батареи может быть получено через MAVlink

885
* панели тока и напряжений могут работать со сглаживанием комплиментарным фильтром 1:10, 1:100 или 1:1000 (на выбор)
