# Файл App.xaml

App.xaml.cs расширяет класс Application, который является базовым классом в приложении WPF Windows. .NET сначала реализует в этом классе стартовые инструкции, а после запускает необходимую страницу WPF. Этот класс, так же, является местом для подписки на важные события в приложении, такие как: старт приложения, необработанные исключения и др., но об этом немного позже.

## Структура App.xaml

```
<Application x:Class="WpfTutorialSamples.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             StartupUri="MainWindow.xaml">
    <Application.Resources>

    </Application.Resources>
</Application>
```
