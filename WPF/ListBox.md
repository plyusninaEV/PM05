# ListBox

ListBox - это элемент управления, который предоставляет список элементов для выбора элемента пользователем. Пользователь может выбрать один или несколько элементов из предопределенного списка элементов одновременно. В списке несколько параметров всегда видны пользователю без какого-либо взаимодействия с пользователем

[ListBox Класс](https://googleweblight.com/sp?hl=ru-RU&geid=NSTN&u=https://docs.microsoft.com/ru-ru/dotnet/api/system.windows.forms.listbox)

# Пример

- Давайте создадим новый проект WPF с именем WPFListBoxControl.
- Перетащите одно поле списка и одно текстовое поле из панели инструментов.
- Когда пользователь выбирает какой-либо элемент из списка, он также отображается в текстовом поле.
- Вот код XAML, в котором ListBox и TextBox создаются и инициализируются некоторыми свойствами.

```
<Window x:Class = "WPFListBoxControl.MainWindow" 
 xmlns = "http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
 xmlns:x = "http://schemas.microsoft.com/winfx/2006/xaml" 
 xmlns:d = "http://schemas.microsoft.com/expression/blend/2008" 
 xmlns:mc = "http://schemas.openxmlformats.org/markup-compatibility/2006" 
 xmlns:local = "clr-namespace:WPFListBoxControl"
 mc:Ignorable = "d" Title = "MainWindow" Height = "350" Width = "604">
 
 <Grid> 
 <ListBox Name = "listbox" Margin = "118,77,293,103">
 <ListBoxItem Content = "XAML Tutorials" /> 
 <ListBoxItem Content = "WPF Tutorials" /> 
 <ListBoxItem Content = "Silverlight Tutorials" /> 
 <ListBoxItem Content = "Windows 10 Tutorials" /> 
 <ListBoxItem Content = "iOS Tutorials" /> 
 </ListBox> 
 
 <TextBox Height = "23" x:Name = "textBox1" Width = "120" Margin = "361,116,0,0" 
 HorizontalAlignment = "Left" VerticalAlignment = "Top" 
 Text="{Binding SelectedItem.Content, ElementName=listbox}" /> 
 </Grid> 
 
</Window>
 x:Class = "WPFListBoxControl.MainWindow" 
   xmlns = "http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
   xmlns:x = "http://schemas.microsoft.com/winfx/2006/xaml" 
   xmlns:d = "http://schemas.microsoft.com/expression/blend/2008" 
   xmlns:mc = "http://schemas.openxmlformats.org/markup-compatibility/2006" 
   xmlns:local = "clr-namespace:WPFListBoxControl"
   mc:Ignorable = "d" Title = "MainWindow" Height = "350" Width = "604">
	
   <Grid> 
      <ListBox Name = "listbox" Margin = "118,77,293,103">
         <ListBoxItem  Content= "XAML Tutorials" /> 
         <ListBoxItem Content = "WPF Tutorials" /> 
         <ListBoxItem Content = "Silverlight Tutorials" /> 
         <ListBoxItem Content = "Windows 10 Tutorials" /> 
         <ListBoxItem Content = "iOS Tutorials" /> 
      </ListBox> 
		
      <TextBox Height = "23" x:Name = "textBox1" Width = "120" Margin = "361,116,0,0"  
         HorizontalAlignment = "Left" VerticalAlignment = "Top"  
         Text="{Binding SelectedItem.Content, ElementName=listbox}" /> 
   </Grid> 
	
</Window>
```
![](https://github.com/plyusninaEV/PM05/blob/main/WPF/images/output_of_listbox.png)

# Перенос текста в listbox

Вам придется переопределить шаблон элемента списка и указать ему необходимость переноса текста явно. К тому же придется отключить горизонтальный скроллбар, иначе контейнер будет всегда давать элементам столько места сколько они хотят:
```
<ListBox FontFamily="Times New Roman" FontSize="16"
         ScrollViewer.HorizontalScrollBarVisibility="Disabled">
    <ListBox.ItemContainerStyle>
        <Style TargetType="ListBoxItem">
            <Setter Property="Background" Value="Gainsboro"/>
            <Setter Property="Margin" Value="5"/>
            <Setter Property="Padding" Value="5"/>
        </Style>
    </ListBox.ItemContainerStyle>
    <ListBox.ItemTemplate>
        <DataTemplate>
            <TextBlock Text="{Binding}" TextWrapping="Wrap"/>
        </DataTemplate>
    </ListBox.ItemTemplate>
</ListBox>
```
![](https://github.com/plyusninaEV/PM05/blob/main/WPF/images/8n9mA.gif)

# Пример 

[ListBox In WPF](https://www.c-sharpcorner.com/uploadfile/mahesh/listbox-in-wpf/)

[The ListBox control](https://www.wpf-tutorial.com/list-controls/listbox-control/)

