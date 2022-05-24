# Класс List<T>
  Начнем наше знакомство с коллекциями с класса List<T>. Эта коллекция является аналогом типизированного массива, который может динамически расширяться. В качестве типа можно указать любой встроенный либо пользовательский тип.

## Создание объекта класса List<T>

Можно создать пустой список и добавить в него элементы позже, с помощью метода Add():
```
List<int> numsList = new List<int>();
numsList.Add(1);
```
Либо воспользоваться синтаксисом, позволяющем указать набор объектов, который будет храниться в списке:
```
List<int> nums = new List<int> {1, 2, 3, 4, 5};
var words = new List<string> {"one", "two", "three"};
  ```
## Работа с объектами List<T>

Ниже приведены таблицы, в которых перечислены некоторые полезные свойства и методы класса List<T>. Более подробную информацию по методам и свойствам List<T> вы можете найти в официальной документации.

## Свойства класса List<T>

| Свойство | Описание |
|----:|:----------|
| Count |	Количество элементов в списке |
| Capacity |	Емкость списка – количество элементов, которое может вместить список без изменения размера |
  
  ```
  Console.WriteLine("Свойства");
Console.WriteLine($"- Count: nums.Count = {nums.Count}");
Console.WriteLine($"- Capacity: nums.Capacity = {nums.Capacity}");
```

## Методы класса List<T>
  
| Метод  |	Описание|
|------:|:-------| 
| Add(T) |	Добавляет элемент к списку |
| BinarySearch(T) | 	Выполняет поиск по списку |
| Clear() | 	Очистка списка
| Contains(T) |	Возвращает true, если список содержит указанный элемент|
| IndexOf(T) |	Возвращает индекс переданного элемента |
| ForEach(Action<T>) |	Выполняет указанное действие для всех элементов списка |
| Insert(Int32, T) |	Вставляет элемент в указанную позицию |
|Find(Predicate<T>) |	Осуществляет поиск первого элемент, для которого выполняется заданный предикат |
|Remove(T) |	Удаляет указанный элемент из списка |
|RemoveAt(Int32) | 	Удаляет элемент из заданной позиции |
| Sort() |	Сортирует список |
| Reverse() |	Меняет порядок расположения элементов на противоположный |

  ```
  Console.WriteLine($"nums: {ListToString(nums)}");            
nums.Add(6);
Console.WriteLine($"nums.Add(6): {ListToString(nums)}");            
Console.WriteLine($"words.BinarySearch(\"two\"): {words.BinarySearch("two")}");
Console.WriteLine($"nums.Contains(10): {nums.Contains(10)}");
Console.WriteLine($"words.IndexOf(\"three\"): {words.IndexOf("three")}");
Console.WriteLine($"nums.ForEach(v => v * 10)");
nums.ForEach(v => Console.Write($"{v} => "));            
nums.Insert(3, 7);
Console.WriteLine($"nums.Insert(3, 7): {ListToString(nums)}");
Console.WriteLine($"words.Find(v => v.Length == 3): {words.Find(v => v.Length == 3)}");
words.Remove("two");
Console.WriteLine($"words.Remove(\"two\"): {ListToString(words)}");
```
Код метода ListToString:
  ```
static private string ListToString<T>(List<T> list) =>
"{" + string.Join(", ", list.ToArray()) + "}";
```
Далее приведен пример работы со списком, в котором хранятся объекты пользовательского типа. Создадим класс Player, имеющий свойства: Name и Skill.
```
  class Player
{
    public string Name { get; set; }
    public string Skill { get; set; }
}
```
Создадим список игроков и выполним с ним ряд действий:
  ```
Console.WriteLine("Работа с пользовательским типом");
List<Player> players = new List<Player> {
    new Player { Name = "Psy", Skill = "Monster"},
    new Player { Name = "Kubik", Skill = "Soldier"},
    new Player { Name = "Triver", Skill = "Middle"},
    new Player { Name = "Terminator", Skill = "Very High"}
};
Console.WriteLine("Количество элементов в players:{0}", players.Count);
//Добавим новый элемент списка players
players.Insert(1, new Player { Name = "Butterfly", Skill = "flutter like a butterfly, pity like a bee"});
//Посмотрим на все элементы списка
players.ForEach(p => Console.W
```
# Пример работы с элементами
  ```
  using System;
using System.Collections.Generic;

namespace Lists
{
    class Program
    {
    static void Main(string[] args)
    {
        List<User> listOfUsers = new List<User>()
        {
        new User() { Name = "John Doe", Age = 42 },
        new User() { Name = "Jane Doe", Age = 34 },
        new User() { Name = "Joe Doe", Age = 8 },
        };

        for(int i = 0; i < listOfUsers.Count; i++)
        {
        Console.WriteLine(listOfUsers[i].Name + " is " + listOfUsers[i].Age + " years old");
        }
        Console.ReadKey();
    }
    }

    class User
    {
    public string Name { get; set; }

    public int Age { get; set; }
    }
}
```
Cнизу определили простой класс для хранения информации о пользователе - просто имя и возраст. Вернемся к верхней части примера, где изменили наш список, чтобы использовать этот класс пользователя вместо простых строк. Здесь используется инициализатор коллекции для заполнения списка пользователями - обратите внимание, что синтаксис тот же, что и раньше, только немного сложнее, потому что мы имеем дело с более сложным объектом, чем строка.     
                                             
## Сортировка
```
using System;
using System.Collections.Generic;

namespace ListSort
{
    class Program
    {
    static void Main(string[] args)
    {
        List<User> listOfUsers = new List<User>()
        {
        new User() { Name = "John Doe", Age = 42 },
        new User() { Name = "Jane Doe", Age = 39 },
        new User() { Name = "Joe Doe", Age = 13 },
        };
        listOfUsers.Sort(CompareUsers);
        foreach (User user in listOfUsers)
        Console.WriteLine(user.Name + ": " + user.Age + " years old");
    }

    public static int CompareUsers(User user1, User user2)
    {
        return user1.Age.CompareTo(user2.Age);
    }
    }

    public class User
    {
    public string Name { get; set; }
    public int Age { get; set; }
    }
}
  ```
[ListBox Класс](https://googleweblight.com/sp?hl=ru-RU&geid=NSTN&u=https://docs.microsoft.com/ru-ru/dotnet/api/system.windows.forms.listbox)
