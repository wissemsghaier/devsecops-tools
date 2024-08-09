# DevSecOps Tools

# Git-Secrets

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Git-Secrets                                                                            |
| **Definition**  |    Prevents the inclusion of secrets (e.g., API keys, passwords) in Git repositories.     |
| **Strength**    |    Detects secrets in Git commits.                                                        |
| **Advantage**   |    Helps avoid accidental exposure of secrets.                                            |
| **Utility**     |    Protects against accidental secrets leakage.                                           |

Why choose this tool?
Git-Secrets prevents sensitive data from being committed to Git repositories, reducing the risk of accidental exposure.

# ESLint

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    ESLint                                                                                 |
| **Definition**  |    Static code analysis tool for JavaScript to detect errors and enforce coding style.    |
| **Strength**    |    Real-time analysis of JavaScript code.                                                 |
| **Advantage**   |    Improves code quality by identifying errors and style issues.                          |
| **Utility**     |    Ensures high-quality JavaScript code.                                           	      |

Why choose this tool?
ESLint helps maintain clean and consistent JavaScript code by catching errors and enforcing coding standards early. 

# Prettier

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Prettier                                                                               |
| **Definition**  |    An opinionated code formatter that supports many programming languages,                |
| **Strength**    |    Ensures a uniform code style across different developers and codebases.                |
| **Advantage**   |    Reduces code review time and improves readability by enforcing consistent formatting.  |
| **Utility**     |    Automates code formatting to maintain a consistent style                               |

Why Choose Prettier?
Prettier automates code formatting, ensuring consistency and reducing the time spent on code reviews.

# Commitizen

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Commitizen                                                                             |
| **Definition**  |    Tool for generating standardized commit messages.                                      |
| **Strength**    |    Standardizes commit messages.                                                          |
| **Advantage**   |    Facilitates version management and change tracking.                                    |
| **Utility**     |    Ensures consistent and readable commit messages.                                       |

Why choose this tool?
Commitizen standardizes commit messages, making versioning and tracking changes more manageable and readable

# Vault

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    HashiCorp Vault                                                                        |
| **Definition**  |    Secret management tool for securely storing and controlling access to secrets.         |
| **Strength**    |    Centralized secret management.                                                         |
| **Advantage**   |    Provides robust security and access control for secrets.                               |
| **Utility**     |    Centralizes and secures sensitive data.                                                |

Why choose this tool?
Vault offers centralized and secure management of secrets, providing strong protection and access control for sensitive information.

# SonarQube

| Propriété  	  |                       Description                                                                      |
|------------     |--------------------------------------------------------------------------------------------------------|
| **Name**        |    SonarQube                                                                                           |
| **Definition**  |    Continuous code quality inspection platform that identifies bugs, vulnerabilities, and code smells. |
| **Strength**    |    Comprehensive code quality analysis.                                                                |
| **Advantage**   |    Provides detailed insights into code quality and security issues.                                   |
| **Utility**     |    Enhances code quality and security.                                                                 |

Why choose this tool?
SonarQube offers detailed analysis of code quality, helping to detect and fix bugs and vulnerabilities early in the development process.

