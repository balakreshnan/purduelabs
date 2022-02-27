# Purdue Smart Factory Architecture

## Smart Foundry Reference Architecture

## Use Case

- Purdue smart Foundry for students to learn
- Modular approach to learn
- Agility to change and try various configurations
- Ability to change the line as needed
- Connected to Enterprise systems and OT network
- Ability to bring data from enterprise systems to MES and to line
- Factory operation in hybrid environment
- MES will run on premise in hybrid hardware - prefered scalable to cloud
- Analytics and Machine learning in Cloud
- Ability to read data from any line and equipment using Industrial IoT Gateway

## Architecture

![Architecture](https://github.com/balakreshnan/purduelabs/blob/main/images/purduelabs-SmartFoundry.jpg "Architecture")

## Architecture Explained

- The above architecture is divided into 2 major parts
- On premise factory environment
- On premise host MES and other Scada systems
- On Premise connects to Enterprise systems
- Move data into cloud for Analytics
- Machine learning training is in cloud
- Inference in cloud and on premise

### Hybrid - On premise - IDC

- IDC is industrial data center, rack server on premise
- Industrial assembly line is connected to Factory talk Edge gateway
- Edge gateway has the necessary tools to pull data from sensor
- Combination of PTC Kepware and Factory talk edge based on production systems
- Factory Talk edge connects to line using CIP protocol
- System should be able to collect data and change as needed
- System should be able to handle schema changes data
- Connectivity and security in place for students to collect data and work
- IT/OT is connected
- OT connectivity goes through a firewall
- IT connectivity goes through a firewall
- Gateway connectivity using VPN inside OT
- Run Gateway in VM inside IDC

### Cloud - Big data and Machine learning analytics

- Gateway uses sdk mode to IoT hub
- Iot Hub will be gateway and also device connected with device security
- Iot hub to store data in storage for long term big data analytics
- Iot hub to send to Azure Data explorer (Historian)
- Build centralized Manufacturing data lake
- Apply Root cause analysis using Big data technologies
- Use data for machine learning and anomaly detection
- Build predictive maintanence models
- Build also Real time or near realtime UI in cloud