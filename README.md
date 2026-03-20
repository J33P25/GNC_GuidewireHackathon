# Guidewire DEVTrails 2026  
## GigGuard AI Solutions  
### Phase 1: Ideation & Foundation  

---

## 1. Project Overview  

GigGuard AI is an AI-driven, hyper-local parametric insurance solution designed to capture the untapped ₹45,000 Crore Indian Gig Insurance Market. Unlike traditional motor or health insurance, GigGuard AI focuses on Income Loss Protection for gig workers. By leveraging real-time telemetry—weather, traffic, and platform outages—it automates payouts to delivery partners when external "Force Majeure" events prevent them from hitting critical income milestones.

---

## 2. Problem Statement  

In the 2026 gig economy, a worker's income is digitally tracked per task, with a base fee and distance pay credited to their app wallet instantly after each delivery. However, the most critical portion of their earnings often up to 40% is locked behind Daily Milestone Bonuses that require completing a high volume of orders within a single day.  

This creates a "double-or-nothing" scenario where a rider may work 10 hours, but if for example a sudden two-hour flood or a "Wet Bulb" heatwave hits, they miss the final orders needed for the bonus, effectively losing their entire profit margin for the day.  

This "Incentive Gap" forces workers into a cycle of physical exhaustion and financial instability, as they must pay for their own fuel and bike maintenance regardless of whether they hit their targets. While the Indian government has introduced the Social Security Fund and the e-Shram portal to provide basic accident and health insurance, these traditional safety nets do not cover the "economic Force Majeure" of missed bonuses.  

Our project, GigGuard AI, solves this by using real-time API triggers to detect environmental or social disruptions, pushing an instant Resiliency Payout to the worker's UPI the moment a milestone becomes mathematically unreachable.

---

## 3. Incentive Gap  

| Category        | Trigger                     |
|----------------|---------------------------|
| Environmental  | Wet Bulb Heat-Stress      |
| Environmental  | Severe AQI/Pollution      |
| Social         | Sudden Strikes/Bandhs     |
| Technical      | Platform/EV Outage        |
| Operational    | Phantom Orders            |
| Infrastructure | Gridlock/Road Damage      |

---

## 4. Methodology  

### Wet Bulb Heat-Stress  

**Tech Methodology:**  
- Trigger: Backend polls the OpenWeather API every 15 minutes.  
- Condition: If the Wet Bulb Temperature (combined heat and humidity) crosses >35°C in the rider’s active 2km grid for more than 1 hour.  

**Worker’s Profit:**  
- They are financially compensated for forced downtime. Instead of risking a heatstroke to hit their 25-order milestone, they get a pro-rated income floor deposited instantly, protecting their day's wages.  

**Company Profit:**  
- Extreme heat is highly predictable weeks in advance. The Predictive Pricing ML automatically raises the weekly premium in hot cities before summer hits. By pricing the risk perfectly, the startup always collects more in premiums than it pays out in heat claims.  

---

### Severe AQI / Pollution  

**Tech Methodology:**  
- Trigger: Integration with AQICN or OpenWeather Pollution APIs.  
- Condition: PM2.5 levels push the AQI over 450 (Hazardous) in the worker’s zone.  

**Worker’s Profit:**  
- Empowers the worker to log off during toxic smog without falling into debt or missing rent. It converts a physical health hazard into financial safety.  

**Company Profit:**  
- Smog is highly localized (e.g., Delhi in November). While the startup might pay out claims in Delhi for one week, the millions of gig workers in clean-air cities (like Mysore, Kochi, or Pune) are still paying their ₹25 weekly premiums and claiming nothing. This creates massive Asymmetric Risk Pooling profit.  

---

### Sudden Strikes / Bandhs  

**Tech Methodology:**  
- Trigger: Dual-validation. First, an NLP AI (BERT) scans local news and Twitter/X for keywords like "Strike," "Bandh," or "Riot" in the worker's city.  
- Second: Google/TomTom Traffic APIs confirm that vehicle flow in commercial zones has flatlined to 0.  

