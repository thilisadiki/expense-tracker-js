# Expense Tracker

## Overview

This is a simple expense tracker application that allows users to:

- Add income and expenses 
- View total income, expenses, and balance
- View transaction history
- Delete transactions
- Persist transactions to localStorage

## Features

- Add transaction with description, amount, and type (income vs expense)
- Transaction amounts are added or subtracted from total balance
- Income and expense totals are calculated 
- Transaction history displayed in list
- Deleting transactions updates totals and removes from list
- All transactions saved to localStorage
- On reload, transactions are loaded from localStorage

## Usage

To use the app:

- Enter transaction description and amount
- Select income or expense type
- Click 'Add Transaction' to add to list
- Transactions are added to list, and totals updated
- Click red 'X' to delete a transaction
- Transactions persist when page is reloaded

## Code Overview

The project consists of:

- `index.html` - HTML structure
- `style.css` - CSS styles 
- `script.js` - JavaScript logic
- `transactions` - Array to store transactions

The `script.js` contains the following functions:

- `init()` - Initializes app, loads from storage
- `updateBalance()` - Calculates total, income, expense
- `addTransaction()` - Add new transaction
- `removeTransaction()` - Remove transaction
- `updateStorage()` - Saves transactions to storage

The `transactions` array stores each transaction object:

```
{
  id: 'unique id', 
  description: 'Transaction description',
  amount: -35, // negative for expense, positive for income
  type: 'expense' // or 'income'
}
```

Local storage is used to persist data between sessions.

## Future Improvements

Some potential improvements:

- Better input validation and error handling
- Categories for transactions
- Visual charts of spending
- Service worker for offline support
- Export transaction history

## Credits

Code based on Brad Traversy's JavaScript Tutorial.
