# {TEMPLATE_SERVICE_NAME} Service Server
Template generated Kotlin server stubs for the gRPC service - {TEMPLATE_SERVICE_NAME} Service

![](logo/bh_grpc_kotlin.png)

## Overview

This directory contains the server impl in Kotlin for the gRPC service - {TEMPLATE_SERVICE_HYPHEN_NAME}.

- This repo was created using builder-hub from a starter template for gRPC and Kotlin.
- For more details on the starter template, see the [project on GitHub](https://github.com/builder-hub/starter-service-server).

You can find detailed instructions for building and running the server from below

## File organization

The server sources are organized into the following top-level folders:

- [{TEMPLATE_SERVICE_HYPHEN_NAME}-service-models]({TEMPLATE_SERVICE_HYPHEN_NAME}-service-models): `.proto` files for generating the stubs
- [{TEMPLATE_SERVICE_HYPHEN_NAME}-service-server]({TEMPLATE_SERVICE_HYPHEN_NAME}-service-server): Kotlin servers based on regular [stub][] artifacts

## Set up the project
<details>
  <summary>Clone the project</summary>

  Clone the project recursively cloning all submodules

  ```sh
  git clone git@github.com:{TEMPLATE_SERVER_REPO_OWNER}/{TEMPLATE_SERVICE_HYPHEN_NAME}-service-server.git --recurse-submodules
  ```

  Navigate into the project:
  ```sh
  cd {TEMPLATE_SERVICE_HYPHEN_NAME}-server
  ```
</details>

## Run the server inside a docker on macOS
<details>
  <summary>Install Docker</summary>

  Download and install the latest version of docker:
  [Download Latest Docker](https://docs.docker.com/desktop/mac/install/)
</details>
<details>
  <summary>Run the server</summary>

  Build a docker image and run the server on a container:
  ```sh
  docker-compose up
  ```
  This will start the server and open up the 50051 port for connections
</details>

## Run the server without any containers on macOS
<details>
  <summary>Install Homebrew</summary>

  Download and install Homebrew:

  ```sh
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
</details>
<details>
  <summary>Install JDK</summary>

  Install any version of JDK (8 preferred):

  ```sh
  brew install openjdk@8
  ```

  Add the installed version of JDK to your path through .zshrc or .bash_profile

  ```sh
  echo 'export PATH="/usr/local/opt/openjdk@8/bin:$PATH"' >> ~/.zshrc
  source ~/.zshrc
  ```

  or

  ```sh
  echo 'export PATH="/usr/local/opt/openjdk@8/bin:$PATH"' >> ~/.bash_profile
  source ~/.bash_profile
  ```
</details>
<details>
  <summary>Run the server</summary>

  Start the server:

  ```sh
  ./gradlew {TEMPLATE_SERVICE_HYPHEN_NAME}-service-server:start
  ```

  This will start the server and open up the 50051 port for connections
</details>

[grpc.io Kotlin/JVM]: https://grpc.io/docs/languages/kotlin/
[Quick start]: https://grpc.io/docs/languages/kotlin/quickstart/
[Basics tutorial]: https://grpc.io/docs/languages/kotlin/basics/
