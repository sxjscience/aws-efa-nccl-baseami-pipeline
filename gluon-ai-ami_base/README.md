# Gluon AI AMI

The script to create the Gluon AI Base AMI.

```
packer build gluonai-gpu-base-ubuntu1804.yml
```

## Created AMI

```
Name: gluon-ai-gpu-base-ubuntu1804-1605304760
AMI ID: ami-0bdad81e64a1086f0
```

## Primitive Layer
This contains the basic dependencies.

- NVIDIA Driver 450.xx
- CUDA 11
- NVIDIA Fabric Manager
- cuDNN 8
- NCCL 2.7.8
- EFA latest driver
- AWS-OFI-NCCL 
- FSx kernel and client driver and utilities
- Intel OneDNN
- NVIDIA runtime Docker

## Environments

### NLP

Install the packages that are suitable for NLP + Graph development.

To activate the environment
```
source ~/env/nlp/bin/activate
````

```
- mxnet (2.0 version)
- pytorch-1.7
- deepspeed
- tensorflow (2.0 version)
- tensorboard
- Jupyter Lab
- sagemaker-training
- dmlc/gluonnlp (master version)
- dmlc/dgl (master version)
- apache/tvm (master version)
- jax
- cupy
- matplotlib
```
