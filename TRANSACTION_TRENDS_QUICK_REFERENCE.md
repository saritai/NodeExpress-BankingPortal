# Transaction Trends - Quick Reference Guide

## 🎯 Overview
Add a "Transaction Trends" analytics page that helps users understand their spending patterns across all accounts.

## ⏱️ Estimated Time: 6-8 hours

---

## 📋 Implementation Checklist

### Phase 1: Foundation (2 hours)
- [ ] Add trend calculation functions to `src/data.js`:
  - `getAllTransactions(accounts)` - aggregate all transactions
  - `categorizeTransactions(transactions)` - group by merchant patterns
  - `calculateTrendMetrics(transactions)` - compute statistics
  - `getTransactionsByType(transactions)` - separate debits/credits
  - `getTopMerchants(transactions, limit)` - find top merchants

- [ ] Add route to `src/routes/services.js`:
  ```javascript
  router.get('/trends', (req, res) => {
    const trendData = calculateTrends(accounts);
    res.render('trends', { title: 'Transaction Trends', ...trendData });
  });
  ```

- [ ] Create `src/views/trends.ejs` with basic structure:
  ```ejs
  <%- include('header') %>
  <h1>Transaction Trends</h1>
  <!-- Content here -->
  <%- include('footer') %>
  ```

### Phase 2: Core Functionality (3 hours)
- [ ] Display overall statistics (total transactions, debits, credits, net change)
- [ ] Show transaction type breakdown (debit vs credit with percentages)
- [ ] Implement merchant categorization (Food, Shopping, Income, etc.)
- [ ] Display spending by category with percentages
- [ ] Show account comparison (transactions and spending per account)
- [ ] Display top 5 merchants by spending

### Phase 3: Polish & Testing (2-3 hours)
- [ ] Format all currency values properly ($X,XXX.XX)
- [ ] Style tables using existing `.data-panel` CSS class
- [ ] Handle edge cases (no transactions, empty accounts)
- [ ] Add navigation link in `src/views/index.ejs`
- [ ] Write tests (if test infrastructure exists for this module)
- [ ] Manual testing and QA
- [ ] Documentation updates

---

## 💡 Key Metrics to Display

### Summary Statistics
- Total transactions
- Total debits
- Total credits  
- Net change
- Average transaction amount

### By Type
- Debit count, total, percentage
- Credit count, total, percentage

### By Category
Top categories with spending and percentages:
- Food & Dining
- Shopping
- Income
- Transfers
- Other

### By Account
- Checking spending and transaction count
- Savings spending and transaction count
- Credit Card spending and transaction count

### Top Merchants
Top 5 merchants by total amount spent

---

## 🏗️ Category Patterns

```javascript
const categoryPatterns = {
  'Food & Dining': ['CAFE', 'RESTAURANT', 'GROCER', 'FOOD'],
  'Shopping': ['STORE', 'RETAIL', 'ACME', 'GAMES', 'BOOKSTORE'],
  'Income': ['EMPLOYER', 'SALARY', 'PAYCHECK'],
  'Transfers': ['XFER', 'TRANSFER', 'INST XFER'],
  'Bills & Utilities': ['UTIL', 'ELECTRIC', 'WATER'],
  'Other': [] // Default
};
```

---

## 📁 Files to Create/Modify

### Create:
- `src/views/trends.ejs` - Main trends view

### Modify:
- `src/data.js` - Add trend calculation functions
- `src/routes/services.js` - Add GET /services/trends route
- `src/views/index.ejs` - Add navigation link

---

## 🧪 Testing Checklist

### Manual Tests:
- [ ] Navigate to /services/trends successfully
- [ ] All metrics display correctly
- [ ] Currency formatted properly
- [ ] Tables styled consistently
- [ ] Link from index works
- [ ] No console errors

### Edge Cases:
- [ ] Works with empty accounts
- [ ] Works with no transactions
- [ ] Handles unknown merchant names
- [ ] All percentages sum correctly

---

## 🎨 UI Components

Use existing patterns:
- `<table class="data-panel">` for all tables
- `<div class="container">` for header sections
- `<%- include('header') %>` and `<%- include('footer') %>`
- Currency: `$<%= amount.toFixed(2) %>`
- Back link: `<a href="/">Back to Account Summary</a>`

---

## 🚫 Out of Scope (Future Enhancements)

- Date range filtering
- Interactive charts/graphs
- Export to CSV/PDF
- Custom categories
- Budget tracking
- Mobile optimization
- Recurring transaction detection

---

## ⚠️ Important Notes

1. **Reuse existing patterns** - Follow the style of transfer.ejs and payment.ejs
2. **Keep it simple** - No new dependencies or libraries
3. **Server-side analysis** - Calculate everything in the route handler
4. **Edge cases matter** - Handle missing/empty data gracefully
5. **Test incrementally** - Build and test each metric separately

---

## 📊 Sample Output Structure

```javascript
{
  title: 'Transaction Trends',
  summary: {
    totalTransactions: 10,
    totalDebits: 958.09,
    totalCredits: 2100.00,
    netChange: 1141.91,
    avgTransaction: 305.81
  },
  byType: {
    debits: { count: 8, total: 958.09, percentage: 31.3 },
    credits: { count: 2, total: 2100.00, percentage: 68.7 }
  },
  byCategory: [
    { name: 'Income', count: 2, total: 2100.00, percentage: 68.7 },
    { name: 'Shopping', count: 2, total: 382.15, percentage: 12.5 }
  ],
  byAccount: [
    { name: 'Checking', count: 4, total: 203.82 },
    { name: 'Savings', count: 2, total: 600.00 },
    { name: 'Credit Card', count: 3, total: 382.15 }
  ],
  topMerchants: [
    { name: 'SHARP*EMPLOYER', count: 1, total: 2100.00 },
    { name: 'WITHDRAWL', count: 1, total: 600.00 }
  ]
}
```

---

## 🔗 Quick Links

- Full Plan: [TRANSACTION_TRENDS_IMPLEMENTATION_PLAN.md](./TRANSACTION_TRENDS_IMPLEMENTATION_PLAN.md)
- Express Routing Docs: https://expressjs.com/en/guide/routing.html
- EJS Docs: https://ejs.co/

---

**Ready to implement?** Start with Phase 1 and build incrementally!
