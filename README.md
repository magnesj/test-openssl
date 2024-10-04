This project can be used to produce the `OpenSSL`  dynamic libraries `libcrypto.so` and `libssl.so`

If vcpkg is a submodule in your project, the following command line options can be used to produce the dynamic libraries, the only requirement is a `vcpkg.json` in a separate folder.

 `vcpkg install --triplet x64-linux-dynamic --x-manifest-root=../ThirdParty/openssl-install-helper --x-install-root=./vcpkg_installed`
