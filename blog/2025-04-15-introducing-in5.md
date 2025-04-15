---
slug: introducing-in5
title: Introducing in5 - Secure Your Environment in 5 Minutes
authors: [novacove]
tags: [in5, security, open-source, imbued]
---

# Introducing in5: Secure Your Environment in 5 Minutes

Today, we're excited to announce the launch of **in5**, a new open-source initiative focused on helping developers secure their environments in 5 minutes or less. As cybersecurity challenges continue to grow in complexity and frequency, we believe that security should be accessible to everyone, not just security experts.

<!-- truncate -->

## The Security Challenge

In today's development landscape, security often feels like an afterthought or a burden. Many developers struggle with:

- **Complexity**: Security tools are often difficult to understand and implement
- **Time constraints**: Security is seen as time-consuming and not immediately valuable
- **Knowledge gaps**: Not everyone has specialized security expertise
- **Friction**: Security measures that hinder productivity tend to be bypassed

The result? Security vulnerabilities that could have been easily prevented with the right tools and practices.

## Our Solution: in5

The **in5** initiative aims to address these challenges by providing simple, effective tools that can be implemented in 5 minutes or less. We focus on practical solutions that address real-world security problems without imposing undue burdens on developers.

Our approach is guided by five core principles:

1. **Security Should Be Accessible**
2. **Practical Over Perfect**
3. **Transparency and Trust**
4. **Defense in Depth**
5. **Developer Experience Matters**

You can read more about these principles in our [documentation](/docs/principles).

## Introducing imbued: Our First Tool

We're launching in5 with our first tool: **imbued**.

**imbued** is a tool that dynamically manages environment variables based on your current directory. It "imbues" your shell session with the appropriate environment variables depending on which project directory you're in, enhancing security by isolating sensitive data and preventing accidental exposure.

### Why Environment Variable Management Matters

Environment variables are a common way to store configuration and sensitive information like API keys, database credentials, and other secrets. However, traditional approaches to environment variable management have several security issues:

1. **Global scope**: Environment variables set in your shell profile are available to all processes
2. **Manual management**: Developers often need to manually source different `.env` files
3. **Accidental leakage**: It's easy to forget which environment variables are set
4. **Inconsistent environments**: Different team members may have different environment setups

**imbued** addresses these issues by providing directory-specific, automatically activated/deactivated environment variables with optional encryption.

## Getting Started

Ready to enhance your security in just 5 minutes? Check out our [Getting Started guide](/docs/tools/imbued/getting-started) to install and configure imbued.

## What's Next?

The in5 initiative is just getting started. We're working on additional tools to address various security challenges, including:

- Secure secret management
- Local development environment hardening
- Automated security scanning
- Secure configuration management

## Join the Community

in5 is an open-source initiative, and we welcome contributions from the community. Whether you're a security expert or a developer interested in improving your security practices, there are many ways to get involved:

- Star and watch our [GitHub repository](https://github.com/novacove/in5)
- Join our [discussions](https://github.com/novacove/in5/discussions)
- Report issues or suggest improvements
- Contribute code or documentation

Together, we can make security more accessible and help developers build more secure applications.

## About NovaCove

[NovaCove](https://novacove.ai) is a cybersecurity company focused on building innovative solutions that make security accessible and effective. The in5 initiative is part of our commitment to improving security practices across the industry.

We believe that by making security tools more accessible and user-friendly, we can help create a more secure digital ecosystem for everyone.

Stay secure!

*The NovaCove Team*
