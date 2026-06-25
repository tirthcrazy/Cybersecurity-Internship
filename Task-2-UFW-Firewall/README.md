# Basic Firewall Configuration with UFW

## Objective

The objective of this project was to configure a basic firewall using UFW (Uncomplicated Firewall) on a Linux system.

## Tool Used

* UFW (Uncomplicated Firewall)
* Kali Linux

## Configuration Steps

The following rules were configured:

* Allowed SSH traffic (Port 22)
* Denied HTTP traffic (Port 80)
* Enabled the firewall

Commands used:

sudo ufw allow ssh

sudo ufw deny http

sudo ufw enable

sudo ufw status verbose

## Firewall Rules

| Service | Port | Action |
| ------- | ---- | ------ |
| SSH     | 22   | Allow  |
| HTTP    | 80   | Deny   |

## Verification

The firewall status was verified using:

sudo ufw status verbose

The output confirmed that SSH traffic was allowed and HTTP traffic was blocked.

## Conclusion

UFW was successfully configured to permit SSH access while blocking HTTP traffic, demonstrating basic firewall rule management and system security configuration.

