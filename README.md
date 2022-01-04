# EpicBattle
using System;

namespace EpicBattleTARpv
{
    class Program
    {
        static void Main(string[] args)
        {
            string[] heroes = { "Chichenec", "Giant German", "Magicheskaya loshka", "Kirkorov" };
            string[] Enemies = { "Valodya", "Pyani Ilya", "Kitaiskaya Partiya", "Farting man", "Bomz","Ninja Teacher" };



            string RandomHero = GetRandomCharacter(heroes);
            string RandomEnemy = GetRandomCharacter(Enemies);
            string HeroWeapon = GetWeapon();
            string EnemyWeapon = GetWeapon();
            Console.WriteLine($"Your hero is {RandomHero}");
            Console.WriteLine($"He have {HeroWeapon}");
            Console.WriteLine($"Your enemy is {RandomEnemy}");
            Console.WriteLine($"He have {EnemyWeapon}");
        }
        public static string GetRandomCharacter(string[] someArray)
        {
            return someArray[GetRandomIndex(someArray)];
        }
        public static string GetWeapon()
        {
            string[] Weapon = { "Butilka Vodki", "Palka", "Yadernaya bomba", "Krisa na shampure", "Knife of Gods", "Vintovka mosina", "Nokia 3310", "Prosrochenoe moloko" };
            return Weapon[GetRandomIndex(Weapon)];
        }
        public static int GetRandomIndex(string[] someArray)
        {
            Random rnd = new Random();
            return rnd.Next(0, someArray.Length);
        }

    }
}
