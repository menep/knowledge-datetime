# Notes on DateTime

## Server
- always store DateTime in ISO 8601 format, UTC timezone (e.g. `2023-01-01T00:00:00Z`)
- always use libraries for DateTime manipulation (e.g. `date-fns`) ^1

## Web
- always use libraries for DateTime manipulation (e.g. `date-fns`) ^1

## Date object
- `toLocaleDateString` et al.: always explicitely pass formatting options to avoid unexpected results in some locales
- only create dates from string when ISO
- it's useful to store user-provided DateTime values in separate variables as numbers (e.g. `new Date(year, zeroIndexedMonth, day, hours, minutes, seconds)`)

## Formats
- never take the order for granted (e.g. `11/10/1990` could mean `1990-10-11` or `1990-11-10`)

## Node.js
- make sure `full-icu` is enabled when running test suites or formatting might default to `en-US`
