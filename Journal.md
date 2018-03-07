# Journal_1
## Jeudi 01 fevrier
### Read the documents
#### Big Data and HPC collocation: Using HPC idle resources for Big Data Analytics
[Go to the link of documents](https://hal.archives-ouvertes.fr/hal-01633507/file/bigdata_hpc_colocation.pdf)
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
### Read the documents
#### Batsim: a Realistic Language-Independent Resources and Jobs Management Systems Simulator
##### part1
[Go to the link of documents](https://hal.archives-ouvertes.fr/hal-01333471/document)
1. to know what is **batsim** and why we need it
2. the general description of batsim
3. the introduction of model and the developpment of batsimSS
4. batsim inner mechanics
5. continue

### Batsim overview
![alt text](https://github.com/Tuo018/Stage_TER/blob/master/Batsim.png)<br/>
### Batsim inner mecanic
![alt text](https://github.com/Tuo018/Stage_TER/blob/master/Images/batsim_inner_mecanic.png)
***

# Journal_3
## Jeudi 08 fevrier
### Read the documents
#### Batsim: a Realistic Language-Independent Resources and Jobs Management Systems Simulator
##### part2
[Go to the link of documents](https://hal.archives-ouvertes.fr/hal-01333471/document)
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
### Read the documents
#### Versatile, Scalable, and Accurate Simulation of Distributed Applications and Platforms
##### part1
[Go to the link of documents](https://hal.inria.fr/hal-01017319v2/document)
In this dpcuemnt,we introduce the importance of simulation,and the developpement of simulation.
We make a comparaison with many different types simulation and we prefere introduce **SimGrid**. The most important is Quote break
>In this work, we rebut popular wisdom and claim that, when developing a >simulation framework,aiming for versatility is the way to achieve better >accuracy and better scalability.
***
And there are cruciel experiments about analysis among accuracy,scalability and versatility to get the best and most modern simulation.(continue)
***

### Learn how to use Grid5000
1. [Get an account](https://www.grid5000.fr/mediawiki/index.php/Grid5000:Get_an_account)</br>
2. [UsagePolicy](https://www.grid5000.fr/mediawiki/index.php/Grid5000:UsagePolicy)</br>
3. [Getting Started](https://www.grid5000.fr/mediawiki/index.php/Getting_Started)
***

# Journal_5
## Jeudi 15 fevrier
### Install **Batsim** and simple Test</br>
[Install and run **batsim**](https://github.com/oar-team/batsim/blob/master/doc/run_batsim.md)
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
We discuss this stage's **perspective**</br>
Overview
![alt text](https://github.com/Tuo018/Stage_TER/blob/master/overview1.jpg)
![alt text](https://github.com/Tuo018/Stage_TER/blob/master/Images/overview2.jpg)
***

# Journal_6
## Mecredi 28 fevrier
### Install __colmet__ and know **NAS**
#### **Colmet**
##### Introduction
> **Colmet** is a monitoring tool to collect metrics about jobs running in a
> distributed environnement, especially for gathering metrics on clusters
> and grids. It provides currently several backends :

> * taskstats: fetch task metrics from the linux kernel.
> * stdout: display the metrics on the terminal.
> * zeromq: transport the metrics across the network.
> * hdf5: store the metrics on the filesystem.

[Downlaod colmet](https://github.com/oar-team/colmet.git)</br>
##### Install, upgrade, uninstall colmet with these commands:
```
$ pip install [--user] colmet
$ pip install [--user] --upgrade colmet
$ pip uninstall colmet
```
Collect metrics about jobs running on localhost *127.0.0.1*
![oops](colmet_node.png)<br/>
[More information about Colmet](https://github.com/oar-team/colmet)

You should know about **Metric**

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

#### Connect to Grid5000
```
ssh tzhao@access.grid5000.fr
```
We have to submit the *public key* in our Grid5000 account

```
ssh-keygen -t rsa
```
Continue about *Grid5000*
***

# Journal_7
## Vendredi 02 Mars
### Review

**Batsim**<br/>
How to dispath jobs and allocate resrouces
> A batch scheduler -- AKA Resources and Jobs Management System (RJMS)
> is a system that manages resources in large-scale computing centers,
> notably by scheduling and placing jobs, and by setting up energy
> policies.</br>

**Colmet**<br/>
Monitoring of applications
> A monitoring tool to collect metrics about jobs running in a distributed > environnement<br/>

**NAS**<br/>
To get the trace
> The NAS Parallel Benchmarks (NPB) are a small set of programs designed to help evaluate the performance of parallel supercomputers.

#### Grid5000
A set of hosts, free resources and respect the specification to use  
> Grid'5000 is a large-scale and versatile testbed for experiment-driven
> research in all areas of computer science, with a focus on parallel and
> distributed computing including Cloud, HPC and Big Data.

***

# Journal_8
## Mecredi 07 Mars

### Utilization of Grid5000
1. Connect to a Grid'5000 access machine
```
ssh tzhao@access.grid5000.fr
```
2. Connecting to a Grid'5000 site
```
ssh Grenoble
```
**Attention**<br/>
> Get a different home directory on each Grid'5000 site. (use **Rsync** or **scp** to move data around.)<br/>
> Grid'5000 does NOT have a BACKUP service for Grid'5000's users home directories

3. Discovering and visualizing resources<br/>
two ways to check the resource status on site<br/>
[Monika](https://intranet.grid5000.fr/oar/Nancy/monika.cgi)<br/>
[Gantt](https://intranet.grid5000.fr/oar/Nancy/drawgantt-svg/)
4. Reserving resources with OAR: the basics<br/>
```
oarsub -I
oarsub -l host=3 -I == oarsub -l nodes=3 -I
oarsub -l core=1 -I
```
To terminate your reservation and return to the frontend
```
exit
```
![alt text][https://github.com/Tuo018/Stage_TER/blob/master/Images/To_reserve_three_hosts%20_three_nodes.png]
**walltime**<br/>
The walltime is the expected duration you envision to complete your work.<br/>
**OARSH**<br/>
Oarsh is a wrapper around ssh that enables the tracking of user jobs inside compute nodes.<br/>
Example:
Change the node
```
oarsh graphene-97.nancy
```
Connect the node
```
oarsh graphene-97.nancy
```
Close the connection
```
logout
```
![alt text][https://github.com/Tuo018/Stage_TER/blob/master/Images/OARSH.png]
5. Reservations in advance
 ```
oarsub -l nodes=3,walltime=3 -r '2018-03-08 13:30:00'
 ```
6. Job management
```
oardel 12345
```
7. Selection of resources using OAR properties
 - Nodes from a given cluster
 ```
 fluxembourg: 	
 oarsub -p "cluster='granduc'" -l nodes=5,walltime=2 -I
 ```
 - Nodes with Infiniband QDR interfaces
 ```
 fgrenoble: 	
 oarsub -p "ib='QDR'" -l nodes=5,walltime=2 -I
 ```
 - Nodes with power sensors and GPUs
 ```
 flyon: 	
 oarsub -p "wattmeter='YES' and gpu='YES'" -l nodes=2,walltime=2 -I
 ```
 - Since -p accepts SQL
 ```
 fnancy: 	
 oarsub -p "wattmeter='YES' and network_address not in ('graphene-140.nancy.grid5000.fr', 'graphene-141.nancy.grid5000.fr')" -l nodes=5,walltime=2 -I
 ```
8. Extending the duration of a reservation
```
oarwalltime 12345 +1:30
```
9. Monitoring your nodes
 - **Kwapi **
 > Kwapi uses probes at the infrastructure level to collect information about network usage and power consumption: it does not require any specific application running on the nodes.<br>
 - **Ganglia**
 > Ganglia uses a service running on the nodes to collect information.<br/>

 [Measurements tutorial](https://www.grid5000.fr/mediawiki/index.php/Measurements_tutorial)

**Question**:
1. fnancy -->> graphene, how to come back<br/>
*fnancy* : reserve resources (get a job id)
*graphene* : check out the host exactment  
