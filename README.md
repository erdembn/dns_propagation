# DNS Propagation Checker

The DNS Propagation Checker is a Jupyter Notebook script that uses the `nslookup` command to check DNS propagation for a specified domain against different DNS servers. It helps you verify whether a domain's DNS records have propagated across the internet.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Usage](#usage)
- [Using a Custom List of IP Addresses](#using-a-custom-list-of-ip-addresses)
- [License](#license)

## Introduction

When you change your domain's DNS settings, it may take some time for the changes to propagate throughout the internet. This propagation delay can cause discrepancies in DNS resolution, where some users see the old settings while others see the updated ones. The DNS Propagation Checker script allows you to check DNS propagation for your domain against specific DNS servers.

## Requirements

To run this script, you need the following:

- Jupyter Notebook installed on your machine.
- The `dnsutils` package for `nslookup` installed. You can install it using the following command:

```bash
!apt-get -q -y install dnsutils
```

## Usage

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/erdembn/dns_propagation.git
   ```

2. Open the Jupyter Notebook file dns_propagation.ipynb using Jupyter Notebook.

3. Run the cells in the notebook to execute the DNS propagation checks against the default DNS servers (1.1.1.1 and 8.8.8.8) for the domain.

4. Review the output to see the DNS records returned by each DNS server. The output will indicate whether the domain's DNS records have propagated to the specified DNS servers.

## Using a Custom List of IP Addresses

If you want to check DNS propagation against specific DNS servers, you can modify the ip_addresses list in the script with the IP addresses of those DNS servers. For example:

    ```
    ip_addresses = ["1.1.1.1", "8.8.8.8", "4.4.4.4", "208.67.222.222"]

    ```

After updating the ip_addresses list, run the cells again to perform the DNS propagation checks against the new list of DNS servers.

## License

The DNS Propagation Checker is open-source software licensed under the MIT License.
