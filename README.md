# Real Estate API - Hybrid OpenAPI Specification

This directory contains the comprehensive OpenAPI specification for the Real Estate API, combining:

- **Official API documentation** from [swagger.json](./swagger.json)
- **Enhanced request schemas** from [inst/schemas/](../../inst/schemas/)
- **Captured response structures** from live API traffic via [mitmproxy](https://mitmproxy.org/)
- **Detailed endpoint documentation** from official per-endpoint specs

## Structure

```plaintext
generated/
├── openapi.yml                 # Main comprehensive OpenAPI 3.1.0 specification
├── components/
│   ├── schemas/               # Request and response schemas
│   │   ├── Property_searchRequest.yml
│   │   ├── Property_searchResponse.yml
│   │   └── ...
│   ├── responses/             # Reusable response definitions
│   ├── parameters/            # Common parameters
│   └── examples/              # Request/response examples
├── paths/                     # Individual endpoint definitions
│   ├── property_search.yml
│   ├── property_detail.yml
│   └── ...
└── README.md                  # This file
```

## Features

✅ **Complete Request Validation**: Combines official schemas with enhanced validation rules  
✅ **Actual Response Structures**: Documents real API responses from captured traffic  
✅ **Comprehensive Documentation**: Detailed descriptions and examples for all endpoints  
✅ **OpenAPI 3.1.0 Compliant**: Modern specification format with proper component organization  
✅ **Security Definitions**: Proper API key authentication documentation  
✅ **Error Response Coverage**: Documents all HTTP status codes and error conditions  

## Key Endpoints

| Endpoint | Path | Description |
|----------|------|-------------|
| Property Search | `/v2/PropertySearch` | Search and filter properties with advanced criteria |
| Property Detail | `/v2/PropertyDetail` | Get detailed information about specific properties |
| Property Comps | `/v3/PropertyComps` | Find comparable properties for valuation |
| AutoComplete | `/v2/AutoComplete` | Address and location autocomplete |
| PropGPT | `/v2/PropGPT` | AI-powered property search and analysis |
| Property Parcel | `/v1/PropertyParcel` | Property parcel and boundary information |

## Usage

### OpenAPI Tooling

Use the main `openapi.yml` file with OpenAPI tools:

```bash
# Generate client SDKs
openapi-generator generate -i openapi.yml -g typescript-fetch -o client/

# Validate specification  
swagger-codegen validate -i openapi.yml

# Generate documentation
redoc-cli build openapi.yml
```

### Schema Validation
Individual schemas can be used for request validation:

```r
# In R with landrise.reapi
schema <- yaml::read_yaml("components/schemas/Property_searchRequest.yml")
reapi_req_validate(request, schema)
```

## Generation Process

This specification is generated automatically by combining:

1. **Official API schemas** - Base request/response definitions
2. **Enhanced schemas** - Validation rules and constraints  
3. **Captured responses** - Real response structures from API traffic
4. **Documentation** - Descriptions and examples from official docs

To regenerate:

```r
source("dev/generate_hybrid_spec.R")
source("dev/fix_generated_spec.R")
```

## Validation Status

- ✅ OpenAPI 3.1.0 specification format
- ✅ All referenced components exist  
- ✅ Schema definitions are consistent
- ✅ Security schemes properly defined
- ✅ Response structures match actual API behavior

Generated on: 
