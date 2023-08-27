# A.RA.YA
Any inappropriate issue will be closed.

# How do I get the package during the maintenance?

```python
def allb_RSA_SHA1_sign(data,pem_key):
    b64_RSA_Iuput = b2a_base64(bytes.fromhex(hashlib.sha1(data).hexdigest())).decode().replace("\n", "")
    pri_key = RSA.importKey(base64.b64decode(pem_key))
    signer = PKCS1_v1_5.new(pri_key)
    hash_obj = SHA1.new(b64_RSA_Iuput.encode())
    signature_b64 = base64.b64encode(signer.sign(hash_obj)).decode()
    
    return signature_b64
```
