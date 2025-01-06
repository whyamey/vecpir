# Vectorized Batch Private Information Retrieval

This repository contains minimal edits of the Vectorized Batch PIR to get it to compile without needing to globally install SEAL and to get it to compile on Linux with gcc. Minimal and only necessary edits are made so that it could be compared with FrodoPIR for our paper. My edits are licensed under the original license since it's a bother to switch to GPL for a few lines of code. 

The original paper detailing the protocol can be found [here](https://ia.cr/2022/1262). Many thanks to the authors for making this code public. 

## ⚠️ Important Warning

This implementation is intended for research purposes only. The code has NOT been vetted by security experts. Therefore, no part of this code should be used in any real-world or production setting.

# Compilation

```bash
# Clone your repository with submodules
git clone --recursive [your-repo-url]
cd vecpir

# Build everything
mkdir build
cd build
cmake ..
make
```

## Contributors
 - [Muhammad Haris Mughees(Lead)](https://mhmughees.github.io)
 - [Ling Ren](https://sites.google.com/view/renling)

*Acknowledgment: Sun I (is16@illinois.edu) for helping with testing the code*

