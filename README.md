# CryptoFinal

a python script to encrypt all files, including mpeg files, in a directory with a public rsa key.

Generate a rsa key pair

python encryptdir.py gen-keys

Create your input folder if not exists

mkdir input

Encrypting

python encryptdir.py encrypt

After, all files in input will be encrypted into output

Decrypting

python encryptdir.py decrypt -in ./folder-with-encrypted-files/ -out ./target-folder/

Test encryption and decryption You can also test encryption and decryption.

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
