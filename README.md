# Party Orb

Solves the guiding centre equations of particle orbit behaviour (including relativistic and non-relativistic versions) based on a specific electromagnetic environment.

## Description

Project based on earlier work carried out by Solar and Magnetospheric Theory Group at University of St Andrews by previous authors. Has been used to study particle behaviour in a range of magnetic and solar-related environments, including magnetic separators, active region simulations, analytical magnetic sturctures, magnetic nulls, collapsing magnetic traps and braking jets. 

## Getting Started

### Dependencies

Requires fortran compilers, MPI installation (only required to read specific data file formats). Tested on Linux and Mac OSX operating systems.

### Installing

To prepare the code for use, type "make" in the root directory.
This creates several additional directories:

./Data/	::	location of output data

./mod/	:: 	location of *.mod files

./obj/	::	location of *.o files

./bin/	::	binary file location

Be careful to use the correct makefile flags, to align correctly with installed fortran compiler. Full details available in the code manual, found in the manual subdirectory (./manual/).

### Executing program

To run the relativistic version of the code, type 
```
./bin/rparty
```
on the command line. 
The nonrelativistic version should run using the command
```
./bin/nrparty
```
(but the non-relativistic version has been depricated, so may contain bugs)

The initial particle conditions are set up in the "newinput.dat" file. The "global_mod.f90" file contains key definitions: the type of field, and location and number of any MHD/code snapshots used as a background field are specified at the beginning of this file. Setting FMOD='test' in this file will run a simple analytical magnetic field model for the particles to act on.

"make clean" removes all these extra directories ready for recompilation.
"make datatidy" deletes all the files in the ./Data/ directory.

Orbit code data was formatted to be read in by IDL. The Start.pro routine will link to many useful IDL functions and codes


## Help

More details on the code structure, makefile contents and algorithms implemented can be found in the manual, or by contacting the code authors.


## Authors
 
*[Dr. James Threlfall](https://www.abertay.ac.uk/staff-search/dr-james-threlfall/) [email](mailto:j.threlfall@abertay.ac.uk)
*[Prof. Thomas Neukirch](https://www.st-andrews.ac.uk/mathematics-statistics/people/tn3/)[email](mailto:tn3@st-andrews.ac.uk)
*[Dr. Alexei Borissov](https://www.epcc.ed.ac.uk/about-us/our-team/alexei-borissov)[email](mailto:a.borissov@epcc.ed.ac.uk)
*Kate Mowbray [email](mailto:jm380@st-andrews.ac.uk)

With credit to earlier work carried out by Dr Solmaz Eradat Oskoui, Dr Keith Grady, Dr Paolo Guiliani, Dr Paul Wood and others.

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Publication List

Selected publications based on/using this code are listed below:
* [Borissov et al. (2020), A&A, 635, 15 p., A63.](https://doi.org/10.1051/0004-6361/201936977)
* [Threlfall et al. (2018) A&A, 611, A40](https://doi.org/10.1051/0004-6361/201731915)
* [Borissov et al. (2017) A&A, 605, A73](http://dx.doi.org/10.1051/0004-6361/201731183)
* [Threlfall et al. (2017) Sol. Phys., 292, 45T](http://dx.doi.org/10.1007/s11207-017-1060-0)
* [Borissov et al. (2016) Sol. Phys., 291, 1385](http://dx.doi.org/10.1007/s11207-016-0915-0)
* [Threlfall et al. (2016b) A&A, 587, A4](http://dx.doi.org/10.1051/0004-6361/201526657)
* [Threlfall et al. (2016a) A&A, 585, A95](http://dx.doi.org/10.1051/0004-6361/201424366)
* [Threlfall et al. (2015) A&A, 574A, 7T](http://dx.doi.org/10.1051/0004-6361/201424366)