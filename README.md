# Lecture-13
// Lecture 13.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
using namespace std;
int main()
{
	cout << "This prints Range Based For Loop:\n";
	string courses[] = { "BSU CC", "BSU BA", "HNC CC", "HND" };
	for (int i = 0; i < 4; i++) {
		cout << courses[i] << endl;
	}
	for (auto course : courses) {//range based for loop
		cout << course << endl;
	}
	cout << "This prints Auto Keyword:\n";
	{
		char letters[] = { 'C', 'o', 'd', 'e', 'L', 'a', 'b\n' };
		for (auto letter : letters) {
			cout << letter;
		}
	}
	cout << "This prints the exercise for Lecture 13:\n";
	{
		int num[5];

		cout << "Welcome, please enter 5 digits:\n";
		for (int i = 0; i < 5; i++) {
			cin >> num[i];

			while (cin.fail() || num[i] > 100) {
				cout << "Invalid input." << endl;
				cin.clear();
				cin.ignore(123, '\n');
				cin >> num[i];
			}
		}

		for (auto num : num) {
			cout << endl;
			cout << num << endl;
		}
	}
	cout << "Thsi code will print 2D Array Initialisation:\n";
	{
		string snacks[3][4] = {
			{"Galaxy silk", "Mars Bar", "Snickers", "Bounty"},
			{"Flavoured Youghurt", "Oman chips", "Oreo", "Lays"},
			{"Apple", "Banana", "Orange", "Pear"}
		};
		for (int i = 0; i < 3; i++) {
			for (int j = 0; j < 4; j++) {
				cout << snacks[i][j] << " ";
			}
			cout << endl;
		}
	}
	cout << "This code will print Array Art:\n";
	cout << "-----\n";
	cout << "-O-O-\n";
	cout << "-@@@-\n";
	cout << "-^^^-\n";
	cout << "-vvv-\n";
}

// Run program: Ctrl + F5 or Debug > Start Without Debugging menu
// Debug program: F5 or Debug > Start Debugging menu

// Tips for Getting Started: 
//   1. Use the Solution Explorer window to add/manage files
//   2. Use the Team Explorer window to connect to source control
//   3. Use the Output window to see build output and other messages
//   4. Use the Error List window to view errors
//   5. Go to Project > Add New Item to create new code files, or Project > Add Existing Item to add existing code files to the project
//   6. In the future, to open this project again, go to File > Open > Project and select the .sln file
