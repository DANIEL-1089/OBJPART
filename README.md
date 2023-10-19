#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <cstring>
#include <conio.h>
#include <iomanip>
#pragma warning(disable : 4996)



using namespace std;
class part {
private:
    char partname[30];
    int partnumber;
    double cost;
public:
    void setpart(const char pname[], int pn, double c) {
        strcpy(partname, pname);
        partnumber = pn;
        cost = c;
    }
    void showpart() {
        cout << "\nName = " << partname;
        cout << ", num = " << partnumber;
        cout << ", cost = $" << cost;
    }
};


int main()
{
    part part1, part2;

    part1.setpart("coupling", 4473, 217.55);
    part2.setpart("tap wrench", 9924, 419.25);
    cout << "\nThe first detail: "; part1.showpart();
    cout << "\nThe second detail: "; part2.showpart();
    cout << endl;

    return 0;
}
