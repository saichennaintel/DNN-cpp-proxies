# deep-nn-proxy
C++/MPI proxies for distributed training of deep neural networks, including `ResNet-50`, `BERT-large`, and `GPT2-large`. Other models (e.g., `GPT-3`) will be added. These proxies cover `data parallelism`, `pipeline parallelism`, and a `hybrid of pipeline and data parallelism`.

## Demo
Compile:

`mpicxx gpt2_large.cpp -o gpt2`

Run:

`mpirun -n 32 ./gpt2`

Setup the number of Transformer layers and the number of pipeline stages:

`mpirun -n 32 ./gpt2 64 8`
