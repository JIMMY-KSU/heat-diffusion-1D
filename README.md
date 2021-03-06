# Heat-Diffusion-1D
This is a software providing a solution to the heat diffusion in a 1D structure. 

We consider:
* Piecewise homogeneous materials 
* Electron system heating with a Gaussian like source
* Two temperature model: electron & lattice temperature

The equation under consideration is: 

 <img src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/DiffusionEq.png" width="750" height="120" />
 
 where *C* = specific heat, *k* = conductivity, *G* is the coupling constant between the two systems (Electron and Lattice)
  <img src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/phiE.png" width="30" height="20" /> and <img src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/phiL.png" width="30" height="20" /> 
  are the respective temperatures of the electron and the lattice system with respect to space *x* and time *t*. The super letters *L* and *E* indicate wether a parameter belongs to the electron or lattice system and the sub index *i* denotes to which layer the parameter belongs.

 Our approach is to use a combination of **finite elements** (B-Splines) to approximate the derivation in space and **Explicit Euler** to approximate the evolution in time.
 To stay within the **stability** region of the Explicit Euler algorithm, a well suited time step is automatically computed.
 
  ### Example:
  In this case the Material under consideration is one layer of Strontium Ruthenium Oxide and one layer of Strontium Titanium Oxide behind it.
    <p align="center"> 
   <img src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/SROSTO1.PNG" width="520" height="60" />     
   </p>
 The output of the solver is the temperature evolution of the electron and lattice system in space and time.
 
  Temperature evolution of electron- lattice system |  Gaussian laser pulse S(x,t) hitting sample
:-------------------------:|:-------------------------:
 <img src="https://media.giphy.com/media/dIUAz7xfof5N8B8tUy/giphy.gif" width="320" height="300" />  |  <img src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/Source.png" width="320" height="300" />
 
 Here we consider a laser source *S(x,t)* = *lambda* * *exp(-lambda* * *(x-x0))* * *G(t-t0)* hitting a material from the left. I.e. Gaussian shape in time and exponentially decaying in space, according to Lambert-Beer’s law. 
 
We can see the following effects in the animation: 
  1. The electron system immediately gets heated up.
  2. Diffusion of the electron heating along the x-axis
  3. Heat gets transported to the lattice system

#### Documentation
Documentation and example sessions can be found in the [Wiki](https://github.com/udcm-su/heat-diffusion-1D/wiki)

#### With: 
This is a project from the Ultrafast Condensed Matter physics groupe in Stockholm. The main contributors are: 
* [Alber Lukas](https://github.com/luksen99) <img align="right" width="100" height="100" src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/SU.jpg">  <img align="right" width="100" height="100" src="https://github.com/udcm-su/heat-diffusion-1D/blob/Developer/Pictures/UDCM_logo.png">
* [Scalera Valentino](https://github.com/VaSca92) 
* [Vivek Unikandanunni](https://github.com/VivekUUnni)
* [UDCM Group of SU](http://udcm.fysik.su.se/)

#### Dependencies:

[Numpy](http://www.numpy.org/)

[Matplotlib](https://matplotlib.org/)

[B-splines](https://github.com/johntfoster)


#### How to contribute : 
Fork from the `Developer`- branch and pull request to merge back into the original `Developer`- branch. 
Working updates and improvements will then be merged into the `Master` branch, which will always contain the latest working version.
  

       
  

 
