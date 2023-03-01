Username and password authentication is based only on what the user knows (the password), but certificate-based client authentication also leverages what the user has (the private key), which cannot be phished, guessed or socially engineered.

## Client config ->

Generation key client:
````bash
 foo@bar:~$ ssh-keygen -t ed25519 -f ~/.ssh/[filename] -C "[Useful Comment]"
````

> -t is the algorym criptografic used
> -f is the file directory where the id will be saved
> -C is the tag name for the key that describe what is the server that you going to connect


Now you need to send the identity to the server and enter the passwod only for this step. It indicates to the server 
````bash
 foo@bar:~$ ssh-copy-id root@192.168.1.2
````

## Server config ->

