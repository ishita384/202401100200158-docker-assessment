# Docker & Container Security Assessment

- **Registration Number:** 202401100200158
- **Application:** FestPass Registration
- **Port:** 8058
- **Backend images:** `fest-backend:0.1` (before hardening), `fest-backend:0.2` (hardened)

## Stage 3 — Image Hardening

The backend image was hardened by using a version-pinned slim Python base image, upgrading Python dependencies, and running the application as a non-root user.

### Trivy vulnerability comparison

| Image | CRITICAL vulnerabilities | HIGH vulnerabilities | Image size |
|---|---:|---:|---:|
| `fest-backend:0.1` | Fill in actual count | Fill in actual count | Fill in actual size |
| `fest-backend:0.2` | Fill in actual count | Fill in actual count | Fill in actual size |

### Evidence

- `S3-1`: Trivy scan before hardening
- `S3-3`: Trivy scan after hardening

### AI tools used

ChatGPT was used for guidance on Dockerfile hardening, vulnerability scanning, and assessment documentation.