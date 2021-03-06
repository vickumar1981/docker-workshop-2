# Workshop: Intro to Container Management using Kubernetes

## TODO

- final practice
    - review agenda (below)
    - review readme and go over presenting it and flow
        - clean up readme with deep dive section-offs 
    - review flow of exercises, do they build well on each other and do they support the right core concepts?
        - service before deployment like NP? How do exercises with 1 image adding on flow?
- beef up cli core command examples/exercises
- backup instructions
    - minikube
    - kube tutoral sandbox backup instructions
    - GCP instructions
- change image used in deployment & service to be the same. Add the service to the deployment to expose.
- change sample deployment on first step to use something very light
- Add exercise for updating app

### If time

- Use a multi-container app if it's feasible for the timeframe (show pod-to-pod communication).
- add step to deployment exercise to kill one and have it spin back up

- does this section need to be in our readme? More inf

    To start using your cluster, you need to run (as a regular user):

    mkdir -p $HOME/.kube
    sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
    sudo chown $(id -u):$(id -g) $HOME/.kube/config

## **Topics to be ready to address:**

    * Architecture of Kubernets (see Pluralsight 3 hour Nigel course)
    * Objects in API, concepts, etc in Docs
    * Docker integration
        * Docker networking expansion
            * [Container Network Model (CNM) design spec]()
        * metrics & monitoring tools (i.e. capturing resourecs used by containers)
    * Linux integratioons
    * Windows kernal integations, Kubernetes on Windows
    * Maintain cluster in EC2, EKS, GCP
    * Set up cluster from scratch
    * Managed Kuberntes vs not
        * Google Kubernetes Engine
        * EKS, AKS
    * Fargate

## Agenda

1.5 hours
Lightning talk on container orchestration
Workshop with/Kube concepts throughout

### Container Orchestration & Kubernets Lightning Talk

    - Container management outline:
        - Summary
            - Interaction with containers is inevidible
            - Abstract underlying infrastructure via an orchestrator like Kube
            - Efficiencies in container management - standardization
            - New way to deploy and manage
            - Differences in tools
        - Why Container Management?
        - Container-based Infrastructure
        - Docker Overivew
        - Deploying with containers
        - Clusters & Cloud Architecture
        - What is Container Orchestion?
        - Container management systems
        - Container management concepts
            - Within reason detail about components like pods, volumes, networking, 
        - Tools Overview
        - Into Kubernetes:
            - The Kubernetes way
                - pods, in prod, volumes, networking

### Workshop

Part A:

- Kubernetes concepts review
- Exercises, with review of concept before each one
    - *SETUP:* Set up a Kubernetes cluster, the quick way for playing
    - Deploy pod via deployment:
        - Command line
        - Manifest
        - Add service
    - Update image
    
Part B: (future)

- Exercises
    - Add volume for stateful app
    - deploy multi-container app
