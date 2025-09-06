# listtoArray
В классе Solution есть два публичных статических метода:

String[] toStringArray(ArrayList<String>), в котором нужно преобразовать список строк в массив строк и вернуть его;
Integer[] toIntegerArray(ArrayList<Integer>), в котором нужно преобразовать список чисел в массив чисел и вернуть его.
Для преобразования списка в массив используй метод списка toArray(), в который нужно передать ссылку на конструктор массива, тип которого соответствует типу списка.
Метод main() не принимает участие в тестировании.


Вpackage com.javarush.task.pro.task18.task1810;

import java.util.ArrayList;
import java.util.Collections;

/* 
Преобразование списка в массив
*/

public class Solution {

    public static void main(String[] args) {
        var strings = new ArrayList<String>();
        Collections.addAll(strings, "Ты", "ж", "программист");

        var integers = new ArrayList<Integer>();
        Collections.addAll(integers, 1000, 2000, 3000);


        String[] stringArray = toStringArray(strings);
        for (String string : stringArray) {
            System.out.println(string);
        }

        Integer[] integerArray = toIntegerArray(integers);
        for (Integer integer : integerArray) {
            System.out.println(integer);
        }
    }

    public static String[] toStringArray(ArrayList<String> strings) {
        return strings.toArray(String[]::new);
    }

    public static Integer[] toIntegerArray(ArrayList<Integer> integers) {
        return integers.toArray(Integer[]::new);
    }
}

























Псевдокод программы:

```
ПСЕВДОКОД: Преобразование списка в массив

ПРОГРАММА Solution:

ФУНКЦИЯ main():
    СОЗДАТЬ пустой список strings типа ArrayList<String>
    ДОБАВИТЬ в strings элементы: "Ты", "ж", "программист"
    
    СОЗДАТЬ пустой список integers типа ArrayList<Integer>
    ДОБАВИТЬ в integers элементы: 1000, 2000, 3000
    
    ВЫЗВАТЬ toStringArray(strings) и сохранить результат в stringArray
    ДЛЯ КАЖДОГО элемента string В stringArray:
        ВЫВЕСТИ string
        
    ВЫЗВАТЬ toIntegerArray(integers) и сохранить результат в integerArray
    ДЛЯ КАЖДОГО элемента integer В integerArray:
        ВЫВЕСТИ integer

ФУНКЦИЯ toStringArray(список strings):
    ПРЕОБРАЗОВАТЬ список strings в массив строк
    ВЕРНУТЬ полученный массив

ФУНКЦИЯ toIntegerArray(список integers):
    ПРЕОБРАЗОВАТЬ список integers в массив целых чисел
    ВЕРНУТЬ полученный массив

КОНЕЦ ПРОГРАММЫ
```

Более детализированный вариант:

```
АЛГОРИТМ:

1. Инициализация:
   - Создать ArrayList strings для хранения строк
   - Добавить строки: "Ты", "ж", "программист"
   - Создать ArrayList integers для хранения целых чисел
   - Добавить числа: 1000, 2000, 3000

2. Преобразование строкового списка:
   - Вызвать метод toStringArray(strings)
   - Внутри метода: преобразовать ArrayList<String> в String[]
   - Вернуть массив строк

3. Вывод строкового массива:
   - Для каждого элемента в stringArray:
        Вывести элемент на экран

4. Преобразование числового списка:
   - Вызвать метод toIntegerArray(integers)
   - Внутри метода: преобразовать ArrayList<Integer> в Integer[]
   - Вернуть массив чисел

5. Вывод числового массива:
   - Для каждого элемента в integerArray:
        Вывести элемент на экран
```

Ключевые операции:

· Collections.addAll() → добавление нескольких элементов в коллекцию
· list.toArray() → преобразование списка в массив
· String[]::new → ссылка на конструктор для создания массива нужного типа
