# Distributed AI Inference System Meta
This system operates in a distributed environment using Nvidia Triton.

## 1. Introduction
This system operates in a distributed environment using Triton.   
Computers with triton-server and triton-agent installed become AI inference servers, referred to as nodes.   
When an external user sends an inference request to triton-gateway-client via triton-server-frontend, the request is routed to a node by triton-scheduler.   
As a result, the AI inference results are received by triton-server-frontend.   

We have resolved the scale-out issues of Triton.   
By using Triton, various AI models can be utilized.   

*Note: This project is no longer receiving updates.*   
*I have been tasked with implementing this technology's ideas as part of my work with a company. Therefore, we will no longer release updated source code.*   

## 2. Repository Structure
|Repository|Description|URL|
|:---|:---|:---|
|trition-server-frontend|This is an example of a frontend utilizing the distributed-ai-inference-server.|[link](https://github.com/ahr-i/triton-server-frontend)|
|trition-gateway-client|It serves as a gateway that receives user requests, acts as an intermediary between the scheduler and nodes, and provides inference results to the user.|[link](https://github.com/ahr-i/triton-gateway-client)|
|trition-agent|The manager controls nodes with triton-server installed, connecting to the distributed-ai-inference-system in a distributed environment to handle user requests.|[link](https://github.com/ahr-i/triton-agent)|
|trition-server|It is responsible for AI inference, connecting to triton-agent to perform inference requests efficiently.|[link](https://github.com/ahr-i/triton-server)|
|trition-scheduler|Based on user requests, it selects the most suitable node among those with triton-agent installed. *Unfortunately, this code is not publicly available.*|X|
|trition-gateway-provider|The gateway includes functionality for providers to deploy models. *Unfortunately, this code is not publicly available.*|X|
|trition-model-store|It receives and stores models deployed by the provider, then deploys them to triton-agent. *Unfortunately, this code is not publicly available.*|X|