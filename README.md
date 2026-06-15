# Redfin (redfin)

Redfin is a technology-powered real estate brokerage that provides property search, home value estimates, listing details, neighborhood statistics, commute data, and downloadable housing market data across the United States. Their platform exposes a Stingray REST API used by the Redfin website and mobile apps, a GIS CSV Export endpoint for bulk property downloads, and the Redfin Data Center for time-series housing market statistics at national, metro, state, county, city, ZIP code, and neighborhood levels.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- CSV Export
- GIS
- Home Values
- Housing Market
- Listings
- Property Data
- Real Estate

## Timestamps

- **Created:** 2026-03-20
- **Modified:** 2026-05-19

## APIs

### Redfin Stingray API

The Redfin Stingray API is the internal REST API powering the Redfin website and mobile applications. It provides endpoints for property search, listing details, home value estimates (Redfin Estimate), neighborhood statistics, commute information, and GIS-based map data. Accessible at redfin.com/stingray endpoints and reverse-engineered by the developer community.

- **Human URL:** [https://www.redfin.com](https://www.redfin.com)

#### Tags

- GIS
- Home Values
- Listings
- Property Data
- Property Search
- Real Estate

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-stingray-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/redfin-stingray-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/redfin-stingray-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Spectral Rules](rules/redfin-rules.yml)
- [Naftiko Capeability](capabilities/shared/stingray-api.yaml)

### Redfin GIS CSV Export API

The Redfin GIS CSV Export API provides bulk property data downloads in CSV format. Returns up to 350 property records per request including address, price, beds, baths, square footage, lot size, year built, days on market, property type, and listing status.

- **Human URL:** [https://www.redfin.com](https://www.redfin.com)

#### Tags

- Bulk Data
- CSV
- Export
- GIS
- Property Data
- Real Estate

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-gis-csv-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/redfin-gis-csv-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/redfin-gis-csv-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Redfin Data Center

The Redfin Data Center provides downloadable housing market data for metropolitan areas, cities, neighborhoods, and ZIP codes across the United States. Data is available at national, metro, state, county, city, ZIP code, and neighborhood levels. Datasets cover median sale prices, homes sold, new listings, days on market, inventory, and price drops. Files are served as compressed TSV from Amazon S3.

- **Human URL:** [https://www.redfin.com/news/data-center/](https://www.redfin.com/news/data-center/)

#### Tags

- Analytics
- CSV
- Housing Market
- Market Data
- Real Estate
- Statistics

#### Properties

- [Documentation](https://www.redfin.com/news/data-center/)
- [Documentation](https://support.redfin.com/hc/en-us/articles/360016476931-Downloading-Data)
- [OpenAPI](openapi/redfin-data-center-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/redfin-data-center.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/redfin-data-center.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/redfin-market-tracker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/redfin-property-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/redfin-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Structure](json-structure/redfin-property-structure.json)
- [JSON Structure](json-structure/redfin-market-tracker-structure.json)
- [Naftiko Capeability](capabilities/shared/data-center.yaml)
- [Vocabulary](vocabulary/redfin-vocabulary.yml)

## Common Properties

- [Website](https://www.redfin.com)
- [Blog](https://www.redfin.com/news/)
- [Support](https://support.redfin.com)
- [Privacy Policy](https://www.redfin.com/about/privacy-policy)
- [Terms of Service](https://www.redfin.com/about/terms-of-use)
- [Login](https://www.redfin.com/login)
- [Data Center](https://www.redfin.com/news/data-center/)
- [News](https://www.redfin.com/news/)
- [LinkedIn](https://www.linkedin.com/company/redfin)
- [X (Twitter)](https://twitter.com/redfin)
- [Investor Relations](https://investors.redfin.com/)
- [Git Hub Org](https://github.com/redfin)
- [Naftiko Capeability](capabilities/property-research.yaml)
- [Naftiko Capeability](capabilities/market-analytics.yaml)
- [Integrations](https://www.redfin.com/partners)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
