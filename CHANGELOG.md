# Changelog
All notable changes to this project will be documented in this file.

## [1.0.5] - 2019-08-06 - Hotfix
### Features
- Added demo / read only mode function to the system; this can be enabled by setting `DEMO_MODE='yes'` in hestia.conf.
- Added php-imagick module to installer and upgrade scripts.
- Added recidive filter function to fail2ban.
- Refactored Multi-PHP functionality. Support for PHP version selection will be enabled by default on new installations.
- Allowed admin user to add or remove PHP versions from Control Panel UI (available from Server > Configure > Web Server).

### Bugfixes
- Added detection of web root for .well-known ACME challenge.
- Reworked Let's Encrypt ACME staging to use Hestia functions.
- Fixed if condition to use Nginx for Let's Encrypt ACME request if present.
- Reworked v-add-sys-ip, removed CentOS/Red Hat support and reworked conditions.
- Enabled HSTS and force SSL in v-add-letsencrypt-host.
- Prevented login action for webmail in list user view.
- Removed hardcoded mail subdomain in exim HELO data (cosmetic fix).
- Fixed SFTP server validation check, thanks to @dbannik!
- Implemented warning message when creating web domains under admin user.
- v-generate-api-key: Fixed wrong quotes used for default keys folder location.
- Fixed permissions to allow access for FTP users created in web domains under admin account.
- Removed left over file manager code from VestaCP.
- Check if user home directory exists before setting SFTP jail permissions.
- Fixed security issue in v-list-user, thanks to Andrea Cardaci for collaborating with us (https://cardaci.xyz/).

## [1.0.4] - 2019-07-09 - Hotfix
### Bugfixes
- Delayed start of services to prevent restart limit.

## [1.0.3] - 2019-07-09 - Hotfix
### Bugfixes
- Fixed Let's Encrypt Mail SSL permission issue.

## [1.0.1] - 2019-06-25
### Features
- Improved support for Let's Encrypt certificate generation.
- v-add-letsencrypt-host: Added Let's Encrypt support for Control Panel's own SSL.
- Enabled use of per-domain SSL certificates for inbound and outbound mail services.
- Consolidated template structure, removing over 50% duplicate code.
- Re-organised file system structure for domain configuration files.
- Added the ability to change release branches through the user interface and the command line.
- v-sys-update-hestia-git: Added the ability to update using Git from the command line.
- Implemented support for SFTP chroot jails.
- A newly redesigned user interface which features:
    - A softer color palette which better matches the Hestia Control Panel logo colors.
    - A consolidated overview of domains and other information.
    - Improved navigation paths to make things easier to find.
    - Improved compatibility when viewing the Control Panel interface from a mobile device.
- Improved handling of mail domain DNS zone values.
- Enabled OCSP stapling on SSL-enabled web domains.
- v-change-web-domain-hsts: Enabled support for HTTP Strict Transport Security (HSTS) on SSL.
- Improved logging and console output during new installations and upgrades.

### Bugfixes
- Fixed issues with HTTP-to-HTTPS redirecton.
- Fixed an issue where another website would load if browsing to a non-SSL enabled domaing using HTTPS.

## [1.0.0-190618] - 2019-06-25
- Please see release notes for [1.0.1].

## [0.9.8-28] - 2019-05-16
### Features
- Implemented force SSL function for web domains.

### Bugfixes
- 


[CURRENT]: https://github.com/hestiacp/hestiacp
[1.0.5]: https://github.com/hestiacp/hestiacp/releases/tag/1.0.5
[1.0.4]: https://github.com/hestiacp/hestiacp/releases/tag/1.0.4
[1.0.3]: https://github.com/hestiacp/hestiacp/releases/tag/1.0.3
[1.0.1]: https://github.com/hestiacp/hestiacp/releases/tag/1.0.1
[1.0.0-190618]: https://github.com/hestiacp/hestiacp/releases/tag/1.0.0-190618
[0.9.8-28]: https://github.com/hestiacp/hestiacp/releases/tag/0.9.8-28
