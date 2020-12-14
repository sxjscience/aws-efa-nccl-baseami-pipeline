# Gluon AI AMI

The script to create the Gluon AI Base AMI.

```
packer build gluonai-gpu-base-ubuntu1804.yml
```

## Created AMI

```
Name: gluon-ai-gpu-base-ubuntu1804-1607484836
AMI ID: ami-0b98938e6bdaa1e48
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

#### Example 1: SQuAD 2.0 Finetuning with ALBERT-base

```
source ~/env/nlp/bin/activate
cd gluon-nlp/scripts/question_answering/
bash commands/run_squad2_albert_base.sh 1 2.0 float16
```

This should give you a model with best F1/best EM = 82.44%/79.65%.


#### Example 2: Running Jupyter Lab Development Environment

```
source ~/env/nlp/bin/activate
jupyter lab
```
