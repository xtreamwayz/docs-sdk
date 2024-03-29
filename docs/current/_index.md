---
title: docs-sdk
version: "1.0"
---

This project consists of a collection of tools to generate the documentation
for the XTREAMWAYZ organization. It's very opinionated and contains hugo templates
and css files as we like them.

## Preview documentation

```bash
# Build documentation into ./build
docker run --rm -it -v ${PWD}:/src xtreamwayz/docs build

# Preview documentation at http:/localhost:1313/
docker run --rm -it -p 1313:1313 -v ${PWD}:/src xtreamwayz/docs server

# Preview documentation at http:/localhost:1313/ (including draft and future content)
docker run --rm -it -p 1313:1313 -v ${PWD}:/src xtreamwayz/docs preview
```

## Build container locally

```bash
# Build container
docker build -t docs .

# Run container
docker run --rm -it -p 1313:1313 -v ${PWD}:/src docs [server|preview|build]
```

## Resources

- https://github.com/actions/checkout
- https://help.github.com/en/github/automating-your-workflow-with-github-actions/virtual-environments-for-github-actions#environment-variables
- https://help.github.com/en/github/automating-your-workflow-with-github-actions/contexts-and-expression-syntax-for-github-actions
