# Prerequisites

Install solo-python usually with pip3 install solo-python.

## Obtain source code and solo tool
Source code can be downloaded from:

[github repository](https://github.com/solokeys/solo1)

Use: `git clone --recurse-submodules https://github.com/solokeys/solo`

## solo tool can be downloaded from:

from python programs repository: `pip install solo-python`

from installing prerequisites: `pip3 install -r tools/requirements.txt`
github repository: repository
installation python enviroment with command make venv from root directory of source code

## To build locally

`rustup target add thumbv7em-none-eabihf`

```
cd targets/stm32l432
make cbor
make build-hacker
cd ../..

make venv
source venv/bin/activate
solo1 program aux enter-bootloader
solo1 program bootloader targets/stm32l432/solo.hex
```

