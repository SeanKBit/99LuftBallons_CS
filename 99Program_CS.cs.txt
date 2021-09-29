using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NinetyNineLuftBalloons
{
    class Program : Balloon
    {
        static void Main(string[] args)
        {
            Console.SetWindowSize(60, 40);

            for (int i = 0; i < 100; i++)
            {
                Console.SetCursorPosition(22, 1);
                Console.WriteLine($"{i} LUFTBALLOONS!");
                System.Threading.Thread.Sleep(500);

                // Create new Balloon object
                Balloon bImage = new Balloon();
                bImage.show();

                if (is99(i)) // If 99 balloons, celebrate...
                {
                    for (int count = 0; count < 5; count++)
                    {
                        System.Threading.Thread.Sleep(500);
                        Console.SetCursorPosition(22, 10);
                        Console.WriteLine("########  ########  #");
                        Console.SetCursorPosition(22, 11);
                        Console.WriteLine("#      #  #      #  #");
                        Console.SetCursorPosition(22, 12);
                        Console.WriteLine("#      #  #      #  #");
                        Console.SetCursorPosition(22, 13);
                        Console.WriteLine("#      #  #      #  #");
                        Console.SetCursorPosition(22, 14);
                        Console.WriteLine("#      #  #      #  #");
                        Console.SetCursorPosition(22, 15);
                        Console.WriteLine("#      #  #      #  #");
                        Console.SetCursorPosition(22, 16);
                        Console.WriteLine("########  ########  #");
                        Console.SetCursorPosition(22, 17);
                        Console.WriteLine("       #         #  #");
                        Console.SetCursorPosition(22, 18);
                        Console.WriteLine("       #         #  #");
                        Console.SetCursorPosition(22, 19);
                        Console.WriteLine("       #         #");
                        Console.SetCursorPosition(22, 20);
                        Console.WriteLine("       #         #  #");
                        Console.SetCursorPosition(22, 21);
                        Console.WriteLine("########  ########  #");
                        System.Threading.Thread.Sleep(500);
                        Console.Clear();
                    }       
                }  
            }
            createPascalsTriangle();


            //Expression-bodied method example
            bool is99(int n) => n == 99;


            // Pascal's Triangle algorithm just because it is often part of coding tests
            void createPascalsTriangle()
            {
                int rows = 10;
                int val = 1;
                int blank, x, y;
                int curX = 12, curY = 10;
                Console.SetCursorPosition(curX, curY);

                for (x = 0; x < rows; x++)
                {
                    for (blank = 1; blank <= rows - 1; blank++)
                    {
                        Console.Write(" ");
                    }
                    for (y = 0; y <= x; y++)
                    {
                        if (y == 0 || x == 0)
                        {
                            val = 1;
                        }
                        else
                        {
                            val = val * (x - y + 1) / y;
                        }
                        Console.Write(val + " ");
                    }
                    curY++;
                    Console.SetCursorPosition(curX, curY);
                    System.Threading.Thread.Sleep(300);
                }
            }
        }
    }
}
