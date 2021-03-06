# gerberos

gerberos scans sources for lines matching regular expressions and containing IPv4 or IPv6 addresses and performs actions on those addresses.
Possible sources are (not necessarily existant) non-directory files and systemd journals.
Addresses can be logged or added to ipsets (`gerberos4` and `gerberos6`) that gerberos will manage autonomously.

Minimal additional logic is applied. This is to adhere to the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy), but impacts gerberos' out-of-the-box usefulness for specific use cases when compared to tools like [fail2ban](https://github.com/fail2ban/fail2ban).

## Requirements

- Go 1.15.2 (development only)
- GNU Make 4.3 (development only, optional)
- ipset 6.34
- iptables 1.6.1

## Build

`make build`

## Example configuration file (TOML)

See [gerberos.toml](gerberos.toml).

## Example systemd service file

See [gerberos.service](gerberos.service).
