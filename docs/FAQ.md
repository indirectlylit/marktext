# Frequently Asked Questions (FAQ)

### What are the supported platforms?

Mark Text is a desktop application and available for:

- Linux x64 (tested on Debian and Red Hat based distros)
- macOS 10.10 x64 or later
- Windows 7-10 x86 and x64

### Is Mark Text open-source and free?

Yes, Mark Text is licensed under the [MIT](https://github.com/marktext/marktext/blob/develop/LICENSE) license and completely free for everyone. The source-code is available on [GitHub](https://github.com/marktext/marktext).

### Can I use Mark Text as note management/taking app?

Mark Text is a pure markdown editor without feature such as knowledge management and tags but yes, you can do this via the integrated filesystem explorer and task lists.

### Where can I find documentation?

Documentation is currently under development.

- [End-user documentation](https://github.com/marktext/marktext/blob/develop/docs/README.md)

- [Developer documentation](https://github.com/marktext/marktext/blob/develop/docs/dev/README.md)

### Can I run a portable version of Mark Text?

Yes, please see [here](PORTABLE.md) for further information.

### How can I report bugs and problems

You can report bugs and problems via our [GitHub issue tracker](https://github.com/marktext/marktext/issues). Please provide a detailed description of the problem to better solve the issue.

### I cannot launch Mark Text on Linux (SUID sandbox)

> *The SUID sandbox helper binary was found, but is not configured correctly.*

Normally, you should never get this error but if you disabled user namespaces, this error message may appears in the command output when launching Mark Text. To solve the issue, that Chromium cannot start the sandbox (process), you can choose one of the following steps:

- Enable Linux kernel user namespaces to use the preferred sandbox: `sudo sysctl kernel.unprivileged_userns_clone=1`.
- Set correct SUID sandbox helper binary permissions: `sudo chown root <path_to_marktext_dir>/chrome-sandbox && sudo chmod 4755 <path_to_marktext_dir>/chrome-sandbox`. This is prefered if you don't want to enable user namespaces.
- Launch Mark Text with `--no-sandbox` argument.

### What is a "Aidou" ?

Aidou is a chinese service that provides images to illustrate articles or blog post. You can enable/disable it via your preferences. Once enabled it is available under 'Aidou' in the 'Edit' menu.
