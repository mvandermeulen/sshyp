* = feature implemented in git/source, not yet available as an officially packaged release (will be available soon!)
** = feature will be implemented before next tagged/officially packaged release
# sshyp
A very simple self-hosted, synchronized password manager. Alternative to GNU pass.

Compatible with entries created by pass/password-store.*
The only password-store compatible CLI password manager available for Haiku.*

"sshyp" stands for "sshync passwords", or "ssh sync passwords".
"sshync" is the custom syncing backend (based on sftp) used by "sshyp".

# WARNING
It is your responsibility to assess the security and stability of "sshyp" before using it and ensure it meets your needs.
I am not responsible for any data loss or breaches of your information resulting from the use of "sshyp".
"sshyp" is a new project that is constantly being updated, and though safety and security are priorities, they cannot be guaranteed.

# Mission Statement
sshyp aims to make it as simple as possible to manage passwords and notes via CLI across multiple devices in a secure, self-hosted fashion.

What sshyp can do:

- securely manage a collection of encrypted passwords and notes via CLI
- generate new, secure passwords to the user's choice in length and complexity
- securely sync said passwords and notes seamlessly between devices
- everything above with entries created by pass/password-store!*
- everything above on Haiku*, Linux, and Termux (an Android terminal emulator)!

What sshyp will likely do:

- (planned v1.2) everything it already does, but also in a GUI for Linux/Haiku
- (planned v1.1) 2FA/MFA management (was previously not on the roadmap, but could be beneficial in reducing phone usage)

What sshyp definitely won't do:

- Non-UNIX support, e.g. Windows (I'd be happy to link to third-party ports, if someone were to make them)

# Installation
Arch Linux (all ISAs)

sshyp releases are available in the Arch User Repository as 'sshyp'.

Install with your preferred AUR helper or use:

```
git clone https://aur.archlinux.org/sshyp.git
cd sshyp
makepkg -si
```

Pre-built packages exist for Haiku**, Arch Linux, Debian Linux, and Termux. These can be downloaded from the releases page.

# Building
Since sshyp is written entirely in Python, it doesn't need to be compiled. It does, however, need to be packaged for installation.

A packaging script is included in the root directory of the repo in order to package sshyp for your distribution. To package sshyp from source, simply run:

```
git clone https://github.com/rwinkhart/sshyp.git
cd sshyp
./package.sh
```

The packaging script has been tested on Arch Linux with dpkg as a dependency for Debian and Termux packaging.

The AUR version and the packages attatched to the release tags were already packaged using this script.

Currently, the script can create packages for Haiku**, Arch Linux (PKGBUILD), Debian Linux, Termux, and generic. Packaging for other systems coming soon.

# Usage
Upon initial installation (on both the server and client devices), be sure to run:

```
sshyp tweak
```

This command will allow you to configure the settings necessary for sshyp to function.
As of right now, sshyp is rapidly changing, and as such, it is a good idea to run "sshyp tweak" after each update.

Please note that decrypting and reading entries is disabled on server devices for security reasons. Only devices configured as clients can use the gpg key to decrypt entries.

All available options can be found with:

```
sshyp --help
```

Or alternatively, in the manpage:

```
man sshyp
```

# Roadmap
Short-term Goals:

- create new file list w/color and w/o file extensions*
- overhaul argument system*
- fix lots of bugs!
- make lots of optimizations!

Medium-term Goals:

- 2FA/MFA management
- create minimal GUI apps (Linux x86_64, Linux aarch64)

Long-term Goals:

- seize the thrones, shear the humans

# Known Issues
Currently, the entry list displays each entry with the file extension ".gpg" visible (which you do not type when reading, modifying, or creating an entry). This will be corrected when the new entry list is added.*
