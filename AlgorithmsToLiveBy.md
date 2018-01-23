# Algorithms to Live by, Tom Griffins and Brian Cristian
## Optimal stopping
- Example: you are interviewing several candidates, if you offer them a job they will surely accept it, but if you discard them they are gone forever
- the problem became famous in the 1950s, by the 1980s it had been developed into a subfield of its own
- you can fail by stopping early or late
    - early: you don't get to see the best applicant
    - late: you hold out for a better applicant, who doesn't exist
- the optimal solution is the **Look-Then-Leap rule**:
    - in a first phase, the Look phase, you discard every applicant
    - then in the leap phase you immediately hire the best-yet candidate, that is a candidate better than all the previous ones
    - if you reach the last candidate you hire hime
- the percentage of applicants to whom it's best to apply the look phase is **37%**
- also the chance to get the best applicant convergest to 37% as the applicant's pool gets larger

### Full information
- the secretary problem assumed that the only metric we had to measure applicants was their relative scores, but what if we have an **absolute metric**, like an SAT exam
- We can use the **threshold rule**: hire a candidate if it has a score higher then $\frac{n}{n+1}\%$ of the people who took the exam, where $n$ is the number of candidates left other than this one.
    - chance of getting the best: **58%**
    - any metric telling us the position of the candidate relative to the population at large can work, not only SAT

### When to sell
- another variation is the problem of selling a house: while you wait for the best offer you have to pay the mortgage
- the math tells us that the only factor involved in choosing the threshold is the relative difference petween the cost of waiting and the range of expected offers
    - it's important to notice that **the threshold doesn't lower as times goes on**, so once it's set trust the math and hold tight

### When to park
- most of parking issues boil down to occupancy rate of the parking lots
- A rise from 90% to 95% accomodates only 5% more people, but doubles the search time
- assume you are on an infinitelylong road with evenly spaced parking spots, you want to minimize the walking time
    - the soluzion is the **Look-Then-Leap rule** 
    - look until $x$ stops from your destination, where $x$ depends on the occupancy rate: 50%-->1 75%-->3, 85%-->5, 95%-->14

### When to quit
- - a burglar can carry out multipe robberies, each with a reward and a chance of success, but if he gets caught he loses all the accumulated gains
- to maximize the gains you should stop after $x$ robberies, where $x=\frac{\text{chance of success}}{\text{chance of failure}}$

### Always be stopping
- research has found that in optimal stopping scenarios **people tend to stop too early**
    - the early stopping can be explained by introducing a waiting cost. E.g. you don't have a secretary, while you keep looking

## Short summary to review
- In an optimal stopping problem use the **Look-then-Leap rule** if you don't have absolute grades (37% success in finding the best candidate), otherwise the **threshold rule**. In this scenarios **people tend to stop early**