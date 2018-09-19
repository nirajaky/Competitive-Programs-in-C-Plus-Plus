#include <iostream>

using namespace std;
int p[100];
int f[100];

void prime() {
    int fact = 0;
    int ind=1;
    for(int i=2; i<500; i++ ) {
        fact = 0;
        for(int j =2; j<=i/2; j++) {
            if (i%j == 0)
                fact++;
        }
        if(fact ==0) {
            //cout << i << " ";
            p[ind] = i;
            ++ind;
        }
    }
}
void fibi() {
   int ind = 1;
   int firstTerm = 0,secondTerm = 1,nextTerm,num;
   f[ind] = secondTerm;

    for(int i=1; i<=50; i++) {
        nextTerm = firstTerm + secondTerm;
        firstTerm = secondTerm;
        secondTerm = nextTerm;
        ++ind;
        f[ind] = nextTerm;
    }
}

int main()
{
    int num;
    int ind1= 1;
    int ind2= 1;
    cout << "Enter num. of terms :" ;
    cin >> num;

    prime();
    fibi();

    for(int i =1; i<=num; i++) {
        if (i%2 == 0){
            cout << p[ind1] << " ";
            ind1++;
        }
        else {
            cout << f[ind2] << " ";
            ind2++;
        }
    }
    return 0;
}
