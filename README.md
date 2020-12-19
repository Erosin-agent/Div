# Div
project
//fun game test
using System;

namespace Rolling_a_dice
{
    class Program
    {
        static void Main(string[] args)
        {

            Random cardDraw = new Random();
            int cards = 0;
            int count = 0;

            Console.WriteLine("This is a game where 2 players try their luck.");
            Console.WriteLine("The game is won by the person who took less tries to roll a 7.");

            while (cards != 7)
            {
                if (count > 10)
                {
                    Console.WriteLine("It took you more than 10 tries.");
                    
                    return;
                    
                }
                else
                {
                    Console.ReadKey();
                    cards = cardDraw.Next(0, 20);
                    Console.WriteLine(cards);
                    
                }
                count++;
            }
            Console.WriteLine("Congratulations! You've won !");
            Console.WriteLine("It took you " + count + " tries to make it.");


        }


    }
}
