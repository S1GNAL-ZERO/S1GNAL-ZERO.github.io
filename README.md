# S1GNAL.ZERO 🛡️

<div align="center">

**AI-Powered Authenticity Verification System**

**AGI Ventures Canada Hackathon 3.0** | **Powered by Solace PubSub+** | **[Live Demo](https://s1gnal-zero.github.io)**

</div>

* * *

## 🎯 Mission

**S1GNAL.ZERO** cuts through manufactured viral trends to reveal the truth behind digital hype. Our multi-agent AI system instantly detects bots, fake reviews, and coordinated manipulation campaigns, protecting consumers and businesses from FOMO-driven deception.

## 🚀 Built at AGI Ventures Canada Hackathon 3.0

* **Event**: [AGI Ventures Canada Hackathon 3.0](https://lu.ma/ai-tinkerers-ottawa) (formerly AI Tinkerers Ottawa)
* **Date**: September 6-7, 2025
* **Location**: Ottawa, Ontario
* **Sponsor**: [Solace PubSub+](https://solace.com)

## ✨ Features

### 🤖 Multi-Agent Intelligence

* **Distributed Python Agents** communicating via Solace Agent Mesh
* **Bot Detection Agent**: Identifies automated accounts and coordinated behavior
* **Trend Analysis Agent**: Detects abnormal growth patterns and viral velocity
* **Review Validator Agent**: Cross-references reviews with purchase patterns
* **Score Aggregator Agent**: Combines all signals into Reality Score™

### ⚡ Event-Driven Architecture

* All analysis requests via Solace topics
* Powered by Solace PubSub+ event streaming
* JCSMP client for guaranteed message delivery
* Real-time WebSocket updates to UI

### 📊 Reality Score™

Our proprietary scoring algorithm provides:

* **0-33%**: Heavily Manipulated (Red Zone)
* **34-66%**: Mixed Signals (Yellow Zone)
* **67-100%**: Authentic Engagement (Green Zone)

## 🔍 Use Cases

1. **Consumer Protection**: Avoid FOMO-driven purchases on manufactured viral products
2. **Brand Protection**: Identify competitor sabotage and fake review attacks
3. **Marketing Due Diligence**: Verify influencer authenticity before partnerships
4. **E-commerce Intelligence**: Detect dropshipping scams and bot-driven trends
5. **Investment Analysis**: Identify pump-and-dump schemes in viral stocks

## 🛠️ Technology Stack

* **Event Broker**: Solace PubSub+ for real-time messaging
* **AI Framework**: Python Agent Mesh for distributed processing
* **Backend**: Spring Boot (Java) with Solace JCSMP
* **Frontend**: Vaadin UI with real-time WebSocket updates
* **Database**: PostgreSQL for user data and analysis history
* **Landing Page**: Static HTML with advanced animations

## 📈 Performance Metrics

* **94%** Bot detection accuracy
* **Sub-second** Event streaming latency
* **Parallel** Agent processing
* **99.999%** Uptime via Solace guarantees

## 🎮 Live Demo

Visit our landing page at [https://s1gnal-zero.github.io](https://s1gnal-zero.github.io)

### Dashboard Overview

The S1GNAL.ZERO dashboard provides a **real-time system-wide view** of viral trend manipulation across the internet. This public feed showcases:

#### System Metrics (Top Row)

* **Average Bot Detection**: Aggregated bot percentage across all platform analyses
* **Median Analysis Time**: System-wide processing speed performance
* **Active Data Sources**: Number of connected APIs and data feeds

#### Reality Score™ Gauge

* **Live Aggregate Score**: Combined authenticity rating of recent system activity
* **Trend Indicators**: Real-time detection of bot surges, paid promotions, and review clusters
* **Visual Feedback**: Color-coded gauge (red/yellow/green) showing overall manipulation levels

#### Latest Flags Feed

* **Multi-Subject Monitoring**: Real-time feed of analyses across different products, influencers, and stocks
* **Community Intelligence**: See what other users are investigating (Stanley Cup tumblers, meme stocks, viral claims)
* **Pattern Detection**: Instant visibility into coordinated manipulation campaigns as they emerge

This system-wide view demonstrates S1GNAL.ZERO's capability to monitor and analyze multiple viral trends simultaneously, providing transparency into the digital manipulation landscape. Individual users also have access to their personal analysis history and detailed reports based on their subscription tier.

### Example Analysis: Stanley Cup Tumbler

    Reality Score: 34%
    ├── 🤖 62% of engagement from accounts < 30 days old
    ├── 📈 Unnatural spike: 10,000% increase in 48 hours
    ├── 💰 127 undisclosed paid promotions detected
    └── ⭐ 73% of 5-star reviews posted within 3-day window

## 🏗️ Architecture

       Vaadin Web UI
            ↓ WebSocket
       Spring Boot App
            ↓ JCSMP
      ┌─────────────┐
      │ Solace      │ ← Event Broker
      │ PubSub+     │
      └─────┬───────┘
            ↓ Topics
      [Agent Mesh - Python]
      ├── Bot Detection Agent
      ├── Trend Analysis Agent  
      ├── Review Validator Agent
      └── Score Aggregator Agent
            ↓
        PostgreSQL

## 🚦 Getting Started

### Prerequisites

* Solace PubSub+ Broker (Docker or Cloud)
* Java 17+ (Spring Boot)
* Python 3.10+ (Agents)
* PostgreSQL 14+
* Maven 3.8+

### Installation

    # Clone the repository
    git clone https://github.com/S1GNAL-ZERO/S1GNAL-ZERO.github.io.git
    cd S1GNAL-ZERO
    
    # Start Solace PubSub+ Docker
    docker run -d -p 55555:55555 -p 8080:8080 -p 1883:1883 \
      --name=solace-pubsub solace/solace-pubsub-standard
    
    # Set up PostgreSQL database
    createdb signalzero
    psql signalzero < database/schema.sql
    
    # Configure environment
    export SOLACE_HOST="tcp://localhost:55555"
    export SOLACE_VPN="default"
    export SOLACE_USERNAME="admin"
    export SOLACE_PASSWORD="admin"
    export DB_URL="jdbc:postgresql://localhost:5432/signalzero"
    
    # Start Spring Boot backend
    cd backend
    mvn spring-boot:run
    
    # Start Python agents
    cd ../agents
    pip install -r requirements.txt
    python start_all_agents.py
    
    # Access the application
    open http://localhost:8080

## 📡 Solace Integration

S1GNAL.ZERO leverages Solace PubSub+ for:

* **Event-Driven Architecture**: All analysis requests flow through Solace topics
* **Guaranteed Delivery**: Persistent messaging ensures no analysis is lost
* **Agent Mesh**: Seamless communication between Java services and Python agents
* **Real-Time Updates**: Live streaming of analysis progress
* **Scalability**: Handle viral traffic spikes without infrastructure changes

### Topic Structure

    signalzero/analysis/request/{userId}/{analysisId}
    signalzero/agent/bot-detector/request
    signalzero/agent/bot-detector/response
    signalzero/agent/trend-analyzer/request
    signalzero/agent/trend-analyzer/response
    signalzero/updates/score/{analysisId}
    signalzero/usage/analysis/{userId}

## 💰 Monetization Model

### Usage-Based Freemium Strategy

S1GNAL.ZERO implements a **usage-based freemium model** that balances public transparency with private insights:

#### Access Levels

**1. Public View (No Account)**

* **Full access** to system-wide dashboard showing real-time manipulation detection
* **View only** - cannot run personal analyses
* **Purpose**: Build trust and create urgency by showing live detection capabilities

**2. Authenticated Users (Account Required)**

* **Personal dashboard** with analysis history
* **Usage-based limits** enforced via Solace events
* **Automatic blocking** when monthly quota exceeded

### Subscription Tiers

| Tier | Price | Monthly Analyses | Features | Use Case |
| --- | --- | --- | --- | --- |
| **PUBLIC** | Free | 0 (View Only) | Live dashboard, community feed | Awareness & lead generation |
| **FREE** | $0  | 3   | Basic Reality Score only | Trust building & proof of value |
| **PRO** | $99/mo | 100 | Detailed reports, API access, 90-day history | Individual power users |
| **BUSINESS** | $499/mo | 1,000 | Team seats (5+), priority queue, 1-year history | Marketing teams & agencies |
| **ENTERPRISE** | Custom | Unlimited | Dedicated Solace queue, SLA, white-label | Large organizations |

### How It Works

The system tracks usage in real-time via Solace events:

    fomokiller/usage/analysis/{userId}        # Track each analysis
    fomokiller/usage/limit-reached/{userId}   # Block when limit hit
    fomokiller/subscription/upgraded/{userId} # Unlock on payment

When users hit their limit:

1. Analysis request is **blocked** at the service level
2. User sees upgrade prompt with clear value proposition
3. Payment instantly unlocks continued access
4. Monthly usage resets automatically

### Revenue Psychology

1. **Public Dashboard** → Creates FOMO ("What's manipulating MY interests?")
2. **Free Tier** → Proves value with 3 analyses (enough to trust, not enough to depend on)
3. **Usage Limits** → Fair, transparent pricing based on actual needs
4. **Detail Gating** → Free users see the score, paid users see the evidence

### Key Differentiators

* **No feature degradation** - All tiers get same AI quality
* **Volume-based pricing** - Pay for how much you analyze, not what you analyze
* **Transparent limits** - Clear usage tracking visible in UI
* **Instant upgrades** - No waiting period, immediate access upon payment

## 🤝 Team

Built with ❤️ by the S1GNAL.ZERO team at AGI Ventures Canada Hackathon 3.0

### Project Creator

**Shawn Jackson Dyck** - Leader behind the build

* Email: [shawn@samjdtechnologies.com](mailto:shawn@samjdtechnologies.com)
* GitHub: [@samjd-zz](https://github.com/samjd-zz)
* Known for: [Answer42](https://github.com/samjd-zz/answer42)

### Event Organizers

* Hai
* Sukhpal Saini
* Kaan UN
* Neilda Pacquing Gagné
* Thoufeek Baber
* Susan Habib

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

* **[Solace](https://solace.com)** for sponsoring and providing PubSub+ platform
* **[AGI Ventures Canada](https://lu.ma/ai-tinkerers-ottawa)** for organizing the hackathon
* The open source community for inspiration

## 📞 Contact

* **Website**: [https://s1gnal-zero.github.io](https://s1gnal-zero.github.io)
* **Email**: [s1gnal.zero.42@gmail.com](mailto:s1gnal.zero.42@gmail.com)
* **GitHub**: [@S1GNAL-ZERO](https://github.com/S1GNAL-ZERO)
* **Event**: [AGI Ventures Canada](https://lu.ma/ai-tinkerers-ottawa)

* * *

<div align="center">

**Detecting truth in digital noise, one signal at a time.**

*S1GNAL.ZERO - Because authenticity matters in the age of virality.*

</div>
