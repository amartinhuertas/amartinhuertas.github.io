@def title = "Research"
@def hascode = true
@def rss = "A short description of the page which would serve as **blurb** in a `RSS` feed; you can use basic markdown here but the whole description string must be a single line (not a multiline string). Like this one for instance. Keep in mind that styling is minimal in RSS so for instance don't expect maths or fancy styling to work; images should be ok though: ![](https://upload.wikimedia.org/wikipedia/en/b/b0/Rick_and_Morty_characters.jpg)"
@def rss_title = "More goodies"
@def rss_pubdate = Date(2019, 5, 1)

@def tags = ["syntax", "code", "image"]


# Research

\toc

## Framing my research career \label{career}



In this introductory section I pinpoint the field of application of my research, and some general features of the problems within this field that my research targets.  This will help the reader understand my trajectory and the main {{rl}} I have carried out, which are covered in Section 
[Research trajectory and main research lines](#sec_rt_rl).

I am computer scientist whose research is framed within the broad field of **{{cse}}** (a.k.a. Scientific Computing). As a researcher working in this field, I contribute to the development of advanced computational models and algorithms able to solve complex physical problems of relevance in science and engineering.  My research is thus **highly interdisciplinary**, as it integrates methodologies from applied mathematics, computer science, and the physical sciences, *while developing new ideas at their interfaces*. Of particular relevance for the wide applicability and success of {{cse}}, *with a high influence on my research career*, are: (1)  the synergy among {{cse}} and **{{hpc}}**; 
and (2) the importance of high-quality, sustainable, and broadly-applicable **large-scale scientific software as a key output of {{cse}} research**. 

While I consider this to be a hallmark of my trajectory, I have had on the downside to devote considerable efforts towards being able to contribute at the interface of computer science and other areas which are not usually covered in the curriculum of a research-oriented computer scientist (and that were unfamiliar to me), such as computational continuum mechanics, finite element discretization methods, and numerical analysis. Despite this, I consider that, in the 10 years since my PhD. graduation ( **this is the last call I can present my candidacy to the "Ayudas para contratos Ramón y Cajal (RYC)"**) I have acquired a large degree of professional independence and academic maturity in this field, and a remarkable level of scientific productivity. In regards to my journal publications, I have to stress that most of my papers are published in Q1-ranked JCR journals, signed by a limited number of authors (3/4 authors on average), and the authors names were ordered in alphabetic order in 15/22 of them (this is indeed the standard practice that is followed, and we have followed, except rare exceptions, for articles published in the scientific computing/computational mathematics field). For a better indication of my contribution to these research papers I refer to Section [Research trajectory and main research lines](#sec_rt_rl). Finally, I would like to stress that, although I am not officially the principal investigator in the EC/ERC projects I have participated during my senior research period at CIMNE (*these indeed were decided accordingly to strategical decisions of the center/research unit*), I have had executive roles in 3 of these projects, in particular I have acted as Work Package leader in the FETHPC-H2020 *ExaQute* project (spanning 2018-2021), and as a Delegated Chief Investigator the EU-FP7 FORTISSIMO and ERC PoC FEXFEM. This have undoubtedly contributed to my capacity to lead my own research lines while managing teams of researchers.

As a researcher working in the {{cse}} field, I contribute to the development of computational models, algorithms, and software for several application problems. All of these share three common general features (not restricted to, though):

1. The physical phenomena to be simulated are governed by a (potentially highly nonlinear) {{pde}}, or more generally, by a system of {{pdes}}. These phenomena may span multiple temporal and spatial scales, and involve different physical models.

1. The system of {{pde}} is discretized by means of the {{fem}}. Thus, broadly speaking, the simulation pipeline encompasses three main ingredients: mesh generation and partitioning, space-time {{fe}} discretization, and solution of (non)linear system(s) of equations.

1. These are application problems with ever increasing modelling accuracy requirements, and thus highly demanding from the computational viewpoint. In particular, simulation pipelines grounded on highly parallel, algorithmically scalable algorithms and {{hpc}} software, thus able to efficiently exploit the vast amount of computational resources in current petascale supercomputers, are required in order to achieve the aforementioned modelling requirements.

The increasing levels of complexity both in terms of algorithms and hardware make the development of scientific software able to tackle the aforementioned features, while running efficiently on state-of-the-art numerical algorithms on {{hpc}} resources, a scientific challenge in itself. *A part of my research work has been devoted towards the achievement of this goal.* This is motivated by the fact that research on advanced, newly developed {{fe}} discretizations and solution algorithms for the {{hpc}} solution of {{cse}} complex problems frequently requires **innovative solutions on the software engineering aspects of a numerical software package as well**, and that these latter also represent an important contribution to other researchers working in the {{cse}} community. I am indeed co-founder, main software architect and project coordinator of `FEMPAR`(available at [https://github.com/fempar/fempar](https://github.com/fempar/fempar)), an open-source, scientific software package for the numerical modelling of problems governed by {{pde}} on {{hpc}} platforms. I am also contributor to `Gridap.jl` (available at [https://github.com/gridap/Gridap.jl](https://github.com/gridap/Gridap.jl)), and co-author of `gridapdistributed.jl` (available at [https://github.com/gridap/GridapDistributed.jl](https://github.com/gridap/GridapDistributed.jl)), its parallel message-passing version, which provide a new {{fe}} framework written in Julia for such a purpose. These latter two packages exploit the modern features of the Julia programming language (available at [https://julialang.org/](https://julialang.org/)) in order to strike a remarkable balance among performance and generality via appropriate mathematically-driven software abstractions. As a recent development, these software packages lay at the core of a 3-year {{dp}} project (ref: DP210103092) spanning 2021-2023 on large-scale inverse interface stochastic problems with application to groundwater modelling that has been recently awarded by the {{arc}}.

## Research trajectory and main research lines 
\label{sec_rt_rl}

This section overviews my research trajectory and main {{rl}} pursued. This will be presented in **reverse chronological order**, and split into three differentiated stages, namely: [senior researcher] (#sec_senior),  [post-doctoral](#sec_post_doc), and [pre-doctoral stages](#sec_phd). We note that that there is not necessarily a one-to-one correspondence among stage and position at an academic organization. The division into stages is done accordingly to the level of professional independence and academic maturity that was expected from me at the corresponding organizational units. 


### Senior researcher stage \label{sec_senior}

This period spans 2016-2020. Early 2016, **I was promoted as senior researcher at the {{cimne}}**, position which I held until late 2019, concurrently with my position as adjoint professor at {{upc}}. Then, early 2020, **I moved to the School of Mathematics at Monash University (Melbourne, Australia), where I have been selected/appointed as senior research fellow (Level B) for a 3-year period after winning an international competitive call for candidates**. During this period, I have carried out/I am carrying three main {{rls}} which are labeled as RL1-RL3 below. These are on-going  {{rls}} , and not chronologically ordered. Besides, they are not fully decoupled, as the research outputs from some of these might indeed provide advances readily to be used for the others as well. RL3 should be regarded as a cross-cutting, continuous {{rl}} , on which the advances of the other {{rls}}  are grounded on, and vice-versa.

#### RL1: Robust and scalable adaptive unfitted finite element methods with application to additive manufacturing \label{sec:rl1}
##### Research line statement
This main long-term research goal of this RL is the development of novel numerical methods for the accurate, computationally efficient and scalable simulation of large-scale transient multiscale {{pdes}} on complex evolving domains, with moving interfaces and/or free boundaries, with application to the simulation of metal {{am}} processes (a.k.a. 3D printing). The traditional {{cad}}/{{cae}} paradigm, which relies on (semi-automatic, hard-to-parallelize) unstructured mesh generators for spatial discretization, and the (inherently sequential) {{mol}} for time discretization, presents a poor integration among {{cad}} geometrical models and the {{pde}} numerical discretization algorithms, and at the most favorable scenario, is not efficient to tackle problems on non-trivial evolving geometries, *if not applicable/feasible at all*; see, e.g., Fig.[1](#fig_am_macro). To this end, **my contribution is the development of parallel-friendly advanced discretization methods based on the so-called unfitted (a.k.a. embedded) embedded finite element techniques \citep{Badia2018,burman_cutfem_2015,Schillinger2015} and their combination with highly scalable parallel linear solvers including multilevel domain decomposition \citep{Toselli2005} and {{amg}} \citep{Briggs2000}**. The final purpose of this research is to speed up the main bottlenecks of large multiscale/multiphysics finite element computations, in particular, the mesh generation, mesh partitioning, and the linear solver phase. More details are given in the subsections below. 

\label{fig_am_macro}
@@row
@@container
@@![](/assets/figures/growingInTime.png) @@
@@
*Figure 1: In an {{am}} macroscopic simulation, one has to design a mechanism that approximates the geometry $\Omega(t)$ following the real scanning path of the machine. It is $*$impractical$*$ to produce body-fitted unstructured meshes conforming with $\Omega(t)$ at all times.  Evolving geometries jeopardize the applicability of traditional simulation workflows. The proposed solution combines tree-based adaptive background meshes for the functional discretisation and cell-wise sub-meshes for integration purposes.*
~~~
<div style="clear: both"></div>
~~~
@@
\label{fig_am_macro}

##### Funding
This {{rl}} has been most recently funded by means of the FETHPC-H2020 *ExaQute* project (spanning 2018-2021). In particular, within this project, I have had the role of leader of the Working Package ''WP3 - Space-time parallelization'' (project web page available at [http://exaqute.eu/](http://exaqute.eu/)). **This has allowed me to fund and supervise a 2-year post-doc on robust and scalable adaptive unfitted {{fe}} methods and non-linear preconditioners for highly non-linear and multi-scale solid mechanics problems, and set up my own research team to work on this research line.** I also prepared a winning project proposal for the  *''Personal Técnico de Apoyo (PTA) 2019''* call in order to co-fund the position at {{upc}}  of a scientific software engineer at my team during a 3-year period. Recently, my project proposal on space-time adaptive unfitted methods has been funded by the Australian National Computational Merit Allocation Scheme (NCMAS) 2021 call (available at [https://my.nci.org.au/mancini/ncmas/2021/](https://my.nci.org.au/mancini/ncmas/2021/)). I have the role of co-{{pi}} in this project.

In early stages, this line was (partially) funded by two large H2020 EU projects, namely the *CAxMan-Computer Aided Technologies for Additive Manufacturing* and *eMUSIC- Efficient Manufacturing for Aerospace Components USing Additive Manufacturing, Net Shape HIP and Investment Casting* projects, in which the applicant participated as a researcher. These projects do not have a strong research component, and are led by the industrial sector.  However, they enabled joint collaboration efforts with leading experimental validation partners of {{am}} computer modelling tools. These include SKLSP in Xian, China, MCAM in Melbourne, Australia, and IK4-Lortek in Gipuzkoa, Spain. Both projects have strong technology-transfer potential. They include the application of their advances to the metal {{am}} process of several industrial use cases, such as the patented NUGEAR gearbox by STAM, Italy. 

##### Publications
The research work I have developed so far within RL1 has resulted in 6x research manuscripts  
 \citep{Badia2019a,Neiva2020,badia_stokes_2018,badia_aggregated_2017,Neiva2019a,Verdugo2019b} published in top quality JCR journals (Q1-ranked) and 2x preprints submitted for publication \citep{Badia2020,badia2020robust}.

##### Scalable Adaptive Mesh Refinement and coarsening (AMR) with dynamic load balancing via forests-of-trees 
\label{sec_scalable_amr}
{{amr}} is a highly appealing technique for the computationally efficient solution of {{pdes}} problems exhibiting highly localized features, such as moving fronts, or internal boundary layers. The basic idea is simple, to adapt the mesh, possibly dynamically, i.e., in the course of the simulation, with a higher mesh resolution wherever it is needed. However, the materialization of this idea on petascale parallel distributed-memory computers is a daunting challenge in itself.  Among others, mesh densification in localized areas can cause severe load unbalance. *The approach that I have pursued to tackle this challenge grounds on a new generation of petascale-capable algorithms and software for fast {{amr}} using adaptive tree-based meshes endowed with {{sfcs}}\citep{Holke2018}.
{{sfcs}} are exploited for efficient data storage and traversal of the adaptive mesh, fast computation of hierarchy and neighborship relations among the mesh cells, and scalable partitioning and dynamic load balancing. In particular, {{sfcs}} remarkably offer a linear run-time solution to the problem of (re)partitioning a tree-based mesh into processors. For hexahedral meshes, the state-of-the-art in tree-based *amr* with {{sfcs}}  is available at the `p4est` software \citep{burstedde_p4est_2011,Isaac2014}, which has been proven to scale up to hundreds of thousands of cores. This approach can be generalized to other cell topologies as well \citep{Holke2018}.

Forest-of-trees meshes provide multi-resolution capability by local adaptation. In the most general case, these meshes are *non-conforming*, i.e., they contain the so-called *hanging {{vefs}}*.  These occur at the interface of neighboring cells with different refinement levels.
Mesh non-conformity introduces additional implementation complexity specially in the case of conforming {{fe}} formulations, {{dofs}} sitting on **hanging** {{vefs}} cannot have an arbitrary value, they have to be judiciously constrained. This complexity can be relaxed, at the price of a higher of number of mesh cells, by enforcing the so-called 2:1 balance constraint. Essentially, additional (balance) refinement is introduced in order to bound the ratio among  the refinement levels of any two neighbouring cells. The set up and application of hanging {{dofs}} constraints is well-established knowledge \citep{Rheinboldt1980,Shephard1984}. **In a parallel distributed-memory environment, these steps are much more involved.** In order to scale {{fe}} simulations to large core counts, the standard practice is to constraint the distributed-memory data structures to keep a single layer of extra ghost cells along with the local cells, thus minimizing the impact of these extra cells on memory scalability.
Under this constraint, if a set of suitable conditions are not satisfied, then the hanging {{dof}} constraint dependencies may expand beyond the single layer of ghost cells, thus leading to an incorrect parallel {{fe}} solver.
To make things worse, **the current literature clearly fails to explain when and why the parallel algorithms and data structures required to support generic conforming {{fe}} discretizations atop tree-based adaptive meshes are correct.**

**My main contribution has been to address *in a rigorous way* the development of algorithms and data structures for parallel adaptive {{fe}} analysis on tree-based meshes endowed with {{sfcs}}**. These are part of a generic {{fe}} simulation framework *that is designed to be general enough to support a range of cell topologies, recursive refinement rules for the generation of adaptive trees endowed with {{sfcs}}, and various types of conforming {{fes}}.*  Starting with a set of (reasonable) assumptions on the basic building blocks that drive the generation of the forest-of-trees, namely, a recursive refinement rule and a {{sfc}} index \citep{Holke2018}, **I have inferred results based on mathematical propositions and proofs, yielding the (correctness of the) parallel algorithms in the framework.**
A {{mpi}}-parallel implementation of these algorithms is available at `FEMPAR` \citep{badia_fempar_2017}. `FEMPAR` uses `p4est` as its specialized forest-of-octrees meshing engine, although any other engine able to fulfill a set of requirements could be plugged in the algorithms of the framework as well. *A strong scaling study of this implementation when applied to Poisson and Maxwell problems reveals remarkable scalability up to 32.2K CPU cores and 482.2M {{dofs}} on the Marenostrum IV supercomputer.  Besides, a comparison of `FEMPAR` performance  with that of the state-of-the art `deal.II` software, reveals at least competitive performance, and at most factor 2-3 improvements on a massively parallel supercomputer.* As an illustration, Fig.2 reports remarkably scalability with a standard benchmark for evaluating the performance and scalability of {{amr}} codes, namely the Galerkin trilinear {{fe}} discretization of a 3D Poisson problem with a discontinuity in the source term that leads to a solution that is non-smooth along a sinusoidal surface through the domain. This tough problem challenges the performance and scalability of {{amr}} codes, as a very fine mesh resolution is required in order to reduce the error in that area.  
In a nutshell, the experiments starts from an initial uniform mesh, and the  mesh is adapted using a posteriori error estimators across several {{amr}} cycles until a target error criteria is fulfilled.  After each cycle, the mesh and related data (e.g., temperature field) is re-distributed/migrated in order to keep the computational load balanced. In Fig.2, we provide the strong scalability on the Gadi supercomputer of the different stages summed across all adaptation levels with 13 and 16 {{amr}} cycles. The curve labelled as "Total sub-assembly" includes the total computational cost involved in the solution of the {{pde}} at hand. The average load per core at the last step ranges, in Fig.[2](#fig_strong_scaling_fempar_amr)(a), from 128.7 KDOFs/core to 4.08K DOFs/core, and, in Fig.[2](#fig_strong_scaling_fempar_amr)(b), from 332.9 MDOFs/core to 20.7K DOFs/core. Beyond that load/core limit, one can barely expect state-of-the-art {{amg}} solvers to be able to reduce the computational time further with increasing number of cores, so that these are excellent scaling results for such a tough problem.

\label{fig_strong_scaling_fempar_amr}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fempar_am_gadi_scalability.png" </img></td>
    </tr> 
    <caption>
    Figure 2: Strong scaling test results (i.e., global problem fixed, increasing number of cores) for `FEMPAR` on Gadi.
    </caption>
</table>
~~~
@@table
@@div
    @@tr
      @@td
        @@img ![](/assets/figures/fempar_am_gadi_scalability.png) @@ 
      @@
    @@
@@
@@
Figure 2: Strong scaling test results (i.e., global problem fixed, increasing number of cores) for `FEMPAR` on Gadi.  


@@row
@@container
@@img-small ![](/assets/figures/fempar_am_gadi_scalability.png) @@
@@
*Figure 2: Strong scaling test results (i.e., global problem fixed, increasing number of cores) for `FEMPAR` on Gadi.*
@@

**This work has been recently published at the *SIAM Journal on Scientific Computing* \citep{Badia2019a}-->**. This paper substantially improves the current understanding of this topic with rigorous proofs of the computational benefits of the 2:1 k-balance (ease of parallel implementation and high-scalability) and the minimum requirements a parallel tree-based mesh must fulfil to yield correct parallel finite element solvers atop them assuming one is to keep the constraint that only a single layer of ghost cells is stored.

##### Relaxing mesh generation constraints with embedded methods
**Mesh generation is known to be one of the main bottlenecks of real-world industrial {{fe}} simulations.** Conventional {{fes}} require meshes that are body-fitted. That is, meshes  that conform to the geometrical boundaries of the computational domain (see Fig.[3b](#fig_fitted-vs-unfitted)). Constructing such grids is not an obvious task for complex geometries, 
it is time consuming and often requires skilled human intervention (mesh generation is estimated as 80\% of total simulation time in industrial applications \citep{Cottrell2009}). 

**An appealing alternative to circumvent this issue are the so-called embedded {{fe}} methods \citep{Badia2018,burman_cutfem_2015,Schillinger2015} (a.k.a. unfitted or immersed boundary methods).** The usage of embedded discretisation schemes drastically reduces the geometrical constraints imposed on the meshes to be used for discretization. Meshes do not require to be body-fitted, allowing one to simulate problems in complex domains using structured meshes (see Fig.[3c](#fig_fitted-vs-unfitted)). **This salient property is indeed essential for large-scale computations, since the generation of unstructured meshes in parallel and their partition using graph-partitioning techniques scale poorly \citep{chevalier_pt-scotch_2008} and in many cases require human intervention.** Embedded discretisation methods are thus highly appealing, among others, for problems posed on complex geometries, and/or for which tracking evolving interfaces or growing domains in time is impractical using body-fitted meshes; see Fig.[1](#fig_am_macro).

\label{fig_fitted-vs-unfitted}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_intro_imb_1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_intro_imb_3.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_intro_imb_2.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
    </tr>
</table>
~~~
*Figure 3: Body-fitted vs. unfitted meshes. (a) Computational domain. (b) Body-fitted mesh. (c) Body-fitted vs. unfitted meshes.*

<!--\label{fig_fitted-vs-unfitted-a}
@@row
@@container
@@left ![](/assets/figures/fig_intro_imb_1.png) @@
@@
*Figure 3(a) Computational domain.*
~~~
<div style="clear: both"></div>
~~~
@@
\label{fig_fitted-vs-unfitted-b}
@@col
@@container
@@left ![](/assets/figures/fig_intro_imb_3.png) @@
@@
*Figure 3b: Body-fitted mesh.*
~~~
<div style="clear: both"></div>
~~~
@@
\label{fig_fitted-vs-unfitted-c}
@@col
@@container
@@left ![](/assets/figures/fig_intro_imb_2.png) @@
@@
*Figure 3c: Body-fitted vs. unfitted meshes.*
~~~
<div style="clear: both"></div>
~~~
@@ 
-->
In an embedded formulation, the geometry is still provided explicitly in terms of a boundary representation  (e.g., a STL mesh) or implicitly via a level-set function. It requires mesh cutting techniques that perform the intersection between the background mesh and the surface description (implicit or explicit). **However, the complexity of this process is significantly lower than the one underlying an unstructured mesh generator.** It is a cell-wise task, and the cell partitions are not used for discretisation but only integration purposes. At the end of the process, we have interior, exterior, and $*$cut cells$*$.


##### The aggregated unfitted finite element method (AgFEM)

However, embedded methods have known drawbacks. The most salient one, **still an open problem nowadays**, is the so-called **small cut cell problem**. Some cells of the unfitted mesh can be intersected by a very small part of the domain, which leads, in practice, to arbitrarily large condition numbers in the underlying discrete {{fe}} operators. In recent years, different approaches have been considered in order to address the small cut cell problem. Initial approaches consist in adding stabilisation terms to the discrete problem, using some kind of artificial viscosity method to make the problem well-posed; see, e.g., the cutFEM method \citep{burman_cutfem_2015} or the Finite Cell Method \citep{Schillinger2015}.  

  In order to avoid, among others, the introduction of artificial viscosity terms into the discrete variational problem (thus sticking into a Galerkin problem), **I have recently developed  in \citep{badia_aggregated_2017} a novel discretization method for elliptic problems, the so-called {{AgFEM}}**; see Fig.[4](#fig_agfem). **In \citep{badia_stokes_2018}, I have also extended these techniques to indefinite problems in incompressible flow discretisations**. Besides, I have been able to mathematically prove for both the elliptic and indefinite cases that the {{AgFEM}} formulation shares the salient properties of body-fitted {{fe}} methods such as stability, condition number bounds, optimal convergence, and continuity with respect data. See Figs.[5](#fig_agfem_poisson) and [6](#fig_agfem_stokes) for selected numerical results. 

\label{fig_agfem}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_spaces_2_z_pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_dof_to_cell_map_3.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_test_popcorn_3d_aggr_light.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
    </tr> 
</table>
~~~
*Figure 4: (a) The shape functions associated to {{dofs}} in the exterior of the domain (marked with a red cross in the figure) may have an arbitrarily small support in the interior of the domain. Thus, there is no guarantee that the condition number of the linear system arising from discretization is bounded. (b) {{AgFEM}} formulations extrapolate these ill-posed {{dofs}} as a linear combination of selected interior {{dofs}} (via suitably-defined algebraic constraints imposed into the space of {{fe}} functions). These constraints are defined by building the so-called cell aggregates (in blue), that give the name to the formulation. A cell aggregation is an agglomeration of cells composed by a single interior cell, and a set of face-connected neighbouring cut cells connected to it. (c) Visualization of the cell aggregates built by the method for a 3D pop-corn like domain embedded in a uniform Cartesian mesh.*
<!-- 
\begin{figure}[H]
\centering
\begin{tabular}{ccc}
\includegraphics[width=0.2\textwidth]{figures/fig_spaces_2_z.pdf} &
\includegraphics[width=0.2\textwidth]{figures/fig_dof_to_cell_map_3.pdf} & 
\includegraphics[width=0.2\textwidth]{figures/fig_test_popcorn_3d_aggr_light.png} \\
(a) & (b) & (c)
\end{tabular}
	*(a) The shape functions associated to {{dofs}} in the exterior of the domain (marked with a red cross in the figure) may have an arbitrarily small support in the interior of the domain. Thus, there is no guarantee that the condition number of the linear system arising from discretization is bounded. (b) {{AgFEM}} formulations extrapolate these ill-posed {{dofs}} as a linear combination of selected interior {{dofs}} (via suitably-defined algebraic constraints imposed into the space of {{fe}} functions). These constraints are defined by building the so-called cell aggregates (in blue), that give the name to the formulation. A cell aggregation is an agglomeration of cells composed by a single interior cell, and a set of face-connected neighbouring cut cells connected to it. (c) Visualization of the cell aggregates built by the method for a 3D pop-corn like domain embedded in a uniform Cartesian mesh.*

\end{figure}
-->
\label{fig_agfem_poisson}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_test_sphere_2d_var_setup.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_test_sphere_2d_var_condest_diri.pdf-1.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a) Moving computational domain</th>
        <th>(b) Condition number vs. domain position</th>
    </tr> 
</table>
~~~
*Figure 5: Poisson problem defined on a moving domain. Note that the standard embedded formulation leads to very high condition numbers, which are very sensitive to the relative position between the computational domain and the background mesh, specially for second order interpolations ($p=2$). In contrast, the condition number is much lower for the enhanced formulation (the {{AgFEM}} method) and it is nearly independent of the position of the domain.*

<!--
\begin{figure}[H]
\centering
\begin{subfigure}[b]{0.27\textwidth}
\centering
\includegraphics[width=\textwidth]{figures/fig_test_sphere_2d_var_setup.pdf}
\caption{Moving computational domain}
\end{subfigure}
\hspace*{1em}
\begin{subfigure}[b]{0.45\textwidth}
\centering
\includegraphics[width=\textwidth]{figures/fig_test_sphere_2d_var_condest_diri.pdf}
\caption{Condition number vs. domain position}
\end{subfigure}
\caption{Poisson problem defined on a moving domain. Note that the standard embedded formulation leads to very high condition numbers, which are very sensitive to the relative position between the computational domain and the background mesh, specially for second order interpolations ($p=2$). In contrast, the condition number is much lower for the enhanced formulation (the {{AgFEM}} method) and it is nearly independent of the position of the domain.}
\label{fig_agfem_poisson}
\end{figure}

-->

\label{fig_agfem_stokes}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_colorbar_h.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_colorbar_h.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_colorbar_h.pdf-1.png" alt="" </img></td>
    </tr>
    <tr>
        <td><img width="100" src="/assets/figures/fig_bullets_3d_geo.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_bullets_3d_sol_u.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/fig_bullets_3d_sol_P.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a) Problem geometry.</th>
        <th>(b) Velocity (magnitude).</th>
        <th>(c) Pressure.</th>
    </tr> 
</table>
~~~
*Figure 6: Numerical solution of a (dimensionless) Stokes problem using the {{AgFEM}} method (streamlines colored by velocity magnitude and pressure). This computation is carried out without constructing an unstructured body fitted mesh thanks to the application of the {{AgFEM}} method.*

<!--
\definecolor{myellow}{RGB}{255,230,128}
\definecolor{gray20}{RGB}{204,204,204}
\definecolor{mygray}{RGB}{204,204,204}
\definecolor{mygreen}{RGB}{138,203,95}
\definecolor{myblue}{RGB}{77,151,214}
\begin{figure}[H]
  \centering
  \begin{subfigure}[c]{0.32\textwidth}
      \centering
      \tikz{\fill[myblue]  (0,0) rectangle (2.0em,0.5em);} {\small Inflow}
      \hspace{1em}
      \tikz{\fill[mygreen]  (0,0) rectangle (2.0em,0.5em);} {\small Outflow}
  \end{subfigure}
      %
  \begin{subfigure}[c]{0.32\textwidth}
    \centering
    \begin{tikzpicture}
      \node[inner sep=0pt] (cbar) at (0,0) {\includegraphics[width=0.4\textwidth]{figures/fig_colorbar_h.pdf}};
      \node[anchor=west] at (cbar.east) {\small $75.0$};
      \node[anchor=east] at (cbar.west) {\small $0.0$};
    \end{tikzpicture}
  \end{subfigure}
      %
  \begin{subfigure}[c]{0.32\textwidth}
    \centering
    \begin{tikzpicture}
      \node[inner sep=0pt] (cbar) at (0,0) {\includegraphics[width=0.4\textwidth]{figures/fig_colorbar_h.pdf}};
      \node[anchor=west] at (cbar.east) {\small $53.0$};
      \node[anchor=east] at (cbar.west) {\small $-1.4$};
    \end{tikzpicture}
  \end{subfigure}

  \begin{subfigure}[b]{0.32\textwidth}
      \centering
      \includegraphics[width=0.99\textwidth]{figures/fig_bullets_3d_geo.png}
      \caption{Problem geometry.}
    \label{fig:complex-case1-sol-a}
  \end{subfigure}
  \hspace{0em}
  \begin{subfigure}[b]{0.32\textwidth}
    \centering
    \includegraphics[width=0.99\textwidth]{figures/fig_bullets_3d_sol_u.png}
    \caption{Velocity (magnitude).}
    \label{fig:complex-case1-sol-b}
  \end{subfigure}
  \begin{subfigure}[b]{0.32\textwidth}
    \includegraphics[width=0.99\textwidth]{figures/fig_bullets_3d_sol_p.png}
    \caption{Pressure.}
    \label{fig:complex-case1-sol-c}
  \end{subfigure}
  \caption{Numerical solution of a (dimensionless) Stokes problem using the {{AgFEM}} method (streamlines colored by velocity magnitude and pressure). This computation is carried out without constructing an unstructured body fitted mesh thanks to the application of the {{AgFEM}} method.}
  \label{fig_agfem_stokes}
\end{figure}
-->

##### Petascale-capable distributed-memory parallelization of AgFEM

**bf The small cut cell problem of embedded methods is a major issue when dealing with large-scale simulations.** In large-scale scenarios, one has to invariably rely on (preconditioned) iterative linear solvers based on the generation of Krylov subspaces \citep{saad_iterative_2003}. Krylov methods are well-known to be very sensitive to the conditioning and spectral properties of the linear system coefficient matrix. Most of the works enabling the usage of iterative linear solvers in combination with embedded {{fe}} methods consider tailored preconditioners for the matrices affected by the small cut cell problem. The main drawback of this approach is that one relies on highly customized solvers, and therefore, it is not possible to take advantage of well-known and established linear solvers for {{fe}} analysis available in renowned scientific computing packages as TRILINOS \citep{Heroux2005} or PETSc \citep{petsc-user-ref}. **The {{AgFEM}} method solves this issue at the discretization level, and thus opens the door for the efficient exploitation of state-of-the art petascale-capable iterative solvers.**

Taking this as a motivation, **I have recently developed the message-passing variants of the algorithms involved in all stages of the {{AgFEM}} method (e.g., construction of cell aggregates, set up and resolution during {{fe}} assembly of ill-posed {{dof}} constraints, etc.).** Up to the fact that the processors might require to retrieve from remote processors the roots of those cell aggregates which are split among processors, this work has proven the {{AgFEM}} method to be a method very amenable to distributed-memory parallelization. In particular, it can be implemented using standard tools in parallel {{fe}} libraries, such as ghost cells nearest neighbour exchanges.  I have implemented these algorithms in `FEMPAR` using MPI for inter-processor communications. **Their high appeal at large scales has been demonstrated with a comprehensive weak scaling test up to 16K cores and up to nearly 300M DOFs and a billion cells in the Marenostrum-IV supercomputer* using the Poisson equation on complex 3D domains as model problem. See Fig.[7](#fig_fig_scalability-agfem).
The obtained results confirm the expectations: when using {{AgFEM}}, the resulting systems of linear algebraic equations can be effectively solved using standard {{amg}} preconditioners. Remarkably,  I did not have to customize the default parameters of the preconditioner, demonstrating that users can take what is already available out there ''out of the box''. To my best knowledge, this is the first time that embedded methods are successfully applied to such large scales. **This work has been recently published at a JCR Q1-ranked journal in the field (see reference \citep{Verdugo2019} for more details).**

\label{fig_fig_scalability-agfem}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_array_geom.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/scalability/fig_paper_phases_time_vs_num_dofs_a0b0c0d1e0f0g0h0i0_l3.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/scalability/fig_solver_phases_time_vs_num_dofs_a0b0c0d1e0f0g0h0i0_l3.pdf-1.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
    </tr> 
</table>
~~~
*Figure 7: (a) Geometry. (b) Wall clock time in seconds in Marenostrum-IV for the major phases (except linear solver) versus scaled problem size in proportion to the number of CPU cores. (c) Linear solver wall clock times.*
<!-- 
\begin{figure}[H]
\centering
\begin{tabular}{ccc}
\includegraphics[width=0.25\textwidth]{figures/fig_array_geom.pdf} &
\includegraphics[width=0.33\textwidth]{figures/scalability/fig_paper_phases_time_vs_num_dofs_a0b0c0d1e0f0g0h0i0_l3.pdf} & 
\includegraphics[width=0.33\textwidth]{figures/scalability/fig_solver_phases_time_vs_num_dofs_a0b0c0d1e0f0g0h0i0_l3.pdf} \\ 
(a) & (b) & (c) \\
\end{tabular}
\caption{(a) Geometry. (a) Wall clock time in seconds in Marenostrum-IV for the major phases (except linear solver) versus scaled problem size in proportion to the number of CPU cores. (c) Linear solver wall clock times.}
\label{fig_fig_scalability-agfem}
\end{figure}
-->

##### $h$-AgFEM: extension of AgFEM to support AMR
Embedded methods can be used with a variety of background mesh types.
**The approach that I have pursued particularly leverages octree-based background meshes using the tools covered in Sec. [Scalable {{amr}} with dynamic load balancing via forests-of-trees](#sec_scalable_amr}).** This is achieved by means of a recursive approach in which a mesh with a very coarse resolution, in the limit a single cube that embeds the entire domain, is recursively refined step by step, until all mesh cells fulfill suitably-defined (geometrical and/or numerical) error criteria. See Fig.[8](#fig_embedded_amr).

\label{fig_embedded_amr}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fig_filling_curve_a.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/BSACB_initial_mesh.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/BSACB_final_mesh_clamped_side.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
    </tr> 
</table>
~~~
*Figure 8: (a) A circle domain with some circular holes inside embedded in a locally-refined quadtree-like background mesh. The colors represent the partition into 6 subdomains induced by a Z-shaped (a.k.a. as Morton) SFC. (b) Mesh used for integration purposes resulting from the intersection of the surface description of a cantilever beam with a set of spherical holes and a uniform Cartesian background mesh. (c) Mesh used for integration purposes resulting from the intersection of the surface above and a locally-adapted octree-like background mesh.*

<!-- 
\begin{figure}[H]
\centering
\begin{tabular}{ccc}
\includegraphics[width=0.25\textwidth]{figures/fig_filling_curve_a.pdf-1.png} &
\includegraphics[width=0.25\textwidth]{figures/BSACB_initial_mesh.png} & 
\includegraphics[width=0.25\textwidth]{figures/BSACB_final_mesh_clamped_side.png} \\ 
(a) & (b) & (c) \\
\end{tabular}
\caption{(a) A circle domain with some circular holes inside embedded in a locally-refined quadtree-like background mesh. The colors represent the partition into 6 subdomains induced by a Z-shaped (a.k.a. as Morton) SFC. (b) Mesh used for integration purposes resulting from the intersection of the surface description of a cantilever beam with a set of spherical holes and a uniform Cartesian background mesh. (c) Mesh used for integration purposes resulting from the intersection of the surface above and a locally-adapted octree-like background mesh.}
\label{fig_embedded_amr}
\end{figure}
-->

In a recent work~\citep{Badia2020}, currently under revision, **I have addressed the challenge of developing an adaptive unfitted finite element scheme that combines {{AgFEM}} with parallel {{amr}}.** At the core of this development lies a  
two-step algorithm to construct the {{fe}} space at hand that carefully mixes aggregation constraints of ill-posed {{dofs}} (to get rid of the small cut cell problem), and standard hanging {{dofs}} constraints (to ensure trace continuity on non-conforming meshes). Following this approach, I have derived a {{fe}} space that can be expressed as the original one plus well-defined linear constraints. Mathematical analysis and numerical experiments demonstrate its optimal mesh adaptation capability, robustness to cut location and parallel efficiency, on classical Poisson $hp$-adaptivity benchmarks. See Figs. [9](#fig_hagfem_solution)- [10](#fig_hagfem_condition). **This work opens the path to functional and geometrical error-driven dynamic mesh adaptation with {{AgFEM}} in large-scale realistic scenarios. Likewise, it can offer guidance for bridging other scalable unfitted methods and parallel {{amr}}.**

\label{fig_hagfem_solution}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/hAgFEM/pacman.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/hAgFEM/popcorn.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/hAgFEM/cheese.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/hAgFEM/array.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/hAgFEM/spiral.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
        <th>(d)</th>
        <th>(e)</th>
    </tr> 
</table>
~~~
*Figure 9: Geometries and numerical solution to the problems studied with tree-based $h$-adaptive {{AgFEM}} (from here on, referred to as $h$-AgFEM). (a)-(b) consider a variant of the Fichera corner problem, whereas (c)-(e) a Poisson problem with multiple shocks.*


<!-- 
\begin{figure}[H]
  \centering
  \begin{subfigure}[b]{0.18\textwidth}
      \centering
      \includegraphics[width=0.99\textwidth]{figures/hAgFEM/pacman.png}
      \caption{}
  \end{subfigure}
  \hspace{0em}
  \begin{subfigure}[b]{0.18\textwidth}
    \centering
    \includegraphics[width=0.99\textwidth]{figures/hAgFEM/popcorn.png}
    \caption{}
  \end{subfigure}
  \begin{subfigure}[b]{0.18\textwidth}
    \includegraphics[width=0.99\textwidth]{figures/hAgFEM/cheese.png}
    \caption{}
  \end{subfigure}
  \begin{subfigure}[b]{0.18\textwidth}
    \includegraphics[width=0.99\textwidth]{figures/hAgFEM/array.png}
    \caption{}
  \end{subfigure}
  \begin{subfigure}[b]{0.18\textwidth}
    \includegraphics[width=0.99\textwidth]{figures/hAgFEM/spiral.png}
    \caption{}
  \end{subfigure}
  \caption{Geometries and numerical solution to the problems studied with tree-based $h$-adaptive {{AgFEM}} (from here on, referred to as $h$-AgFEM). (a)-(b) consider a variant of the Fichera corner problem, whereas (c)-(e) a Poisson problem with multiple shocks.}
  \label{fig_hagfem_solution}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.7\textwidth]{figures/hAgFEM/convergence_unfitted.png}
\caption{For all cases in Fig.~\ref{fig:hagfem_solution}, $h$-{{AgFEM}} converges optimally. Moreover, in contrast to standard (std.) FEM, it does not suffer from severe ill-conditioning, that precludes generating solutions where $h$-{{AgFEM}} can.}
\label{fig:hagfem_convergence}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=0.7\textwidth]{figures/hAgFEM/condition_numbers_unfitted.png}
\caption{For all cases in Fig.~\ref{fig:hagfem_solution}, $h$-{{AgFEM}} condition number estimates are consistently well-below those of std. FEM.}
\label{fig_hagfem_condition}
\end{figure}
-->
\label{fig_hagfem_convergence}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/hAgFEM/convergence_unfitted.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 10: For all cases in Fig.[9](#fig:hagfem_solution), $h$-{{AgFEM}} converges optimally. Moreover, in contrast to standard (std.) FEM, it does not suffer from severe ill-conditioning, that precludes generating solutions where $h$-{{AgFEM}} can.*

\label{fig_hagfem_condition}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/hAgFEM/condition_numbers_unfitted.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 11: For all cases in Fig.[9](#fig_hagfem_solution), $h$-{{AgFEM}} condition number estimates are consistently well-below those of std. FEM.*


##### Extension of $h$-AgFEM to non-linear solid mechanics 
**Recently, in a close collaboration with the post-doc researcher that I have supervised during a 2-year period, we have introduced the algorithmic extensions to $h$-{{AgFEM}} in order to deal with non-linear solid mechanics problems.** This work has been recently submitted for publication, and is currently under review \citep{badia2020robust}. In a first stage, we have restricted ourselves to problems involving nonlinear materials whose behavior depends on the strain history. This sort of problems are used as a demonstrator, but we
stress that the techniques presented can also be applied to, e.g., problems with geometric nonlinearities (i.e., solids undergoing large deformations or deflections).
For such a purpose, we have devised a novel strategy that uses $h$-adaptive dynamic mesh refinement and re-balancing driven by a-posteriori error estimators in combination with an incremental solution of the nonlinear problem (a.k.a. pseudo-time stepping). Besides, this work also addresses the functional space representation of the history variables describing the nonlinear evolution of the constitutive model. The strategy is general enough to cover a wide range of constitutive models endowed with variables of any tensorial order.

As an illustration, **Fig.[12](ig_hagfem_plasticity) reports the results obtained from a nonlinear J2-plasticity production simulation for analyzing the strain-stress response of a  Cantilever beam with spherical holes made of a relevant ductile steel alloy on the Australian Gadi supercomputer.** In this experiment, as usual in nonlinear solid mechanics, a final load is imposed on the beam in load increments (pseudo time-steps), and the objective is to observe the permanent plastic deformation that the beam undergoes. Given that the problem is characterized by strain localization, the $h$-{{AgFEM}}  method is used in order to appropriately capture the geometry of the beam, in combination with {{amr}} in order to produce a locally refined mesh while deformation is localizing in order to achieve an error tolerance while keeping computational resources low. This experiment includes all the steps in a $h$-{{AgFEM}} simulation, namely skin mesh and background mesh intersection for each mesh adaptation cycle, setup of $h$-{{AgFEM}} and hanging node constraints, transfer of historical variables among meshes, dynamic load-balancing at each step, Newton-Raphson linearization with line search accelerated with {{amg}} preconditioning, etc. with localization given by a posteriori error estimators. In Fig. [12](#fig_hagfem_plasticity), we report the raw wall clock times of these simulations with increasing number of cores as reported by the job queuing system in Gadi for a problem with 11.687 MDOFs at the last load step. Thus, this is the true time that the user experiences when using the software. The value given in the "Serial run" row does not actually correspond to a real measurement, but to a linear extrapolation from the time measured with 192 cores. Memory consumption for $P=192$ was around 86\% of the total amount of memory available in 4 nodes. **Clearly, the most salient observation from Fig. [12c](#fig_hagfem_plasticity) is the considerably reduction in execution times. By exploiting parallel resources, the execution time can be reduced from months to less than a couple of hours.**

*Figure 12: (a) Lateral view of the adapted mesh at the last load step. (b) A section of the plastic deformation of the beam.  (c) Raw wall clock times with increasing number of Gadi cores. Simulation ends after 41 load steps.*

\label{fig_hagfem_plasticity}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/beam_lateral_view_mesh_final_load.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/BSPH_final_mesh_deformed_shape_displ_X.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
    </tr> 
</table>
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/strong_scaling_beam.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(c)</th>
    </tr> 
</table>
~~~
*Figure 12: (a) Lateral view of the adapted mesh at the last load step. (b) A section of the plastic deformation of the beam.  (c) Raw wall clock times with increasing number of Gadi cores. Simulation ends after 41 load steps.*


<!--
\begin{figure}[H]
  \centering
  \begin{subfigure}[b]{0.4\textwidth}
      \centering
      \includegraphics[width=0.99\textwidth]{figures/beam_lateral_view_mesh_final_load.png}
      \caption{}
  \end{subfigure}
  \begin{subfigure}[b]{0.3\textwidth}
      \centering
      \includegraphics[width=0.99\textwidth]{figures/BSPH_final_mesh_deformed_shape_displ_X.png}
      \caption{}
  \end{subfigure}
  \begin{subfigure}[b]{0.6\textwidth}
      \centering
      \includegraphics[width=0.99\textwidth]{figures/strong_scaling_beam.png}
      \caption{}
  \end{subfigure}
  \caption{(a) Lateral view of the adapted mesh at the last load step. (b) A section of the plastic deformation of the beam.  (c) Raw wall clock times with increasing number of Gadi cores. Simulation ends after 41 load steps.}
  \label{fig_hagfem_plasticity}
\end{figure}
-->

##### Application to metal additive manufacturing processes
I am applying the tools presented in previous sections, together with other modelling and numerical discretization inventions, in order to build an accurate computational model for the simulation of metal AM processes. (I note, however, that these are essential contributions in numerical methods for the {{fe}} discretization of {{pdes}}, and thus, their applicability goes far beyond AM computer modeling.) **The advances so far in this regard have been published in two  Q1-ranked JCR research journals<~\citep{Neiva2020,Neiva2019a}.**

AM (a.k.a. 3D printing) refers to a set of sophisticated manufacturing technologies to build up 3D objects, on a layer-by-layer basis, from a CAD model. AM has nowadays become sufficiently mature for the 3D printing of metallic objects readily to operate in industrially-relevant applications, including the aerospace, aeronautic, automotive or medical industry, among others. **The main breakthrough of AM is its ability to create cost-effective, short time-to-market objects with properties (i.e., strength, surface quality, material behavior, shape, etc.) almost impossible to produce with traditional technologies as e.g., casting or welding.** However, high-energy sources used to melt metal powders during the printing process induce thermo-mechanical shape distortions and residual stresses, that deteriorate the geometrical quality and the requested material properties. 
The current industrial practice is based on an expensive, time-consuming, trial-and-error process, which involves the production of hundreds of uncertified copies of the object before reaching the final part. A more sophisticated approach to cope with this limitation is to shift to virtual-based design and certification, using predictive computer modeling tools. **However, state-of-the-art simulation software available at the literature is still far beyond the accuracy and time frame requirements to unlock the full potential of 3D printers in real industrial use.**

**My work addresses, specifically, some of the challenges that arise due to the different length scales involved in the heat transfer analysis of AM processes by {{pbf}}  methods.**
In these methods, a laser is used in order to selectively melt a new {{pbf}} layer, which is spread over the building platform with a leveling blade. In this context, typical dimensions of a printed part are on the order of [cm]. However, the relevant physical phenomena are localized around the moving melt pool [μm], following the laser spot. Likewise, the layer size is also on the order of [μm], i.e. the scale of growth of the geometry is much smaller than the scale of the part. The printing of a layer starts with the spread of a layer of powder particles across the building camber, followed by the laser-melting and solidification of the cross section of the part that corresponds to the current layer height. It is clear from here that the material can be either a porous powder or nonporous liquid/solid medium, having rather different thermomechanical properties. A high-fidelity thermal analysis requires (at the very least) that the discretization appropriately captures
the interface among the porous and nonporous media. This jeopardizes the use of conventional {{fe}}
methods, that require a mesh to conform to this interface at all times to provide meaningful results. Even using {{amr}} techniques (to cope with the multiple spatial scales), this becomes a bottleneck in the simulation, because the mesh size is restricted across the whole layer, even far away from the melt pool. 

The specific goal is the high-fidelity thermal simulation of the printing process of parts with non-trivial geometries. **Given a set of material and printing process parameters, the outcome with relevant industrial interest is the capability to predict potential printing defects, such as excess or lack of powder fusion.** This sort of insightful information is crucial for application problem experimentalists, as, e.g., those at the Monash Centre for AM, with whom I collaborate. **To this end, I have developed a 3D transient thermal solver that can work on CAD geometries using  the $h$-{{AgFEM}} method on background octree-based meshes, reads the scanning sequence of the laser (using the same files as the AM machine), includes an activation procedure to determine the domain at all times, locally adapts in the melt pool via {{amr}} and exploits distributed-memory parallelism at all stages.** See Fig.[13](#fig_AM-AggFEM). These features, which are cornerstone for increasing modeling accuracy, and applicability to complex, industrially-relevant bodies, are not present in other AM modelling {{fe}} tools available at the literature. Indeed, the results obtained with this tool on an multi-core-based {{hpc}} cluster equipped with thousands of cores confirm that it is able to simulate AM processes with very thin layers, longer processes, higher deposition volumes, more complex geometries, significantly less time-to-solution etc., compared to the ones reached by a state-of-the-art (non-{{hpc}}, non-h-adaptive, body-fitted) software tool. 

\label{fig_AM-AggFEM}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/popcornFlake-0425.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/popcornFlake-0427.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/popcornFlake-0429.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/popcornFlake-0431.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
        <th>(c)</th>
        <th>(d)</th>
    </tr> 
</table>
~~~
*Figure 13: Snapshots of a thermal 3D printing simulation using the $h$-{{AgFEM}} method in order to effectively represent the geometry of the growing piece.*
<!--
\begin{figure}[H]
\centering
\vspace*{-1mm}
\includegraphics[width=0.25\textwidth]{figures/popcornFlake-0425.png}
\hspace*{-7mm}
\includegraphics[width=0.25\textwidth]{figures/popcornFlake-0427.png}
\hspace*{-7mm}
\includegraphics[width=0.25\textwidth]{figures/popcornFlake-0429.png}
\hspace*{-7mm}
\includegraphics[width=0.25\textwidth]{figures/popcornFlake-0431.png}

\caption{Snapshots of a thermal 3D printing simulation using the $h$-{{AgFEM}} method in order to effectively represent the geometry of the growing piece.}
\label{fig_AM-AggFEM}
\end{figure}
-->
#### RL2: Advanced numerical methods for the large-scale simulation of high temperature superconductors
\label{sec_rl2}
##### Funding
This {{ar}} was initiated simultaneously with the FORTISSIMO EU-FP7 experiment project entitled "Multi-physics simulation of {{hts}} devices”, in a joint collaboration of an {{hpc}} software provider (CIMNE), an application-problem specialist (ICMAB-CSIC), an {{hpc}} service provider (CESGA), and an end-user, technology-based company in the {{hts}} sector (OXOLUTIA S.L.). The efforts were focused on the development and experimental validation of an {{hpc}} modeling tool able to equip the latter with a very valuable quantitative understanding of the design process of {{hts}} tapes and bulks, towards the improvement of its {{hts}}-based products, thanks to a fast and high-fidelity virtual prototyping compatible with time-to-market restrictions. **In the course of this project, I led a small team within my local institution (1x PhD student, and 1x scientific software engineer) towards the achievement of the project goals.** Despite being a high-technology-transfer potential, with a medium-low research component project, these joint collaborations have equipped my team with very insightful feedback to support this {{ar}}, namely: (1) deep expertise regarding the highly challenging physical processes, and accompanying {{pde}}-based mathematical models, which are involved in the simulation of {{hts}} tapes and bulks; (2) the necessary equipment required to perform experimental validation tasks of the software tools grounded on the research outputs of RL2. 

##### Publications
The research work I developed so far within RL2 has resulted in 2x research manuscripts published at Q1-ranked JCR journals~\citep{Badia2019maxwell,Olm2019}. 

##### Motivation, research work description, and outcomes
A high temperature superconductor is a material that reaches the superconductor state at temperatures above the liquid nitrogen boiling temperature of 77K, i.e., far beyond the range of critical temperatures needed by conventional superconductors to reach the superconductor state (from around 20K to less than 1K). PIT (Powder In Tube co-extrusion and lamination) and coating technologies have allowed the development of wires and tapes able to substitute copper and conventional conductors in the manufacturing of cables and coils. In the present, the preferred format for these advanced materials is in the shape of flexible metallic tapes. **The benefits of using {{hts}} materials mainly stem from the resistance-free characteristics of {{hts}} wires coupled to its excellent performance in high magnetic fields.** Its range of application goes from very high field coils used for confining magnetically the hot plasma in future nuclear fusion reactors (like ITER or DEMO), energy storage or high resolution MRI, to motors, generators, cables, transformers or sensors and electronic devices. In all of the above applications, magnetic field, current density, temperature, heat generation, and mechanical stresses related to the high forces developed during cooling down and the working conditions at high magnetic fields should be considered. 

Computational tools are a powerful technique to simulate the behavior of {{hts}} tapes by solving the system of {{pdes}} that governs the problem. {{fe}} methods are commonly used in {{hts}} modeling, because they can handle complicated geometries, while providing a rigorous mathematical framework. **However, {{hts}} modeling is an extremely challenging, computationally-intensive task.** It is a multi-physics (involves electromagnetism, thermodynamics and mechanics), multi-scale (microns to millimeters), extremely non-linear problem. An appropriate formulation of the system of {{pdes}} governing the problem, the {{fe}} discretization scheme, and non-linear solver thus plays a crucial role in order to obtain meaningful results. The standard practice regarding computational modeling in the {{hts}} community consists on the usage of commercial software (such as e.g., COMSOL). **These software packages are not typically equipped with {{hts}}-tailored, state-of-the-art numerical methods, and are either sequential or poorly scale beyond a moderate number of cores.** As a consequence, a myriad of simplifications are introduced in the computational model, and computing times span from days up to some weeks, even for very simplified 2D models. In order to by-pass this bottleneck, **the research work that I have carried out pursues the development of advanced, {{hts}}-tailored numerical algorithms, and {{hpc}} software tools for the large-scale simulation of {{hts}} tapes and bulk on high-end computing environments.**
% 

\label{fig_hts_current_density}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/image21.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 14: Current density profile (color map) computed by the {{hts}} modeling tool for a toy 3D problem at a given fixed time.*


<!--
\begin{wrapfigure}{r}{0.5\linewidth}
\centering
\includegraphics[width=0.4\textwidth]{figures/image21.png}
\caption{Current density profile (color map) computed by the {{hts}} modeling tool for a toy 3D problem at a given fixed time.}
\label{fig:hts_current_density}
\end{wrapfigure}
-->
One of the outputs so far by this RL is a novel {{hpc}} software tool, grounded on `FEMPAR` (see Sec. [](#sec_rl3)), for the non-linear eddy current, AC loss large-scale modelling of {{hts}} tapes and bulks. **The hallmark of this tool, compared to any other available in the literature, is its ability to combine arbitrary-order Edge {{fes}} for the Maxwell Equations with {{amr}} on octree-based meshes (see Sec.[](#sec_scalable_amr)) while exploiting message-passing parallelism in all stages of the simulation pipeline \citep{Olm2019}, and a novel 2-level BDDC preconditioner that I have developed for the linearized discrete Maxwell Equations with heterogeneous materials able to scale up to dozens of thousands for computational cores \citep{Badia2019maxwell}**. The problem to be simulated consists of a superconductor material surrounded by a dielectric (i.e., extremely high resistivity) box, ''large enough'' (compared to region spanned by the superconductor) for neglecting the effects of the superconductor magnetization on the boundary of the dielectric box; see Fig.[14](#fig_hts_current_density). The system of {{pdes}} selected for describing this problem is grounded on the H-formulation of the Maxwell system of equations, properly extended to {{hts}} modelling via a judiciously-selected power law to describe the electric field-current density relation (see \citep{Olm2019} and references therein). This latter constitutive equation, which is required to describe the penetration of the magnetic flux and induced currents on {{hts}} materials, transforms the linear system of Maxwell equations into an extremely non-linear problem. 

The {{fe}} discretization and solver machinery is based on {{hts}}-tailored, state-of-the-art numerical algorithms. First, **the magnetic field is discretized using curl-conforming, Nèdèlec (a.k.a. edge) {{fes}} of arbitrary order.**  The usage of this sort of {{fe}} spaces is absolutely essential for the robust and accurate modelling of {{hts}} devices, as they relax continuity-constraints, compared to nodal Lagrangian {{fes}} typically used in the structural mechanics community, by letting the normal component of the discrete magnetic field to be discontinuous across the interface of two media (i.e., superconductor-dielectric box) with highly contrasting properties. 
On the other hand, **parallel {{amr}} by means of non-conforming, octree-based meshes, is used in order to tackle the multiscale nature of the phenomena, while keeping moderate computational requirements.** For example, in Fig.[14](#fig_hts_current_density), magnetic field and current density have to be captured in high detail within the superconductor through a high resolution mesh, while the ones at the dielectric box hardly vary, and thus a coarse-mesh resolution suffices. Finally, at the (non)linear solver kernel, **I have developed a highly-scalable software implementation of the aforementioned preconditioner (grounded on the advances in Sec.[](#sec_rl4), tailored for the discrete curl-curl operator with heterogeneous materials \citep{Badia2019maxwell}.** In a nutshell, in order to enforce the continuity across subdomains of the method, I have used a partition of the interface objects (edges and faces) into sub-objects determined by the variation of the physical coefficients of the problem. Besides, the addition of perturbation terms to the preconditioner is empirically shown to be effective in order to deal with the case where the two coefficients of the model problem jump simultaneously across the interface.  The new method, in contrast to existing approaches for problems in curl-conforming space does not require spectral information whilst providing robustness with regard to coefficient jumps and heterogeneous materials.  
This numerical algorithm is essential in order to accelerate the convergence of the underlying iterative solver at each Newton-Raphson non-linear step, while keeping bounded the number of iterations for both higher mesh resolution, and number of computational cores. See Fig.[15](fig_hts_tfs).

\label{fig_hts_tfs}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/iters_hts_first_step.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/times_hts_first_step.pdf-1.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a) Number of PCG iterations.</th>
        <th>(b) Wall clock time.</th>
    </tr> 
</table>
~~~
*Figure 15: Weak scalability on the MN-IV supercomputer, for different local problem sizes (i.e., $(\frac{H}{h})^3$ {{fes}}/core), of the novel 2-level BDDC preconditioner for the discrete Maxwell equations when applied to the first linearization of the non-linear problem corresponding to the first time step in a {{hts}} simulation.*

The results that my team and me have obtained with this tool on the BSC-CNS MN-IV supercomputer are very remarkable. 
First, **it has been shown to be able to accurately model an industrially-relevant, state-of-the-art, large-scale problem in the {{hts}} community with unprecedented resolution, and time-to-solution \citep{Badia2019maxwell}.** 
Second, in the framework of the collaboration with ICMAB-CSIC, **we could confirm that it significantly reduces computational times (with respect to a COMSOL-based solution) from weeks and hours, to days and minutes**, resp., for a number of 2D toy benchmarks problem proposed by ICMAB-CSIC, while being able to successfully (accurately) model 3D problems, **out of reach until today by ICMAB-CSIC**. 
Third, **the numerical tool has been validated experimentally against the so-called Hall probe mapping experiment**. A high agreement of numerical results against measured data was observed; see Fig.[16](#fig_hts-validation), and \citep{Olm2019} for details. 
Fourth, although it is still a prototype, **this tool is already providing insightful understanding of the electromagnetic behavior, under different design parameters (e.g., size and shape), of the {{hts}} tapes manufactured by OXOLUTIA S.L.** On-going work within RL2 is being focused on the improvement of this tool. In particular, it is being extended to thermo-mechanical coupling. 

\label{fig_hts-validation}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/experimental-rig-hts.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/B_400up.png" alt="" </img></td>
    </tr>
    <tr>
        <th>(a)</th>
        <th>(b)</th>
    </tr> 
</table>
~~~
*Figure 16: (a)Experimental rig designed by ICMAB-CSIC in order to measure the external magnetic field produced by a transport current in a 2G HTS tape. (b)Vertical component of the magnetic field at different tape regions for a
snapshot at a particular time in which the external applied current is of 400 Amperes.*


#### RL3: Software engineering of large scale scientific applications, open source scientific software
\label{sec_rl3}
##### Funding
This RL was *directly* funded by the EU-ERC PoC project, *FEXFEM-On a free open source extreme scale finite element software*, in which **I led a research team within the CIMNE-LSSC department (1x early career post-doc, 1x PhD. Student, and 1x scientific software engineer) towards the accomplishment of the project goals.**


##### Publications
The research work I developed so far within RL3 has resulted in 4x research manuscripts published in Q1-ranked JCR journals \citep{Badia.etal.ACME.2013,Badia2020fempar,Olm2019b,badia_fempar_2017}, and in the form of open source {{hpc}} software packages for the general {{cse}} community.

##### Research line statement and motivation
This work is motivated by the fact that research on **advanced, newly developed {{fe}} discretizations and solution algorithms for the {{hpc}} solution of {{cse}}  complex problems frequently requires innovative solutions on the software engineering aspects of a numerical software package as well, and that these latter also represent an important contribution to other researchers working in the {{cse}}  community**. As an example, edge {{fes}} for the Maxwell equations, although well-understood mathematically, are hard to implement in practice, at least in its full generality (e.g., bricks and simplices, arbitrary polynomial order, arbitrary neighbouring cells orientation, etc.). This is due to their extremely complex mathematical structure. In \citep{Olm2019b}, I have presented a mathematically-supported software architecture that sheds some light into this task to practitioners working in this field  by providing, among others, an straightforward manner for constructing its associated functional spaces. 

A part of  my research career has been focused on developing advanced mathematical software, in particular, software which can be re-used by other researchers in the community, in the seek, among others, of reproducible science. 
**Poorly software engineered codes, rigid, non-extensible, with a limited life span, developed by within a single research group or university department for a target application problem, and/or a specific numerical method, clearly do not serve the purpose**. A robust, efficient, sustainable software, engineered, among other criteria, with flexibility, usability, extensibility, composability, and interoperability in mind, resilient to new algorithmic and hardware trends, which in turn fosters collaboration among researchers from different institutions and background becomes essential. This is the ultimate goal of this RL. 

##### Research work description, and outcomes
**I am co-founder, main software architect and project coordinator of `FEMPAR` \citep{badia_fempar_2017}** (available at [https://github.com/fempar/fempar](https://github.com/fempar/fempar)), an open-source, {{hpc}}, hybrid MPI+OpenMP parallel, scientific software package for the numerical modelling of problems governed by {{pdes}} on {{hpc}} platforms (from multi-core based clusters, to high-end petascale supercomputers). The first public release of `FEMPAR` has almost 300K lines of code written in (mostly) {{oo}} Fortran and makes intensive use of the features defined in the 2003/2008 standards of the language. 
 
`FEMPAR` has a mature software architecture equipped with robust software abstractions for all the basic building blocks typically involved in a {{fe}} simulation; see Fig.[](#fig_main-structure) for an sketch of the ones involved in the discretization of the {{pde}} problem at hand. This software architecture has been judiciously engineered using advanced {{oo}} mechanisms (inheritance, dynamic run-time polymorphism, data hiding and encapsulation), design patterns and principles, in order to break {{fe}}-based simulation pipelines into smaller blocks that can be arranged to fit user’s application requirements. Through this approach, **`FEMPAR` supports a large number of different applications covering a wide range of scientific areas, programming methodologies, and application-tailored algorithms, without imposing a rigid framework into which they have to fit**; see e.g., the ones covered in RL1, RL2, and RL4. In seek, among others, of `FEMPAR` to become a community code, it is released for free for non-commercial purpose under the terms of the open source GNU GPLv3 license.

\label{fig_main-structures}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/fempar-abstractions.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 17: Main software abstractions in `FEMPAR` and some of their relationships.*

There is a number of, high-quality, open source OO {{fe}} libraries available in the community, e.g., deal.II, FEniCS, GRINS, Nektar++, MOOSE, MFEM, FreeFem++, DUNE, OpenFOAM. In general, these libraries aim to provide all the machinery required to simulate complex problems governed by {{pdes}} using {{fe}} techniques. However, **in all of these libraries, the solution of the linear system is clearly segregated from the discretization step.** The linear system is transferred to a general-purpose sparse linear algebra library, mainly PETSc, Hypre, and/or TRILINOS. This might limit numerical robustness and efficiency for specific applications. It in particular eludes to fully exploit the underlying properties of the PDE operator and the numerical discretization at hand to build an optimal solver. In contrast to this approach. **`FEMPAR`’s hallmark is that it has been developed with the aim to provide a framework that will allow researchers to investigate on novel complex computational algorithms that are not well-suited in the traditional segregated workflow commented above, among other advantages**. Even though every block within the library preserves modularity, the interface between discretization and numerical linear algebra modules within `FEMPAR` is very rich and focused on PDE-tailored linear systems.

**`FEMPAR` has been successfully used in 40x JCR Q1-ranked research papers on different topics and application areas**: simulation of turbulent flows and stabilized {{fe}} methods \citep{colomes_assessment_2015,colomes_segregated_2016,colomes_mixed_2016,colomes_segregated_2017}, MHD \citep{badia_analysis_2015, badia_unconditionally_2013, badia_unconditionally_2013-1, planas_approximation_2011, smolentsev_approach_2015}, monotonic {{fes}} \citep{badia_monotonicity-preserving_2017, badia_differentiable_2017, badia_discrete_2015, badia_monotonicity-preserving_2014, hierro_shock_2016,Badia2020euler,Bonilla2019b,Bonilla2020}, unfitted {{fes}} and embedded boundary methods \citep{badia_robust_2017,badia_stokes_2018,badia_aggregated_2017,Verdugo2019b}, {{amr}} \citep{Badia2019a}, AM \citep{Neiva2020,Neiva2019a,chiumenti_numerical_2017} and {{hts}} \citep{Olm2019} simulations, and scientific software engineering \citep{Badia2020fempar,Olm2019b,badia_fempar_2017}. It has also been used for the highly efficient implementation of DD solvers \citep{badia_highly_2014,badia_enhanced_2013,badia_implementation_2013,badia_multilevel_2016,badia_scalability_2015,badia_balancing_2016,badia_space-time_2017,Badia2018pb,Badia2019,Badia2019maxwell} and block preconditioning techniques [badia_block_2014]. Its users/developers span different research groups on national and international-level institutions, including UPC, CIMNE, ICMAB-CSIC, CIEMAT, ICTJA-CSIC, Czech Academy of Sciences (Czech Republic), Sandia National Labs (EEUU), North Carolina State University (USA), Duy Tan University (Vietnam),  Monash University (Australia), and l’Ecole Politechnique (Paris). Besides, it has been/is being a crucial tool for the successful execution of several high-quality EU-funded projects, namely, 1x ERC starting grant, 2x ERC PoC projects, 1x EU-FP7 project, and 3x H2020 projects.

Apart from `FEMPAR`, recently, I have started a new scientific endeavour within the so-called the Gridap ecosystem of Julia packages (available at [https://github.com/gridap](https://github.com/gridap)). At the core of this ecosystem lie the `Gridap.jl` and `GridapEmbedded.jl` Julia packages. `Gridap.jl` is an extensible {{fe}} toolbox fully written in Julia, while  `GridapEmbedded.jl`  extends `Gridap.jl` in order to support embedded {{fe}} discretizations. On top of these two packages,  **I am leading the development of `GridapDistributed.jl`**, which  provides programming paradigm-neutral, parallel {{fe}} data structures for distributed computing environments. This feature implies that communication among tasks are not tailored for a particular programming model, and thus can be leveraged with, e.g., MPI or the master-worker programming model built-in in Julia. Whenever one sticks to MPI as the underlying communication layer,  `GridapDistributed.jl`  leverages the suite of non-linear and linear solvers available in the PETSc software package for the solution of discrete systems of equations. The architecture and API of these packages has been carefully designed in order to achieve a remarkable balance among typically competing constraints, namely generality, flexibility, extensibility, ease-of-use and high performance. To this end, these packages judiciously combine a set of novel features in Julia, namely Just-In-Time (JIT) compilation, dynamic type inference, multiple dispatching, immutable data types, and its powerful abstract interfaces.

In a close link to this RL, **I am co-organizer and co-lecturer (together with my colleagues at NAG, Durham and Cambridge University, UK) of the so-called "Fortran Modernization Workshop" initiative**, a research-oriented workshop, targeting {{cse}}  practitioners and researchers, that encourages, among others, the usage of clean and modern software engineering practices in scientific software. This workshop is free for the attendees, and is funded by NAG (private company) and the UK government. I chaired the instance of the workshop, held at UPC in July, 2017. 70x researchers from different institutions and countries (Spain, Portugal, Germany, USA, and Sweden) attended the workshop. Further instances were held in Cambridge, UK and Germany during 2018-2020.

### Post-doctoral researcher stage 
\label{sec_post_doc}
 This research stage can in turn be split into two separated periods. The first period encompasses the work initiated during a short 6-month post-doc at {{uji}} in the context of the TEXT EU-FP7 project. During this period I initiated a {{ar}} labeled as ''RL5'' below (see Sec.[](#sec_rl5)). The second period, much longer, spans 2011-2015, at Barcelona, Spain, where I developed the bulk of my post-doctoral research career. During this period, I have worked for two different institutions, namely {{cimne}} and {{upc}}. The position at {{upc}} was funded by two competitive post-doctoral research grants I was awarded, by {{upc}} and AGAUR (Generalitat de Catalunya), respectively, with an aggregate amount of 108K€. In collaboration with renowned researchers from these institutions, and other EU and international-level ones, I contributed with success to several topics within the framework of the {{fe}} approximation of large-scale {{pdes}}, towards achieving to a large extent a position of professional maturity and independence. Besides, I have participated as a researcher in several national and high-quality funded EU-level research projects (2x national projects, 1x ERC Starting Grant, and 1x EU-FP7). During this period, I carried out the line labeled as ''RL4'' below (see Sec.[](#sec_rl4)).

#### RL4: Advanced numerical methods for the large-scale simulation of nuclear fusion reactors breeding blankets
\label{sec_rl4}
##### Funding
This {{ar}} is framed within my participation as a researcher in several national and EU level projects: (1) the Spanish MICINN’s CONSOLIDER-TECNOFUS project, in which I worked in collaboration with the Fusion National Laboratory at CIEMAT on the computer simulation of some concepts of {{tbms}}  for the ITER project; (2) the **ERC Starting Grant COMFUS**, to support basic research in the development and mathematical analysis of {{fe}} techniques for Magneto-Hydrodynamics (MHD) and plasma physics simulations, as well as in optimal parallel solvers and {{hpc}} tools for the simulation of realistic fusion technology problems; (3) the Spanish National Plant project FUSSIM, aimed at the development of MHD-magnetic-structure solvers for the accurate structural analysis of the {{bbs}}, and (4) the EU FP7 project NUMEXAS, in which a partnership composed of several EU research-oriented, and private sector institutions (from Spain, Greece, and Germany) focused their joint interdisciplinary efforts towards the next generation of advanced numerical methods and computer codes able to efficiently exploit the intrinsic capabilities of future Exascale computing infrastructures for grand-challenge problems arising in {{cse}}. While performing this research, **my position at {{upc}} was funded by two competitive post-doctoral research grants I was awarded, by {{upc}} and AGAUR (Catalan Government), respectively, with an aggregate amount of 108K€**.


##### Publications
The work I developed as part of this {{ar}} resulted in 7x papers published in Q1-ranked JCR journals \citep{badia_highly_2014,badia_enhanced_2013,badia_implementation_2013,badia_multilevel_2016,Badia2018pb,Badia2019,badia_block_2014} , and 1x paper in a Q3-ranked one  \citep{badia_scalability_2015}.


##### Research line statement and motivation
The ultimate goal of RL4 is the realistic simulation of liquid metals in {{bbs}} that surround the plasma in a nuclear fusion reactor. The {{bb}} is one of the key components in a fusion reactor. It consists of a set of micro-channels filled with a liquid metal (Pb-Li) that acts as a neutron shielding, extracts the energy out of the reactor, and produces and extracts Tritium, needed to maintain the plasma. In the frame of the ITER project (See [https://www.iter.org/](https://www.iter.org/) for more details.), the experimental fusion reactor will not have {{bbs}}, since the ITER reactor will not be a complete fusion reactor. In any case, it will have the so-called {{tbms}} that will be similar to {{bbs}}, and will allow evaluating the feasibility of different {{bb}} concepts. There are many {{tbm}} designs in progress, but it is unclear whether or not the designs studied nowadays will be useful for the development of {{bbs}}. Since the facilities required to carry out experimentation will not be operative in the forthcoming decade, numerical simulation of {{tbms}} is the only way to aid in their design process. The liquid metal flow inside the blanket channels can be modelled through **the thermally-coupled incompressible inductionless {{mhd}} system of PDE equations**. This model describes the dynamics of an electrically conducting fluid under an external electromagnetic field with thermal coupling, where the magnetic field induced by the currents is negligible with respect to the externally applied one. **The numerical {{fe}} solution of these equations is a computationally-demanding task.** Apart from the multi-physics, highly non-linear nature of the system, it involves length and time scales of very different orders of magnitude, leading to truly multi-scale problems. Implicit algorithms are able to obtain meaningful large-scale results without the need to solve for the smallest scales due to stability constraints. However, they require to solve a huge and sparse (non)linear system at every time step, so that massively parallel and scalable algorithms/software as well as the computational power provided by state-of-the-art petascale computers is needed. 

##### Extreme-scale preconditioned iterative linear solvers for one-physics problems
The block recursive LU preconditioners discussed below, at the preconditioner level, the computation of every physical variable in a multi-physics problem. Thus, even though the starting point is a complex multi-physics problem to be solved, the application of the block LU preconditioner only involves the solution of one-physics problems, usually Poisson or CDR-type problems (diagonal blocks). Next, these one-physics problem are replaced, e.g., by a highly scalable parallel solver, in order to end up with a truly scalable {{mhd}} solver. In this context, a remarkable contribution within RL4 is as follows: **I have been able to demonstrate the high-suitability of Multilevel BDDC preconditioners for the efficient/scalable solution of huge sparse linear systems arising from the {{fe}} discretization of linear elliptic {{pdes}} (e.g., Poisson, Elasticity) on current state-of-the-art petascale world-class massively parallel processors.** In order to achieve this goal, **I have proposed a novel bulk-asynchronous, fully-distributed, communicator-aware, inter-level overlapped, and recursive algorithmic adaptation of MultiLevel BDDC preconditioners towards extreme-scale computations** which has been shown to efficiently scale up to the 458K cores of the IBM BG/Q supercomputer installed in JSC, Germany, in the solution of linear elliptic {{pde}} problems with dozens of billions of unknowns; see Fig.[18](#fig_weak_mlbddc). **This work was published in a series of two papers at the SIAM Journal of Scientific Computing~ \citep{badia_highly_2014,badia_multilevel_2016}**. This sort of solvers are not only of paramount importance for large-scale {{mhd}} simulations, but are at the core of many large-scale scientific codes grounded on the {{fe}} solution of {{pde}} problems. Indeed, extreme-scale solvers for sparse linear algebra is a broad and timely subject of strategic importance, as evidenced by the significant increase in investment during the past few years. **Thanks to these outstanding results, `FEMPAR` has been qualified for High-Q club status \citep{brommel_juqueen_2015}, a distinction that JSC (Germany) awards to the most scalable EU codes.**

\label{fig_weak_mlbddc}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/weak_3D_H_div_h_4_3_bddc_ce_tot.pdf-1.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 18: Weak scalability (computation time in seconds) for a 4-level MLBDDC preconditioner in the solution of a Poisson problem up to 20 billion {{dofs}} on 1.8M MPI tasks at the IBM BG/Q supercomputer.*


Within this line of research **I have also contributed to the rehabilitation of the Balancing Neumann-Neumann preconditioner as an efficient preconditioning strategy for large-scale fluid and solid mechanics simulations \citep{badia_enhanced_2013}, and to the scalability boost of inexact BDDC preconditioners \citep{badia_scalability_2015}**. Besides, **I have developed a new variant of BDDC for multi-material problems~\citep{Badia2018pb}**}. The coarse space in this preconditioner, referred as PB-BDDC, is based on a Physics-Based aggregation technique, and unlike BDDC solvers based on adaptive selection of constraints, does not involve expensive eigenvalue solvers. The new preconditioner have been shown to be robust and scalable for materials with heterogeneous properties. Besides, in \citep{Badia2018pb}, it is compared against a state-of-the-art, highly efficient MPI implementation of an adaptive-coarse-space BDDC preconditioner implemented in the PETSc software package from ANL. For the largest-scale problem evaluated (more than a half billion {{dofs}} on 8.2K cores), the new algorithm/software combination is 8x times faster, while consuming significantly less memory resources. Finally, **in \citep{Badia2019}, I have also developed an enhanced variant of the original BDDC preconditioner that is able to eliminate the condition number matrix dependence on the ratio among the subdomain and mesh resolutions.**

##### A novel stabilized FE formulation and block LU preconditioning formulations
The Galerkin {{fe}} approximation of this problem by means of grad-conforming Lagrangian {{fe}} spaces faces several well-known drawbacks. First, convective dominated flows may lead to oscillations because the system loses its elliptic nature. Second, a strong coupling between the two saddle-point subproblems, the hydrodynamic and the magnetic ones, may introduce numerical instabilities when solving the resulting linear systems of equations. Finally, in order to have a well-posed problem, the classical inf-sup conditions between the approximation spaces for the velocity and the pressure must be satisfied. This also applies to the current density and the electric potential as well. There exist several options to circumvent these difficulties, with stabilization methods being one of the most widely used. In order to cope with this problem, **a first remarkable contribution within RL4 comes in the form of a new stabilized, variational multiscale-like {{fe}} scheme tailored for this system of {{pdes}}**; see Fig.[19](#fig_sherc_asgs) for the convergence analysis of the new method for the so-called Shercliff’s benchmark, and [badia_block_2014] for further details. **The most particular feature of these approaches is the current density being treated as an actual unknown of the problem.** This is in contrast to the typical approach based on simplifying the original problem by decoupling the fluid and electromagnetic problems. For large Hartmann numbers (in fusion {{bb}} simulations these are in the order of $10^4$-$10^5$), this latter approach can only work for extremely small time steps, and it cannot be used for steady problems. 

\label{fig_sherc_asgs}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/sherc_asgs_ha10.pdf-1.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 19: Optimal convergence for the $L^2$-norm of the velocity error and its gradient, and the current density error, and its divergence.*


**A remarkable contribution within RL4 comes in the form of algorithmically scalable (i.e., mesh resolution independent) preconditioning algorithms for the discrete operators resulting from these new {{fe}} schemes**. The novel approach that was proposed in order to tackle these highly-coupled, multi-physics problems is based on an approximate block recursive LU factorization of the system matrix. An abstract setting presented in [badia_block_2014] enables the application of this idea to other multi-physics problems like resistive {{mhd}} or liquid crystal problems. For the particular problem at hand, I derived two different preconditioners using this abstract setting. The first preconditioner, the so-called fluid-magnetic subproblem factorization (**FMS preconditioner**) is based on an initial factorization of the system matrix into fluid and magnetic subproblems. The second preconditioner, the so-called Field-Lagrange multiplier factorization (**FLM preconditioner**), segregates at the first level field variables (velocity and current) from Lagrange multiplier-type variables (pressure and electric potential). The key point for these preconditioners to be efficient relies in obtaining a good approximation of the Schur complement for all 2x2 systems. In order to define the Schur complement approximations, I extended the ideas used for the incompressible Navier-Stokes equations to the inductionless {{mhd}} system. The efficiency and robustness of the FMS and FLM block LU recursive preconditioners was confirmed with respect to both mesh size and Hartmann number by means of a detailed set of numerical tests [badia_block_2014].

##### Large-scale TBM simulations

**The combination of all the novel algorithms developed within this RL has enabled large-scale realistic {{bb}} simulations up to scales and (high) Hartmann numbers unprecedented in the computational fusion community.** In particular, the {{hpc}} software tool developed (grounded on `FEMPAR`, see Sec.[](#sec_rl3)), was applied to the {{mhd}} simulation of a dual-coolant liquid metal blanket designed by the Spanish {{bb}} Technology Programme TECNOFUS (details available at [http://fusionwiki.ciemat.es/wiki/TECNO_FUS](http://fusionwiki.ciemat.es/wiki/TECNO_FUS)). The simulation of the TECNOFUS {{tbm}} is a very challenging task due to its extreme physical conditions. As an illustration, the dimensionless numbers corresponding to the physical properties of the fluid (a liquid metal, the alloy Pb-15.7Li) are as high as Reynolds number of and a Hartmann number of. Fig.[20](#fig_tecnofus) shows the fluid velocity streamlines computed by the {{hpc}} simulation tool (at a fixed snapshot in time) for the whole {{tbm}}, and a zoom of those around the turn. This simulation was performed on a 100 million unstructured tetrahedral mesh on 4096 CPU cores of the MN-III supercomputer (at BSC-CNS), with a time step size as large as 0.025 secs.

\label{fig_tecnofus}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/stream1.pdf-1.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/stream2.pdf-1.png" alt="" </img></td>
    </tr>
        <tr>
        <th>(a) Velocity streamlines.</th>
        <th>(b) Zoom of velocity streamlines around the turn.</th>
    </tr> 
</table>
~~~
*Figure 20: Simulation results for the Tecnofus {{tbm}}*


#### RL5: Leveraging novel parallel programming models in legacy parallel scientific software packages
\label{sec_rl5}
##### Funding
This research line was initiated during a short 6-month post-doc position at {{uji}} in the context of the EU-FP7 project *TEXT-Towards EXaflop applicaTions*, with tight collaboration with Profs. Jesús Labarta and Rosa M. Badia (BSC-CNS, Barcelona, Spain), and researchers from other EU partners.

##### Publications
The work developed resulted in 1x paper published in a Q1-ranked JCR journal \citep{martin_leveraging_2014}, and 1x article published in a peer-reviewed book series \citep{BadLMMMQR12}.

##### Research line statement
 The main aim of this {{ar}} was to demonstrate the ability of a novel parallel programming model, based on the many-task asynchronous execution of parallel tasks, namely OMPSs, to leverage the performance and scalability of a set of parallel software packages/libraries judiciously selected by the high impact of the application problems they are able to solve in their respective scientific communities. 


##### Outcomes
**I demonstrated the ability of OMPSs to drastically boost the performance and scalability of ScaLAPACK, the de-facto standard library for dense linear algebra on distributed-memory computers.** Computational kernels in ScaLAPACK are at the core of several fast solver algorithms of paramount importance in {{cse}}, such as sparse direct solvers, domain decomposition or AMG preconditioners, and it is distributed as part of software packages with high impact on the community, such PETSc3 or TRILINOS4 from ANL, and Sandia US national labs, resp. However, ScaLAPACK was developed in the mid 90s, when a single processor (CPU) per node was mainstream, and thus are not well-suited to leverage the intra-node concurrency of as-of-today clusters nodes equipped with multicore technology. **The work opened the door to reusing legacy libraries by introducing up to-date techniques like look-ahead and dynamic out-of-order scheduling that significantly upgrade their performance, while avoiding a costly rewrite/reimplementation.** Fig.[21](#fig_ompss_scalapack) reports the strong scalability (percentage of machine peak performance versus number of cores) of the developed software (blue color), compared to other solutions available at the literature (including ScaLAPACK in red color, and Elemental library in yellow), on a {{hpc}} cluster equipped with 17.7K cores for the computation of a Cholesky factorization of a $n=178,884$ dense matrix.


\label{fig_ompss_scalapack}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/scalapack_ompss.jpg" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 21: Weak/strong scalability of proposed solution (''SMPSs'') compared with other parallel Cholesky codes on a 17.7K CPU cores HPC cluster.*

### Pre-doctoral researcher stage
#### RL6: Task-parallel friendly variants of multilevel preconditioners built from inverse-based ILUs
\label{sec_rl6}
##### Funding
This period started on January, 2006, when I enrolled a PhD program of the {{uji}} at Castellón, Spain, and ended on July, 2010, where I obtained my PhD degree in Computer Science (CS) with honors (Cum Laude) under the supervision of Profs. Enrique S. Quintana-Ortí and José I. Aliaga. **A 4-year competitive FPI fellowship awarded by Generalitat Valenciana funded my PhD. studies**, and let me incorporate to the {{hpc}}\&A research group at {{uji}} where I participated as a researcher in several regional, national, and EU-level competitive projects. **The main {{ar}} was developed in tight collaboration with the group of Prof. Matthias Bollhöfer at TU Braunschweig, Germany.** During this period, I also visited this group 4 times, for a total duration of 4 months. **These research stays were funded by a competitive fellowship that {{uji}} awarded to me, and a project of the “Acciones Integradas” and DAAD subprograms of the Spanish MICINN and the German Science Foundation, respectively.**

##### Publications
This research work that I performed within this {{ar}} has resulted in 2x papers published in Q1-ranked JCR journals \citep{aliaga_exploiting_2011,aliaga_assessing_2014}, 1x chapter at the Encyclopedia of Parallel Computing by Springer \citep{AliBMQ10c}, and 5x articles published in peer-reviewed book series \citep{AliBMQ10,AliBMQ08a,AliDMMQ12,AliBMQ07,AliBMQ09}.

##### Research line statement and motivation
In applications involving the discretization of {{pdes}}, the efficient solution of sparse linear systems is one major computational task. For a large class of application problems, sparse direct solvers have proven to be extremely efﬁcient. However, the enormous size of the underlying applications arising in 3D {{pdes}} requires fast and efﬁcient solution techniques. This in turn demands for alternative approaches and, often, approximate factorization techniques, combined with iterative methods based on Krylov subspaces, reﬂect an attractive alternative for these kind of application problems. With this in mind, **the main {{ar}} developed during my predoctoral research was devoted to the design, development, and {{hpc}} software implementation of novel task-parallel friendly variants (thus amenable for the efficient exploitation of parallel computers) of multilevel preconditioners constructed from inverse-based {{ilus}}.**

#### Research work description, and outcomes
\label{fig_ilupack_pivoting}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/ilupack_pivoting.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 22: Left: ILUPACK pivoting strategy. Right: multilevel preconditioner.*


Multilevel preconditioners constructed from inverse-based {{ilus}} lay the foundations for the software package ILUPACK. ILUPACK is the abbreviation for Incomplete LU factorization PACKage. It is a software library, written in Fortran77 and C, for the iterative solution of large sparse linear systems. **The first release of ILUPACK was launched in 2004 by Prof. Bollhoefer, and was restricted to sequential computers. Since then, it has been improved in a number of ways, including its ability to efficiently exploit parallel computers. This latest feature is the main software outcome of my PhD. thesis**. ILUPACK is mainly built on {{ilus}} applied to the system matrix in conjunction with Krylov subspace methods. **The fundamental difference of ILUPACK is the so-called inverse-based approach.** This approach consists on extracting information from the approximate inverse factors during the incomplete factorization itself in order to improve preconditioner robustness. While this idea has been shown to be successful to satisfy this goal, its downside was initially that the norm of the inverse factors could become large such that small entries could hardly be dropped during Gaussian elimination, resulting in an unacceptable level of fill-in in the resulting preconditioner. To overcome this shortcoming, a multilevel strategy is in charge of limiting the growth of the inverse factors. For example, for preconditioning the conjugate gradient (PCG) method, ILUPACK computes an incomplete factorization $P\approx LDL^T$, where  is $L$ unit lower triangular and entries of small modulus are dropped in the course of the factorization. ILUPACK’s hallmark is to keep $||L ^{-1}||$  below a given bound $\kappa$. To do so, at each step, the factorization of the current row/column is pursued whenever $||L ^{-1}|| \leq \kappa$, or postponed, otherwise, as shown in Fig.[22](#fig_ilupack_pivoting), left. The block of postponed updates $S_C$ (known as Schur complement) becomes the starting matrix of the next level; see [22](#fig_ilupack_pivoting), right. Using this inverse-based strategy and a moderate value of $\kappa$ (e.g. $\kappa=5$) it can be shown that small eigenvalues of $P$ are revealed by $S_C$. Thus,  $S_C$ serves as some kind of coarse-grid system, which resembles those built by {{amg}} preconditioners, in particular, when applied, e.g., to elliptic {{pdes}}.

**The research work carried out was focused on the design, development, and {{hpc}} software implementation of task-parallel friendly variants of the algorithm presented so far.** At this point, it is important to stress that this sort of algorithm does not inherently expose parallelism readily to be exploited. Thus, it had to be transformed towards the achievement of this goal. Parallelism in the computation of approximate factorizations can be exposed by means of graph-based symmetric reordering algorithms. Among this class of algorithms, nested dissection orderings enhance parallelism in the approximate factorization of the linear system coefficient matrix $A$ by partitioning its associated adjacency graph $G(A)$ into a hierarchy of vertex separators and independent subgraphs; see Fig.[23](#fig_nested_dissection). Relabeling the nodes of $G(A)$ according to the levels in the hierarchy, leads to a reordered matrix, $\Phi^T A \Phi$, with a structure amenable to efficient parallelization. This type of parallelism can be expressed by a binary task dependency tree, where nodes represent concurrent tasks and edges dependencies among them. State-of-the-art reordering software packages as, e.g., METIS or SCOTCH, provide fast and efficient multilevel variants of nested dissection orderings.

\label{fig_nested_dissection}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/nested_dissection.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 23: Nested dissection partitioning.*

The dependencies in the task tree are resolved while the computational data and results are generated and passed from the leaves towards the root. The leaves are responsible for approximating the leading diagonal blocks of, while those blocks which will be later factorized by their ancestors are only updated. In other words, ILUPACK pivoting strategy in Fig.[22](#fig_ilupack_pivoting), left, is restricted to the leading diagonal blocks of $\Phi^T A \Phi$, instead of being applied to the whole matrix as in the sequential algorithm. This is the main compromise that it is taken in order to expose concurrent tasks. **The approach proposed leads to an algorithm that exposes a high degree of parallelism, at the price of enforcing a certain order of elimination.** Thus, an important effort of the research work focused on evaluating to what extent the algorithmic variant proposed preserved preconditioning robustness and efficiency. Both set of algorithms were thoroughly compared using metrics such as memory consumption, fill-in ratio in the preconditioner, and number of PCG iterations for a wide range of application problems. **The study revealed that the algorithmic variation introduced has a negligible impact on the numerical properties of the inverse-based preconditioning approach**, in the sense that the convergence rate of the preconditioned iterative method is largely independent on the number of parallel tasks used to decompose the computation.

Apart from the novel algorithm design, **I also developed a parallel multi-threaded software implementation of this algorithm written in C and Fortran77 distributed as part of the ILUPACK software package.** The development of a code in charge of the efficient computation of parallel inverse-based {{ilus}} using sparse matrix data structures (i.e., compress storage formats) is of high complexity, and it requires familiarity with a wide range of low-level code implementation techniques (e.g., manipulation of array-based linked-lists in the presence of pivoting). The target parallel computer architecture of this code is shared-memory and multicore-based parallel computers (equipped with a moderate number of cores, i.e., units/dozens of computational cores). In a nutshell, some of the features of this computer code are: (1) parallel execution of the task tree orchestrated by a runtime which dynamically maps tasks to threads (processors), and that can be thus tuned for a particular target platform and a specific application problem. (2) Application of the preconditioner conformal with the logical structure built during its construction to reduce the number of data transferences (cache misses), and for other major operations in PCG: matrix-vector products, inner products, and vector updates. (3) Use of OpenMP parallel programming to parallelize all stages.

Fig.[](#fig_par_ilupack_perf) shows the performance and scalability of the code developed when applied to the P1 {{fe}} discretization of $-\nabla \cdot (A \nabla u) = f$ in a 3-D domain, where then second-order tensor $A(x,y,z)$ is chosen with positive random coefficients. The domain is a cube with some cylindrical holes inside discretized with tetrahedral meshes of increasingly larger resolution. The size of the systems ranges from n=1.7K to 5.5M of equations/unknowns. Fig.[](#fig_par_ilupack_perf), Left shows its parallel speed-up for 2, 4, 8 and 16 processors on a SGI Altix 350 shared-memory machine. **The speed-up always increases with the number of processors for a fixed problem size, and the parallel efficiency rapidly grows with problem size for a given number of processors.** For the largest problem size, sequential ILUPACK required 736 secs. to solve the linear system, while the parallel variant 44.4 secs on 16 processors. Fig.[](#fig_par_ilupack_perf), Right illustrates the number of PCG iterations required to converge for each linear system considered, as a function of a parameter  which controls the degree of concurrence, i.e., the number of parallel tasks in the task tree. **The number of iterations required to converge is largely independent on the degree of concurrence exposed.**

\label{fig_par_ilupack_perf}
~~~
<table>
    <div style="clear: both"></div>
    <tr>
        <td><img width="100" src="/assets/figures/mic_scal_nd_hamd_b.png" alt="" </img></td>
        <td><img width="100" src="/assets/figures/par_ilupack_iterations.png" alt="" </img></td>
    </tr>
</table>
~~~
*Figure 24: Left: Parallel speed-up. Right: Number of PCG iterations versus degree of concurrence.


## References
@@bibrefs

\biblabel{Badia2018}{1}
1. S. Badia, F. Verdugo, and **A. F. Martín**. The aggregated unfitted finite element method for elliptic problems. *Computer Methods in Applied Mechanics and Engineering*, 336:533–553, 2018. \doi{10.1016/j.cma.2018.03.022}.
\biblabel{burman_cutfem_2015}{2}
2. E. Burman, S. Claus, P. Hansbo, M. G. Larson, and A. Massing. CutFEM: Discretizing Geometry and Partial Differential Equations. *International Journal for Numerical Methods in Engineering*, 104(7):472–501, 2015. \doi{10.1002/nme.4823}.
\biblabel{Schillinger2015}{3}
3. D. Schillinger and M. Ruess. The Finite Cell Method: A Review in the Context of Higher-Order Structural Analysis of CAD and Image-Based Geometric Models. *Archives of Computational Methods in Engineering*, 22(3):391–455, 2015. \doi{10.1007/s11831-014-9115-y}.
\biblabel{Toselli2005}{4}
4. A. Toselli and O. B. Widlund. Domain Decomposition Methods — Algorithms and Theory, volume 34 of Springer Series in Computational Mathematics. Springer Berlin Heidelberg, Berlin, Heidelberg, 2005. \doi{10.1007/b137868}.
\biblabel{Briggs2000}{5}
5. W. L. Briggs, V. E. Henson, and S. F. McCormick. A Multigrid Tutorial, Second Edition. *Society for Industrial and Applied Mathematics*, 2000. \doi{10.1137/1.9780898719505}.
\biblabel{Badia2019a}{6}
6. S. Badia, **A. F. Martín**, E. Neiva, and F. Verdugo. A Generic Finite Element Framework on Parallel Tree-Based Adaptive Meshes. **SIAM Journal on Scientific Computing**, 42(6):C436–C468, 2020. \doi{10.1137/20M1328786}.
\biblabel{Neiva2020}{7}
7. E. Neiva, M. Chiumenti, M. Cervera, E. Salsi, G. Piscopo, S. Badia, **A. F. Martín**, Z. Chen, C. Lee, and C. Davies. Numerical modelling of heat transfer and experimental validation in powder-bed fusion with the virtual domain approximation. *Finite Elements in Analysis and Design*, 168, 2020. \doi{10.1016/j.finel.2019.103343}
\biblabel{badia_stokes_2018}{8}
8. S. Badia, **A. F. Martín** and F. Verdugo. Mixed Aggregated Finite Element Methods for the Unfitted Discretization of the Stokes Problem. *SIAM Journal on Scientific Computing*, 40(6):B1541–B1576, 2018.\doi{10.1137/18M1185624}.
\biblabel{badia_aggregated_2017}{9}
9. S. Badia, F. Verdugo, and **A. F. Martín**. The aggregated unfitted finite element method for elliptic problems. *Computer Methods in Applied Mechanics and Engineering*, 336:533–553, 2018. \doi{10.1016/j.cma.2018.03.022}.
\biblabel{Neiva2019a}{10}
10. E. Neiva, S. Badia, **A. F. Martín**, and M. Chiumenti. A scalable parallel finite element framework for growing geometries. Application to metal additive manufacturing. *International Journal for Numerical Methods in Engineering*, \doi{10.1002/nme.6085}.
\biblabel{Verdugo2019b}{11}
11. F. Verdugo, **A. F. Martín**, and S. Badia. Distributed-memory parallelization of the aggregated unfitted finite element method. *Computer Methods in Applied Mechanics and Engineering*, 357:112583, 2019. \doi{10.1016/j.cma.2019.112583}.
\biblabel{Badia2020}{12}
12. S. Badia, A. F. Martín, E. Neiva, and F. Verdugo. The aggregated unfitted finite element method on parallel tree-based adaptive meshes. 2020.
\biblabel{badia2020robust}{13}
13. S. Badia, M. Caicedo, A. F. Martín, and J. Principe. A robust and scalable unfitted adaptive finite element framework for nonlinear solid mechanics. *Arxiv preprints - 2012.00280*, 2020.
\biblabel{Holke2018}{14}
14. J. Holke. Scalable Algorithms for Parallel Tree-based Adaptive Mesh Refinement with General Element Types. 2018.
\biblabel{burstedde_p4est_2011}{15}
15. C. Burstedde, L. C. Wilcox, and O. Ghattas. p4est: Scalable Algorithms for Parallel Adaptive Mesh Refinement on Forests of Octrees. *SIAM Journal on Scientific Computing*, 33(3):1103–1133, 2011. \doi{10.1137/100791634}.
\biblabel{Isaac2014}{16}
16. T. Isaac, C. Burstedde, L. C. Wilcox, and O. Ghattas. Recursive Algorithms for Distributed Forests of Octrees. *SIAM Journal on Scientific Computing*, 37(5), 2014. \doi{10.1137/140970963}.
\biblabel{Rheinboldt1980}{17}
17. W. C. Rheinboldt and C. K. Mesztenyi. On a Data Structure for Adaptive Finite Element Mesh Refinements. *ACM Transactions on Mathematical Software (TOMS)*, 6(2):166–187, 1980. \doi{10.1145/355887.355891}.
\biblabel{Shephard1984}{18}
18. M. S. Shephard. Linear multipoint constraints applied via transformation as part of a direct stiffness assembly process. *International Journal for Numerical Methods in Engineering*, 20(11):2107–2112, 1984. \doi{10.1002/nme.1620201112}.
\biblabel{Cottrell2009}{19}
19. J. A. Cottrell, T. J. R. Hughes, and Y. Bazilevs. Isogeometric analysis: toward integration of CAD and FEA. Wiley, 2009. \doi{10.1002/9780470749081.ch7}.
\biblabel{chevalier_pt-scotch_2008}{20}
20. C. Chevalier and F. Pellegrini. PT-Scotch: a tool for efficient parallel graph ordering. *Parallel Computing*, 34(6–8):318–331, 2008. \doi{10.1016/j.parco.2007.12.001}.
\biblabel{saad_iterative_2003}{21}
21. Y. Saad. Iterative Methods for Sparse Linear Systems, Second Edition. Society for Industrial and Applied Mathematics, 2 edition, 2003.
\biblabel{Heroux2005}{22}
22. M. A. Heroux, E. T. Phipps, A. G. Salinger, H. K. Thornquist, R. S. Tuminaro, J. M. Willenbring, A. Williams, K. S. Stanley, R. A. Bartlett, V. E. Howle, R. J. Hoekstra, J. J. Hu, T. G. Kolda, R. B. Lehoucq, K. R. Long, and R. P. Pawlowski. An overview of the Trilinos project. *ACM Transactions on Mathematical Software*, 31(3):397–423, 2005. \doi{10.1145/1089014.1089021}.
\biblabel{petsc-user-ref}{23}
23. S. Balay, S. Abhyankar, M. Adams, J. Brown, P. Brune, K. Buschelman, L. Dalcin, A. Dener, V. Eijkhout, W. Gropp, D. Kaushik, M. Knepley, D. May, L. C. McInnes, R. T. Mills, T. Munson, K. Rupp, P. Sanan, B. Smith, S. Zampini, H. Zhang, and H. Zhang. PETSc Users Manual. Technical Report ANL-95/11 - Revision 3.10, Argonne National Laboratory, 2018.
\biblabel{Verdugo2019}{24}
24. F. Verdugo, **A. F. Martín**, and S. Badia. Distributed-memory parallelization of the aggregated unfitted finite element method. Computer Methods in Applied Mechanics and Engineering, 357:112583, 2019. \doi{10.1016/j.cma.2019.112583}.
\biblabel{Badia2019maxwell}{25}
25. S. Badia, **A. F. Martín**, and M. Olm. Scalable solvers for complex electromagnetics problems. *Finite Elements in Analysis and Design*, 161:16–31, 2019. \doi{10.1016/J.FINEL.2019.04.003}.
\biblabel{Olm2019}{26}
26. M. Olm, S. Badia, and **A. F. Martín**. Simulation of High Temperature Superconductors and experimental validation. *Computer Physics Communications*, 237:154–167, 2019. \doi{10.1016/J.CPC.2018.11.021}.
\biblabel{Badia.etal.ACME.2013}{27}
27. S. Badia, **A. F. Martín**, and J. Principe. Implementation and Scalability Analysis of Balancing Domain Decomposition Methods. *Archives of Computational Methods in Engineering*, 20(3):239–262, 2013. \doi{10.1007/s11831-013-9086-4}.
\biblabel{Badia2020fempar}{28}
28. S. Badia and **A. F. Martín**. A tutorial-driven introduction to the parallel finite element library FEMPAR v1.0.0. *Computer Physics Communications*, 248:107059, 2020. \doi{10.1016/j.cpc.2019.107059}
\biblabel{Olm2019b}{29}
29. M. Olm, S. Badia, and **A. F. Martín**. On a general implementation of h- and p-adaptive curl-conforming finite elements. *Advances in Engineering Software*, 132:74–91, 2019. \doi{10.1016/J.ADVENGSOFT.2019.03.006}.
\biblabel{badia_fempar_2017}{30}
30. S. Badia, **A. F. Martín** and J. Principe. FEMPAR: An Object-Oriented Parallel Finite Element Framework. *Archives of Computational Methods in Engineering*, 25(2):195-271, 2018. \doi{10.1007/s11831-017-9244-1}.
\biblabel{colomes_assessment_2015}{31}
31. O. Colomés, S. Badia, R. Codina, and J. Principe. Assessment of variational multiscale models for the large eddy simulation of turbulent incompressible flows. *Computer Methods in Applied Mechanics and Engineering*, 285:32–63, 2015. \doi{10.1016/j.cma.2014.10.041}.
\biblabel{colomes_segregated_2016}{32}
32. O. Colomés and S. Badia. Segregated Runge–Kutta methods for the incompressible Navier–Stokes equations. *International Journal for Numerical Methods in Engineering*, 105(5):372–400, 2016. \doi{10.1002/nme.4987}.
\biblabel{colomes_mixed_2016}{33}
33. O. Colomés, S. Badia, and J. Principe. Mixed finite element methods with convection stabilization for the large eddy simulation of incompressible turbulent flows. *Computer Methods in Applied Mechanics and Engineering*, 304:294–318, 2016. \doi{10.1016/j.cma.2016.02.026}.
\biblabel{colomes_segregated_2017}{34}
34. O. Colomés and S. Badia. Segregated Runge–Kutta time integration of convection-stabilized mixed finite element schemes for wall-unresolved LES of incompressible flows. *Computer Methods in Applied Mechanics and Engineering*, 313:189–215, 2017. \doi{10.1016/j.cma.2016.09.040}.
\biblabel{badia_analysis_2015}{35}
35. S. Badia, R. Codina, and R. Planas. Analysis of an Unconditionally Convergent Stabilized Finite Element Formulation for Incompressible Magnetohydrodynamics. *Archives of Computational Methods in Engineering*, 22(4):621–636, 2015. \doi{10.1007/s11831-014-9129-5}.
\biblabel{badia_unconditionally_2013}{36}
36. S. Badia, R. Codina, and R. Planas. On an unconditionally convergent stabilized finite element approximation of resistive magnetohydrodynamics. *Journal of Computational Physics*, 234(0):399–416, 2013. \doi{10.1016/j.jcp.2012.09.031}.
\biblabel{badia_unconditionally_2013-1}{37}
37. S. Badia, R. Planas, and J. V. Gutiérrez-Santacreu. Unconditionally stable operator splitting algorithms for the incompressible magnetohydrodynamics system discretized by a stabilized finite element formulation based on projections. *International Journal for Numerical Methods in Engineering*, 93(3):302–328, 2013. \doi{10.1002/nme.4392}.
\biblabel{planas_approximation_2011}{38}
38. R. Planas, S. Badia, and R. Codina. Approximation of the inductionless MHD problem using a stabilized finite element method. *Journal of Computational Physics*, 230(8):2977–2996, 2011. \doi{10.1016/j.jcp.2010.12.046}.
\biblabel{smolentsev_approach_2015}{39}
39. S. Smolentsev, S. Badia, R. Bhattacharyay, L. Bühler, L. Chen, Q. Huang, H.-G. Jin, D. Krasnov, D.-W. Lee, E. M. de les Valls, C. Mistrangelo, R. Munipalli, M.-J. Ni, D. Pashkevich, A. Patel, G. Pulugundla, P. Satyamurthy, A. Snegirev, V. Sviridov, P. Swain, T. Zhou, and O. Zikanov. An approach to verification and validation of MHD codes for fusion applications. *Fusion Engineering and Design*, 100:65–72, 2015. \doi{10.1016/j.fusengdes.2014.04.049}.
\biblabel{badia_monotonicity-preserving_2017}{40}
40. S. Badia and J. Bonilla. Monotonicity-preserving finite element schemes based on differentiable nonlinear stabilization. *Computer Methods in Applied Mechanics and Engineering*, 313:133–158, 2017. \doi{10.1016/j.cma.2016.09.035}.
\biblabel{badia_differentiable_2017}{41}
41. S. Badia, J. Bonilla, and A. Hierro. Differentiable monotonicity-preserving schemes for discontinuous Galerkin methods on arbitrary meshes. *Computer Methods in Applied Mechanics and Engineering*, 320:582–605, 2017. \doi{10.1016/j.cma.2017.03.032}.
\biblabel{badia_discrete_2015}{42}
42. S. Badia and A. Hierro. On discrete maximum principles for discontinuous Galerkin methods. *Computer Methods in Applied Mechanics and Engineering*, 286:107–122, 2015. \doi{10.1016/j.cma.2014.12.006}.
\biblabel{badia_monotonicity-preserving_2014}{43}
43. S. Badia and A. Hierro. On Monotonicity-Preserving Stabilized Finite Element Approximations of Transport Problems. *SIAM Journal on Scientific Computing*, 36(6):A2673–A2697, 2014. \doi{10.1137/130927206}.
\biblabel{hierro_shock_2016}{44}
44. A. Hierro, S. Badia, and P. Kus. Shock capturing techniques for -adaptive finite elements. *Computer Methods in Applied Mechanics and Engineering*, 309:532–553, 2016. \doi{10.1016/j.cma.2016.06.017}.
\biblabel{Badia2020euler}{45}
45. S. Badia, J. Bonilla, S. Mabuza, and J. N. Shadid. On differentiable local bounds preserving stabilization for Euler equations. *Computer Methods in Applied Mechanics and Engineering*, 370:113267, 2020. \doi{10.1016/j.cma.2020.113267}.
\biblabel{Bonilla2019b}{46}
46. J. Bonilla and S. Badia. Maximum-principle preserving space–time isogeometric analysis. *Computer Methods in Applied Mechanics and Engineering*, 354:422–440, 2019. \doi{10.1016/J.CMA.2019.05.042}.
\biblabel{Bonilla2020}{47}
47. J. Bonilla and S. Badia. Monotonicity-preserving finite element schemes with adaptive mesh refinement for hyperbolic problems. *Journal of Computational Physics*, 416:109522, 2020. \doi{10.1016/j.jcp.2020.109522}
\biblabel{badia_robust_2017}{48}
48. S. Badia and F. Verdugo. Robust and scalable domain decomposition solvers for unfitted finite element methods. *Journal of Computational and Applied Mathematics*, 2017. \doi{10.1016/j.cam.2017.09.034}.
\biblabel{chiumenti_numerical_2017}{49}
49. M. Chiumenti, E. Neiva, E. Salsi, M. Cervera, S. Badia, J. Moya, Z. Chen, C. Lee, and C. Davies. Numerical modelling and experimental validation in Selective Laser Melting. *Additive Manufacturing*, 18:171–185, 2017. \doi{10.1016/j.addma.2017.09.002}.
\biblabel{badia_highly_2014}{50}
50. S. Badia, A. **F. Martin**, and J. Principe. A Highly Scalable Parallel Implementation of Balancing Domain Decomposition by Constraints.*SIAM Journal on Scientific Computing*, 36(2):C190–C218, 2014. \doi{10.1137/130931989}.
\biblabel{badia_enhanced_2013}{51}
51. S. Badia, **A. F. Martín**, and J. Principe. Enhanced balancing Neumann-Neumann preconditioning in computational fluid and solid mechanics. *International Journal for Numerical Methods in Engineering*, 96(4):203–230, 2013. \doi{10.1002/nme.4541}.
\biblabel{badia_implementation_2013}{52}
52. S. Badia, **A. F. Martín**, and J. Principe. Implementation and scalability analysis of balancing domain decomposition methods. *Archives of Computational Methods in Engineering*, 20(3):239–262, 2013. \doi{10.1007/s11831-013-9086-4}.
\biblabel{badia_multilevel_2016}{53}
53. S. Badia, **A. F. Martín** and J. Principe. Multilevel Balancing Domain Decomposition at Extreme Scales. *SIAM Journal on Scientific Computing*, 38(1):C22-C52, 2016. \doi{10.1137/15M1013511}.
\biblabel{badia_scalability_2015}{54}
54. S. Badia, **A. F. Martín**, and J. Principe. On the scalability of inexact balancing domain decomposition by constraints with overlapped coarse/fine corrections. *Parallel Computing*, 50:1–24, 2015. \doi{10.1016/j.parco.2015.09.004}.
\biblabel{badia_balancing_2016}{55}
55. S. Badia and H. Nguyen. Balancing Domain Decomposition by Constraints and Perturbation.* SIAM Journal on Numerical Analysis*, 54(6):3436–3464, 2016. \doi{10.1137/15M1045648}.
\biblabel{badia_space-time_2017}{56}
56. S. Badia and M. Olm. Space-Time Balancing Domain Decomposition. SIAM Journal on Scientific Computing, 39(2):C194–C213, 2017. \doi{10.1137/16M1074266}.
\biblabel{Badia2018pb}{57}
57. S. Badia, **A. F. Martín**, and H. Nguyen. Physics-Based Balancing Domain Decomposition by Constraints for Multi-Material Problems. *Journal of Scientific Computing*, 79(2):718–747, 2019. \doi{10.1007/s10915-018-0870-z}.
\biblabel{Badia2019}{58}
58. S. Badia, **A. F. Martín**, and H. Nguyen. Balancing domain decomposition by constraints associated with subobjects. *Applied Mathematics Letters*, 87:93–100, 2019. \doi{10.1016/J.AML.2018.07.033}.
\biblabel{brommel_juqueen_2015}{59}
59. Brömmel, B. J. N. Wylie, and W. Frings. JUQUEEN Extreme Scaling Workshop 2015. Technical Report FZJ-2015-01645, FZJ-JSC-IB-2015-01, Jülich Supercomputing Center, 2015.
\biblabel{martin_leveraging_2014}{60}
60. **A. F. Martín**, R. Reyes, R. M. Badia, and E. S. Quintana-Ortí. Leveraging task-parallelism in message-passing dense matrix factorizations using SMPSs. *Parallel Computing*, 40(5-6):113–128, 2014. \doi{10.1016/j.parco.2014.04.001}.
\biblabel{BadLMMMQR12}{61}
61. R. M. Badia, J. Labarta, V. Marjanovic, **A. F. Martín**, R. Mayo, E. S. Quintana-Ortí, and R. Reyes. Symmetric rank-k update on clusters of multicore processors with SMPSs. *Advances in Parallel Computing*, 22:657–664, 2012. \doi{10.3233/978-1-61499-041-3-657}
\biblabel{aliaga_exploiting_2011}{62}
62. J. I. Aliaga, M. Bollhoefer, **A. F. Martín**, and E. S. Quintana-Ortí. Exploiting thread-level parallelism in the iterative solution of sparse linear systems. *Parallel Computing*, 37(3):183–202, 2011. \doi{10.1016/j.parco.2010.11.002}.
\biblabel{aliaga_assessing_2014}{63}
63. J. I. Aliaga, M. Barreda, M. F. Dolz, **A. F. Martín**, R. Mayo, and E. S. Quintana-Ortí. Assessing the impact of the CPU power-saving modes on the task-parallel solution of sparse linear systems. *Cluster Computing*, 17(4):1335–1348, 2014. \doi{10.1007/s10586-014-0402-z}.
\biblabel{AliBMQ10c}{64}
64. XXXX
\biblabel{AliBMQ10}{65}
65. J. I. Aliaga, M. Bollhoefer, **A. F. Martín**, and E. S. Quintana-Ortí. Parallelization of Multilevel ILU Preconditioners on Distributed-Memory Multiprocessors. *Lecture Notes in Computer Science*, 7133:162–172, 2012. \doi{10.1007/978-3-642-28151-8_16}.
\biblabel{AliBMQ10}{65}
65. M. Bollhoefer, J. I. Aliaga, **A. F. Martín**, and E. S. Quintana-Ortí. ILUPACK. In D. A. Padua, editor, Encyclopedia of Parallel Computing, pages 917–926. Springer, 2011.
\biblabel{AliBMQ08a}{66}
66. J. I. Aliaga, M. Bollhoefer, **A. F. Martín**, and E. S. Quintana-Ortí. Design, Tuning and Evaluation of Parallel Multilevel ILU Preconditioners. *Lecture Notes in Computer Science*, 5336:314-327, 2008. \doi{10.1007/978-3-540-92859-1_28}
\biblabel{AliDMMQ12}{67}
67. J. I. Aliaga, M. F. Dolz, **A. F. Martín**, R. Mayo, and E. S. Quintana-Ortí. Leveraring Task-Parallelism in Energy-Efficient ILU Preconditioners. *Lecture Notes in Computer Science*, 7453:55–63, 2012. \doi{10.1007/978-3-642-32606-6_5}
\biblabel{AliBMQ07}{68}
68. J. I. Aliaga, M. Bollhöfer, **A. F. Martín**, and E. S. Quintana-Ortí. Parallelization of Multilevel Preconditioners Constructed from Inverse-Based ILUs on Shared-Memory Multiprocessors. *Advances in Parallel Computing*, 15:287–294, 2008. \doi{10.1007/978-3-642-28151-8}.
\biblabel{AliBMQ09}{69}
69. J. I. Aliaga, M. Bollhoefer, **A. F. Martín**, and E. S. Quintana-Ortí. Evaluation of Parallel Sparse Matrix Partitioning Software for Parallel Multilevel ILU Preconditioning on Shared-Memory Multiprocessors. *Advances in Parallel Computing*, 19:125–132, 2009. \doi{10.3233/978-1-60750-530-3-125}.

<!-- NO REFERENCIADO
\biblabel{badia_block_2014}{42}
[^badia_block_2014] S. Badia, **A. F. Martín**, and R. Planas. Block recursive LU preconditioners for the thermally coupled incompressible inductionless MHD problem. *Journal of Computational Physics*, 274:562-591, 2014. \doi{10.1016/j.jcp.2014.06.028}.

\biblabel{Badia2018a}{Badia2018a}
S. Badia, **A. F. Martín** and F. Verdugo. Mixed Aggregated Finite Element Methods for the Unfitted Discretization of the Stokes Problem. *SIAM Journal on Scientific Computing*, 40(6):B1541–B1576, 2018. \doi{10.1137/18M1185624}.

\biblabel{Baker2011}{Baker2011}
A. H. Baker, M. Schulz, U.M. Yang. On the performance of an algebraic multigrid solver on multicore clusters. *Lecture Notes in Computer Science (including subseries Lecture Notes in Artificial Intelligence and Lecture Notes in Bioinformatics*, 6449 LNCS:102-115, 2011. \doi{10.1007/978-3-642-19328-6_12}.

\biblabel{DePrenter2017}{DePrenter2017}
F. de Prenter, C. V. Verhoosel, G. J. van Zwieten, E. H.van Brummelen. Condition number analysis and preconditioning of the finite cell method. *Computer Methods in Applied Mechanics and Engineering*, 316:297-327, 2017. \doi{10.1016/j.cma.2016.07.006}.

\biblabel{Elman2008}{Elman2008}
H. Elman, V. E. Howle, J. Shadid, R. Shuttleworth, R. Tuminaro. A taxonomy and comparison of parallel block multi-level preconditioners for the incompressible Navier-Stokes equations. *Journal of Computational Physics*, 227(3):1790-1808, 2008. \doi{10.1016/j.jcp.2007.09.026}.

\biblabel{Kohler2017}{Kohler2017}
B. K{\"{o}}hler, S. Born, Roy F.P. van Pelt, A. Hennemuth, U. Preim and B. Preim. A Survey of Cardiac 4D PC-MRI Data Processing. *Computer Graphics Forum*, 36(6):5-35, 2017. \doi{10.1111/cgf.12803}.

\biblabel{menk_robust_2011}{menk_robust_2011}
A. Menk, St{\'{e}}phane P A. Bordas. A robust preconditioning technique for the extended finite element method. *International Journal for Numerical Methods in Engineering*, 85(13):1609-1632, 2011. \doi{10.1002/nme.3032}.

\biblabel{Badia2019-fempar}{Badia2019-fempar}
S. Badia and **A. F. Martín**. A tutorial-driven introduction to the parallel finite element library FEMPAR v1.0.0. *Computer Physics Communications*, 248:107059, 2020. \doi{10.1016/j.cpc.2019.107059}.

\biblabel{heroux_overview_2005}{heroux_overview_2005}
M. A. Heroux, E. T. Phipps, A. G. Salinger, H. K. Thornquist, R. S. Tuminaro, J. M. Willenbring, A. Williams, K. S. Stanley, R. A. Bartlett, V. E. Howle, R. J. Hoekstra, J. J. Hu, T. G. Kolda, R. B. Lehoucq, K. R. Long, and R. P. Pawlowski. An overview of the Trilinos project.
*ACM Transactions on Mathematical Software*, 31(3):397–423, 2005. \doi{10.1145/1089014.1089021}.

\biblabel{Badia2020a}{Badia2020a}
S. Badia and F. Verdugo. Gridap: An extensible Finite Element toolbox in Julia. *Journal of Open Source Software*, 5(52), 2020. \doi{10.21105/joss.02520}.
-->
@@



