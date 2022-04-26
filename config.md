<!--
Add here global page variables to use throughout your website.
-->

@def bibliography = "/assets/bib/refs.bib"

@def agg = "AgFEM"  <!--Aggregated unfitted Finite Element Method-->
@def upc = "UPC"  <!--Technical University of Catalonia-->
@def cimne = "CIMNE"  <!--International Centre for Numerical Methods in Engineering-->
@def lssc = "LSSC"  <!--Large Scale Scientific Computing-->
@def dof = "DOF"  <!--Degree Of Freedom-->
@def dofs = "DOFs"  <!--Degrees Of Freedom-->
@def vef = "VEF"  <!--Vertex, Edge, and Face-->
@def vefs = "VEFs"  <!--Vertices, Edges, and Faces-->
@def sfc = "SFC"  <!--Space-Filling Curve-->
@def sfcs = "SFCs"  <!--Space-Filling Curves-->
@def bddc = "BDDC"  <!--Balancing Domain Decomposition by Constraints-->
@def pcg = "PCG"  <!--Preconditioned Conjugate Gradient-->
@def dg = "DG"  <!--Discontinuous Galerkin-->
@def pi = "PI"  <!--Principal Investigator-->
@def mpi = "MPI"  <!--Message Passing Interface-->
@def cad = "CAD"  <!--Computer Aided Design-->
@def cae = "CAE"  <!--Computer Aided Engineering-->
@def am = "AM"  <!--Additive Manufacturing-->
@def mol = "MOL"  <!--Method of Lines-->
@def pbf = "PBF"  <!--Powder-Bed Fusion-->
@def fe = "FE"  <!--Finite Element-->
@def fem = "FEM"  <!--Finite Element Method-->
@def fes = "FEs"  <!--Finite Elements-->
@def pde = "PDE"  <!--Partial Differential Equation-->
@def pdes = "PDEs"  <!--Partial Differential Equations-->
@def amr = "AMR"  <!--Adaptive Mesh Refinement and coarsening-->
@def hts = "HTS"  <!--High-Temperature Superconductors-->
@def amg = "AMG"  <!--Algebraic MultiGrid-->
@def hpc = "HPC"  <!--High Performance Computing-->
@def oo = "OO"  <!--Object-Oriented-->
@def bddc = "BDDC"  <!--Balancing Domain Decomposition by Constraints-->
@def mpi = "MPI"  <!--Message Passing Interface-->
@def cse = "CSE"  <!--Computational Science \& Engineering-->
@def ilu = "ILU"  <!--Incomplete LU decomposition-->
@def ilus = "ILUs"  <!--Incomplete LU decompositions-->
@def sfc = "SFC"  <!--Space-Filling Curve-->
@def rl = "RL"  <!--Research Line-->
@def rls = "RLs"  <!--Research Lines-->
@def tbm = "TBM"  <!--Test Blanket Module-->
@def tbms = "TBMs"  <!--Test Blanket Module-->
@def bb = "BB"  <!--Breeding Blanket-->
@def bbs = "BBs"  <!--Breeding Blankets-->
@def mhd = "MHD"  <!--Magneto Hydrodynamics-->
@def uji = "UJI"  <!--Jaime I University-->
@def dp = "DP"  <!--Discovery Project-->
@def arc = "ARC"  <!--Australian Research Council-->

@def agg_extended = "Aggregated unfitted Finite Element Method (AgFEM)"
@def upc_extended = "Technical University of Catalonia (UPC)"
@def cimne_extended = "International Centre for Numerical Methods in Engineering (CIMNE)"
@def lssc_extended = "Large Scale Scientific Computing (LSSC)"
@def dof_extended = "Degree Of Freedom (DOF)"
@def dofs_extended = "Degrees Of Freedom (DOFs)"
@def vef_extended = "Vertex, Edge, and Face (VEF)"
@def vefs_extended = "Vertices, Edges, and Faces (VEFs)"
@def sfc_extended = "Space-Filling Curve (SFC)"
@def sfcs_extended = "Space-Filling Curves (SFCs)"
@def bddc_extended = "Balancing Domain Decomposition by Constraints (BDDC)"
@def pcg_extended = "Preconditioned Conjugate Gradient (PCG)"
@def dg_extended = "Discontinuous Galerkin (DG)"
@def pi_extended = "PPrincipal Investigator (PI)"
@def mpi_extended = "Message Passing Interface (MPI)"
@def cad_extended = "Computer Aided Design (CAD)"
@def cae_extended = "Computer Aided Engineering (CAE)"
@def am_extended = "Additive Manufacturing (AM)"
@def mol_extended = "Method of Lines (MOF)"
@def pbf_extended = "Powder-Bed Fusion (PBF)"
@def fe_extended = "Finite Element (FE)"
@def fem_extended = "Finite Element Method (FEM)"
@def fes_extended = "Finite Elements (FEs)"
@def pde_extended = "Partial Differential Equation (PDE)"
@def pdes_extended = "Partial Differential Equations (PDEs)"
@def amr_extended = "Adaptive Mesh Refinement and coarsening (AMR)"
@def hts_extended = "High-Temperature Superconductors (HTS)"
@def amg_extended = "Algebraic MultiGrid (AMG)"
@def hpc_extended = "High Performance Computing (HPC)"
@def oo_extended = "Object-Oriented (OO)"
@def bddc_extended = "Balancing Domain Decomposition by Constraints (BDDC)"
@def mpi_extended = "Message Passing Interface (MPI)"
@def cse_extended = "Computational Science & Engineering (CSE)"
@def ilu_extended = "Incomplete LU decomposition (ILU)"
@def ilus_extended = "Incomplete LU decompositions (ILUs)"
@def sfc_extended = "Space-Filling Curve (SFC)"
@def rl_extended = "Research Line (RL)"
@def tbm_extended = "Test Blanket Module (TBM)"
@def bb_extended = "Breeding Blanket (BB)" 
@def mhd_extended = "Magneto Hydrodynamics (MHD)"  
@def uji_extended = "Jaime I University (UJI)" 
@def dp_extended = "Discovery Project (DP)"
@def arc_extended = "Australian Research Council (ARC)"

+++

author = "Alberto F Martín"
mintoclevel = 2

# Add here files or directories that should be ignored by Franklin, otherwise
# these files might be copied and, if markdown, processed by Franklin which
# you might not want. Indicate directories by ending the name with a `/`.
# Base files such as LICENSE.md and README.md are ignored by default.
ignore = ["node_modules/"]

# RSS (the website_{title, descr, url} must be defined to get RSS)
generate_rss = true
website_title = "Alberto F Martin Website"
website_descr = "Alberto F Martin Website"
website_url   = "https://amartinhuertas.github.io"
+++

<!--
Add here global latex commands to use throughout your pages.
-->
\newcommand{\R}{\mathbb R}
\newcommand{\scal}[1]{\langle #1 \rangle}

\newcommand{\doi}[1]{[DOI:#1](https://dx.doi.org/#1)}
