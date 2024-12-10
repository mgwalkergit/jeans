# jeans

A package for calculating properties of (spherical) dark matter halos and embedded (spherical) stellar populations, including integration of the (spherical) Jeans equation.

Author: Matthew G. Walker (2024) 

# Instructions 

* Install jeans. You can either pip install the released version or install from github

```
pip install jeans
```
# Available Dark Matter Halo Models

The alpha/beta/gamma ('abg') model has density profile $\rho(r)=\frac{\rho_s}{(r/r_s)^{\gamma}[1+(r/r_s)^{\alpha}]^{(\beta-\gamma)/\alpha}}$.

The Navarro-Frenk-White ('nfw') model is a special case of the above, with $(\alpha,\beta,\gamma)=(1,3,1)$.

The core-NFW-tides model is

In order to create an object representing an NFW halo with overdensity parameter $\triangle=200$, halo mass given by $M_{\triangle}=1\times 10^{10}M_{\odot}$ and concentration $c_{\triangle}=r_{\triangle}/r_s=10$, where $M_{\triangle}\equiv M(r_{\triangle})$ is the mass enclosed within a sphere of radius $r_{\triangle}$ and the mean halo density within a sphere of radius $r_{\triangle}$ is $\triangle$ times the cosmological critical density given by $3H_0/(8\pi G)$, with $h\equiv H_0/100$ (km/s/Mpc)$^{-1}$:

```dmhalo=jeans.dmhalo('nfw',triangle=200,m_triangle=1.e+10,c_triangle=10)```

# Examples 

For examples of ...

# Acknowledgement

