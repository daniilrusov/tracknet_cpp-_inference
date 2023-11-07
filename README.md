# tracknet_cpp_inference
## Libtorch
Get libtorch from https://pytorch.org/get-started/locally/
```bash
wget https://download.pytorch.org/libtorch/cpu/libtorch-shared-with-deps-2.1.0%2Bcpu.zip
unzip libtorch-shared-with-deps-2.1.0+cpu.zip
```

## Test data
To get test data:
```bash
python spdsim_v3.py 1000
```
Will generate the output.tsv file with 1000 events.

## Build with cmake
```bash
mkdir build
cd build
cmake -DCMAKE_PREFIX_PATH=/path/to/libtorch/ ..
cmake --build . --config Release
```
