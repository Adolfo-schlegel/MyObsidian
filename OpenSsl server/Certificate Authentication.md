Username and password authentication is based only on what the user knows (the password), but certificate-based client authentication also leverages what the user has (the private key), which cannot be phished, guessed or socially engineered.

Generation key client:
````bash
 foo@bar:~$ ssh-keygen
````

You can see the generated key in /.ssh directory

Now you need send the identity to the server;