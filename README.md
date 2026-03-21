# Redfin (redfin)
Redfin is a technology-powered real estate brokerage that provides property search, home value estimates, and housing market data across the United States. Their platform offers APIs for property listings, GIS-based map data, and downloadable market statistics at national, metro, city, and neighborhood levels.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Real Estate, Property Data, Home Values, Housing Market, GIS, Listings

## Timestamps

- **Created:** 2026-03-20
- **Modified:** 2026-03-20

## APIs

### Redfin Stingray API
The Redfin Stingray API is the internal REST API that powers the Redfin website and mobile applications. It provides endpoints for property search, listing details, home value estimates (Redfin Estimates), neighborhood statistics, commute information, and GIS-based map data. The API supports searching by region, price range, property type, and various filters, returning structured JSON responses with property details including address, price, beds, baths, square footage, lot size, and days on market. While not officially documented by Redfin, this API has been reverse-engineered by the developer community and is accessible at redfin.com/stingray endpoints.

**Human URL:** [https://www.redfin.com](https://www.redfin.com)


#### Tags:

 - Real Estate, Property Search, Listings, Home Values, Property Data, GIS

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-stingray-api-openapi.yml)

### Redfin GIS CSV Export API
The Redfin GIS CSV Export API provides bulk property data downloads in CSV format. This endpoint returns up to 350 property records per request in tabular format, making it suitable for data analysis and spreadsheet workflows. It accepts parameters for market selection, price ranges, bedroom and bathroom counts, region identifiers, and property status filters. The CSV output includes fields such as address, list price, property type, square footage, lot size, and listing status, enabling developers and analysts to aggregate property data for research and comparison purposes.

**Human URL:** [https://www.redfin.com](https://www.redfin.com)


#### Tags:

 - Real Estate, Property Data, CSV, Bulk Data, GIS, Export

#### Properties

- [Documentation](https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md)
- [OpenAPI](openapi/redfin-gis-csv-api-openapi.yml)

### Redfin Data Center
The Redfin Data Center provides downloadable housing market data for metropolitan areas, cities, neighborhoods, and zip codes across the United States. Data is available at national, metro, state, county, city, zip code, and neighborhood levels. Weekly data is updated every Wednesday with new data for the prior week, computed as rolling 1, 4, or 12-week windows. Monthly data is released during the Friday of the third full week of each month. The platform enables users to visualize trends and download datasets covering median sale prices, homes sold, new listings, days on market, inventory levels, and price drops.

**Human URL:** [https://www.redfin.com/news/data-center/](https://www.redfin.com/news/data-center/)


#### Tags:

 - Real Estate, Housing Market, Market Data, Statistics, Analytics, CSV

#### Properties

- [Documentation](https://www.redfin.com/news/data-center/)
- [Documentation](https://support.redfin.com/hc/en-us/articles/360016476931-Downloading-Data)
- [OpenAPI](openapi/redfin-data-center-openapi.yml)

## Common Properties

- [Website](https://www.redfin.com)
- [Blog](https://www.redfin.com/news/)
- [Support](https://support.redfin.com)
- [PrivacyPolicy](https://www.redfin.com/about/privacy-policy)
- [TermsOfService](https://www.redfin.com/about/terms-of-use)
- [Login](https://www.redfin.com/login)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
