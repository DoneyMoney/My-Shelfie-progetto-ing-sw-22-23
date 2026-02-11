![](https://cf.geekdo-images.com/Sgg2B7kxtx8fFXz_2mPefA__opengraph/img/u7oY_IuMdJmX2X_xOlSd1XBsFNo=/0x179:3085x1798/fit-in/1200x630/filters:strip_icc()/pic7193695.png)

# My Shelfie - Distributed Board Game

[![Java](https://img.shields.io/badge/Java-SE-orange?style=flat-square&logo=java)](https://www.oracle.com/java/)
[![Maven](https://img.shields.io/badge/Maven-3.9-blue?style=flat-square&logo=apache-maven)](https://maven.apache.org/)
[![Software Engineering](https://img.shields.io/badge/Polimi-Software%20Engineering-red?style=flat-square)](https://www.polimi.it/)

This repository contains the digital implementation of the **My Shelfie** board game, developed as the final project for the **Software Engineering** course at **Politecnico di Milano** (A.Y. 2022/2023).

## 📋 Official Documentation & Rules
The project follows the official game rules and the technical specifications provided by the university:

* 📄 [**Official Rulebook (ITA)**](https://www.craniocreations.it/storage/media/product_downloads/79/1010/Rulebook_ITA_My-Shelfie.pdf) - **Reference version for rules**.
* 📄 [**Official Rulebook (ENG)**](https://www.craniocreations.it/storage/media/product_downloads/48/538/MyShelfie_Ruleboo_ENG_lowres_new.pdf).
* 🛠️ [**Technical Requirements (PDF)**](./Requirements.pdf) - Official project constraints (Italian).

---

## 🏗️ Project Requirements (Summary)
Since the original requirement document is in Italian, here is a summary of the technical constraints and goals achieved in this project:

### System Architecture
* **Distributed System**: Implemented using a **Client-Server** architecture.
* **MVC Pattern**: Full adoption of the **Model-View-Controller** design pattern to separate game logic, data management, and user interfaces.
* **Language**: All code identifiers, comments, and technical documentation (JavaDoc) are in **English**.



### Networking & Interfaces
* **Multi-Protocol Support**: Simultaneous support for **RMI** and **TCP Sockets**. The server can manage matches where different players use different technologies.
* **Dual Interface**:
    * **GUI (Graphical User Interface)**: Built with **JavaFX** for an immersive visual experience.
    * **TUI (Textual User Interface)**: A command-line interface (CLI) with ANSI color support.

### Advanced Features (FA)
* **Persistence**: The server periodically saves the game state to disk, allowing recovery after a crash.
* **Disconnection Resilience**: Players can rejoin an ongoing match after a network failure. While a player is disconnected, the game continues by skipping their turns.

---

## 🚀 How to Run
The project is managed via **Maven**. All components (Server and Client) are bundled into a single executable JAR file.

### Prerequisites
* **Java SDK 19** or higher.
* **Maven 3.8+**.

### 1. Build the Project
Generate the executable JAR in the `/target` directory:
```bash
mvn clean package
```
### 2. Launch the Application
Run the JAR file from your terminal:
```bash
java -jar MyShelfie.jar
```
### 3. Select Role
Upon startup, the system will prompt you to choose your configuration:

1. **Server**: Select option `0` to host the game session.
2. **Client**: Choose between **GUI** (option `1`) or **TUI** (option `0`) for your interface.
3. **Connection**: Select **RMI** or **Socket** as the communication protocol.

> **Note for CLI users**: Run `EnableAnsiCmd.bat` before starting the JAR on Windows to enable terminal colors.

---

## 👥 The Team (Group PSP01)
* **Donato Fiore**
* **Alessandro Fornara**
* **Samuele Pietro Galli**
* **Edoardo Gennaretti**

---

## ⚖️ Copyright
**My Shelfie** is a board game designed and published by **Cranio Creations Srl**. All graphical assets and game-specific trademarks are used with permission for educational purposes only as part of the Politecnico di Milano software engineering curriculum. Commercial use, reproduction, or redistribution of these contents is strictly prohibited.
