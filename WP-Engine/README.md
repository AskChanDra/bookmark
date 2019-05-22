#WP Engine

###### SSH Key Generation

```bash
$ ssh-keygen -t rsa -b 4096 -C "email@example.com"
```

- Copy 

- Copy the `rsa.pub` and paste in the WPEngine `GIT Push` section 

- Testing SSH connection

```bash
ssh git@git.wpengine.com info
```

- Add files & make changes and commit repo

- Add remote 

```bash
git remote add production git@git.wpengine.com:production/prod-env-name.git
git remote add staging git@git.wpengine.com:production/stage-env-name.git
git remote add development git@git.wpengine.com:production/dev-env-name.git
```

- To conifrm remotes successfully added

```bash
git remote -v
```


###### 
