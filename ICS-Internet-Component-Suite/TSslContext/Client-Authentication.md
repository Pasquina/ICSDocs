### The Identity Settings
These properties are used if the mail server requires your software to present its own certificate before allowing a connection.

:::Note
This is completely distinct and apart from your standard username and password.
:::

+------------------------+--------------------------------------------------------------------------+-----------------------------------------------------------------------------+
| Property               | Setting                                                                  | Function                                                                    |
+========================+==========================================================================+=============================================================================+
| SslCertfile (String)   | Path to the public client certificate file (.pem or .crt).               | Provides access to the certificate that verifies your client to the server. |
+------------------------+--------------------------------------------------------------------------+-----------------------------------------------------------------------------+
| SslPrivateKey (String) | Path to the private key file (.key) associated with the certificate.     | Allows the client to utilize the private key for encryption purposes.       |
+------------------------+--------------------------------------------------------------------------+-----------------------------------------------------------------------------+
| SslPassword (String)   | The passphrase used to unlock the SslPrivateKey file if it is encrypted. | Allows the client to utilize the private key for encryption purposes.       |
+------------------------+--------------------------------------------------------------------------+-----------------------------------------------------------------------------+

:::tip
These three properties remain entirely blank for nearlyh all public SMTP configurations (Gmail, SendGrid, Mailgun). They are generally utilized for high-security enterprise architectures demanding mutual TLS (mTLS).
:::