using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace script_combining_stuff_I_ve_learned_so_far_8oct
{
    class Program
    {
        static void Main(string[] args)
        {


            bool mainloop = true;
            while (mainloop)
            {
                //this program was made by me to combine everything I had learned after 3 days of a programing course on oct 8. -PJ
                //this program is meant to emulate the kind of personal info input websites usually asks for when making an account,name, age and gender, while also making sure it doesn't crash or get the wrong input. -PJ


                Console.WriteLine("Hello, whats your name?");

                string name = Console.ReadLine(); //users name

                Console.WriteLine(value: "Hey " + name + " how old are you?");
                int trueage = 0; //set a value to this int so I can load it later outside of the code
                bool ageloop = true;
                while (ageloop) //loop until the user input a valid age
    
                {

                    int age;

                    string ageStr = Console.ReadLine();

                    //trueage = age;

                    int.TryParse(ageStr, out age); //failed tryparse always results in 0

                    //int age = Convert.ToInt32(ageStr); //crashes if anything but a number is entered


                    //trueage = age;
                    trueage = age;


                    if (trueage > 30)
                    {
                        Console.WriteLine(age + "? Really? you look so much younger than that.");
                        ageloop = false;
                    }
                    else if (30 >= trueage && trueage > 0)
                    {
                        Console.WriteLine(trueage + "? Really? you look older than that.");
                        ageloop = false;
                    }
                    else if (trueage == 0)
                    {
                        Console.WriteLine("Only use whole positive numbers above 0 please.");
                       
                    }

                    else
                    {
                        Console.WriteLine("Only use whole positive numbers please.");
                    }

                }

                Console.WriteLine("Lastly, what are your prefered pronouns?");

                string pronoune = ("They / them"); //define this string here so I can load it outside of the loop

                bool genderloop = true;
                while (genderloop) //loop until user confirms that it's correct
                {
                    Console.WriteLine("1. He/him");
                    Console.WriteLine("2. She/her");
                    Console.WriteLine("3. They/them");

                    string genderStr = Console.ReadLine();

                    //int gender = Convert.ToInt32(genderStr); //crashes if you press enter or unicode
                    int gender;

                    int.TryParse(genderStr, out gender);

                    if (gender == 1)
                    {
                        Console.WriteLine("Is He/him correct?");
                        Console.WriteLine("Y/N");

                        String awnserStr = Console.ReadLine();

                        char response = Convert.ToChar(awnserStr);

                        if (response == 'Y' || response == 'y')
                        {
                            genderloop = false;
                        }
                        else if (response == 'N' || response == 'n') //loops back to the gender options
                        {


                        }
                        else
                        {
                            Console.WriteLine("use only Y or N please."); //incase the user doesn't press the correct input
                            Console.ReadKey();
                        }
                    }
                    else if (gender == 2)
                    {

                        Console.WriteLine("Is she/her correct?");
                        Console.WriteLine("Y/N");

                        String awnserStr = Console.ReadLine();

                        char response = Convert.ToChar(awnserStr);

                        if (response == 'Y' || response == 'y')
                        {
                            genderloop = false;
                        }
                        else if (response == 'N' || response == 'n') //loops back to the gender options
                        {

                        }
                        else
                        {
                            Console.WriteLine("use only Y or N please."); //incase the user doesn't press the correct input
                            Console.ReadKey();
                        }
                    }
                    else if (gender == 3)
                    {

                        Console.WriteLine("Is They/Them correct?");
                        Console.WriteLine("Y/N");

                        String awnserStr = Console.ReadLine();

                        char response = Convert.ToChar(awnserStr);

                        if (response == 'Y' || response == 'y')
                        {
                            genderloop = false;
                        }
                        else if (response == 'N' || response == 'n') //loops back to the gender options
                        {

                        }
                        else
                        {
                            Console.WriteLine("use only Y or N please."); //incase the user doesn't press the correct input
                            Console.ReadKey();
                        }
                    }
                    else
                    {
                        Console.WriteLine("Please only use 1,2 or 3");
                    }

                }//genderloop

                Console.WriteLine("So your name is " + name + ", you're " + trueage + " years old and your pronounes are " + pronoune + ".");
                Console.WriteLine("Is this correct?");
                bool finalloop = true;
                while (finalloop)
                {
                
                Console.WriteLine("Y/N");

                    string finalresponseStr = Console.ReadLine();

                    //char finalresponse = Convert.ToChar(finalresponseStr);

                    char finalresponse;

                    char.TryParse(finalresponseStr, out finalresponse);

                if (finalresponse == 'y' || finalresponse == 'Y') 
                        {
                        Console.WriteLine("Thank you " + name + " for using my program! - PJ");
                        finalloop = false;
                        mainloop = false;
                        }

                else if (finalresponse == 'n'||finalresponse == 'N')
                {
                        //mainloop = true;
                        finalloop = false;
                        //mainloop = true;
                    }

                else
                {
                    Console.WriteLine("Please only use Y or N");
                        //Console.ReadKey();
                }
                }
                


            }//mainloop while

            Console.ReadKey();




        }//main
    }//program
}//program
