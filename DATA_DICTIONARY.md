# Raw Dataset — Data Dictionary

All records are synthetic and created for portfolio demonstration. Currency is Indonesian Rupiah (IDR). Dates use ISO format `YYYY-MM-DD`.

| File | Description |
|---|---|
| `chart_of_accounts.csv` | Chart of accounts with account type and normal balance. |
| `opening_balances.csv` | Balanced opening balances as of 1 January 2025. |
| `product_master.csv` | Product master with unit, standard selling price, and opening stock assumptions. |
| `opening_inventory.csv` | Opening quantity and inventory value by SKU. |
| `sales_transactions.csv` | Invoice line items, sales values, and moving weighted-average cost at sale. |
| `purchase_transactions.csv` | Purchase invoice line items by supplier and SKU. |
| `cash_receipts.csv` | Customer collections linked to sales invoice IDs. |
| `cash_payments.csv` | Supplier and operating expense payments linked to source records. |
| `operating_expenses.csv` | Monthly operating expense records and account mapping. |

## Key relationships

- `sales_transactions.invoice_id` links to `cash_receipts.invoice_id`.
- `purchase_transactions.purchase_id` links to `cash_payments.reference_id` for supplier payments.
- `operating_expenses.expense_id` links to `cash_payments.reference_id` for operating expense payments.
- `sku` links transaction rows to `product_master.csv` and `opening_inventory.csv`.

## Accounting assumptions

- Reporting period: 1 January–31 December 2025.
- Accounting basis: accrual; inventory system: perpetual.
- Inventory cost flow: moving weighted average, updated chronologically for purchases and sales.
- Sales and purchases are initially recorded on credit; cash settlements are represented separately.
- Customer receipts are scheduled in two installments (65% and 35%). Supplier payments are scheduled in two installments (70% and 30%).
- Some December settlements may occur in January 2026 and remain outstanding at year-end.
- No VAT, income tax, returns, depreciation posting, or loan transactions are included in this initial dataset.
- Opening balances are balanced; opening inventory subledger totals IDR 25,000,000 and agrees with the inventory control account.
