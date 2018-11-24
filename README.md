# CryptoFinal

a python script to encrypt all files, including mpeg files, in a directory with a public rsa key.

Generate a rsa key pair

   ```
    python encryptdir.py gen-keys
    ```

Create your input folder if not exists

   ```bash
    mkdir input
    ```

Encrypting

   ```bash
    python encryptdir.py encrypt
    ```

  

After, all files in input will be encrypted into output. After encrypting, the output folder looks like:
  
  ```
    drwxr-xr-x  12 PaoloBondi  staff   384 Nov 24 15:21 .
    drwxr-xr-x@  9 PaoloBondi  staff   288 Nov 24 15:21 ..
     -rw-r--r--   1 PaoloBondi  staff  1408 Nov 24 15:21 test-0.gz.enc
    -rw-r--r--   1 PaoloBondi  staff   512 Nov 24 15:21 test-0.key.enc
    -rw-r--r--   1 PaoloBondi  staff  1408 Nov 24 15:21 test-1.gz.enc
    -rw-r--r--   1 PaoloBondi  staff   512 Nov 24 15:21 test-1.key.enc
    -rw-r--r--   1 PaoloBondi  staff  1392 Nov 24 15:21 test-2.gz.enc
    -rw-r--r--   1 PaoloBondi  staff   512 Nov 24 15:21 test-2.key.enc
    -rw-r--r--   1 PaoloBondi  staff  1376 Nov 24 15:21 test-3.gz.enc
    -rw-r--r--   1 PaoloBondi  staff   512 Nov 24 15:21 test-3.key.enc
    -rw-r--r--   1 PaoloBondi  staff  1392 Nov 24 15:21 test-4.gz.enc
    -rw-r--r--   1 PaoloBondi  staff   512 Nov 24 15:21 test-4.key.enc
  ```

Decrypting

  python encryptdir.py decrypt -in ./folder-with-encrypted-files/ -out ./target-folder/

You can also test encryption and decryption.

#mkdir input && insert some test files (optional)
python encryptdir.py test

HELP 
python encryptdir.py --help


Libraries used: 
  argparse
  hashlib
  os
  random
  re
  shutil
  subprocess

References: 
  https://www.openssl.org/docs/apps/enc.html#supported_ciphers
  stackoverflow.com
