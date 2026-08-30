

```markdown
# ♻️ EcoLoop AI
**AI-Powered Waste Triage & Intelligent Handoff Platform**

[![Made with Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
[![Built with Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)]()
[![AI by TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)]()

## 🚨 The Problem
Every day, citizens walk past public waste, hazardous materials, or illegal dumping. While they can report it, they cannot realistically pick it up, carry it, sort it, or sell it. Current systems fail because they tie the **burden of discovery** to the **burden of disposal**. 

## 💡 Our Core Innovation: "Scan & Leave"
EcoLoop AI solves this by separating waste discovery from waste handling. 
* **The Citizen:** SCAN → REPORT → LEAVE
* **The AI System:** UNDERSTAND → DECIDE → DISPATCH → VERIFY → REWARD

The citizen acts purely as a detector. The AI assesses the risk and routes the ticket to the correct municipal officer, local scrap collector, or specialized biohazard team. 

---

## ✨ Key Features

* **📷 Real-Time Hybrid Scanner:** A frictionless web interface using HTML5 Camera and Geolocation APIs. Citizens scan waste instantly without downloading a heavy native app.
* **🧠 Multi-Stage AI Classifier:** Powered by TensorFlow and MobileNetV2. It doesn't just guess waste types; it detects if bags are "sealed" and handles uncertainty gracefully without hallucinating contents.
* **⚠️ Risk & Action Engine:** Automatically flags hazardous waste (e.g., broken glass, medical waste) with strict "DO NOT TOUCH" instructions, dynamically matching the incident to handlers with the correct capabilities.
* **🗺️ Smart Route Optimizer:** A custom greedy nearest-neighbor algorithm using the Haversine formula. It generates optimized collection routes for handlers by weighting ticket priority, risk level, report age, and geographical proximity.
* **✅ Proof of Collection:** Handlers upload "after" photos with GPS timestamps to verify collection, triggering automated status updates and reward distribution.
* **🪙 EcoPoints Reward Economy:** Gamified wallets reward citizens *only* after a collection is verified, preventing spam and incentivizing genuine environmental impact.

---

## 🛠️ Technology Stack

**Frontend**
* HTML5, CSS3 (Custom Dark Glassmorphism UI)
* Vanilla JavaScript (Zero-dependency state management)
* Leaflet.js (Interactive mapping & route visualization)
* WebRTC / HTML5 Media & Geolocation APIs

**Backend & Database**
* Python 3
* Flask & Flask-RESTful
* SQLite (via Flask-SQLAlchemy ORM)
* Flask-JWT-Extended (Role-based authentication)

**AI & Algorithms**
* TensorFlow & MobileNetV2
* Custom Haversine-based Route Optimization Engine

---

## ⚙️ Local Installation & Setup

To run EcoLoop AI locally, you will need two terminal windows.

### 1. Backend Setup (Terminal 1)
```bash
# Clone the repository
git clone [https://github.com/yourusername/ecoloop-ai.git](https://github.com/yourusername/ecoloop-ai.git)
cd ecoloop-ai/backend

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the Flask API Server
flask --app app.py --debug run

```

*The backend will run on `http://127.0.0.1:5000*`

### 2. Frontend Setup (Terminal 2)

```bash
# Navigate to the frontend directory
cd ../frontend

# Start a local web server (requires Python)
python -m http.server 8000

```

*Open your browser and navigate to `http://localhost:8000*`

---

## 🚀 What's Next?

* **Predictive Hotspots:** Using historical ticketing data to predict where illegal dumping will occur next.
* **Dynamic Fleet Routing:** Upgrading our greedy algorithm to Google OR-Tools for enterprise-scale municipal fleet management.
* **Computer Vision Verification:** Comparing "before" and "after" photos algorithmically to fully automate the verification pipeline.

```

```
