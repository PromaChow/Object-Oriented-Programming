```class Payment { }

class CreditCardPayment extends Payment {
    void pay() {
        System.out.println("Paid using credit card");
    }
}

class BkashPayment extends Payment {
    void pay() {
        System.out.println("Paid using bKash");
    }
}

class CashPayment extends Payment {
    void pay() {
        System.out.println("Paid using cash");
    }
}

public class Main {
    static void processPayment(Payment payment) {
        if (payment instanceof CreditCardPayment) {
            ((CreditCardPayment) payment).pay();
        } else if (payment instanceof BkashPayment) {
            ((BkashPayment) payment).pay();
        } else if (payment instanceof CashPayment) {
            ((CashPayment) payment).pay();
        }
    }


public static void main(String[] args) {
    processPayment(new CreditCardPayment());
    processPayment(new BkashPayment());
    processPayment(new CashPayment());
}
```

}

## What problem might arise when a new payment method is added?

