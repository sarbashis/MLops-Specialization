# MLops-Specialization
## Week 1
### Introduction to Model Serving
What is Serving a Model?

Provide user to access the model and interact with it.

- Model Traininig
- Model Prediction


Important Metrics to optimized:

- Latency:
    - Delay between the user's action and response of application to user's action.
    
    - Latency of the whole process, starting from the sending data to server, performaing inference and returning the result
    
    - Minimal latency is a key requirement to maintain customer statisfaction

- Throughput: 
    - Number of successfull requests sever per unit time

- Cost:
    - The cost associated with each inference should be minimised
        - Infrastructure
            - CPU
            - Harware Accelerators
            - Caching infrastructure for faster data retrieval


- Balance Cost, Latency and Throughput
  
Cost increases wit scalling of infrastructure. 
To reduce the latency and increase highthroughput the following approch can be applied.
 - Reduce costs by GPU Sharing
 - Multi-model serving
 - Optimizing models used for inference. 


### Introduction to Model Serving Infrastructure
While serving a model we need to look into the two following metrics
- Model's optimizing metric:
    - Accuracy
    - precision
    - Recall

- Satisficing (Gating) metric:
    - latency
    - Model Size
    - GPU Load

    
`Note: GPU is good for parallel throughput while TPUs for complex models and large batches`

NoSQL databases for Caching and Feature Lookup

Example:
    - Google Cloud Memorystore (Redis based): In memory cache

    - Google Cloud FireStore : Scalable, can handle slowly changing data

    - Goolge cloud BigTable: Scalable, can handle dynamically changing data

    - Amazon DynamoDB: single digit milisecond read latency

### Deployment Options

#### Constrained Environment: Mobile Phone
Prediction Latency is Almost Always Important
- Opt for on-device inference whenever possible
    This will enhances user experience by reducing the response time of your app.

#### Improving PRediction Latency and Reducing Resource Costs

Clipper open source tool for model serving

### Installing Tensorflow Serving

- tensorflow-model-server: 
    - Fully optimize server
    -  May not work on older machines

- tensorflow-model-server-universal
    - basic optimization 
    - Work on most of the machines

---    
## Week 2
---
### Model Serving Architecture
ML Infrastructure for Model Serving
    
- On Prem
    - TF-Serving, KF-Serving, NVIDIA and more
- On Cloud
    - Create VMs and use open source pre-built servers
    - Use the provided ML workflow

Example of Model Servers
 - Tensorflow Serving
 - KF Serving
 - PyTorch
 - Triton Inference Server

 ### Tensorflow Serving Acheticture
 - Provide both batch and Real-time Inference
 - Multi-Model Serving
 - Exposes REST or gRCP protocol
 

----
## Week 3
----

### Scaling infrastructure

Scaling Approches:
- Horizontal Scaling:
    - More CPU/GPUs instead of bigger one
    - Benefit of elasticity
    - Application never goes offline
    - No Limit hardware capacity

- Vertical Scaling
    - Increase Hardware resources


Virtual Machine(VM) is running on the top of the operating system. Hypervisor act as manager of the VMs. However VM is not an optimized solution as each VM requires operating system.

Containers are better than VMs. Here are the advantages of it
- Less OS requirement -- more apps
- Abstraction
- Easy deployment based on container run time

Container orchestration: Manages life cycle of the containers in production environment

Two most popular Container orchestration tools are: (a) __Kubernetes__ and (b) __docker Swam__


ML Workflows on Kubernetes -- KubeFlow
- Dedicated to make deployments of machine learning (ML) workflows on kubernetes simple, portable and scalable
- Anywhere you are running kuberntes, you should able to run KubeFlow
- Can be run on premise or on Kubernetes engine on cloud offering AWS, GCP, Azure etc.


 Video Ref: Microservices to Kubernetes
 
 https://www.youtube.com/watch?v=H06qrNmGqyE

