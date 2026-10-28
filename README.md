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

sha256:907745ea8af0fa0b537d8f6a836905a6537703b9869f33213920a2b978311dde

## Stage 4 — Docker Hub Release

- Docker Hub repository: https://hub.docker.com/r/ishitasri6/fest-backend
- Release tags: `1.0.0`, `1.0`
- Image digest: `sha256:907745ea8af0fa0b537d8f6a836905a6537703b9869f33213920a2b978311dde`
- Deployment: Docker Compose pulls `ishitasri6/fest-backend:1.0.0` from Docker Hub.
- Verification: The backend and PostgreSQL started successfully; `/api/health` returned `database: True`, registration number `202401100200158`, and version `1.0.0`.

### Stage 4 evidence

- `S4-1.png` — Docker Hub release and digest
- `S4-2.png` — Registry pull and Compose deployment
- `S4-3.png` — Application and registration verification
