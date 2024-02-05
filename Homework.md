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