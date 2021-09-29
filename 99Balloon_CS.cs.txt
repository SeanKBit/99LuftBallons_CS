using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace NinetyNineLuftBalloons
{
    class Balloon
    {
        private int intX, intY;
        
        public Balloon()
        {
            Random rand = new Random();
            intX = rand.Next(0, 56);
            intY = rand.Next(0, 33);
        }

        public void show()
        {
            Console.SetCursorPosition(intX, intY);
            Console.WriteLine("----");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 1);
            Console.WriteLine("|  |");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 2);
            Console.WriteLine("|  |");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 3);
            Console.WriteLine("----");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 4);
            Console.WriteLine("  | ");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 5);
            Console.WriteLine(" |  ");
            System.Threading.Thread.Sleep(100);
            Console.SetCursorPosition(intX, intY + 6);
            Console.WriteLine(" |  ");
        }
    }
}
