# Synthetic Financial Data Generation Pipeline
## 📌 Project Objective
Enterprise AI models require massive datasets for training, but strict privacy laws (like GDPR) restrict the use of real customer records (PII). This project solves that bottleneck by generating a synthetic e-commerce dataset that perfectly mimics real-world statistical patterns and financial constraints without containing any real user data.
## ⚙️ The Tech Stack
* **Python 3.x**
* **Pandas:** For structuring the generated data into a manipulatable DataFrame and exporting to CSV.
* **Faker:** To generate highly realistic, randomized UUIDs and customer data.
## 💼 Business Logic & Financial Constraints
Machine learning engineers often randomize numerical data, which can lead to mathematically impossible scenarios (e.g., negative profit margins). This pipeline integrates strict commerce constraints:
1. **Margin Control:** The `Unit_COGS` (Cost of Goods Sold) is algorithmically constrained to always be 40% to 70% of the `Unit_Price`. This ensures the synthetic dataset maintains realistic gross margins and no mathematically impossible negative profits.
2. **Time-Series Realism:** Purchase timestamps are generated within a rolling 180-day window to simulate seasonal e-commerce pacing.
## 🚀 How to Run the Generator
1. Clone this repository to your local machine.
2. Ensure you have the required libraries installed:
   `pip install pandas faker`
3. Run the script:
   `python generate_data.py`
4. The script will output a `synthetic_ecommerce_data.csv` file containing 5,000 rows of clean, mathematically sound AI training data.
## 📊 Sample Output

| Order_ID | Customer_ID | Order_Date | Category | Quantity | Unit_Price | Unit_COGS | Total_Amount |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 5f3a... | 4921 | 2023-10-12 | Electronics | 2 | 299.50 | 149.75 | 599.00 |
| 9a2b... | 1104 | 2023-11-05 | Apparel | 5 | 45.00 | 22.50 | 225.00 |
