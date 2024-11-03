# krish
This is my first GIT Repository
This is the demo.


#include <iostream>
#include <iomanip>
#include <cmath>
using namespace std;
class calculator
{
    double a, b;

public:
    void set_data(double x, double y)
    {
        a = x;
        b = y;
    }
    double sum(double, double)
    {
        return (a + b);
    }
    double difference(double, double)
    {
        return (a - b);
    }
    double product(double, double)
    {
        return (a * b);
    }
    double division(double, double)
    {
        if (b != 0)
        {
            return (a / b);
        }
        else
        {
            cout << "mathematical error" << endl;
        }
    }
    double loga(double)
    {
        return (log(a));
    }
    double logb(double)
    {
        return (log(b));
    }
    double squareroota(double)
    {
        return (sqrt(a));
    }
    double squarerootb(double)
    {
        return (sqrt(b));
    }
    double cuberoota(double)
    {
        return (cbrt(a));
    }
    double cuberootb(double)
    {
        return (cbrt(b));
    }
    double power2a(double)
    {
        return (pow(a, 2));
    }
    double power2b(double)
    {
        return (pow(b, 2));
    }
    void display_menu()
    {
        cout << "What do you want to perform?" << endl
             << endl
        << endl
        << "1.sum" << endl
        << "2.difference" << endl
        << "3.product" << endl
        << "4.division" << endl
        << "5. log of first number" << endl
        << "6. log of second number" << endl
        << "7. square root of first number" << endl
        << "8. square root of second number" << endl
        << "9. cube root of first number" << endl
        << "10. cube root of second number" << endl
        << "11. square of first number" << endl
        << "12. square of second number" << endl
        << "13. others cannot perform so exit" << endl
        << endl
        << endl;
    }
};
int main()
{
    calculator krish;
    int choice;
    double a, b;
    do
    {
        krish.display_menu();
        cin >> choice;
        if (choice >= 1 && choice <= 13)
        {
            cout << "Enter the two numbers" << endl;
            cin >> a >> b;
        }
        krish.set_data(a, b);
        switch (choice)
        {
        case 1:
            cout << "Results: " << krish.sum(a, b);
            break;
        case 2:
            cout << "Results: " << krish.difference(a, b);
            break;
        case 3:
            cout << "Results: " << krish.product(a, b);
            break;
        case 4:
            cout << "Results: " << krish.division(a, b);
            break;
        case 5:
            cout << "Results: " << krish.loga(a);
            break;
        case 6:
            cout << "Results: " << krish.logb(b);
            break;
        case 7:
            cout << "Results: " << krish.squareroota(a);
            break;
        case 8:
            cout << "Results: " << krish.squarerootb(b);
            break;
        case 9:
            cout << "Results: " << krish.cuberoota(a);
            break;
        case 10:
            cout << "Results: " << krish.cuberootb(b);
            break;
        case 11:
            cout << "Results: " << krish.power2a(a);
            break;
        case 12:
            cout << "Results: " << krish.power2b(b);
            break;
        case 13:
            cout << "Exiting the calculator" << endl;
            break;
        default:
            cout << "Invalid result. choice shoulkd be between 1 to 13" << endl;
        }
        cout << endl;
        cout << endl;
        cout << endl;
    } while (choice != 13);
    return 0;
}
