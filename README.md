# s1_MarloweTadiliJr

#include <iostream>
#include <string>
using namespace std;
int main() {
		
	string User;
	int age, subject[2],result,resultSwitch;
	int count = 0;
	int total = 0;
	cout << "Enter full Name: ";
	getline(cin, User);
	cout << "\nEnter Age: "; cin >> age;
	if (cin.fail()) {
		cin.clear();
		system("cls");
		cout << "ERROR";
	}
	while (count < 2) {
		cout << "\n(0-100)Enter Two Subjects Grades: ";
		cin >> subject[count];
		if (cin.fail()) {
			cin.clear();
			system("cls");
			cout << "ERROR";
		}
		else if (subject[count] >= 0 && subject[count] <= 100) {
		total += subject[count];
		count++;
		}
		else {
			system("cls");
			cout << "ERROR";
		}
	}
	result = total / 2;
	resultSwitch = result / 10;
	system("cls");
	cout << "Name: " << User << endl;
	cout << "Age: " << age << endl;
	cout << "Average Grade: " << result << endl;
	switch (resultSwitch) {
	default:
		system("cls");
		cout << "ERROR";
		break;
	case 1:
	case 2:
	case 3: {
		cout << "Mark: F" << endl;
			break;
	}case 4: {
		cout << "Mark: D" << endl;
		break;
	}case 5: {
		cout << "Mark: C" << endl;
		break;
	}case 6: {
		cout << "Mark: B" << endl;
		break;
	}
	case 7:
	case 8:
	case 9:
	case 10: {
		cout << "Mark: A" << endl;
		break;
	}


	}

	return 0;
}

