# All about OpenMPI in C++

### Compile MPI Programs 
`mpic++ sourcecode.cpp -o bin_name`
#

### Run MPI Programs
`mpirun -np # ./bin_name` 
#

### Initializing MPI Environment
`MPI_Init(int *argc, char ***argv);   //Parameters are Optional.`
#

### Returning MPI_COMMUNICATOR Size
`MPI_Comm_size(MPI_Comm communicator,int *size)`
###### What is a Communicator in MPI?
It is an object used by the MPI to group those processes which are allowed to communicate with each other. *MPI_COMM_WORLD* is the default communicator which contains all the process.
#



### References
[1. MPI Hello World, Wes Kendall](https://mpitutorial.com/tutorials/mpi-hello-world/) 
[2. Communicators and Groups](http://www.rc.usf.edu/tutorials/classes/tutorial/mpi/chapter9.html)
