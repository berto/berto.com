# Measuring success with cohorts

Whenever you launch a new marketing campaign, or a new product line, or get some good old PR, you want to see what’s the effect of that action. Cause and effect. The easiest way of doing it is to track cohorts.

Cohorts are just groups of people that share a common characteristic. As your business progresses with time, the easiest and broader cohorts to track are time cohorts. In this case, a cohort would be defined as the group of people who first bought during a certain period: day or week or month. How many customers did we acquire this week vs. last week? How good of a customer is a customer who bought on christmas vs. one which bought on valentines? All these questions are answered if you track your cohorts.

The simplest time cohort has two axis. On one axis you have the date of FIRST purchase of the customer. On the other, you have the date of ANY order. Just like in the picture above, you see that the diagonal is the first time a customer purchased — customers who first purchased in march who also purchase in march are first time customers. Also, for each group of customers who FIRST bought on a specific date, ANY purchase with date bigger than REAL date is a return purchase. Simple.

How to build such cohorts?

1. you start with a list of all orders. The minimum information is a customer id and date of purchase. Believe me, with that you can already build something super powerful. If you want to do other things, you can include spend, number of items on the basket and other information.
2. then you need to mark, for each order, the date of that customers’ first purchase on a new column. For first purchases, the date of that order and the date of customer’s first purchase will be the same. All you need is a vlookup.
3. then you can build a model yourself (eheheh) or just throw it all under a pivot to crunch.

You can check and download the following file with the individual steps here: [my first cohort table](https://docs.google.com/spreadsheets/d/1hKCg9rCBnUvA5FUjoFXzVpaywCUBNePSF0WutNWAUaY). You won’t have permissions to change anything, but you can download the model by going File/ Download/ Excel.

On this particular example, if you look at step 3, we can see that the first month had a lot of activity (27 purchases) and that on the following months we some mild activity (between 3 and 6 purchases). The next 3 months cohorts only had 1 person each, and this three people (1 per cohort) came back actually quite a lot comparatively (between 0 and 3 times on each successive months). So these cohorts of people show a better behaviour relative to their initial month of purchase than the first cohort, which was big (27) but didn't have a lot of returning action.

With a cohort like this, you can:

* understand if you are acquiring more or less customers per period
* understand if each new cohort of people is returning more or less often
* extrapolate a natural timely behaviour of people and do projections
* compare all this with real world actions (campaigns, product changes) and understand the impact of your actions

So, what other types of cohorts are there?

* time cohorts. The ones i described above
* campaign cohorts. Instead of grouping customers by date or period, you group them by the campaign which acquired them, independently of when they were acquired (or in addition to)
* behavioural cohorts. Really, any trait can be used and analysed. How do female customers behave in the months following a purchase vs. male customers?

The data plotted in a cohorts analysis can be varied as well:

* orders. How many orders each cohort created on their first and subsequent months/ period
* revenue. How much revenue each cohort brought on their first and subsequent purchases
* items per order. Yep
* fancy something kinky? Really, anything related to the orders can be crunched

Finally, there’s an interesting twist I like to give to cohort analysis, which is if you do your analysis orthogonally. Orthogonal means things are independent from each other. So, in a way, instead of doing a big cohort which tracks revenue, you can build several cohorts that track users, orders per user and revenue per order. Each of these sub-cohorts can be affected by different events:

* boosting your customer acquisition campaigns will affect mostly the amount of users
* opening on weekend probably affect the amount of new customers and orders per user
* launching a companion product will most likely affect revenue per order more than anything

Hands-on time! Check out this cohort model that you can explore. It tracks several orthogonal variables across the real data you input. It tracks their evolution and their projects the growth of current and future cohorts from those variables. Finally it uses a convolution of all the cohorts to project revenue.

In order for anyone to access it, I put it on Google Drive [Orthogonal cohort model](https://docs.google.com/spreadsheets/d/1ntcmkOEEVg3lCX1K5078Czu-9fAan9Xu7yJdw8wzv1A/edit?usp=sharing). You won’t have permissions to change anything, but you can download the model by going File/ Download/ Excel.

Have fun!