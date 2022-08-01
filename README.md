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

### Returning MPI Communicator Size
`MPI_Comm_size(MPI_Comm communicator,int *size)`
###### What is a Communicator in MPI?
It is an object used by the MPI to group those processes which are allowed to communicate with each other. The default communicator is *MPI_COMM_WORLD*, which contains all processes.
#

### Returning the rank of  process in a communicator
`MPI_Comm_ranke(MPI_Comm communicator,int *rank)`
###### What is a Rank?
Each process within a communicator is assigned an incremental rank. Ranks are primarily used during message sending and receiving for identification purposes.
#



### References
[1. MPI Hello World, Wes Kendall](https://mpitutorial.com/tutorials/mpi-hello-world/) <br>
[2. Communicators and Groups](http://www.rc.usf.edu/tutorials/classes/tutorial/mpi/chapter9.html)
