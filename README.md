//# LeapYear-Checker
#include<iostream>
using namespace std;
int main() {
	cout << "Student Name: Maryam Zulfiqar" << endl;
	cout << "Student ID: BC240207360" << endl;
	int studentID = 240207360;
	//droping two digits from right:
	int IDwithout_two_digits = studentID / 100;
	//extrat next four digits:
	int year = IDwithout_two_digits % 10000;
	if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
		cout << "The year " << year << " is a leapyear:" << endl;
	}
	else {
		cout << "The year " << year << " is not a leap year:" << endl;
	}
	int month;
	do {
		//input for month
		cout << "Enter the month (1-12), or -1 to stop: ";
		cin >> month;
		if (month == -1) {
			break; // Exit loop if user enters -1
		}
		if (month < 1 || month > 12) {
			cout << "Invalid month!" << endl;
			continue; // enter input again if month is invalid
		}
		//starting from the switch statment for the days of month
		int days;
		switch (month) {
		case 1:
			days = 31;
			cout << "Month " << month << " - january has " << days << " days " << endl;
			break;
		case 2:  // February
			if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
				days = 29;
				cout << "Month " << month << " - February has " << days << " days" << endl;
			}
			else {
				days = 28;
				cout << "Month " << month << " - February has " << days << " days" << endl;
			}
			break;
		case 3:
			days = 31;
			cout << "Month " << month << " - March has " << days << " days " << endl;
			break;
		case 4:
			days = 30;
			cout << "Month " << month << " - April has " << days << " days " << endl;
			break;
		case 5:
			days = 31;
			cout << "Month " << month << " - May has " << days << " days " << endl;
			break;
		case 6:
			days = 30;
			cout << "Month " << month << " -June has " << days << " days " << endl;
			break;
		case 7:
			days = 30;
			cout << "Month " << month << " - July has " << days << " days " << endl;
			break;
		case 8:
			days = 31;
			cout << "Month " << month << "_August has " << days << " days " << endl;
			break;
		case 9:
			days = 31;
			cout << "Month " << month << "_September has " << days << " days " << endl;
			break;
		case 10:
			days = 30;
			cout << "Month " << month << "_October has " << days << " days " << endl;
			break;
		case 11:
			days = 30;
			cout << "Month " << month << "_November has " << days << " days " << endl;
			break;
		case 12:
			days = 31;
			cout << "Month " << month << "_December has " << days << " days " << endl;
			break;
		default:
			cout << "Invalid month!" << endl;
		}
	} while (true);
	}
