# Ledgerly — Private Finance Tracker

A private, mobile-first personal finance workspace for manually recording bank accounts, bank-statement entries, and cash movements. Each signed-in user's records are persisted in the managed database and remain scoped to that user. Ledgerly does not connect to banks or import or upload statements.

The interface includes Overview, Activity, Accounts, and Categories views, plus an installable PWA shell. New transactions can be queued in IndexedDB while offline and are replayed when connectivity returns. An idempotency key prevents duplicate inserts if a server response is lost during a retry. The app caches the last loaded overview locally for offline access on the same browser profile. Activity can be exported using the browser print dialog; choose “Save as PDF” (on iOS, use the print/share sheet).

## Development

- `pnpm dev` — start the React/Express app on the configured runtime port.
- `pnpm check` — run TypeScript checks.
- `pnpm test` — run the test suite.
- `pnpm build` — build the frontend and server.
- `pnpm db:migrate` — apply checked-in Drizzle migrations.

The application uses Manus OAuth and server-side user-scoped access checks. Development and published runtime share the managed database; database changes should be additive and migrations should be reviewed before running. Before deploying this version, apply the new `0002_offline_entry_idempotency` migration with `pnpm db:migrate`; the offline retry protection requires the `clientMutationId` column and unique index.
