# high-z-quasars-hubble-diagram

This is a Python implementation of using quasars as standard candles described in "Quasars as standard candles III. Validation of a new sample for cosmological studies", A&A 2020. The catalog used in this script is available at http://cdsarc.u-strasbg.fr/viz-bin/cat/J/A+A/642/A150.

Below code is a step-by-step instruction of how researchers establish the hubble diagram for quasars at high redshift:
1. Perform a linear fit on the UV and X-ray flux data to find the log-linear relationship.

This is based on a log-linear relation found between luminosities of X-ray and Ultraviolet:

log(Lx)=β+γlog(Luv) 

Replacing Luminosity in the equation with expression of flux, we get the log-linear relation of flux that we can perform a linear fit to get the parameters β and γ:

log(Fx)=Φ(Fuv, $D_L$)=β+(γ−1)log(4π)+γlog(Fuv)+2(γ−1)log($D_L$),



2. Use fitted parameters to calculate luminosity distance $D_L$.

Rearranging the fitted equation of flux X-ray and flux Ultraviolat, we can express luminosity distance as a function of flux X-ray and flux UV.  

log($D_L$)=[1/2(γ−1)][log(Fx)−γlog(Fuv)−β-(γ−1)log(4π)]



3. From $D_L$ calculate distance modulus DM and e_DM.

As hubble law also defines, 

$D_L$=(c/ $H_0$)ln(1+z)

DM is a distance modulus defined as DM=5log[ $D_L$ /(10pc)]. Then, we can get DM as a function of z.



4. Plot the Hubble diagram of DM vs. z and fit the diagram with MCMC.

We applied the fully Bayesian MCMC method to the DL vs. log(1+z) scatter plot using python package emcee. At first, the fitting results were not reliable, but later the problem was solved by employing a Gaussian weight function. The discrepancy between flat ΛCDM model and polynomial expansion at high z indicated in the paper is also reproduced in the hubble diagram.

   
