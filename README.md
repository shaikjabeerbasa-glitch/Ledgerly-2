# Ledgerly

A lightweight personal finance dashboard built with vanilla HTML, CSS, and JavaScript.

Ledgerly helps you manage accounts, transactions, recurring bills, budgets, and categories in one local-first app. It is designed for people who want a simple, private, browser-based financial tool without needing a backend, subscription, or heavy framework.

## Why this project exists

Managing personal finances often becomes messy when data is scattered across spreadsheets, notes, banking apps, and manual logs. Ledgerly aims to solve that by giving users a clear and focused workspace to:

- track income and spending
- organize transactions by category
- set monthly budgets
- manage recurring transactions
- review trends and totals in a dashboard
- keep data safe with backups and undo support

## Features

- Multi-account tracking for personal finance records
- Transaction management with create, edit, delete, filter, sort, and bulk actions
- Category hierarchy with nested parent/child organization
- Budget tracking with monthly limits and warning states
- Recurring transaction scheduling
- Dashboard charts and summary metrics
- CSV import and export
- JSON backup and restore functionality
- Undo/redo support for the current session
- Dark mode and responsive layout
- Local browser persistence using `localStorage`

## Tech stack

- HTML5
- CSS3
- JavaScript (ES modules)
- Canvas charts
- localStorage for persistence
- Node.js + jsdom for tests

## Project structure

```text
Ledgerly/
├── index.html
├── styles.css
├── package.json
├── package-lock.json
├── README.md
├── js/
│   ├── app.js
│   ├── render.js
│   ├── routing.js
│   ├── state.js
│   ├── storage.js
│   └── validation.js
├── tests/
│   ├── core.test.js
│   └── dom.test.js
└── .gitignore
```

## Getting started

### Prerequisites

- Node.js
- Modern browser
- Optional: Live Server extension for VS Code

### Install dependencies

```bash
npm install
```

### Run the app locally

Because this project uses ES modules, it should be served through a local web server instead of opened directly as a file.

#### Option 1: Live Server

1. Open the project folder in VS Code
2. Right-click `index.html`
3. Select "Open with Live Server"

#### Option 2: Python server

```bash
cd "/path/to/Ledgerly"
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Screenshots

The app includes views for:

- Dashboard
- Accounts
- Transactions
- Budgets
- Categories
- Recurring transactions
- Settings



## Data handling and safety

- Data is saved in the browser using `localStorage`
- Invalid or corrupted stored state is detected and preserved for recovery
- JSON backups are validated before applying changes
- CSV imports are validated before new records are added
- Undo/redo protects against accidental changes in-session

## Notes

This project is a local-first finance tracker and is especially useful for learning front-end app architecture, state management, validation, CSV handling, and browser-based persistence.

## License

This project is provided as-is for personal and educational use.

## Summary

Ledgerly is a clean, local-first finance manager built to make everyday money tracking easier, more structured, and more transparent without the overhead of a full SaaS product.


