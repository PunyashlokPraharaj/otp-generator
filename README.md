//link: https://github.com/PunyashlokPraharaj/otp-generator

#include <iostream>
#include <ctime>
#include <cstdlib>
using namespace std;
void generateOTP(int length) {
    int* otp = new int[length];
    srand(time(0));
    cout << "Generated OTP: ";
    for (int i = 0; i < length; ++i) {
        otp[i] = rand() % 10;
        cout << otp[i];
    }
    cout << endl;
    delete[] otp;
}
int main() {
    int length;
    cout << "Enter the number of digits for the OTP: ";
    cin >> length;

    if (length <= 0) {
        cout << "Invalid input. Length must be a positive number." << endl;
         return 1;
    }

    generateOTP(length);
    return 0;
}
