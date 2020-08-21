# Git Notes

## Github

### Setting up SSH Keys

1. Generate ssh key: 
    
    `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

2. Create ssh config: 
    
    `touch ~/.ssh/config`

3. Add config to store passphrases:

    ```bash
    Host *
    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ~/.ssh/id_rsa
    ```

4. Add ssh key to ssh-agent: 
    
    `ssh-add -K ~/.ssh/id_rsa`

#### Source

https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh