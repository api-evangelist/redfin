# Redfin (redfin)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
