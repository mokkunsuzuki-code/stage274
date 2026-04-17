# Stage274: Key Management Model

## Status

- KMS: active
- HSM: compatible
- YubiKey: pending

## Goal

This stage defines how cryptographic keys are protected and how the system can evolve toward hardware-backed signing.

## Key Principles

- Private keys MUST NOT leave the secure boundary
- Managed signing is preferred over file-only private keys
- Hardware-backed signing is a supported upgrade path

## Supported Models

### 1. KMS (Active)

- Cloud-managed key storage
- Signing through managed APIs
- Non-exportable key model
- Auditability support

### 2. HSM (Compatible)

- Dedicated hardware boundary
- Stronger isolation for key material
- Suitable for higher-assurance environments

### 3. YubiKey (Pending)

- Human-in-the-loop signing
- Physical possession requirement
- Stronger approval semantics for critical operations

## What This Stage Proves

- Keys are not treated as file-only assets
- Managed key architecture exists
- Hardware-backed upgrade path exists
- Key protection is becoming explicit and reviewable

## What This Stage Does Not Yet Prove

- Real production KMS signing
- Active HSM-backed signing
- Active YubiKey-based signing

Those will be added in future stages.
