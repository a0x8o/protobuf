# Superset Examples

Example configurations for MySQL, PostgreSQL, SQLite, and Celery are provided, along with a simple demo script for starting them.

Each demo provides a `superset_config.py` and a `docker-compose.yml`. Use these as guides for laying down your own instances.

Start a demo of Superset using the `demo.sh` script. The script takes a single argument that determines the back end for Superset: `sqlite`, `mysql`, `postgres`, or `celery`.

<<<<<<< HEAD
The example requires bazel 0.5.4 or newer to build. You can download/install
the latest version of bazel from bazel's release page:

    https://github.com/bazelbuild/bazel/releases

Once you have bazel installed, simply run the following command in this examples
directory to build the code:

    $ bazel build :all

Then you can run the built binary:

    $ bazel-bin/add_person_cpp addressbook.data

To use protobuf in your own bazel project, please follow instructions in the
[BUILD](BUILD) file and [WORKSPACE](WORKSPACE) file.

## Build the example using make

You must install the protobuf package before you can build it using make. The
minimum requirement is to install protocol compiler (i.e., the protoc binary)
and the protobuf runtime for the language you want to build.

You can simply run "make" to build the example for all languages (except for
Go). However, since different language has different installation requirement,
it will likely fail. It's better to follow individual instructions below to
build only the language you are interested in.

### C++

You can follow instructions in [../src/README.md](../src/README.md) to install
protoc and protobuf C++ runtime from source.

Then run "make cpp" in this examples directory to build the C++ example. It
will create two executables: add_person_cpp and list_people_cpp. These programs
simply take an address book file as their parameter. The add_person_cpp
programs will create the file if it doesn't already exist.

To run the examples:

    $ ./add_person_cpp addressbook.data
    $ ./list_people_cpp addressbook.data

Note that on some platforms you may have to edit the Makefile and remove
"-lpthread" from the linker commands (perhaps replacing it with something else).
We didn't do this automatically because we wanted to keep the example simple.

### Python

Follow instructions in [../README.md](../README.md) to install protoc and then
follow [../python/README.md](../python/README.md) to install protobuf python
runtime from source. You can also install python runtime using pip:

    $ pip install protobuf

Make sure the runtime version is the same as protoc binary, or it may not work.

After you have install both protoc and python runtime, run "make python" to
build two executables (shell scripts actually): add_person_python and
list_people_python. They work the same way as the C++ executables.

### Java

Follow instructions in [../README.md](../README.md) to install protoc and then
download protobuf Java runtime .jar file from maven:

    https://mvnrepository.com/artifact/com.google.protobuf/protobuf-java

Then run the following:

    $ export CLASSPATH=/path/to/protobuf-java-[version].jar
    $ make java

This will create the add_person_java/list_people_java executables (shell
scripts) and can be used to create/display an address book data file.

### Go

The Go example requires a plugin to the protocol buffer compiler, so it is not
build with all the other examples.  See:

    https://github.com/golang/protobuf

for more information about Go protocol buffer support.

First, install the Protocol Buffers compiler (protoc).

Then, install the Go Protocol Buffers plugin ($GOPATH/bin must be in your $PATH
for protoc to find it):

    go get github.com/golang/protobuf/protoc-gen-go

Build the Go samples in this directory with "make go".  This creates the
following executable files in the current directory:

    add_person_go      list_people_go

To run the example:

    ./add_person_go addressbook.data

to add a person to the protocol buffer encoded file addressbook.data.  The file
is created if it does not exist.  To view the data, run:

    ./list_people_go addressbook.data

Observe that the C++, Python, Java, and Dart examples in this directory run in a
similar way and can view/modify files created by the Go example and vice
versa.

### Dart

First, follow the instructions in [../README.md](../README.md) to install the Protocol Buffer Compiler (protoc).

Then, install the Dart Protocol Buffer plugin as described [here](https://github.com/dart-lang/dart-protoc-plugin#how-to-build-and-use).
Note, the executable `bin/protoc-gen-dart` must be in your `PATH` for `protoc` to find it.

Build the Dart samples in this directory with `make dart`.

To run the examples:

```sh
$ dart add_person.dart addessbook.data
$ dart list_people.dart addressbook.data
=======
```bash
bash demo.sh mysql|postgres|sqlite|celery
>>>>>>> a0x8o
```

You will be prompted to set up an admin user.

When finished navigate to [http://localhost:8088/](http://localhost:8088/) to see the demo.

Log in with the credentials you just created.

The demo will live for 5 minutes and then be brought down.

Here is a more detailed explanation of what the demo script is doing:

## MySQL

```bash
cd mysql

# Start Redis & MySQL services
docker-compose up -d redis mysql
# Wait for services to come up fully...

# Start Superset
docker-compose up -d superset
# Wait for Superset to come up fully...

# Initialize Superset DB
docker-compose exec superset superset-demo
# or `docker-compose exec superset superset-init` if no demo data needed

# Play around in demo...

# Bring everything down
docker-compose down -v
```

## PostgreSQL

```bash
cd postgres

# Start Redis & PostgreSQL services
docker-compose up -d redis postgres
# Wait for services to come up fully...

# Start Superset
docker-compose up -d superset
# Wait for Superset to come up fully...

# Initialize demo
docker-compose exec superset superset-demo
# or `docker-compose exec superset superset-init` if no demo data needed

# Play around in demo...

# Bring everything down
docker-compose down -v
```

## SQLite

```bash
cd sqlite

# Start Redis service
docker-compose up -d redis
# Wait for services to come up fully...

# Touch SQLite db file
mkdir -p superset
touch superset/superset.db

# Start Superset
docker-compose up -d superset
# Wait for Superset to come up fully...

# Initialize demo
docker-compose exec superset superset-demo
# or `docker-compose exec superset superset-init` if no demo data needed

# Play around in demo...

# Bring everything down
docker-compose down -v
```

## Celery

```bash
cd celery

# Start Redis & PostgreSQL services
docker-compose up -d redis postgres
# Wait for services to come up fully...

# Start Superset
docker-compose up -d superset
# Wait for Superset to come up fully...

# Start Celery worker
docker-compose up -d worker

# Initialize demo
docker-compose exec superset superset-demo
# or `docker-compose exec superset superset-init` if no demo data needed

# Play around in demo...

# Bring everything down
docker-compose down -v
```
