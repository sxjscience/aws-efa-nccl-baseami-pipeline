# Gluon AI AMI

The script to create the Gluon AI Base AMI.

It contains three layers.

### Primitive Layer
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
### Application Layer
- MXNet 
- PyTorch 
- TensorFlow
- Conda
- Jupyter Lab
- SageMaker support
### Gluon Toolkits
- gluon-nlp
- gluon-cv
- gluon-ts
- autogluon
- dgl