## Docker-compose of Sonarqube 
```
version: '3.8'

services:
  sonarqube:
    image: sonarqube:latest
    container_name: sonarqube
    ports:
      - "9001:9000" 
    volumes:
      - sonarqube_data:/opt/sonarqube/data
      - sonarqube_extensions:/opt/sonarqube/extensions
    networks:
      - devsecops

networks:
  devsecops:
    driver: bridge

volumes:
  sonarqube_data:
  sonarqube_extensions:
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up SonarQube.

### 1. Services

#### sonarqube

- **image**: `sonarqube:latest` 
  Uses the latest version of the SonarQube image from Docker Hub.

- **container_name**: `sonarqube` 
  Names the container `sonarqube` for easier reference.

- **ports**:
  - `"9001:9000"` 
    Maps port 9001 on the host to port 9000 on the container, making SonarQube accessible via [http://localhost:9001](http://localhost:9001).

- **volumes**:
  - `sonarqube_data:/opt/sonarqube/data` 
    Persists SonarQube data to ensure it is retained across container restarts.
  - `sonarqube_extensions:/opt/sonarqube/extensions` 
    Persists SonarQube extensions for the same reason.

- **networks**:
  - `devsecops` 
    Connects the container to the `devsecops` network.

### 2. Networks

#### devsecops

- **driver**: `bridge` 
  Creates a custom network with a bridge driver to allow communication between containers if needed.

### 3. Volumes

- **sonarqube_data** 
  Stores SonarQube’s data, ensuring persistence even if the container is stopped or removed.

- **sonarqube_extensions** 
  Stores SonarQube’s extensions, ensuring persistence even if the container is stopped or removed.


# Jest

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Jest                                                                                   |
| **Definition**  |    JavaScript testing framework for unit, integration, and snapshot tests.                |
| **Strength**    |    Fast and easy to configure.                                                            |
| **Advantage**   |    Supports unit and snapshot testing with minimal setup.                                 |
| **Utility**     |    Provides efficient testing for JavaScript applications.                                                |

Why choose this tool?
Jest simplifies the process of writing and running tests for JavaScript applications, ensuring robust and reliable code.

# PHPUnit

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    PHPUnit                                                                                |
| **Definition**  |    Testing framework for PHP that supports unit testing.                                  |
| **Strength**    |    Comprehensive unit testing for PHP.                                                    |
| **Advantage**   |    Ensures PHP code quality and reliability through unit tests.                           |
| **Utility**     |    Facilitates unit testing for PHP projects.                                             |

Why choose this tool?
PHPUnit is essential for maintaining high-quality PHP code by enabling thorough unit testing and validation.

# Snyk

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Snyk                                                                                   |
| **Definition**  |    Tool for finding and fixing vulnerabilities in open source dependencies.               |
| **Strength**    |    Detects and fixes vulnerabilities in dependencies.                                     |
| **Advantage**   |    Enhances security of open source components by addressing vulnerabilities              |
| **Utility**     |    Secures open source dependencies.                                                      |

Why choose this tool?
Snyk helps secure open source dependencies by identifying and fixing vulnerabilities, reducing risk in software projects.

# Dependency-Track

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    OWASP Dependency-Track                                                                 |
| **Definition**  |    Manages and monitors software dependencies for vulnerabilities.                        |
| **Strength**    |    Comprehensive vulnerability management and real-time alerts.                           |
| **Advantage**   |    Integrates with CI/CD pipelines and supports various data sources.                     |
| **Utility**     |    Helps track and manage vulnerabilities in dependencies effectively.                    |

Why choose this tool?
OWASP Dependency-Track is chosen for its extensive integration capabilities and real-time monitoring of vulnerabilities, making it ideal
for proactive security management

## Docker-compose of Dependency-Track
```
version: '3.8'

services:
  dependency-track:
    image: dependencytrack/bundled:latest
    container_name: dependency-track
    ports:
      - "8080:8080"  # Maps host port 8080 to container port 8080
    environment:
      - DATABASE_URL=jdbc:postgresql://db:5432/dependencytrack
      - DATABASE_USER=dependencytrack
      - DATABASE_PASSWORD=dependencytrack
    volumes:
      - dependencytrack_data:/opt/dependency-track/data
    networks:
      - devsecops
    depends_on:
      - db

  db:
    image: postgres:latest
    container_name: dependencytrack_db
    environment:
      - POSTGRES_USER=dependencytrack
      - POSTGRES_PASSWORD=dependencytrack
      - POSTGRES_DB=dependencytrack
    volumes:
      - postgres_data:/var/lib/postgresql/data
    networks:
      - devsecops

networks:
  devsecops:
    driver: bridge

volumes:
  dependencytrack_data:
  postgres_data:
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up Nexus.

### Version

- **version: '3.8'**  
  Specifies the version of the Docker Compose file format. Version `3.8` is compatible with Docker Engine 19.03.0 and later, offering improved features and functionality.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### dependency-track

- **image**: `dependencytrack/bundled:latest`  
  Specifies the Docker image to use for this service. `dependencytrack/bundled:latest` pulls the latest version of Dependency-Track from Docker Hub. Dependency-Track is a dependency vulnerability management platform.

- **container_name**: `dependency-track`  
  Assigns a custom name (`dependency-track`) to the container for easier reference and management.

- **ports**:
  - `"8080:8080"`  
    Maps port 8080 on the host to port 8080 on the container, allowing access to Dependency-Track via http://localhost:8080.

- **environment**:
  - `DATABASE_URL=jdbc:postgresql://db:5432/dependencytrack`  
    Sets the JDBC URL for connecting to the PostgreSQL database.
  - `DATABASE_USER=dependencytrack`  
    Sets the username for the PostgreSQL database.
  - `DATABASE_PASSWORD=dependencytrack`  
    Sets the password for the PostgreSQL database.

- **volumes**:
  - `dependencytrack_data:/opt/dependency-track/data`  
    Mounts the `dependencytrack_data` volume to `/opt/dependency-track/data` in the container, ensuring that Dependency-Track data persists across container restarts.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network, allowing communication with other containers on this network.

