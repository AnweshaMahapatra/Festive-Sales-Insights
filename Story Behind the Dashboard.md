## 🧠 The Meeting Nobody Wanted to Have

Every festive season, AtliQ Mart runs promotions.
Discounts, cashbacks, bundle deals the works. 

The stores fill up. The tills ring. And then the season ends, and someone has to write the report.

That report usually says: **revenue went up.**

And technically, it did.

1.Pre-promotion revenue was **₹141 million**

2.Post-promotion it was **₹296 million**.

3.Incremental revenue: **₹155 million**.  **A 211% lift**
  Numbers that look spectacular on a slide.

But somewhere in the planning room for the next campaign, a quieter question starts circulating.

**Did the promotions actually cause that? And if they did which ones?**

**That question is harder to answer than it looks.
And answering it honestly required building something that didn't exist yet.**

---

## 🧩 Two Products That Changed the Conversation

Before any dashboard existed:

The first step was SQL. Raw queries against the transaction data, asked to produce specific answers to specific questions.

One of the first: **list products priced over ₹500 that were featured in a BOGOF promotion.**

The result came back with two products.

**Atliq Waterproof Immersion Rod-:₹1,190.**  
**Atliq Double Bedsheet Set:-₹1,020.**

Buy one, get one free. On products priced above a thousand rupees.

This is not a trivial promotional decision.

When you offer BOGOF on a **₹1,190 product**, the effective price per unit becomes- **₹595 a 50%** discount, absorbed entirely by the business. 
The question of whether the volume uplift justifies that margin sacrifice is exactly what the analysis needed to answer.

The short answer:

As the dashboard later confirmed: for these specific products, in the Home Appliances and Home Care categories, the answer was yes.

**Atliq Waterproof Immersion Rod ended the campaign period with a 266.19% IR%**-the highest incremental revenue percentage of any product across both campaigns. 

The sacrifice paid off. But that conclusion required data to reach it couldn't be assumed in advance.

---

## 🏙️ What Bengaluru Knows That Vijayawada Doesn't

The store distribution query returned a simple ranked list:

**Bengaluru has 10 stores. Chennai has 8. Hyderabad has 7. Trivandrum and Vijayawada have 2 each.**

That distribution matters because it sets the stage for the most important geographic finding in the analysis.

When incremental revenue percentage is ranked by city, the cities with the most stores:

**Bengaluru (116.05%)** 

**Hyderabad (100.15%) are not leading the table**.

**Madurai, with just 4 stores, is at the top at 120.00%.**

**Chennai at 116.84%. Bengaluru third at 116.05%**.

And at the bottom: **Visakhapatnam at 94.39%.**

Below 100% means the city generated less revenue during the promotional period than it would have at baseline pricing. 

The promotions, in net terms, cost Visakhapatnam money. 

Customers who would have paid full price instead paid promotional prices and not enough new customers came in to make up the difference.

Visakhapatnam has 5 stores:

A meaningful presence. But its promotional result is the worst in the network. 

The question isn't whether to notice this. 

It's whether leadership will change the promotional approach in that market before the next campaign, or run the same playbook again and expect different results.

---

## 🎉 The Diwali vs Sankranti Calculation

The campaign revenue query required careful SQL. Because different promotion types have different revenue mechanics-BOGOF doesn't just discount.

It doubles units delivered; 500 Cashback reduces effective price per unit by a fixed ₹500; percentage discounts apply proportionally the revenue calculation had to account for each promotion type's mechanics separately using a **`CASE WHEN`** structure.

When that calculation was run, the comparison was clear:

| Campaign | Revenue Before | Revenue After |
|---|---|---|
| Diwali | ₹83M | ₹171M |
| Sankranti | ₹58M | ₹124M |

Both campaigns generated positive impact. 

But Diwali's lift was larger in both absolute and proportional terms. More importantly, the data behind those numbers told a different story at the promotion-type level.

Diwali's performance was almost entirely driven by **500 Cashback generating ₹77M in IR**

A premium, high-revenue-per-unit promotion applied during the peak gifting season when customers are already motivated to spend on high-ticket items. 

