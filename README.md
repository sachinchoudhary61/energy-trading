# Energy Trading Platform

## Overview
This project is an **open-source energy trading platform** built with **Elixir Phoenix** and **DynamoDB**. It enables real-time data collection from multiple power units, allowing consumers to bid for energy based on their needs.

### Key Features
- **IoT-based energy trading**: Simulating real-world energy transactions using AWS IoT Core.
- **Real-time data ingestion**: Power units post energy metrics, which we capture via MQTT topics.
- **Multiple power unit monitoring**: Data is aggregated from multiple power sources for a unified view.
- **Tortoise MQTT Client**: Efficient subscription to power unit topics to handle real-time data streaming.
- **DynamoDB for scalable storage**: Storing energy data in a highly available and scalable NoSQL database.
- **Consumer bidding mechanism**: Users can bid for energy based on real-time power availability.

## Tech Stack
- **Elixir Phoenix** - Web framework for backend services.
- **DynamoDB** - NoSQL storage for energy data.
- **AWS IoT Core** - MQTT-based communication for power unit data.
- **Tortoise MQTT Client** - Handling MQTT subscriptions and message processing.

## Architecture
1. **Power Units Posting Data**: Each power unit continuously sends data to an IoT Core topic.
2. **MQTT Subscription**: We use **Tortoise** to subscribe to the topic and retrieve data.
3. **Data Processing**: The data is structured and stored in **DynamoDB**.
4. **Visualization & Trading**: Consumers can see live energy availability and bid accordingly.

## Installation & Setup
### Prerequisites
- **Elixir & Phoenix** installed ([Installation Guide](https://hexdocs.pm/phoenix/installation.html))
- **AWS IoT Core** setup ([Guide](https://docs.aws.amazon.com/iot/latest/developerguide/iot-security-identity.html))
- **DynamoDB** instance ([Guide](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html))

### Steps
1. **Clone the repository:**
   ```sh
   git clone https://github.com/your-repo/energy-trading-platform.git
   cd energy-trading-platform
   ```
2. **Install dependencies:**
   ```sh
   mix deps.get
   ```
3. **Set up environment variables** (AWS credentials, IoT topics, etc.) in `.env`.
4. **Run the server:**
   ```sh
   mix phx.server
   ```

## Energy Trading Research Papers
- [Decentralized Energy Trading using Blockchain](https://www.sciencedirect.com/science/article/pii/S1364032121006120)
- [Energy Market Challenges & Opportunities](https://ieeexplore.ieee.org/document/9175775)
- [Peer-to-Peer Energy Trading: Concepts & Future Directions](https://arxiv.org/abs/1906.08417)

## Contribution
We welcome contributions! Feel free to open issues, suggest features, or submit PRs.