- **depends_on**:
  - `db`  
    Specifies that the `dependency-track` service depends on the `db` service. Docker Compose will start `db` before `dependency-track`.

#### db

- **image**: `postgres:latest`  
  Specifies the Docker image to use for the PostgreSQL service. `postgres:latest` pulls the latest version of PostgreSQL from Docker Hub.

- **container_name**: `dependencytrack_db`  
  Assigns a custom name (`dependencytrack_db`) to the PostgreSQL container.

- **environment**:
  - `POSTGRES_USER=dependencytrack`  
    Sets the PostgreSQL username.
  - `POSTGRES_PASSWORD=dependencytrack`  
    Sets the PostgreSQL password.
  - `POSTGRES_DB=dependencytrack`  
    Creates a PostgreSQL database named `dependencytrack`.

- **volumes**:
  - `postgres_data:/var/lib/postgresql/data`  
    Mounts the `postgres_data` volume to `/var/lib/postgresql/data` in the container, ensuring that PostgreSQL data persists across container restarts.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network, allowing communication with other containers on this network.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **dependencytrack_data**  
  A named volume used by the `dependency-track` service to store Dependency-Track data. This ensures that the data persists even if the container is stopped or removed.

- **postgres_data**  
  A named volume used by the `db` service to store PostgreSQL data. This ensures that the database data persists even if the container is stopped or removed.


# npm

| Propriété  	  |                       Description                                                                |
|------------     |--------------------------------------------------------------------------------------------------|
| **Name**        |    npm (Node Package Manager)                                                                    |
| **Definition**  |    The default package manager for JavaScript and Node.js, used to manage project dependencies   |
| **Strength**    |    Manages packages and dependencies efficiently with a vast repository.                         |
| **Advantage**   |    Simplifies dependency management and provides access to a wide range of JavaScript libraries  |
| **Utility**     |    Facilitates the management of JavaScript project dependencies and automates scripts.          |

Why Choose npm?
npm provides robust dependency management and access to a comprehensive ecosystem of JavaScript packages, streamlining development.

# Maven

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Maven                                                                                  |
| **Definition**  |    A build automation tool for Java projects that manages project builds, dependencies    |
| **Strength**    |    Streamlines build processes and dependency management for Java applications.           |
| **Advantage**   |    Simplifies complex build configurations                                                |
| **Utility**     |    Automates the build lifecycle and dependency management in Java applications.          |

Why Choose Maven?
Maven automates the build and dependency management process for Java projects, ensuring a consistent and standardized approach.

# Selenium

| Propriété  	  |                       Description                                                                           |
|------------     |-------------------------------------------------------------------------------------------------------------|
| **Name**        |    Selenium                                                                                                 |
| **Definition**  |    The default package manager for JavaScript and Node.js, used to manage project dependencies and scripts  |
| **Strength**    |    Manages packages and dependencies efficiently with a vast repository.                                    |
| **Advantage**   |    Simplifies dependency management and provides access to a wide range of JavaScript libraries and tools.  |
| **Utility**     |    Facilitates the management of JavaScript project dependencies and automates scripts.                     |

Why choose this tool?
Selenium enables automation of web application testing, providing a way to verify functionality and performance across different browsers.

# Nexus

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Nexus Repository Manager                                                               |
| **Definition**  |    Manages and stores software artifacts and dependencies.                                |
| **Strength**    |    Centralized repository management.                                                     |
| **Advantage**   |    Simplifies artifact storage and dependency management.                                 |
| **Utility**     |    Manages and organizes software components.                                             |

Why choose this tool?
Nexus provides a centralized solution for managing and storing software artifacts, streamlining the management of dependencies and versions.

## Docker-compose of Nexus
```
version: '3'

services:
  nexus:
    image: sonatype/nexus3:latest
    container_name: nexus
    ports:
      - "8081:8081"
    volumes:
      - nexus_data:/nexus-data
    networks:
      - devsecops

volumes:
  nexus_data:

networks:
  devsecops:
    driver: bridge
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up Nexus.

### Version

- **version: '3'**  
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### nexus

- **image**: `sonatype/nexus3:latest`  
  Specifies the Docker image to use for this service. `sonatype/nexus3:latest` pulls the latest version of the Nexus 3 image from Docker Hub. Nexus Repository Manager is used to manage and host your software artifacts.

- **container_name**: `nexus`  
  Assigns a custom name (`nexus`) to the container for easier reference and management.

- **ports**:
  - `8081:8081`  
    Maps port `8081` on the host to port `8081` on the container. This allows you to access Nexus's web interface via `http://localhost:8081`.

