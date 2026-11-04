# 🍽️ Zomato Restaurant Analysis – Power BI Dashboard

An interactive 5-page Power BI dashboard that analyses restaurants across countries and cities: where they are, how they are rated, what cuisines and services they offer, and what they cost.

📌 **Business Problem**

A food-discovery platform wants to understand its restaurant listings. The dashboard answers:

1. Where are the restaurants located (continent, country, city)?
2. How are restaurants rated, and which ones are highly rated?
3. Which cuisines are most common, and which restaurants offer the widest variety?
4. How many restaurants offer Online Delivery and Table Booking?
5. What is the average cost for two, and how does it vary by place?

📂 **Dataset**

* Zomato restaurant dataset
* Size: 9,551 restaurants
* Main fields: Restaurant ID, Restaurant Name, Address, City, Country, Cuisines, Average Cost for two, Currency, Has Table booking, Has Online delivery, Price range, Aggregate rating, Rating text, Votes, Latitude, Longitude

🛠️ **Tools Used**


* Power BI Desktop
* Power Query
* DAX

🧹 **Data Preparation**

* Combined the continent-wise restaurant files and joined them to the fact table (cost, rating, services, votes) using Restaurant ID
* Split the combined Restaurant Name,Address column into Restaurant Name and Address (split at the first comma only)
* Created a Cuisines Count column (number of cuisines per restaurant)
* Created a Service Availability column (Both / Online delivery only / Table booking only / Neither)
* Treated rating 0 ("Not rated") separately so it does not lower the average rating
* Used Price range for comparisons, because costs are in different currencies.

📊 **Dashboard Pages**

1. Global Overview	KPI cards (Total Restaurants, Cities, Countries, Average Rating), map of restaurants, restaurants by continent and by country.
2. Rating Analysis	Restaurants by rating category, High Rated Restaurants, table of restaurants with ratings and votes.
3. Cuisine Analysis	Distinct cuisines, cuisines per restaurant, restaurants by cuisine, restaurants offering the most cuisines.
4. Service Analysis	Online Delivery Restaurants, Table Booking Restaurants, restaurants offering both, service availability chart.
5. Cost Analysis	Average Cost for Two, cost by city and country with currency.

**Filters on every page:** Has Online delivery · Has Table booking · Aggregate rating · Price range

**Screenshots**

* Rating Analysis
* Cuisine Analysis
* Service Analysis
* Cost Analysis

📐 **Key KPIs**

* Total Restaurants
* Average Rating
* High Rated Restaurants
* Distinct Cuisines
* Online Delivery Restaurants
* Table Booking Restaurants
* Both Services
* Average Cost for Two

🔍 **Key Insights**

* Service availability: Of 9,551 restaurants, 2,451 (25.7%) offer online delivery and 1,158 (12.1%) offer table booking. Only 435 (4.6%) offer both, and 6,377 (66.8%) offer neither.
* Location: The data is heavily concentrated in India, which has about 90% of all restaurants (8,652 of 9,551).
* Cuisines (Asia): North Indian is the most common cuisine (about 45% of restaurants), followed by Chinese (about 31%) and Fast Food (about 22%).
* Premium cuisines: Mediterranean, European and Asian cuisines have the highest average ratings (3.9–4.0) and the highest price ranges, but fewer restaurants.
* Variety and ratings: Restaurants offering 4–6 cuisines tend to have higher ratings than those offering 1–2 cuisines.
* Data quality: About 24% of Asian restaurants are "Not rated", so rating averages should be read with care.

💡 **Recommendations**

* Grow delivery and booking: Two out of three restaurants offer neither service. Onboarding more restaurants to online delivery and table booking is the biggest opportunity.
* Promote under-served cuisines for delivery, especially those with very low delivery share.
* Highlight premium cuisines (Mediterranean, European, Asian) in recommendations, since they combine high ratings with high engagement.
* Encourage ratings: Nudge customers to rate restaurants so that far fewer listings remain "Not rated".
* Standardise currency in the data so that cost can be compared fairly across countries.

⚠️ **Limitations**

* Most records come from one country, so country comparisons are limited.
* Costs are in local currencies, so Average Cost cannot be compared directly across countries.
* The data is a snapshot and does not show trends over time.
