# License System

States:

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

Architecture:

LicenseService
    ↓
LicenseValidator
    ↓
LicenseProvider
    ↓
External Provider

Private secrets must remain server-side.
