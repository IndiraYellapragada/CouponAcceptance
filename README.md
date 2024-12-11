Context

Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

Overview

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

Data

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).

Approach to the Goal:
Investigate the dataset:
1. Identify if any duplicates records and remove them
2. Identify number of null values in each column
3. Fetch the value counts of each column -This lets us identify columns which can be converted to numeric .

Observations:
#This indicates that 56% of observations have accepted the coupons

**Analysis on Bar Coupons**
1. *Overall Acceptance of Bar Coupons:* 40% of all bar coupons distributed were accepted by drivers.
2. Drivers Visiting Bars Frequently (More than Once a Month):

        Without Kid Passengers: 91% of these drivers accepted the coupons, particularly those not employed in farming, fishing, or forestry occupations.
        Over Age 25: 54% of drivers over 25 who visited bars more than once accepted the coupons compared to others.

3. Under Age 30: 91% of drivers under 30 who visited bars accepted coupons versus those older than 30.
Income and Restaurant Type:

4. Only 17% of drivers with an income below $50K and who visited cheap restaurants accepted bar coupons.
Passenger Influence:

5. Drivers visiting bars more than once with no kids and no widow passengers had a 43% coupon acceptance rate.
6. Drivers who went to bars less frequently accepted the coupon four times more than those who visited bars more frequently.

**High Chances of Bar Coupon Acceptance :**
1. Drivers visiting bars more than once a month without kid passengers have the highest chance of accepting coupons (91% acceptance rate).
2. Young drivers under the age of 30 who visit bars frequently are also likely to accept coupons at a similar rate (91%).
**Moderate Chances **
   Drivers aged over 25 who visit bars more than once accept coupons moderately often (54% acceptance rate).
Low Chances:

Drivers with an income below $50K and those visiting cheap restaurants are less likely to accept coupons (17%).

**Analysis on Coffee House Coupons**

1. 49% of all coffee house coupons distributed were accepted.
2. Acceptance Based on Coffee House Visit Frequency:Drivers who visited coffee houses more frequently had a higher acceptance rate compared to those who visited less often.
3. Impact of Passenger Demographics:

      Drivers who visited coffee houses more than once and had no kid passengers accepted coupons at a rate 1.5 times higher than others.
      Drivers who visited coffee houses more than once with no kid passengers and no married passengers also had an acceptance rate 1.5 times higher than others.
      Drivers who visited coffee houses more than once with no kid passengers and were aged <30 had an acceptance rate 51% of others, suggesting that younger drivers in this group were less likely to accept the coupon.
4. Weather Conditions and Acceptance Rates:

On sunny days, drivers who visited coffee houses more than once with no kid passengers had an acceptance rate 1.13 times higher than others.
On rainy days, the acceptance rate for this group was significantly lower, at only 3% of other drivers.

**High Chances of Coffe House Coupon Acceptance :**

Drivers who visit coffee houses more frequently, particularly with no kid passengers, show a consistently higher likelihood of accepting coupons.
Moderate Chances of Acceptance:

Drivers visiting coffee houses more than once with no kid passengers on sunny days exhibit moderately higher acceptance rates, indicating favorable weather conditions encourage acceptance.
Low Chances of Acceptance:

Drivers aged under 30 in the group of frequent coffee house visitors with no kid passengers are less likely to accept coupons compared to their older counterparts.
Drivers with no kid passengers on rainy days have a significantly reduced acceptance rate, suggesting adverse weather discourages coupon usage.


