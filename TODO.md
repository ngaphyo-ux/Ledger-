# Ledgerly — Build Outcomes

## Secure private access and persistent ledger data
- [x] Require secure sign-in before personal finance records can be read or changed. Persist accounts, opening balances, categories, and manually entered ledger records in the managed relational database so they survive reloads and sessions.
- [x] Scope every account, category, ledger entry, overview result, and edit operation to the signed-in user. Validate that any account and category referenced by an entry belong to that same user.
- [x] Show the logged-out sign-in state until a real authenticated session is established; do not expose or seed another user's financial records.

## Accounts and account balances
- [x] Let the signed-in user create and edit each individual bank account with account name, institution, optional last four digits, and opening balance.
- [x] Show current balance for each account, calculated from its opening balance and recorded cash-in/cash-out activity, in the overview and Accounts view.

## Manual activity records
- [x] Let the signed-in user create and edit ledger entries assigned to one of their bank accounts and, optionally, one of their categories. Each entry must have record type cash or bank statement; flow cash-in or cash-out; amount; date; description; and optional remarks.
- [x] Clearly distinguish money in from money out and show the signed amount, date, account, category, and record type in the activity timeline. Updates must flow through to totals and balances.
- [x] Keep record entry manual. Do not add direct bank connections, automatic bank feeds, CSV imports, or bank-statement uploads.

## Categories and defaults
- [x] Let the signed-in user create and edit categories classified as income, expense, or both, and choose an accent color for each category.
- [x] When a user has no categories, create their own defaults: Salary, Transfer in, Groceries, Bills, Transport, and Other.

## Overview and navigation
- [x] Provide an overview headed “PW9 Bank Accounts Balance” with total account position, money in, money out, net movement, recent activity, and current balances by account.
- [x] Provide Overview, Activity, Accounts, and Categories views with touch-friendly mobile bottom navigation and desktop side navigation.
- [x] Keep the interface responsive and usable on phone-size screens and larger screens, with clear empty, loading, error, and save-feedback states.

## Installable PWA and Signal Deck presentation
- [x] Include installable PWA metadata and app icons, an offline-friendly application shell, and clear install, online, and offline status feedback.
- [x] Preserve the approved Signal Deck visual direction from the uploaded reference: compact high-contrast field-instrument styling, dark navy surfaces, blue and vivid yellow accents, green income and red expense states, sharp panels, Space Grotesk typography, technical clarity, and touch-friendly controls.
