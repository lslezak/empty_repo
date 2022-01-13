## Empty Repository

This is just an empty RPM package repository, it does not provide any packages.

But the important detail is that this repository is signed by the official
SUSE GPG signing keys. So if you add it in the SUSE/openSUSE products
you will not see any GPG signature problems.

That might be useful for testing, if you want to test that adding and using
a repository works fine.

An empty repository has these advantages:

- It is compatible with any product in any version
- It cannot create unwanted package conflicts or install any packages accidentally
- It is secure :smile:

You can create an empty repository also this way:

```shell
mkdir empty_repo
createrepo_yum empty_repo
```

But the generated repository will be unsigned and the package manager will
complain when adding such a repository.


## Usage

The repository URL is https://raw.githubusercontent.com/lslezak/empty_repo/main.

You can use it in YaST or in zypper:

```shell
zypper addrepo https://raw.githubusercontent.com/lslezak/empty_repo/main empty_repo
```

## Notes

This was created as a snapshot of https://updates.suse.com/SUSE/Updates/SLE-INSTALLER/15-SP4/x86_64/update
at the time when it was empty.
