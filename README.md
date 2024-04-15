# ci-cd
CI/CD scripts and builds for MUSC-BRIDGE application development. Utilities are
primarily deployed in Docker image available on the following registeries:

1. dmri/ci-cd
2. ghcr.io/muscbridge/ci-cd

## Development
Developers can build images locally with
```bash
docker buildx build -t dmri/ci-cd:test -f Dockerfile_py3.11 --platform linux/amd64 --build-arg MAKE_JOBS=8 .
```

## Deployment
All build are automatically built and published to registeries upon pushing commits
to main branch.