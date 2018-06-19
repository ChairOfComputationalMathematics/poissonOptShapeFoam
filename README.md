# Optimal Shape Design for Poisson Equation

We study the shape design problem through the minimization of the cost function

<p align="center">
  <img src="https://latex.codecogs.com/gif.latex?%5Cmathcal%7BJ%7D%20%5Cleft%28%20%5Ctheta%2C%20y%20%5Cright%29%20%3D%20%5Cfrac%7B1%7D%7B2%7D%20%5Cint_%7B%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%7D%20%5Cleft%28%20y%20-%20y_d%20%5Cright%29%20%5E2%20%5C%2C%20%5Cmathrm%7Bd%7D%20%5COmega%2C">
</p>

where <img src="https://latex.codecogs.com/gif.latex?y%20%5Cin%20L%5E2%20%5Cleft%28%20%5COmega%20%5Cright%29"> is the state variable, <img src="https://latex.codecogs.com/gif.latex?y_d%20%5Cin%20L%5E2%20%5Cleft%28%20%5COmega%20%5Cright%29"> is a target function, and <img src="https://latex.codecogs.com/gif.latex?%5Ctheta%20%5Cleft%28%20%5Cmathbf%7Bx%7D%20%5Cright%29"> the normal displacement to a reference boundary,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5CGamma%20%5Cleft%28%20%5Ctheta%20%5Cright%29%20%3D%20%5Cleft%5C%7B%20%5Cmathbf%7Bx%7D%20&plus;%20%5Ctheta%20%5Cleft%28%20%5Cmathbf%7Bx%7D%20%5Cright%29%20%5Cmathbf%7Bn%7D%20%5Cleft%28%20%5Cmathbf%7Bx%7D%20%5Cright%29%20%3A%20%5Cmathbf%7Bx%7D%20%5Cin%20%5CGamma_%7B0%7D%20%5Cright%5C%7D.">
</p>

The problem is subject to the following elliptic PDE in <img src="https://latex.codecogs.com/gif.latex?%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%20%5Csubset%20%5Cmathbb%7BR%7D%5Ed"> with Dirichlet boundary conditions on <img src="https://latex.codecogs.com/gif.latex?%5CGamma%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%20%3D%20%5CGamma_w%20%5Ccup%20%5CGamma_s%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29">,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%5CDelta%20y%20%3D%20f%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%2C%5C%5C%20y%20%3D%20y_%7Bw%7D%20%26%20%5Ctext%7Bin%20%7D%20%5CGamma_w%2C%5C%5C%20y%20%3D%20y_%7Bs%7D%20%26%20%5Ctext%7Bin%20%7D%20%5CGamma_s%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%2C%20%5Cend%7Bcases%7D">
</p>

with <img src="https://latex.codecogs.com/gif.latex?f%20%5Cin%20L%5E2%20%5Cleft%28%20%5COmega%20%5Cright%29">.

We consider the set of admissible domains whose measure is fixed,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cmathcal%7BU%7D_%7Bad%7D%20%3D%20%5Cleft%5C%7B%20%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%20%3A%20%5Clvert%20%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%20%5Crvert%20%3D%20%5COmega_0%20%5Cright%5C%7D%2C">
</p>

and aim at finding the optimal shape that minimizes the cost function. In order to do so, we use the steepest descent method with descent direction given by

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cdelta%20%5Ctheta%20%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%3D%20-%20%5Cleft%5B%20%5Cfrac%7B1%7D%7B2%7D%20%5Cleft%28%20y%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20-%20y_d%20%5Cright%29%20%5E2%20&plus;%20%5Cfrac%7B%5Cpartial%20v%7D%7B%5Cpartial%20n%7D%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%5Cfrac%7B%5Cpartial%20y%7D%7B%5Cpartial%20n%7D%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20&plus;%20q%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%5Cright%5D%2C">
</p>

with <img src="https://latex.codecogs.com/gif.latex?v"> solution of the adjoint problem

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%20%5CDelta%20v%20%3D%20y%20-%20y_d%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%2C%20%5C%5C%20v%20%3D%200%20%26%20%5Ctext%7Bon%20%7D%20%5CGamma%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%20%3D%20%5CGamma_w%20%5Ccup%20%5CGamma_s%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29.%20%5Cend%7Bcases%7D">
</p>

