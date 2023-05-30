# Mkdocs

## Deployment

```bash
# Build image from Dockerfile
sudo docker build -t mkdocs .

# Run image
sudo docker run --restart always -p 9001:9001 mkdocs
```
