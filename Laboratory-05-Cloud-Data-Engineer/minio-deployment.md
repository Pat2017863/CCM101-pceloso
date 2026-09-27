# MinIO Deployment

## Docker Command

```bash
docker run -d \
-p 9000:9000 \
-p 9001:9001 \
--name minio-server \
-e MINIO_ROOT_USER=cloudadmin \
-e MINIO_ROOT_PASSWORD=CloudNova2026! \
bitnamilegacy/minio:2025.7.23-debian-12-r5
