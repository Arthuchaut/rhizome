# Table of content

- [Table of content](#table-of-content)
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Transport layer](#transport-layer)
- [Interests](#interests)

# Introduction

Rhizome is a decentralized communication substrate designed to support large-scale, heterogeneous compute networks by enabling brokerless, asynchronous interactions between autonomous nodes.  
It provides the foundational messaging, discovery, and routing mechanisms required for machines to dynamically join, leave, and cooperate within a globally distributed pool of computational resources.

# Objectives

In a decentralized compute network, participating nodes are inherently volatile: devices vary in capability, availability, trust level, and network conditions. Rhizome addresses this environment by decoupling communication from physical topology and static infrastructure. Nodes interact through logical identities and capabilities rather than fixed endpoints, allowing workloads, control signals, and coordination messages to be exchanged without prior knowledge of where or how peers are deployed.

# Transport layer

Rhizome uses QUIC as its primary transport protocol, with TCP/TLS as a fallback, providing secure, multiplexed communication well-suited to unreliable and heterogeneous networks. This transport layer enables a uniform substrate for control-plane operations such as peer discovery, capability advertisement, scheduling coordination, heartbeat propagation, and job lifecycle management, while remaining agnostic to execution models and workload semantics.

# Interests

Unlike traditional HPC fabrics optimized for tightly coupled, static environments, or centralized cloud platforms that rely on global schedulers and brokers, Rhizome is intentionally designed for open, adaptive, and failure-prone networks. It does not attempt to optimize numerical kernels or replace high-performance interconnects; instead, it focuses on enabling coordination, orchestration, and communication across independently owned and operated machines at planetary scale.  

By providing a neutral, brokerless communication layer, Rhizome allows higher-level systems (such as decentralized schedulers, compute marketplaces, volunteer networks, or distributed machine learning frameworks) to be built without embedding assumptions about topology, trust, or lifecycle into the communication fabric itself.