# 🚀 GigGuard – Income Protection for Gig Workers

## 📌 Problem Statement
Gig workers in the food delivery sector (Zomato/Swiggy) face **income volatility**.  
A “No-Work” day due to external factors (weather, pollution, strikes) means a **“No-Pay” day**.

---

## 🎯 Solution Overview
**GigGuard** is a parametric income protection system that:
- Detects disruptions automatically
- Verifies rider presence
- Instantly compensates for lost income

---

## 👤 Persona & Scenarios

### 🧍 Ravi – Swiggy Rider (Bengaluru)
- Avg income: ₹600/day  
- Heavy rainfall (>50mm/hr) → Orders drop to zero  
- ✅ GigGuard triggers payout: **₹280 within 10 minutes**

---

### 🧍 Priya – Zomato Rider (Delhi)
- AQI > 400 (Severe) → Govt advisory  
- Orders drop by 65%  
- ✅ Automatic **partial-day income protection payout**

---

### 🧍 Arjun – Swiggy Rider (Mumbai)
- Local bandh in Dharavi  
- Orders drop >70%  
- ✅ System verifies via news + GPS → **Automatic payout**

---

## ⚙️ Workflow

1. **Onboarding**  
   - Link Delivery Partner ID  
   - Choose coverage tier  

2. **Weekly Subscription**  
   - AI suggests premium (e.g., ₹28/week)

3. **Real-Time Monitoring**  
   - APIs checked every 15 minutes  

4. **Automatic Trigger**  
   - Disruption >2 hours → Claim initiated  

5. **Verification**  
   - Multi-factor presence validation  

6. **Instant Settlement**  
   - UPI payout to rider  

---

## 💰 Financial Model

### 📊 Weekly Premium Plans

| Tier      | Weekly Premium | Max Weekly Payout |
|----------|---------------|-------------------|
| Basic    | ₹29           | ₹300              |
| Standard | ₹49           | ₹600              |
| Plus     | ₹79           | ₹1000             |

---

## ⚡ Parametric Triggers

| Trigger          | Data Source            | Threshold                     |
|------------------|----------------------|------------------------------|
| Heavy Rainfall   | OpenWeatherMap API   | > 15 mm/hr                   |
| Extreme Heat     | OpenWeatherMap API   | Temp > 44°C                  |
| Severe AQI       | AQICN API            | AQI > 300                    |
| Social Strike    | GDELT / News API     | Orders drop > 70% (2+ hrs)   |

---

## 🌐 Platform Choice

### Progressive Web App (PWA)
Built using **React + Tailwind**

- ✅ No app installation required  
- ✅ Instant updates (no app store delays)  
- ✅ Accessible via link or QR  

---

## 🤖 AI/ML Integration

1. **Dynamic Premium Calculation**
   - Regression-based risk scoring

2. **Predictive Disruption Forecasting**
   - Time-series models for early detection

3. **Fraud Detection**
   - Anomaly detection algorithms

4. **Income Loss Estimation**
   - Regression-based payout calculation

---

## 🛡️ Anti-Fraud & Security (GigShield)

### 🔍 Multi-Factor Proof of Presence (PoP)

#### A. Sensor Fusion
- Accelerometer & Gyroscope analysis  
- Network fingerprinting (WiFi + Cell towers)

#### B. Cluster Anomaly Detection
- Detects fraud syndicates using Isolation Forest  
- Flags unusual group behavior  

#### C. Device Integrity
- Detects mock location & developer mode  
- Disables coverage instantly  

---

## ⚖️ UX for Honest Riders

- ⭐ Trust Scores for reliable users  
- 🎥 Optional 5-sec environment video for disputes  
- ⚡ Provisional payouts for network issues  

---

## 🧑‍💻 Tech Stack

| Layer     | Technology              | Purpose                     |
|----------|------------------------|-----------------------------|
| Frontend | React (PWA)            | Rider & Admin UI           |
| Backend  | Node.js + Express      | API & business logic       |
| AI/ML    | Python (Scikit-learn)  | Risk & fraud engine        |
| Database | MongoDB                | Data storage               |
| Payment  | Razorpay               | UPI simulation             |

---

## 🔗 APIs & Integrations

| API Type   | Provider              | Use Case                          |
|------------|----------------------|----------------------------------|
| Weather    | OpenWeatherMap       | Rain & temperature triggers      |
| Pollution  | AQICN               | AQI monitoring                   |
| Traffic    | Google Maps         | Movement validation              |
| Location   | Google Play Services | GPS + network verification       |
| Platform   | Custom APIs         | Orders & earnings simulation     |

---

## 📈 Business Viability

- 🚀 Reduces administrative costs by **90%**
- 🤖 Fully automated claim processing
- 🔐 Solves GPS spoofing fraud problem
- 💡 Scalable & sustainable model
- 🦄 Strong potential for **IPO-level growth**

---

## 🏁 Conclusion

GigGuard ensures that gig workers:
- Don’t lose income due to uncontrollable factors  
- Receive **instant, fair, and automated payouts**  
- Are protected with **AI-powered fraud prevention**

---

## 📎 Reference
Based on project document:  
:contentReference[oaicite:0]{index=0}
