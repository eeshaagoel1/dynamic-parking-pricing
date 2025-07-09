# 🚗 Real-Time Dynamic Parking Pricing System

This project builds a real-time pricing engine for urban parking lots using historical occupancy, traffic data, and competition intelligence.  
Implemented fully in Python with real-time streaming via Pathway and live visualization using Bokeh.

---

## 🧠 Models Implemented

### 1️⃣ Model 1: Occupancy-Based Linear Pricing
Price increases linearly based on occupancy.

### 2️⃣ Model 2: Demand-Based Pricing
Considers:
- Occupancy ratio
- Queue length
- Nearby traffic condition
- Vehicle type
- Special day

### 3️⃣ Model 3: Competition-Based Adjustment
Checks nearby parking lots within 0.5 km and adjusts the price slightly higher/lower based on competitors.

---

## ⚙️ Tech Stack Used

| Component | Description |
|----------|-------------|
| Python | Core logic (Pandas, NumPy) |
| Google Colab | Development platform |
| Pathway | Real-time data stream simulation |
| Bokeh + Panel | Live visualization |
| GitHub | Code hosting and submission |

---

## 🏗️ Architecture Flow

```mermaid
flowchart LR
    A[CSV Parking Data] --> B[Apply Model 1, 2, 3]
    B --> C[Save Final Dataset]
    C --> D[Stream Row-by-Row via Pathway]
    D --> E[Real-Time Pricing Output]
    E --> F[Bokeh Dashboard]
