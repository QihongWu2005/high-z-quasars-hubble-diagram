This is a Python implementation of using quasars as standard candles described in "Quasars as standard candles III. Validation of a new sample for cosmological studies", A&A 2020. The catalog used in this script is available at http://cdsarc.u-strasbg.fr/viz-bin/cat/J/A+A/642/A150.

Below code is a step-by-step instruction of how researchers establish the hubble diagram for quasars at high redshift:
1. Perform a linear fit on the UV and X-ray flux data to find the log-linear relationship.
This is based on a log-linear relation found between luminosities of X-ray and Ultraviolet. Replacing Luminosity in the equation with expression of flux, we get the log-linear relation of flux that we can perform a linear fit to get the parameters beta and gamma. 

2. Use fitted parameters to calculate luminosity distance $d_L$.
Rearranging the fitted equation of flux X-ray and flux Ultraviolat, we can express luminosity distance as a function of flux X-ray and flux UV.  

3. From $d_L$ calculate distance modulus DM and e_DM.
DM is a distance modulus defined as 5log($d_L$)

4. Plot the Hubble diagram of DM vs. z and fit the diagram with MCMC.
