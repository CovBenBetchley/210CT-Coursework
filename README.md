# 210CT-Coursework
All coursework completed in the 210CT will be posted and explained here.

//Ben Betchley
//1. Write a function that randomly shuffles an array of integers and explain the rationale behind its
//implementation.Input: [5, 3, 8, 6, 1, 9, 2, 7](One potential example of) Output : [2, 8, 3, 1, 9, 7, 5, 6].

//First I create the array, use srand to change the seed to generate a random number.
//Create a for loop and use swap to swap numbers in the array to a random position, and continues until all 8 have
//been repositioned.


#include <iostream>
#include <cstdlib>
#include <ctime>
#include <array>

using namespace std;

int main() {

	array<int, 8> rArray = { 5,3,8,6,1,9,2,7 };
	int n;

	srand(time(NULL));

	for (int i = 0; i < 8; i++) {

		int r = rand() % 8;
		int swap = rArray[i]; rArray[i] = rArray[r];  rArray[r] = swap;

	}
	
	for (int c = 0; c < rArray.size(); c++) {

		cout << rArray[c] << " " << endl;
	}

		system("pause");
}
