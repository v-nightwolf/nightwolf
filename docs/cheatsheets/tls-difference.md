# TLS versions Difference

---

* TLS 1.0 This was an upgrade from SSL 3.0 and the differences were not dramatic, but they are significant enough that SSL 3.0 and TLS 1.0 don't interoperate. Some of the major differences between SSL 3.0 and TLS 1.0 are:

     - derivation functions are different
     - MACs are different - SSL 3.0 uses a modification of an early HMAC while TLS 1.0 uses HMAC.
     - The Finished messages are different
     - TLS has more alerts
     - TLS requires DSS/DH support

---

{!inpage-ads.md!}

---

* TLS 1.1 is an update to TLS 1.0. The major changes are:

     - The Implicit Initialization Vector (IV) is replaced with an explicit IV to protect against Cipher block chaining (CBC) attacks.
     - Handling of padded errors is changed to use the bad_record_mac alert rather than the decryption_failed alert to protect against CBC attacks.
     - IANA registries are defined for protocol parameters.
     - Premature closes no longer cause a session to be non-resumable.

---

{!inpage-ads.md!}

---

* TLS 1.2 Based on TLS 1.1, TLS 1.2 contains improved flexibility. The major differences include:

     - The MD5/SHA-1 combination in the pseudorandom function (PRF) was replaced with cipher-suite-specified PRFs.
     - The MD5/SHA-1 combination in the digitally-signed element was replaced with a single hash. Signed elements include a field explicitly specifying the hash algorithm used.
     - There was substantial cleanup to the client's and server's ability to specify which hash and signature algorithms they will accept.
     - Addition of support for authenticated encryption with additional data modes.
     - TLS Extensions definition and AES Cipher Suites were merged in.
     - Tighter checking of EncryptedPreMasterSecret version numbers.
     - Many of the requirements were tightened.
     - Verify_data length depends on the cipher suite.
     - Description of Bleichenbacher/Dlima attack defenses cleaned up.


---

<br>

 {!inpage-ads.md!}

---
<br>
{!footer.md!}