- **volumes**:
  - `nexus_data:/nexus-data`  
    Defines a volume mapping. It mounts the `nexus_data` volume to the `/nexus-data` directory in the container. This volume is used to persist Nexus's data, including configuration and repository data, ensuring it is retained across container restarts.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **nexus_data**  
  A named volume used by the `nexus` service to store Nexus's data. This ensures that configuration and repository data persist even if the container is stopped or removed.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.


# Docker

| Propriété  	  |                       Description                                                                                   |
|------------     |---------------------------------------------------------------------------------------------------------------------|
| **Name**        |    Docker                                                                                                           |
| **Definition**  |    A platform for containerizing applications and their dependencie and its environment.                            |
| **Strength**    |    Provides lightweight, portable containers that encapsulate application code                                      |
| **Advantage**   |    Facilitates scalability, deployment, and management of applications across different environments.               |
| **Utility**     |    Simplifies application deployment and ensures consistency across different environments through containerization.|

Why Choose Docker?
Docker ensures consistent application environments and simplifies deployment, scaling, and management through containerization.

# Trivy

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Trivy                                                                                  |
| **Definition**  |    Security scanner for container images and configurations.                              |
| **Strength**    |    Comprehensive vulnerability scanning for containers.                                   |
| **Advantage**   |    Detects security issues in container images and configurations.                        |
| **Utility**     |    Enhances container security by identifying vulnerabilities.                            |

Why choose this tool?
Trivy helps ensure container security by scanning images and configurations for vulnerabilities, improving overall security posture.

## Docker-compose of Trivy
```
version: '3'

services:
  trivy:
    image: aquasec/trivy:latest
    container_name: trivy
    entrypoint: ["trivy"]
    volumes:
      - trivy_cache:/root/.cache/trivy
    networks:
      - devsecops

volumes:
  trivy_cache:

networks:
  devsecops:
    driver: bridge
```

## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up Trivy.

### Version

- **version: '3'** 
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports features such as defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### trivy

- **image**: `aquasec/trivy:latest` 
  Specifies the Docker image to use for this service. `aquasec/trivy:latest` pulls the latest version of the Trivy image from Docker Hub. Trivy is a security scanner for container images.

- **container_name**: `trivy`  
  Assigns a custom name (`trivy`) to the container for easier reference and management.

- **entrypoint**: `[ "trivy" ]`  
  Sets the entrypoint of the container. The `trivy` command will be executed when the container starts, overriding the default entrypoint specified in the Docker image.

- **volumes**:
  - `trivy_cache:/root/.cache/trivy`  
    Defines a volume mapping. It mounts the `trivy_cache` volume to the `/root/.cache/trivy` directory in the container. This volume is used to persist Trivy’s cache data, which improves performance by avoiding repeated scans.

- **networks**:
  - `devsecops` 
    Connects the container to the `devsecops` network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **trivy_cache** 
  A named volume used by the `trivy` service. It is used to store Trivy’s cache data, ensuring that this data persists across container restarts and is not lost when the container is stopped or removed.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge` 
    Creates a custom network with the `bridge` driver, allowing containers to communicate with each other over this network.

# Kubernetes

| Propriété  	  |                       Description                                                                                   |
|------------     |---------------------------------------------------------------------------------------------------------------------|
| **Name**        |    Kubernetes                                                                                                       |
| **Definition**  |    An open-source platform for automating the deployment, scaling, and management ofcontainerized                   |
| **Strength**    |    Provides powerful orchestration capabilities for managing containerized applications.                            |
| **Advantage**   |    Enables efficient scaling, load balancing, and self-healing of applications within clusters.                     |
| **Utility**     |    Facilitates the orchestration and management of containerized applications, improving scalability and reliability|

Why Choose Kubernetes?
Kubernetes offers advanced orchestration and management for containerized applications, ensuring scalability and reliability in complex deployments. 

# Falco

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Falco                                                                                  |
| **Definition**  |    Runtime security tool that detects abnormal behavior in containers and hosts.          |
| **Strength**    |    Real-time monitoring for suspicious activity.                                          |
| **Advantage**   |    Detects and alerts on unexpected or malicious behavior.                                |
| **Utility**     |    Monitors runtime behavior to detect security threats.                                  |

Why choose this tool?
Falco provides real-time security monitoring for containers and hosts, detecting abnormal behavior and potential threats.

## Docker-compose of Falco 

```
version: '3'

services:
  falco:
    image: falcosecurity/falco:latest
    container_name: falco
    privileged: true
    volumes:
      - /proc:/host/proc:ro
      - /boot:/host/boot:ro
      - /lib/modules:/host/lib/modules:ro
      - falco_rules:/etc/falco
    networks:
      - devsecops