**Worker’s Profit:**  
- Shields the worker from political volatility. If a local strike shuts down pickup locations, their expected milestone bonus is pro-rated and saved.  

**Company Profit:**  
- Strikes are sudden but incredibly rare. The startup collects the "Social Disruption" portion of the weekly premium 52 weeks a year, but only pays it out maybe once or twice a year. The margin on this specific coverage is near 95%.  

---

### Platform / EV Outage  

**Tech Methodology:**  
- Trigger: A server-ping script checks the status of Swiggy/Zepto partner servers or EV battery APIs (like Yulu/Zypp).  
- Condition: Returns a 503 Service Unavailable or Timeout for >45 minutes.  

**Worker’s Profit:**  
- Monetizes "Dead Time." If the billionaire tech company's app crashes, the worker doesn't suffer. They get paid for the hour they sat on the sidewalk waiting for the app to come back online.  

**Company Profit:**  
- Tech companies have 99.9% uptime Service Level Agreements (SLAs). Outages almost never happen. Offering this coverage makes the insurance look incredibly attractive to the worker, driving massive user acquisition, while costing the startup almost nothing in actual payouts.  

---

### Phantom Orders / Fake Orders  

**Tech Methodology:**  
- Trigger: API sync with the delivery platform (mocked for the hackathon).  
- Condition: Validates that the worker's GPS shows they traveled >5km to a customer, but the order status was flagged as "Customer Unreachable / Fake Order."  

**Worker’s Profit:**  
- Recovers their wasted fuel money and time instantly. They don't have to fight with Swiggy support for a ₹30 cancellation fee.  

**Company Profit:**  
- This is where your Intelligent Fraud AI makes you money. If a rider claims "Phantom Orders" three times in a week, the AI flags them as a scammer. It automatically drops their "Resiliency Score," denies the claim, and increases their premium. The startup actively protects its money from bad actors.  

---

### Gridlock / Road Damage (Infrastructure)  

**Tech Methodology:**  
- Trigger: TomTom Traffic API merged with the worker’s live state.  
- Condition: Average speed in the zone is 5km/h for 60 mins, and the worker's API status is strictly set to "On Active Delivery."  

**Worker’s Profit:**  
- Maximizes their net income. Traffic jams are the #1 reason workers miss their daily bonus targets. This trigger ensures that the 1 hour lost in traffic is compensated, keeping their daily ₹600 bonus in reach.  

**Company Profit:**  
- Strict state-validation prevents fraud. If the worker is sitting in a traffic jam but isn't on an active order (e.g., just drinking tea on a busy street), the system rejects the claim. Furthermore, these are "micro-payouts" (e.g., ₹40 for lost time). Paying out tiny amounts builds immense brand trust, causing the worker to renew their subscription for years (High Lifetime Value).  

---

## 5. Tech Stack & Platform Justification  

### Parametric Triggers  

- Wet Bulb Heat Stress: OpenWeather API polled every 15 minutes; payout triggers if wet bulb temperature exceeds 35°C for 1 hour in the rider’s 2 km grid.  
- Severe AQI / Pollution: OpenWeather Pollution API triggers when AQI > 450 (Hazardous) in the worker’s zone.  
- Sudden Strikes: NLP model scans news platforms and Twitter/X, then confirms traffic collapse using Google/TomTom Traffic APIs.  
- Gridlock / Road Damage: TomTom Traffic API detects average speed <5 km/h for 60 minutes while rider status is Active Delivery.  

---

### Platform Choice  

A lightweight web application ensures zero installation friction, easy accessibility on low-storage phones, and instant updates without requiring users to download new versions.  

---

### Tech Stack  

- Frontend: React.js + Tailwind CSS  
- Backend: Python FastAPI (handles trigger validation and APIs)  
- Database: PostgreSQL  
- ML Intelligence: Scikit-learn, TensorFlow, Regression algorithm, DBSCAN, NLP  
- APIs: OpenWeather, Google/TomTom Traffic, Delivery Platform, Geolocation  
