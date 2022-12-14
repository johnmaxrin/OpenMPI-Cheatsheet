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

### Destroy MPI Object
`MPI_Finalize()`
A MPI call can no longer be made after this point.
#

### MPI Broadcast
`int MPI_Bcast(void* buffer, int count, MPI_Datatype datatype, int emitter_rank, MPI_Comm communicator);` <br> <br>
<strong>Buffer: &nbsp;</strong> Contains the value to be broadcasted. <br>
<strong>Count: &nbsp;</strong> Number of elements in the buffer broadcasted. <br>
<strong>Datatype: &nbsp;</strong> Type of the buffer element broadcasted. <br>
<strong>Emitter Rank: &nbsp;</strong> Rank of process which emitt the buffer. <br>
<strong>Communicator: &nbsp;</strong> Communicator in which the broadcast takes palce. <br>

### MPI Scatter
`MPI_Scatter(void* send_data,int send_count,MPI_Datatype send_datatype,void* recv_data,int recv_count,MPI_Datatype recv_datatype,int root,MPI_Comm communicator);
` <br> <br>
<strong>Send Data: &nbsp;</strong> It is an array of data that resides on the root process.<br>
<strong>Send Count: &nbsp;</strong> Number of elements in the array to be sent. <br>
<strong>Send Datatype: &nbsp;</strong> Type of the array element scattered. <br>
<strong>Recv Data: &nbsp;</strong> It is an array of data that each process gets from root process.<br>
<strong>Recv Count: &nbsp;</strong> Number of elements in the array received. <br>
<strong>Recv Datatype: &nbsp;</strong> Type of the array element scattered. <br>
<strong>Root: &nbsp;</strong> Rank of root process. <br>
<strong>Communicator: &nbsp;</strong> Communicator in which the broadcast takes palce. <br>

### MPI Gather 
`MPI_Scatter(void* send_data,int send_count,MPI_Datatype send_datatype,void* recv_data,int recv_count,MPI_Datatype recv_datatype,int root,MPI_Comm communicator);
` <br> <br>
<strong>Send Data: &nbsp;</strong> It is an array of data that resides on the  processes.<br>
<strong>Send Count: &nbsp;</strong> Number of elements in the array to be sent. <br>
<strong>Send Datatype: &nbsp;</strong> Type of the array element Gathered. <br>
<strong>Recv Data: &nbsp;</strong> It is an array of data that root process gets from child process. (All process may sent NULL other than root) <br>
<strong>Recv Count: &nbsp;</strong> Number of elements in the array received. <br>
<strong>Recv Datatype: &nbsp;</strong> Type of the array element scattered. <br>
<strong>Root: &nbsp;</strong> Rank of root process. <br>
<strong>Communicator: &nbsp;</strong> Communicator in which the broadcast takes palce. <br>





### References
[1. MPI Hello World, Wes Kendall](https://mpitutorial.com/tutorials/mpi-hello-world/) <br>
[2. Communicators and Groups](http://www.rc.usf.edu/tutorials/classes/tutorial/mpi/chapter9.html) <br>
[3. About MPI Broadcast](https://rookiehpc.github.io/mpi/docs/mpi_bcast/index.html)
