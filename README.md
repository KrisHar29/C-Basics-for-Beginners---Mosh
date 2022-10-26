# C-Basics-for-Beginners---Mosh
Exercises from course.


using System;

namespace MoshFundamentals
{

    class Program
    {
        static void Main(string[] args)

        {

            // 1- Write a program and ask the user to enter a number. The number should be between 1 to 10. If the user enters a valid number, display "Valid" on the console. Otherwise, display "Invalid". (This logic is used a lot in applications where values entered into input boxes need to be validated.) 
          
            Console.WriteLine
                ("Enter a number between 1 and 10");
            var input1 = Console.ReadLine();
            int input2 = Convert.ToInt32(input1);

            if(input2 >= 1 && input2 <= 10 )
            {
                Console.WriteLine("Valid.");
                
            }
            else
            {
                Console.WriteLine("Invalid");
            }



            // 2- Write a program which takes two numbers from the console and displays the maximum of the two.

            Console.WriteLine("Enter 1 number");
            var inputNumber1 = Console.ReadLine();
            Console.WriteLine("Enter a 2nd number");
            var inputNumber2 = Console.ReadLine();
            int inputNumber1Parse = Convert.ToInt32(inputNumber1);
            int inputNumber2Parse = Convert.ToInt32(inputNumber2);
            int higherNumber = Math.Max(inputNumber1Parse, inputNumber2Parse);
            Console.WriteLine(higherNumber);

            // 3- Write a program and ask the user to enter the width and height of an image. Then tell if the image is landscape or portrait.

            Console.WriteLine("Input the width of the image.");
            var width = Console.ReadLine();
            Console.WriteLine("Input the height of the image.");
            var height = Console.ReadLine();
            int widthP = Convert.ToInt32(width);
            int heightP = Convert.ToInt32(height);
            if (heightP > widthP)
            {
                Console.WriteLine("Image is Landscape.");
            }
            else
            {
                Console.WriteLine("Image is Portrait.");
            }

            //4- Your job is to write a program for a speed camera. For simplicity, ignore the details such as camera, sensors, etc and focus purely on the logic. Write a program that asks the user to enter the speed limit. Once set, the program asks for the speed of a car. If the user enters a value less than the speed limit, program should display Ok on the console. If the value is above the speed limit, the program should calculate the number of demerit points. For every 5km/hr above the speed limit, 1 demerit points should be incurred and displayed on the console. If the number of demerit points is above 12, the program should display License Suspended.

            Console.WriteLine("Enter the speed limit.");
            var speedLimit = Console.ReadLine();
            int SpeedLimit = Convert.ToInt32(speedLimit);
            Console.WriteLine("What is the speed of the car");
            var speed = Console.ReadLine();
            int Speed = Convert.ToInt32(speed);
            int demerit = Speed - SpeedLimit / 5;

            if (SpeedLimit > Speed)
            {
                Console.WriteLine("Speed is OK.");
            }
            if (demerit < 12)
            {
                Console.WriteLine("Total demerits = " + demerit);
            }
            else
            {
                Console.WriteLine("License suspended");
            }

        }




    }
}
