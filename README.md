# Vectorized Batch Private Information Retrieval

This repository contains an implementation of the Vectorized Batch Private Information Retrieval (PIR) Protocol published in IEEE Security and Privacy, 2023. The protocol introduces a novel approach where both communication and computation are amortized over a batch of entries, resulting in significantly lower communication overhead for small entry sizes (ranging from 32 bytes to 256 bytes). Specifically, for a batch of 256 entries and an entry size of 32 bytes, the communication overhead is 11 times less compared to previous schemes.

The paper detailing the protocol can be found [here](https://ia.cr/2022/1262).
# Compilation for my edits

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

## ⚠️ Important Warning

This implementation is intended for research purposes only. The code has NOT been vetted by security experts. Therefore, no part of this code should be used in any real-world or production setting.
