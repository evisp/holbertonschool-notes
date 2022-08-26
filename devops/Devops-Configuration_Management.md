# DevOps: Configuration Management

## Introduction to Configuration Management

- Refers to the process of systematically handling changes to a system in a way that it maintains integrity over time. Automation plays an essential role in server configuration management. Automation is, in fact, the heart of configuration management for servers.
- There are a number of configuration management tools available in the market. `Puppet`, `Ansible`, `Chef` and `Salt` are popular choices.

## Puppet Resource Type: File
- The `file` type manages files, including their content, ownership, and permissions. The type should be specified in the ensure attribute. File contents can be managed directly with the content attribute, or downloaded from a remote source using the source attribute