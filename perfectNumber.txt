#include <iostream>

using namespace std;

int main()
{
    int num, sum =0;

    cout << "Enter a number : ";
    cin >> num;

    int num1 = num;

    for(int i=1; i<num; i++ ) {
        if(num%i == 0)
            sum = sum + i;
    }
    if (num1 == sum)
        cout << "Perfect Number " << endl;
    else
        cout << "Not a Perfect Number" << endl;

    return 0;
}
