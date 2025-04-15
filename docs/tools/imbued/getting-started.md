---
sidebar_position: 2
---

# Getting Started with imbued

This guide will help you install, configure, and start using imbued in less than 5 minutes.

## Installation

### Prerequisites

- Unix-like operating system (macOS, Linux, WSL)
- Bash or Zsh shell
- Git (optional, for installation via clone)

### Option 1: Install via Package Manager

#### macOS (Homebrew)

```bash
brew install novacove/tap/imbued
```

#### Linux (using curl)

```bash
curl -sSL https://install.novacove.ai/imbued | bash
```

### Option 2: Manual Installation

1. Clone the repository:

```bash
git clone https://github.com/novacove/imbued.git
cd imbued
```

2. Run the installation script:

```bash
./install.sh
```

3. Add the following to your shell profile (`.bashrc`, `.zshrc`, etc.):

```bash
# Initialize imbued
source "$HOME/.imbued/init.sh"
```

4. Restart your shell or source your profile:

```bash
source ~/.bashrc  # or ~/.zshrc
```

## Quick Setup

### 1. Initialize a Project

Navigate to your project directory and initialize imbued:

```bash
cd ~/projects/my-awesome-project
imbued init
```

This creates an `.imbued` directory in your project with a template environment file.

### 2. Configure Your Environment Variables

Edit the generated `.imbued/env` file:

```bash
# Project environment variables
export API_KEY="your-api-key-here"
export DATABASE_URL="postgresql://user:password@localhost:5432/db"
export DEBUG="true"
```

### 3. Test It Out

Now, whenever you navigate to your project directory, imbued will automatically load these environment variables:

```bash
cd ~/some-other-directory
# Environment variables are NOT loaded here

cd ~/projects/my-awesome-project
# Environment variables ARE loaded here
echo $API_KEY  # Should display your API key
```

When you leave the directory, the variables are automatically unloaded:

```bash
cd ~/
echo $API_KEY  # Should be empty
```

## Advanced Configuration

### Encrypted Environment Files

For sensitive environments, you can encrypt your environment file:

```bash
imbued encrypt
```

This will prompt you for a password and create an encrypted `.imbued/env.enc` file.

To use the encrypted file:

```bash
imbued decrypt
# Enter your password when prompted
```

### Sharing with Team Members

1. Add the encrypted file to version control:

```bash
git add .imbued/env.enc
git commit -m "Add encrypted environment configuration"
```

2. Share the decryption password securely with your team members.

3. Team members can then decrypt the file:

```bash
imbued decrypt
```

### Multiple Environments

You can create different environment configurations:

```bash
imbued init --env development
imbued init --env production
```

Switch between environments:

```bash
imbued use development
imbued use production
```

## Command Reference

- `imbued init`: Initialize imbued in the current directory
- `imbued status`: Show currently loaded environment variables
- `imbued encrypt`: Encrypt the environment file
- `imbued decrypt`: Decrypt the environment file
- `imbued use <env>`: Switch to a specific environment
- `imbued edit`: Open the environment file in your default editor
- `imbued help`: Display help information

## Troubleshooting

### Variables Not Loading

If your environment variables aren't loading automatically:

1. Ensure imbued is properly initialized in your shell profile
2. Check that the `.imbued/env` file exists and contains valid exports
3. Run `imbued status` to see the current state

### Encryption Issues

If you're having trouble with encrypted files:

1. Make sure you're using the correct password
2. Check file permissions on the `.imbued` directory
3. Try re-encrypting the file: `imbued encrypt --force`

## Next Steps

- Learn about [advanced usage patterns](./advanced-usage)
- Explore [integrating with CI/CD](./ci-cd-integration)
- Check out [best practices for environment management](./best-practices)

## Getting Help

If you encounter any issues or have questions:

- Open an issue on [GitHub](https://github.com/novacove/imbued/issues)
- Join our [community discussions](https://github.com/novacove/imbued/discussions)
- Check the [FAQ](./faq)
