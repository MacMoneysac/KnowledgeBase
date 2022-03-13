# Git Multiple Accounts

All you need to do is configure your SSH setup with multiple SSH keypairs.

- This link is easy to follow (Thanks Eric):
<http://code.tutsplus.com/tutorials/quick-tip-how-to-work-with-github-and-multiple-accounts--net-22574>

- Generating SSH keys (Win/msysgit)
<https://help.github.com/articles/generating-an-ssh-key/>

**Relevant steps from the first link:**

1. Generate an SSH-key `ssh-keygen -t rsa -C "john@doe.com"`, follow the prompts and decide a name, e.g. `id_rsa_doe_company`.
2. Copy the SSH public-key to GitHub from `~/.ssh/id_rsa_doe_company.pub` and tell ssh about the key: `ssh-add ~/.ssh/id_rsa_doe_company`.
3. Create a `config` file in `~/.ssh` with the following contents:

```text
Host github-doe-company
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_doe_company
```

4. Add your remote `git remote add origin git@github-doe-company:username/repo.git` or change using `git remote set-url origin git@github-doe-company:username/repo.git` and finally `git push --set-upstream origin main`

----------

Also, if you're working with multiple repositories using different personas, you need to make sure that your individual repositories have the user settings overridden accordingly:

Setting user name, email and GitHub token – Overriding settings for individual repos
<https://help.github.com/articles/setting-your-commit-email-address-in-git/>

Hope this helps.

**Note:**
Some of you may require different emails to be used for different repositories, from git **2.13** you can set the email on a directory basis by editing the global config file found at: `~/.gitconfig` using conditionals like so:

```text
    [user]
        name = Pavan Kataria
        email = defaultemail@gmail.com
    
    [includeIf "gitdir:~/work/"]
        path = ~/work/.gitconfig
 ```

And then your work specific config ~/work/.gitconfig would look like this:

```text
    [user]
        email = pavan.kataria@company.tld

Thank you @alexg for informing me of this in the comments. 

  [1]: <http://ufz.github.com/help/multiple-ssh-keys/>
```