volumes:
  falco_rules:

networks:
  devsecops:
    driver: bridge
```

## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up Flaco.

### Version

- **version: '3'**  
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### falco

- **image**: `falcosecurity/falco:latest`  
  Specifies the Docker image to use for this service. `falcosecurity/falco:latest` pulls the latest version of the Falco image from Docker Hub. Falco is a security tool for detecting anomalous activity in your applications.

- **container_name**: `falco`  
  Assigns a custom name (`falco`) to the container for easier reference and management.

- **privileged**: `true`  
  Runs the container in privileged mode, which grants it extended permissions. This is necessary for Falco to access certain system features and perform its security monitoring.

- **volumes**:
  - `/proc:/host/proc:ro`  
    Mounts the host's `/proc` directory into the container at `/host/proc` in read-only mode. This allows Falco to access system information.

  - `/boot:/host/boot:ro`  
    Mounts the host's `/boot` directory into the container at `/host/boot` in read-only mode. This is used to access kernel modules and other boot-related files.

  - `/lib/modules:/host/lib/modules:ro`  
    Mounts the host's `/lib/modules` directory into the container at `/host/lib/modules` in read-only mode. This allows Falco to access kernel modules needed for monitoring.

  - **falco_rules**: `/etc/falco`  
    Mounts a named volume `falco_rules` to `/etc/falco` in the container. This volume is used to persist Falco's configuration and rules.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **falco_rules**  
  A named volume used by the `falco` service to store Falco's configuration files and rules. This ensures that the configuration is persistent and can be reused across container restarts.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.


# OWASP ZAP

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    OWASP ZAP                                                                              |
| **Definition**  |    Security scanner for finding vulnerabilities in web applications.                      |
| **Strength**    |    Comprehensive web application security scanning.                                       |
| **Advantage**   |    Identifies security vulnerabilities in web applications.                               |
| **Utility**     |    Helps secure web applications by detecting security flaws.                             |

Why choose this tool?
OWASP ZAP provides an effective way to identify and address security vulnerabilities in web applications, enhancing overall security.

## Docker-compose of OWASP-ZAP

```
version: '3'

services:
  owasp-zap:
    image: owasp/zap2docker-stable:latest
    container_name: owasp-zap
    ports:
      - "8080:8080"
    volumes:
      - zap_data:/zap/wrk
    networks:
      - devsecops

volumes:
  zap_data:

networks:
  devsecops:
    driver: bridge
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up OWASP-ZAP.

### Version

- **version: '3'**  
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### owasp-zap

- **image**: `owasp/zap2docker-stable:latest`  
  Specifies the Docker image to use for this service. `owasp/zap2docker-stable:latest` pulls the latest stable version of the OWASP ZAP image from Docker Hub. OWASP ZAP is a popular security scanner for finding vulnerabilities in web applications.

- **container_name**: `owasp-zap`  
  Assigns a custom name (`owasp-zap`) to the container for easier reference and management.

- **ports**:
  - `8080:8080`  
    Maps port `8080` on the host to port `8080` on the container. This allows you to access OWASP ZAP's web interface via `http://localhost:8080`.

- **volumes**:
  - `zap_data:/zap/wrk`  
    Defines a volume mapping. It mounts the `zap_data` volume to the `/zap/wrk` directory in the container. This volume is used to persist ZAP's data, ensuring that scan results and configurations are retained across container restarts.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **zap_data**  
  A named volume used by the `owasp-zap` service to store ZAP’s data. This ensures that data such as scan results and configuration settings persist even if the container is stopped or removed.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.



# OpenSCAP

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    OpenSCAP                                                                               |
| **Definition**  |    Framework for compliance monitoring and vulnerability management.                      |
| **Strength**    |    Compliance and security configuration auditing.                                        |
| **Advantage**   |    Provides detailed compliance and security configuration reports.                       |
| **Utility**     |    Ensures compliance and manages vulnerabilities.                                        |

Why choose this tool?
OpenSCAP helps ensure compliance and manage security configurations, providing valuable insights into system security and compliance status.

