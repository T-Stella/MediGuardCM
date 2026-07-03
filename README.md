# MediGuardCM
## Blockchain-Enabled Pharmaceutical Verification System for Cameroon

### 📋 Overview
MediGuardCM is a comprehensive blockchain-based solution designed to combat 
substandard and falsified medicines in Cameroon. The system addresses the 
critical "Paper Gap" in Cameroon's National Pharmaceutical Traceability System 
(NPTS) by providing:

- ✅ **GS1-compliant drug verification** via mobile app
- 📱 **USSD/SMS module** for 58.1% offline population
- 💾 **Offline Verification Vault** for rural areas
- 🔗 **DHIS2 interoperability** for real-time surveillance
- 📊 **Adverse Drug Reaction (ADR) reporting**

### 🎯 Problem Statement
- **369.8 million CFA** worth of counterfeit drugs seized (Jan-June 2025)
- **8.69 billion CFA** cumulative seizures since 2020
- **14 data units per district** still use manual paper forms
- **2-year reporting delays** → counterfeit batches kill before detection
- **45% of health platforms** cannot interoperate with DHIS2
- **58.1% of Cameroonians** have no internet access

### 🏗️ Architecture
┌─────────────────────────────────────────────────────────────┐
│ MEDIGUARDCM SYSTEM │
├─────────────────────────────────────────────────────────────┤
│ ┌─────────────┐ ┌──────────────┐ ┌──────────────────┐ │
│ │ Blockchain │ │ Verification │ │ USSD/SMS Module │ │
│ │ Backend │◄─┤ Client │──┤ (*123#) │ │
│ │ (Immutable) │ │ (Mobile) │ │ (Offline) │ │
│ └─────────────┘ └──────────────┘ └──────────────────┘ │
│ │ │ │ │
│ └───────────────┼────────────────────┘ │
│ ▼ │
│ ┌─────────────────────┐ │
│ │ Offline Vault │ │
│ │ (Cached Batches) │ │
│ └─────────────────────┘ │
│ │ │
│ ▼ │
│ ┌─────────────────────┐ │
│ │ DHIS2 Integration │ │
│ │ (HL7/FHIR API) │ │
│ └─────────────────────┘ │
└─────────────────────────────────────────────────────────────┘

### 🛠️ Technical Stack
| Component | Technology |
|-----------|------------|
| Backend | Node.js + Express (or Python Flask) |
| Frontend | React.js (Web) / React Native (Mobile) |
| Blockchain | Permissioned (simulated with cryptographic hashing) |
| Database | PostgreSQL + Redis (caching) |
| APIs | GS1 Lightweight Messaging (JSON), HL7/FHIR |
| Offline | Local storage + cryptographic signing |

### 📊 Project Timeline
- **Week 1**: Design & Setup (Current)
- **Week 2**: Core Prototype Development
- **Week 3**: Features & Integration
- **Week 4**: Testing & Documentation

### 👥 Target Stakeholders
1. **Ministry of Public Health** - Regulatory oversight
2. **CENAME** - National procurement
3. **Pharmaceutical Manufacturers** - Product registration
4. **Pharmacies & Distributors** - Verification points
5. **Consumers** - End users

### 📈 Expected Impact
- Reduce counterfeit drug consumption
- Enable real-time market surveillance
- Empower consumers at point of purchase
- Bridge the "Paper Gap"
- Achieve 45% interoperability with DHIS2

### 🚀 Getting Started

#### Prerequisites
- Node.js v18+ or Python 3.9+
- Git
- VS Code (recommended)

#### Installation
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/MediGuardCM.git
cd MediGuardCM

# Backend setup
cd backend
npm install   # or pip install -r requirements.txt

# Frontend setup
cd ../frontend
npm install

# Run development servers
# Backend: npm start (port 5000)
# Frontend: npm start (port 3000)
📝 License
MIT

👤 Author
Tabe Stella - tabestella86@gmail.com - IUG

### Step 1.5: Push Initial Code

```bash
# Add all files to git
git add .

# Commit the changes
git commit -m "Initial project setup: create repository structure and README"

# Push to GitHub
git push origin main