# Принципы создания графического пользовательского интерфейса (GUI)

Для создания интерфейса, который делал бы работу с программой приятной, разработчику нужно понимать, какие задачи будут решать пользователи с помощью данной программы. Выделяют общие принципы проектирования пользовательских интерфейсов:

1. Программа должна помогать выполнить задачу, а не становиться этой задачей. Интерфейс должен быть легким для освоения и не создавать перед пользователем преграду, которую он должен будет преодолеть, чтобы приступить к работе.

2. При работе с программой пользователь не должен ощущать себя дураком. Не нужно давать разрабатываемой программе слишком большие полномочия и право указывать пользователю, что именно ему делать. Один из примеров такого неправильного отношения к пользователю является отказ программы выполнить вполне естественную с точки зрения пользователя программных продуктов операцию и вывод диалогового окна, требующего выполнить какую-то другую последовательность действий. Например, известный текстовый редактор "Блокнот" из состава Windows95. Если пользователь открывал эту программу и решал перед началом набора текста дать создаваемому "Блокнотом" по умолчанию файлу "Untitled" какое-нибудь имя, выбрав из меню команду Сохранить как, редактор отказывался сделать это, показывая сообщение: "Вы не ввели какой-либо текст, чтобы его можно было сохранить. Наберите какой-нибудь текст, а затем попытайтесь [сохранить его] снова". Другой пример недооценки возможностей пользователя — вывод информационных сообщений в ситуациях, когда этого не требуется. Например, для того, чтобы облегчить освоение продукта или информировать пользователей о полезных функциях программы. Но если пользователь уже достаточно уверенно чувствует себя при работе с программой и не нуждается в подсказках, выскакивающих каждую минуту. Поэтому среди разработчиков программного обеспечения хорошим тоном считается предоставление пользователю возможности отключить вывод информационных сообщений. Это позволяет сохранить легкость освоения продукта для начинающих пользователей и добиться того, чтобы информационные сообщения не вызывали у опытных пользователей раздражения.

3. Программа должна работать так, чтобы пользователь не считал компьютер дураком. Программа не должна прерывать работу пользователя глупыми вопросами и выводить на экран бессмысленные сообщения, повергая его в недоумение в самых простых ситуациях. Например, вопрос о подтверждении изменений в базе данных при уходе пользователя из карточки студента будет лишним, если пользователь не изменял данные студента.

**Формы** - это строительные блоки интерфейса пользователя. Особый вид форм - формы, предназначенные для ввода данных. В форме ввода данных необходимо максимально использовать свободное пространство, поскольку открытие и закрытие дополнительных форм существенно замедляет работу. При разработке форм ввода данных следует придерживаться следующих правил:

- Всегда назначайте клавиатурные эквиваленты команд.
- Расположение элементов должно быть согласовано с задачами пользователя. Не заставляйте пользователя перепрыгивать из раздела в раздел, при вводе информации это совсем не обязательно. Если пользователь собирается ввести около 1000 записей, то необходимо расположить на форме кнопку подтверждения ввода данных, а не подтверждать их ввод после каждой записи.
- Не заставляйте пользователя выполнять лишнюю работу. Например, если информация, содержащаяся в полях со 2-го по 10-е, необходима только, когда первое поле имеет определенное значение, не нужно заставлять пользователя заполнять все поля подряд.
- Используйте заметную, но ненавязчивую обратную связь с пользователем. Например, всплывающая подсказка на кнопках или окрашивание полей в красный цвет, если они заполнены некорректно или если они должны быть заполнены в обязательном порядке.
- Если возможно, выполняйте добавление и редактирование записей в одной и той же форме, тогда пользователю не придется осваивать несколько методов доступа к одним и тем же данным.

Если в программе присутствует несколько форм, необходимо определиться с видом интерфейса:

- однодокументный (SDI). Однодокументный интерфейс - это тип интерфейса, в котором предоставляется возможность работы только с одним документом в одном окне. Для работы с несколькими документами в таком интерфейсе необходимо многократно запускать приложение. Для каждого типа данных и документов требуется своя форма и, соответственно, свое приложение с интерфейсом типа SDI.
- многодокументный (MDI). Главная особенность MDI заключается в том, что для этого типа интерфейса можно многократно открывать форму одного вида документа для нескольких разных по содержанию документов (например, программа Microsoft Word). Для интерфейса такого типа характерно наличие одного главного окна (MDI-окно), которое обычно именуется родительским окном, и необходимого для работы количества подчиненных (вложенных) окон, называемых дочерними. Количество открытых дочерних окон ограничено лишь возможностями компьютера.

Не зависимо от выбранного вида интерфейса необходимо продумать сценарий появлений форм на экране так, чтобы у пользователей не было возможности нарушить предписанные ход выполнения  программы (например, пользователь не может открыть форму редактирования ведомости, если список доступных для редактирования ведомостей пуст).

Рекомендации по созданию пользовательского интерфейса:

Небольшая палитра инструментов. Логическое развитие правила применения стандартных элементов: не используйте слишком большое их количество. Например, если где-то в одном из диалоговых окон программы вы поместили командную кнопку стандартного вида, то не нужно в другом месте программы использовать кнопку, отличающуюся от нее по оформлению.

