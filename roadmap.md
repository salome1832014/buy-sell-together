# Marketplace roadmap

- [ ] Build the first-screen marketplace with shopping and seller entry points.
- [ ] Support buyer and seller access in the same account, with optional email and phone profile details.
- [ ] Brand the marketplace as “Buy and Sell Together.”
- [ ] Connect Shopify catalog and cart/checkout; keep marketplace seller listing support distinct from the single Shopify store.
- [ ] Complete signup, profile storage, and seller listing persistence after Lovable Cloud setup is available.
- [ ] Replace the temporary marketplace name when the user provides one.

## Seller commissions and dashboards

- [ ] Add a seller dashboard showing that seller's completed sales, monthly sales total, commission due, payment history, and settlement status.
- [ ] Add an owner-only dashboard listing all sellers, each seller's monthly completed sales, commission due, payments received, outstanding balances, and total owner commission.
- [ ] Set the marketplace commission to 30% for the app owner and 70% for the seller.
- [ ] Calculate the monthly commission from the value of completed sales for that seller: owner share = sales total × 0.30; seller share = sales total × 0.70.
- [ ] Exclude cancelled and fully refunded orders from commission calculations; account for partial refunds by reducing the eligible sales total.
- [ ] Generate a monthly statement for each seller and let sellers contact the owner and pay the 30% commission monthly.
- [ ] Let the owner record and confirm each commission payment, including payment date, amount, reference/proof, and the month settled; keep an auditable payment history.
- [ ] Show unpaid, partially paid, and paid statuses, and carry any unpaid balance forward without counting it as a new sale.
- [ ] Enforce role-based access so sellers can see only their own sales and statements, while only the app owner can see all sellers and platform-wide commission totals.
- [ ] Obtain seller acceptance of the 30%/70% commission terms before enabling seller listings.

Implementation note: database/schema changes must be made through the connected Lovable editor. Do not implement commission settlement by assuming Shopify checkout automatically splits payments between sellers; the marketplace needs its own seller accounting and settlement records.
