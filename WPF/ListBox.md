# ListBox

ListBox - это элемент управления, который предоставляет список элементов для выбора элемента пользователем. Пользователь может выбрать один или несколько элементов из предопределенного списка элементов одновременно. В списке несколько параметров всегда видны пользователю без какого-либо взаимодействия с пользователем

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
