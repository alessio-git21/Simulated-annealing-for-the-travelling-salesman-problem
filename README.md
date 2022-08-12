# Simulated annealing: the travelling salesman problem
The simulated annealing algorithm is an optimization algorithm. Let's suppose to have a complex cost function you want to minimize with many independent discrete variables. This is not an easy taks and all exact methods known require too much time.
The simulated annealing algorithm is an alternative of these methods and allow us to reach a solution within a reasonable time.
The algorithm is based on statistical mechanics and, indeed, it is a stochastic algorithm. This implies that at the end of the algorithm we can't be sure to have reached the global minimum of the cost function. However it gives very good results in a limited time.

The travelling salesman problem is a typical problem we can solve using the simulated annealing algorithm. The problem is to find the shortest CLOSED path that connects N cities to visit. In this case the cost function is the path lenght and, if N is large, it has a complex shape. As in statistical mechanics we are interested to find the ground state of the system (that is the system with the lower energy), in the travelling salesman problem we want to find the shortest path. So referring to a physical system, the possible paths are the states of the system and the path lenght is the energy of the state.

See the references to better understand the algorithm and the convergence criteria used in this project.

## The project
In this project we choose 100 random cities around the world. You can use the dataset you prefer, you only need to have the coordinates for each cities: [kaggle](https://www.kaggle.com/datasets?search=world+cities+database) offer some of these dataset. Since we are moving on the earth surface, the distance between cities is the geodetic distance. Clearly this code can also be used to found the minimum path in a plane by replacing the geodetic distance with the Euclidean one.

The following figure shows 100 random cities (the black circle) and the shortest path found by the simulated annealing algorithm. Lines between
cities are curved because they represent the geodedic distance (the minimum distance between two points on a spherical surface). Note that the path is closed.

![shortest_path](https://user-images.githubusercontent.com/100300894/184449436-92113081-7e43-4c5b-97a3-336705fee30e.png)


## Packages
* numpy
* cartopy


## References
[Kirkpatrick,Gellat,Vecchi-Optimization by Simulated Annealing-Science,Vol. 220,pp. 671-680](http://wexler.free.fr/library/files/kirkpatrick%20(1983)%20optimization%20by%20simulated%20annealing.pdf)

[Zomaya,Kazman-Simulated Annealing Techniques](https://dl.acm.org/doi/pdf/10.5555/1882757.1882790)

[Eglese-Simulated Annealing: A Tool for Operational Research-European Journal of Operational Research,Vol. 46,pp. 271-281](https://www.sciencedirect.com/science/article/pii/037722179090001R)


## License
[GNU GPLv2](https://choosealicense.com/licenses/gpl-2.0/)