## Docker-compose of OpenSCAP
```
version: '3'

services:
  openscap:
    image: openscap/openscap:latest
    container_name: openscap
    entrypoint: ["oscap"]
    volumes:
      - openscap_data:/data
    networks:
      - devsecops

volumes:
  openscap_data:

networks:
  devsecops:
    driver: bridge
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up OpenSCAP.

### Version

- **version: '3'**  
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### openscap

- **image**: `openscap/openscap:latest`  
  Specifies the Docker image to use for this service. `openscap/openscap:latest` pulls the latest version of the OpenSCAP image from Docker Hub. OpenSCAP is a security compliance scanner.

- **container_name**: `openscap`  
  Assigns a custom name (`openscap`) to the container for easier reference and management.

- **entrypoint**:  
  - `["oscap"]`  
    Sets the entrypoint of the container to the `oscap` command. This overrides the default entrypoint specified in the Docker image, ensuring that `oscap` is executed when the container starts.

- **volumes**:
  - `openscap_data:/data`  
    Defines a volume mapping. It mounts the `openscap_data` volume to the `/data` directory in the container. This volume is used to store OpenSCAP data, ensuring persistence across container restarts and preventing data loss when the container is stopped or removed.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network, allowing communication with other containers on the same network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **openscap_data**  
  A named volume used by the `openscap` service to store OpenSCAP data. This ensures that the data persists even if the container is stopped or removed.

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.

# ELK Stack

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    ELK Stack (Elasticsearch, Logstash, Kibana)                                            |
| **Definition**  |    Collection of tools for searching, analyzing, and visualizing log data.                |
| **Strength**    |    Centralized logging and visualization.                                                 |
| **Advantage**   |    Provides powerful search, analysis, and visualization of logs.                         |
| **Utility**     |    Enables effective log management and analysis.                                         |

Why choose this tool?
The ELK Stack offers robust log management, search, and visualization capabilities, helping to monitor and analyze system and application logs effectively.

## Docker-compose of OWASP-ZAP

```
version: '3'

services:
  elasticsearch:
    image: docker.elastic.co/elasticsearch/elasticsearch:8.0.0
    container_name: elasticsearch
    environment:
      - discovery.type=single-node
    ports:
      - "9200:9200"
      - "9300:9300"
    volumes:
      - elasticsearch_data:/usr/share/elasticsearch/data
    networks:
      - devsecops

  logstash:
    image: docker.elastic.co/logstash/logstash:8.0.0
    container_name: logstash
    ports:
      - "5044:5044"
    volumes:
      - logstash_config:/usr/share/logstash/config
      - logstash_pipelines:/usr/share/logstash/pipeline
    networks:
      - devsecops

  kibana:
    image: docker.elastic.co/kibana/kibana:8.0.0
    container_name: kibana
    ports:
      - "5601:5601"
    depends_on:
      - elasticsearch
    networks:
      - devsecops

volumes:
  elasticsearch_data:
  logstash_config:
  logstash_pipelines:
  kibana_data:

networks:
  devsecops:
    driver: bridge
```
## Explication Docker Compose Configuration 

This section explains the configuration of the Docker Compose file for setting up ELK.

### Version

- **version: '3'**  
  Specifies the version of the Docker Compose file format. Version `3` is compatible with Docker Engine 1.13.0 and later and supports defining services, networks, and volumes.

### Services

This section defines the services that make up your application. Each service represents a container that Docker Compose will manage.

#### elasticsearch

- **image**: `docker.elastic.co/elasticsearch/elasticsearch:8.0.0`  
  Specifies the Docker image to use for this service. `docker.elastic.co/elasticsearch/elasticsearch:8.0.0` pulls Elasticsearch version 8.0.0 from the Elastic Docker repository. Elasticsearch is a search and analytics engine.

- **container_name**: `elasticsearch`  
  Assigns a custom name (`elasticsearch`) to the container for easier reference and management.

- **environment**:
  - `discovery.type=single-node`  
    Configures Elasticsearch to run in single-node mode, suitable for development or testing environments.

- **ports**:
  - `9200:9200`  
    Maps port `9200` on the host to port `9200` on the container, making Elasticsearch accessible via `http://localhost:9200`.

  - `9300:9300`  
    Maps port `9300` on the host to port `9300` on the container, used for internal cluster communication.

- **volumes**:
  - `elasticsearch_data:/usr/share/elasticsearch/data`  
    Defines a volume mapping. It mounts the `elasticsearch_data` volume to the `/usr/share/elasticsearch/data` directory in the container. This volume is used to persist Elasticsearch data, ensuring it is retained across container restarts.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

#### logstash

- **image**: `docker.elastic.co/logstash/logstash:8.0.0`  
  Specifies the Docker image to use for this service. `docker.elastic.co/logstash/logstash:8.0.0` pulls Logstash version 8.0.0 from the Elastic Docker repository. Logstash is used for collecting, parsing, and storing logs.

- **container_name**: `logstash`  
  Assigns a custom name (`logstash`) to the container for easier reference and management.

- **ports**:
  - `5044:5044`  
    Maps port `5044` on the host to port `5044` on the container, typically used for Logstash input plugins.

