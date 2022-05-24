# Связывание данных в WPF

Связывание данных это общепринятый механизм, при котором осуществляется связывание двух источников данных/информации с последующей их синхронизацией.

Связывание в WPF - это наиболее предпочтительный вариант доставки данных от кода до графического интерфейса. Конечно, Вы можете определять свойства элементов управления вручную или создать ListBox, добавляя содержимое в цикле, но наиболее простым способом в WPF будет "связывание" источника данных и целевого элемента интерфейса.

Ключом к механизму привязки к данным является объект класса System.Windows.Data.Binding, который «склеивает» между собой два свойства и открывает коммуникационный канал между ними. Объект Binding можно один раз настроить и поручить ему дальнейшую заботу о синхронизации.

- [Привязка элементов](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level8/8_1.php)
- [Команды](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level9/9_1.php)
- [Ресурсы](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level10/10_1.php)
- [Стили](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level8/bas_WPF_index.php?ysclid=l3k2fz199j)
- [Привязка данных](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level19/19_1.php)
- [Форматирование привязанных данных](https://professorweb.ru/my/WPF/binding_and_styles_WPF/level8/bas_WPF_index.php?ysclid=l3k2fz199j)



[Общие сведения о привязке данных (WPF .NET)](https://docs.microsoft.com/ru-ru/dotnet/desktop/wpf/data/?view=netdesktop-5.0)
