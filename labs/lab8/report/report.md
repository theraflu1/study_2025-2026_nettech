---
## Front matter
title: "Отчёт о лабораторной работе"
subtitle: "Лабораторная работа 8"
author: "Мошаров Денис Максимович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить принципы маршрутизации в IPv4- и IPv6-сетях и принципы настройки сетевого оборудования.

# Выполнение лабораторной работы

Создаём новый проект в GNS3 с названием "lab8" (рис. [-@fig:001]).

![Новый проект](image/1.png){#fig:001}

Выстраиваем топологию сети, согласно данному заданию, размещаем коммутаторы, маршрутизаторы FRR и оконечные устройства (рис. [-@fig:002]).

![Топология](image/2.png){#fig:002}

Настраиваем IP-адрес и шлюз по умолчанию на PC1 10.0.10.10/24 10.0.10.1 (рис. [-@fig:003]).

![Настройка PC1](image/3.png){#fig:003}

Настраиваем IP-адрес и шлюз по умолчанию на PC2 ip 10.0.11.10/24 10.0.11.1 (рис. [-@fig:004]).

![Настройка PC2](image/4.png){#fig:004}

Настроим IPv4-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-01 (рис. [-@fig:005]).

![msk-dmmosharov-gw-01](image/5.png){#fig:005}

Настроим IPv4-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-02 (рис. [-@fig:006]).

![msk-dmmosharov-gw-02](image/6.png){#fig:006}

Настроим IPv4-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-03 (рис. [-@fig:007]).

![msk-dmmosharov-gw-03](image/7.png){#fig:007}

Настроим IPv4-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-04  (рис. [-@fig:008]).

![msk-dmmosharov-gw-04](image/8.png){#fig:008}

Присваиваем IPv6-адреса оконечным устройствам PC1 и PC2 в соответствии с данными в таблице  (рис. [-@fig:009]).

![IPv6-PC1](image/9.png){#fig:009}

Проделываем тоже самое для PC2 (рис. [-@fig:010]).

![IPv6-PC2](image/10.png){#fig:010}

Настраиваем IPv6-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-01 (рис. [-@fig:011]).

![msk-dmmosharov-gw-01](image/11.png){#fig:011}

Настраиваем IPv6-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-02 (рис. [-@fig:011.1]).

![Пmsk-dmmosharov-gw-02](image/11.1.png){#fig:011.1}

Настраиваем IPv6-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-03 (рис. [-@fig:012]).

![msk-dmmosharov-gw-03](image/12.png){#fig:012}

Настраиваем IPv6-адреса на интерфейсах маршрутизаторов:
msk-dmmosharov-gw-04 (рис. [-@fig:013]).

![msk-dmmosharov-gw-04](image/13.png){#fig:013}

Настроим RIP на маршрутизаторах в качестве протокола динамической маршрутизации на каждом из msk-dmmosharov-gw-0* (рис. [-@fig:014]).

![msk-dmmosharov-gw-01](image/14.png){#fig:014}

Также протокол RIP версии 2 на следующем маршрутизаторе (рис. [-@fig:015]).

![msk-dmmosharov-gw-02](image/15.png){#fig:015}

Также протокол RIP версии 2 на следующем маршрутизаторе (рис. [-@fig:016]).

![msk-dmmosharov-gw-03](image/16.png){#fig:016}

Также протокол RIP версии 2 на следующем маршрутизаторе (рис. [-@fig:017]).

![msk-dmmosharov-gw-04](image/17.png){#fig:017}

Выведя статус защиты SSH убеждаемся, что бан был снят (рис. [-@fig:018]).

![Отсутствие блокировки](image/18.png){#fig:018}

Убеждаемся, что маршрутизация по RIP настроена на каждом маршрутизаторе (рис. [-@fig:019]).

![Проверка RIP](image/19.png){#fig:019}

Проверяем gw-02 (рис. [-@fig:020]).

![Проверка RIP](image/20.png){#fig:020}

Проверка gw-03 (рис. [-@fig:021]).

![Проверка RIP](image/21.png){#fig:021}

Проверка gw-04 (рис. [-@fig:022]).

![Проверка RIP](image/22.png){#fig:022}

Проверим пути прохождения пакетов, с PC1 пингуем PC2 (рис. [-@fig:023]).

![Пингуем PC2 с PC1](image/23.png){#fig:023}

Проверяем метрики протокола RIP на gw-01 (рис. [-@fig:024]).

![Метрики](image/24.png){#fig:024}

Отключаем на маршрутизаторе gw-02 интерфейс (рис. [-@fig:025]).

![Отключение интерфейса](image/25.png){#fig:025}


Проверяем метрики протокола RIP на gw-01 (рис. [-@fig:026]).

![Метрики](image/26.png){#fig:026}


С PC1 пингуем PC2 и определяем (рис. [-@fig:027]).

![С PC1 пингуем PC2](image/27.png){#fig:027}

Включим на маршрутизаторе msk-user-dmmosharov-02 интерфейс (рис. [-@fig:028]).

![Включим на маршрутизаторе](image/28.png){#fig:028}

С PC1 пропингуем PC2 и определим путь следования пакетов (рис. [-@fig:029]).

![С PC1 пингуем PC2](image/29.png){#fig:029}

Посмотрим захваченный на соединениях трафик (рис. [-@fig:030]).

![Захваченный трафик](image/30.png){#fig:030}
![Захваченный трафик](image/31.png){#fig:031}

На маршрутизаторах настроим RIPng для сетей IPv6:
msk-dmmosharov-gw-01 (рис. [-@fig:032]).

![Настраиваем RIPng для msk-dmmosharov-gw-01](image/32.png){#fig:032}

На маршрутизаторах настроим RIPng для сетей IPv6:
msk-dmmosharov-gw-02 (рис. [-@fig:033]).

![Настраиваем RIPng для msk-dmmosharov-gw-02](image/33.png){#fig:033}

На маршрутизаторах настроим RIPng для сетей IPv6:
msk-dmmosharov-gw-03 (рис. [-@fig:034]).

![Настраиваем RIPng для msk-dmmosharov-gw-03](image/34.png){#fig:034}

На маршрутизаторах настроим RIPng для сетей IPv6:
msk-dmmosharov-gw-04 (рис. [-@fig:035]).

![Настраиваем RIPng для msk-dmmosharov-gw-04](image/35.png){#fig:035}

Проверим пути прохождения пакетов. С PC1 пропингуем PC2 и определим путь следования пакетов (рис. [-@fig:036]).

![С PC1 пропингуем PC2](image/36.png){#fig:036}

Проверим метрики протокола RIPng (рис. [-@fig:037]).

![Проверяем метрики](image/37.png){#fig:037}

Отключим на маршрутизаторе msk-dmmosharov-gw-02 интерфейс (рис. [-@fig:038]).

![Отключаем интерфейс](image/38.png){#fig:038}

Проверим метрики протокола RIPng (рис. [-@fig:039]).

![Проверяем метрики](image/39.png){#fig:039}

Посмотрим захваченный на соединениях трафик (рис. [-@fig:040]).

![Захваченный трафик](image/40.png){#fig:040}
![Захваченный трафик](image/41.png){#fig:041}
![Захваченный трафик](image/42.png){#fig:042}

На маршрутизаторах настроим OSPFv2 для сетей IPv4: msk-dmmosharov-gw-01 (рис. [-@fig:043]).

![Настроим OSPFv2 для msk-dmmosharov-gw-01](image/43.png){#fig:043}

На маршрутизаторах настроим OSPFv2 для сетей IPv4: msk-dmmosharov-gw-02 (рис. [-@fig:044]).

![Настроим OSPFv2 для msk-dmmosharov-gw-02](image/44.png){#fig:044}

На маршрутизаторах настроим OSPFv2 для сетей IPv4: msk-dmmosharov-gw-03 (рис. [-@fig:045]).

![Настроим OSPFv2 для msk-dmmosharov-gw-03](image/45.png){#fig:045}

На маршрутизаторах настроим OSPFv2 для сетей IPv4: msk-dmmosharov-gw-04 (рис. [-@fig:046]).

![Настроим OSPFv2 для msk-dmmosharov-gw-03](image/46.png){#fig:046}

С PC1 пропингуем PC2 и определим путь следования пакетов (рис. [-@fig:047]).

![С PC1 пропингуем PC2](image/47.png){#fig:047}

Проверим таблицу маршрутизации протокола (рис. [-@fig:048]).

![Проверка таблицы](image/48.png){#fig:048}

С PC1 пропингуем PC2 и определим путь следования пакетов (рис. [-@fig:050]).

![С PC1 пропингуем PC2](image/50.png){#fig:050}

Включим на маршрутизаторе msk-dmmosharov-gw-02 интерфейс (рис. [-@fig:051]).

![Включаем интерфейс](image/51.png){#fig:051}

Посмотрим захваченный на соединениях трафик (рис. [-@fig:052]).

![Захваченный трафик](image/52.png){#fig:052}

На маршрутизаторах настроим OSPFv3 для сетей IPv6: msk-dmmosharov-gw-01 (рис. [-@fig:053]).

![настроим OSPFv3 для сетей IPv6](image/53.png){#fig:053}

На маршрутизаторах настроим OSPFv3 для сетей IPv6: msk-dmmosharov-gw-02 (рис. [-@fig:054]).

![настроим OSPFv3 для сетей IPv6](image/54.png){#fig:054}

На маршрутизаторах настроим OSPFv3 для сетей IPv6: msk-dmmosharov-gw-03 (рис. [-@fig:055]).

![настроим OSPFv3 для сетей IPv6](image/55.png){#fig:055}

На маршрутизаторах настроим OSPFv3 для сетей IPv6: msk-dmmosharov-gw-04 (рис. [-@fig:056]).

![настроим OSPFv3 для сетей IPv6](image/56.png){#fig:056}

С PC1 пропингуем PC2 и определим путь следования пакетов (рис. [-@fig:057]).

![С PC1 пропингуем PC2](image/57.png){#fig:057}

Проверим таблицу маршрутизации протокола (рис. [-@fig:058]).

![Проверка таблицы](image/58.png){#fig:058}

С PC1 пропингуем PC2 и определим путь следования пакетов  (рис. [-@fig:060]).

![С PC1 пропингуем PC2](image/60.png){#fig:060}

Посмотрим захваченный трафик (рис. [-@fig:061]).

![Захваченный трафик](image/61.png){#fig:061}

Создадим проект в GNS3. Разместим и соеденим устройства в соответсвии с топологией. (рис. [-@fig:062]).

![Проект](image/62.png){#fig:062}

Присвоим адреса оконечным устройствам (рис. [-@fig:063]).

![Присвоим адреса](image/63.png){#fig:063}

Присвоим адреса оконечным устройствам (рис. [-@fig:064]).

![Присвоим адреса](image/64.png){#fig:064}

На маршрутизаторах перейдем в режим конфигурирования и изменим имя устройства (рис. [-@fig:065]).

![Перейдем в режим конфигурирования](image/65.png){#fig:065}

На маршрутизаторах перейдем в режим конфигурирования и изменим имя устройства (рис. [-@fig:066]).

![Перейдем в режим конфигурирования](image/66.png){#fig:066}

На маршрутизаторах перейдем в режим конфигурирования и изменим имя устройства (рис. [-@fig:067]).

![Перейдем в режим конфигурирования](image/67.png){#fig:067}

Настроим адреса на интерфейсах маршрутизаторов (рис. [-@fig:068]).

![Настроим адреса](image/68.png){#fig:068}

Настроим адреса на интерфейсах маршрутизаторов (рис. [-@fig:069]).

![Настроим адреса](image/69.png){#fig:069}

Настроим адреса на интерфейсах маршрутизаторов (рис. [-@fig:070]).

![Настроим адреса](image/70.png){#fig:070}

Убедимся, что появились адреса ближайших к ним маршрутизаторов (рис. [-@fig:071]).

![Убедимся, что появились адреса](image/71.png){#fig:071}


Настроим маршрутизацию IPv4 (рис. [-@fig:073]).

![Настройка маршрутизации](image/73.png){#fig:073}

Настроим маршрутизацию IPv4 (рис. [-@fig:074]).

![Настройка маршрутизации](image/74.png){#fig:074}

Настроим маршрутизацию IPv4 (рис. [-@fig:075]).

![Настройка маршрутизации](image/75.png){#fig:075}

Проверим маршруты (рис. [-@fig:076]).

![Проверка](image/76.png){#fig:076}

Создадим туннель IPv6 через сеть IPv4 (рис. [-@fig:077]).

![Туннель](image/77.png){#fig:077}

Создадим туннель IPv6 через сеть IPv4 (рис. [-@fig:078]).

![Туннель](image/78.png){#fig:078}

Настроим статическую маршрутизацию IPv6 (рис. [-@fig:079]).

![Настройка](image/79.png){#fig:079}

Настроим статическую маршрутизацию IPv6 (рис. [-@fig:080]).

![Настройка](image/80.png){#fig:080}

Проверим достпуность оконечных устройств (рис. [-@fig:081]).

![Проверка доступности](image/81.png){#fig:081}

Проверим достпуность оконечных устройств (рис. [-@fig:082]).

![Проверка доступности](image/82.png){#fig:082}

Проанализируем трафик (рис. [-@fig:083]).

![Трафик](image/83.png){#fig:083}

# Самостоятельная работа

Построим топологию сети (рис. [-@fig:084]).

![Топология сети](image/84.png){#fig:084}

![Самостоятельная работа](image/85.png){#fig:085}

![Самостоятельная работа](image/86.png){#fig:086}

![Самостоятельная работа](image/87.png){#fig:087}

![Самостоятельная работа](image/88.png){#fig:088}

![Самостоятельная работа](image/89.png){#fig:089}

![Самостоятельная работа](image/90.png){#fig:090}

![Самостоятельная работа](image/91.png){#fig:091}

![Самостоятельная работа](image/92.png){#fig:092}

![Самостоятельная работа](image/93.png){#fig:093}

![Самостоятельная работа](image/94.png){#fig:094}

![Самостоятельная работа](image/95.png){#fig:095}

![Самостоятельная работа](image/96.png){#fig:096}

![Самостоятельная работа](image/97.png){#fig:097}

![Самостоятельная работа](image/98.png){#fig:098}

![Самостоятельная работа](image/99.png){#fig:099}

![Самостоятельная работа](image/100.png){#fig:100}

![Самостоятельная работа](image/101.png){#fig:101}

![Самостоятельная работа](image/102.png){#fig:102}

![Самостоятельная работа](image/103.png){#fig:103}


# Выводы

В результате выполнения лабораторной работы были изучены принципы маршрутизации в IPv4- и IPv6-сетях и принципов     настройки сетевого оборудования.