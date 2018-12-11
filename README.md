//perimeter
#include <iostream>
#include<string>
#include <iomanip>
#include <cstdlib>
#include <ctime>

using namespace std;
const int mbili = 2;
int getPerimeter(int length, int width)
{
	int perimeter = pow(length, mbili) + pow(width, mbili);
	return perimeter;

}



int main()
{
	
	int length = 0;
	int width = 0;
	do
	{
		cout << "Please enter the length of your perimeter " << endl;
		cin >> length;
		if (cin.fail()||length <= 0 )
		{
			cout << "Invalid, please input the length again" << endl;
			cin.clear();
			cin.ignore(INT_MAX, '\n');
			//cin >> length;
			
		}

	} while (length < 0);
	do
	{
		cout << "Please enter the width of your recangle" << endl;
		cin >> width;
		if (cin.fail() || width <= 0)
		{
			cout << "Invalid, please input the width again" << endl;
			cin.clear();
			cin.ignore(INT_MAX, '\n');
			cin >> width;

		}

	} while (width < 0);
	cout << "The perimeter of the rectangle is " << getPerimeter(length, width) << endl;
	

	

	
	system("PAUSE");
	return 0;
}
