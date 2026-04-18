# ecom-app-config-repo

Central configuration repository for the e-commerce microservices platform. It is consumed by the Spring Cloud Config Server so that shared and service-specific properties can be managed outside the application codebases.

## Contents

- global settings in `application.properties`
- service-specific configuration files such as `customer-service.properties`, `product-service.properties`, and `vente-service.properties`
- environment-specific overrides including `customer-service-dev.properties` and `customer-service-prod.properties`

## Why This Repository Exists

- keeps runtime configuration separate from service code
- supports shared parameters across services
- makes profile-based configuration easier to manage
- works with `config-service` as the remote configuration source

## Notes

The current configuration includes shared actuator and discovery settings as well as service-level parameters. This repository is most useful when it is versioned alongside the rest of the e-commerce platform.
