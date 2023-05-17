#include <iostream>
#include <string>
using namespace std;

class Car
{
	private:
		int year;
		string customer;
		int speed;

	public:
		   Car(int y,string model)
		{
			customer = model;
			year = y;
			speed = 0;
		}
		string getCustomer()
		{
			return customer;
		}
		int getYear()
		{
			return year;
		}
		int getSpeed()
		{
			return speed;
		}
		int accelerate()
		{
			return speed += 10;
		}
		int carBreak()
		{
			return speed -= 10;
		}
};


int main()
{
	string customer;
	int year;

	cout << "What year is your car? ";
	cin >> customer;

	cout << "What is your car model? ";
	cin >> year;


	// Class objects
	Car BMW(2005, "Explorer"), honda(year, customer);


	// honda object
	cout << endl << "honda information" << endl;
	for (int x = 1; x <= 5; x++)
	{
		cout << honda.accelerate() << endl;
	}
	cout << "Your speed is " << honda.getSpeed() << " for the car model of " << honda.getYear() << endl;
	for (int x = 1; x <= 5; x++)
	{
		honda.carBreak();
	}
	cout << "You stopped the car with a speed of " << honda.getSpeed() << endl;


	//BMW object
	cout << endl << "BMW information" << endl;
	cout << BMW.getCustomer() << endl;
	cout << BMW.getYear() << endl;
	for (int x = 1; x <= 20; x++)
	{
		BMW.accelerate();
	}
	cout << "Your speed for the BMW is " << BMW.getSpeed() << endl;


	return 0;
}
