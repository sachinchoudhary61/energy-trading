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

## AWS Setup Guide
### Why AWS?
To simulate real-world energy trading, we use **AWS IoT Core** for device communication and **DynamoDB** for scalable data storage. AWS provides a free-tier account where users can access free credits, making it easy to experiment without incurring costs.

### Setting Up AWS
1. **Create an AWS Free Tier Account**:
   - Visit [AWS Free Tier](https://aws.amazon.com/free/) and sign up.
   - AWS offers free usage credits for new users, allowing them to experiment with IoT Core and DynamoDB.

2. **Set Up AWS IoT Core**:
   - Navigate to the AWS IoT Core service.
   - Create a new **Thing** (representing a power unit device).
   - Generate security certificates and policies for MQTT communication.
   - Create an **MQTT topic** where power units will publish data.

3. **Configure DynamoDB**:
   - Open the **DynamoDB** service in AWS.
   - Create a new table (e.g., `power_units_data`) with a **primary key** for identifying power unit records.

4. **Obtain AWS Credentials**:
   - Generate IAM user credentials with appropriate permissions.
   - Store the AWS access key and secret key in your environment variables.

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
