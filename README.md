# Case-Mount-Item-Export


[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0) ![This script was last tested in Nuix 8.8](https://img.shields.io/badge/Script%20Tested%20in%20Nuix-9.2-green.svg)

View the GitHub project [here](https://github.com/clgillis/Case-Mount-Item-Export) or download the latest release [here](https://github.com/clgillis/Case-Mount-Item-Export/releases).

# Overview
Display your Nuix selected case items as a drive letter (windows). This script when run will mount a drive letter representing the items you have selected.

![Drive letter](https://raw.githubusercontent.com/Nuix/Case-Mount/main/images/webDav%20Nuix%20drive.png)

## Why would you want to do this?

Prevention of any items exported for discovery that may contain a virus, malware, worms, etc. An antivirus application can be used to scan the drive mount and any items deleted will be added to an exclusion list in your original case named 'deleted'.

# Getting Started

## Setup

Begin by downloading the latest release.  Extract the contents of the archive into your Nuix scripts directory.  In Windows the script directory is likely going to be either of the following:

- `%appdata%\Nuix\Scripts` - User level script directory
- `%programdata%\Nuix\Scripts` - System level script directory

## Usage

## Select items to be mounted.

Filter and select the items in your case you want mounted.  

Alternatively, select no items to export and the script will mount the entire case.

### Ensure you have access to the binary source

To do this attempt to do a 'save as...' through the workstation GUI. If there are errors here it would be a good idea to make your source available.

Alternatively, highlight an item and check the Binary tab in the Preview window and see if you have data.  If the tab is blank you do not have access to the binary source.

### Scripts -> Run Case Mount Item Export

This will prompt for:

IP Address <-- most of the time the server will default to 127.0.0.1 for private access, however you can change it for a network address and allow others access to your case.

### Wait

A cache will be built (progress dialog) which after a short while will finish and a drive letter will be shown to the user.
Drive letter is chosen from N: onwards.

### Enjoy navigating!

When you are finished, disconnect the drive in windows. The script checks every few seconds for the drives presence and when it is no longer used the webDav server will be stopped.

As a failsafe when the case goes into a processing/reloading/closing states the server will also be stopped.

### Extra
The port is usually going to be port 80, if unavailable will choose the next port.
Similarly with Drive letter, the default is N: if unavailable the next letter will be chosen

# License

```
Copyright 2021 Nuix

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
