
<p float="center">
  <p align="center"><img src="https://github.com/koifissh/GeneticAlgoSim/assets/112574689/7bae39a6-2b0e-4c88-b8b8-e039048378f0" width="620" />
</p>

## Genetic Algorithm Program
Author: Daniel Huynh

## Statement
This information can be used to visualize the iterations that a genetic algorithm may go through to optimize for a certain desired trait. In this graph, there were several weights and penalities/rewards that enouraged the behaviour of this algorithm. In each of the 100 generations, there contains a population of 500 randomized variants of schedules that can be a fit. The factors for these schedules were: preferred and non-preferred facilitators, available time, activity, and room. Certain conditions such as consecutive or concurrent loads were penalized. Certain activities had a preference toward preferred facillitators which was rewarded by increasing the fitness/desirability score of the schedule by a certain amount. Mutation, Crossover, Softmax, and Selection functions were involved.

Fitness Function Conditions
-  For each activity, fitness starts at 0.
  > Activity is scheduled at the same time in the same room as another of the activities: -0.5
-  Room size:
  > Activities is in a room too small for its expected enrollment: -0.5
> 
  > Activities is in a room with capacity > 3 times expected enrollment: -0.2
> 
  > Activities is in a room with capacity > 6 times expected enrollment: -0.4
> 
  > Otherwise + 0.3
> 
-  Facilitator:
  > Activities is overseen by a preferred facilitator: + 0.5
> 
  > Activities is overseen by another facilitator listed for that activity: +0.2
> 
  > Activities is overseen by some other facilitator: -0.1
> 
- Facilitator load:
>  Activity facilitator is scheduled for only 1 activity in this time slot: + 0.2
> 
>  Activity facilitator is scheduled for more than one activity at the same time: - 0.2
> 
>  Facilitator is scheduled to oversee more than 4 activities total: -0.5
> 
>  Facilitator is scheduled to oversee 1 or 2 activities*: -0.4
> 
>  *Exception: Dr. Tyler is committee chair and has other demands on his time.
> 
>  *No penalty if he’s only required to oversee < 2 activities.

-  Activity-specific adjustments:
>  The 2 sections of SLA 101 are more than 4 hours apart: + 0.5
> 
>  Both sections of SLA 101 are in the same time slot: -0.5
> 
>  The 2 sections of SLA 191 are more than 4 hours apart: + 0.5
> 
>  Both sections of SLA 191 are in the same time slot: -0.5
> 
>  A section of SLA 191 and a section of SLA 101 are overseen in consecutive time slots (e.g., 10
AM & 11 AM): +0.5
>
> In this case only (consecutive time slots), one of the activities is in Roman or Beach,
and the other isn’t: -0.4
> 
>  A section of SLA 191 and a section of SLA 101 are taught separated by 1 hour (e.g., 10
AM & 12:00 Noon): + 0.25
> 
> A section of SLA 191 and a section of SLA 101 are taught in the same time slot: -0.25

## Usage
To use this program, follow these steps:

1. Ensure that you have the necessary `.pynb` file
2. Run the `AIProgram2.ipynb` file.
3. By running the last part of the program, it will generate the fitness scores of each generation. The best schedule of the last generation along with a visual graph will be printed at the end.
4. To modify certain parameters of this program, you can go into the code and change variables: population, generation, and mutation rate.

## Additional Details
- The program could be expanded with heavier penalties for further schedule optimization.
