# Lecture-9-While-Loops

SLIDE 8, While Loop Example

    #include <iostream>
    using namespace std;

    int main()
    {
        int count = 1; //variable

        //while loop is used to iterate a part of the program several times
        while (count <= 1000) { //less than or equal to 1000
            cout << count << endl; 
            count++; //program will count less than or equal to 1000 by 1
        }
    }
    
SLIDE 10, Break Example
    
    #include <iostream>
    using namespace std;

    int main()
    {
        cout << "Enter a whole number: " << //character output
            endl; int userNum; //variable
        cin >> userNum; //character input

        int count = 1;
        while (true) {
            cout << count << endl;
            if (count == userNum) {
                break;
            }
            count++; //it will count until the whole number that is inputted
        }
    }

SLIDE 11, Alternative to Previous Break Solution

    #include <iostream>
    using namespace std;
    
    int main()
    {
        cout << "Enter a whole number: " << endl;
        int userNum;
        cin >> userNum;

        int count = 1; //count by 1
        while (count <= userNum) {
            cout << count << endl;
            count++; //it will count until the whole number that is inputted
        }
    }
    
SLIDE 12, While Loop Error Check Example
  
    #include <iostream>
    using namespace std;

    int main()
    {
        cout << "Enter your age: " << endl;
        int age; //variable
        cin >> age;
        while (cin.fail()) {
            cout << "Invalid input.\nPlease enter a valid age:" << endl;
            cin.clear();
            cin.ignore(1000, '\n'); //its going to ignore the string of characters 1000 times then next line
            cin >> age;
        }
        cout << "Your age is: " << age;
    }
    
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
    
DO WHILE LOOPS

SLIDE 17, Login Do While Example

    #include <iostream>
    #include <string>
    using namespace std;
    
    int main()
    {
        //variables
        string password = "1234password";
        string userInput;

        do { //'do' will execute the code block once, before checking if the condition is true
            //then it will repeat the loop as long as the condition is true
            cout << "Enter your Password: ";
            cin >> userInput;
        } while (password != userInput); //userInput does not have the same value

        cout << "\nWelcome to the super secure banking area" << endl;
    }
    
SLIDE 18, Login While Alternative

    #include <iostream>
    #include <string>
    using namespace std;
    
    int main()
    {
        //variables
        string password = "1234password";
        string userInput;

        cout << "Enter your password: " << endl;
        cin >> userInput;

        while (password != userInput) { //userInput does not have the same value
            cout << "Enter your password: " << endl; //it will show this same character output again
            cin >> userInput; //character input
        }
        cout << "\nWelcome to the super secure banking area" << endl;
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
        //variables
        int num = 1 || 2; //integer is equals to 1 or 2

        cout << "Enter a number between 1 and 2: "; cin >> num;

        while (num > 0) //while conditional check
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
