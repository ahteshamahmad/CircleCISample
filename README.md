# CircleCISample
version: 2.1
jobs:
  build:
    docker:
      - image: docker:20.10.7
        context: docker://my-registry-url.com
        auth:
          username: $DOCKER_USERNAME
          password: mypass123
    steps:
      - run:
          name: Pull private Docker image
          command: |
            docker pull ahteshamdocker/spring-boot-image:latest
