# Hotel Booking Demand - Exploratory Data Analysis
## About this project
For this project, I explored the Hotel Booking Demand dataset to understand what hotel booking data can tell us about customer behaviour and booking patterns.

I used Python, Pandas, Matplotlib and Seaborn to inspect the data, deal with missing values and duplicate records, calculate summary statistics, and create visualisations. I wanted to go beyond simply looking at the numbers and find patterns that help explain how people book hotels, when they travel, and how often bookings are cancelled.

The analysis was carried out in Google Colab.

## Dataset Used - Hotel Booking Demand dataset on Kaggle

The Original dataset contains 119,390 rows and 32 columns. It includes information about two types of hotels - City Hotels and Resort Hotels - along with booking dates, guest details, length of stay, booking channels, customer types, cancellation status and average daily rate (ADR).

## My Approach to the Analysis
I started by getting familiar with the dataset before moving on to visualisations. The notebook covers the following steps:
1. Loaded the dataset and checked its shape, column data types, memory usage, and first and last rows.
2. Looked for missing values and used a visualisation to understand where they occurred.
3. Explored numerical columns using summary statistics and categorical columns using value counts.
4. Checked for duplicate records and removed exact duplicates.
5. Handled missing values where appropriate. For example, missing children values were filled using the median, and missing country values were labelled as Unknown.
6. Converted the reservation status date into a datetime format.
7. Created two additional columns — total_guests and total_nights — to make some parts of the analysis easier.
8. Investigated unusual values, such as negative or unusually high ADR values, bookings with no guests, and very long lead times.
9. Created charts to explore booking patterns and relationships in the data.
    
After removing exact duplicate records, the cleaned dataset contained 87,396 rows. I kept missing agent and company identifiers because there was no reliable way to determine their actual values. For a few charts, I excluded extreme values only from that particular visualisation so that the main patterns would be easier to see; these records were not removed from the main cleaned dataset.

## Visualisations
I created seven visualisations, each to explore a different question about the bookings:

### 1. Hotel Type Distribution

![Hotel Type Distribution](visualizations/Hotel_Type.png)

### 2. Cancellation Rate by Hotel Type

![Cancellation Rate](visualizations/Cancellation_Rate.png)

### 3. Monthly Booking Trends

![Monthly Bookings](visualizations/Monthly_Bookings_trends.png)

### 4. Booking Lead Time Distribution

![Lead Time Distribution](visualizations/Lead_Time.png)

### 5. Average Daily Rate (ADR) Distribution

![ADR Distribution](visualizations/ADR_Distribution.png)

### 6. Market Segment Distribution

![Market Segment](visualizations/Market_Segment.png)

### 7. Correlation Heatmap

![Correlation Heatmap](visualizations/Correlation_Heatmap.png)
 
## A Few Takeaways from the Data

While exploring the dataset, I came across a few interesting patterns:

- **City Hotels received more bookings** compared to Resort Hotels.
- **July and August had the highest number of arrivals**, showing that these months were particularly busy.
- **Cancellations were more common for City Hotels** than for Resort Hotels.
- **Online Travel Agents contributed the largest share of bookings**, making them the most commonly used market segment.
- **Booking lead times varied quite a bit.** Most guests made their bookings closer to their arrival date, while some booked several months in advance.

These patterns helped me get a better understanding of booking behaviour in the dataset. They reflect only the data explored in this project and may differ across other hotels or destinations.

## Tools and Technologies I Worked With

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
