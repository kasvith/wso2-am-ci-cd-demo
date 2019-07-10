# CI/CD Pipeline for WSO2 API Manager with Jenkins

This repository contains demo files for creating a CI/CD pipeline for APIs with WSO2 API Manager with Jenkins.

> This can be even used with other CI/CD tools like DroneCI/CircleCI/TravisCI etc.

## Prerequisites

- Jenkins installation
- Latest [APIMCLI](https://github.com/wso2/product-apim-tooling/releases) tool configured in Jenkins Machine
- Working API Manager instances(at least two)

## Important Notes

1. API Manager instances must be accessible from CI/CD servers
2. Tweak `config.sh` to setup each API Manager as a different environment(this setup assumes you have 3 running APIM instances in port offset 0,1,2)
3. `api_params.yaml` file contains environment specific configurations. Edit this file to specify endpoint configuration, certificates for each environment etc.
4. `api_params.yaml` can be kept anywhere, in here its inside the API Project directory. It will be automatically detected by tool. You can specify a parameters file by providing `--params <Path to Parameter file>`
