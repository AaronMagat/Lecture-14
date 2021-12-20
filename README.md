# Lecture-14




#include <iostream>
#include <string>
#include <algorithm>
#include <exception>
#include <array>
#include <random>
using namespace std;

int main()
{
	int sum = 0;
	//initializing array with size of 10
	srand(7);
	array<int,1000> randomArry;
	for (int i = 0; i < 1000; i++)
	{
		//rand is use to generate a random variable
		//using % 10 to make sure number aren’t too big

		randomArry[i] = rand()%50;
		cout << randomArry[i] << ",";
		if (randomArry[i] == 6)
		sum++;
		}
	cout << "The number 6 appeared: " << sum << " times" << endl;
}
                                                              
                                                              
                                                              
                                                              
                                                              
                                                              
                                                              
                                                              
                                                              
 #include <iostream>
#include <array>
#include <algorithm>
#include <string>
using namespace std;

int main()
{
    int i;
    double x = 0, arr[10];
    cout << "Enter total number of elements(1 to 10): \n";
    // Store number entered by the user
    for (i = 0; i < 10; ++i)
    {
        cout << "Enter Number " << i + 1 << " : ";
        cin >> arr[i];

        while (cin.fail())
        {
            cout << "Incorrect command, kindly enter the number again ";
            cin.clear();
            cin.ignore(1000, '\n');
            cin >> arr[i];
        }
    }

    // Loop to store largest number to arr[0]
    x = arr[0];
    for (i = 0;i < 10; i++)
    {
        // Change < to > if you want to find the smallest element

        if (x > arr[i])
            x = arr[i];
    }
    cout << "Smallest element = " << x;

    return 0;
}
  
  
  
  
  
  
  #include <iostream>
#include <array>
#include <algorithm>
#include <string>
using namespace std;

int main()
{
    int i;
    double x=0,arr[10];
    cout << "Enter total number of elements(1 to 10): \n";
    // Store number entered by the user
    for (i = 0; i < 10; i++)
    {
        cout << "Enter Number " << i + 1 << " : ";
        cin >> arr[i];

        while (cin.fail())
        {
            cout << "Incorrect command, kindly enter the number again ";
            cin.clear();
            cin.ignore(1000, '\n');
            cin >> arr[i];
        }
    }

    // Loop to store largest number to arr[0]
    for (i = 0;i < 10; ++i)
    {
        // Change < to > if you want to find the smallest element

        if (x < arr[i])
            x = arr[i];
    }
    cout << "Largest element = " << x;

    return 0;
}
