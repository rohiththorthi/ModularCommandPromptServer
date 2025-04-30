# ModularCommandPromptServer
My first Modular Command Prompt Server

🧠 Modular Command Prompt Server (MCPS)
A lightweight, extensible command prompt server written in Java. Accepts TCP connections and processes modular commands like a custom shell. Ideal for learning or extending into a developer utility, system monitor, or remote controller.

📦 Features
🧩 Modular command architecture using OOP

🧵 Multi-threaded client handling

📡 TCP-based server for CLI-style input/output

📜 Built-in commands like hello, time, help, exit

🧰 Easily extendable with custom commands

🔌 Plugin-friendly structure

🧪 Unit test ready

🚀 Ready for REST or WebSocket expansion

🐳 Dockerizable and cloud-deployable

🗂️ Project Structure
bash
Copy
Edit
modular-cp-server/
├── src/
│   └── com/mcps/
│       ├── MainServer.java
│       ├── CommandHandler.java
│       ├── CommandRegistry.java
│       ├── ClientHandler.java
│       └── commands/
│           ├── HelloCommand.java
│           ├── TimeCommand.java
│           └── ExitCommand.java
└── README.md
⚙️ How It Works
Clients connect via TCP (e.g., using Telnet or custom CLI)

Command input is parsed and routed to a registered CommandHandler

Each command is a self-contained Java class

Multiple clients can connect simultaneously

🧱 Getting Started
✅ Prerequisites
Java 17+

Git

Maven or Gradle

🔧 Build & Run
bash
Copy
Edit
git clone https://github.com/your-username/modular-cp-server.git
cd modular-cp-server
javac com/mcps/MainServer.java
java com.mcps.MainServer
By default, the server listens on port 9999.

🧪 Connect as Client (from another terminal)
bash
Copy
Edit
telnet localhost 9999
📜 Built-in Commands

Command	Description
hello	Returns a greeting
time	Shows current server time
help	Lists all available commands
exit	Disconnects from server
✍️ Adding a New Command
Create a new class in commands/ implementing CommandHandler:

java
Copy
Edit
public class PingCommand implements CommandHandler {
    public String getCommandName() {
        return "ping";
    }
    public String handle(String[] args) {
        return "pong";
    }
}
Register it in CommandRegistry.java:

java
Copy
Edit
register(new PingCommand());
🔐 Future Roadmap
 Add REST API via Spring Boot

 Add WebSocket communication

 Add authentication (JWT or API keys)

 Add command history/logging

 Plugin system for loading JARs dynamically

 Dockerfile and CI/CD integration

🧠 Concepts Covered
Java OOP (Interfaces, Polymorphism)

Multi-threading and concurrency

Socket programming

Command pattern

Modular architecture

Real-time data flow

Clean coding practices

📜 License
MIT License

🤝 Contributing
Fork the repo

Create a feature branch (git checkout -b feature-name)

Commit changes (git commit -m 'Add new feature')

Push (git push origin feature-name)

Open a Pull Request

📢 Contact
Built by [Your Name]
📧 Email: yourname@example.com
🌐 GitHub: github.com/your-username


