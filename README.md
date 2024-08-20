# Project Overview

This repo consists of application yaml files and helm charts for  **numbers-api** and **forwarder** applications to be deoloyed using ArgoCD.

## Directory Structure
```csharp
/
├── envs
│   ├── dev
│   │   ├── forwarder
│   │   │   └── application.yaml
│   │   └── numbers-api
│   │       └── application.yaml
│   └── prod
│       ├── forwarder
│       │   └── application.yaml
│       └── numbers-api
│           └── application.yaml
└── helm-charts
    ├── forwarder
    │   ├── Chart.yaml
    │   ├── charts
    │   └── values.yaml
    └── numbers-api
        ├── Chart.yaml
        ├── charts
        └── values.yaml
```


## Components

### Application yaml
- **numbers-api**:
- ArgoCD Application manifest, configured to deploy an application called numbers-api to the dev namespace in your Kubernetes cluster.

- **forwarder**: A FastAPI-based web application that sends an api request to the given url from an environment variable named `API_URL` and returns the response.
- ArgoCD Application manifest, configured to deploy an application called forwarder to the dev namespace in your Kubernetes cluster.

### helm-charts
Both applications include a Helm chart for deployment.
Helm charts have dependencies on a base mutual Helm chart (application) version 3.0.0 available at Stakater Helm Charts.
