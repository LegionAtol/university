# Santorini Board Game – Java Multiplayer

University project to implement the board game **"Santorini"** in Java, featuring complete game rules, a command-line interface (CLI), and a multiplayer client-server architecture over TCP sockets. The project follows the **Model-View-Controller (MVC)** pattern, uses **Maven** as build tool, and includes a **automated tests** with high code coverage on the core components.

## Project Structure

- `model/`: Contains the core game logic and data structures (e.g., `Cell`, `Map`, `Player`). This represents the **Model** in the MVC architecture.
- `view/`: Implements the **View**, handling the user interface and remote communication using the Observer pattern (`Observable`, `Observer`, `RemoteView`).
- `controller/`: Coordinates the interaction between the model and view. Implements the **Controller** logic, enforcing game rules and flow.
- `server/`: Manages player connections, instantiates game sessions, and coordinates client-server interactions.
- `client/`: Handles the client-side startup and communication. Parses user input via CLI and interacts with the server.
- `test/`: Unit tests for `model` and `controller` components using JUnit, with coverage above 90%.

## Game rules
Each player controls two workers and takes turns to move and build on a 5x5 grid. The goal is to move one of your workers onto the third level of a building.

**Turn Overview**:

Move: Choose one of your workers and move it to an adjacent space (orthogonal or diagonal) that is:
   - Not occupied
   - Not more than one level higher than the current space

Build: After moving, build on an adjacent space. You can increase the building’s level (up to level 3), or cap it with a dome (level 4).

**Win conditions**:

- You win if one of your workers moves to the third level of a building.

**Restrictions**:

- You cannot move into a space with a dome.
- You cannot move into a space already occupied by any worker.
- You can move down any number of levels.

**Special Powers**:

The game includes optional God powers that modify the basic rules, such as:
- Apollo: Swap places with an opponent’s worker.
- Artemis: Move twice (but not back to the original space).
- Athena: Opponent cannot move up if you moved up last turn.


## Teamwork
- Team of 3 people
