# STM32 Build Server example 
A sample repo to demonstrate how CI works on STM32 projects. This sample is based on the [following tutorial](https://blog.jumper.io/stm32-build-server/). Follow the instructions in the [link](https://blog.jumper.io/stm32-build-server/) to set this up yourself.

Click here to see the latest build result and artifact on CircleCI - [![CircleCI](https://circleci.com/gh/Jumperr-labs/stm32_cubemx_sample.svg?style=svg)](https://circleci.com/gh/Jumperr-labs/stm32_cubemx_sample)

Here's another example of a working continuous integration tool using Travis CI - [![Build Status](https://travis-ci.org/Jumperr-labs/stm32_cubemx_sample.svg?branch=master)](https://travis-ci.org/Jumperr-labs/stm32_cubemx_sample)

## How to run the build server locally

1. Install Docker (if you’re looking to implement a continuous integration process, Docker is one of the building blocks you’ll need).
2. docker pull jumperio/vlab-gcc-arm
3. git clone https://github.com/Jumperr-labs/stm32_cubemx_sample.git
4. cd stm32_cubemx_sample
5. docker run -v $PWD:/my_files_in_docker –entrypoint /usr/bin/make jumperio/vlab-gcc-arm -C my_files_in_docker
