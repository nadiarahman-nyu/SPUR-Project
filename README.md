# SPUR Project

SPUR explores whether AI and data tools can help reduce environmental harm in
fashion while keeping worker well-being in view.

Project site: https://nadiarahman-nyu.github.io/SPUR-Project/

- [Sustainable planning prototype](docs/index.html)
- [H&M research notes](docs/hm-research.html)
- [How to use the prototype](docs/how-to-use.html)

## Sustainable demand planning prototype

Open [`docs/index.html`](docs/index.html) in a browser, or publish the `docs/`
folder with GitHub Pages. The self-contained prototype demonstrates:

- A transparent, illustrative product-demand forecast from recent sales,
  search/social interest changes, and current inventory.
- Sustainability-first inventory suggestions, including pausing orders,
  checking transfers, and considering resale or repair before producing more.
- Optional company-level revenue and inventory context transcribed from a
  financial statement or annual report.
- CSV import for authorized product-level sales and stock data.

The sample values are fictional. The page does not automatically connect to SEC
EDGAR, Google Trends, TikTok, or other sites. Public filing data is generally
company-level; it cannot substitute for product/store sales history. Public
search and social signals need to be collected with permitted sources and
entered for comparable terms and time windows. Enter source links to retain
provenance; non-US companies may publish annual reports or Form 20-F rather than
a US Form 10-K. Retail price forecasts are not implemented; the cost/interest
indicator is directional context only.

The forecast is a simple, inspectable baseline—not a validated AI model. The
emissions figure is an estimate of emissions associated with excess stock using
the uploaded per-unit factor; it is not a measured reduction or avoided
emissions claim. Validate forecasts and sustainability outcomes against actual
sales, production, returns, disposal, and supplier data before making business
decisions. CSV processing happens in the browser; this static prototype does
not upload the selected file to a server.

CSV required columns: `product, inventory, units_sold`.

Optional columns: `category, previous_units_sold, search_change_pct,
social_change_pct, material_cost_change_pct, emissions_kg_per_unit,
lead_time_days, source_url`.
