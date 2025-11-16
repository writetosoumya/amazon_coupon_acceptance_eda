# amazon_coupon_acceptance_eda
To analyze and predict the coupon acceptance pattern and behavior of Amazon delivery drivers. 
# Coupon Acceptance EDA

### Practical Application 1 – Machine Learning Fundamentals (UC Berkeley ML/AI Program)

This project explores **customer behavior in accepting driving coupons** based on contextual factors like weather, passenger type, time of day, and destination.  
It applies **Exploratory Data Analysis (EDA)**, statistical summarization, and data visualization techniques using Python (Pandas, Matplotlib, and Seaborn).

---

## Objective
To answer the question:  
> “Will a customer accept the coupon?”

By analyzing 12,000+ survey responses from the UCI Machine Learning Repository, this project identifies behavioral patterns and actionable insights that influence coupon acceptance.

---

## Dataset
- **Source:** [UCI Machine Learning Repository – In-Vehicle Coupon Recommendation](https://archive.ics.uci.edu/ml/datasets/in-vehicle+coupon+recommendation)
- **Size:** ~12,684 records  
- **Target Variable:** `Y` (1 = accepted, 0 = rejected)  
- **Coupon Types:**
  - Bar  
  - Coffee House  
  - Carry-out & Take-away  
  - Restaurant (< $20)  
  - Restaurant ($20–$50)

---

## Tools & Libraries
- **Language:** Python 3  
- **Libraries:**  
  - `pandas` – data cleaning & summarization  
  - `numpy` – numeric analysis  
  - `matplotlib` & `seaborn` – data visualization  
  - `scipy` – probability & distribution analysis  

## Analyses Performed

### 1. Exploratory Data Analysis (EDA)
- Loaded, inspected, and cleaned the dataset  
- Converted categorical data into meaningful numeric groups  
- Analyzed distribution of `temperature`, `weather`, `time`, and `destination`  

### 2. Coupon-Specific Investigations
#### Bar Coupons
- Acceptance higher for adults (age > 25) who visit bars > 1–3 times/month  
- Social context (no kids, not widowed) strongly increases acceptance  
- Lifestyle segmentation showed highest acceptance among socially active groups

####  Coffee House Coupons
- Acceptance peaks between **10 AM – 2 PM**, especially with **friends or partners**  
- Insight: Works best as a mid-day, social offer

####  Restaurant (< $20) Coupons
- Highest acceptance among **lower-income** drivers (< $50K)  
- Frequent diners (4+ visits/month) most responsive  
- Insight: Impulse and budget-friendly coupon type

#### Carry-Out & Take-Away Coupons
- Acceptance highest on **sunny days** and around **lunch hours (10 AM–2 PM)**  
- Insight: Works when people are already out and hungry

#### Restaurant ($20–$50) Coupons
- **Longer expiration (1 day)** drives higher acceptance than 2 h coupons  
- **“No Urgent Place”** destinations show higher conversion  
- Insight: Planned dining behavior needs flexible timing

---

## Visualizations
- Histograms for continuous variables (`temperature`, `age`)  
- Bar charts for categorical features (`coupon`, `time`, `weather`, `destination`)  
- Comparative plots for acceptance rates across coupon categories  

All plots were created using `matplotlib` and `seaborn` and appear inline in `prompt.ipynb`.

---

## Key Insights
| Factor | Behavior |
|--------|-----------|
| **Time of day** | Morning–afternoon (10 AM–2 PM) increases acceptance |
| **Passenger** | Friends/partners raise acceptance; kids lower it |
| **Weather** | Sunny days slightly increase response rates |
| **Income** | Lower-income groups favor low-cost coupons |
| **Expiration** | Longer (1 day) benefits planned spending |

---

##  Recommendations
1. **Target context, not just demographics:** Match coupon type to time, passenger, and trip purpose.  
2. **Push short-term coupons** (coffee/carry-out) during active daytime hours.  
3. **Use longer expiration** for planned, higher-value coupons (restaurants $20–$50).  
4. **Segment customers** by lifestyle frequency (e.g., bar visits, dining frequency).  

---

## Repository Structure
coupon-acceptance-eda/
├── data/
│ └── coupons.csv
├── images/
│ └── (optional plots)
├── prompt.ipynb # main Jupyter notebook with analysis
└── README.md # project overview

## How to Run
1. Clone this repository  
   ```bash
   git clone https://github.com/<your-username>/coupon-acceptance-eda.git
   cd coupon-acceptance-eda
2. Install dependencies if needed
   pip install pandas numpy matplotlib seaborn
3. Launch Jupyter Notebook
   jupyter notebook prompt.ipynb
4. Run all cells sequentially

## License
This project is for educational purposes as part of UC Berkeley’s ML/AI Professional Program.
Dataset © UCI Machine Learning Repository.
## Author
Soumyamol Vijayamma Surendran
UC Berkeley ML/AI Program – Practical Application 1
📧 [ writetosoumya@gmail.com)]
🌐 https://github.com/<writetosoumya>
