# Superset

![version](https://img.shields.io/docker/v/amancevice/superset?color=blue&label=version&logo=docker&logoColor=eee&sort=semver&style=flat-square)
[![latest](https://img.shields.io/github/workflow/status/amancevice/docker-superset/latest?label=latest&logo=github&style=flat-square)](https://github.com/amancevice/docker-superset/actions)
[![edge](https://img.shields.io/github/workflow/status/amancevice/docker-superset/edge?label=edge&logo=github&style=flat-square)](https://github.com/amancevice/docker-superset/actions)

Docker image for [Superset](https://github.com/ApacheInfra/superset).

This project is unofficial and not related to Superset or Apache.

## Download

Download this image from the Docker registry:

```bash
docker pull amancevice/superset:<version>
```

## Building

*I do not recommend building this image on your own. Instead, try pulling a tag from the Docker registry.*

If you insist on building an image from the source, use the `make` to supervise the build.

```bash
make [ SUPERSET_VERSION=<version> ]
```

## Issues

Please **only** file issues in this project that are related to Docker and **do** include the Docker commands or compose configuration of your setup when filing issues (be sure to hide any secrets/passwords before submitting).

File issues/bugs with Superset at the [source](https://github.com/apache/incubator-superset/issues).

Please **do not** files issues like "Please include `<some-python-pip>` in the Dockerfile," open a [pull request](https://github.com/amancevice/superset/pulls) for updates/enhancements.


## Examples

<<<<<<< HEAD
| Language                             | Source                                                      | Ubuntu | MacOS | Windows |
|--------------------------------------|-------------------------------------------------------------|--------|-------|---------|
| C++ (include C++ runtime and protoc) | [src](src)                                                  | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-cpp_distcheck.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fcpp_distcheck%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-bazel.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fbazel%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-dist_install.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fdist_install%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fcpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-cpp_distcheck.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fcpp_distcheck%2Fcontinuous) | [![Build status](https://ci.appveyor.com/api/projects/status/73ctee6ua4w2ruin?svg=true)](https://ci.appveyor.com/project/protobuf/protobuf) |
| Java                                 | [java](java)                                                | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-java_compatibility.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fjava_compatibility%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-java_jdk7.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fjava_jdk7%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-java_oracle7.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fjava_oracle7%2Fcontinuous) | | |
| Python                               | [python](python)                                            | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python27.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython27%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python33.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython33%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python34.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython34%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python35.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython35%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python36.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython36%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python37.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython37%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python_compatibility.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython_compatibility%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python27_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython27_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python33_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython33_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python34_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython34_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python35_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython35_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python36_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython36_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python37_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython37_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-python-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fpython_release%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-python.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fpython%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-python_cpp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fpython_cpp%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-python-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fpython_release%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/windows-python-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fwindows%2Fpython_release%2Fcontinuous) |
| Objective-C                          | [objectivec](objectivec)                                    | | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-objectivec_cocoapods_integration.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fobjectivec_cocoapods_integration%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-objectivec_ios_debug.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fobjectivec_ios_debug%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-objectivec_ios_release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fobjectivec_ios_release%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-objectivec_osx.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fobjectivec_osx%2Fcontinuous) | |
| C#                                   | [csharp](csharp)                                            | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-csharp.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fcsharp%2Fcontinuous) | | [![Build status](https://ci.appveyor.com/api/projects/status/73ctee6ua4w2ruin?svg=true)](https://ci.appveyor.com/project/protobuf/protobuf)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/windows-csharp-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fwindows%2Fcsharp_release%2Fcontinuous) |
| JavaScript                           | [js](js)                                                    | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-javascript.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fjavascript%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-javascript.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fjavascript%2Fcontinuous) | |
| Ruby                                 | [ruby](ruby)                                                | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-ruby23.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fruby23%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-ruby24.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fruby24%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-ruby25.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fruby25%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-ruby26.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fruby26%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-ruby-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fruby_release%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-ruby23.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fruby23%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-ruby24.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fruby24%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-ruby25.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fruby25%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-ruby26.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fruby26%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-ruby-release.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fruby_release%2Fcontinuous) | |
| Go                                   | [golang/protobuf](https://github.com/golang/protobuf)       | | | |
| PHP                                  | [php](php)                                                  | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-php_all.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2Fphp_all%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/linux-32-bit.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fubuntu%2F32-bit%2Fcontinuous) | [![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-php5.6_mac.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fphp5.6_mac%2Fcontinuous)<br/>[![Build status](https://storage.googleapis.com/protobuf-kokoro-results/status-badge/macos-php7.0_mac.png)](https://fusion.corp.google.com/projectanalysis/current/KOKORO/prod:protobuf%2Fgithub%2Fmaster%2Fmacos%2Fphp7.0_mac%2Fcontinuous) | |
| Dart                                 | [dart-lang/protobuf](https://github.com/dart-lang/protobuf) | [![Build Status](https://travis-ci.org/dart-lang/protobuf.svg?branch=master)](https://travis-ci.org/dart-lang/protobuf) | | |
=======
Navigate to the [`examples`](./examples) directory to view examples of how to configure Superset with MySQL, PostgreSQL, or SQLite.
>>>>>>> a0x8o


## Versions

This repo is tagged in parallel with superset. Pulling `amancevice/superset:0.18.5` will fetch the image of this repository running superset version `0.18.5`. It is possible that the `latest` tag includes new features/support libraries but will usually be in sync with the latest semantic version.


## Configuration

Follow the [instructions](https://superset.incubator.apache.org/installation.html#configuration) provided by Apache Superset for writing your own `superset_config.py`. Place this file in a local directory and mount this directory to `/etc/superset` inside the container. This location is included in the image's `PYTHONPATH`. Mounting this file to a different location is possible, but it will need to be in the `PYTHONPATH`.

View the contents of the [`examples`](./examples) directory to see some simple `superset_config.py` samples.


## Volumes

The image defines two data volumes: one for mounting configuration into the container, and one for data (logs, SQLite DBs, &c).

The configuration volume is located alternatively at `/etc/superset` or `/home/superset`; either is acceptable. Both of these directories are included in the `PYTHONPATH` of the image. Mount any configuration (specifically the `superset_config.py` file) here to have it read by the app on startup.

The data volume is located at `/var/lib/superset` and it is where you would mount your SQLite file (if you are using that as your backend), or a volume to collect any logs that are routed there. This location is used as the value of the `SUPERSET_HOME` environmental variable.

## Database Initialization

After starting the Superset server, initialize the database with an admin user and Superset tables using the `superset-init` helper script:

```bash
docker run --detach --name superset [options] amancevice/superset
docker exec -it superset superset-init
```

## Upgrading

Upgrading to a newer version of superset can be accomplished by re-pulling `amancevice/superset`at a specified superset version or `latest` (see above for more on this). Remove the old container and re-deploy, making sure to use the correct environmental configuration. Finally, ensure the superset database is migrated up to the head:

```bash
# Pull desired version
docker pull amancevice/superset

# Remove the current container
docker rm -f superset-old

# Deploy a new container ...
docker run --detach --name superset-new [options] amancevice/superset

# Upgrade the DB
docker exec superset-new superset db upgrade

# Sync the base permissions
docker exec superset-new superset init
```
