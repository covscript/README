# Covariant Script Programming Language Organization
## Copyright
### Interpreter
Copyright © 2017-2023 李登淳(@mikecovlee)
#### Copyright Notice
```
This software is registered with the National Copyright Administration
of the People's Republic of China(Registration Number: 2020SR0408026)
and is protected by the Copyright Law of the People's Republic of China.
```
#### Open Source License
```
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
### Interpreter Extensions
Most of official maintained extensions are licensed under same license as interpreter(Apache 2.0), but some of them are licensed under other license due to the limitations of their dependencies. Please read separate license in the repository carefully.
### Libraries
All libraries written in CovScript and distributed using CSPKG will delivered as source code.

Please read separate license in the repository carefully.
## Definition
Covariant Script Programming Language Organization is an open source organization while it's main duty is maintaining the community edition of Covariant Script Interpreter.

Also, The Covariant Script Organization is the main constitutor of the standardization of Covariant Script Programming Language.

## Composition
### Introduction and Download
See http://covscript.org.cn/ (in Simplified Chinese)
### Documents and Language Standard
See https://csman.info/ (in Simplified Chinese)
### Core Toolchain
https://github.com/covscript/covscript

Interpreter, REPL, Debugger and SDK are included

https://github.com/covscript/ecs

Extended CovScript compiler

https://github.com/covscript/csbuild

Official maintained building and releasing tools

https://github.com/covscript/cspkg

Official maintained package(libraries, extensions, etc.) manager 

#### Standard Library
##### Application

[Standard Utilities](https://github.com/covscript/stdutils)
 + *cffi*: Libffi integration, support calling dynamic libraries directly
 + *bitwise*: Raw binary operations
 + *stdutils*:
   + Useful tools of array
   + Console progress bar
   + Coroutine wrapper
   + Simpile JSON APIs
   + String formatter
   + CSV file reader
   + CRC32 hasher
 + *sdk_extension*: Internal functions provided by SDK

[Zip File Support](https://github.com/covscript/covscript-zip)

[Dear ImGui GUI](https://github.com/covscript/covscript-imgui)

##### Data Processing

[Base64 Codecs, JSON Codec and Hashers](https://github.com/covscript/covscript-codec)

[Data Analysis Framework](https://github.com/covscript/covanalysis)

[Mike Lee's LR Parser](https://github.com/mikecovlee/parsergen)

[Regular Expression](https://github.com/covscript/covscript-regex)

##### Database

[CovScript Database Connectivity](https://github.com/covscript/csdbc)

[ODBC Database Connectivity](https://github.com/covscript/covscript-database)

[SQLite3 Database](https://github.com/covscript/covscript-sqlite)

##### Network

[ASIO Network](https://github.com/covscript/covscript-network)

[cURL Network](https://github.com/covscript/covscript-curl)

[Network Utilities](https://github.com/covscript/netutils)
 + Simple HTTP Server
 + Simple HTTP Client (GET and POST)

##### System

[Darwin Console Graphics](https://github.com/covscript/covscript-darwin)

[LibMozart Process](https://github.com/covscript/covscript-process)

##### Platform Specified Library

[wiringPi](https://github.com/covscript/covscript-wiringpi)

## Package Submitting

[CSPKG Source](https://github.com/covscript/cspkg-sources)

[Build your package](https://github.com/covscript/cspkg#build-your-package)

[Build your package with CSBuild](https://github.com/covscript/csbuild#build-your-package-with-csbuild)

## Legacy Platforms

Covariant Script drops mainstream support for legacy platforms listed below:
+ Microsoft Windows XP, Vista or older versions
+ 32-bit support for Microsoft Windows and macOS

To satisfy some special compatible requirements, we provide incomplete support for these platforms:
+ [Microsoft Windows XP 32-bit](https://github.com/covscript-archives/legacy_windows_support/)
  + Lack of CSPKG and Libcurl support
