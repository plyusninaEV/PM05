# Работа с несколькими окнами: WINDOWS

MainWindow.xaml
```
<Window x:Class="WINDOWS.MainWindow"
 …
 Title="Главное окно" SizeToContent="WidthAndHeight" 
 ResizeMode="CanMinimize" Loaded="Window_Loaded" >
<StackPanel Margin="5">
 <Button x:Name="button1" MinWidth="200" Margin="5" 
 Content="Открыть подчиненное окно" 
 Padding="5" Click="button1_Click" />
 <Button x:Name="button2" Margin="5" 
 Content="Открыть диалоговое окно" Padding="5" 
 Click="button2_Click" />
 </StackPanel>
</Window>
```
Window1.xaml
```
<Window x:Class="WINDOWS.Window1"
 …
 Title="Подчиненное окно" Height="300" Width="300" 
 ShowInTaskbar="False" >
 <Grid>
 
 </Grid>
</Window>
```
Window2.xaml
```
<Window x:Class="WINDOWS.Window2"
 …
 Title="Диалоговое окно" Height="300" Width="300" 
 WindowStartupLocation="CenterScreen" ResizeMode="NoResize" 
 ShowInTaskbar="False" WindowStyle="ToolWindow" >
 <Grid>
 
 </Grid>
</Window>
```
#  Модальные и обычные кнопки диалогового окна
```
<Window x:Class="WINDOWS.Window2"
 …
 SizeToContent="WidthAndHeight"
 IsVisibleChanged="Window_IsVisibleChanged" >
 <Grid Margin="5">
 <Grid.RowDefinitions>
 <RowDefinition/>
 <RowDefinition/>
 <RowDefinition/>
 </Grid.RowDefinitions>
 <Grid.ColumnDefinitions>
<ColumnDefinition/>
 <ColumnDefinition/>
 </Grid.ColumnDefinitions>
 <Label Content="Заголовок главного окна:" Margin="5" />
 <Label Content="Заголовок подчиненного окна:" Margin="5" 
 Grid.Row="1" />
 <TextBox x:Name="textBox1" Grid.Column="1" Margin="5" 
 Text="Главное окно" MinWidth="200" />
 <TextBox x:Name="textBox2" Grid.Column="1" Margin="5" 
 Grid.Row="1" Text="Подчиненное окно" />
 <StackPanel Grid.ColumnSpan="2" 
 HorizontalAlignment="Right" Margin="0" Grid.Row="2" 
 Orientation="Horizontal">
 <Button x:Name="button1" Content="ОК" Width="75" 
 Margin="5" IsDefault="True" 
 Click="button1_Click" />
 <Button x:Name="textBox2" Content="Применить" 
 Width="75" Margin="5" Click="button2_Click" />
 <Button Content="Отмена" Width="75" Margin="5" 
 IsCancel="True" />
 </StackPanel>
 </Grid>
</Window>
```

## Работа с датами и временем

**Отображение текущего времени**
```
<Window x:Class="CLOCK.MainWindow"
 …
 Title="Clock" ResizeMode="CanMinimize" 
 SizeToContent="WidthAndHeight" 
 WindowStartupLocation="CenterScreen">
 <StackPanel>
 <Border Margin="10" BorderBrush="Black" BorderThickness="1" >
 <TextBlock x:Name="label1" Text="00:00:00" FontSize="100" 
Padding="50" FontFamily="Arial" TextAlignment="Center"/>
 </Border>
 </StackPanel>
</Window>
```
## Выделение активного поля ввод

В файле MainWindow.xaml.cs в описание класса MainWindow добавьте 
поля
```
Brush backgr;
Brush foregr;
В конструктор класса MainWindow добавьте следующие операторы:
backgr = textBox1.Background;
foregr = textBox1.Foreground;
textBox1.Focus();
Наконец, определите в классе MainWindow ранее созданные обработчики:
private void textBox1_GotFocus(object sender, RoutedEventArgs e)
{
 TextBox tb = e.Source as TextBox;
 tb.Foreground = Brushes.White;
 tb.Background = Brushes.Green;
}
private void textBox1_LostFocus(object sender, RoutedEventArgs e)
{
 TextBox tb = e.Source as TextBox;
 tb.Foreground = foregr;
 tb.Background = backgr;
}
```