The normal displacement is updated at every iteration,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Ctheta%5E%7B%5Cleft%28%20n%20&plus;%201%20%5Cright%29%7D%20%3D%20%5Ctheta%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20&plus;%20%5Cepsilon%20%5Cdelta%7B%5Ctheta%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%7D%2C">
</p>

with <img src="https://latex.codecogs.com/gif.latex?\epsilon"> sufficiently small. The Lagrange multiplier is computed so that the volume contraint is fulfilled, thus

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?q%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%3D%20-%20%5Cfrac%7B1%7D%7B%5Cleft%7C%5CGamma_s%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%5Cright%7C%7D%20%5Cint_%7B%5CGamma_s%20%5Cleft%28%20%5Ctheta%20%5Cright%20%29%7D%20%5Cleft%5B%20%5Cfrac%7B1%7D%7B2%7D%20%5Cleft%28%20y%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20-%20y_d%20%5Cright%29%20%5E2%20&plus;%20%5Cfrac%7B%5Cpartial%20v%7D%7B%5Cpartial%20n%7D%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%5Cfrac%7B%5Cpartial%20y%7D%7B%5Cpartial%20n%7D%5E%7B%5Cleft%28%20n%20%5Cright%29%7D%20%5Cright%5D%20%5Cmathrm%7Bd%7D%20%5CGamma.">
</p>









, <img src="https://latex.codecogs.com/gif.latex?y"> the state variable and <img src="https://latex.codecogs.com/gif.latex?y_d"> a target function. The minimization problem is subject to the elliptic partial differential equation

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%5CDelta%20y%20%3D%20f%20&plus;%20u%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%2C%20%5C%5C%20y%20%3D%200%20%26%20%5Ctext%7Bon%20%7D%20%5CGamma.%20%5Cend%7Bcases%7D">
</p>

In order to use the conjugate gradient method, the state variable is separated in two terms as

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?y%20%3D%20y_u%20&plus;%20y_%7Bf%7D%2C">
</p>

where <img src="https://latex.codecogs.com/gif.latex?y_u"> solves the state equation with zero Dirichlet boundary conditions,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%5CDelta%20y_u%20%3D%20u%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%2C%20%5C%5C%20y_u%20%3D%200%20%26%20%5Ctext%7Bon%20%7D%20%5CGamma%2C%20%5Cend%7Bcases%7D">
</p>

and <img src="https://latex.codecogs.com/gif.latex?y_f"> is the control-free solution to the state equation,

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%5CDelta%20y_%7Bf%7D%20%3D%20f%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%2C%20%5C%5C%20y_%7Bf%7D%20%3D%200%20%26%20%5Ctext%7Bon%20%7D%20%5CGamma.%20%5Cend%7Bcases%7D">
</p>

With the above separation of the state variable, the cost functional can be expressed as

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cmathcal%7BJ%7D%20%5Cleft%28%20u%20%5Cright%29%20%3D%20%5Cfrac%7B1%7D%7B2%7D%20%5Cleft%28%20y_u%20&plus;%20y_f%20-%20y_d%2C%20y_u%20&plus;%20y_f%20-%20y_d%20%5Cright%29_%7BL%5E2%5Cleft%28%20%5COmega%20%5Cright%29%7D%20&plus;%20%5Cfrac%7B%5Cbeta%7D%7B2%7D%20%5Cleft%28%20u%20%2C%20u%20%5Cright%29%20_%7BL%5E2%5Cleft%28%20%5COmega%20%5Cright%29%7D.">
</p>

We define a linear operator 

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%5CLambda%3A%20L%5E2%5Cleft%28%20%5COmega%20%5Cright%29%20%26%20%5Crightarrow%20L%5E2%5Cleft%28%20%5COmega%20%5Cright%29%20%5C%5C%20u%20%26%20%5Crightarrow%20y_u%20%5Cend%7Balign*%7D2">
</p>

