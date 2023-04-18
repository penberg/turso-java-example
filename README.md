# Turso Java Example

## Getting Started

Build and install the Java SDK for LibSQL:

```bash
git clone https://github.com/libsql/libsql-client-java.git
cd libsql-client-java
mvn install
```

Please note that this step will be eliminated after we publish to Maven Central.

Create a database:

```bash
turso db create java-example
```

and add some tests data:

```bash
turso db shell java-example "CREATE TABLE users (email TEXT)"
turso db shell java-example "INSERT INTO users (email) VALUES ('alice@example.org')"
```

Configure URL and access token in environment variables:

```bash
export DATABASE_URL=$(turso db show --url java-example)
export DATABASE_TOKEN=$(turso db tokens create java-example)
```

Build the example application:

```bash
mvn package
```

and run it:

```bash
java -jar turso-example.jar
```

## License

This project is licensed under the MIT license.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in this project by you, shall be licensed as MIT, without any additional terms or conditions.
