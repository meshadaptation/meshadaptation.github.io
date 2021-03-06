---
layout: media
permalink: /
image:
  feature: "banner.png"

#excerpt: "Be patient - the project is just bootstrapping..."
#title: "Next generation subsurface imaging software"

---

# Description
[PRAgMaTIc (Parallel anisotRopic Adaptive Mesh
ToolkIt)](https://github.com/meshadaptation/pragmatic) provides 2D/3D
anisotropic mesh adaptivity for meshes of simplexes. The target applications
are finite element and finite volume methods although it can also be used as a
lossy compression algorithm for 2 and 3D data (e.g. image compression). It
takes as its input the mesh and a metric tensor field which encodes desired
mesh element size anisotropically.

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

# Download the source and build
```shell
git clone https://github.com/meshadaptation/pragmatic
mkdir pragmatic-build
cd pragmatic-build
cmake ../pragmatic
make
make test # this may take some time...
```

# Install
If you want to install to a specific location then specify the
argument --prefix=/target_location for ./configure. The default
location is /usr/local.

```shell
make install
```

# Documentation
Source code documentation with [Doxygen](doxygen/index.html).

# Mailing list
You can join the PRAgMaTIc mailing list
[here](https://mailman.ic.ac.uk/mailman/listinfo/pragmatic). For bug reporting
etc please use the [issue tracker on the github
pages](https://github.com/meshadaptation/pragmatic/tree/master).

# License
[BSD 2-Clause "Simplified" or "FreeBSD"
license](https://github.com/meshadaptation/pragmatic/blob/master/LICENSE). See
the [Open Source Initiative](http://opensource.org) for further information
about licenses.
