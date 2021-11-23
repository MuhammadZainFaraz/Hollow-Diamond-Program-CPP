#include<iostream>
using namespace std;
void main()
{
	int row1, symb1 = 1;
	cout << "Enter Number Of Rows : ";
	cin >> row1;
	int row = row1;
	for (int a = (2*(row)-1); a > 0; a--)
	{
		if (a >= row)
		{
			for (int b = row1 - 1; b > 0; b--)
			{
					cout << " ";
			}
			for (int c = symb1; c > 0; c--)
			{
				if ((c == symb1) || (c == 1))
				{
					cout << "*";
				}
				else
				{
					cout << " ";
				}
			}
			symb1 += 2;
			row1 -= 1;
		}
		if (a < row)
		{
			symb1 -= 2;
			for (int d = row1 + 1; d > 0; d--)
			{
				cout << " ";
			}
			for (int e = symb1 - 2; e > 0; e--)
			{
				if (e == (symb1 - 2) || (e == 1))
				{
					cout << "*";
				}
				else
				{
					cout << " ";
				}
			}
			row1 += 1;
		}
		cout << endl;
	}
}
