# Multi-Agent System Using Phidata

A scalable multi-agent system built with Python and Phidata, where multiple AI agents collaborate to accomplish complex tasks towards autonomous content creation.

## 🌟 Features

- Modular agent architecture for easy expansion and maintenance
- Asynchronous communication between agents
- Built-in monitoring and logging
- Configurable agent behaviors and roles
- Scalable infrastructure using Phidata
- Comprehensive error handling and recovery

## 🛠 System Architecture

The system consists of several specialized agents:

1. **Coordinator Agent**: Orchestrates tasks and manages communication between agents
2. **Task Processing Agents**: Handle specific domain tasks
3. **Monitoring Agent**: Tracks system health and agent performance
4. **Data Management Agent**: Handles data storage and retrieval

## 📋 Prerequisites

- Python 3.9+
- pip or conda package manager
- Git

## 🚀 Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/AmirSh15/content_creation_agent.git
cd your-project-name
```

2. Create and activate a virtual environment:
```bash
conda create -n content-agent python=3.9
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

### Configuration

1. Copy the example configuration file:
```bash
cp config/example.config.yaml config/config.yaml
```

2. Update the configuration file with your settings:
```yaml
project:
  name: your-project-name
  environment: development

agents:
  coordinator:
    enabled: true
    max_workers: 2
  task_processor:
    enabled: true
    instances: 3
```

### Running the System

1. Start the system:
```bash
python main.py
```

2. Monitor the agents:
```bash
python tools/monitor.py
```

## 📁 Project Structure

```
├── agents/
│   ├── __init__.py
│   ├── coordinator.py
│   ├── task_processor.py
│   ├── monitor.py
│   └── data_manager.py
├── config/
│   ├── __init__.py
│   ├── example.config.yaml
│   └── config.yaml
├── core/
│   ├── __init__.py
│   ├── communication.py
│   └── utils.py
├── tests/
│   ├── __init__.py
│   └── test_agents/
├── tools/
│   └── monitor.py
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## 🔧 Development

### Adding a New Agent

1. Create a new agent file in the `agents/` directory
2. Inherit from the base agent class:
```python
from phidata import BaseAgent

class NewAgent(BaseAgent):
    def __init__(self, config):
        super().__init__(config)
        
    async def process(self, message):
        # Agent-specific processing logic
        pass
```

3. Register the agent in the configuration file

### Testing

Run the test suite:
```bash
pytest tests/
```

Run specific test categories:
```bash
pytest tests/test_agents/
```

## 📊 Monitoring

The system provides several monitoring endpoints:

- Agent Status: `http://localhost:8080/status`
- System Metrics: `http://localhost:8080/metrics`
- Health Check: `http://localhost:8080/health`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Open an issue on GitHub
- Contact the maintainers at [your-email@example.com]

## 🙏 Acknowledgments

- [Phidata](https://github.com/phidatahq/phidata) for the excellent agent framework
- All contributors who have helped shape this project
