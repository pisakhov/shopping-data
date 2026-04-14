# Shopping Data Marketplace

A web-based data marketplace interface for selecting API endpoints and field mappings to create PostgreSQL tables. This tool provides an interactive UI for browsing financial data providers, selecting API endpoints, configuring field mappings, and deploying data bundles to PostgreSQL.

## Features

- **Multi-Provider Catalog**: Browse data from Bloomberg, FactSet, Haver, and LSEG
- **Interactive Field Mapping**: Select and map API fields to PostgreSQL column types
- **Nested Data Support**: Handle arrays and nested JSON structures with multiple storage strategies
- **Bundle Management**: Create and deploy multiple tables as a single bundle
- **Test & Preview**: Preview data and test API connections before deployment
- **Scheduling**: Configure hourly, daily, weekly, or monthly data refresh schedules

## Usage

1. Open `index.html` in a web browser
2. Load a JSON data folder containing market data files
3. Select a provider (Bloomberg, FactSet, Haver, LSEG)
4. Choose a product and API endpoint
5. Map fields to PostgreSQL types
6. Add to bundle with a custom table name
7. Deploy the bundle when ready

## Data Folder Structure

Place your JSON data files in the `./data` directory with filenames like:
- `bloomberg_eod_pricing.json`
- `bloomberg_equities.json`
- `factset_income_statements.json`
- `haver_macro.json`
- `lseg_esg_scores.json`

## Technology Stack

- **Frontend**: HTML, Tailwind CSS, Vanilla JavaScript
- **Backend**: PostgreSQL (for deployed bundles)
- **Data Sources**: JSON files for market data

## PostgreSQL Field Types Supported

- TEXT
- VARCHAR(255)
- INTEGER
- BIGINT
- DECIMAL
- TIMESTAMP
- DATE
- BOOLEAN
- JSONB
- UUID

## Nested Data Strategies

- **JSONB**: Store nested structures as JSONB
- **child_table**: Create separate child tables
- **flatten**: Flatten nested fields to root level

## License

MIT