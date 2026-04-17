# Stage274: Key Management Hardening

## Overview

Stage274 introduces a minimal and clean key management model for QSP.

This stage focuses on how keys are protected, not only how signatures are verified.

## Current Status

- KMS: active
- HSM: compatible
- YubiKey: pending

## What This Stage Adds

- A documented key management model
- A managed-key configuration example
- A hardware-backed upgrade path
- Verifiable key-management evidence

## Files

- `docs/key_management_model.md`
- `kms/kms_config_example.yaml`
- `hsm/hsm_model.md`
- `yubikey/yubikey_signing.md`
- `tools/verify_key_management.py`
- `out/key_management_evidence.json`

## Evidence

Run:

```bash
python3 tools/verify_key_management.py

This generates:

out/key_management_evidence.json

Example evidence state:

KMS: active
HSM: compatible
YubiKey: pending
Security Meaning

Before this stage, trust focused mainly on signatures and verification outputs.

Stage274 adds a new dimension:

where keys are protected
whether keys are exportable
whether hardware-backed signing is available

This strengthens Identity Trust and creates a path toward stronger real-world key protection.

Limitations

This stage does NOT yet prove:

live KMS-backed signing
active HSM-backed operations
active YubiKey signing

Those will be added in future stages.

Next Step

The natural next step is Stage275:

key usage policy
who can use keys
under what conditions
with what approval requirements
License

MIT License