Sankranti's performance was driven by **BOGOF generating 313,000 incremental units** 

A volume promotion that moved product but generated comparatively modest revenue per unit **(₹53M IR on 313K ISU vs Diwali's ₹77M on 34K ISU from the same promo type)**.

The two campaigns were doing different things, even though they looked similar in the aggregate headline numbers.

---

## ⚡ The Category That Shocked Everyone

The Diwali category ISU% ranking used a CTE building the before/after comparison first, then applying `ROW_NUMBER() OVER (ORDER BY ISU% DESC)` to rank categories cleanly. 
The result:

| Category | ISU% | Rank |
|---|---|---|
| Home Appliances | 588.45% | 1 |
| Home Care | 203.14% | 2 |
| Combo1 | 202.36% | 3 |
| Personal Care | 31.06% | 4 |
| Grocery & Staples | 18.05% | 5 |

1. Home Appliances at **588%** during Diwali alone. 

2. Nearly six times the pre-promotion volume. This is not an incremental improvement.

3. It is a category that essentially sits dormant at full price and erupts when a meaningful promotion appears. 

4. Customers are waiting. The promotion is the trigger.

5. Grocery & Staples at **18%** is the inverse story.

6. Customers buy staples regardless. Promotions on essential items attract some incremental volume but mostly discount existing demand. 

7. The business is giving away margin on purchases that would have happened anyway.

8. These two data points placed side by side in the same ranking table contain a significant strategic implication: the promotional budget being spent on Grocery & Staples       discounts is subsidising behaviour that doesn't need a subsidy. 

9. That budget would generate far more incremental return if reallocated to Home Appliances.

---

## 🚨 The Three Promotions That Were Never Supposed to Show Up Here

The promotion type analysis was built to answer a simple question: 

Which promotion type generated the most revenue? The expectation was a ranking with some promotions better than others.

Nobody expected three of the five to be negative.

**25% OFF: –₹3M. 33% OFF: –₹2M. 50% OFF: –₹1M.**

The discount-based promotions the ones that feel most intuitive, most familiar, most "promotional" all destroyed revenue. 

Not marginally. Not rounding-error negative. Structurally, reliably negative across both campaigns.

The mechanism is straightforward once you see it: 

A 33% discount applied to a product requires a 50% increase in volume just to break even on revenue. 

A 50% discount requires a 100% volume increase. These thresholds were not reached. 

The volume uplift these promotions generated was real but insufficient to offset the pricing concession.

The right conclusion is not that discounts never work.

It's that these specific discount levels, applied to this product mix, in these markets, during these campaigns, did not work. The data is specific enough to act on. 

The decision now is whether to retire these promotion types for the next cycle, restructure them at shallower discount depths, or test them on a narrower product selection where price elasticity is demonstrably higher.

What the dashboard has ensured is that the conversation can no longer be avoided.

---

## 📊 What the Dashboard Was Actually For

The Power BI dashboard didn't discover any of this. 

The MySQL queries discovered it. The dashboard made it possible for the people who needed to act on it to see it without running SQL themselves.

Store managers who need to know how their store ranks on IR vs other stores in their city. 

Category managers who need to see Home Appliances' **265.21% IR%** next to **Personal Care's–34.20%** in the same visual. 

Campaign planners who need to see Diwali's **500 Cashback result (₹77M IR) and Sankranti's BOGOF result (313K ISU**) in a single table before they decide what to run next season.

The three slicers: City, Promo Type, Campaign mean every viewer can ask their own version of the question. 

Filter to Visakhapatnam and see only that city's numbers. Filter to **BOGOF** and see what it generated in each campaign. 

Filter to Diwali and compare all five promotion types within a single festive period.

The analysis answers the question that festive season reports almost never ask: 

Not just **did revenue go up**, but **what specifically caused it, what specifically hurt it, and what should we do differently next time.**

Those three questions now have answers. What happens next is a planning decision.

---

*Festive Sales Analysis | MySQL & Power BI | Diwali 2023 & Sankranti 2024* ✨