Одинаковое расстояние между элементами управления. Элементы управления на форме приложения располагаются на разном расстоянии между ними.

**TabOrder**. "Правильный" порядок. TabOrder — это порядок, в котором экранный курсор перемещается по элементам управления в форме при нажатии клавиши <Таb> на клавиатуре компьютера. На стадии разработки программы, при размещении элементов управления на форме, TabOrder эквивалентен тому порядку, в котором создаются эти элементы. Однако в процессе проектирования программы автор многократно меняет расположение элементов на форме, какие-то из них удаляет, добавляет новые компоненты. В результате почти всегда оказывается, что TabOrder не соответствует тому порядку, в котором визуально расположены элементы, и при нажатии клавиши <Таb> курсор хаотично скачет по экрану вместо последовательного перемещения по компонентам.

**Выбор шрифтов**. Не стоит выбирать никаких шрифтов. Оставьте их такими, какими они определены по умолчанию. В этом случае смена пользователем стандартных шрифтов Windows по своему вкусу с помощью Панели управления отразится и на внешнем виде вашей программы. Таким образом, пользователь, запустив ваш продукт, окажется в знакомом ему окружении.

**Выбор цветов**. При создании интерфейса забудьте о свойстве Цвет (Color) элементов управления. Оставьте цвета стандартными, и пусть ваша программа выглядит так, как этого хочет ее пользователь. Если вы хотите указать цвета в своей программе, то это может послужить причиной возникновения одного неприятного эффекта. Так как с помощью Панели управления можно легко изменить цветовую гамму Windows. Жестко фиксируя в своей программе выбранные цвета, автор не учитывает, что его программа выглядит хорошо только до тех пор, пока она работает на компьютере с такой же цветовой гаммой, как и на компьютере разработчика. Если же ее запускают в системе с другим цветовым оформлением, то результат может выглядеть, мягко говоря, не очень хорошо. Для предотвращения таких досадных ошибок в процессе разработки программы нужно время от времени переключаться на другие цветовые "схемы" Windows.

В графическом пользовательском интерфейсе элемент управления — это средство, при помощи которого пользователь взаимодействует с компьютерной программой. Качество этого взаимодействия зависит от двух аспектов:

- соответствия элемента управления выполняемой им задаче;
- от последовательности правил, по которым функционирует элемент управления.

Достаточно выбрать не тот инструмент работы или изменить правила, но которым он действует, и вы создадите проблемы для пользователей своей программы.

Заголовок окна (формы). Данный элемент определяется свойством Заголовок (Caption) объекта Форма (Form).Заголовок главного окна программы традиционно используется для вывода информации о двух вещах: названии программы и названии документа, с которым в данный момент работает пользователь.

Командные кнопки. Наиболее частая ошибка начинающих разработчиков интерфейсов — использование в проекте нестандартных кнопок, включающих, помимо текста, также и графику. Почти всегда у автора программы не хватает рисунков на все кнопки, имеющиеся в программе, и часть кнопок приходится делать обычными, с текстовыми подписями и без рисунков.  Командная кнопка — один из тех элементов управления, для которых наиболее часто применяется динамически изменяемое свойство disable, т. е. отключение кнопки, когда она перестает реагировать на нажатия, и ее включение, в зависимости от текущего состояния программы. Для индикации состояния отключения граница вокруг кнопки и буквы текста на ней становятся светло-серыми. Например, в диалоговых окнах кнопка ОК остается недоступной до тех нор, пока пользователь не введет необходимые данные, т. е. при каждом изменении информации происходит ее проверка. Но если пользователь при вводе сложных данных может не иметь информации о том, что именно он делает неправильно. "Серая" отключенная кнопка только говорит ему о том, что он что-то сделал не так, как нужно — например, ввел неверные или неполные данные, но вот в чем конкретно состоит проблема, пользователь понять не может. В этом случае стоит сделать так, чтобы кнопка ОК была доступном, а после ее нажатия выдавалось бы сообщение об ошибке. Например, командная кнопка сохранить может становиться активной только в том случае, если были внесены изменения в карточку студента.

Меню - список команд по работе с программой, предлагаемых на выбор пользователя. Рекомендации по созданию меню:

- Группировать пункты меню в логическом порядке и по содержанию.
- Для группировки пунктов в раскрывающихся меню использовать разделительные линии
- Избегать избыточных меню.
- Избегать пунктов меню верхнего уровня, не содержащих раскрывающихся меню
- По возможности использовать клавиатурные эквиваленты команд и "горячие" клавиши.

   Списки. Элемент управления Список (ListBox) позволяет легко просматривать большие объемы информации и осуществлять выделение нужных строк. Например, его удобно использовать для формирования группы учащихся, перетаскивая из списка всех учащихся данного курса в список учащихся формируемой группы.
   
   # Принципы построения интерфейсов

