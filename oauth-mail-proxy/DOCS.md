# OAuth Mail Proxy

## Description

OAuth Mail Proxy is a Home Assistant add-on that provides secure email functionality via IMAP with OAuth2 authentication support. This was put together specifically to help support the Mail and Packages component that relies on IMAP.

## Features

- OAuth2 authentication for secure mail access via IMAP

## Installation

1. Add this repository to Home Assistant
2. Install the OAuth Mail Proxy add-on
3. Configure your OAuth credentials and mail server settings

- You can manually configure by following configuration instructions for [https://github.com/simonrob/email-oauth2-proxy](https://github.com/simonrob/email-oauth2-proxy)
- Use my [ha-oauth-mail](https://github.com/nathanfiscus/ha-oauth-mail) custom component to setup the proxy.

4. Start the add-on

## Configuration

No UI configuration required, but a port must be enabled for IMAP communication. Default is 1993.

## Support

For issues and feature requests, visit the repository.

## AI Disclaimer

This project used AI to integrate it with my other custom component to help create the configuration file via the Home Assistant front-end
