# Draw-a-Square
using System;

namespace _030621
{
    class Program
    {
        static void Main()
        {

            int i, j, s; //s is a side of square which need to scan
            char c; //c is character which need to scan

            Console.WriteLine("Enter a symbol: ");//(*,/,-,+,.,?,…)
            c = char.Parse(Console.ReadLine());
            Console.WriteLine("Enter a side of a square:  ");
            s = int.Parse(Console.ReadLine());

                for (i = 1; i <= s; i++)
                {
                    for (j = 1; j <= s; j++)
                    {
                        if (i == 1 || i == s || j == 1 || j == s || j == (s + 1) / 2 && i <= (3*s + 3) / 4 && i >= (s + 3) / 4
                            || i == (s + 1) / 2 && j >= (s + 3) / 4 && j <= (3*s + 3) / 4)
                            Console.Write("{0} ", c);
                        else
                            Console.Write("  ");
                    }
                    Console.Write("\n");
                }
                Console.ReadKey();
        }
    }
}

