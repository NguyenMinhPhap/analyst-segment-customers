# analyst-segment-customers
analyst and category customer groups 
1, Overview:-This project analyses customer purching behavior using the RFM (Recency, Frequency, Monetary) model
-The objective is to segment customers based on their transaction history to better understand customer value and support marketing strategies 
-The analysis was performed using SQL Server for data processing
2, Dataset:The dataset used in this project is the Online Retail dataset, which contains transactional records including:CustomerID,InvoiceNo,InvoiceDate,quantity,Unitprice
  These fields allow the calculation of RFM metrics for each customer
3, Tools Used:-SQL Server/ Azure Data Studio
             - RFM Model for Customer Segmentation
  4, RFM Model Explanation: Metric	                                        Meaning
                          Recency (R)	                                    How recently a customer made a purchase
                          Frequency (F)	                                  How often a customer makes purchases
                          Monetary (M)	                                  How much money the customer spends
  5,Analysis Process:-Data Cleaning:Remove null customerIDs
                                    Calculate total purchase value 
                      -Calculate RFM Metrics:Recency = Days since last purchase
                                             Frequency = Number of purchases
                                             Monetary = Total spending
                      -Create RFM Scores:Using SQL window functions to assign scores (1–5)
                      - Customer Segmentation:   Customers are grouped into segments based on RFM scores.
  6,Customer Segments:  segments            Description
                       Champions	          Recently purchased, frequent buyers, high spenders
                      Loyal Customers	      Frequent buyers with strong engagement                     
                       New Customers	      Recently acquired customers
                      Regular Customers	    Moderate purchase activity
                      Lost Customers        Customers who have not purchased recently
  7,Project Structure
├── data
│   └── online_retail.csv
│
├── sql
│   └── rfm_analysis.sql
└── README.md
