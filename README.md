# repository3
resizing array and populating with double the numbers in given array
#include<iostream>
using namespace std;
#define size 50
int resize(int[], int);
int main()
{
	cout << "enter size of array" << endl;
	int s;
	cin >> s;
	int array[size];
	cout << "enter array" << endl;
	for (int i = 0; i < s; i++)
	{
		cin >> array[i];
	}
	cout << "GIVEN ARRAY" << endl;
	for (int i = 0; i < s; i++)
	{
		cout<<  array[i];
	}
	cout << endl;
	resize(array, s);
}
//function
int resize(int arr[size], int x)
{
	int newarr[size] = { 0 };
	int newsize = x * 2;
	for (int i = 0; i < x; i++)
	{
		newarr[i] = arr[i];
	}
	/*for (int i = 0; i < newsize; i++)
	{
		cout << newarr[i] << "	";
	}*/
		int j = 0;
		for (int i = x; i < newsize; i++)
		{
			newarr[i] = arr[j] * 2;
			j++;
		}
	cout << "RESIZED ARRAY" << endl;
	for (int i = 0; i < newsize; i++)
	{
		cout << newarr[i] << "	";
	}
	return 0;
}
