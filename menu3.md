@def title = "Software"

# Software

\tableofcontents

## Current projects 

### Role: Leader 

#### GridapHybrid.jl

#### GridapDistributed.jl

#### GridapGeosciences.jl

### Role: Essential contributor

#### Gridap.jl

@@im-100
![](/assets/gridap-banner.png)

![](/assets/fig_gridap_intro.png)
@@

[Gridap.jl](https://github.com/gridap/Gridap.jl) is a free and open source {{fe}} library exclusively written in [Julia](https://julialang.org/). It is a general-purpose library which, rather than providing pre-bluid solvers for particular equations and methods, it makes available a feature-rich set of tools that allows users to build advanced solvers for their particular needs. With Gridap.jl, one can easily prototype FE methods in a laptop and eventually deploy them in large HPC clusters, with virtually no modifications of the high-level user code, and without departing from Julia code (i.e., no knowledge of C/C++ or fortran required at any point of the workflow).

The library currently supports linear and nonlinear PDE systems for scalar and vector fields, single and multi-field problems, conforming and nonconforming {{fe}} discretizations, on structured and unstructured meshes of simplices and n-cubes. Gridap.jl is extensible and modular. One can implement new {{fe}} spaces, new reference elements, use external mesh generators, linear solvers, post-processing tools, etc. See, e.g., the list of available [Gridap.jl plugins](https://github.com/gridap/Gridap.jl#plugins).

> **More info:**
> - Visit the official Gridap.jl [Github repository](https://github.com/gridap/Gridap.jl).
> - To get started, take a look at the [Gridap.jl Tutorials](https://gridap.github.io/Tutorials/stable/).
> - Ask us anything in our [Gitter chat](https://gitter.im/Gridap-jl/community).

I am an essential contributor to the project since early 2020 (e.g., 3rd in number of commits). I have adquired a deep understanding of its internals, and developed/improved some major components of it, mainly those related to extending it towards distributed memory parallelism and hybridizable finite element discretization schemes. I have also written several tutorials, including a [major one for developers](https://gridap.github.io/Tutorials/dev/pages/t013_poisson_dev_fe/), which goes over its internals, and it is an essential resource to computational math researchers that want to leverage the package for their own research. 

## Past projects 

### Role: leader

#### FEMPAR 

@@im-100
![](/assets/gridap-banner.png)

![](/assets/fig_gridap_intro.png)
@@

I am co-founder and main developer of FEMPAR (available at [https://github.com/fempar/fempar](https://github.com/fempar/fempar)), an open-source, mathematical software package for the numerical modelling of problems governed by {{pde}} on {{hpc}} platforms. It provides a set of state-of-the-art numerical discretizations, including finite element methods, discontinuous Galerkin methods, XFEM, and spline-based functional spaces. The library was originally designed to efficiently exploit distributed-memory supercomputers and easily handle multiphysics problems. It also provides a set of highly scalable numerical linear algebra solvers based on multilevel domain decomposition for the systems of equations that arise from PDE discretizations. In particular, it contains a novel bulk-asynchronous, fully-distributed, communicator-aware, inter-level overlapped, and recursive algorithmic adaptation of multilevel domain decomposition preconditioners towards extreme-scale computations which was shown to efficiently scale up to the 458K cores of the IBM BG/Q supercomputer installed in JSC, Germany. Thanks to these outstanding results, FEMPAR was qualified for High-Q club status, a distinction that JSC (Germany) awards to the most scalable EU codes.

The first public release of FEMPAR was almost 300K lines of code written in (mostly) {{oo}} Fortran and it made intensive use of the features defined in the 2003/2008 standards of the language. **`FEMPAR` was successfully used in 40x JCR Q1-ranked research papers on different topics and application areas**: simulation of turbulent flows and stabilized {{fe}} methods, MHD, monotonic {{fes}}, unfitted {{fes}} and embedded boundary methods, {{amr}}, {{am}} and {{hts}} simulations, and scientific software engineering. It has also been used for the highly efficient implementation of DD solvers  and block preconditioning techniques. Its users/developers span different research groups on national and international-level institutions, including UPC, CIMNE, ICMAB-CSIC, CIEMAT, ICTJA-CSIC, Czech Academy of Sciences (Czech Republic), Sandia National Labs (EEUU), North Carolina State University (USA), Duy Tan University (Vietnam),  Monash University (Australia), and l’Ecole Politechnique (Paris). Besides, it was a crucial tool for the successful execution of several high-quality EU-funded projects, namely, 1x ERC starting grant, 2x ERC PoC projects, 1x EU-FP7 project, and 3x H2020 projects.

For those who are interested on the design and rationale behind the mathematically-supported software abstractions in FEMPAR, a very through presentation is available at the following reference:

Santiago Badia, Alberto F. Martín and Javier Principe. \
FEMPAR: An object-oriented parallel finite element framework. \
*Archives of Computational Methods in Engineering* 25, 2 (2018), 195–271. \
[[ArXiv link]](https://arxiv.org/abs/1708.01773) [[DOI]](https://link.springer.com/article/10.1007%2Fs11831-017-9244-1)


A very nice tutorial-driven introduction to the software library (v1.0.0) can be found at the following reference:

Santiago Badia, and Alberto F. Martín. \
A tutorial-driven introduction to the parallel finite element library FEMPAR v1.0.0 \
*Computer Physics Communications* Volume 248, March 2020, 107059. \
[[ArXiv link]](https://arxiv.org/abs/1908.00891) [[DOI]](https://www.sciencedirect.com/science/article/pii/S0010465519303832)
