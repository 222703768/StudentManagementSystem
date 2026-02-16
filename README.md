StudentManagementSystem

SOLID Principles Applied
Single Responsibility Principle (SRP)

Each class has one responsibility:

Student → Defines common structure and behavior.

UndergraduateStudent: Handles undergraduate-specific data and tuition calculation.

GraduateStudent: Handles graduate-specific logic.

Builder classes: Responsible only for object construction.

Example:

public double calculateTuition() {
    double costPerCredit = 300;
    return (creditHours * costPerCredit) - scholarshipAmount;
}


The tuition logic is contained within the specific student class, not mixed elsewhere.

Liskov Substitution Principle (LSP)

Objects of UndergraduateStudent and GraduateStudent can be used wherever Student is expected.

Example:

Student undergrad = new UndergraduateStudent.Builder().build();
Student graduate = new GraduateStudent.Builder().build();


Both work through polymorphism.
