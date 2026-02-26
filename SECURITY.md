# Security Policy

## Supported Scope

This repository is a public academic website. Security reports are welcome for:
- accidental credential exposure
- vulnerable third-party script usage
- unsafe deployment or content injection risks

## How to Report

Please report security issues privately instead of opening a public issue.

Use one of the following channels:
- Maintainer email: `<add security contact email>`
- Or PI contact email listed on the website contact page

Include:
- affected file/path
- brief reproduction steps
- potential impact

## Response Expectations

- Initial acknowledgement target: within 7 days
- Remediation timeline: based on severity and maintainer availability
- Public disclosure: after fix and key rotation (if applicable)

## Sensitive Data Handling

If a secret/token is exposed:
1. rotate/revoke it immediately
2. remove it from current files
3. add/update ignore rules and prevention checks
4. evaluate whether history rewrite is required
