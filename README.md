#include <iostream>
#include <string>
using namespace std;

class Person {
private:
    string name;
    int age;
    string id;
    string contact;

public:
    Person(string n, int a, string i, string c) {
        setName(n);
        setAge(a);
        setId(i);
        setContact(c);
    }

    ~Person() {}

    string getName() { return name; }
    void setName(string n) {
        if (!n.empty()) name = n;
    }

    int getAge() { return age; }
    void setAge(int a) {
        if (a > 0 && a < 120) age = a;
    }

    string getId() { return id; }
    void setId(string i) {
        id = i;
    }

    string getContact() { return contact; }
    void setContact(string c) {
        contact = c;
    }

    virtual void displayDetails() {
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
        cout << "ID: " << id << endl;
        cout << "Contact: " << contact << endl;
    }

    virtual double calculatePayment() {
        return 0.0;
    }
};# FOCP-II-Assignment-2
