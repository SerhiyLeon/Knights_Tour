/ Serhiy Leonchyk
//
// Program: P5 Knights Tour
//
// Class Section A
//
// Description: This program uses recursion to fill in an 8x8 board
// that represents a chess board. It is meant to simulate how a
// knight would move throughout the board. You first input where on
// the baord you would like to start, and then the program runs until
// it finds the correct moves to move to each spot on the board once
// and fill in the whole baord. It then outputs the amount of moves
// that it took as well as the board.
#include <iostream>
#include <iomanip>
using namespace std;
// Global Variables
int board[8][8] = { 0 }; // This is the 2D array that represents the board
long long int numMoves = 0; // Number of moves performed
bool moveKnight(int row, int col, int& movNum); // Recursive function
prototype
void boardOutput(); // Function that outputs the baord (to clean up main
())
int main() {
// Local variables
int moveNum = 1;
int row, col;
// Input message
cout << "What column would you like to start in (1 - 8)? ";
cin >> col;
cout << "What row would you like to start in (1 - 8)? ";
cin >> row;
// If starting column is outside of the board
if (row < 1 || row > 8)
{
cout << "\nERROR: Invalid starting point" << endl;
cout << "Please enter a valid starting row: " << endl;
cin >> row;
}

// If starting row is outside of the board
if (col < 1 || col > 8) {
cout << "\nERROR: Invalid starting point" << endl;
cout << "\nPlease enter a valid starting column: " << endl;
cin >> col;
}
// Initiates the recursion
moveKnight(row - 1, col - 1, moveNum);
// Outputs the amount of moves that it took
cout << "\nNumber of Moves Performed: " << endl;
cout << numMoves << endl;
boardOutput();
return 0;
}
bool moveKnight(int row, int col, int& movNum) // Recursive Function
{
// If move is not on the board return false
if (row < 0 || row > 7 || col < 0 || col > 7)
{
return false;
}
// If move is already taken return false
if (board[row][col] != 0)
{
return false;
}
// Sets place on board equal to the move number
board[row][col] = movNum;
// If all of the moves have been completeed return
if (movNum == 64) {
return true;
}
// Otherwise increment move number and pass it on to the next
recursion
numMoves++;
movNum++;
// Move type 1
if (moveKnight((row - 2), (col + 1), movNum))
{
return true;
}
// Move type 2
if (moveKnight((row - 1), (col + 2), movNum))
{
return true;
}
// Move type 3
if (moveKnight((row + 1), (col + 2), movNum))
{
return true;
}
// Move type 4
if (moveKnight((row + 2), (col + 1), movNum))
{
return true;
}
// Move type 5
if (moveKnight((row + 2), (col - 1), movNum))
{
return true;
}
// Move type 6
if (moveKnight((row + 1), (col - 2), movNum))
{
return true;
}
// Move type 7
if (moveKnight((row - 1), (col - 2), movNum))
{
return true;
}
// Move type 8
if (moveKnight((row - 2), (col - 1), movNum))
{
return true;
}
// If none of the moves were completed set this place back to 0
board[row][col] = 0;

// Decrement move number
movNum--;
return false;
}
// Outputs the board
void boardOutput() {
// Outputs the completed board
cout << "\nCompleted Board: " << endl << endl;
// This is for the border that contains the numbered columns
for (int i = 0; i < 9; i++) {
cout << setw(4) << i;
}
cout << endl << " ----------------------------------" << endl;
// Board as well as the border that contains the numbered columns
for (int i = 0; i < 8; i++) {
cout << setw(3) << i + 1 << "|";
for (int j = 0; j < 8; j++) {
cout << setw(4) << board[i][j];
}
cout << endl;
}
}
