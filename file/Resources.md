# Resources

Модель WPF предлагает очень удобный функционал: возможность хранить данные как ресурс, локально для элемента управления, локально для всего окна либо глобально для всего приложения. Данные могут быть любыми по факту, начиная от текущей информации, заканчивая иерархией элементов WPF. Это позволяет разместить данные в одном месте и после этого использовать их в разных местах, что может пригодится при разработке.
Этот функционал часто используется для работы со стилями и шаблонами, которые мы еще будем обсуждать в руководстве, но, как будет показано в этой главе - область применения ресурсов очень широкая. 
```
<Window x:Class="WpfTutorialSamples.WPF_Application.ResourceSample"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:sys="clr-namespace:System;assembly=mscorlib"
        Title="ResourceSample" Height="150" Width="350">
    <Window.Resources>
        <sys:String x:Key="strHelloWorld">Hello, world!</sys:String>
    </Window.Resources>
    <StackPanel Margin="10">
        <TextBlock Text="{StaticResource strHelloWorld}" FontSize="56" />
        <TextBlock>Just another "<TextBlock Text="{StaticResource strHelloWorld}" />" example, but with resources!</TextBlock>
    </StackPanel>
</Window>
```

Ресурсы в WPF имеют ключ (атрибут **x:Key**), с помощью которого становится возможным сослаться на эти ресурсы из любой другой части приложения, используя ключ с выражением разметки StaticResource. В этом примере я просто сохранил строку в ресурсах, которую позже использовал в двух разных элементах **TextBlock**.


WPF имеет 2 типа ресурсов.
1. Статический ресурс
1. Динамический ресурс

Как объявить: здесь мы можем объявить ресурсы в соответствии с их областью использования. Есть 4 способа:

Ресурсы оконного уровня:

```
<Window.Resources>
<Thickness x:Key="MarginTop">0 5 0 0</Thickness>
</Window.Resources>  
```
Ресурсы панельного уровня:
```
<Grid.Resources>
<Thickness x:Key="MarginTR">0 5 5 0</Thickness>
</Grid.Resources> 
```
Ресурсы прикладного уровня
 
Перейдите в App.xaml приложения
```
<Application.Resources>
<Thickness x:Key="MarginTR">0 5 5 0</Thickness>
</Application.Resources>
```

[Работа с ресурсами приложения](https://metanit.com/sharp/wpf/3.3.php?#:~:text=%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%20%D1%81%20%D1%80%D0%B5%D1%81%D1%83%D1%80%D1%81%D0%B0%D0%BC%D0%B8%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
