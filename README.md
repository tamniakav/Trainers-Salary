using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_4
{
    class Program
    {
        static void Main(string[] args)
        {
            int lectures = int.Parse(Console.ReadLine());
            double budget = double.Parse(Console.ReadLine());

            double Jelev = 0;
            double RoYaL = 0;
            double Roli = 0;
            double Trofon = 0;
            double Sino = 0;
            double Others = 0;

            for (int i = 0; i < lectures; i++)
            {
                string names = Console.ReadLine();

                if (names == "Jelev")
                {
                    Jelev++;
                }
                else if (names == "RoYaL")
                {
                    RoYaL++;
                }
                else if (names == "Roli")
                {
                    Roli++;
                }
                else if (names == "Trofon")
                {
                    Trofon++;
                }
                else if (names == "Sino")
                {
                    Sino++;
                }
                else
                {
                    Others++;
                }
            }
            double paySlip = budget / lectures;

            Console.WriteLine("Jelev salary: {0:f2} lv", paySlip * Jelev);
            Console.WriteLine("RoYaL salary: {0:f2} lv", paySlip * RoYaL);
            Console.WriteLine("Roli salary: {0:f2} lv", paySlip * Roli);
            Console.WriteLine("Trofon salary: {0:f2} lv", paySlip * Trofon);
            Console.WriteLine("Sino salary: {0:f2} lv", paySlip * Sino);
            Console.WriteLine("Others salary: {0:f2} lv", paySlip * Others);
        }
    }
}

