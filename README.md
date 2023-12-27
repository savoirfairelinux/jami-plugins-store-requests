# Plugins Store Request Repository

This repository is used to request a certificate to be illegible for the [Plugins Store](https://dl.jami.net/plugins) and upload new plugin.

**Jami Plugin Store** is a repository of plugins for the Jami client. It is a way for developers to share their plugins with the community.
It is also a way for users to securely find and install plugins.

## Request an organization certificate

To request a certificate for your organization, please open an issue with the [given template](https://github.com/savoirfairelinux/jami-plugins-store-requests/issues/new?assignees=&labels=organization+plugins+store+request&projects=&template=organization-request.md&title=).

1. Create a new certificate signing request (CSR) for your organization with [Plugins tool](https://git.jami.net/savoirfairelinux/jami-plugins).
2. Keep the private key and send the CSR to us with the command ```/csr <your-csr>.gz``` .
3. If the CSR is valid, a message will confirm that your certificate is ready to be check by our team.
4. If your CSR is not valid, a message will tell you to retry.
> Note: It's very recommanded to use the Plugins tool to create your CSR. If you use another tool,
please make sure that your CSR is valid with the command ```openssl req -text -noout -verify -in <your-csr>.gz``` and you use gzip compression.
4. If your organization is illegible, we will send you back your certificate signed by the ca.

## Submitting a plugin

To request to upload a plugin, please open an issue with the [given templace]().

1. Sign your plugin with [Plugins tool](https://git.jami.net/savoirfairelinux/jami-plugins) and your certificate.
If you don't have a certificate, please follow the steps to [request a certificate](#request-an-organization-certificate)
2. Please upload your plugin in a source that can be fetch by anyone. To be sure, use this command:  curl -o tmp/plugin.jpl -L <url-to-fetch-file>
3. Please use the command to start the verification: /upload <url-to-fetch-file> as a comment in the issue
4. Wait until it respond successfully to the verification.
5. An administrator will upload your plugin.

## More Information

For more information about the Plugins Store, please visit the [Plugins Store documentation](https://git.jami.net/savoirfairelinux/jami-docs/-/blob/master/developer/jami-plugins-certificate.md).