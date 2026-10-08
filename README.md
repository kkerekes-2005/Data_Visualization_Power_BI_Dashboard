# E-Commerce Analytics Dashboard (Power BI)

An interactive Power BI dashboard analyzing an e-commerce business in Spain: sales and profitability, customer behavior, geographic distribution, product reviews and returns. The dashboard itself is in Spanish.

## Overview

The report has five pages, navigable from the left-hand menu:

| Page | What it shows |
|---|---|
| **Visión general** (Overview) | KPIs (total revenue, total cost, profit, average order value, total orders, average rating), revenue vs. cost trend with trendline, orders by status and by purchase channel, revenue by category, year slicer |
| **Un mes en compras** (One month of purchases) | Year and month drill-down: daily profit, payment method distribution, customers by subscription type (Prime/Standard), orders by hour of day |
| **Distribución geográfica** (Geography) | Heat map of orders across Spain and the top 5 regions by revenue vs. cost |
| **Reviews** | Rating distribution, ratings by subcategory, average vs. expected rating by brand, top return reasons, return count |
| **Conclusiones** (Conclusions) | Key findings and business recommendations |

## Screenshots

### Overview
![Overview](screenshots/01_overview.png)

### One month of purchases
![One month](screenshots/02_one_month.png)

### Geographic distribution
![Geography](screenshots/03_geography.png)

### Reviews and returns
![Reviews](screenshots/04_reviews.png)

### Conclusions
![Conclusions](screenshots/05_conclusions.png)

## Data Model

The model is built from seven related tables: `Clientes` (customers), `Pedidos` (orders), `DetallePedidos` (order lines), `Productos` (products), `Reviews`, `Devoluciones` (returns), plus an automatic date table. Key fields include `CanalCompra`, `MetodoPago`, `EstadoPedido`, `TipoSuscripcion`, `Categoria`, `Subcategoria`, `Marca`, `CCAA`, `Ciudad` and `Rating`.

## Key Findings

- Total revenue of about €2.30M with a profit of about €743K, a margin of roughly 32%
- Revenue grows steadily from 2024 to 2026, with pronounced peaks in late 2025
- Electronics accounts for over 50% of revenue (€1.18M)
- The App channel generates 57.7% of orders vs. 42.3% for Web
- Card is the preferred payment method, and purchases peak between 14:00 and 20:00
- Andalucía, Cataluña and Comunidad de Madrid generate the most revenue
- Average rating is 4.19/5, and 80.6% of orders are delivered successfully
- "Defective product" is the top return reason (147 cases), followed by "Damaged packaging" (87)

## Recommendations

1. Invest in the web channel to capture more sales
2. Diversify the catalog, since Food & Beverage and Beauty have very low revenue
3. Reduce returns from defective products by reviewing suppliers and quality control
4. Run campaigns and promotions during peak hours (14:00 to 20:00)
5. Expand into low-revenue regions such as La Rioja, Navarra and Cantabria

## Repository Contents

```
.
├── power_bi_ecommerce_dashboard.pbix   # Power BI file (open with Power BI Desktop)
├── ecommerce_dashboard.pdf             # PDF export of all pages
├── screenshots/                        # One image per dashboard page
├── README.md
└── .gitignore
```

## How to Use

1. Download `power_bi_ecommerce_dashboard.pbix`
2. Open it with [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only)
3. Use the year/month slicers and the left-hand menu to explore

## Tools

Power BI Desktop · DAX · Power Query · Data modeling

## Author

Kinga Kerekes
