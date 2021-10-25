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
            cin.ignore(1000, '\n'); //1000 is the limit
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
        } while (password != userInput); //while the inputted password is not equal to the password

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

        while (password != userInput) { //while the inputted password is not equal to the password "1234password"
            cout << "Enter your password: " << endl; //it will show this same character output again
            cin >> userInput; //character input
        }
        cout << "\nWelcome to the super secure banking area" << endl;
    }
    
