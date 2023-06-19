### Testing

Note 1: Github has one key, and this key is shared for every commit done on their website.

Note 2: Forking is required for random accounts to add things to GitHub accounts which blocks super obvious attacks that way, but if given write abilites or sneaking into a large github, could potentially slip by.

Note 3: Git can automatically assign someone's username and email. 
This can result in someone having a key, and it being them but still be unverified.

Note 4: Only the email matters when pushing a commit from a local machine. 
And github will not register any changes to just the username.

Note 5: With write access, direct manipulation is perfectly fine. 
So, this could allow attackers to infiltrate a group by doing minor fixes, and then to scramble the code(to cause delays) or inject negative code as an attack. 
Scrambling code can be rolled back, but delayed time negative code could be inserted amongst innocous commits and executed at a later date without it being easy to rollback.

Note 6: Minor vulnerability with that someone could steal a computer and launch commits from there, likewise, as long as they can clone the branch, the may not need to even be a real user to make actual changes (More of a github vulnerability).

Note 7: As long as the key is known on a computer and associated with an account, you can make commits in that account's name. 
So, leave your computer open at work, then someone can make a commit in your name to cause potential damage.
Possibly could occur on the same network if your private key is known or shared.
Sidenote: This makes sharing keys very bad since if they know your Github Email and key, then they can do anything and have it be verified which makes key generation and management very important.

Note 8: I just changed the email to my test user Dwight Eisenhower. 
So, this commit will now be in Dwight's name. 
However, it is currently unverified since the email doesn't match, but the key is shared between accounts.

Note 9: You have to add the ID to the key otherwise, it is unverified. 
This is however, trivially easy once known, and can be done in roughly less than a minute. 
Must add the ID before putting the key in your profile. 
But, when you do that, even previously unverified commits will become verified which seems a bit dangerous.

Note 10: Cannot add additional emails to your profile on Github. 
However, this can be circumvented by the shared key, however, there are notable issues with adding an id. 
Once you do, then every single commit seems to be done from the new ID regardless of whose credentials are used in the push. So, it seems very inconsistent.

Note 11: Notably, there is a passphrase, but when it comes out is incredibly inconsistent along with the fact that the default is no passphrase at all. 
Notably, passphrase in a shared key is shared which further incentivises no pass phrase to be used.

Note 12: A shared crackable key could cause the entire verification for a project to be eliminated. 
Also, a shared key needs only to change the primary user to impersonate that user effectively making the verification pointless within any large enough group.
Possible to use multiple master keys or subkeys to reduce this threat.
Should be noted that very few online resources actually cover subkeys and their benefits, but plenty cover how to generate master keys and use those for signing.

Note 13: Keys are not easily transportable. 
Keys are stuck to the computer that they are on, and to set up on another computer is difficult.
Items like Yubikey can be used to transport keys and subkeys around, but that now means that keys could be physically stolen or physically lost which depending on the person, may make the system less secure.
(Possible good question to see if they use YubiKey)

Note 14: SSH keys can be cracked as long as a hacker knows who they're targeting and can get access to the computer hosting the ssh password, and they don't have expiration dates which could cause significant headaches in the future.
Sidenote: SSH keys require later versions of GIT to even use which makes them have a limited rollout compared to GPG keys.
Sidenote 2: The official Gitgub website has the SSH key's algorithim be ED25519 which is an excellent choice. 
However, a user can still designate whatever algorithim they want allowing for users to use cracked or unsafe algorthims.

Note 15: S/MIME also utilizes certificates for verification which means that the downsides from CA's who don't do their homework can cause issues.
It also requires working closely with a third party and likely cause increased expenses along with the fact that certificates expire which may make older code appear less safe even if it is perfectly safe.

Note 16: PGP Key Signatures can be found for any repo that you have write access to. 
Private repos require your git access token though which is seperate from the signing key. 
The GPG public keys can be found using simple Javascript for anyone profile, but they require the Git Access Token.

If you delete a key, it becomes unverified. Which means that verification really only works as long as that key is there, and it would be a shame if it say expired like with S/MIME or was cracked like with RSA 1024.
Can resign with another kye after the fact in the case of it being compromised, but it is a time-consuming process which would take a while depending on the repository.

So, we are now trying to see if it will actually commit as comalle again, and it seems to only allow you to use the last person to be added.

Also, worth noting that the low end for Encryption is RSA 1024 from GPG which has been cracked previously. 
It defaults to 2048, and defaults to infinite key, and it defaults to having no passphrase which makes it entirely possible to have a (theoretically) crackable key with permanent access to everything you have by just following the defaults of GPG. 
Also means since GPG signing has been available for a bit, that there could be legacy keys that are crackable and able to be used for false verification.
Passphrases are also potentially susceptible to random guessing attacks if they are even made by the user. 
