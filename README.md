# 🚗 Uber Trip Analysis | Power BI Dashboard

An interactive, three-page Power BI dashboard that analyzes Uber trips in New York for **June 2024**. It helps answer when demand peaks, where trips start and end, which vehicle types and payment methods are most used, and how trip distance and booking value vary.

---

## 🎯 Project Objective
To turn raw trip-level data (103.7K bookings) into a clear, interactive report that supports decisions on demand patterns, vehicle mix, payment preferences and location hotspots.

---

## 📊 Dashboard Pages

| Page | What it shows |
|------|---------------|
| **Overview Analysis** | KPI cards, payment type and day/night trip breakdown, vehicle type analysis, daily booking trend, location analysis |
| **Time Analysis** | Trip distance by pickup time, by day of week, and an hour-by-day heat map |
| **Details** | Trip-level table for drilling into individual bookings |

---

## 🔑 Key Metrics
- **103.7K** total bookings
- **$1.55M** total booking amount
- **$15** average booking value
- **3 miles** average trip distance
- **16 minutes** average trip time

---

## 💡 Key Insights
- **UberX** is the most booked vehicle type (about 38.7K bookings).
- **Uber Pay** accounts for roughly two-thirds of payments, with Cash making up most of the rest.
- **Manhattan** is the most frequent pickup point, and **Upper East Side North** is the most frequent drop-off point.
- Trip distance peaks in the **afternoon and early evening**, and is highest on **weekends**.
- The farthest trip recorded was **144.1 miles**, from Lower East Side to Crown Heights North.

---

## 🗂️ Data Model
A star schema with one fact table and two dimension tables:

- **Trip details** (fact table): trip ID, pickup and drop-off time, passenger count, trip distance, pickup and drop-off location IDs, fare amount, surge fee, vehicle and payment type
- **Dim_Location**: location ID, location (zone) and city (borough), based on the NYC TLC Taxi Zone Lookup
- **Calendar table**: date dimension for time analysis

The location table has two relationships to the fact table: an active one on pickup location and an inactive one on drop-off location, used in DAX with `USERELATIONSHIP`.

---

## 🧮 DAX Measures
- Total Booking, Total Booking Amount, Total Trip Distance
- Average Booking Value, Average Trip Distance, Average Trip Time
- Most Frequent Pickup Point and Most Frequent Drop-off Point
- Farthest Trip (pickup, drop-off and distance)

---

## ✨ Features
- Date range and city slicers
- Metric switcher (Total Booking, Total Booking Amount, Total Trip Distance)
- Page navigation and custom icons
- Cross-filtering between visuals

---

## 🖼️ Screenshots

### 🏠 Overview
![Overview](Overview-Report.png)

### ⏰ Time Analysis
![Time Analysis](Time-Analysis.png)

### 📋 Details
![Details](Details-Report.png)

---

## 📁 Repository Files
| File | Description |
|------|-------------|
| `Uber Trip Analysis - Power BI Dashboard.pbix` | The Power BI report |
| `Uber Trip Details.xlsx` | Trip data (fact table) |
| `Dim_Location.xlsx` | Location dimension table |

---

## 🛠️ Tools Used
Power BI Desktop · Power Query · DAX · Excel

---

## ▶️ How to Open
1. Download the `.pbix` file from this repository.
2. Open it in **Power BI Desktop** (free to download from Microsoft).
3. If Power BI asks for the data, point it to `Uber Trip Details.xlsx` and `Dim_Location.xlsx`.

---

## 👤 Author
**Maheshwaran M**
🔗 LinkedIn: [add your profile link here]
