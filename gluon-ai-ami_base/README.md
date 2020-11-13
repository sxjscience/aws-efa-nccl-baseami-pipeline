# Gluon AI AMI

The script to create the Gluon AI Base AMI.

```
packer build gluonai-gpu-base-ubuntu1804.yml
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

To activate the environment
```
source ~/env/nlp-1.0/bin/activate
````

```
- mxnet (2.0 version)
- pytorch-1.7
- deepspeed
- tensorflow (2.0 version)
- jupyter lab
- sagemaker-training
- gluonnlp-1.0
- tvm
```
