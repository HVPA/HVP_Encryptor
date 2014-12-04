Prerequisite:
- Python 2.6+
- PyCrypto

HVP_Encryption:
This python script is used for encrypting/decrypting files as well as generating private and public keys for
both sender and reciever to encrypt and decrypt data.

Usage:
To see a list of command run "python HVP_Encryption -h" for more info.

    Encrypt:
    To encrypt run with "-e" param followed by the public key, private key, input and output file paths params. 
        
        params:
        --public public key of the recipent
        --private private key of the sender
        --input file path to be encrypted
        --output directory path to output encrypted file
        e.g: "python HVP_Encryption -e --public pub.public --private prv.private --input /files/input --output /files/output"

    Decrypt:
    To decrypt run with "-d" param followed by the public key, private key, input and output file paths params.

        params:
        --public public key of the sender
        --private key of the reciepent
        --input file path of the encrypted files to be decrypted
        --output directory path to output decrypted file
        e.g: "python HVP_Encryption -d --public pub.public --private prv.private --input /files/input --output /files/output"
    
    Create public and private keys:
    To generate a set of public and private keys run with "-c" param followed by a keyname.
        
        params:
        --keyname=<my_keyname> name for the keys to be generated
        e.g: "python HVP_Encryption -c keyname=my_keyname"
    
Py2exe:
To create the executable for the HVP_Encyption run the setup.py

eg: python setup.py p2exe

This will create dist folder with the "HVP_Encryption.exe" executable.