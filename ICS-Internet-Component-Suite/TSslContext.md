## General Comments
In attempting to implement a TSslHtmlSmtpCli ICS component I ran into something of a paucity of documentation, and certainly my own understanding of TSslHtmlSmtpCli along with TSslContext is very rudimentary at best. Therefore, I resovled to do a little research to clarify my own understanding of the components and document my findings in a form I could easily access for future reference. Simultaneously, these pages might be useful to the community at large; feel free to explore them and let me know of any errors or failings you may discover.

### What Is `TSslContext`?
`TSslConterxt` is a wrapper around the vast, raw `OpenSSL` C-API. According to Google it is…

> …a wall of cryptographic acronyms, opaque and lacking structured documentation.

:::note
`TSslContext` is used by a number of other ICS components, but not necessarily by all. If a particular component supports SSL/TLS then it is likely that it will require an instance ofd TSslContext to run correctly.
:::

### Understanding `TSslContext`
To assist in understanding `TSslContext` the discussion is divided into sections that cover distinct functional topics.

- [Certificate Validation](dm-topic://_s2d4j1yfg4)
- [Protocol and Cypher Control](dm-topic://_8mdxxfiyfj)
- [Client Authentication](dm-topic://_czb0pz9a72)

:::tip
Additonally, there is a [TSslContext Summary](dm-topic://_08u9e3tk0r) is included as a quick reference or cheat sheet.
:::