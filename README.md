# OOMMF-temperature
Provides input parameter files (MIF) to include temperature in micromagnetc simulations with the Object Oriented Micromagnetic Framework (OOMMF).

OOMMF can be found under https://math.nist.gov/oommf/

To simulate the movement of the macroscopic magnetic moment in ferromagnetic systems under the influence of elevated
temperatures, the stochastic version of the Landau-Lifshitz (LL) or the Landau-Lifshitz-Gilbert equation with a spin density of
one per unit cell can used. To apply the stochastic LL to micromagnetic simulations, where the spin density per unit cell
is generally higher, a conversion has to be performed. Details can be found in the literature1. Briefly:
To determine the scaling between the physical temperature (T_eff ) and the input parameter used as simulation temperature (T_sim )
the lattice constant (a_eff ) and the length of a elementary simulation cell (a_sim ) has to be set into relation. The temperature T_sim
as used in the simulation as input parameter can be determined from the physical temperature T_eff by:
T_sim =  (a_sim / a_eff) * T_eff 
The range where scaling can be applied one has to consider the temperature effects on the exchange length of the system.1
Cell sizes of 1-2 nm in combination with time steps around 1 fs are a reasonable starting points. Sample files for OMMF are
attached. These files can be used to determine the Curie temperature for the classical bulk magnets, iron, nickel and cobalt.

References
Hahn, M. B. Temperature in micromagnetism: Cell size and scaling effects of the stochastic Landau–Lifshitz equation.
Journal of Physics Communications 3, 075009 (2019). DOI 10.1088/2399-6528/ab31e6.

https://doi.org/10.1088/2399-6528/ab31e6
