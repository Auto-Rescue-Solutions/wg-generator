# WireGuard autosetup

This script will generate the requisite keys for a device.

It will automatically generate a .conf and append it to the network config

for the wg interface and restart the service, as well as generate a .conf for

the client & print a QR code.

This script assumes 1 wg interface and 1 /24 subnet but will auto-detect

both. Client configuration files are generated in the `conf/` dir and QR codes

are saved in `qr/`.

Requires: `qrencode`, `wireguard`, the included `template` client config.

Modify the template with your server's public key and URL. 

Copy the contents of this repo into `/etc/wireguard`

Run with `./new`