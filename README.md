# sample app

This repository is a high level deployment defintion for Kubernetes. The repo contains [Fabrikate](https://github.com/Microsoft/fabrikate) defintions for a boilerplate [Cloud Native stack](https://github.com/timfpark/fabrikate-cloud-native) and Helm charts for a demo application called [Project Jackson](https://github.com/CatalystCode/kubemalt/tree/master/demo).

## Features
* Istio based canary deployment configuration of the Project Jackson API microservice
* Mulicluster support

## How to adjust the canary deployment traffic weights

1. Navigate to the [common.yaml](services/project-jackson/jackson-api/config/common.yaml) file. 
2. Modifiy the `stableWeight` and `canaryWeight` values. (Below sure they total to 100)

## How to run Fabrikate on this repository
1. Run Fabrikate at the root level of this repository
   1. `fab install .`
   2. `fab generate $ENV_CONFIG_NAME`
