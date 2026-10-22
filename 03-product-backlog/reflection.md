# Product Backlog Reflection

## Situation

Students needed a clear Product Catalogue before they could select groceries, build bulk orders or continue to checkout. The catalogue therefore required structured product data, search and filtering support, product availability and prices suitable for student budgets.

## Task

The Trello checklists assigned me responsibility for designing the product database, connecting the catalogue to the database, displaying student discounts and availability, testing catalogue loading performance, and supporting bug fixing and the final review.

## Action

I organised my contribution around the dependency between the database and the frontend catalogue. The portfolio documents the `dfb.products` table in TiDB, the catalogue's database connection and the product fields used by the application. I linked my assigned work to four daily checklist screenshots and direct Trello cards. I also included frontend evidence showing products filtered below R100 and below R200 to demonstrate how structured catalogue data supports budget-based browsing.

## Result

The Product Backlog evidence now connects my assigned contribution to the Trello records, a populated TiDB product query and two frontend price-filter views. This creates clear traceability from planned catalogue work to the available database and interface evidence. Loading-time measurements, formal acceptance-test results and a detailed bug report are not included, so I cannot use these screenshots alone to claim that every catalogue requirement passed testing. I learnt to link backlog items to objective evidence while distinguishing demonstrated progress from unverified outcomes.
