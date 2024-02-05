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