### Does EmailNotification override send() or does it overload it?

```class EmailNotification extends Notification {
    void send(Object message) {
        System.out.println("Sending email: " + message);
    }
}

public class Main {
    public static void main(String[] args) {
        Notification notification = new EmailNotification();
        notification.send("Hello!");
    }
}```
