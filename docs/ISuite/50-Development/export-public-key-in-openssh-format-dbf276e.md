<!-- loiodbf276e7a5b34d17b87bfc0478f7e6d8 -->

# Export Public Key in OpenSSH Format

Export a public key in OpenSSH format.



Perform the following call:


<table>
<tr>
<th valign="top">

Method



</th>
<th valign="top">

Resource Path



</th>
</tr>
<tr>
<td valign="top">

GET



</td>
<td valign="top">

 `/KeystoreEntries('{Hexalias}')/Sshkey/$value` 



</td>
</tr>
</table>

The following keys are supported: rsa-encrypted and dsa-encrypted keys. Other algorithms \(for example, elliptic curve \(EC\)\) aren't supported.

Assume you like to get the public key of keystore entry `baltimore cybertrust root` \(hexadecimal value: `62616c74696d6f7265206379626572747275737420726f6f74`\) in OpenSSH format, send the following GET request:

`https://<host address>/api/v1/KeystoreEntries('62616c74696d6f7265206379626572747275737420726f6f74')/Sshkey/$value`

Certain values \(for example, for the alias when indicated in the example request as `<hexalias>`\) need to be provided in hexadecimal notation. String characters are stored by the computer as numbers. When the hexadecimal notation is required, the text is to be provided not as decimal number but as a hexadecimal number instead. For example: The string `my alias` is expressed by the following decimal numbers: `109 121 32 97 108 105 97 115` \(because, according to the American Standard Code for Information Interchange \(ASCII \), the letter `m` is translated to the decimal number `109`, and so forth\). If you convert each number to a hexadecimal number, you get: `6D 79 20 61 6C 69 61 73`. Note that `6D` is the hexadecimal representation of `109`, and so forth. If you like to specify `my alias` in an example request, enter `6D7920616C696173`.

As response, you get:

```
ssh-rsa AAAAB3NzaC1yc2E ...... dKoanTZDcJxo5 public key for alias baltimore cybertrust root
```

