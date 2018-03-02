# Journal_1
## Jeudi 01 fevrier
Lire le documents
### Big Data and HPC collocation: Using HPC idle resources for Big Data Analytics
[go to the link of documents](https://hal.archives-ouvertes.fr/hal-01633507/file/bigdata_hpc_colocation.pdf)

1. to know the raison why we need **Big Data**' and **HPC** collocaton
2. to know the problem of collocation between Big Data and HPC
3. th solution
4. intrduction and descprtion of BEBIDA
5. experiments with BEBIDA
6. dicussion and analysis of the result
7. conclusion
***

# Journal_2
## Jeudi 07 fevrier
read the documents
### Batsim: a Realistic Language-Independent Resources and Jobs Management Systems Simulator
#### part1
[go to the link of documents](https://hal.archives-ouvertes.fr/hal-01333471/document)
1. to know what is **batsim** and why we need it
2. the general description of batsim
3. the introduction of model and the developpment of batsimSS
4. batsim inner mechanics
5. continue

### Batsim overview
![alt text](https://github.com/Tuo018/Stage_TER/blob/master/Batsim.png)
***
# Journal_3
## Jeudi 08 fevrier
read the documents
### Batsim: a Realistic Language-Independent Resources and Jobs Management Systems Simulator
#### part2
[go to the link of documents](https://hal.archives-ouvertes.fr/hal-01333471/document)
5. batsim evaluation experiment introduction of **profile** generation the type of profile
the fonction of profile
*_workload_ generation
the mode of multiplication
*execution workloads in a real platform.(**OAR**)
*execution worklaods in Simulation.(**Batsim**)
6. results *There is not a big difference in the two environments* we also analyse the similarities and differences

7. Try to reproduce our work
we need to control the three elemtns below
**environments**
*OS and programs and libraries
**experiments design and workflow**
we use two tools **EXECO**,**EVALYS**to evaluate
**inputs and outputs**

8. conclusion and future work

* future work
we used completely **homogeneous** in our experiments
energy model not been validated in a real machines yet
number and duration ofjobs(_scale experiments_)
opposite type of connection
*batsim capabilities
SMPI
IO problem
User reaction
***

# Journal_4
## Jeudi 14 fevrier
read the documents
### Versatile, Scalable, and Accurate Simulation of Distributed Applications and Platforms
#### part1
[go to the link of documents](https://hal.inria.fr/hal-01017319v2/document)
In this dpcuemnt,we introduce the importance of simulation,and the developpement of simulation.
We make a comparaison with many different types simulation and we prefere introduce **SimGrid**. The most important is Quote break
>In this work, we rebut popular wisdom and claim that, when developing a >simulation framework,aiming for versatility is the way to achieve better >accuracy and better scalability.
***
And there are cruciel experiments about analysis among accuracy,scalability and versatility to get the best and most modern simulation.(continue)
***

### learn how to use Grid5000
[get an account](https://www.grid5000.fr/mediawiki/index.php/Grid5000:Get_an_account)

[usagePolicy](https://www.grid5000.fr/mediawiki/index.php/Grid5000:UsagePolicy)

[Getting Started](https://www.grid5000.fr/mediawiki/index.php/Getting_Started)
***

# Journal_5
## Jeudi 15 fevrier
Install **Batsim** and simple Test

[install and run **batsim**](https://github.com/oar-team/batsim/blob/master/doc/run_batsim.md)
```
curl https://nixos.org/nix/install | sh
~/nix-profiles/etc/profile.d/nix.sh

git clone https://gitlab.inria.fr/vreis/datamove-nix.git
nix-env --install batsim

nix-env --file ./datamovepkgs -iA batsched
```
[Test Batsim](https://github.com/oar-team/batsim)
```
git clone https://gitlab.inria.fr/batsim/batsim.git
cd batsim

batsim -p platforms/small_platform.xml -w workload_profiles/test_workload_profile.json

batsched
```
we discuss this stage's **perspective**

Overview![alt text](https://github.com/Tuo018/Stage_TER/blob/master/overview1.jpg)
***
# Journal_6
## Mecredi 28 fevrier
install __colmet__ and know **NAS**
#### **Colmet**
##### Introduction
> **Colmet** is a monitoring tool to collect metrics about jobs running in a
> distributed environnement, especially for gathering metrics on clusters
> and grids. It provides currently several backends :

> * taskstats: fetch task metrics from the linux kernel.
> * stdout: display the metrics on the terminal.
> * zeromq: transport the metrics across the network.
> * hdf5: store the metrics on the filesystem.

[Downlaod colmet](https://github.com/oar-team/colmet.git)

Install, upgrade, uninstall colmet with these commands:
```
$ pip install [--user] colmet
$ pip install [--user] --upgrade colmet
$ pip uninstall colmet
```
Collect metrics about jobs running on localhost *127.0.0.1*
![oops](colmet_node.png)

You should know about **Metric**


[more information about Colmet](https://github.com/oar-team/colmet)

#### NAS
##### Introduction
The NAS Parallel Benchmarks (NPB) are a small set of programs designed to help evaluate the performance of parallel supercomputers.
##### About NPB
1. the composition
...five kernels and three pseudo-applications in the original.. "pencil-and-paper" specification (NPB 1)..
2. the developpment
3. the types/classes
4. the reports and results (experiment)

[More information about NAS](https://www.nas.nasa.gov/publications/npb.html)

We just need to know which **benmarks** we'll use in our experiemnts

###### Connect to Grid5000
```
ssh tzhao@access.grid5000.fr
```
we have to submit the *public key* in our Grid5000 account

```
ssh-keygen -t rsa
```
***
# Vendredi 02 Mars
Review

**Batsim**
A batch scheduler simulator(jobs and resources Management)
