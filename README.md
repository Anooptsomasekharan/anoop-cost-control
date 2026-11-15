# Anoop Group of Restaurants – Cost Control & Analytics (demo)

A single-page F&B cost control and analytics website for a multi-brand restaurant group: 5 brands, 8 outlets, 12 months of data.

**All figures are sample data for a fictional group.** No real company data is included.

## What it covers
- Leadership Summary: gross and net sales, net contribution, customers, average check, sales targets by brand and outlet
- Menu engineering: where each item's selling price goes (food, packaging, commission, promos, net)
- Recipe costing: food cost, packaging cost, total cost and online cost per item
- Promotions: 10%, 30% and 50% offers for online and offline sales, by brand, with the extra sales each offer needs and recipes to promote or avoid
- Delivery and channels, packaging, purchasing (GRPO prices, suppliers, purchase loss)
- Cost control: recipe variance, loss by product, wastage, stock counts, reconciliation
- Cold drinks include ice cubes in their recipes
- Users & access: sign-in screen, and an admin page to create users and choose the pages each one can open

## How to view
Open `index.html` in a browser, or enable GitHub Pages for this repository (Settings → Pages → Deploy from branch → `main` / root).

The page is self-contained: one HTML file with the data, charts and styles inside it.

## Sign in
Demo administrator login:

- Username: `admin`
- Password: `Anoop@2026`

The administrator opens **Users & access** (under Admin in the side menu) to add users, set their passwords and tick the pages they can open.

Two limits of this demo login:

- It is a screen lock, not real security. The sample data is inside the page, so do not put confidential data in this version.
- On this GitHub copy, users you create are saved only in the browser where you create them. They do not work on other devices.

## Data model
The sample data follows 16 tables.

| Type | Tables |
| --- | --- |
| Master | Brands, Outlets, Suppliers, Items, Contract_Prices, Menu_Items, Recipe_Lines, Sales_Channels, Employees |
| Transaction | Sales, GRPO_Lines, Wastage_Log, Stock_Counts, Sales_Targets, Large_Checks, Employee_Monthly |

ID columns link the tables: `Outlet_ID`, `Brand_ID`, `Supplier_ID`, `Item_Code`, `Menu_Item_Code`, `Channel_ID`, `Employee_ID`. Cost %, leakage, net contribution and menu classes are calculated by the page, not stored.

The site currently generates this sample data inside the page. It does not yet read from a spreadsheet.
