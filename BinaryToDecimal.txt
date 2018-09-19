#include <iostream>

using namespace std;

int main()
{
    int num,dNum=0,b=1;
    cout << "Enter a number: " ;
    cin >> num;
    while(num>0) {
        int temp=num%10;
        dNum =dNum +temp*b;
        num=num/10;
        b=b*2;
    }
    cout << dNum;
    return 0;
}
