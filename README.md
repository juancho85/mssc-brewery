# SFG Beer Works - Brewery Microservice

Udemy course:
* [Spring Boot Microservices with Spring Cloud](https://www.udemy.com/spring-boot-microservices-with-spring-cloud-beginner-to-guru/?couponCode=GIT_HUB2)

* Initialize project
* Use https://start.spring.io/ with:
    * Spring web Starter
    * Lombok
    * Spring Boot DevTools
    * Spring Boot Actuator
* Enable annotation processing (Settings > Build, Execution, Deployment, Compiler, Annotation Processors)
* Install Lombok Plugin
	* Adds refactor Lombok/Delombok options to see generated code
* Install MapStruct Support plugin
* Install Axis TCP Monitor Plugin (https://plugins.jetbrains.com/plugin/154-axis-tcp-monitor-plugin/)
* 

## Developer tools
* Added to project via spring-boot-devtools
* Automatically disabled when running a packaged application (java -jar)
* Restart are very fasts
* Uses two classloaders. One for the application and another for the jar dependencies
* IntelliJ: By default you need to select "build / make project", there is an advanced setting to make this more seamless
* Developer tools will disable template caching so the restart is not required to see changes
* LiveReload is a technology to automatically trigger a browser refresh when resources are changed
* Spring Boot devTools include a liveReload server. Browser plugins are available for a free download at livereload.com

## Versioning
* Convention: Putting the in the url: ex: "/api/v1/beer"
* Allows evolution without breaking current clients
* Typical lifespan:
    * v1 - first release
    * v2 - Notify consumers v1 is deprecated
    * v3 - Remove v1 (optional), notify consumers v2 is deprecated
* Semantic versioning: https://semver.org/
    * MAJOR.MINOR.PATCH
    * Examples of minor or patch versions
        * new optional parameter
        * New response fields
        * New service (endpoint)
        * Bug fixes - behavior change, NOT change to the API itself
    * Breaking changes (MAJOR)
        * New required parameter
        * Removal of existing parameter
        * Removal of response value
        * Parameter name change or type
        * Deprecation of a service
* Git semflow: https://github.com/lyndseypadget/semflow