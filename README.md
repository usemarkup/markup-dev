Installer for the Markup Laptops (mostly aimed at running VMs)

### Installs

- Brew (for Ruby/PHP etc)
- Ruby >= 2.4
- PHP 7.1
- Bundler (To install gems)
- Vagrant (to aid running virtual machines)

Will check and instruct you on what to do to get VirtualBox installed but will not actually do it due to some restrictions in what Brew can do.

### How to use

```
curl https://raw.githubusercontent.com/usemarkup/markup-dev/master/init.sh | bash
```

While the script is running, you should setup you Github SSH keys so you can clone the private repos later. These clone functions generally use ssh-style git clones.

To do this:

1. Open a terminal and run `ssh-keygen`. The location and name you provide to your generated key doesn't matter.
2. Add the key to your keychain using `ssh-add` then whatever path you saved the private key to. For example `ssh-add ~/.ssh/id_rsa`
3. Open https://github.com/settings/keys and click "New Key". Give your key a name.
4. `cat` the public key and copy/paste it into the "Key" box.

Now, when you run any init scripts for the product virtual environments, private repos should be cloned properly.
