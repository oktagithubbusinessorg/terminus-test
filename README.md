# Terminus

Terminus is a one-stop onboarding service for all engineering resources.

For in-depth documentation, see `/docs`.

## Development

### Pre-requisites

1. `brew install docker`
2. `brew install minikube`
3. `brew install skaffold`
4. `brew install helm`
5. `brew install poetry`
6. `minikube start`

### Build

```bash
.bacon/build.sh
```

| *envvar*      | *description* |
| ------------- | ------------- |
| `DO_FORMAT=0` | allows you to auto format the code    |
| `SKIP_LINT=0` | allows you to skip any of the linting |

> e.g. `DO_FORMAT=0 .bacon/build.sh`

### Local Dev Continuous Testing

```bash
# terminal 1
skaffold dev --port-forward

# terminal 2
curl localhost:8000/repos
```

> Note: This will deploy mongodb into minikube.  In order to connect follow
> the chart's prompt which will tell you how to connect.

### IDE Integration

#### PyCharm Setup Tips

- Install `poetry` plugin
- Set poetry created python to project interpreter
