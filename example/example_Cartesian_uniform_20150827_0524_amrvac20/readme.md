### Purpose and working flow with codes under this path

This path contains the user files for the potential and nonlinear force-free field extrapolation in the Cartesian coordinates with a uniform grid. 

The files have to be used in combination with MPI-AMRVAC version 2.0+ (commit b7e967e), which can be found via [this link](https://github.com/amrvac/amrvac/tree/b7e967ecfbaa027a683fd54525f3a83cd0ad9251).

The usrer files and setups for both the potential field and nonlinear force-free field are provided in the files:
> ./example_Cartesian_uniform_20150827_0524_amrvac20/potential    
> ./example_Cartesian_uniform_20150827_0524_amrvac20/   

respectively. The extrapolations are performed in the following steps:

(1) Go to     
> ./example_Cartesian_uniform_20150827_0524_amrvac20/potential/potential_boundary

Run the read_boundary.pro, which is an IDL procedure. It prepares the boundary conditions 
for the potential field. Note that allboundaries.dat contains the vector magnetic field 
on the photosphere observed by SDO/HMI. It has been processed following the steps detailed 
in [this paper](https://ui.adsabs.harvard.edu/abs/2017ScChD..60.1408G), and has been processed 
by the codes under [this path](https://github.com/njuguoyang/magnetic_modeling_codes/tree/main/example/example_vector_magnetic_field_20150827).

(2) Go to     
> ./example_Cartesian_uniform_20150827_0524_amrvac20/potential

Setup, make, and run amrvac to get the potential field.

(3) Go to     
> ./example_Cartesian_uniform_20150827_0524_amrvac20/nlfff_boundary

Run read_boundary.pro to prepare the boundary condition for the nonlinear force-free 
field extrapolation.

(4) Setup, make, and run amrvac to get the nonlinear force-free field in 
> ./example_Cartesian_uniform_20150827_0524_amrvac20

Note: refer to [amrvac.org](http://amrvac.org) for more information on how to setup, make, and run amrvac.
