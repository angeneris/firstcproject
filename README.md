Thanks @Jabrils for making this great tutorial on Youtube to follow along. This was my first C# project, first day coding in the language and everything was coded alongside the tutorial by @Jabrils. The only code I truly copied and pasted was the first few lines and to be honest I'm still figuring out what those first few lines mean- help me out if it's something painfully obvious. 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace FirstCproject
{
    class Program
    {
        static void Main(String[] arg)
        {
            //initialize variables
            string user, USA, looking, trees, feet, earthquake, scared, axe, punk, workout;
            string[] insult = new string[3];
            //Get user input

            Console.WriteLine("Welcome, user! ");
            Console.WriteLine("Let's play a game of Mad Libs!");
            Console.WriteLine("What's your name? Please enter it below");

            user = Console.ReadLine();

            Console.WriteLine($"Hello {user}, are you ready for this adventure?"+" Where do you want to be transported to?");
            USA= Console.ReadLine();
         
            Console.WriteLine($"Okay, so you want to be transported to {USA}?" + " Interesting choice...");
            Console.WriteLine($"Let's go to {USA}, then");
            //new input
            Console.WriteLine("Now, give me a verb to represent what you'll be doing in this new place (in present tense)");
            looking = Console.ReadLine();
            //new input
            Console.WriteLine($"You get it... I'd be {looking} too! Now this time I want you to guess this next word correctly. " +
            $"What's something you have two of in your body?");
            feet = Console.ReadLine();
            Console.WriteLine($"Haha, yup, you do have two {feet}");
            //New input
            Console.WriteLine($"Give me a plural noun- name anything in the world you might SEE (plural)");
            trees = Console.ReadLine();

            //new input
            Console.WriteLine($"Now I need a noun for something loud that makes things rumble");
            earthquake = Console.ReadLine();
            //new input
            Console.WriteLine($"Alright, sorry but now I need a verb to describe how you feel in your nightmares :( ");
            scared = Console.ReadLine();
            //new input
            Console.WriteLine($"So if you're going to be {scared}, then what will you use to fight your demons?");
            axe = Console.ReadLine();
            Console.WriteLine($"Great weapon choice...Now I need 3 insults you wouldn't expect someone to use on you");

      
                for(int i=0;i < insult.Length;i++)
            {
                Console.WriteLine($"Insult { i+1} / {insult.Length}");
                insult[i]= Console.ReadLine();

            }
            Console.WriteLine($"Wow, do you kiss your mother with that mouth?!...JK...Last thing! What's an activity you know you should do more of?");
            workout =Console.ReadLine();

            Console.WriteLine($"Thanks for participating :) Here is your mad lib. Hope you like it!");

            //Initialize story

            string madlibstory =
            $"The other day I had a dream that I was in a very strange place in {USA}. " +
            $"I was {looking} around and all I could see were {trees}. Then, I heard a sound." +
            $"I saw two big {feet} coming my way. The ground was shaking like a big {earthquake}." +
            $"I was so {scared} that I called my mom and she told me that it's going to be okay" +
            $"I'm not ashamed that I had to call my mom at the fine age of 25." +
            $"My mom even said she'd be right there and right before my eyes she appeared. " +
            $"I was stunned, she came blazing though with a big {axe} in hand and armor to save the day." +
            $"Then she told me I should really learn to stop being such a {insult[0]},{insult[1]},and a {insult[2]} and flew away." +
            $"Offended yet relieved, I woke up feeling like I should take her advice and go {workout}.";

            //Print story

            Console.WriteLine(madlibstory);
            Console.ReadKey();  
        }
    }
}
