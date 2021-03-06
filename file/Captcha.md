# Создание капчи с помощью C#

Капча (CAPTCHA) – это защитный код, который пользователю требуется ввести в специальном поле на сайте для его защиты от действия автоматических сервисов (ботов, спама, флуда и пр.), вредящих ресурсу.
Вы можете убедиться, что пользователь является реальным лицом, а не компьютерной программой, используя CAPTCHA для проверки пользователей при регистрации
CAPTCHA означает полностью автоматизированный открытый тест Turing для информирования компьютеров и людей друг от друга. CAPTCHA — это тест с запросом и ответом , в котором пользователю предлагается сделать что-то легко, но для этого достаточно сложно выполнить автоматизированную программу. Наиболее распространенным типом CAPTCHA является то, что вы видите несколько искаженных букв и запрашиваете их ввод. (Искажение должно заставить программы-роботы расшифровать буквы.)

# Два главных свойства капчи

Любая капча должна обладать двумя свойствами, без которых она не будет работать:

**Устойчивость к распознаванию** — свойство, защищающее капчу от распознавания алгоритмом — например системой распознавания текста. Гарантирует то, что человек сможет прочитать текст на картинке, а компьютер нет.
Антипример: стандартная капча форумов phpBB 2.x таким свойством не обладала — из-за относительной простоты распознавания появились скрипты, которые спамили все подряд форумы вынуждая веб-мастеров менять капчу на более стойкую.

**Устойчивость к угадыванию** — свойство капчи, не позволяющее угадать её значение за небольшое число попыток (менее 1000). Если набор возможных значений капчи невелик, программе не составит труда угадать её подбором вместо распознавания.
Антипример: арифметическая капча вроде «1+2» (перебор чисел от 1 до 20 в скором времени даст результат).
Антипример: выбрать из нескольких картинок ту, на которой изображён котик.

# Юзабилити

Не просите ввести капчу, если вы уже убедились, что перед вами человек. Тут однако, надо быть осторожным, чтобы форму нельзя было использовать скриптом неограниченное число раз после однократного ввода капчи человеком.
Пример: форма регистрации. Если я где-то регистрируюсь, и забыл ввести поле «почтовый индекс», но правильно ввёл капчу — не надо показывать мне новую. Потратьте 10 минут на то, чтобы сохранить где-то у себя, что вот эту конкретную форму сейчас пытается заполнить живой человек.

Для облегчения распознавания человеком: не используйте в капче одновременно буквы и цифры, не используйте одновременно прописные и строчные буквы, исключите похожие символы.


[Делаем свою капчу (asp.net, c#)](https://calmsen.ru/delaem-svoyu-kapchu-asp-net-c/?ysclid=l3fgj7bha3)

[Создание CAPCHA для Windows Form приложений ](http://csharpsourescode.blogspot.com/2013/02/capcha.html)

[CAPTCHA in WPF Using C#](https://www.c-sharpcorner.com/UploadFile/631fc0/captcha-in-wpf-using-C-Sharp/)

[Создание капчи на ASP.NET MVC](https://metanit.com/sharp/articles/mvc/7.php?ysclid=l3fh24lygb)
