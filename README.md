# association-rule-mining

### Market Basket Analysis:
Market basket analysis is a technique used to discover associations and relationships between items frequently purchased together by customers. The Apriori algorithm is a popular algorithm used to perform market basket analysis. 

It is evaluated on following:
- Support
- Confidence
- Lift
- Leverage
- Conviction

Support: The Apriori algorithm starts by calculating the support of each item in the dataset. Support is the proportion of transactions in which an item appears. It helps identify the most frequently occurring items.



ing:

Support: Support is the proportion of transactions in a dataset that contains a specific itemset. It indicates how frequently an itemset appears in the dataset. Support is calculated as the number of transactions containing the itemset divided by the total number of transactions. A higher support value indicates a stronger association between the items.

$$support(X) = \frac{\sum(transactions\ with\ X)}{\sum(all\ transactions)}$$

$$support(X+Y) = \frac{\sum(transactions\ with\ X\ and\ Y)}{\sum(all\ transactions)}$$

support is fraction of transactions that contain item X or itemset (X+Y)

support = 0.05 for example means that the item appears in 5% of the transactions

Confidence: Confidence measures the conditional probability of finding the consequent item in a transaction given that the transaction contains the antecedent itemset. It is calculated as the support of the combined itemset (antecedent and consequent) divided by the support of the antecedent itemset. Confidence ranges from 0 to 1, where 1 indicates a perfect correlation. Higher confidence values indicate a stronger relationship between the antecedent and consequent.

$$confidence(X->Y) = \frac{\sum(transactions\ with\ X\ and\ Y)}{\sum(transactions\ with\ X)}$$

$$confidence(X->Y) = \frac{support(X+Y)}{support(X)}$$

confidence is how often item Y appears in the transactions that contain item X

confidence 0.27 for example means that item Y appears in 27% of all transactions with item X

Lift: Lift is a measure of the strength of association between the antecedent and consequent in an association rule. It compares the observed support of the combined itemset with the expected support if the items were independent of each other. Lift greater than 1 indicates a positive association, lift equal to 1 indicates independence, and lift less than 1 indicates a negative association. Higher lift values suggest a stronger association between the items.

$$lift(X->Y) = \frac{confidence(X->Y)}{support(Y)}$$

lift is how much our confidence wil increase that Y will be purchased once X is added to the basket

lift > 1: item Y is likely to be purchased when item X is purchased

lift < 1: item Y is unlikely to be purchased when item X is purchased

lift = 1.4 for example means that once item X is purchased the likelihood that item Y will be purchased increases 40%

Leverage: Leverage quantifies the difference between the observed support of the combined itemset and the support expected under independence. It measures how much the occurrence of the antecedent and consequent together deviates from what would be expected if they were independent. A leverage value of 0 indicates independence, while positive or negative values indicate the presence of association.

Conviction: Conviction measures the degree of implication of the consequent by the antecedent in an association rule. It indicates how much more likely the consequent is to appear in a transaction when the antecedent is present compared to when the antecedent is not present. Conviction is calculated as the ratio of the complement of the confidence of the rule and the complement of the support of the consequent. Conviction values greater than 1 indicate a strong implication, while values close to 1 suggest weak implication.

$$conviction(X->Y) = \frac{1-support(Y)}{1-confidence(X->Y)}$$

conviction = 1.32 for example means that the rule would be incorrect 32% more often if the association between X and Y was and accidental chance

By applying the Apriori algorithm, market basket analysis can provide valuable insights into customer behavior, product placement, and targeted marketing strategies.
