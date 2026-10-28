## Question: Do you agree with the developer's choice of using composition in this case?

A software developer is designing a system for a company that has different types of employees. The developer writes the following code:

```java
class Employee {
    protected String name;
    protected double salary;

    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    public void displayDetails() {
        System.out.println("Name: " + name);
        System.out.println("Salary: " + salary);
    }
}

class Manager {
    private Employee employee;

    public Manager(String name, double salary) {
        employee = new Employee(name, salary);
    }

    public void displayDetails() {
        employee.displayDetails();
    }
}