and its adjoint

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%5CLambda%3A%20L%5E2%5Cleft%28%20%5COmega%20%5Cright%29%20%26%20%5Crightarrow%20L%5E2%5Cleft%28%20%5COmega%20%5Cright%29%20%5C%5C%20%5Cphi%20%26%20%5Crightarrow%20%5Clambda%20%5Cend%7Balign*%7D">
</p>

with <img src="https://latex.codecogs.com/gif.latex?\lambda"> solution to

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cbegin%7Bcases%7D%20-%20%5CDelta%20%5Clambda%20%3D%20%5Cphi%20%26%20%5Ctext%7Bin%20%7D%20%5COmega%2C%20%5C%5C%20%5Clambda%20%3D%200%20%26%20%5Ctext%7Bon%20%7D%20%5CGamma.%20%5Cend%7Bcases%7D">
</p>

The directional derivative of the cost function then reads as

<p align="center">
    <img src="https://latex.codecogs.com/gif.latex?%5Cmathcal%7BD%7D_%7B%5Cdelta%20u%7D%20%5Cmathcal%7BJ%7D%5Cleft%28%20u%20%5Cright%29%20%3D%20%5Cleft%28%20%5Cunderbrace%7B%20%5Cleft%28%20%5CLambda%5E*%20%5CLambda%20&plus;%20%5Cbeta%20I%20%5Cright%29%7D_%7BA_%7Bcg%7D%7D%20u%20-%20%5Cunderbrace%7B%20%5CLambda%5E*%20%5Cleft%28%20y_d%20-%20y_f%20%5Cright%29%7D_%7Bb_%7Bcg%7D%7D%2C%20%5Cdelta%20u%20%5Cright%29%20_%7BL%5E2%5Cleft%28%20%5COmega%20%5Cright%29%7D.">
</p>

After having identified <img src="https://latex.codecogs.com/gif.latex?A_%7Bcg%7D"> and <img src="https://latex.codecogs.com/gif.latex?b_%7Bcg%7D"> we can use the conjugate gradient method to reach the optimal control faster. 

## Getting Started

The solver must be compiled in the terminal. It is advisable to first clean previous compilations with

```
wclean
```

and then use

```
wmake
```

### Prerequisites

OpenFOAM C++ library must be installed in order to compile the code.

The OpenFOAM distribution provided by the [OpenFOAM Foundation](https://openfoam.org/) was used.

## Running a Case

In order to run the solver move to the case folder _poissonCGAdjoinFoamCase_ and type in the command line

```
./Allprepare

poissonCGAdjointFoam
```

The _poissonCGAdjointFoam_ solver has been tested in a square domain <img src="https://latex.codecogs.com/gif.latex?%5B0%2C%201%5D%20%5Ctimes%20%5B0%2C%201%5D"> with zero Dirichlet boundary conditions and <img src="https://latex.codecogs.com/gif.latex?%5Cbeta%20%3D%2010%5E%7B-3%7D%2C10%5E%7B-4%7D%2C10%5E%7B-5%7D%2C10%5E%7B-6%7D">. The target function is <img src="https://latex.codecogs.com/gif.latex?y_d%20%3D%20xy%20%5Csin%20%5Cleft%28%20%5Cpi%20x%20%5Cright%29%20%5Csin%20%5Cleft%28%20%5Cpi%20y%20%5Cright%29">.

<p align="center">
  <img src="poissonCGAdjointFoamCase/cg_J.png">
</p>

<p align="center">
  <img src="poissonCGAdjointFoamCase/cg_Jy.png">
</p>

### Warning

It might be needed to use 

```
sed -i -e 's/\r$//' filename
```

and

```
chmod +x filename
```

in order to be able to execute 

```
./filename
```

## Author

* **Jose Lorenzo Gomez**
* **Víctor Hernández-Santamaría**

## Acknowledgments

This project has received funding from the European Research Council (ERC) under the European  Union’s Horizon 2020 research and innovation programme (grant agreement No. 694126-DyCon).
 
[DyCon Webpage](http://cmc.deusto.eus/dycon/)

## References

* F. Tröltzsch. _Optimal control of partial differential equations: theory, methods, and applications_. American Mathematical Soc., 2010.
