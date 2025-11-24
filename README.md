# alga-comments
Project to group all others alga-comments projects

## Commands used in this project

Creating a ssh key to add in github.
```
ssh-keygen -t ed25519 -C "your email address"
```

You can see your key with:
```
ls -al ~/.ssh
```

With your generate key go to https://github.com and copy and past your id_ed25519.pub value to new SSH Key configuration.
This configuration will enable you to pull requests to github via ssh command in terminal.

### Cloning projects

Before using the commands below, create this projects on github site: alga-comments, alga-comment-service and alga-moderation-service.

```
git clone git@github.com:klebersouza87/alga-comments.git alga-comments
cd alga-comments
mkdir microservices
git submodule add https://github.com/klebersouza87/alga-comments-service.git microservices/alga-comment
git submodule add https://github.com/klebersouza87/alga-moderation-service.git microservices/moderation-service
git status
git commit -m "New modules added"
git push
```

### Additional commands

If you want to update all submodules you can use this command.
```
git pull --recurse-submodules
```

You can clone all submodules with this command:
```
git clone --recurse-submodules -j8 git@github.com:klebersouza87/alga-comments.git alga-comments
```