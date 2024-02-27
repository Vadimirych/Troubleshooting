# Kali - crackmapexec "Error detecting the version of libcrypto"

## Problem: "Error detecting the version of libcrypto"

```
kali>crackmapexec                                                                                  
Traceback (most recent call last):
  File "/usr/bin/crackmapexec", line 8, in <module>
    sys.exit(main())
             ^^^^^^
  File "/usr/lib/python3/dist-packages/cme/crackmapexec.py", line 117, in main
    args = gen_cli_args()
           ^^^^^^^^^^^^^^
  File "/usr/lib/python3/dist-packages/cme/cli.py", line 76, in gen_cli_args
    protocol_object = p_loader.load_protocol(protocols[protocol]['path'])
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3/dist-packages/cme/loaders/protocol_loader.py", line 15, in load_protocol
    protocol = imp.load_source('protocol', protocol_path)
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/imp.py", line 170, in load_source
    module = _exec(spec, sys.modules[name])
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 621, in _exec
  File "<frozen importlib._bootstrap_external>", line 940, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/usr/lib/python3/dist-packages/cme/protocols/rdp.py", line 11, in <module>
    from aardwolf.commons.factory import RDPConnectionFactory
  File "/usr/lib/python3/dist-packages/aardwolf/commons/factory.py", line 7, in <module>
    from asyauth.common.credentials import UniCredential
  File "/usr/lib/python3/dist-packages/asyauth/common/credentials/__init__.py", line 182, in <module>
    from asyauth.common.credentials.kerberos import KerberosCredential
  File "/usr/lib/python3/dist-packages/asyauth/common/credentials/kerberos.py", line 9, in <module>
    from minikerberos.common.creds import KerberosCredential as KCRED
  File "/usr/lib/python3/dist-packages/minikerberos/common/creds.py", line 21, in <module>
    from oscrypto.asymmetric import rsa_pkcs1v15_sign, load_private_key
  File "/usr/lib/python3/dist-packages/oscrypto/asymmetric.py", line 19, in <module>
    from ._asymmetric import _unwrap_private_key_info
  File "/usr/lib/python3/dist-packages/oscrypto/_asymmetric.py", line 27, in <module>
    from .kdf import pbkdf1, pbkdf2, pkcs12_kdf
  File "/usr/lib/python3/dist-packages/oscrypto/kdf.py", line 9, in <module>
    from .util import rand_bytes
  File "/usr/lib/python3/dist-packages/oscrypto/util.py", line 14, in <module>
    from ._openssl.util import rand_bytes
  File "/usr/lib/python3/dist-packages/oscrypto/_openssl/util.py", line 6, in <module>
    from ._libcrypto import libcrypto, libcrypto_version_info, handle_openssl_error
  File "/usr/lib/python3/dist-packages/oscrypto/_openssl/_libcrypto.py", line 9, in <module>
    from ._libcrypto_cffi import (
  File "/usr/lib/python3/dist-packages/oscrypto/_openssl/_libcrypto_cffi.py", line 44, in <module>
    raise LibraryNotFoundError('Error detecting the version of libcrypto')
oscrypto.errors.LibraryNotFoundError: Error detecting the version of libcrypto

```

## Solution
https://github.com/wbond/oscrypto/issues/78
```
kali>pip install -I git+https://github.com/wbond/oscrypto.git
```