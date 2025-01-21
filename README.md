# ollvm-project-android
ollvm project base on llvm-android of google

> [!WARNING]  
> This project does **NOT**  contain all the original files.  
> Considering that the original project is too large, it only contains the code that needs to be modified or added.

# Build instructions
See [here](https://android.googlesource.com/toolchain/llvm_android/+/main/BUILD.md)

# Example build commands
- Using WSL(Ubuntu22+) in Windows11 system

- Install require packages
  ```shell
  apt install repo make yacc cmake bison python-is-python3 -y
  ```
- Init the llvm repo
  ```shell
  mkdir llvm-toolchain && cd llvm-toolchain
  repo init -u https://android.googlesource.com/platform/manifest -b llvm-toolchain
  repo sync -c
  ```
- Modify the llvm source code. For example, add obfuscation

- Build the llvm
  ```shell
  # Full build
  # python toolchain/llvm_android/build.py --skip-tests
 
  # Build for windows only
  python toolchain/llvm_android/build.py --skip-tests --no-build linux
 
  # Build for linux only
  # python toolchain/llvm_android/build.py --skip-tests --no-build windows
  ```


> If you want to build the NDK specified LLVM version  
> See [instructions-to-rebuild-a-particular-toolchain-release](https://android.googlesource.com/toolchain/llvm_android/+/main/BUILD.md#instructions-to-rebuild-a-particular-toolchain-release)

# Credits
[LLVM](https://github.com/llvm/llvm-project)

[llvm_android](https://android.googlesource.com/toolchain/llvm_android)

[DreamSoule-ollvm17](https://github.com/DreamSoule/ollvm17)

[CYRUS-STUDIO-LLVM](https://github.com/CYRUS-STUDIO/LLVM)
