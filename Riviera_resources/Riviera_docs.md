## Riviera Quick Start

Riviera is Colorado State University's high performance computing (HPC) cluster. Riviera currently consist of  2,112 CPU cores, 20 NVIDA A100s capable of 10 petaflops of AI computing and two high memory nodes (two terabytes of RAM per node). Along with three petabytes of storage.

### Riviera Quick-Start

1. From a *login node* load the slurmtools module to access the SLURM job scheduler instance for Riviera:
   ```bash
   $ module load slurmtools
   ```
*It is useful to add this command to ~/.bashrc so that slurm is loaded automatically at shell startup*
2. Once the Riviera Slurm job scheduler has been loaded you can submit and start jobs on the Riviera cluster. Consult the [requesting resources](#requesting-resources) section and the [examples](#examples) section below to learn how to direct your jobs to the appropriate Riviera compute nodes.

3. Software can be loaded into the Riviera compute environment via the LMOD [module system](../../compute/modules.html), which allows users choose software from our pre-installed software stack.

4. If you would like to use software that is not within our preinstalled stack your application must be compiled using locally. Consult our [compiling and linking documentation](../../compute/compiling.md) for more information on compiling software. 
### Cluster Summary
#### Nodes
The Riviera cluster is made up of different types of nodes outlined below:
- **CPU nodes**: 
	- Long 
	- Regular 
	- Short
- **GPU nodes**:
	-  Long 
	- Regular 
	- Short
- **High-memory nodes**:
	-  Long 
	- Regular 
	- Short
All nodes are available to all users.
### Node Features
The Riviera cluster features some heterogeneity. A variety of feature tags are applied to nodes deployed in Riviera to allow jobs to target specific CPU, GPU, network, and storage requirements.

Use the `sinfo` command to determine the features that are available on any node in the cluster.

> _**Note:**_ **Feature descriptions and finalized partitions names are still being added to Riviera nodes. Refer to the description of features list below for current node features.**

```bash
sinfo --format="%N | %f"
```

### Job Scheduling

All jobs on Riviera are run through a queue system using the SLURM job scheduler. Though many HPC workflows are run through batch-type jobs, interactive jobs on compute nodes are allowed but these must also be initiated through the scheduler. High-priority jobs move to the top of the queue and are thus guaranteed to start running within a few minutes, unless other high-priority jobs are already queued or running ahead of them. High-priority jobs can run for a maximum wall time of 24 hours. Low-priority jobs have a maximum wall time of 7 days.

More details about how to use SLURM to run jobs can be found in our [running applications with jobs](../../running-jobs/running-apps-with-jobs.md) documentation.
