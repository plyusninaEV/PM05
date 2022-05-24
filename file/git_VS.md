# Формирование репозитория проекта, определение уровня доступа в системе контроля версий. Распределение ролей

Система контроля версий (англ. Version Control System) - программное обеспечение хранящееся все версии возможного файла, и дающее возможность получить к ним доступ. Существуют разные системы: git, mercurial, subversion(svn), Team Foundation server (TFS), однако наибольшую популярность завоевала система Git из-за простоты использования и внедрения в другие системы.

# Принципы Git
Разберём основные понятия git систем:

- Репозиторий - обособленное хранилище кода внутри которого будут отслеживаться изменения файлов
- Ветвь (branch) - отдельная цепочка (ветка) отслеживаемых изменений
- Мастер branch - главная ветка в репозитории
- Коммит - зафиксированная точка изменений
- Удаленный сервер (remote server) - сервер на котором хранится репозиторий
- Merge (слияние) - процесс слияния двух ветвей
- tag - ссылка на определенный коммит

[**Git**](https://github.com/plyusninaEV/test/blob/main/Git.md) - это утилита для работы в командной строке (хотя есть и опции для работы через графический интерфейс)

Основные команды:
- **git pull** - забрать изменения с удалённого сервера
- **git push** - отправить локальные изменения на удалённый сервер
- **git branch** - показать текущую ветку/список веток
- **git merge** <branch_name> - влить в текущую ветку указанную
- **git add** - добавить в текущее состояние изменённые файлы
- **git commit** - зафиксировать изменения и сделать коммит
- **git stash** - сохранить локальные изменения не создавая коммит и откатиться до состояния удалённого сервера

Курс для самостоятельной работы: https://stepik.org/course/3145

Работа с Git: https://smartiqa.ru/courses/git

[История изменений и колективная работа в C#. Visual Studio и GitHub](https://zen.yandex.ru/media/pss/istoriia-izmenenii-i-kolektivnaia-rabota-v-c-visual-studio-i-github-5f88542d9eb9a66f8bb62712)

[Совместная разработка в команде на GitHub](https://code.tutsplus.com/ru/articles/team-collaboration-with-github--net-29876)

# Команда проекта, роли и функции членов команды


[ИТ-КОМАНДЫ: ИХ ФУНКЦИИ И ТИПЫ](https://www.careerist.com/ru-insights/it-komandy-ih-funkcii-i-tipy?)

[Распределение ролей в современной IT команде](https://www.be-analyst.ru/single-post/2019/07/30/%D1%80%D0%B0%D1%81%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%80%D0%BE%D0%BB%D0%B5%D0%B9-%D0%B2-%D1%81%D0%BE%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9-it-%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B5)