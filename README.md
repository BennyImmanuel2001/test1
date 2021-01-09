using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace sscTechnologies
{
    class Program
    {
        static void Main(string[] args)
        {
            int rowsize = 2, colsize = 4;
            Random random = new Random();

            #region 2d array
            try
            {
                Console.WriteLine("Please enter the dimension for 2D array ");
                Console.WriteLine("Default is [2,4]");
                Console.WriteLine("Enter the Row size:");
                rowsize = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter the Column size:");
                colsize = Convert.ToInt32(Console.ReadLine());
                Console.Clear();
            }
            catch (Exception e)
            {
                Console.Clear();
                Console.WriteLine("Default value is assigned \"[2,4]\"");
                rowsize = 2;
                colsize = 4;
            }


            

            int[,] testarr = new int[rowsize, colsize];
           
         
            Console.WriteLine("\n2D Array\n");
            for (int i = 0; i < rowsize; i++)
            {
                for (int j = 0; j < colsize; j++)
                {
                    int val = random.Next(1, 10);
                    testarr[i, j] = val;
                    Console.Write($"index {i},{j}: {testarr[i, j]}\t");
                }
                Console.WriteLine();
            }
            Console.WriteLine();
            #endregion
