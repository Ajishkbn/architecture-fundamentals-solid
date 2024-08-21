# Single Responsibility Principle (SRP)

The Single Responsibility Principle (SRP) is one of the five SOLID principles of object-oriented design. It states that a class should have only one reason to change, meaning it should have only one job or responsibility.

## Moto

A class should have a single responsibility

## Example Violating SRP

In the following example, the `User` class has two responsibilities:

1. Managing user data.
2. Handling database operations.

### Code

```cpp
#include <iostream>
#include <string>

class User {
public:
    User(const std::string& name, const std::string& email)
        : name(name), email(email) {}

    void displayUser() {
        std::cout << "Name: " << name << ", Email: " << email << std::endl;
    }

    void saveToDatabase() {
        // Simulate saving to a database
        std::cout << "Saving " << name << " to database." << std::endl;
    }

private:
    std::string name;
    std::string email;
};

int main() {
    User user("John Doe", "john.doe@example.com");
    user.displayUser();
    user.saveToDatabase();
    return 0;
}
```

```plantuml
A -> B: abc
```
