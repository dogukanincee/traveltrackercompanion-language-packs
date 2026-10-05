# TravelTrackerCompanion Remote Language Packs Repository

Centralized, versioned, public runtime localization asset delivery system for [TravelTrackerCompanion](https://github.com/dogukanincee/TravelTrackerCompanion).

## Architecture & Security Model

- **Permanent English Local Baseline**: English (`en`) remains bundled permanently inside the mobile application binary and acts as the offline-safe fallback.
- **On-Demand Single-Pack Runtime Loading**: The mobile application downloads at most **ONE** non-English language pack at a time when explicitly selected by the user.
- **Integrity Verification**: Every pack is verified against SHA-256 checksums and byte sizes published in `manifest.json`.
- **Zero Secrets**: Language packs contain user interface string data only — zero API keys, secrets, or internal infrastructure tokens.

## Endpoints

- **Manifest**: `https://dogukanincee.github.io/traveltrackercompanion-language-packs/manifest.json`
- **Packs**: `https://dogukanincee.github.io/traveltrackercompanion-language-packs/packs/<lang>.json`
