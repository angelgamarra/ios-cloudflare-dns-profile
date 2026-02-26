# iOS Cloudflare DNS over HTTPS Profile

This repository contains a signed iOS configuration profile (.mobileconfig) that enables system-wide DNS over HTTPS (DoH) using Cloudflare's public DNS resolvers (1.1.1.1 and 1.0.0.1).

## Purpose

This profile was created primarily for personal use, but it is publicly available for anyone who may find it useful.

It configures iOS to use encrypted DNS resolution via HTTPS, improving privacy by preventing DNS queries from being transmitted in plain text.

## What This Profile Does

- Enables DNS over HTTPS (DoH)
- Uses Cloudflare resolvers:
  - 1.1.1.1
  - 1.0.0.1
  - IPv6 equivalents
- Applies system-wide DNS configuration
- Does not block or filter content
- Does not modify any other device settings

## Signature Information

The profile is digitally signed using a self-signed certificate.

- Certificate validity: 10 years
- Purpose: Ensures file integrity and removes unsigned profile warnings
- This is NOT a publicly trusted certificate authority

Because the certificate is self-signed, iOS may still indicate that the profile is not verified by a trusted authority. This is expected behavior.

## Installation

1. Download the `.mobileconfig` file.
2. Open it on your iOS device.
3. Go to Settings → Profile Downloaded.
4. Install and confirm.

## Security Notes

- No private keys are included in this repository.
- The certificate used for signing is not intended for identity verification.
- This profile does not route traffic through any third party — it only sets DNS to Cloudflare.

## Disclaimer

Use at your own discretion. Always review configuration profiles before installing them on your device.
