# Encrypted personal update channel

This directory carries encrypted, signed recovery metadata for a private client. It contains no plaintext node passwords, API tokens, signing keys, or directly installable APKs.

Release assets with a `.bin` suffix are AES-256-GCM encrypted. They are decrypted only by the privately distributed client and then checked against signed metadata, SHA-256, package identity, and the original APK signing certificate. A downloaded `.bin` file is not an APK.

The recovery channel is independent of the VPN server. Its public address stays fixed when the private server address changes. A configuration refresh is not a software installation, and Android still requires confirmation for an APK installation.
