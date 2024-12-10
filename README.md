# jeans

A package for calculating properties of (spherical) dark matter halos and embedded (spherical) stellar populations, including integration of the (spherical) Jeans equation.

Author: Matthew G. Walker (2024) 

# Instructions 

* Install jeans. You can either pip install the released version or install from github

```
pip install jeans
```
# Available Dark Matter Halo Models

The alpha/beta/gamma ('abg_triangle') halo has mass density profile $\rho(r)=\frac{\rho_s}{(r/r_s)^{\gamma}[1+(r/r_s)^{\alpha}]^{(\beta-\gamma)/\alpha}}$.

The Navarro-Frenk-White ('nfw') halo is a special case of the above, with $(\alpha,\beta,\gamma)=(1,3,1)$, but can be called directly. 

The Dehnen Cusp ('dehnen_cusp') halo is a special case of the 'abg' halo, with $(\alpha,\beta,\gamma)=(1,4,1)$, but can be called directly.

The Dehnen Core ('dehnen_core') halo is a special case of the 'abg' halo, with $(\alpha,\beta,\gamma)=(1,4,0)$, but can be called directly. 

The core-NFW ('cnfw') halo is by Read et al. (arXiv:1805.06934), defined in terms of the enclosed mass profile, $M_{\rm cNFW}(r)=M_{\rm NFW}(r)f^n$, where $M_{\rm NFW}(r)$ is the enclosed mass profile of the NFW halo and $f^n=[\tanh(r/r_c)]^n$, with $r_c$ a core radius.

The core-NFW-tides ('cnfwt') halo is by Read et al. (arXiv:1805.06934), with density profile $\rho_{\rm cNFWt}(r)=\rho_{\rm cNFW}(r)$ for $r<r_{\rm t}$ and $\rho_{\rm cNFWt}(r)=\rho_{\rm cNFW}(r_{\rm t})(r/r_{\rm t})^{-\delta}$, allowing for power-law decrease in density beyond `tidal' radius $r_{\rm t}$.


# Available Models for Tracer component

The alpha/beta/gamma ('abg') model has number density profile $\nu(r)=\frac{\nu_0}{(r/r_s)^{\gamma}[1+(r/r_s)^{\alpha}]^{(\beta-\gamma)/\alpha}}$.

The Plummer model is a special case of the 'abg' model, with $(\alpha,\beta,\gamma)=(2,5,0).

The 'a2bg' model is a special case of the 'abg' model, with $\alpha=2$.

The exponential model is defined in terms of projected density, $\Sigma(R)=\Sigma_0\exp(-R/R_e)$.




In order to create an object representing an NFW halo with overdensity parameter $\triangle=200$, halo mass given by $M_{\triangle}=1\times 10^{10}M_{\odot}$ and concentration $c_{\triangle}=r_{\triangle}/r_s=10$, where $M_{\triangle}\equiv M(r_{\triangle})$ is the mass enclosed within a sphere of radius $r_{\triangle}$ and the mean halo density within a sphere of radius $r_{\triangle}$ is $\triangle$ times the cosmological critical density given by $3H_0/(8\pi G)$, with $h\equiv H_0/100$ (km/s/Mpc)$^{-1}$:

```dmhalo=jeans.dmhalo('nfw',triangle=200,h=0.7,m_triangle=1.e+10,c_triangle=10)```

# Examples 

For examples of ...

# Acknowledgement

