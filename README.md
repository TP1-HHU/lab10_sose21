# Lab 10
### Advection equation

In this lab we want to study the advection equation
<p align="center">
<img src="stuffy_stuff/f1.png" width="120">
</p>

In particular we are interested in solving the initial value
problem
<p align="center">
<img src="stuffy_stuff/f2.png" width="230">
</p>

* Our first goal is to solve the advection equation for *V*=1 on the domain
[-10,10] up to *tEnd* = 5 by implementing the Upwind method
(see lecture notes).
* This program and many that will follow all need about the same infrastructure.
You get a starter code in this repository, make yourself familiar with it.
See which part of the code is still missing and implement it. Do not change
function interfaces.
* We use *N* = 256 points to discretize the domain spatially.
* Use periodic boundary conditions. This means that the neighbor of u<sub>N-1</sub> is u<sub>0</sub>
  and vice versa.
* Try different ratios *dt/dx*, in particular *dt* = *dx/V*
 (and values slightly larger/smaller than this ratio).
* Plot the evolution of u(x,t), what do you observe for the different ratios?  

After you finished your Upwind project, make a copy of your code and implement
the FTCS method.

What are your observations now?

----
In this project you might want to plot mulitple output files with very similar file names *u_0, u_1,...* at once in gnuplot. There is an easy way to do this: 
```
plot for [i=1:10] 'u_'.i w l title 'u_'.i
```
Another way to look at the data is to generate a short animation in gnuplot via
```
do for [i=0:10] { p "u_".i w l;pause 0.5 }
```
