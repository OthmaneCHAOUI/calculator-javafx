# Calculatrice JavaFX

> A simple desktop calculator built with JavaFX and styled with CSS.

## Overview

Calculatrice JavaFX is a lightweight graphical calculator for performing basic arithmetic operations. It provides a button-based interface, displays the current expression and result, and can be reset at any time.

## Features

- Addition, subtraction, multiplication, and division.
- Decimal number input.
- Dynamic expression and result display.
- Clear (`C`) button to reset the calculator.
- Color-coded calculator buttons with hover and pressed states.
- Responsive button layout using JavaFX `GridPane`.

## Tech Stack

| Component | Technology |
|---|---|
| Language | Java 21 |
| UI framework | JavaFX 21.0.2 |
| Styling | JavaFX CSS |
| Build tool | Apache Maven |
| Testing framework | JUnit 5 (configured; no tests are currently included) |

## Architecture

The application uses a small event-driven structure:

1. [`Main`](src/main/java/main/Main.java) extends JavaFX `Application` and creates the calculator window.
2. Button events are handled by the calculator logic in `Main`.
3. Arithmetic operations are evaluated by `calculate`.
4. [`style.css`](src/main/java/style/style.css) defines the visual appearance and interaction states of the controls.

The calculator keeps its state in memory and does not use a database, network service, or external configuration.

## Requirements

- JDK 21 or later.
- Maven 3.9 or later.
- A graphical environment capable of running JavaFX.

JavaFX dependencies are downloaded automatically by Maven.

## Installation

Clone the repository and enter its directory:

```bash
git clone https://github.com/OthmaneCHAOUI/calculator-javafx.git
cd calculator-javafx
```

Compile the project:

```bash
mvn clean compile
```

## Usage

Start the application with the JavaFX Maven plugin:

```bash
mvn javafx:run
```

Then use the calculator buttons to:

1. Enter the first number.
2. Select an operator (`+`, `-`, `x`, or `/`).
3. Enter the second number.
4. Select `=` to display the result.
5. Select `C` to clear the current calculation.

## Configuration

No environment variables or configuration files are required. Maven and JavaFX settings are defined in [`pom.xml`](pom.xml).

## Testing

Run the configured test lifecycle with:

```bash
mvn test
```

JUnit 5 is configured as a test dependency, but the repository currently contains no automated test classes.

## Project Structure

```text
calculator-javafx/
├── pom.xml
├── src/
│   └── main/
│       ├── java/
│       │   ├── main/
│       │   │   └── Main.java
│       │   └── style/
│       │       └── style.css
└── README.md
```

## Limitations

- The calculator supports one binary operation at a time.
- There is no calculation history, keyboard input, or advanced mathematical functions.
- Division by zero and malformed expressions do not have dedicated user-facing validation.
- Automated tests and continuous integration are not currently included.

## Roadmap

- [x] Implement the JavaFX calculator interface.
- [x] Support the four basic arithmetic operations.
- [x] Add CSS styling and button interaction states.
- [ ] Add input validation and user-friendly error messages.
- [ ] Add automated tests for calculation and input handling.
- [ ] Support chained operations and keyboard input.

## Contributing

Contributions and suggestions are welcome. Before opening a pull request:

1. Create a focused branch for your change.
2. Run `mvn test`.
3. Describe the behavior you changed and how it was verified.

## License

No license file is currently included in this repository.
