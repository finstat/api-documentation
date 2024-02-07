``` python
import hashlib

def calculateHash(publicKey, privateKey, value):
    hashString = 'SomeSalt+' + publicKey + '+' + privateKey + '++' + value + '+ended'
    sha = hashlib.sha256()
    sha.update(str(hashString).encode())
    return sha.hexdigest();
```