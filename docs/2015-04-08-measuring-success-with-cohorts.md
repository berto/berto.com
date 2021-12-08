# Measuring success with cohorts

Whenever you launch a new marketing campaign, or a new product line, or get some good old PR, you want to see what’s the effect of that action. Cause and effect. The easiest way of doing it is to track cohorts.

Cohorts are just groups of people that share a common characteristic. As your business progresses with time, the easiest and broader cohorts to track are time-based cohorts. You can do them weekly or monthly, and i'll mention different examples below. In this case, a cohort would be defined as the group of people who first bought during a certain period: day or week or month. All these questions are answered if you track these time-based cohorts:
- How many customers did we acquire this week vs. last week? 
- How good is a customer who first purchased during Christmas vs. one which we acquired for Valentines? 

The simplest cohort table has two axis, and can be rendered in two separate ways:
- time elapsed. On the vertical axis you list the cohorts: the months of first puchases. On the horizontal axis you list months elapsed: 0 (month of first purchase), 1 (the month after), 2, etc.
- real time. The vertical axis is the same as above. On the horizontal axis you list real months, Jan 2022, Feb 2022, etc.

# How to build cohorts?

The following examples are all hosted in Rows, the spreadsheet platform my team and I are building. You can (should!) clone my spreadsheet and play around with it, by clicking the + icon. That will create your own copy on your own account!

## Introduction to cohorts 

1. you start with a list of all orders in the table `Sales data`. The minimum information is a customer id and date of purchase. Believe me, with that you can already build something super powerful. If you want to do other things, you can include spend, number of items on the basket and other information as i did in the example.
2. then you need to calculate, for each order on that table, some helper columns that determine the `month of the sale`, `month of cohort` (month of first purchase of that person), `months elapsed` (from this user's cohort to the current order) and the `purchase in month` for this client. Those are all just a few INDEX MATCH functions and other math tricks.
3. then you can build a cohort table (elapsed) by doing a COUNTIFS that counts, for each cell, the number of orders that were done for that cohort (row) and (elapsed month) column from different individuals (order for the person in the month =1). you can also compute a % of the month 0, to see what % of people comes back, and then plot it in a chart, as I did.

You can check the cohorts [here](https://rows.com/humberto/analytics/cohorts-introduction-6EEmgZhfuc2euqbFWCyWTx/live). 

With a cohort like this, you can:

* understand if you are acquiring more or less customers per period
* understand if each new cohort of people is returning more or less often
* extrapolate a natural timely behaviour of people and do projections
* compare all this with real world actions (campaigns, product changes) and understand the impact of your actions

## Cohorts with real data

To go one step further, there’s an interesting twist I like to give to cohort analysis, which is to do my cohorts orthogonally. Orthogonal means that variables are independent from each other. So, in a way, instead of doing a big cohort which tracks revenue, you can build several cohorts that track users, orders per user and revenue per order, and then multiply them to build the outcome (revenue).

I built a much more complete - and orthogonal - cohort model [here](https://rows.com/humberto/analytics/cohorts-for-e-commerce-real-data-7AgSTMDhctsstfl7hUQMxN/a8e012a4-8fb2-44b3-8f70-f1ccbb124fa3/live). 

Check how it looks, or duplicate and play with it by clicking +.

With a cohort like this, and it's independenent variables, you will be able to understand that:

* boosting your customer acquisition campaigns will affect mostly the amount of users.
* opening on weekend probably affect the amount of new customers and orders per user.
* launching a companion product will likely affect revenue per order more than anything.

## Cohorts for simulations

To complete this, I build one last model, for simulating purposes. Here i used a complete, orthogonal cohort model, and I set the inputs to the simulation as editable cells so that you can play around. Check it [here](https://rows.com/humberto/analytics/cohorts-for-e-commerce-simulator-2tyl566FH2bc8fNtbMvmyI/6ce4e9ad-2e74-47a3-9886-99891384d424/live). 

If you want it, duplicate it ane continue to evolve it!


