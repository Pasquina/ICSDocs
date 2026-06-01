Actual use of SSL in your applications requires OpenSSL files:

* libcrypto-3.dll or libcrypto-3-x64.dll
* libcrypto-4.dll or libcrypto-4-x64.dll
* libssl-3.dll or libssl-3-x64.dll
* libssl-4.dll or libssl-4-x64.dll
* legacy.dll or legacy-x64.dll

:::warning
The DLLs are different for versions 3 and 4, but have the same names, don't mix them up.
:::

:::tip
The legacy DLLs are only needed if support for old algorithms is needed; this
includes most password protected PFX/PCS12 certificates. 
:::