# Файл App.xaml

App.xaml.cs расширяет класс Application, который является базовым классом в приложении WPF Windows. .NET сначала реализует в этом классе стартовые инструкции, а после запускает необходимую страницу WPF. Этот класс, так же, является местом для подписки на важные события в приложении, такие как: старт приложения, необработанные исключения и др., но об этом немного позже.

## Структура App.xaml

Основная задача данного файла состоит в определении ресурсов, общих для приложения. Поэтому тут по умолчанию определен пустой элемент Application.Resources, в который, собственно, и помещаются ресурсы. 

```
<Application x:Class="WpfTutorialSamples.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             StartupUri="MainWindow.xaml">
    <Application.Resources>

    </Application.Resources>
</Application>
```
Главным местом в этом коде является свойство StartupUri. Собственно, эта часть сигнализирует приложению о том, какая Страница или Окно будет являться домашним при запуске. В этом случае, MainWindow.xaml будет домашней страницей, но при желании Вы можете изменить ее на любую другую, просто изменив содержание свойства StartupUri



Структура App.xaml.cs

Обычно, файл App.xaml.cs для нового проекта будет выглядеть следующим образом:

```
using System;
using System.Collections.Generic;
using System.Windows;

namespace WpfTutorialSamples
{
	public partial class App : Application
	{

	}
}
```
[Класс Application](https://docs.microsoft.com/ru-ru/dotnet/desktop/wpf/app-development/application-management-overview?view=netframeworkdesktop-4.8#:~:text=%D0%B8%20%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%20%D0%B8%D0%BC%D0%B8.-,%D0%9A%D0%BB%D0%B0%D1%81%D1%81%20Application,-%D0%92%20WPF%20%D0%BE%D0%B1%D1%89%D0%B8%D0%B5)

[Приложение и класс Application](https://metanit.com/sharp/wpf/3.php#:~:text=%D0%9D%D0%90%D0%A1%D0%A2%D0%A0%D0%9E%D0%99%D0%9A%D0%98-,%D0%9F%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B8%20%D0%BA%D0%BB%D0%B0%D1%81%D1%81%20Application,-%D0%9A%D0%BB%D0%B0%D1%81%D1%81%20Application)

[Создание стиля элемента управления (WPF .NET)](https://docs.microsoft.com/ru-ru/dotnet/desktop/wpf/controls/how-to-create-apply-style?view=netdesktop-5.0#:~:text=%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%D1%82%D0%B8%D0%BB%D1%8F%20%D1%8D%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%20%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F%20(WPF%20.NET))

[Пример 1](https://www.nookery.ru/wpf-static-and-dynamic-resources/?)
