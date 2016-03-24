# Filebeats

#### Table of Contents

1. [Description](#description)
1. [Setup - The basics of getting started with filebeats](#setup)
    * [Setup requirements](#setup-requirements)
    * [Beginning with filebeats](#beginning-with-filebeats)
1. [Usage - Configuration options and additional functionality](#usage)
1. [Reference - An under-the-hood peek at what the module is doing and how](#reference)
1. [Limitations - OS compatibility, etc.](#limitations)
1. [Development - Guide for contributing to the module](#development)

## Description

Very simple puppet module to install and configure elastic search file beats

## Setup

puppet module install hetzner-filebeats

### Setup Requirements **OPTIONAL**

Puppet labs APT module version 1.8.0 >=
Puppet labs STDLIB module version 4.6.0 >=

### Beginning with filebeats

Use puppet module install function to install module and simply include it from your enc/site.pp.

## Usage

The module can be called with the following parameters:
*`export_log_paths`

An array of Strings that specifies which logs the filebeats application must export.
*`shield_username`

The username filebeats should use to authenticate should your cluster make use of shield
*`shield_password`

The password filebeats should use to authenticate should your cluster make use of shield
*`elasticsearch_proxy_host`

A string containing the hostname of your proxy host used for load balancing your cluster.
If left empty it will default to exporting logs to your local host on port 9200.

## Reference

* `Package`

Configures the apt resrouce for filebeats.
* `Config`

Configures the filebeats.yml file.
* `Service`

Ensures the service is running.
* `Params`

Specifies defaults for the installation and configuration

## Limitations

Does not support SSL/TLS or any other customisations to log exporting besides the very basics.

## Development

All pull requests are welcome. This module was just created for our use and functionality will be added as we require it.
