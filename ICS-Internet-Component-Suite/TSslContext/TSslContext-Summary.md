### Cheat Sheet for SMTP Clients
When configuring TSslContext to support general TSslHtmlSmtpCli operations where security needs are customary and generally adequate, you only need to configure three properties:

| Property         | Recommended Value     | Function                                                                               |
|------------------|-----------------------|----------------------------------------------------------------------------------------|
| SslMethod        | sslV_TLSv1_2_or_later | Guarantees compliance with modern mail servers.                                        |
| SslVerifyPeer    | True                  | Protects your connection from data interception.                                       |
| UseSharedCAStore | True                  | Automates certificate management using built-in bundles or Windows certificate stores. |
