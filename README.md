<img src="Pulse.png" alt="Pulse Log Logo" width="250" height="250"/>
**Pulse** is a robust and scalable log management solution designed for Linux-based systems. It provides real-time log collection, secure transmission, and insightful visualization for better system monitoring and troubleshooting.

## 🚀 **Key Features**

- **Secure Log Transmission:** Encrypted communication between nodes and the server using public-key cryptography.
- **Centralized Log Aggregation:** Manage logs from multiple Linux nodes in a single interface.
- **Real-Time Monitoring:** Efficient log collection with real-time updates.
- **Node Management:** Easily register, manage, and monitor nodes using the `pulsectl` CLI tool.
- **Extensible Design:** Built with scalability and future enhancements in mind.

## 🔧 **Components**

1. **pulsectl (Node Agent CLI):** A lightweight, secure CLI tool for node registration, log management, and communication with the LogPulse server.
2. **Pulse API Server:** Handles log aggregation, storage, and visualization.

## 🛡️ **Security**

- End-to-end encrypted communication between nodes and the API server.
- JSON-based encrypted storage on the node for configuration and log metadata.

## 💡 **Use Cases**

- System log analysis for distributed Linux environments.
- Security auditing and compliance monitoring.
- Troubleshooting and debugging system behavior.

## 📚 **Getting Started**

### **Prerequisites**
- Linux-based operating system
- Python 3.8+ (for the Pulse server)
- Go 1.18+ (for `pulsectl` CLI)

### **Installation**
#### **1. Clone the Repository**
```bash
git clone https://github.com/yourusername/LogPulse.git
cd LogPulse
```

#### **2. Set Up the API Server**
```bash
cd api_server
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

#### **3. Install `pulsectl` on Node**
```bash
cd pulsectl
go build -o pulsectl
./pulsectl --help
```

### **Usage**
#### **Initialize and Generate Keys**
```bash
./pulsectl --init
```
#### **Register Node with API Server**
```bash
./pulsectl --register config.yaml
```
#### **Start the Log Agent**
```bash
./pulsectl --start
```
#### **Check Status**
```bash
./pulsectl --status
```

## 🛠️ **Project Structure**
```
LogPulse/
├── api_server/    # Pulse API Server source code
├── pulsectl/      # Node Agent CLI tool source code
├── docs/          # Documentation files
└── README.md      # Project documentation
```

## 🤝 **Contributing**
We welcome contributions! Please fork the repository and submit a pull request.

## 📝 **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 **Contact**
If you have any questions, feel free to open an issue or reach out at [your.email@example.com](mailto:your.email@example.com).
