# RFM Analysis Project

This project aims to evaluate RFM score for each customer and use these insights to provide data-driven recommendations to SuperStore for launching marketing campaigns to thank customers for supporting the company over the past time. 

## Data Description
This dataset contains all the transactions that occurred between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail company. The company primarily sells unique all-occasion gifts, and many of its customers are wholesalers.

- **InvoiceNo:** Invoice number, a 6-digit integral number uniquely assigned to each transaction. If it starts with the letter 'C,' it indicates a cancellation.
- **StockCode:** Product (item) code, a 5-digit integral number uniquely assigned to each distinct product.
- **Description:** Product (item) name.
- **Quantity:** The quantities of each product (item) per transaction.
- **InvoiceDate:** Invoice date and time, representing the day and time when each transaction was generated.
- **UnitPrice:** Unit price, indicating the product price per unit in sterling.
- **CustomerID:** Customer number, a 5-digit integral number uniquely assigned to each customer.
- **Country:** Country name, specifying the customer's country of residence.

## Business Questions
SuperStore is a global retail company with a vast customer base. To express gratitude to customers who have supported the company during the Christmas and New Year season, the Marketing department wants to run marketing campaigns. They also aim to leverage potential customers and convert them into loyal ones.

- Classify the segments of each customer to deploy each marketing program suitable for each customer group.
- Recommend marketing campaigns to thank customers in the Christmas and New Year season.
- Suggest to the Marketing and Sales team with the company's retail model, which of the three indicators R, F, and M should be most interested in.

## Insights and Recommendations

### General

![no_of_transactions_by_country](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/a3daca6c-9c7b-466a-aeb1-c0fe64230b79)

The majority of transactions are in the UK, which is expected due to the company's UK-based nature.

---

![scatter_plot_of_customer_spending](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/955adc33-4c48-4f2d-8da8-098cbfe36eee)

- While some customer are outstanding with very high spending, most customers tend to fall around the average spending range.
- There are no customers with signigiciantly lower spending than the average.

---

![top_20_values_in_frequency](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/68edb7d7-f8df-426c-b374-39b3e7539d02)

![distribution_of_recency](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/b4ff52d1-6e24-4e16-b079-1ff93178458e)

- Most customers are making only 1-2 purchases during the given one-year period, and there are relatively few customers making more than 6 purchases. In the context of the online retail industry, this suggests that customers purchase requenct is relatively low.
- This, coupled with the fact that most customers made their last purchase within 50 days, indicates that while the company effectively attracts only new customers but not does not effectively retain existing ones

&rarr; The Sales and Marketing team need to pay attention to the **F metric** to improve customer retention and engagement.

### Customer Segments

![Tree map RFM segment](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/8d011327-69ce-459c-b0b2-f38b4a47a0a4)

The segments with the highest number of customers are as follows:
- Champions (19.22%).
- Hibternating customers (15.97%).
- Lost customers (11.15%).
- Loyal (9.84%).
- At risk (9.77%).
- Potential Loyalist (9.47%)

**Definition and recommended action for each customer segment:**

| Segment | Characteristics | Recommendation |
| :-: | :-: | :-: |
| Champions | Bought recently, buy often and spend the most! | Reward them. Can be early adopters for new products. Will promote your brand. |
| Loyal | Spend good money with us often. Responsive to promotions. | Upsell higher value products. Ask for reviews. Engage them. |
| Potential Loyalist | Recent customers, but spent a good amount and bought more than once. | Offer membership / loyalty program, recommend other products. |
| New customers | Bought most recently, but not often. | Provide on-boarding support, give them early success, start building relationship. |
| Promising | Recent shoppers, but haven’t spent much. | Create brand awareness, offer free trials |
| Need attention | Above average recency, frequency and monetary values. May not have bought very recently though. | Make limited time offers, Recommend based on past purchases. Reactivate them. |
| About to sleep | Below average recency, frequency and monetary values. Will lose them if not reactivated. | Share valuable resources, recommend popular products / renewals at discount, reconnect with them. |
| At risk | Spent big money and purchased often. But long time ago. Need to bring them back! | Send personalized emails to reconnect, offer renewals, provide helpful resources. |
| Cannot lose them | Made biggest purchases, and often. But haven’t returned for a long time. | Win them back via renewals or newer products, don’t lose them to competition, talk to them. |
| Hibernating customers | Last purchase was long back, low spenders and low number of orders. | Offer other relevant products and special discounts. Recreate brand value. |
| Lost customers | Lowest recency, frequency and monetary scores. | Revive interest with reach out campaign, ignore otherwise. |

---

![avg_spending-by_segment](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/49a81445-5d0c-434f-ac94-e6faf08cd0fd)

On average, each customer spends approximately $2000 on purchases at SuperStore. Among the customer segments, the three with the highest and above-average spending are:
- **Champions**.
- **Loyal**.
- **Cannot lose them**.

&rarr; The Marketing team should prioritize these segments for the next campaign.

### Marketing Campaigns

![scatter_plot_between_2_variable_RFM](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/5efe96a7-cafb-403b-a5ab-0c8808ae4012)

- There might be a relationship between recency and frequency.
- There doesn't seem to be a clear correlation between the frequency of purchases and the monetary value of customers.
- There might be a positive correlation between recency and monetary value.
  &rarr; Customers who recently made purchases tend to not only be frequent buyers but also spend more, representing potential candidates for becoming loyal customers. SuperStore should focus on **nurturing recent buyers**, as they are more likely to become loyal, high-value customers.

---

![top_10_product_by_no_of_orders](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/2a4fda4a-e154-44bd-b273-c61e64eff039)

This is a campaign launched during the Christmas and new-year season, so we analyze transactions from November and December:
- For products that have both a high number of orders and are typically purchased in large quantities *(stockcodes 22086, 23084, 85123A, 85099B, 84879, and 22197)*, **creating product combos** can be an effective strategy.
- For products with high order numbers but low quantities per purchase *(stockcodes 22112, 22423, 22111, 23355, and 21034)*, **offering discounts or cross-selling** them with similar items is a good approach.

---

![customer_segments_by_shopping_hour](https://github.com/thanhtruchhh/RFM_Analysis/assets/145547282/c1689cf0-25a7-4c38-a26b-281164e412a7)

Most customers across different segments tend to shop during the midday, roughly **between 10 AM and 3 PM**. SuperStore can introduce special offers exclusively for this time frame to reach a larger customer base. Additionally, it's essential to ensure that the website/ mobile app can handle a high volume of users.
