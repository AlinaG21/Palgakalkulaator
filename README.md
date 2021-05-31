# Palgakalkulaator
    using System;

    namespace Kalkulaator
    {
    class Program
    {

        
        static void Main(string[] args)
       
        {
            int BrutoSalary = 0;

            Console.WriteLine("Enter Bruto Salary");
            BrutoSalary = Convert.ToInt32(Console.ReadLine());

            if (BrutoSalary <= 1200 && BrutoSalary >= 500)
            {
                Calculation1(BrutoSalary);
            }

            if (BrutoSalary <= 2099 && BrutoSalary >= 1201)
            {
                Calculation2(BrutoSalary);
            }

            if (  BrutoSalary >= 2100)
            {
                Calculation3(BrutoSalary);
            }

        }

        static void Calculation1(double BrutoSalary)
        {
            double pensionFond = BrutoSalary * 0.02;
            double Insurance = BrutoSalary * 0.016;
            double Tax = (BrutoSalary - 500 - pensionFond - Insurance) * 0.2;
            double Calculation1 = BrutoSalary - pensionFond - Insurance - Tax;

            Console.WriteLine("Your Neto Salary is = "+ Calculation1);
        }

        static void Calculation2(double BrutoSalary)

        {
            double pensionFond = BrutoSalary * 0.02;
            double Insurance = BrutoSalary * 0.016;
            double TaxFreeInCome = 500 - 0.55556 * (BrutoSalary - 1200);
                double Tax = (BrutoSalary - pensionFond - Insurance - TaxFreeInCome) * 0.2;
            double Calculation2 = BrutoSalary - pensionFond - Insurance - Tax;
            Console.WriteLine("Your Neto Salary is = " + Calculation2);
        }
        static void Calculation3(double BrutoSalary)
        {

            double pensionFond = BrutoSalary * 0.02;
            double Insurance = BrutoSalary * 0.016;
            double Tax = BrutoSalary * 0.2;
            double Calculation3 = BrutoSalary - pensionFond - Insurance - Tax;
                Console.WriteLine("Your Neto Salary is = " + Calculation3);
        }
    }
}
