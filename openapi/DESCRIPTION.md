# Real Estate API - Focused Specification

> OpenAPI specification for <api.realestateapi.com> tailored for use with the `{landrise.reapi}` R package.

## Endpoints

Includes specifications for the Real Estate API endpoints used by the `{landrise.reapi}` R package:

- `/v1/PropertyParcel`
- `/v2/AutoComplete`
- `/v2/PropertyDetail`
- `/v2/PropertySearch`
- `/v2/PropertySearch/odata`
- `/v2/PropGPT`
- `/v3/PropertyComps`

## Specification Details

This specification was generated using a hybrid approach, consolidating information from multiple sources:

- Original [`swagger.json`](https://api.realestateapi.com/swagger.json) Specification from [Real Estate API Swagger UI](https://api.realestateapi.com/swagger#/v2)

- Official Documentation from <developer.realestateapi.com/reference> 

- Downloaded request and response schemas from each endpoint's dedicated documentation sources:
  - [AutoComplete API](https://developer.realestateapi.com/reference/autocomplete-api.md)
  - [Property Boundary (Parcel) API](https://developer.realestateapi.com/reference/property-parcel-api.md)
  - [Property Detail API](https://developer.realestateapi.com/reference/property-detail-api-1.md)
  - [Property Search API](https://developer.realestateapi.com/reference/property-search-api.md)
  - [Property Comps (v3) API](https://developer.realestateapi.com/reference/v3-comps-response-object.md)
  - [PropGPT API](https://developer.realestateapi.com/reference/propgpt-api.md)

- [RealEstateApi/docs](https://github.com/RealEstateApi/docs) GitHub repository

- Enhanced request schemas with validation rules through API usage and patterns
- Captured response structures from live API traffic
- Real examples from actual usage
- Complete documentation for all endpoints

## Authentication

<SecurityDefinitions />
