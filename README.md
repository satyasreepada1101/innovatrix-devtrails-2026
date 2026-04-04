# 🛡️ Swizo 
### Parametric Income Protection for Gig Workers in the Food Delivery Segment  

**Guidewire DEVTrails 2026**  
**Team: Innovatrix**  
**Amrita School of Engineering, Bengaluru**

---

## 🚀 Phase 2 Evolution
We have shifted from ideation to an operational engine. **Swizo** is now a fully autonomous, executable **Parametric Insurance Platform** that:
- Actively manages policies  
- Executes **Zero-Touch claims in real-time**  
- Dynamically scores **rider reliability (Trust Rating System)**  

---

## 🎯 The Core Focus: Autonomous Protection

In the current economy, a **"No-Work" day = "No-Pay" day**.  
Traditional insurers fail to cover micro-losses due to high administrative costs.

### ✅ Our Solution: Pure Automation
Swizo provides **Zero-Touch Parametric Insurance**:
- Continuously monitors external data (APIs + sensors)  
- Detects income disruption events  
- Automatically processes payouts  
- Directly deposits compensation into the rider’s wallet  

**No paperwork. No claims. No delays.**

---

## ⚙️ Executable Features (Phase 2)

- 🟢 **Live Policy Management**  
  Secure Rider ID login with real-time policy activation  

- 📈 **Dynamic Risk & Pricing**  
  Premiums calculated using hyper-local actuarial risk  

- 🌍 **Live Environmental Polling**  
  Real-time data engine (`fetchMockEnvironmentData`) tracking:
  - Rainfall  
  - AQI  
  - External disruptions  

- ⭐ **Dynamic Rider Trust Rating**
  - Valid claim → **+0.1 trust score**
  - Spoof attempt → **-0.5 penalty**
  - Ensures long-term system integrity  

---

## 🚨 Automated Triggers & Demonstration Scenarios

### 🌧️ Scenario 1: Heavy Rainfall Alert
- **Trigger Check:** `precip_mm > 8` in rider’s zone  
- **System Action:** Auto-trigger `rare_hourly` payout  

---

### 🌫️ Scenario 2: Hazardous AQI
- **Trigger Check:** `AQI ≥ 300`  
- **System Action:** Validates rider → processes environmental claim  

---

### 🚧 Scenario 3: Civil Disruption (Protest/Riot)
- **Trigger Check:** Roadblocks / protests detected  
- **System Action:** Immediate unavoidable compensation payout  

---

## 🛡️ Anti-Spoofing & Fraud Prevention

To prevent GPS spoofing and coordinated fraud:

- ⏱️ **Activity & Temporal Consistency**  
  Matches timestamps with motion sensor data  

- 🔍 **validateAntiSpoof() Engine**
  - Detects anomalies in GPS patterns  
  - Rejects invalid claims  

- ⭐ **Dynamic Trust Penalty System**
  - Fraud detected → **-0.5 trust score**
  - Valid claim → **+0.1 trust score**

🚫 Suspicious users are flagged in the administrative ledger, protecting platform liquidity.

---

## 📊 Actuarial Model & Dynamic Pricing

### 🔢 Risk Calculation
Risk = Base Probability × Area Vulnerability Factor

- **Base Probability:** Historical likelihood of events  
- **Area Vulnerability:** Risk multiplier (e.g., flood-prone zones)

---

### 💰 Premium Equation
Weekly Premium = (Expected Max Payout × Adjusted Risk Likelihood) / (1 - Target Gross Margin)


✔️ Ensures:
- Liquidity pool solvency  
- Affordable pricing for workers  

---

## 💻 Tech Stack & Architecture

| Layer | Technology | Purpose |
|------|-----------|--------|
| Frontend | React Native (Expo) PWA | Browser-based rider interface |
| Backend / Logic | TypeScript Engine | Trigger engine, claims engine, trust system |
| Database | AsyncStorage + Mock DB | Persistent state & claim logs |
| APIs | Environmental Mock APIs | Simulated real-world conditions |

---

## 🎥 Deliverables & Links

- 🌐 **Live PWA App:** _[Insert Vercel/Expo link]_  
- 🎬 **Phase 2 Demo Video:** _[Insert YouTube link]_  
- 🎤 **Phase 1 Pitch Video:** (https://www.youtube.com/watch?v=jU6UIrdP0-U)_  

> 🎥 Watch our 2-minute demo showcasing:
> - Zero-Touch claim execution  
> - Environmental trigger detection  
> - Anti-spoofing trust engine  

---

## 👥 Team Innovatrix

**Amrita School of Engineering, Bengaluru**

- **Laavya Sri Paruchoori** — Team Leader  
- **Kalyani Deepu Narayanan** — Member  
- **K Deepti** — Member  
- **Gandrala Venkata Satya Sreepada** — Member  
- **Ishaan Balakrishna Duddi** — Member  

---

## 📌 Summary

Swizo transforms insurance from a **reactive model** into a **fully autonomous financial safety net**, ensuring gig workers are protected in real-time — without friction.

---
