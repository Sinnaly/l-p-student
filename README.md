# l-p-student
#include <iostream>
#include <string>

class Student {
private:
    std::string name;
    int id;
    float gpa;

public:
    // Constructor
    Student(std::string n, int i, float g) : name(n), id(i), gpa(g) {}

    // Getter methods
    std::string getName() { return name; }
    int getId() { return id; }
    float getGpa() { return gpa; }

    // Setter methods
    void setName(std::string n) { name = n; }
    void setId(int i) { id = i; }
    void setGpa(float g) { gpa = g; }

    // Method to display student information
    void displayInfo() {
        std::cout << "Name: " << name << ", ID: " << id << ", GPA: " << gpa << std::endl;
    }
};

int main() {
    std::string name;
    int id;
    float gpa;

    // User input
    std::cout << "Enter student's name: ";
    std::getline(std::cin, name);
    std::cout << "Enter student ID: ";
    std::cin >> id;
    std::cout << "Enter student GPA: ";
    std::cin >> gpa;

    // Create Student object with user input
    Student student(name, id, gpa);

    // Display student information
    std::cout << "\nStudent Information:" << std::endl;
    student.displayInfo();

    return 0;
}
