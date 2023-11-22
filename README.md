# SGX-enclaves

Implementation of SGX enclaves for simple protocol. Enclave A will create challenges, i.e. a pair of Integers, and send them to enclave B. Enclave B will add the Integers and send the result back to enclave A. Enclave A verifies and outputs whether the result is correct.  

## How to run

From terminal, go to Enclave_B directory and issue the following commands:

```bash
make clean
make SGX_MODE=SIM
./app
```

open another terminal window, go to Enclave_A directory and issue the following commands:

```bash
make clean
make SGX_MODE=SIM
./app
```

Notice that socket communication is used on arbitrarily chosen port 8080. If such port is not available, simply change it on both Enclave_A and Enclave_B app files.
