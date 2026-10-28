## Scenario Question: Do you agree with the developer's choice of using inheritence in this case?

A developer is designing a car rental system. They create a `Car` class and use inheritance to represent its engine, as shown below:

```java
class Car {
    protected String model;

    public Car(String model) {
        this.model = model;
    }

    public void start() {
        System.out.println(model + " is starting.");
    }
}

class Engine extends Car {
    private int horsepower;

    public Engine(String model, int horsepower) {
        super(model);
        this.horsepower = horsepower;
    }

    public void displayEngineDetails() {
        System.out.println("Horsepower: " + horsepower);
    }
}