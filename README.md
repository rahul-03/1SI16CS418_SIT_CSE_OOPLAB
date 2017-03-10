# 1SI16CS418_SIT_CSE_OOPLAB

#include <iostream>
using namespace std;

class TwoVal
{
	int val1,val2;

	public:
		void getdata(void);
		void print_Value(void);
		friend void swap(TwoVal&);
};

void TwoVal ::getdata(void)
{
    cout << "Enter two values" << endl;
    cin >> val1 >> val2;
}
void TwoVal :: print_Value(void)
{
	cout << "Values are = \n" << val1 << "\t" << val2 << endl;
}

void swap(TwoVal& v1)
{
    int t;

    t = v1.val1;
    v1.val1 = v1.val2;
    v1.val2 = t;
}

int main()
{
    TwoVal pair1;
    pair1.getdata();
    cout << "\nBefore swapping \n";
    pair1.print_Value();
    swap(pair1);
    cout << "\nAfter swapping \n";
    pair1.print_Value();
    return 0;
}
