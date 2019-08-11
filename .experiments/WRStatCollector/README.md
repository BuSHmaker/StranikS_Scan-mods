﻿# WRStatCollector

## Описание
Скрипт для получения статистики из реплеев с сайта **[http://wotreplays.ru](http://wotreplays.ru)** путем парсинга **html**-страниц.

## Использование
Скачиваем программу **[PjOrion](https://koreanrandom.com/forum/topic/15280-)**, затем скачиваем **py**-скрипт выше. Открываем его в программе и жмем *F5* для исполнения кода, после чего ждём завершения работы программы. Должна появится соответствующая надпись, а также папка **Log** в каталоге, откуда был запущен **py**-скрипт.

Пример сообщения:
```
<<< 201 replays: 12324924...12325124      <-- обработан 201 реплей начиная с http://wotreplays.ru/site/12324924
<<< 12324924 not found!                   <-- реплей был удалён с сайта (страница 404)
<<< 12324927 not found!
<<< 12324929 not standard or interrupted! <-- страница реплея не стандартная или реплей записан не до конца
<<< ...
<<< Completed!
```

Пример лога:
**[Log\Log_ver_1.1_110819_092132472.csv](./Log/Log_ver_1.1_110819_092132472.csv)**

## Настройка
Перед выполнением скрипта можно в начале **py**-файла изменить параметры:

Параметр          | Описание
------------------|------------
REPLAYS_IDS_RANGE | Диапазон анализируемых номеров реплеев (номера следует брать из **URL**-адресов страниц)
URL_TIMEOUT       | Максимальное время ожидания ответа сервера, с
THREADS_COUNT     | Количество параллельных запросов на сервер (если вкл. загрузка статы с **WG**-сервера, то больше 10 ставить нет смысла из-за ограничений сервера)
CACHE_SIZE        | Буфер лога (число записей, накапливаемых в памяти перед сохранением в файл)
LOG_FILENAME      | Путь и имя файла лога (путь относительно каталога, где лежит **py**-скрипт)
WG_API_STATS      | Загружать стату игрока с **WG**-сервера 

## История версий
Со списком версий и изменениями можно ознакомиться [тут](./HISTORY.md).
