# Santorini Board Game – Java Multiplayer

University project to implement the board game **"Santorini"** in Java, featuring complete game rules, a command-line interface (CLI), and a multiplayer client-server architecture over TCP sockets. The project follows the **Model-View-Controller (MVC)** pattern, uses **Maven** as build tool, and includes a **automated tests** with high code coverage on the core components.

## Project Structure

- `model/`: Contains the core game logic and data structures (e.g., `Cell`, `Map`, `Player`). This represents the **Model** in the MVC architecture.
- `view/`: Implements the **View**, handling the user interface and remote communication using the Observer pattern (`Observable`, `Observer`, `RemoteView`).
- `controller/`: Coordinates the interaction between the model and view. Implements the **Controller** logic, enforcing game rules and flow.
- `server/`: Manages player connections, instantiates game sessions, and coordinates client-server interactions.
- `client/`: Handles the client-side startup and communication. Parses user input via CLI and interacts with the server.
- `test/`: Unit tests for `model` and `controller` components using JUnit, with coverage above 90%.

## Teamwork
- Team of 3 people
