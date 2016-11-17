Parallelism

What is Parallelism?
Parallelism is doing multiple tasks at the EXACT same time
It turns programming from executing instructions line by line to executing multiple lines that can be different at the same time.

Things you should not parallelize
Sequential logic
Def test():
	A = 3
	B = a + 32
	C = a + b
There is no speed up if the operations are extremely dependent on previous operations
If the input is small, parallelizing will make it slower!




Things you should parallelize
Things which are independent of each other. 
If the internals of a loop are independent of each iteration then it can be parallelized
Network requests
Database connections
Almost anything that blocks (Waits for a long time before continuing execution)


Parallel Example
def square_very_big_list(list):
For i in range(list):
	List[i] = list[i] * list[i]
Return list
		

Threads
Ever noticed how you can do multiple things at the same time on a computer?
We call those multiple things processes.
Threads are mini processes!
They let you execute multiple lines of code at the same time while sharing variables.

Threading Example



Let’s create 2 threads but call them with different messages.

 
Thread 2 Output

def print_msg(msg)
while True:
print msg
Thread(print_msg(“hello”))
Thread(print_msg(“goodbye”))



Thread 1 Output

Threading Example
Hello
Hello
Hello
Hello



Let’s create 2 threads but call them with different messages.

 
Thread 2 Output

def print_msg(msg)
while True:
print msg
Thread(print_msg(“hello”))
Thread(print_msg(“goodbye”))



Thread 1 Output
Goodbye
Goodbye
Goodbye
Goodbye


Hello
Hello
Goodbye
Hello
Goodbye
Hello
Goodbye
Goodbye
Unified Output
Why is it not consistent?


Hello
Hello
Goodbyte
Hello
Goodbye
Hello
Goodbye
Goodbye
Unified Output
Why is it not consistent?
The threads are executing at the exact same time. But since they are printing to only one screen and your operating system is doing other things in the background, the time they print at varies a tiny bit.



Python Parallelism
Python was not designed for parallelism
Has a global interpreter lock (GIL) hooked into the very base of python
The GIL prevents threads from working well with python




Python Parallelism cont...
Since Python cannot use threads what do we do?
Use processes!
Processes are heavyweight threads!
They are orchestrated in parallel at the OS level, not at the interpreter level
This gets around the GIL
Each process gets a GIL for itself and does not even know its in parallel


Python Parallelism cont...
What do I mean by heavyweight?
Each process has an ENTIRE interpreter loaded
Cannot easily share memory between processes
So we get less parallelism than is possible with other languages


Thread Pools
Threads are cheaper than processes
But they are not free 
Creating new threads and destroying them immediately is wasteful and less efficient
Let’s recycle
Use a couple of threads and when they are done with the work, give them new work


Data races
Thread 1
Total = 0 # This is a global variable
def increment():
	For i in range(10):
		# oldTotal is a local variable 
		oldTotal = Total
		Total = 1 + oldTotal

Thread 2
Total = 0 # This is the same variable as thread 1
def increment():
	For i in range(10):
# This oldTotal is different from thread 1 ‘s old total
		oldTotal = Total
		Total = 1 + oldTotal



Data races result
Total could be any value between 10 and 20!
How?


Data races t = 0
Thread 1
Total = 0
def increment():
	For i in range(10): <-@
		oldTotal = Total
		Total = 1 + oldTotal

Thread 2
Total = 0
def increment():
	For i in range(10):
		oldTotal = Total <-@oldTotal==0
		Total = 1 + oldTotal



Data races t = 1
Thread 1
Total = 0
def increment():
	For i in range(10): 
		oldTotal = Total <-@ oldTotal==0
		Total = 1 + oldTotal

Thread 2
Total = 0
def increment():
	For i in range(10):
		oldTotal = Total
		Total = 1 + oldTotal<-@



Data races t = 2
Thread 1
Total = 0
def increment():
	For i in range(10): 
		oldTotal = Total <-@ oldTotal==0
		Total = 1 + oldTotal

Thread 2
Total = 0
def increment():
	For i in range(10):
		oldTotal = Total
		Total = 1 + oldTotal<-@Total==1



Data races t = 3
Thread 1
Total = 0
def increment():
	For i in range(10): 
		oldTotal = Total 
		Total = 1 + oldTotal <-@ Total==1

Thread 2
Total = 0
def increment():
	For i in range(10):<-@
		oldTotal = Total
		Total = 1 + oldTotal



Data races t = 4
Thread 1
Total = 0
def increment():
	For i in range(10): <-@
		oldTotal = Total 
		Total = 1 + oldTotal 

Thread 2
Total = 0
def increment():
	For i in range(10):
		oldTotal = Total <-@oldTotal == 1 
#BUT IT SHOULD BE 2
		Total = 1 + oldTotal



Data Races
Parallelism can lead to stale values being used to compute new values 
With things executing at the exact same time, programs get really really confusing

Locks
Locks let you designate variables or sections of code as only allowing one thread to use it at a time.
Other threads trying to use the section end up waiting
So locks can be used to fix problems like the incrementing function

Locking Example
Old version
def increment():
	For i in range(10): 
		oldTotal = Total 
		Total = 1 + oldTotal 
		
Locked version
def increment():
	For i in range(10): 
		lock()
		oldTotal = Total 
		Total = 1 + oldTotal 
		unlock()


Problems with locking
As you can probably see, locking slows programs down dramatically
Locks also have problems with threads which are too fast or too slow
If thread 1 is much faster than thread 2, it will always grab the lock
Causes what we call starvation.
Deadlock
Say you need 2 locks, but thread 1 has lock A and thread 2 has lock B
Both threads cannot advance and so all execution stops



Atomicity
What else can we do besides locking?

Atomic Operations
We can make some instructions indivisible
This is locking at the hardware level, so it is cheap compared to software locks
Say we have a increment operator += which is atomic.
No matter what += will get the latest value of whatever, add 1 to it and store it
Total += 1 running in many threads will always work if its atomic


Green Threads
Python shifts the parallelism down the stack to the OS
OS handles switching processes 
You can also do the opposite!
Shift the parallelism up the stack to the interpreter
Threads are typically coordinated between the interpreter and the OS
Make the threads managed by the interpreter


Green Threads
Switching threads now only occurs within the interpreter
No more need to coordinate with the OS
Threads are now really really cheap!
Can have 10000s of threads

Actor Model
Now if threads are cheap like in green threads this lets us create a cool abstraction
Have each object contain an act function, receive message function, and a send message function
All communication now happens through those functions
Each actor’s act function does not share variables with any other actor
We get parallelism without locks or atomicity!! 
(Well almost, locking happens behind the scenes)


Scaling
More cores in CPUs!
GPUs
 

Hyper Scaling
More computers!
Treat each computer as a thread!

Distributed Systems
When you go beyond one computer you hit different problems
The speed of light

