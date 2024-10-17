### [S-#] Storing the password on-chain makes it visable to anyone, and no longer private


**Description:** All data stored on-chainis visible to anyone, and can be read directly from the blockchain. The `PasswordStore::s_password` variable is intended to be a private variable  and only accessed through the `PasswordStore::getPassword` function, which is intended to be only called by the owner of the contract.

We show one such method of reading any data off chain below.

**Impact:** Anyone can read the private password, severly breaking the functionality of the protocol.

**Proof of Concept:** (Proof of Code)

The below test case shows the anyone can read the 

**Recommended Mitigation:**