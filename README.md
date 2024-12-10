# jeans

A package for calculating properties of (spherical) dark matter halos and embedded (spherical) stellar populations, including integration of the (spherical) Jeans equation.

Author: Matthew G. Walker (2024) 

# Instructions 

* Install jeans. You can either pip install the released version or install from github

```
pip install jeans
```
# Available Dark Matter Halo Models

The alpha/beta/gamma ('abg') model has density profile $\rho(r)=\frac{\rho_s}{(r/r_s)^{\gamma}[1+(r/r_s)^{\alpha}]^{(\beta-gamma)/\alpha}}

In order to create an object representing an NFW halo with overdensity parameter `triangle', halo mass  :

```dmhalo=jeans.dmhalo('nfw',triangle=200,m_triangle=1.e+10,c_triangle=10)```

# Examples 

For examples of ...

# Acknowledgement

