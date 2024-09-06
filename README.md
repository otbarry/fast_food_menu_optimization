# **Five Guys Menu Math: Crunching Cost & Quality**
## **Background**
- Five Guys needs to minimize ingredient purchasing costs while ensuring enough stock to meet demand.
- Challenges include managing limited storage space, fluctuating demand, varying ingredient costs, and supplier reliability.
- The optimization would balance cost and supply for profitability, ensure consistent availability and quality for customers, and provide suppliers with reliable purchasing patterns.

## **Model**
**Variables:**
- Xi: Quantity of ingredient i to be ordered. (2 brands for each) eg: Ball Park Buns, Pepperridge farm Buns

**Objective:**
- Minimizing the sum of the cost of goods with discounts included, Minimize z=∑(Ci⋅Xi) Where Ci is the cost of ingredient i
- In addition to that apply tiered discounts 

**Constraints:**
- Nutritional Constraints: Find combination of ingredients for menu and then constrain protein, fat, and calories for that menu item
- Demand Constraints
- Supplier Constraints: Spend over $100 from each supplier and at most $5000 at any one supplier, 100 <= (X * Xprice) <= 500
- Storage Constraint
  
**Scenarios**
- Model 1: All constraints
- Model 2: No nutritional constraints (more realistic for fast food)
- Model 3: No supplier constraints (relaxing operational limits)
  
## **Key Insights**
**Model 1:**
- Most nutritional constraints non-binding, Storage constraint non-binding, Demand binding for all items, high sensitivity for burger buns and patties, Many supplier constraints binding (e.g., buns, Kraft cheese)
- Takeaway: Balanced menu optimization; high-demand items critical
- Recommendation: Renegotiate supplier contracts, focus on high-impact items\

**Model 2:**
- Demand and supplier constraints binding, Storage constraint non-binding, High sensitivity to burger demand
- Takeaway: Removing nutritional guidelines allows slightly cheaper costs
- Recommendation: Renegotiate supplier contracts; benefits of nutritional constraints may outweigh minimal cost savings

**Model 3:**
- Demand constraints binding, Storage constraint non-binding, High sensitivity to most demand constraints
- Takeaway: Simplifying supply doesn't significantly impact nutritional demands; minimal cost differences between suppliers
- Recommendation: Prioritize improving nutritional constraints over supplier constraints if cost savings needed

**Comparison**
- 1st model more expensive, 3rd slightly cheaper than 1st, 2nd most affordable
- Get rid of nutrition constraints before the supplier constraint.
- Increase demand as storage is non binding

