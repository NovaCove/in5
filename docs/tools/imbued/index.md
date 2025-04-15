---
sidebar_position: 1
---

# imbued

**Dynamic environment variable management for enhanced security**

## What is imbued?

**imbued** is a tool that dynamically manages environment variables based on your current directory. It "imbues" your shell session with the appropriate environment variables depending on which project directory you're in, enhancing security by isolating sensitive data and preventing accidental exposure.

## The Problem

Environment variables are a common way to store configuration and sensitive information like API keys, database credentials, and other secrets. However, traditional approaches to environment variable management have several security issues:

1. **Global scope**: Environment variables set in your shell profile (like `.bashrc` or `.zshrc`) are available to all processes, increasing the risk of accidental exposure
2. **Manual management**: Developers often need to manually source different `.env` files when switching between projects
3. **Accidental leakage**: It's easy to forget which environment variables are set, leading to potential security issues when running untrusted code
4. **Inconsistent environments**: Different team members may have different environment setups, leading to "works on my machine" problems

## How imbued Solves It

imbued addresses these issues by:

1. **Directory-based activation**: Environment variables are only loaded when you're in the relevant project directory
2. **Automatic switching**: Variables are automatically loaded and unloaded as you navigate between projects
3. **Isolation**: Each project's environment variables are isolated from other projects
4. **Visibility**: Clear indication of which environment variables are currently active
5. **Version control friendly**: Store encrypted environment files safely in version control

## Key Features

- **Directory-specific environments**: Different environment variables for different projects
- **Automatic activation/deactivation**: Variables are loaded/unloaded as you change directories
- **Secure storage**: Optional encryption of environment files
- **Shell integration**: Works with bash, zsh, and other common shells
- **Minimal overhead**: Designed to be fast and lightweight
- **Team sharing**: Securely share environment configurations with team members

## Use Cases

imbued is particularly useful for:

- **Developers working on multiple projects** that require different API keys or configurations
- **Teams that need consistent environments** across all team members
- **Security-conscious organizations** looking to minimize the risk of credential leakage
- **Open source contributors** who want to isolate project environments

## Getting Started

Ready to enhance your environment variable security? Check out our [Getting Started guide](./getting-started).
