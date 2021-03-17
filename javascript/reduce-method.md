# How to use reduce properly in javascript.

What is reduce?
Reduce is a powerful method that call execute a provided function for each value (acc) than returns only one value (total).

Ex:
Let’s say we have a bank app and I need to show the total of income, spendings and the balance. We could achieve using the reduce method.

```javascript
const summary = transactions.reduce(
  (acc, transaction) => {
    if (transaction.type === 'income') {
      acc.income += transaction.amount;
      acc.balance += transaction.amount;
    } else {
      acc.spendings -= transaction.amount;
      acc.balance -= transaction.amount;
    }

    return acc;
  },
  {
    income: 0,
    spendings: 0,
    balance: 0,
  }
);
```
