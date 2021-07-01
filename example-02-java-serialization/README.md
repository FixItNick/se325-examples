# SE325 Example 02 - Java Serialization
This project contains an example of how to serialize instances of Java classes, and how to send serialized data over a TCP connection.

The `Employee`, `Manager`, and `EmployeeRequest` classes (in the [`employees`](./src/main/java/se325/example01/employees) package) each implement the [`Serializable`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/Serializable.html) interface (or in the case of `Manager`, extend from a class which does). This tags them as being eligible for serialization.

Each member (instance variable) within these classes is also serializable. Therefore, we can serialize (marshall) and deserialize (unmarshall) instances of these classes using [`ObjectOutputStream`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/ObjectOutputStream.html) and [`ObjectInputStream`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/io/ObjectInputStream.html), respectively. This is demonstrated in the `Client` and `Server` classes in the [`tcp`](./src/main/java/se325/example01/employees/tcp) package, and also in the [`TestEmployees`](./src/test/java/se325/example01/employees/TestEmployees.java) unit test.