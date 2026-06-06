### The Security Settings

These properties dictate the encryption math and the TLS handshake version.

+-------------------------+-------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Property                | Setting                                                                                                     | Function                                                                                                                             |
+=========================+=============================================================================================================+======================================================================================================================================+
| SslMethod (Enumeration) | Protocol Version, (i.e., sslV_TLSv1_2, sslV_TLSv1_3, etc.)                                                  | Sets the allowed TLS/SSL protocol versions possible for use.                                                                         |
+-------------------------+-------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| SslCipherList (String)  | A long, colon-separated string passing raw configuration text directly to OpenSSL (e.g., HIGH:!aNULL:!MD5). | It restricts which mathematical algorithms are used to lock the data. If left blank, ICS lets OpenSSL use its safe, modern defaults. |
+-------------------------+-------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+

:::note
Modern mail servers (like Gmail or Microsoft 365) will instantly terminate connections trying to use obsolete protocol versions like TLS 1.0 or 1.1. In general, always default SslMethod to `sslV_TLSv1_2_or_later` to ensure compatibility with modern standards.
:::

:::note
 You rarely need to specify `SslCipherList` unless a corporate server specifically demands or bans a certain cipher.
:::