## Scenario Question: Do you agree with the developer's choice of using composition in this case?


A developer is designing a computer system. They create a `Computer` class and use inheritance to represent its processor, as shown below:

```java
class Computer {
    protected String model;

    public Computer(String model) {
        this.model = model;
    }

    public void start() {
        System.out.println(model + " is starting...");
    }
}

class Processor extends Computer {
    private String brand;

    public Processor(String model, String brand) {
        super(model);
        this.brand = brand;
    }

    public void processData() {
        System.out.println(brand + " processor is processing data.");
    }
}