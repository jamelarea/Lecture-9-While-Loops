Lecture 9 While & do-while Loops

SLIDE 13, Remain Positive
    #include <iostream>
    #include <string>
    using namespace std;

    int main()
    {
        //variable
        float myNum = 20; //starts with 20

        while (myNum >= 0) { //positive number
            cout << myNum << endl; 
            myNum = myNum -0.5; //it will count by decreasing 0.5
        }

        return 0;
    }

EXERCISE BREAK
    
SLIDE 20, Reverse 9 times table

    #include <iostream>
    using namespace std;

    int main()
    {
        int num = 108; //declare and initialise variable

        while (num > 0) { //while conditional check
            //code to output then decrease number
            cout << num << endl;
            num -= 9;
        }
        cin.get(); //keeps console window open in Visual Studio
        return 0;
    }

SLIDE 21, The Pointless Box
   
    #include <iostream>
    using namespace std;

    int main()
    {
        int num = 1 || 2; //integer is equals to 1 or 2

        cout << "Enter a number between 1 and 2: "; cin >> num;

        while (num > 0)
        {
            if (num == 1)
            {
                cout << "\nYou have entered the number 1" << endl;
                cout << "Enter a number between 1 and 2: "; cin >> num;
            }
            if (num == 2)
            {
                cout << "\nYou have entered the number 2" << endl;
                cout << "Enter a number between 1 and 2: "; cin >> num;
            }
            else
            {
                break;
            }
        }
            cout << "\nIncorrect input." << endl;
            cin.get(); //keeps console window open in Visual Studio
            return 0;
        }

SLIDE 22, Input Improvement

    #include <iostream>
    using namespace std;

    int main()
    {
        //variable
        char input;

        do { //'do' will execute the code block once, before checking if the condition is true
            cout << "Would you like to quit (Y/N)? "; //character output
            cin >> input; //character input

        } while ((input != 'Y') && (input != 'y')); //while conditional check
        //loop will stop when user inputs Y
        return 0;
    }

Lecture 9 While do while Loops - exercises
    
SLIDE 2, Brute-Force Attack
    
    #include <iostream>
    using namespace std;

    int main()
    {
        string password = "246";
        string userInput;

        while (userInput != password)
        {
            cout << "Enter the pass code for the safe" << endl;
            cin >> userInput;

        }
        //to print the ran out of message only if the password was not found within 5 attempts
        cout << "You found the code";
        return 0;
    }
    
SLIDE 3, Bruce-Force Attack II
    
    #include <iostream>
    using namespace std;

    int main()
    {
        string password = "246";
        string userInput;
        int x = 5;
        cout << "You will only have 5 attempts" << endl;


        while (x > 0)
        {
            cout << "Enter the pass code for the safe" << endl;
            cin >> userInput;
            if (userInput == password)
            {
                cout << "You have finally unlocked the safe" << endl;

                break;
            }
            else
                x--;
        }
        //to print the ran out of message only if the password was not found within 5 attempts
        if (x == 0)
        {
            cout << "You ran out of attempts" << endl;
        }
        return 0;
    }

SLIDE 4, Input Improvement
    
    #include <iostream>
    using namespace std;
    int main() {

    char input; 
    do
    {
        cout << "Would you like to Quit (Y/N)?" <<
            endl;
        cin >> input;
    } 
    while ((input != 'Y') && (input != 'y'));

    return 0;
    }
    
SLIDE 5, Loopy
    
    #include <iostream>  
    using namespace std;

    int main()
    {
        int myInt = 0, counter;

        cout << "Enter a number\n";
        cin >> counter;

        do
        {
            cout << myInt << endl;
            myInt++;

        } while (myInt <= counter);

        return 0;
    }

    
    
