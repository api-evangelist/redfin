# Redfin GraphQL Schema

## Overview

This directory contains a conceptual GraphQL schema for the Redfin real estate platform. Redfin does not publish an official GraphQL API; this schema is derived from the publicly documented Redfin Stingray REST API, the GIS CSV Export endpoint, and the Redfin Data Center bulk data downloads.

The schema captures the full domain model of Redfin's platform including property search, listings, agents, market data, mortgage tools, and transaction workflows.

## Source APIs

| API | Base URL | Notes |
|-----|----------|-------|
| Stingray REST API | `https://www.redfin.com/stingray/` | Powers the Redfin website and mobile apps |
| GIS CSV Export | `https://www.redfin.com/stingray/api/gis-csv` | Bulk property downloads, up to 350 records |
| Data Center | `https://www.redfin.com/news/data-center/` | Time-series housing market statistics |

## Schema File

- [`redfin-schema.graphql`](redfin-schema.graphql) — Full GraphQL schema definition

## Type Summary

### Core Property & Listing (8 types)
- `Property` — Root property entity with all attributes, history, and relationships
- `Listing` — Active or historical listing tied to a property
- `ListingStatus` — Status codes (active, pending, contingent, sold, off-market)
- `ListPrice` — Asking price at a point in time
- `SalePrice` — Final closed sale price
- `PriceChange` — Individual price reduction or increase event
- `DaysOnMarket` — Days a listing has been active
- `PropertyType` — Enum of property types (single-family, condo, land, etc.)

### Address & Location (3 types)
- `Address` — Street, unit, city, state, zip, country
- `Location` — Geographic coordinates, county, walk/transit/bike scores, flood zone
- `LatLng` — Latitude/longitude coordinate pair

### Neighborhood (1 type)
- `Neighborhood` — Named area with boundaries, demographics, and market statistics

### Schools (4 types)
- `School` — Individual school record with contact info and distance
- `SchoolScore` — Rating with subcategory scores from third-party sources
- `SchoolType` — Enum (public, private, charter, magnet)
- `SchoolLevel` — Enum (elementary, middle, high, K-12)

### Agents, Teams & Offices (9 types)
- `Agent` — Licensed real estate agent with ratings, reviews, and service details
- `Team` — Group of agents under a shared brand
- `Office` — Physical brokerage office
- `Broker` — Licensed broker overseeing one or more offices
- `AgentRating` — Numeric rating across multiple dimensions
- `ReviewCount` — Star-rating distribution
- `AgentService` — Service model and fee structure
- `BuyerRebate` — Estimated rebate for buyers working with Redfin agents

### Pricing & Estimates (6 types)
- `PriceEstimate` — Redfin Estimate (AVM) with confidence range
- `Estimate` — Wraps price and rent estimates for a property
- `ValueHistory` — Time-series of estimated values
- `MortgageRate` — Current rate quotes by loan type and term
- `BuyingPower` — Affordability calculation based on income and down payment
- `StatedIncome` — Borrower income used in mortgage calculations

### Tax, Comps & Permits (3 types)
- `TaxRecord` — Annual assessed value and tax amount
- `CompSale` — Recent comparable sale used in valuations
- `PermitRecord` — Building permit on record for the property

### Photos & Media (1 type)
- `Photo` — Image with URL, dimensions, caption, and display order

### Showings & Open Houses (4 types)
- `OpenHouse` — Scheduled public showing with type (in-person, virtual)
- `OpenHouseType` — Enum of open house formats
- `ShowingSchedule` — Private showing availability slots
- `ShowingSlot` — Individual available appointment window

### Offers, Contract & Escrow (8 types)
- `Offer` — Buyer offer with price, contingencies, and status
- `OfferStatus` — Accepted, rejected, countered, or pending
- `ContractStatus` — Stage of the purchase agreement
- `ContingencyDeadline` — Individual contingency with due date
- `Escrow` — Escrow company and officer contact
- `Timeline` — Ordered events from listing through closing
- `TimelineEvent` — Single milestone in the transaction

### Closing & Inspection (5 types)
- `Closing` — Final closing details including costs and net proceeds
- `Inspection` — Scheduled or completed property inspection
- `InspectionFinding` — Individual finding from the inspector's report
- `Title` — Title company, status, and insurance coverage
- `HomeReport` — Consolidated property report bundling estimate, comps, permits, and schools

### Search (10 types)
- `Search` — Query with filters, sort, and results
- `SearchResult` — Paginated listing results with map cluster data
- `MapBounds` — North/south/east/west viewport coordinates
- `ClusterGroup` — Map pin cluster with count and price range
- `FilterCriteria` / `FilterCriteriaInput` — Full search filter set
- `SortOption` / `SortOptionInput` — Field and direction for result ordering
- `SortField` — Enum of sortable fields
- `SortDirection` — ASC or DESC

### Saved Searches & Alerts (4 types)
- `SavedSearch` — Persisted search with filters and alert configuration
- `HomeAlert` — Notification rule tied to a saved search
- `AlertFrequency` — Instant, daily, or weekly
- `AlertChannel` — Email, push notification, or SMS

### Market Data (6 types)
- `MarketData` — Snapshot of housing market metrics for a region and time period
- `MarketTrend` — Single metric trend for a region
- `TrendData` — Monthly time series with year-over-year comparison
- `RegionType` — Enum (national, state, metro, county, city, ZIP, neighborhood)
- `TrendDirection` — Up, down, or flat

### User (1 type)
- `User` — Registered user with saved searches, homes, alerts, and buying power

### Root Operations
- `Query` — 20 query fields covering property lookup, search, agents, schools, market data, mortgage rates, and estimates
- `Mutation` — 11 mutation fields for saving searches, scheduling showings, submitting offers, and managing alerts

## Total Named Types

58 named types (object types, enums, and scalars) plus 7 input types.

## Usage Notes

- All monetary values use the `Money` scalar. Clients should treat this as a numeric value in USD.
- The `GeoJSON` scalar represents neighborhood boundary polygons in GeoJSON Feature format.
- `DateTime` values are ISO 8601 strings. `Date` values are `YYYY-MM-DD` strings.
- The `Search` query is the primary entry point for property discovery and maps to the Stingray `/api/gis` and `/api/gis-csv` endpoints.
- `MarketData` types map to the Redfin Data Center CSV exports available at national, metro, state, county, city, ZIP, and neighborhood granularity.

## References

- Redfin Stingray API documentation: https://github.com/alientechsw/RedfinPlus/blob/master/docs/REDFIN.md
- Redfin Data Center: https://www.redfin.com/news/data-center/
- Redfin Data download guide: https://support.redfin.com/hc/en-us/articles/360016476931-Downloading-Data
- Redfin GitHub organization: https://github.com/redfin
