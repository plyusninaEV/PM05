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
