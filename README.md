## Prometheus metrics collection from Amazon ECS

This Git repository contains software artifacts related to two different approaches for collecting Prometheus metrics from applications deployed to an Amazon ECS cluster. Both approaches employ the same custom service discovery mechanism that leverages the integration between Amazon ECS and AWS Cloud Map to dynamically discover scraping targets for Prometheus. The Golang code in the repository pertains to that of a side-car container which impements the custom service discovery mechanism. 

The two sub-directories, namely [deploy-prometheus](https://github.com/aws-samples/prometheus-for-ecs/blob/main/deploy-prometheus) and [deploy-adot](https://github.com/aws-samples/prometheus-for-ecs/blob/main/deploy-adot) contain the artifacts required to deploy the solution to an Amazon ECS cluster.

- The first approach employs a single instance of [Prometheus server deployed to an ECS cluster](https://github.com/aws-samples/prometheus-for-ecs/blob/main/deploy-prometheus/README.md).

- The second approach employs a single instance of [AWS Distro for OpenTelemetry (ADOT) Collector deployed to an ECS cluster](https://github.com/aws-samples/prometheus-for-ecs/blob/main/deploy-adot/README.md). Prometheus metrics are collected by the [Prometheus Receiver](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/receiver/prometheusreceiver) that runs in the ADOT Collector pipeline.


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

