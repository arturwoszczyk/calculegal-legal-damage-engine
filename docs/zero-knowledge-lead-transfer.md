# Zero-Knowledge Lead Transfer

CalcuLegal’s privacy architecture is based on the idea that the platform operator should not need access to user-identifying data in clear text.

This repository describes the principle, not the production implementation.

## Conceptual model

1. The user runs an anonymous simulation.
2. The user receives an orientative result.
3. Only if the user explicitly chooses professional orientation, selected data may be prepared for transfer.
4. The data is encrypted for the designated professional recipient.
5. The platform stores or transmits only encrypted payloads and limited operational metadata.

## Design goals

- the platform should not access personal data in clear text;
- professionals should receive only data the user consents to share;
- different professional recipients should not decrypt each other’s payloads;
- the system should preserve traceability without creating unnecessary exposure.

## Publicly documented cryptographic pattern

The public documentation describes a hybrid encryption concept:

- symmetric encryption for the payload;
- asymmetric encryption for the payload key;
- separation between public and private keys;
- professional-side decryption.

## What is intentionally not published

This repository does not include:

- production cryptographic code;
- endpoint names;
- key rotation procedures;
- partner assignment logic;
- production payload schema;
- operational database schema;
- real lead transfer workflows.

## Why this matters

Sensitive legal scenarios require more than policy statements. The architecture should reduce access by design.
