# OpenConnect VPN Manager (ocvpn)
ocvpn is a simple yet powerful Bash script for managing VPN connections on Ubuntu systems. It utilizes openconnect for VPN connectivity and allows users to easily switch between multiple VPN profiles defined in an environment file.

## Features
- Automates the installation of openconnect if not present.
- Manages multiple VPN connections through a .env configuration file.
- Easy switching between different VPN profiles.

## Prerequisites
- Ubuntu or a similar Linux distribution.
- Bash shell.
- `sudo` privileges for installing openconnect.

## Installation
1. Clone the Repository:

```bash
git clone https://github.com/danialzash/openconnect.git
cd ocvpn
```

2. Prepare the Environment File:

- Copy the example environment file:

```bash
cp .env.example .env
```

- Edit .env to include your VPN credentials and server details.

3. Make the Script Executable:

```bash
chmod a+x ocvpn
```

4. Optional: Add Script to Path

Move the script to a directory in your PATH, for example:

```bash
sudo mv ocvpn /usr/local/bin/
```
- Reload the shell configuration:

```bash
source ~/.bashrc
```

## Usage

After installation, you can use ocvpn to connect to your VPNs:

- Connect to the Default VPN:

```bash
ocvpn
```

- Connect to a Specific VPN Profile:

  - If you have VPN_SERVER_2 set in your .env, use:

```bash
ocvpn 2
```

  - Replace 2 with the appropriate profile number for other servers.


## Configuring VPN Profiles
In the .env file, define each VPN profile like this:

```
VPN_USER=your_username
VPN_PASS=your_password
VPN_SERVER=vpn.default.com
VPN_SERVER_2=vpn.secondary.com
...
```

Replace the values with your actual VPN credentials and server addresses.

## Contributing
Contributions are welcome! Feel free to submit pull requests or open issues for any improvements or suggestions.

