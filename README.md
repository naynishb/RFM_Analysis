RFM ANALYSIS OF A RETAIL STORE

This is an Google Bigquery based project for creating an RFM segmentation of customers.

**Table of Contents**
**Usage**

Problem Statement:
We will be performing a RFM analysis for a chain of retail stores that sells a lot of
different items and categories.
The stores need to adjust their marketing budget and have better targeting of customers
so they need to know which customers to focus on and how important they are for the
business.
______________________________________________________________________
What is RFM Score?
We all know that valuing customers based on a single parameter is flawed. The biggest
value customer may have only purchased once or twice in a year, or the most frequent
purchaser may have a value so low that it is almost not profitable to service them.
One parameter will never give you an accurate view of your customer base, and you’ll
ignore customer lifetime value.
We calculate the RFM score by attributing a numerical value for each of the criteria.
The customer gets more points -
● if they bought in the recent past,
● bought many times or
● if the purchase value is larger.
Combine these three values to create the RFM score.
This RFM score can then be used to segment your customer data platform (CDP).
● Ultimately, we will end up with 5 bands for each of the R, F and M-values, this
can be reduced to bands of 3 if the variation of your data values is narrow.
● The larger the score for each value the better it is. A final RFM score is
calculated simply by combining individual RFM score numbers.
● There are many different permutations of the R,F & M scores, 125 in total, which
is too many to deal with on an individual basis and many will require similar
marketing responses.
Analysis of the customer RFM values will create some standard segments.
The UK Data & Marketing Association (DMA) laid out 11 segments, and specified
marketing strategies according to their respective characteristics:
Think about what percentage of our existing customers would be in each of these
segments and evaluate how effective the recommended marketing action can be for
your business.
______________________________________________________________________
Data
Attribute Information:
● InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to
each transaction. If this code starts with letter 'c', it indicates a cancellation.
● StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned
to each distinct product.
● Description: Product (item) name. Nominal.
● Quantity: The quantities of each product (item) per transaction. Numeric.
● InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction
was generated.
● UnitPrice: Unit price. Numeric, Product price per unit in sterling.
● CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to
each customer.
● Country: Country name. Nominal, the name of the country where each customer
resides.
RFM Segmentation in BigQuery
The RFM Segmentation can be executed using these five steps:
1. Data processing
2. Compute for recency, frequency, and monetary values per customer
3. Determine quantiles for each RFM metric
4. Assign scores for each RFM metric
5. Define the RFM segments using the scores in step 4
______________________________________________________________________
Prerequisites
● Dataset link: [sales.csv](https://drive.google.com/file/d/1ROnStKd7awDAa2ofVqE2JsDOzwkKx_S9/view?usp=sharing)
