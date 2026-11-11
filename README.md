# GeoNames API — Postman Collection (gazetteer for genealogy)

A Postman (v2.1) collection with 23 requests for the **[GeoNames](https://www.geonames.org) web services**. GeoNames lists more than 12 million places worldwide, including their **historic and alternate names**, administrative hierarchy and coordinates. It is useful for turning place names found in old records (*Nagybecskerek*, *Gross-Betschkerek*, *Beodra*) into modern places (*Zrenjanin*, *Novo Miloševo*), and for working out which county or diocese archive covers a village.

**Import link** (Postman → Import → Link):
```
https://raw.githubusercontent.com/mikeyeves/GeoNames-API-Postman/main/GeoNames_API.postman_collection.json
```

## Setup (one time, free)
1. Create an account at https://www.geonames.org/login.
2. Confirm the email, then go to https://www.geonames.org/manageaccount and click **"Click here to enable"** for free web services.
3. In Postman, set the collection variable `geonames_username` to your username. The collection auth then adds `username=…` to every request.

Free limits are 10,000 credits per day and 1,000 per hour. The shared `demo` account usually runs out of credits early in the day, so use your own.

## Folders
| Folder | Requests | Notes |
|---|---|---|
| ★ Search places | 8 | Search all fields, **historic or alternate names**, exact name, fuzzy (misspellings), name prefix, local-language names, churches or cemeteries in an area |
| Place details & hierarchy | 6 | Full record with every alternate name, **administrative hierarchy**, subdivisions, neighbouring places, country info |
| Reverse geocoding | 4 | Nearest village, nearby features, subdivision and timezone for a coordinate |
| Postal codes | 3 | Search by place name, look up a code, find codes near a point |
| Wikipedia | 2 | Geotagged Wikipedia articles |

Each request includes a **Visualizer** results table. The *Search* requests also save the first result's `geonameId` to a variable, so you can run *Hierarchy* or *Get place* straight after.

## Status
Every call needs a personal username, so these requests have **not been run live**. They follow the [official documentation](https://www.geonames.org/export/ws-overview.html). The endpoint itself is online: a call with the shared `demo` user returned GeoNames' normal "daily limit exceeded" message.

## Feature codes worth knowing
| Code | Meaning |
|---|---|
| `P` / `PPL` | populated place (feature class / code) |
| `CH` | church |
| `CMTY` | cemetery |
| `MSTY` | monastery |
| `ADM1`–`ADM4` | administrative divisions |
| `PPLH` | historical populated place |

## Related collections
[Kartverket place names (Norway bundle)](https://github.com/mikeyeves/Digitalarkivet-API-Postman) · [Wikidata places (European Archives)](https://github.com/mikeyeves/European-Archives-APIs-Postman) · [Logainm and OS Names (UK and Ireland)](https://github.com/mikeyeves/UK-Ireland-Archives-APIs-Postman)

*Unofficial. Not affiliated with GeoNames. GeoNames data is licensed CC BY 4.0.*
