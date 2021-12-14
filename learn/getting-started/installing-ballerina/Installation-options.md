---
layout: ballerina-installing-ballerina-left-nav-pages-swanlake
title: Installation Options
description: Get started with the Ballerina programming language by following these instructions on installing and setting up Ballerina.
keywords: ballerina, installing ballerina, programming language, ballerina installation
permalink: /learn/installing-ballerina/installation-options/
active: installation-options
intro: The sections below include information about installing Ballerina.
redirect_from:
  - /learn/installing-ballerina
  - /learn/installing-ballerina/
  - /learn/installing-ballerina/#installing-from-source
  - /learn/installing-ballerina/#installing-from-source/
  - /swan-lake/learn/getting-started/installing-ballerina/
  - /swan-lake/learn/getting-started/installing-ballerina
  - /learn/getting-started/installing-ballerina/
  - /learn/getting-started/installing-ballerina
  - /learn/user-guide/getting-started/setting-up-ballerina/installation-options
  - /learn/user-guide/getting-started/setting-up-ballerina/installation-options/
  - /learn/user-guide/getting-started/installation-options
  - /learn/user-guide/getting-started/installation-options/
  - /learn/getting-started/installing-ballerina/installation-options
  - /learn/getting-started/installing-ballerina/installation-options/
  - /learn/installing-ballerina/installation-options
---



## Installing Ballerina via Installers

Follow the instructions below to install the latest Ballerina version using the installer. The installer will automatically uninstall the old Ballerina version if you have one already installed.

>**Info:** Ballerina installers support operating systems such as Windows, Ubuntu, Red Hat Enterprise Linux, macOS, and CentOS. If you are using an unsupported operating system, [install via the Ballerina language ZIP file](#installing-via-the-ballerina-language-zip-file).

### Installing on macOS

[Download the package file](/downloads) and double-click on it to launch the installer. The installer guides you through the installation process and installs the Ballerina distribution in the `/Library/Ballerina` directory.

The package automatically sets your PATH environment variable for you. You may need to restart any open Terminal sessions for the change to take effect.

### Installing on Windows

[Download the MSI file](/downloads) and double-click on it to launch the installer. The installer guides you through the installation process and installs the Ballerina distribution in the `C:\Program Files\Ballerina` directory.

The installer should put the `C:\Program Files\Ballerina\<BALLERINA-DIRECTORY>\bin` directory in your PATH environment variable. You may have to restart any open command prompts for the change to take effect.

### Installing on Linux

[Download the DEB file or RPM file](/downloads) and double-click on it to launch the installer. The installer guides you through the installation process and installs the Ballerina distribution in the following directory.
- For DEB file:  `/usr/lib/ballerina`
- For RPM file:  `/usr/lib64/ballerina`

> **Info:** Alternatively, you can use either of the commands below to install Ballerina using the downloaded DEB or RPM file. Replace the `ballerina-linux-installer-x64-<BALLERINA-VERSION>.deb` or `ballerina-linux-installer-x64<BALLERINA-VERSION>.rpm` with the actual file path. 

For example, for the DEB file:
```
dpkg -i ballerina-linux-installer-x64-swan-lake-<VERSION>.deb 
```

For example, for the RPM file:
```
rpm -i ballerina-linux-installer-x64-swan-lake-<VERSION>.rpm 
```


## Installing via the Ballerina Language ZIP File

> **Note:** Before you install Ballerina using the ZIP file, ensure that you have a supported Java Runtime Environment (JRE) installed. It is recommended to use the [AdoptOpenJRE](https://adoptopenjdk.net/) version 11 or above.

1. <a id="packWindows" href="{{ site.dist_server }}/downloads/{{ site.data.swanlake-latest.metadata.version }}/ballerina-{{ site.data.swanlake-latest.metadata.version }}.zip" class="cGTMDownload cDownload" data-download="downloads" data-pack="{{ site.data.swanlake-latest.metadata.zip-installer }}"> Download the Ballerina language ZIP file </a> <a href="{{ site.dist_server }}/downloads/{{ site.data.swanlake-latest.metadata.version }}/ballerina-{{ site.data.swanlake-latest.metadata.version }}.zip.md5">(md5, </a> <a href="{{ site.dist_server }}/downloads/{{ site.data.swanlake-latest.metadata.version }}/ballerina-{{ site.data.swanlake-latest.metadata.version }}.zip.sha1">SHA-1, </a> <a href="{{ site.dist_server }}/downloads/{{ site.data.swanlake-latest.metadata.version }}/ballerina-{{ site.data.swanlake-latest.metadata.version }}.zip.asc">asc)</a> and unzip it to a preferred location using an archiver tool of your choice. This creates a directory named `ballerina-<VERSION>` in your system.

2. Follow either of the steps below depending on your operating system to configure your system environment to run Ballerina:
    - **For Linux or macOS:** set the PATH environment variable to point to the bin directory of the unzipped Ballerina distribution.
    - **For Windows:** add a new environment variable specifying the following values:
        - **Variable name:** PATH
        - **Variable value:** The location of the bin directory of the unzipped Ballerina distribution. For example, `C:\Program Files\Ballerina\ballerina-<VERSION>\bin`


## Verifying the Installation

After installing Ballerina, run the following test to verify if Ballerina has been successfully installed. 

Execute the command below from the command shell of the operating system.

```bash
bal -v
```

Make certain the command output shows the version that you downloaded as shown below.

```bash
Ballerina Swan Lake <VERSION>
Language specification 2021R1
Update Tool 1.3.6
```

## Updating Ballerina

If you already have a jBallerina version above 1.1.0 installed, you can use the update tool to update to the latest jBallerina version and set it as the active version by executing either of the commands below.

**Command**|**Description**
:-----:|:-----:
`bal dist update`|Update to the latest patch version of the active distribution
`bal dist pull latest`|Update to the latest jballerina version
`bal dist pull <JBALLERINA-VERSION>`|Fetch a specific distribution 

For more information, see [Keeping Ballerina Up to Date](/learn/tooling-guide/cli-tools/update-tool/).


## Building from Source

For instructions, see [Building from Source](/learn/user-guide/getting-started/building-from-source/).



## Uninstalling Ballerina

Usually, the installation location is `/Library/Ballerina/` in macOS, `/usr/lib/ballerina/` for DEB and `/usr/lib64/ballerina/` for RPM in Linux, and `C:\Program Files\Ballerina\` in Windows.

To remove:

- a specific jBallerina version (via the update tool): execute `bal dist remove` 
- all non-active distributions (via the update tool): execute `bal dist remove -a` 
- all the installed jBallerina versions: delete the `/../Ballerina` directory in the respective installation location

> **Info:** Alternatively, you can uninstall Ballerina using the commands below by replacing the actual package name in Linux and from the control panel in Windows.

For example, for the DEB file:
```
apt-get remove ballerina-swan-lake-<VERSION>
```

For example, for the RPM file:
```
rpm -e ballerina-swan-lake-<VERSION>
```


## What's Next?

Once you have successfully installed Ballerina, now you can [write your first Ballerina program](/learn/user-guide/getting-started/writing-your-first-ballerina-program/).

>**Tip:** To get help when you work with Ballerina, see [Community](/community).

