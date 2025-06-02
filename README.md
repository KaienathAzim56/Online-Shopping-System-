# Online-Shopping-System-
Online shopping :
class User {
    String name;
    Account account;

    public User(String name, Account account) {
        this.name = name;
        this.account = account;
    }
}

class Account {
    String email;
    String password;

    public Account(String email, String password) {
        this.email = email;
        this.password = password;
    }
}

class Product {
    String productId;
    String name;
    double price;

    public Product(String productId, String name, double price) {
        this.productId = productId;
        this.name = name;
        this.price = price;
    }
}

class Order {
    String orderId;
    Product[] products;
    String status;

    public Order(String orderId, Product[] products) {
        this.orderId = orderId;
        this.products = products;
        this.status = "Pending";
    }

    public void placeOrder() {
        System.out.println("Order placed with ID: " + orderId);
        this.status = "Confirmed";
    }
}

class Shipping {
    String address;

    public Shipping(String address) {
        this.address = address;
    }

    public void shipOrder(Order order) {
        System.out.println("Shipping order " + order.orderId + " to " + address);
        order.status = "Shipped";
    }
}
