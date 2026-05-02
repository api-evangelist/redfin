# Redfin (redfin)

Redfin is a technology-powered real estate brokerage that provides property search, home value estimates (Redfin Estimate), listing details, neighborhood statistics, commute data, and downloadable housing market data across the United States. Their platform exposes a Stingray REST API used internally by Redfin.com and mobile apps, a GIS CSV Export endpoint for bulk property downloads, and the Redfin Data Center for time-series housing market statistics at national, metro, state, county, city, ZIP code, and neighborhood levels.

**URL:** [https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

Real Estate, Property Data, Home Values, Housing Market, GIS, Listings, CSV Export

## Timestamps

- **Created:** 2026-03-20
- **Modified:** 2026-05-02

## APIs

### Redfin Stingray API

The internal Redfin REST API powering the Redfin website and mobile applications. Provides endpoints for property search, listing details, home value estimates (Redfin Estimate), neighborhood statistics, commute information, and GIS-based map data. Accessible at redfin.com/stingray endpoints.

**Human URL:** [https://www.redfin.com](https://www.redfin.com)

#### Tags

GIS, Home Values, Listings, Property Data, Property Search, Real Estate

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-stingray-api-openapi.yml)
- [SpectralRules](rules/redfin-rules.yml)
- [NaftikoCapeability](capabilities/shared/stingray-api.yaml)

---

### Redfin GIS CSV Export API

Provides bulk property data downloads in CSV format. Returns up to 350 property records per request including address, price, beds, baths, square footage, lot size, year built, days on market, property type, and listing status.

**Human URL:** [https://www.redfin.com](https://www.redfin.com)

#### Tags

Bulk Data, CSV, Export, GIS, Property Data, Real Estate

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-gis-csv-api-openapi.yml)

---

### Redfin Data Center

Downloadable housing market data at national, metro, state, county, city, ZIP code, and neighborhood levels. Datasets cover median sale prices, homes sold, new listings, days on market, inventory, and price drops. Distributed as compressed TSV files from Amazon S3, updated weekly and monthly.

**Human URL:** [https://www.redfin.com/news/data-center/](https://www.redfin.com/news/data-center/)

#### Tags

Analytics, CSV, Housing Market, Market Data, Real Estate, Statistics

#### Properties

- [Documentation](https://www.redfin.com/news/data-center/)
- [OpenAPI](openapi/redfin-data-center-openapi.yml)
- [JSONSchema](json-schema/redfin-market-tracker-schema.json)
- [JSONSchema](json-schema/redfin-property-schema.json)
- [JSON-LD](json-ld/redfin-context.jsonld)
- [JSONStructure](json-structure/redfin-property-structure.json)
- [JSONStructure](json-structure/redfin-market-tracker-structure.json)
- [NaftikoCapeability](capabilities/shared/data-center.yaml)
- [Vocabulary](vocabulary/redfin-vocabulary.yml)

---

## Capabilities

### Shared Definitions

| File | Description |
|---|---|
| [capabilities/shared/stingray-api.yaml](capabilities/shared/stingray-api.yaml) | Stingray API — property search, details, AVM, neighborhood, commute |
| [capabilities/shared/data-center.yaml](capabilities/shared/data-center.yaml) | Data Center — market tracker dataset downloads at all geographic levels |

### Workflow Capabilities

| File | Description |
|---|---|
| [capabilities/property-research.yaml](capabilities/property-research.yaml) | Property Research — search, listing details, AVM, neighborhood stats, commute |
| [capabilities/market-analytics.yaml](capabilities/market-analytics.yaml) | Market Analytics — regional trends and bulk market data downloads |

## Examples

| File | Description |
|---|---|
| [examples/redfin-gis-search-example.json](examples/redfin-gis-search-example.json) | GIS property search request and response |
| [examples/redfin-property-details-example.json](examples/redfin-property-details-example.json) | Above-the-fold property detail request and response |
| [examples/redfin-market-tracker-example.json](examples/redfin-market-tracker-example.json) | Market tracker TSV sample record |

## Common Properties

- [Website](https://www.redfin.com)
- [Blog](https://www.redfin.com/news/)
- [Support](https://support.redfin.com)
- [PrivacyPolicy](https://www.redfin.com/about/privacy-policy)
- [TermsOfService](https://www.redfin.com/about/terms-of-use)
- [Login](https://www.redfin.com/login)
- [DataCenter](https://www.redfin.com/news/data-center/)
- [LinkedIn](https://www.linkedin.com/company/redfin)
- [X](https://twitter.com/redfin)
- [InvestorRelations](https://investors.redfin.com/)
- [GitHubOrg](https://github.com/redfin)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
