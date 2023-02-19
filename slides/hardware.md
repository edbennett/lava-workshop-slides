# Background

-

## Context

- LFT is a top consumer of computing resources
- Researchers are likely to need to use them
- We need to ensure they can do so effectively and efficiently
  - How to run code
  - Where to run code
  - How to write efficient code

-

## Pyramid of computational demand

![Pyramid diagram showing "Configuration generation" at the bottom, "Measurement" in the middle, and "Analysis" at the top. An arrow points upwards reading "number of researchers" and downwards reading "computational demand".](images/computation_pyramid.svg) <!-- .element width="400px" -->

Plus separate considerations for:

- Tensor networks
- Machine learning
- Quantum computing/simulation

---

# Proposed syllabus

-

## High-level topics

- Accessing HPC, submitting jobs
- CPUs, etc.
- GPUs, etc.
- Interconnects
- Storage
- [Quantum computers $\rightarrow$ Thursday session]

-

## Accessing HPC, submitting jobs

- SSH, keys*
- Unix shell, shell scripts*
- Job schedulers and scripts*
- Modules, compilers*

\* Applicable for all learners

-

## CPUs, etc.

- Sockets, cores, threads*
- Memory capacity and connectivity*
- Memory latencies, CPU caches, the TLB
- Memory bandwidth, arithmetic intensity, roofline models
- Vectorisation/SIMD
- Pipelining, branch prediction?
- Specific vendor quirks (Intel, AMD, Arm)?

\* Applicable for all learners

-

## GPUs, etc.

- GPU strengths and weaknesses*
- GPU&ndash;host and GPU&ndash;GPU connectivity*
- GPU abstract structure: SMs, warps, threads
- GPU memory hierarchy
- Pipelining
- Specific vendor quirks (NVIDIA, AMD, Intel)?

\* Applicable for all learners

-

## Interconnects

- Strong and weak scaling studies*
- On-node vs. off-node scaling*
- Interconnect topologies*
- Infiniband specifics (SHARP, etc.)
- Interaction between interconnects and GPUs

\* Applicable for all learners

-

## Storage

- Types of storage (NFS, high-speed networked, node-local, RAM disk, archival)*
- File striping*
- Parallel I/O

\* Applicable for all learners

---

## Existing material

-

## Existing material: access and submitting

- [Software Carpentry][swc] (Unix shell, shell scripts, SSH keys)
- [Video on SSH keys and config][ssh-video]
- [Carpentries Incubator introduction to HPC][carpentries-hpc]
  - Most HPC centres also have similar documentation

[carpentries-hpc]: https://carpentries-incubator.github.io/hpc-intro/
[ssh-video]: https://www.youtube.com/watch?v=iZQkfdGRBKo
[swc]: https://software-carpentry.org

-

## Existing material: CPU

- Intel (and training partners) have some excellent material
  - Somewhat but not entirely Intel-specific
  - Ideally examples should be changed from engineering to LFT
- EXALAT and ExaTEPP projects in UK have material
- Need to extract basic "everyone should know" points

-

## Existing material: GPU

- NVIDIA has some excellent material
  - Relatively NVIDIA-specific
- Need to extract basic "everyone should know" points

-

## Existing material: Interconnect

- NVIDIA Networking (formerly Mellanox) should have material
- Need to extract basic "everyone should know" points

-

## Existing material: Storage

- tbc

---

# Other questions

-

## Overlaps

- Quantum computing
  - Aim for material to connect but not overlap
- Hardware for machine learning
  - Material should connect with/form part of both streams
- Reproducibility
  - Both likely to benefit from some Carpentries material
- Algorithms
  - Hardware design affects choice of algorithm
  - Material should dovetail

-

## Other communities

- The Carpentries
  - Introductory software skills for researchers
- DiRAC, ExCALIBUR, PRACE, other HPC initiatives

-

## Learning objectives: "Beginner"

All researchers should be able to:

- Connect to HPC resources securely
- Compile the software they need
  - With relatively optimal compilation options
- Submit their workloads to scheduler on an appropriate machine
- Choose relatively optimal choices for run options
  to make best use of the machine,
  e.g.
  - Parallelisation
  - Process placement
  - File locations

-

## Learning objectives: "advanced"

Experienced researchers with specific need should be able to:

- Write software that is robust, scalable, and efficient,
  maximizing performance per cycle/joule/currency unit
- Identify aspects of existing software
  that require adapting to take better advantage of available performance

-

## Exercises with code and data

"Would homeworks or exercises with code or data be useful 
to present new ideas in your topic?"

Yes.

-

## Prerequisites

- Carpentries material is designed to teach from scratch;
  few prerequisites
- Access to HPC for hands-on learning

-

## Other possible contributors

- Peter Boyle and team have significant expertise in this area
