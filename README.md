# GigShield 🛡️

> **Parametric Income Protection for Gig Workers in the Food Delivery Segment**

**Guidewire DEVTrails 2026** | Team: Innovatrix | Amrita School of Engineering, Bengaluru

---

## 1. Requirement & Persona Scenarios

Our solution addresses the **Income Volatility of gig workers in the Food Delivery segment** (Zomato/Swiggy). In the current economy, a **"No-Work" day** due to external factors means a **"No-Pay" day**.

---

## 2. Persona & Scenarios

### Scenario 1 — Ravi, Swiggy Rider, Bengaluru
Ravi earns ₹600/day on average. On a Tuesday afternoon, rainfall exceeds 50mm/hr in his delivery zone (Koramangala). Orders drop to zero. GigShield detects the parametric trigger, validates Ravi's active status in that zone, and initiates a payout of **₹280** (proportional to lost hours) directly to his UPI ID — within **10 minutes**.

### Scenario 2 — Priya, Zomato Rider, Delhi
Delhi's AQI crosses 400 (Severe category). The government issues an outdoor advisory. Order volumes on Zomato drop 65% in Priya's zone. GigShield's AQI trigger fires, cross-references her GPS activity, and processes a **partial-day income protection payout** automatically.

### Scenario 3 — Arjun, Swiggy Rider, Mumbai
A sudden local bandh is declared in Dharavi. Arjun's GPS shows he is in the affected zone. GigShield's social disruption trigger cross-checks the **GDELT Project news API** for strike/protest keywords in his geofence, confirms zone-level order activity has dropped over 70%, and processes his payout **without Arjun filing anything**.

---

## 3. Workflow

1. **Onboarding:** Riders link their Delivery Partner ID and choose a weekly coverage tier.
2. **Weekly Subscription:** Based on next week's forecast, our AI suggests a dynamic premium (e.g., ₹28/week).
3. **Real-Time Monitoring:** Our backend pings Weather, AQI, and Social APIs every 15 minutes.
4. **Automatic Trigger:** When a disruption exceeds 2 continuous hours in a rider's geofence, a claim is initiated by the system, not the rider.
5. **Adversarial Verification:** Our AI-Multi-Factor engine verifies the rider's presence before payout.
6. **Instant Settlement:** Money is pushed to the worker's digital wallet via mock UPI.

---

## 4. Financial & Platform Strategy

### Weekly Premium Model

Gig workers operate on weekly cycles; we match this with three simple tiers:

| Coverage Tier | Weekly Premium | Max Weekly Payout |
|---------------|----------------|-------------------|
| Basic         | ₹29/week       | ₹300              |
| Standard      | ₹49/week       | ₹600              |
| Plus          | ₹79/week       | ₹1,000            |

### Parametric Triggers

| Trigger        | Data Source          | Threshold                          |
|----------------|----------------------|------------------------------------|
| Heavy Rainfall | OpenWeatherMap API   | > 15mm/hr in rider zone            |
| Extreme Heat   | OpenWeatherMap API   | Temp > 44°C                        |
| Severe AQI     | AQICN API            | AQI > 300 (Severe)                 |
| Social Strike  | GDELT / News Scraper | Zone orders drop > 70% for 2+ hrs  |

### Platform Choice: Progressive Web App (PWA)

We are building a **PWA (React/Tailwind)** for high agility:

- **Low Friction:** No app store downloads; accessible via simple link or QR.
- **No Deployment Delays:** Allows us to update the "Trigger Engine" instantly without waiting for App Store approvals.

---

## 5. AI/ML Integration

### 1) Dynamic Premium Calculation using Risk Regression
The system uses a regression-based risk scoring model to estimate the likelihood of income loss in a worker's delivery zone.

### 2) Predictive Disruption Forecasting (Proactive Protection)
A time-series forecasting model analyzes weather forecasts, pollution trends, and historical disruption patterns to predict potential income-loss events.

### 3) Intelligent Fraud Detection using Anomaly Detection
To prevent misuse of automated payouts, the platform employs AI-driven anomaly detection mechanisms.

