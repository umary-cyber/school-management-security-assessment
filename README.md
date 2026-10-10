# Web Security Assessment — Shezad Children Academy

## Overview
A preliminary web security assessment of the Shezad Children Academy School Management System, focusing on publicly accessible security configurations and frontend resources.

## Scope
- HTTPS and HTTP-to-HTTPS redirection
- HTTP security headers
- Public metadata paths
- Frontend JavaScript inspection
- Basic checks for potentially exposed secrets
- Limited manual login/logout and role-visibility checks

## Tools Used
- Kali Linux
- cURL
- grep
- Nano
- Pandoc

## Key Observations
- HSTS was present in the inspected HTTP response.
- Several other checked security headers were not observed.
- The security.txt path returned HTML rather than a dedicated security.txt document.
- No exposed secret or exploitable vulnerability was confirmed by the checks performed.

## Files
- `report.pdf` — assessment report
- `report.md` — editable report
- `evidence/headers-check.txt` — captured HTTP response headers

## Limitations
This was a preliminary assessment, not a comprehensive penetration test. Backend security and server-side authorization were not independently verified.

## Disclaimer
Assessment results reflect only the checks performed on the assessment date. Testing and publication should be authorized by the system owner.



