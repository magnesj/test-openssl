# Standalone project used to produce OpenSSL dynamic libraries

This project can be used to produce the `OpenSSL`  dynamic libraries `libcrypto.so` and `libssl.so`

    cmake . --preset=ninja
    cd build
    ninja


# vcpkg as submodule in a project

If vcpkg is a submodule in your project, the following command can be used to produce the dynamic libraries, the only requirement is a `vcpkg.json` in a separate folder containing the dependency on `openssl`.

Content of `mySubFolder/vcpkg.json`

    {
      "dependencies": [
        "openssl"
      ]
    }

 `vcpkg install --triplet x64-linux-dynamic --x-manifest-root=../mySubFolder --x-install-root=./vcpkg_installed`
