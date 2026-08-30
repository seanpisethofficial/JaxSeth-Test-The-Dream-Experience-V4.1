# 🇰🇭 License System — មេរៀន

## States

CHECKING
ACTIVE
NOT_FOUND
EXPIRED
REVOKED
INVALID
USER_MISMATCH
PRODUCT_MISMATCH
SERVICE_UNAVAILABLE
VERSION_UNSUPPORTED

## Architecture

LicenseService
↓
LicenseValidator
↓
LicenseProvider
↓
External Provider

## Security

License Secret មិនត្រូវបង្ហាញទៅ Client។

បើ External API ត្រូវការ Secret:

Secret ត្រូវរក្សាទុកតែ Server-side។

## License Not Found

UI អាចបង្ហាញ:

LICENSE NOT FOUND

Product
Version
Status

ប៉ុន្តែមិនត្រូវបង្ហាញ private verification details។
