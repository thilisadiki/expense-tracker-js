# Expense Tracker

## Overview

This is a simple expense tracker application that allows users to:

- Add income and expenses 
- View total income, expenses, and balance
- View transaction history
- Delete transactions
- Persist transactions to localStorage
- Works offline using a service worker
- Installable to device home screen
- Fast load times using cache

## Features

- Add transaction with description, amount, and type (income vs expense)
- Transaction amounts are added or subtracted from total balance
- Income and expense totals are calculated 
- Transaction history displayed in list
- Deleting transactions updates totals and removes from list
- All transactions saved to localStorage
- On reload, transactions are loaded from localStorage

## New PWA Features
- Service worker - caches assets for offline access
- Web app manifest - enables install to homescreen
- IndexedDB - handles data storage
- Load fast on repeat visits with cache

## Usage

To use the app:

- Enter transaction description and amount
- Select income or expense type
- Click 'Add Transaction' to add to list
- Transactions are added to list, and totals updated
- Click red 'X' to delete a transaction
- Transactions persist when page is reloaded 
- Load the app in a browser
- Install to your device - add to home screen
- Use the expenses app offline
- Data is saved between sessions

## Code Overview

The project consists of:

- `index.html` - HTML structure
- `style.css` - CSS styles 
- `script.js` - JavaScript logic
- `transactions` - Array to store transactions
- `manifest.json`
- `service-worker.js`

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

## Learnings
- Building this web app I learned:

- How to make a progressive web app
- Using service workers for offline capability
- Storing data in IndexedDB
- Configuring a web app manifest
- Debugging PWAs and service workers

## Future Improvements

## Some potential improvements:

- Better input validation and error handling
- Categories for transactions
- Visual charts of spending
- Service worker for offline support
- Export transaction history

## Credits
- PWA functionality based on Google DevDocs.
- Code based on Brad Traversy's JavaScript Tutorial.
