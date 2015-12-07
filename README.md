# Objects

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace GenericListOfObjects
{
    class Book
    {
        public string Title { get; set; }
        public string Author { get; set; }
        public string ISBN { get; set; }

        public void Print()
        {
            Console.WriteLine("\"{0}\", {1}, (ISBN: {2}))", Title, Author, ISBN);
        }
    }
}

namespace GenericListOfObjects
{
    class Automobile
    {
        public string Make { get; set; }
        public string Model { get; set; }
        public int Year { get; set; }
        public int Miles { get; set; }
        public string ExteriorColor { get; set; }

        public void Print()
        {
            Console.WriteLine("{0} {1} {2} with {3} exterior (Odometer: {4})", Year, Make, Model, ExteriorColor, Miles);
        }
    }
}

namespace GenericListOfObjects
{
    class Program
    {
        static void Main(string[] args)
        {
            List<Automobile> inventory = new List<Automobile>();

            Automobile a1 = new Automobile();
            a1.Make = "Dodge";
            a1.Model = "Dart";
            a1.Year = 1976;
            a1.ExteriorColor = "Green";
            a1.Miles = 111001;

            Automobile a2 = new Automobile();
            a2.Make = "Oldsmobile";
            a2.Model = "Cutlas Supreme";
            a2.Year = 1985;
            a2.ExteriorColor = "Silver";
            a2.Miles = 75001;

            Automobile a3 = new Automobile();
            a3.Make = "Geo";
            a3.Model = "Prism";
            a3.Year = 1992;
            a3.ExteriorColor = "Green";
            a3.Miles = 154001;

            Automobile a4 = new Automobile();
            a4.Make = "Nissan";
            a4.Model = "Altima";
            a4.Year = 2000;
            a4.ExteriorColor = "Black";
            a4.Miles = 105001;

            Automobile a5 = new Automobile();
            a5.Make = "BMW";
            a5.Model = "745Li";
            a5.Year = 2005;
            a5.ExteriorColor = "Black";
            a5.Miles = 70001;

            inventory.Add(a1);
            inventory.Add(a2);
            inventory.Add(a3);
            inventory.Add(a4);
            inventory.Add(a5);

            Console.WriteLine("We have the following items in inventory: ");
            foreach (Automobile item in inventory)
            {
                item.Print();
            }

            Console.WriteLine("");
            Console.WriteLine("Our oldest car was built in {0}.", inventory[0].Year);

            Console.ReadLine();

            Book b1 = new Book();
            b1.Author = "Robert Adams";
            b1.Title = "Microsoft .NET XML Web Services";
            b1.ISBN = "0-000-00000-0";

            //inventory.Add(b1);
        }
    }
}
