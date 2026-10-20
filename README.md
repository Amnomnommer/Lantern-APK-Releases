# Lantern APK Releases

Public, binary-only update channel for the Portable Mobile Lantern Node.

This repository intentionally contains no Lantern core source, Workstation state, processing inputs, results, credentials, or signing keys.

## Mobile update contract

The app reads only:

- `channels/mobile-latest.json`
- release assets named `Lantern-mobile-debug.apk`
- tags named `mobile-debug-v<version_code>`

A channel manifest is published only after its APK has been built and inspected. Until then, the missing manifest is a safe “feed not available yet” state.

Each published manifest binds the APK to its Android version code, visible version name, application ID, exact byte length, SHA-256 digest, signing-certificate SHA-256, private-source revision identifier, and short release notes.

Android still requires owner confirmation before installation. Lantern verifies the downloaded hash, package identity, increasing version code, and signing identity before asking Android to install it.

## Current status

Repository initialized. No APK or active channel manifest has been published yet.
