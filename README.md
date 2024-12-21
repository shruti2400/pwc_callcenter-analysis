# 📢 Call Center Dashboard Project

## **Problem Statement**
The goal of this project is to create a Power BI dashboard for the Call Center Manager that displays all relevant Key Performance Indicators (KPIs) and metrics derived from the dataset. This dashboard will assist the manager in monitoring performance, identifying trends, and making data-driven decisions.

### **Key Performance Indicators (KPIs)**
- 📈 **Overall Customer Satisfaction**
- 📊 **Overall Calls Answered/Abandoned**
- ⏰ **Calls by Time**
- ⌛ **Average Speed of Answer**
- 💡 **Agent’s Performance Quadrant**
  - Average Handle Time (Talk Duration) vs. Calls Answered

## **Data Source**
The dataset, titled **"Call Centre Trends"**, was provided by PwC and includes call center trends over a span of three months.

### **Data Preparation**
1. **🔄 Handling Null Values**:
   - Missing or null values were managed appropriately to ensure data integrity.

2. **🔧 Changing Data Types**:
   - Data types of columns were adjusted to match their appropriate usage in analysis (e.g., numeric for metrics, text for categorical values, datetime for time-based analysis).

---

## **🪙 DAX Measures**
The following DAX formulas were used to create key metrics:

### 1. **Number of Answered Calls**
```DAX
# of Answered = 
CALCULATE(
    DISTINCTCOUNT('Sheet1'[Call Id]),
    FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "Y")
)
```
**Description**: This measure calculates the distinct count of answered calls.

### 2. **Number of Resolved Calls**
```DAX
# of Resolved = 
CALCULATE(
    DISTINCTCOUNT('Sheet1'[Call Id]),
    FILTER('Sheet1', 'Sheet1'[Resolved] = "Y")
)
```
**Description**: This measure calculates the distinct count of resolved calls.

---

## **🔍 Insights**

- 🌟 **Customer Satisfaction**: Satisfaction ratings declined from January to March, with January having the highest and March the lowest.
- 🚫 **Issue Resolution**: January saw the highest issue resolution percentage; it dipped in February but recovered in March.
- 🕒 **Call Timing**: Most calls occur in the morning.
- 🕵️‍♂️ **Agent Performance**:
  - Joe has the fastest average speed of answer.
  - Jim leads in call resolution rate despite slower response times.
  - Becky has the slowest speed of answer but ranks fifth in resolution rate.
  - Martha excels in speed of answer but has a slightly lower resolution rate.

---

## **🎨 Dashboard Design**

### **Visuals Used**
1. **Overall Customer Satisfaction**:
   - Line chart displaying monthly trends.
2. **Calls Answered/Abandoned**:
   - Pie chart showing answered vs. abandoned calls.
3. **Calls by Time**:
   - Area chart visualizing call volume throughout the day.
4. **Average Speed of Answer by Agent**:
   - Bar chart comparing agents’ average speed of answer.
5. **Agent’s Performance Quadrant**:
   - Scatter plot mapping agents based on average handle time vs. number of calls answered.

### **Interactivity**
- 🔢 Filters for:
  - Time period (e.g., month).
  - Agent-specific performance.
- 🔄 Dynamic visuals that update based on selected filters.

---

## **🔐 Conclusion**
This dashboard provides a comprehensive view of call center performance, enabling the manager to:
- 📊 Monitor KPIs effectively.
- 🔍 Identify trends and areas for improvement.
- 🙏 Recognize top-performing agents and provide targeted support to others.

By leveraging these insights, the call center manager can enhance customer satisfaction, optimize operational efficiency, and support staff development.

---

## **🔧 How to Use**
1. **Open Power BI Desktop**.
2. Import the `.pbix` file associated with this project.
3. Interact with the visuals by applying filters and exploring different metrics.