### 4) Smart Income Loss Estimation Model
A regression-based payout estimation model calculates the actual income loss within the coverage tier limit.

---

## 6. Adversarial Defense & Anti-Spoofing Strategy

To counter **"Telegram Syndicates"** using GPS-spoofing to drain the liquidity pool, GigShield uses a **Multi-Factor Proof-of-Presence (PoP)** engine.

### A. Sensor Fusion (Beyond GPS)
- **Telemetry Analysis:** We analyze Accelerometer and Gyroscope data. A bike in a storm has a specific vibration signature; a spoofed phone on a bedside table is static.
- **Network Fingerprinting:** We cross-reference GPS with Cell Tower IDs and WiFi SSIDs. If the GPS says "Bandra" but the phone is on "Home_WiFi," the claim is flagged.

### B. Cluster Anomaly Detection
- **Syndicate Identification:** Our Isolation Forest model flags "Cluster Anomalies" — if 50 riders are perfectly still at the same coordinate while non-insured riders show normal movement, the group is flagged as a fraud ring.
- **Device Integrity:** The app detects "Mock Location" permissions or "Developer Options." If detected, the insurance shield is instantly deactivated.

### C. UX Balance for Honest Riders
- **Trust Scores:** High-performing riders with zero fraud flags get "Benefit of the Doubt" during network drops, with provisional payouts settled once pathing is verified.
- **Visual Proof:** In disputed cases, riders can upload a 5-second "Environment Video." Our AI matches the weather in the video to API timestamps.

---

## 7. Tech Stack + Development Plan

| Layer    | Technology            | Purpose                 | Justification                                               |
|----------|-----------------------|-------------------------|-------------------------------------------------------------|
| Frontend | React (PWA)           | Rider & Admin Interface | Fast development, cross-platform, no app install required.  |
| Backend  | Node.js + Express API | API & Business Logic    | Lightweight, real-time capable, and easy integration.       |
| AI/ML    | Python (Scikit-learn) | Risk & Fraud Engine     | Efficient for Anomaly Detection and Premium Calculation.    |
| Database | MongoDB               | Data Storage            | NoSQL flexibility for fast reads/writes of claims and earnings. |
| Payment  | Razorpay              | Simulated Transactions  | Reliable India-friendly UPI payout simulation.              |

### APIs & Core Integrations

| API Type | Provider             | Primary Use Case                                                         |
|----------|----------------------|--------------------------------------------------------------------------|
| Weather  | OpenWeatherMap       | Real-time rain and temperature monitoring for triggers.                  |
| Pollution| AQICN                | Air quality for health-based disruption payouts.                         |
| Traffic  | Google Maps Platform | Validating congestion and verifying rider movement.                      |
| Location | Google Play Services | GPS + Network validation to detect spoofing syndicates.                  |
| Platform | Custom (Simulated)   | Mocked Zomato/Swiggy APIs for orders and earnings data.                  |

---

## 8. Business Viability (The "Unicorn" Perspective)

Traditional insurers cannot process small claims because **manual administration costs exceed the claim value**. GigShield reduces **Administrative Costs by 90%** through pure automation. By solving the **"GPS Spoofing" crisis**, we ensure the sustainability of the liquidity pool, making us a high-tier candidate for **IPO**.

---

## 9. Team

| Name                            | Role        |
|---------------------------------|-------------|
| Laavya Sri Paruchoori           | Team Leader |
| Kalyani Deepu Narayanan         | Member      |
| K Deepti                        | Member      |
| Gandrala Venkata Satya Sreepada | Member      |
| Ishaan Balakrishna Duddi        | Member      |

**University:** Amrita School of Engineering, Bengaluru

---

## 10. Links

| Resource           | Link            |
|--------------------|-----------------|
| GitHub Repository  | https://github.com/satyasreepada1101/innovatrix-devtrails-2026 |
| Phase 1 Demo Video | https://www.youtube.com/watch?v=jU6UIrdP0-U |
| Try It Out Link  | https://devtrails2026frontend.vercel.app/ |

---

*Built for Guidewire DEVTrails 2026 — Unicorn Chase. Seed. Scale. Soar.*
