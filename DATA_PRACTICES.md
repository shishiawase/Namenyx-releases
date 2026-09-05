# Namenyx Data Practices Notice

Version 1.0 — effective 1 September 2026

This notice describes data handled by the Namenyx desktop application and official Namenyx modules. It does not describe separately installed third-party modules, whose publishers must provide their own disclosures.

## Local data

Namenyx stores application settings, module configuration, module packages, operational state and logs on the user's device. Authentication tokens, webhook credentials, passwords and module secrets managed through the Namenyx secret API are stored using Windows Credential Manager.

Logs can contain channel identifiers, account names, command input, operational events and error details. Namenyx attempts to redact known secret formats, but logs should still be reviewed before they are shared.

## Data sent to services

When a user configures and enables the relevant feature, Namenyx or an official module may send the data required to perform that feature directly to the selected service. Depending on configuration, this can include:

- authentication credentials and account, channel, stream or chat data exchanged with Twitch;
- notification content and stream information sent to a configured Discord or Telegram destination;
- commands and status exchanged with an OBS WebSocket endpoint selected by the user;
- update and module-catalog requests sent to the configured distribution sources.

The receiving service processes that data under its own terms and privacy policy. Namenyx does not control the service's retention or subsequent processing.

## Module permissions

Modules receive access through declared Namenyx capabilities. The installation and update interfaces show the permissions and disclosed transmitted-data categories supplied by the module package. Granting a permission makes the corresponding Core capability available; it is not a guarantee about how a third-party module will use that access.

Official modules are covered by this notice. Third-party modules are independent software. Review their publisher, source, permissions, license and data disclosures before installation or update.

## Retention and removal

Local data remains on the device until it is replaced or removed by the application, the user or the operating system. Removing a module can remove its package and module data, but data already sent to an external service remains subject to that service's controls. Removing Namenyx does not necessarily remove credentials or application data unless the relevant removal option is selected.

Users should remove credentials, module data and logs they no longer need and use the relevant service controls for data already transmitted externally.
