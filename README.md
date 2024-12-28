# HOTEL-BOOKING-CANCELLATION-ANALYSIS


## **Comparison of Models: Logistic Regression, KNN, and Pre-Pruning Decision Tree**

## **Problem Definition**
The hospitality industry faces significant challenges due to booking cancellations, which can lead to revenue losses, misallocation of resources, and reduced operational efficiency. Accurately predicting cancellations allows hotels to implement proactive strategies such as dynamic pricing, overbooking policies, and personalized guest experiences. By developing a predictive model for booking cancellations, hotels can optimize occupancy rates, enhance revenue management, and improve guest satisfaction.


---
## **Importance**

This project focuses on predicting hotel booking cancellations based on a dataset containing various features such as booking lead time, room type, customer demographics, and special requests. The goal is to understand key drivers of cancellations and provide actionable insights for better decision-making in hotel operations.


---

## **Key Stakeholders**
This problem is of interest to multiple stakeholders within the hospitality industry:

- **Hotel Management**: To optimize revenue and occupancy rates by reducing cancellations.
- **Revenue Managers**: To improve forecasting and implement dynamic pricing strategies.
- **Marketing Teams**: To create targeted campaigns for high-value, low-risk customers.
- **Operations Teams**: To allocate resources effectively based on predicted occupancy.
- **Travel Platforms**: To enhance user experience by providing accurate booking insights.

By predicting cancellations, stakeholders can minimize risks, improve operational efficiency, and maximize profitability, thereby gaining a competitive edge in the market.



---

## **Dataset Description**
The dataset contains 119,390 records, where each record represents a unique hotel booking. The target variable is **is_canceled,** indicating whether a booking was cancelled **(1)** or not **(0)**. The dataset includes the following features:

- **Hotel**: The type of hotel (e.g., Resort Hotel or City Hotel), which influences booking patterns.
- **Is Canceled**: The target variable indicating whether the booking was cancelled.
- **Lead Time**: The number of days between the booking date and the arrival date, impacting cancellation likelihood.
- **Arrival Date Year/Month/Day**: Details about the booking's arrival date, which can show seasonal trends.
- **Stays in Weekend Nights**: Number of weekend nights in the booking, reflecting leisure travel patterns.
- **Stays in Week Nights**: Number of weeknights in the booking, which may correlate with business travel.
- **Adults**: Number of adults in the booking, affecting room type and service requirements.
- **Children**: Number of children in the booking, influencing family-oriented services.
- **Babies**: Number of infants, further tailoring family accommodations.
- **Meal**: Type of meal plan included in the booking, which may correlate with cancellation behavior.
- **Country**: The nationality of the guest, providing insights into geographical trends.
- **Market Segment**: The distribution channel through which the booking was made (e.g., online, offline).
- **Distribution Channel**: Specific booking source (e.g., direct, corporate).
- **Is Repeated Guest**: Indicator of whether the guest is a returning customer.
- **Previous Cancellations**: Number of previous cancellations made by the guest.
- **Previous Bookings Not Canceled**: Number of successful bookings made by the guest in the past.
- **Reserved Room Type**: Type of room initially reserved by the guest.
- **Assigned Room Type**: Type of room assigned upon arrival.
- **Booking Changes**: Number of changes made to the booking, which may indicate uncertainty.
- **Deposit Type**: Type of deposit made (e.g., no deposit, refundable, non-refundable).
- **Days in Waiting List**: Days the booking spent on the waiting list.
- **Customer Type**: Customer classification (e.g., transient, group, contract).
- **ADR (Average Daily Rate)**: The average revenue earned per occupied room.
- **Required Car Parking Spaces**: Number of parking spaces requested.
- **Total of Special Requests**: Total number of special requests made by the guest.
_______
# **Conclusions**
- 4.1 Best Model: Among pre-pruning, KNN, and Logistic Regression, which one gives you the best accuracy? Which one gives you the best recall? Which one gives you the best precision? What measures will you use to determine the final model? Describe your choice, results, and reasoning.

- 4.2. Managerial Implications: What insights can you provide to managers if you use decision tree? For instance, interpret the feature importance from the decision tree.

### **4.1 Best Model: Pre-Pruning, KNN, Logistic Regression**
### a.  **Comparison of Metrics**

Here’s the comparison of **Logistic Regression**, **KNN**, and **Decision Tree** models in a markdown table format, showing the metrics in percentages:

---

### Model Comparison Table

| Metric                     | Logistic Regression (%) | KNN (%) | Pre Pruning (%) |
|----------------------------|--------------------------|---------|--------------------|
| **Accuracy**               | 72                      | 70      | 73                 |
| **Precision**    | 47                     | 44     | 63                |
| **Recall**    | 7                      | 30      | 03               |
| **F1**       | 12                      | 36      | 06                 |
                
----
### b. **Evaluation**
### **Comparison of Models: Logistic Regression, KNN, and Pre-Pruning Decision Tree**

#### **Best Metrics**
1. **Best Accuracy**:
   - **Pre-Pruning Decision Tree**: **73%**
     - Slightly outperforms Logistic Regression (72%) and KNN (70%).
     - Indicates good overall prediction performance.

2. **Best Recall**:
   - **KNN**: **30%**
     - Performs significantly better in identifying cancellations (class `1`) compared to Logistic Regression (7%) and Pre-Pruning Decision Tree (3%).
     - Critical for minimizing false negatives (missed cancellations).

3. **Best Precision**:
   - **Pre-Pruning Decision Tree**: **63%**
     - Outperforms Logistic Regression (47%) and KNN (44%) in predicting cancellations accurately.
     - Indicates fewer false positives (incorrectly predicting cancellations).

---
### c. **Final Choice**
- **Chosen Model**: KNN

KNN is the best model because it achieves the **highest recall for class 1 (30%)**, making it more effective at identifying cancellations compared to Logistic Regression (7%) and the Pre-Pruning Decision Tree (3%). This is crucial for minimizing missed cancellations, which can lead to overbooking and revenue losses. Additionally, KNN balances recall with acceptable precision (44%) and a competitive F1-score (36%), providing better performance in handling cancellations while maintaining reasonable accuracy (70%). Its ability to model nonlinear relationships further justifies its selection over simpler models like Logistic Regression or Decision Tree.

--
### d. **Recommendations**
1. Improve predictive power by adding or transforming features.
2. Address class imbalance using techniques like oversampling or class weighting.
3. Experiment with ensemble methods (e.g., Random Forest or Gradient Boosting).

---
## 4.2 Managerial Implications

Based on the results of your decision tree analysis, it is evident that factors like **lead time**, **ADR (Average Daily Rate)**, and **booking channels** significantly influence cancellation rates. Long lead-time bookings are more prone to cancellations, suggesting the need for stricter cancellation policies, such as non-refundable deposits or tiered fees for these bookings. High ADR bookings, often associated with price-sensitive customers, could benefit from value-added incentives, like free upgrades or discounts, to increase commitment and reduce cancellations.

To address the observed challenges, managers should focus on high-risk segments identified by the model, such as customers booking through OTAs or with a history of cancellations. Proactive communication strategies, personalized offers, and dynamic pricing based on seasonal trends can help retain these bookings. By leveraging these insights, managers can minimize revenue loss, improve customer satisfaction, and optimize operational efficiency.



