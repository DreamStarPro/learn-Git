GPG keys help you to get your contribution be verified and that build trust among collaborators.

**Step 1:** Open Git Bash

**Step 2:** Type 
$ gpg --gen-key

Next, select default settings or of your choice and hit enter to generate the GPG Key.

[ Recommended choice : Kind of Key - RSA and RSA, Key Size - 4096, Key Expiry: None, and Passphrase: Empty ]

After successful creation of GPG Key,

**Step 3:** Type 
$ gpg --list-secret-keys --keyid-format LONG

Copy the GPG Key ID from the shown details at 'sec' line after '/'.

**Step 4:** Now, type
$ gpg --armor --export (copied key id)

[ Remove brackets around above command while executing. ]

Now, copy the ASCII format shown beginning with -----BEGIN PGP PUBLIC KEY BLOCK----- and 

ending with -----END PGP PUBLIC KEY BLOCK-----.

**Step 5:** Add the copied text to [GPG Keys settings](https://github.com/settings/keys) in your Github account.

**Step 6:** Finally, say to Git about this GPG Key that you want to use in further commits.

Type
$ git config --global user.signingkey (copied key id)


After following these steps successfully, you could see verified sign for your future commits.



Refernce: [Signing commits with GPG](https://help.github.com/articles/signing-commits-with-gpg/)
