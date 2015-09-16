## Spring Boot and DevOps

#### SpringOne2GX 2015: Wednesday 10:30AM

* Spring boot offers the following for free:
** Metadata
** Monitoring
** Confuguration (Beans, property values, controller mapping)
* Spring pet clinic starter project.
* By adding actuator, we have the metadata, health checks, metrics, configs, beans and url mappings.
* Spring boot has devtools.

##### Metadata
* This will abstract away the info endpoint.
* ANythig thta starts with "info" in the properties file will be in the the metadata. `http://localhost:8080/info`
* `info.application.artifactId=@project.artifactId@` will add the artifact id to the metadata.
* `git-commit-id-plugin` this will generate the git properties file. This will add the git information to the metadata.

##### Health Checks
* /health aggregate all the checks
* Implement `HealthIndicator` interface to have your own health check configs.

##### Metrics
* Gauge and Counter.
* the metrics can viewed in JMX through jconsole, graphite and http.
* To export in JMX, create new config class. `@Bean JmxMetricWrite`
* `@Bean GraphiteReporter` to export metrics to graphite.
* If the graphite server is down in dev env. To tackle that we can do:
** Add annottaion `@ConditionalOnMissingBean` to the graphite bean,
** Mock the metric for dev env.
* Custom metrics
** Create a class and get a handle to `GaugeService`
** Create a `@Bean` of the above custom metric.
