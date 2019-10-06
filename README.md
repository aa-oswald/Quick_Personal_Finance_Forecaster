# Welcome  to **[Quick_Personal_Finance_Forecaster](https://github.com/aa-oswald/Quick_Personal_Finance_Forecaster)**
This is a Python script that reads in a series of revenue/cost commitments from an Excel sheet and converts it into a time series forecast of what expected balances ought to be.

# Use Case

There is a desire to be able to forecast future account balances in order to determine whether or not a person can achieve different financial goals. Apps like Betterment and Wealthfront give the ability to make quite long term forecasts. For example, Wealthfront gives the ability for a user to determine how a house will fit into their retirement plan and what kind of house they can expect to reach.

Likewise, apps like YNAB allow users to do monthly budgets that assign every incoming dollar to an expense. This is great for keeping in the green on a month-to-month basis, and it's also great for setting short term (<1yr) goals.

Neither set of personal finance tools allow for mid-term planning between the short-term and the retirement worthy. This is reasonable- planning for this period is notorious, being too far away to be very precise but not far enough away to be smoothed out by time.

# Theory

This script attempts to pull security from the jaws of uncertainty by allowing future personal revenue/cost streams to be "gamed". The ability to do this gaming comes from using an Excel spreadsheet where each row relates to a specific "stream" of revenues or costs. For example, "Rent" is a cost stream that you generally charge to your checking account. 

The concept of this stream is essentially a "YNAB" calculator across time (income comes at multiple times a month whereas rent may come once a month and other costs may be weekly!) 

The script generates a list of transactions listed that go to the stream's end date on some periodic schedule (weekly, biweekly, monthly). 

There is also the ability to convert a row into a "Goal" which will calculate the size of the transactions and then make a stream within the period you are attempting to reach that goal. This is the *true* intent of this script: by stringing together "Goals" you can forecast the ability to afford medium-term goals that sit above the revenue-cost streams of day-to-day life. 