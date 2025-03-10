# Fluent Bit Packaging

This directory contains Docker files used to build [Fluent Bit](http://fluentbit.io) Linux packages for different distros, the following table describe the supported targets:

| Distro       |   Version / Code Name   | Arch    | Target Option           |
|--------------|-------------------------|---------|-------------------------|
| AmazonLinux  |   2                     | x86_64  | amazonlinux/2           |
| AmazonLinux  |   2                     | arm64v8 | amazonlinux/2.arm64v8   |
| CentOS       |   8                     | x86_64  | centos/8                |
| CentOS       |   8                     | arm64v8 | centos/8.arm64v8        |
| CentOS       |   7                     | x86_64  | centos/7                |
| CentOS       |   7                     | arm64v8 | centos/7.arm64v8        |
| Debian       |   10                    | x86_64  | debian/buster           |
| Debian       |   10                    | arm64v8 | debian/buster.arm64v8   |
| Debian       |   9                     | x86_64  | debian/stretch          |
| Debian       |   9                     | arm64v8 | debian/stretch.arm64v8  |
| Debian       |   8                     | x86_64  | debian/jessie           |
| Debian       |   8                     | arm64v8 | debian/jessie.arm64v8   |
| Ubuntu       |   20.04 / Focal Fossa   | x86_64  | ubuntu/20.04            |
| Ubuntu       |   18.04 / Bionic Beaver | x86_64  | ubuntu/18.04            |
| Ubuntu       |   16.04 / Xenial Xerus  | x86_64  | ubuntu/16.04            |
| Raspbian     |   10 / Buster           | arm32v7 | raspbian/buster         |
| Raspbian     |   9 / Stretch           | arm32v7 | raspbian/stretch        |
| Raspbian     |   8 / Jessie            | arm32v7 | raspbian/jessie         |
| openSUSE     |   15 / Leap             | x86_64  | opensuse/leap           |

## Usage

The _build.sh_ script can be used to build packages for a specific target, the command understand the following format:

```
$ ./build.sh -v VERSION -d DISTRO [-b BRANCH_NAME] [-t TARBALL]
```

Details about the script parameters:

| Name        | Description                  | Example                |
|-------------|------------------------------|------------------------|
| VERSION     | Github Tag or version number  | 1.3.x                 |
| TARGET      | Target platform for the packages | ubuntu/18.04       |

Optionally the script supports the option __-b__ to specify a custom branch, this is useful to package and test _master_ or specific branches.

### Build examples

#### Package version 1.3.1 for Ubuntu 18.04:

```
$ ./build.sh -v 1.3.1 -d ubuntu/18.04
```
