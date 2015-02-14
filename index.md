---
layout: media
permalink: /
image:
  feature: "banner.png"

#excerpt: "Be patient - the project is just bootstrapping..."
#title: "Next generation subsurface imaging software"

---

# Description
PRAgMaTIc (Parallel anisotRopic Adaptive Mesh ToolkIt) provides 2D/3D
anisotropic mesh adaptivity for meshes of simplexes. The target
applications are finite element and finite volume methods although
it can also be used as a lossy compression algorithm for 2 and 3D data
(e.g. image compression). It takes as its input the mesh and a metric
tensor field which encodes desired mesh element size
anisotropically.

The toolkit is written in C++ but also provides interfaces for Fortran. It 
has been integrated with [FEniCS/Dolfin](http://fenicsproject.org) and
integration with PETSc/DMPlex is planned.  One of the design goals of PRAgMaTIc
is to develop highly scalable algorithms for clusters of multi-core and
many-core nodes. PRAgMaTIc uses OpenMP for thread parallelism and MPI for
domain decomposition parallelisation.

# Publications
*A thread-parallel algorithm for anisotropic mesh adaptation*
Under review: [arXiv:1308.2480](http://arxiv.org/abs/1308.2480)

*Hybrid OpenMP/MPI anisotropic mesh smoothing*
DOI: [10.1016/j.procs.2012.04.166](http://dx.doi.org/10.1016/j.procs.2012.04.166)

*Accelerating Anisotropic Mesh Adaptivity on nVIDIA's CUDA Using Texture Interpolation*
DOI: [10.1007/978-3-642-23397-5_38](http://dx.doi.org/10.1007/978-3-642-23397-5_38)

# Build
$ cmake .
$ make

# Testing
$ make test

# Install
If you want to install to a specific location then specify the
argument --prefix=/target_location for ./configure. The default
location is /usr/local.

$ make install

