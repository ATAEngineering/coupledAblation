# Coupled Ablation Module
This module was developed by [ATA Engineering](http://www.ata-e.com) as an 
add-on to the Loci/CHEM computational fluid dynamics (CFD) solver. The module 
can be used to couple Loci/CHEM to the computational structural dynamics (CSD)
solver Abaqus, and the charring ablator response code 
[CHAR](https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20160005889.pdf). 
The module uses CHAR to model surface reactions including ablation. Loci/CHEM 
will morph its mesh to account for the ablating solid's change in shape and 
introduce the off gases at the interface boundary. Loci/CHEM will export the 
surface pressure, heat flux, and species mass fractions present at the surface 
to CHAR for use in the ablation solution. To account for structural effects the 
Simulia Co-Simulation Engine (CSE) can be used to include an Abaqus finite 
element model (FEM) in the analysis. The addition of Abaqus allows for thermal 
expansion and stresses to be modeled within the solid.

# References
[1] Blades, E.L., N.D. Reveles, M. Nucci, and M. MacLean. Simulations of an 
    Eroding Graphite Nozzle via a Fully Coupled Aero-Thermochemical-Elastic 
    Framework. 53rd AIAA/SAE/ASEE Joint Propulsion Conference, Atlanta, GA, July
     2017.  
[2] Reveles, N.D., R.S. Miskovish, and E.L. Blades. A Closely Integrated 
    Fluid/Solid Framework with Chemistry for Hypersonic Ablating Vehicles. 
    National Space and Missile Symposium, Chantilly, VA, 2015.  

# Dependencies
This module depends on both Loci and CHEM being installed. Loci is an open
source framework developed at Mississippi State University (MSU) by Dr. Ed 
Luke. The framework provides a rule-based programming model and can take 
advantage of massively parallel high performance computing systems. CHEM is a 
full featured open source CFD code with finite-rate chemistry built on the Loci 
framework. CHEM is export controlled under the International Traffic In Arms 
Regulations (ITAR). Both Loci and CHEM can be obtained from the 
[SimSys Software Forum](http://www.simcenter.msstate.edu) hosted by MSU.

This module also leverages the CSE and is intended for co-simulation with an 
Abaqus FEM, so licenses for the CSE and Abaqus are required.

This module interacts with NASA's charring ablator response code CHAR, so a
copy of that is required as well. Contact NASA for more information and to 
request a copy.

# Obtaining The Module
The source code for the module is freely available to the US Government under
SBIR data rights. For more information and to request a copy please contact 
mnucci@ata-e.com.