- **volumes**:
  - `logstash_config:/usr/share/logstash/config`  
    Mounts the `logstash_config` volume to the `/usr/share/logstash/config` directory in the container, allowing you to provide custom configuration files for Logstash.

  - `logstash_pipelines:/usr/share/logstash/pipeline`  
    Mounts the `logstash_pipelines` volume to the `/usr/share/logstash/pipeline` directory in the container, where you can define Logstash pipeline configurations.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

#### kibana

- **image**: `docker.elastic.co/kibana/kibana:8.0.0`  
  Specifies the Docker image to use for this service. `docker.elastic.co/kibana/kibana:8.0.0` pulls Kibana version 8.0.0 from the Elastic Docker repository. Kibana is a data visualization tool for Elasticsearch.

- **container_name**: `kibana`  
  Assigns a custom name (`kibana`) to the container for easier reference and management.

- **ports**:
  - `5601:5601`  
    Maps port `5601` on the host to port `5601` on the container, making Kibana accessible via `http://localhost:5601`.

- **depends_on**:
  - `elasticsearch`  
    Ensures that the `elasticsearch` service is started before `kibana` to avoid connection issues.

- **networks**:
  - `devsecops`  
    Connects the container to the `devsecops` network.

### Volumes

This section defines the named volumes that are used to persist data or share data between containers.

- **elasticsearch_data**  
  A named volume used by the `elasticsearch` service to store Elasticsearch data. This ensures that data persists even if the container is stopped or removed.

- **logstash_config**  
  A named volume used by the `logstash` service to store Logstash configuration files.

- **logstash_pipelines**  
  A named volume used by the `logstash` service to store Logstash pipeline configurations.

- **kibana_data**  
  A named volume used by the `kibana` service to store Kibana's data (not used in the current configuration but reserved for potential future use).

### Networks

This section defines the networks used to enable communication between containers.

- **devsecops**:
  - **driver**: `bridge`  
    Creates a custom network with the `bridge` driver. This allows containers on this network to communicate with each other.


# Slack

| Propriété  	  |                       Description                                                         |
|------------     |-------------------------------------------------------------------------------------------|
| **Name**        |    Slack                                                                                  |
| **Definition**  |    Collaboration platform for team communication and integration                          |
| **Strength**    |    Facilitates team communication and collaboration.                                      |
| **Advantage**   |    Integrates with various tools for streamlined workflows.                               |
| **Utility**     |    Enhances team communication and workflow integration.                                  |



# Kubernetes Tools:

## kubectl

| Property          | Description                                                                              |
|-------------------|------------------------------------------------------------------------------------------|
| **Tool**          | kubectl                                                                                  |
| **Description**   | Command-line interface for interacting with Kubernetes.                                  |
| **Justification** | Allows management and manipulation of Kubernetes resources from the command line.        |
 
## Helm

| Property          | Description                                                                                          |
|-------------------|------------------------------------------------------------------------------------------------------|
| **Tool**          | Helm                                                                                                 |
| **Description**   | Package manager for Kubernetes that simplifies the installation and management of applications.      |
| **Justification** | Streamlines deployment, configuration, and management of Kubernetes applications.                    |
 
## Kustomize

| Property          | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| **Tool**          | Kustomize                                                                  |
| **Description**   | Tool for customizing Kubernetes configurations.                            |
| **Justification** | Allows modification of Kubernetes configuration files without duplication. |

## K9s

| Property          | Description                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| **Tool**          | K9s                                                                           |
| **Description**   | Terminal-based user interface for managing Kubernetes.                        |
| **Justification** | Provides an interactive command-line interface for easier cluster management. |

## Kubeless

| Property          | Description                                                      |
|-------------------|------------------------------------------------------------------|
| **Tool**          | Kubeless                                                         |
| **Description**   | Serverless solution for Kubernetes.                              |
| **Justification** | Enables serverless function deployment on Kubernetes.            |

## ArgoCD

| Property          | Description                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------|
| **Tool**          | ArgoCD                                                                                            |
| **Description**   | Continuous deployment tool for Kubernetes based on GitOps.                                        |
| **Justification** | Facilitates automated deployment and management of applications using Git as the source of truth. |

## Prometheus

| Property          | Description                                                                             |
|-------------------|-----------------------------------------------------------------------------------------|
| **Tool**          | Prometheus                                                                              |
| **Description**   | Monitoring and alerting toolkit for Kubernetes.                                         |
| **Justification** | Provides metrics collection and monitoring capabilities with a powerful query language. |

## Grafana

