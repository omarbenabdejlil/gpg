# GPG Tuto :

![gpg](https://wiki.trezor.io/images/Gnupg_logo.svg.png)

> steps to crypt a file : 
```bash
gpg --full-generate-key 
```
![exemple](https://i.ibb.co/ZWCCtw1/full-gen.png)
> Encrypt the file , in my exemple my file named by `omar.txt` so i got `omar.txt.asc`
```bash
gpg --encrypt --sign --armor -r 802.killer@gmail.com omar.txt 
```
![exemple](https://i.ibb.co/x5cMFv1/asc-file.png)

> Decryption of file ==> `omar.txt.asc` :

```bash
gpg --decrypt omar.txt.asc > omar_new.txt
```
>  checking the fingerprint : 
```bash
gpg --fingerprint mary-geek@protonmail.com
```

> Share Your Public Key : 
```bash
gpg --output ~/omar.key --armor --export 802.killer@gmail.com
```

<hr>

## SCP exemple that you need ! 
> Copy __file__ from __local host__ to a __remote host__ SCP example :
```bash
scp fichier.txt.asc username@IP:/remote/directory/
```
> Copy __directory__ from a __remote host__ to __local host__ SCP example :
```bash
scp -r username@from_host:/remote/directory/  /local/directory/
```
