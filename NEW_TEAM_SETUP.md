# New Team Setup

This example will setup team foo after the pass-foo repo has been created on
Github or a private git server.

### Modify shell

````
alias pass-foo='PASSWORD_STORE_DIR=~/.password-store-foo pass'
```

### Initialize the store and the repo

```
$ pass-foo init akosmin@sailthru.com
mkdir: created directory '/home/akosmin/.password-store-foo/'
Password store initialized for akosmin@sailthru.com

$ pass-foo git init
Initialized empty Git repository in /home/akosmin/.password-store-foo/.git/
[master (root-commit) e19bae1] Add current contents of password store.

$ pass-foo git remote add origin ...
```
### Add a password to the team's password store

```
  $ pass-foo insert bar
  Enter password for bar:
  Retype password for bar:
  [master d337478] Add given password for bar to store.
  1 file changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 bar.gpg

  $ pass-foo
  Password Store
  └── bar

  $ pass-foo git push -u --all
```
