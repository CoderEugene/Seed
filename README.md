[![Build Status](https://travis-ci.com/CoderEugene/Seed.svg?branch=master)](https://travis-ci.com/CoderEugene/Seed) ![language](https://img.shields.io/badge/language-java-orange.svg) ![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# What‘s Seed？

Seed is a skeleton project based on springboot2.x, integrating common components such as dubbo, redis, and various best practices, and its submodule division rules are as follows: 

- ❑ common：Common module
- ❑ dal：Data Access Layer
- ❑ service：Service Layer
- ❑ controller：Controller Layer
- ❑ integration：Integrate third-party services, such as dubbo
- ❑ facade：Provide dubbo services

With this skeleton project, you have completed the integration of the following modules:

- [x] Dubbo
- [x] Druid
- [x] Mybatis
- [x] Pagehelper
- [x] Swagger
- [x] Redission
- [x] Curator
- [ ] Spring Security
- [ ] Sharding-JDBC
- [ ] Sentinel
- [ ] RocketMQ
- [ ] Elastic-Job
- [ ] Seata
- [ ] Nacos
- [ ] SkyWalking
- [ ] MapStruct

# Quick Start

You can choose to modify directly from the source or generate from the skeleton. The way to use the skeleton is as follows: 

1. Put the Skeleton into the Maven Local Repository

   ```bash
   $ cd seed
   $ mv ./seed-archetype ~/.m2/repository/com/base/seed-archetype
   ```

2. Generate new project

   ```bash
   $ mvn archetype:generate \
     -DinteractiveMode=false \
     -DarchetypeGroupId=com.base \
     -DarchetypeArtifactId=seed-archetype \
     -DarchetypeVersion=0.0.1-SNAPSHOT \
     -DgroupId=[your groupId] \
     -DartifactId=[your artifactId] \
     -Dpackage=[your package] \
     -Dversion=[your version]
   ```

3. Modify `application.yml` configuration file

   ```yaml
   server.port
   spring.application.name
   spring.datasource.druid.url
   spring.datasource.druid.username
   spring.datasource.druid.password
   dubbo.redistry.address
   registry.zookeeper.serverLists
   ```
   

> - Disabled Redis: set `redis.enabled = false` in `application.yml`
> - Multi-Profiles: `mvn xxx -Pdev/test/prod`


# Component Version

|                                  |                 |
| -------------------------------- | --------------- |
| `spring`                         | `5.2.2.RELEASE` |
| `spring-boot-starter-parent`     | `2.2.2.RELEASE` |
| `dubbo-spring-boot-starter`      | `2.7.4.1`       |
| `druid-spring-boot-starter`      | `1.1.17`        |
| `pagehelper-spring-boot-starter` | `1.2.13`        |
| `mybatis-spring-boot-starter`    | `2.1.1`         |
| `vjkit`                          | `1.0.8`         |
| `fastjson`                       | `1.2.70`        |
| `swagger`                        | `2.9.2`         |
| `lombok`                         | `1.8.12`        |
| `redission`                      | `3.13.1`        |
| `curator`                        | `5.1.0`         |
| `zookeeper`                      | `3.6.0`         |
| `mockito`                        | `3.5.13`        |

