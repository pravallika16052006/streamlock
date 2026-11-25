# 🛡️ STREAMLOCK: Encrypted Terminal & AI Banking Hub

STREAMLOCK is a high-performance, full-stack financial ecosystem featuring real-time Kafka event-streaming, biometric-grade VPN security, and an AI-powered Expenditure Planner. Built for the future of decentralized finance, it replaces traditional IDs with secure Node Identifiers (Mobile Numbers).

## 🚀 Key Features

- **Decentralized Infrastructure**: Apache Kafka backbone for real-time transaction settling and event-sourced auditing.
- **Node-Based Transactions**: Real-world identification using **10-digit Mobile Numbers**, eliminating the need for complex UPI handles.
- **AI Expenditure Planner**: A 10-step interactive wizard that analyze your spending,      provides financial health scores, and generates 6-month growth roadmaps.
- **Triple-Layer VPN Security**: 
  - **Level 1**: Secure JWT-based Authentication.
  - **Level 2**: Simulated **VPN Tunnel Entry** using unique 16-character alphanumeric Secret Keys.
  - **Level 3**: 4-digit Transaction PIN for secure settlements.
- **AI Hub Services**: 
  - **Voice Assistant**: STT/TTS assistant with a 2,000-record dataset and precision microphone control.
  - **Node Hub**: A futuristic, glassmorphism-based utility grid for Mobile, Electricity, DTH, and Credit Card management.
- **Premium Aesthetics**: High-fidelity dark mode with fluid micro-animations (Framer Motion) and interactive data visualizations (Recharts).

---

## 🛠️ Execution Setup

### 1. Prerequisites
- **Node.js**: v18+ recommended.
- **Docker**: For running Kafka, Zookeeper, and MongoDB.

### 2. Infrastructure (Docker)
In the root directory, run:
```bash
docker-compose up -d
```

### 3. Backend Setup
```bash
cd backend
npm install
# Seed the banking dataset for the AI Assistant
node seeders/chatbotSeeder.js
# Start the encrypted server
node server.js
```

### 4. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

---

## 📱 Interactive Modules

### 1. Secure Onboarding
- **Register**: Enter your email and a **10-digit Mobile Number**.
- **OTP Verification**: Check your **Terminal/Console** for the simulated 6-digit registration OTP.
- **VPN Key**: Upon success, you are issued a unique **VPN Secret Key**. **Store this safely**; you will need it for every login.

### 2. AI Expenditure Planner 🧠
- Navigate to the **Budget AI** (Brain icon) tab.
- Enter your Salary and EMIs.
- Complete the 10-category spending wizard.
- Receive immediate AI feedback on overspending and view your **Savings Projection Roadmap**.

### 3. The Node Services Hub
- View your **Encrypted Balance** on the main dashboard.
- Explore the **Services Grid** (Mobile, Electricity, DTH, etc.) styled with unique STREAMLOCK futuristic aesthetics.
- Monitor your **Kafka Stream Latency** and Network Protocol health live.

### 4. Making a Payment
- Navigate to **Send Payment**.
- Enter the recipient's **10-digit Mobile Number**.
- Grant **VPN Tunnel Permission** and authorize with your **4-digit PIN**.
- Payments are settled near-instantly across the decentralized stream.

---

## ⚙️ System Architecture

### 1. Secure VPN Tunnel Logic
- **Secret Keys**: High-entropy keys generated at registration and stored with one-way encryption.
- **Tunneling**: Authentication requires a valid JWT *and* a verified VPN handshake to access sensitive financial data.

### 2. AI Analytical Engine (Recharts & Natural)
- **Expenditure Logic**: Uses a rule-based AI engine to compare spending against the 50/30/20 rule and provide corrective insights.
- **Assistant**: Powered by a TF-IDF vectorizer and the `natural` NLP library for sub-second responses.

### 3. Real-time Event Streaming (Kafka)
- Transactions are published to the `payment-events` topic.
- A decoupled consumer processes these events for auditing, ensuring the UI remains responsive even during high-traffic settlements.

---
*Created with ❤️ by the StreamLock Engineering Team.*
