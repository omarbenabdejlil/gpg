# gpg

> steps to crypt a file : 
```bash
gpg --full-generate-key 
```
> Encrypt the file , in my exemple my file named by `omar.txt`
```bash
gpg --encrypt --sign --armor -r 802.killer@gmail.com omar.txt 
```

> Decryption de fichier `omar.txt.asc` :

```bash
gpg --decrypt omar.txt.asc > omar_new.txt
```
  
