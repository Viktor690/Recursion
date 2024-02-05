// Задача 1. Задайте значения M и N.
// Напишите программу, которая выведет все натуральные числа
// в промежутке от M до N. Использовать рекурсию, не использовать циклы.
// Console.WriteLine("Введите 2 числа:");
// int m = Convert.ToInt32(Console.ReadLine());
// int n = Convert.ToInt32(Console.ReadLine());
int m = 9;
int n = 15;
void PrintNumbersMN(int start, int end)
{
    if (end > start)
    {
        PrintNumbersMN(start,end-1);
    }
    Console.WriteLine(end);
}

if (m < n)
{
    PrintNumbersMN(m+1,n-1);
}
else
{
    PrintNumbersMN(n+1,m-1);
}



Задача 2: Напишите программу вычисления функции Аккермана с помощью рекурсии.  Даны два неотрицательных числа m и n.
int CalcAkkerman(int m, int n)
{
    if (m == 0)
    {
        return n + 1;
    }        
    else
    {
        if ((m != 0) && (n == 0))
        {
            return CalcAkkerman(m - 1, 1);
        }
        else
        {
            return CalcAkkerman(m - 1, CalcAkkerman(m, n - 1));
        }
    }
} 
Console.WriteLine(CalcAkkerman(3, 2)); //29



Задача 3: Задайте произвольный массив. Выведете его элементы, начиная с конца. Использовать рекурсию, не использовать циклы.
void PrintReverseNumbers(int[] array, int low, int high)
{
    // low индекс первого элемента массива
    // high индекс последнего элемента массива
    if (low < high)
    {
        int temp = array[low];
        array[low] = array[high];
        array[high] = temp;
        PrintReverseNumbers(array, low + 1, high - 1);
    }
}
int[] array = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
int size = array.Length;
PrintReverseNumbers(array, 0, size - 1);
int[] result = array;
Console.WriteLine($"Результат: [ {string.Join(", ", result)} ]");