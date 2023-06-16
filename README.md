# Testing

Note 1: Github has one key, and this key is shared for every commit done on their website.

Note 2: Forking is required for random accounts to add things to GitHub accounts which blocks super obvious attacks that way, but if given write abilites or sneaking into a large github, could potentially slip by.

Note 3: Git can automatically assign someone's username and email. This can result in someone having a key, and it being them but still be unverified.

Note 4: Only the email matters when pushing a commit from a local machine. And github will not register any changes to just the username.

Note 5: With write access, direct manipulation is perfectly fine. So, this could allow attackers to infiltrate a group by doing minor fixes, and then to scramble the code(to cause delays) or inject negative code as an attack. Scrambling code can be rolled back, but delayed time negative code could be inserted amongst innocous commits and execute at a later date without it being easy to rollback.

Note 6: Minor vulnerability with that someone could steal a computer and launch commits from there, likewise, as long as they can clone the branch, the may not need to even be a real user to make actual changes (More of a github vulnerability).

Note 7: As long as the key is known on a computer and associated with an account, you can make commits in that account's name. So, leave your computer open at work, then someone can make a commit in your name to cause potential damage. Possibly could occur on the same network if your private key is known or shared.
Sidenote: This makes sharing keys very bad since if they know your Github Email and key, then they can do anything and have it be verified which makes key generation and management very important.

Note 8: I just changed the email to my test user Dwight Eisenhower. So, this commit will now be in Dwight's name. However, it is currently unverified since the email doesn't match. However, the key is shared between accounts.

Note 9: You have to add the ID to the key otherwise, it is unverified. This is however, trivially easy once known, and can be done in roughly less than a minute.
