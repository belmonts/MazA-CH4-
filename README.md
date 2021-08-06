# MazA-CH4-

I have made this for the sole purpose of having an accesible catalogue of all the possible variations of the code I have been working on for the past two weeks thank you for understanding.

Authors:
  - Alexandra Mazanko
  - Courtney Allen

## Basic Information

To utilize the model user must download the zip file with associated update date, unzip the file and run the following commands in the Julia prompt.

```
julia> include("RPinput[080621].jl")
Main.Rho

julia> include("zodiac[080621].jl")
Main.ChemoSim

julia> u0 = ChemoSim.InitialConditions();

julia> tspan = (0.0,20.0)

julia> sol = ChemoSim.ExampleSol(tspan,u0);

julia> ChemoSim.plot(sol)
```

## Global Sensitivity

To execute global sensitivity analysis, run the following commands:

```
julia> include("GlobeSense[080621].jl")
Main.GlobeSense

julia> num = 50

julia> gsol = GlobeSense.GlobeSenseSol(tspan,u0,num);
```
