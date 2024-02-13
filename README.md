# tracknet_cpp_inference
## Libtorch
Get libtorch from https://pytorch.org/get-started/locally/ and unzip it into ```include``` directory.
```bash
wget https://download.pytorch.org/libtorch/cu118/libtorch-cxx11-abi-shared-with-deps-2.2.0%2Bcu118.zip
unzip libtorch-cxx11-abi-shared-with-deps-2.2.0%2Bcu118.zip
```

## Test data
To get test data:
```bash
python spdsim_v3.py 1000
```
Will generate the output.tsv file with 1000 events.

## Create docker
```bash
docker-compose up -d
```
Connect to terminal:
```bash
docker-compose exec app bash
```

## Build with cmake
```bash
cmake -S . -B build
cmake --build build
```
Then execute:
 ```bash
 ./main file.tsv n_events
 ```
