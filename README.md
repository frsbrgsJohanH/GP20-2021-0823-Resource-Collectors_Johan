# GP20-2021-0823-Resource-Collectors

In this exercise, we will write a small Unity Resource Collector Demo as a base ground for applying Test-Driven-Development.\
In our game, we have one Resource: Wood.\
We can build and upgrade up to 5 Storages.\
Storages grant the following Resource Capacities:\
\[100,200,350,550,800] Wood\
Building/Upgrading Storages costs per level:\
\[100,300,600,1050,1650] Wood\
You start the game with one Storage on Level 1.\
You can collect wood through a button, it yields 500 Wood every time you click it.

In the game, we want to be able to see all relevant information:

<img width="959" alt="Resource collector" src="https://user-images.githubusercontent.com/7360266/130404536-a6ed4a92-d5f6-4ba5-87fc-031c60b65378.png">

## We have the following requirements for the system:
The system is supposed to divide the resources evenly among all storages. It is supposed to aim at having all storages similarly full in percentages. As in: Even if they all have different levels, after I collected wood, they should be similarly full in percent.\
Resources should never be redistributed between Storages, as in you should not go and take 5 wood from storage 1 and put it in storage 2, just to even out the capacities. You can only try evening out the capacities of each storage when:\
Withdrawing Wood (when building or upgrading a storage), by taking Wood from the most filled storages first.\
Depositing Wood (when collecting 100), by putting Wood into the most empty storages first.\
It is a requirement of the system to be deterministic, as in: it needs clear rules to avoid randomness or confusion.\
Assume that there is another team on the other end of the world implementing the server that validates the game in another programming language. That team needs to be able to get exactly the same results as you do on the Unity Client without any numbers being off.

## Your Task:
Try taking notes of all the requirements of the system before implementation.\
Try to think of all edge cases that might happen.\
What behaviour would you expect in these edge cases?\
Hint: There is many edge case behaviours that I have not phrased as requirements in above instructions, yet. You need to notice these and ask me, how the system is supposed to behave in order to be able to implement the algorithm correctly. Make suggestions as to how you would implement these edge cases and I'll let you know how it's supposed to work according to my idea.\
Write Unit Tests for your System before implementing any feature for depositing or withdrawing wood.\
=> Test Driven Development\
How can you make your System easily testable?

## Grading
Grading will be done by seeing, how well your algorithm matches my test cases.