| Property          | Description                                                                          |
|-------------------|--------------------------------------------------------------------------------------|
| **Tool**          | Grafana                                                                              |
| **Description**   | Visualization tool for metrics collected by Prometheus.                              |
| **Justification** | Allows creation of interactive dashboards to visualize metrics and performance data. |


# Docker Tools

## Docker CLI

| Property          | Description                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------|
| **Tool**          | Docker CLI                                                                                   |
| **Description**   | Command-line interface for interacting with Docker.                                          |
| **Justification** | Allows management of Docker containers, images, volumes, and networks from the command line. |

## Docker Compose

| Property          | Description                                                                            |
|-------------------|----------------------------------------------------------------------------------------|
| **Tool**          | Docker Compose                                                                         |
| **Description**   | Tool for defining and running multi-container Docker applications.                     |
| **Justification** | Simplifies the management of complex applications using a single configuration file.   |

## Docker Swarm

| Property          | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Tool**          | Docker Swarm                                                                |
| **Description**   | Docker's native clustering and orchestration tool.                          |
| **Justification** | Manages Docker container clusters with built-in orchestration capabilities. |

## Docker Registry

| Property          | Description                                                               |
|-------------------|---------------------------------------------------------------------------|
| **Tool**          | Docker Registry                                                           |
| **Description**   | Server for storing and distributing Docker images.                        |
| **Justification** | Enables storage and distribution of Docker images within an organization. |

## Portainer

| Property          | Description                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| **Tool**          | Portainer                                                                     |
| **Description**   | User interface for managing Docker environments.                              |
| **Justification** | Provides a graphical interface for managing and monitoring Docker containers. |

## Docker Hub

| Property          | Description                                                                                |
|-------------------|--------------------------------------------------------------------------------------------|
| **Tool**          | Docker Hub                                                                                 |
| **Description**   | Cloud-based registry service for storing and sharing Docker images.                        |
| **Justification** | Offers a public and private repository for Docker images with search and sharing features. |










## Getting started

To make it easy for you to get started with GitLab, here's a list of recommended next steps.

Already a pro? Just edit this README.md and make it your own. Want to make it easy? [Use the template at the bottom](#editing-this-readme)!

## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.u-cloudsolutions.xyz/summary-internship/2024/wissem-sghaier/devsecops-tools.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

- [ ] [Set up project integrations](https://gitlab.u-cloudsolutions.xyz/summary-internship/2024/wissem-sghaier/devsecops-tools/-/settings/integrations)

## Collaborate with your team

- [ ] [Invite team members and collaborators](https://docs.gitlab.com/ee/user/project/members/)
- [ ] [Create a new merge request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)
- [ ] [Automatically close issues from merge requests](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)
- [ ] [Enable merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/approvals/)
- [ ] [Set auto-merge](https://docs.gitlab.com/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html)

## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing (SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html)

***

# Editing this README

When you're ready to make this README your own, just edit this file and use the handy template below (or feel free to structure it however you want - this is just a starting point!). Thanks to [makeareadme.com](https://www.makeareadme.com/) for this template.

## Suggestions for a good README

Every project is different, so consider which of these sections apply to yours. The sections used in the template are suggestions for most open source projects. Also keep in mind that while a README can be too long and detailed, too long is better than too short. If you think your README is too long, consider utilizing another form of documentation rather than cutting out information.

## Name
Choose a self-explaining name for your project.

## Description
Let people know what your project can do specifically. Provide context and add a link to any reference visitors might be unfamiliar with. A list of Features or a Background subsection can also be added here. If there are alternatives to your project, this is a good place to list differentiating factors.

## Badges
On some READMEs, you may see small images that convey metadata, such as whether or not all the tests are passing for the project. You can use Shields to add some to your README. Many services also have instructions for adding a badge.

## Visuals
Depending on what you are making, it can be a good idea to include screenshots or even a video (you'll frequently see GIFs rather than actual videos). Tools like ttygif can help, but check out Asciinema for a more sophisticated method.

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

## Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

## Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

## Roadmap
If you have ideas for releases in the future, it is a good idea to list them in the README.

## Contributing
State if you are open to contributions and what your requirements are for accepting them.

For people who want to make changes to your project, it's helpful to have some documentation on how to get started. Perhaps there is a script that they should run or some environment variables that they need to set. Make these steps explicit. These instructions could also be useful to your future self.

You can also document commands to lint the code or run tests. These steps help to ensure high code quality and reduce the likelihood that the changes inadvertently break something. Having instructions for running tests is especially helpful if it requires external setup, such as starting a Selenium server for testing in a browser.

## Authors and acknowledgment
Show your appreciation to those who have contributed to the project.

## License
For open source projects, say how it is licensed.

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