Золотое сечение. Форма, в основе построения которой лежит сочетание симметрии и золотого сечения, способствует наилучшему зрительному восприятию. Золотое сечение — это такое пропорциональное деление отрезка на неравные части, при котором весь отрезок так относится к большей части, как сама большая часть относится к меньшей; или другими словами, меньший отрезок так относится к большему, как больший ко всему.

а : b =  b : с или с : b = b : а.

Отрезки золотой пропорции выражаются бесконечной иррациональной дробью 0,618..., если с принять за единицу, а = 0,382. Отношение же отрезков а и b составляет 1,618. Прямоугольник с таким отношением сторон стали называть золотым прямоугольником.

Формы диалоговых окон и элементов управления, стороны которых относятся как 1,618, очень привлекательны для пользователей.

 Вкладки (Tabs) позволяют логически группировать большое количество информации, тем самым дают возможность пользователю комфортно воспринимать ее. Например, режим редактирования данных о студенте.
 
 Принцип группировки. Согласно этому правилу, экран программы должен быть разбит на ясно очерченные блоки элементов, может быть, даже с заголовком для каждого блока. 
 
 Видимость отражает полезность. Смысл этого принципа состоит в том, чтобы вынести самую важную информацию и элементы управления на первый план и сделать их легкодоступными пользователю, а менее важную — переместить, например, в меню. 
 
 Равенство между системой и реальным миром. Система должна разговаривать с пользователем на его языке. Имеется в виду не язык его страны, хотя это тоже имеет значение. В данном случае подразумевается использование понятий и образов, которые уже знакомы пользователю по реальному миру, к которым он привык. Нельзя использовать специализированные термины. Многие авторы даже при разработке приложений, ориентированных на широкую аудиторию, применяют понятия, которые годятся только для профессиональных справочников по программированию. Например, сохранение данных в сетевой информационной системе происходит про подтверждении транзакции, при этом пользователь программы при сохранении данных нажимает на кнопку с надписью «Сохранить», но не все пользователи поймут назначение кнопку с надписью «Подтвердить транзакцию».

Однако такое заимствование идей из окружающего мира нужно производить осторожно. Дело в том, что программы, которые уже знакомы пользователю — тоже часть его мира, часть его знаний, навыков и привычек. Поэтому некоторые детали компьютерных интерфейсов являются для пользователей более привычными, чем объекты реального мира — это особенно касается элементов интерфейса, реализующих функции, не имеющих прямых аналогов в реальном мире.

Свобода действий пользователя. Пользователь должен иметь контроль над системой и возможность изменить текущее состояние программы. Очень часто пользователь дает различные команды по ошибке (например, случайно нажав не ту кнопку или "промахнувшись" мышью мимо нужного пункта меню), и у него должен быть "аварийный выход" из этой ситуации, четко обозначенный в программе. Чаще всего такой "выход" реализуется в виде кнопки «Отмена», расположенной в диалоговом окне и позволяющей прекратить выполнение текущей операции или закрыть это диалоговое окно. Кроме этого, нажатие на клавиатуре клавиши <Escape> является традиционным и поэтому привычным для большинства пользователей средством "аварийного выхода".

Последовательность и стандарты. Принцип последовательности означает использование одних и тех же средств для выражения схожих образов и выполнения действий, имеющих одинаковую природу. Принцип последовательности при разработке интерфейсов должен соблюдаться буквально во всем.

Во-первых, последовательность при выборе средств оповещения о событиях и действиях. Например, информация о текущем статусе программы, как уже говорилось при рассмотрении принципа "Видимость состояния системы", обычно выводится в статусную строку в нижней части экрана, а сообщения с результатами запросов пользователя — в отдельном диалоговом окне. Сообщения о критических ошибках при этом должны сильно отличаться от обычных информационных сообщений: например, они могут сопровождаться резким звуком.

Во-вторых, последовательность при оформлении элементов интерфейса. Если дизайн форм вашей программы основан на классическом интерфейсе Windows-приложений, характеризующемся строгой цветовой гаммой, прямыми линиями и углами, то очень странным выглядело бы решение придать одному из окон программы овальную форму и раскрасить его яркими цветами.

В-третьих, последовательность при выборе терминов. Пользователей не должно сбивать с толку то, что три разных понятия, используемых в вашей программе, на самом деле означают одно и то же. Например, для сохранения информации в программе будут использовать кнопки с надписью «Сохранить», а не кнопки с различными надписями такими как «Сохранить», «Подтвердить», «Отправить на сервер».
 
 # Проектирование
 
 ## Основы проектирования классических приложений
 
 - Как разработать отличный пользовательский интерфейс для классических приложений(https://docs.microsoft.com/ru-ru/windows/win32/uxguide/how-to-design-desktop-ux)
 - Контрольный список пользовательского интерфейса для классических приложений(https://docs.microsoft.com/ru-ru/windows/win32/uxguide/top-violations)
 
 Windows (основы проектирования)(https://docs.microsoft.com/ru-ru/windows/win32/uxguide/windows)
 
 Рекомендации(https://docs.microsoft.com/ru-ru/windows/win32/uxguide/guidelines)

 [Проектирование графического интерфейса пользователя](https://habr.com/ru/post/208966/?ysclid=l3k0zej3a0)
