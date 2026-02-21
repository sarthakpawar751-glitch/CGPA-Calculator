# CGPA-Calculator
#include <iostream>
using namespace std;

int main() {
    int numCourses;
    float grade, credit;
    float totalCredits = 0;
    float totalGradePoints = 0;

    cout << "Enter the number of courses: ";
    cin >> numCourses;

    float grades[numCourses];
    float credits[numCourses];

    for (int i = 0; i < numCourses; i++) {
        cout << "\nCourse " << i + 1 << endl;

        cout << "Enter Grade (e.g., 8.5): ";
        cin >> grade;
        grades[i] = grade;

        cout << "Enter Credit Hours: ";
        cin >> credit;
        credits[i] = credit;

        totalCredits += credit;
        totalGradePoints += (grade * credit);
    }

    float cgpa = totalGradePoints / totalCredits;

    cout << "\n----- Course Details -----" << endl;
    for (int i = 0; i < numCourses; i++) {
        cout << "Course " << i + 1 
             << " | Grade: " << grades[i] 
             << " | Credits: " << credits[i] << endl;
    }

    cout << "\nTotal Credits: " << totalCredits << endl;
    cout << "Final CGPA: " << cgpa << endl;

    return 0;
}
