# Web Security Assessment — School Management System

## Overview
A preliminary, non-intrusive security assessment of a school management web application, focusing on publicly accessible security configurations and frontend resources.

- **Assessment date:** 10 October 2026
- **Authorization:** Conducted with the permission of the system owner
- **Assessor:** Muhammad Umar

## Scope
- HTTPS and HTTP-to-HTTPS redirection
- HTTP security headers
- Public metadata paths (robots.txt, manifest.json, security.txt)
- Frontend JavaScript inspection
- Basic checks for potentially exposed secrets
- Limited manual login/logout and role-visibility checks

**Out of scope:** exploitation, brute-forcing, denial of service, backend and server-side authorization testing.

## Tools Used
| Purpose | Tools |
|---|---|
| Assessment | Kali Linux, cURL, grep |
| Documentation | Nano, Pandoc, Markdown |

## Findings Summary
| # | Finding | Severity | Status |
|---|---|---|---|
| 1 | CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy and Permissions-Policy not observed | Low | Recommendation |
| 2 | `/.well-known/security.txt` returns HTML, not a valid security.txt | Informational | Recommendation |
| 3 | localStorage usage and password-related code in frontend; no confirmed exposed secret | Informational | Review recommended |
| 4 | Limited role-visibility checks showed no confirmed access-control issue; server-side authorization not verified | Informational | Further testing recommended |
| 5 | HSTS present | N/A | Positive observation |

> No exploitable vulnerability was confirmed by the checks performed.

## Recommendations
- Configure appropriate HTTP security headers (can be applied at hosting level)
- Publish a valid `/.well-known/security.txt` with a security contact
- Review client-side storage for sensitive information
- Verify server-side authentication and authorization for every role

## Repository Contents
- `report.pdf` — full assessment report
- `report.md` — editable report
- `evidence/headers-check.txt` — captured HTTP response headers

## Skills Demonstrated
HTTP header analysis, web reconnaissance, frontend code review, security reporting, responsible disclosure mindset

## Limitations
This was a preliminary assessment, not a comprehensive penetration test. Backend security and server-side authorization were not independently verified.

## Disclaimer
Results reflect only the checks performed on the assessment date and do not guarantee the application is free of vulnerabilities. No sensitive data is included in this repository.
