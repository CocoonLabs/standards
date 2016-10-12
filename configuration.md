## Configuration

This document describes how we configuration applications and modules.

Our standards were inspired by [https:\/\/12factor.net\/config](https://12factor.net/config)

### Environment Variables

Applications must pick configuration from the runtime's environment variables and not on static files.

```bash
$ cd project
CONFIG_VAR=CONFIG_VAL HOST=0.0.0.0 PORT=80 ./bin/server
```

No named environments..

```bash
$ ls project/configs/
production.yml development.yml staging.yml
```

So no dirty states

```bash
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

         modified: configs/production.yml
         modified: configs/thisenvironment.yml


no changes added to commit (use "git add" and/or "git commit -a")
```

