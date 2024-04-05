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
