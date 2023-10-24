# Notes on DateTime

- Server: store DateTime in ISO 8601 format, UTC timezone (e.g. `2023-01-01T00:00:00Z`)
- Server, client: use libraries (e.g. `date-fns`)
- `Date.toLocaleDateString`: always explicitely pass formatting options to avoid unexpected results in some locales
