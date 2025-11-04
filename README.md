## Part C: Spring + Hibernate Transaction Management

### Description

* Banking system demonstrating **transaction management** using Spring and Hibernate.
* `BankingService` ensures **atomic money transfer** between accounts.
* Uses `@Transactional` annotation for declarative transactions.

### How to Run

1. Make sure MySQL is running and `nimbusdb` exists. Update `hibernate.cfg.xml` with your credentials.
2. Navigate to `PartC_SpringHibernateTransaction/src/main/java`.
3. Compile all Java files:

```bash
javac -cp "path_to_spring_jars/*:path_to_hibernate_jars/*:path_to_jpa_jars/*:path_to_mysql_connector/*" com/example/banking/*.java com/example/banking/config/*.java com/example/banking/dao/*.java com/example/banking/model/*.java com/example/banking/service/*.java
```

4. Run the application:

```bash
java -cp ".:path_to_spring_jars/*:path_to_hibernate_jars/*:path_to_jpa_jars/*:path_to_mysql_connector/*" com.example.banking.MainApp
```

**Expected Output:**

* Creates two accounts
* Performs money transfer
* Prints updated balances
* If transfer fails (e.g., insufficient funds), the transaction is rolled back
