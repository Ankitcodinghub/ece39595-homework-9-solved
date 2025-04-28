# ece39595-homework-9-solved
**TO GET THIS SOLUTION VISIT:** [ECE39595 Homework 9 Solved](https://www.ankitcodinghub.com/product/ece39595-homework-9-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;119776&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE39595 Homework 9 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this homework we’ll convert a sequential program to a program that executes items in a work queue in parallel.

What I’ve given you:

In the HW9CPPAssigned directory, in addition to this .pdf you will find a working C++ program. The program has a working quicksort (QuickSort.h and QuickSort.cpp), a main.cpp file, and Command.h file, which will not be used now but will be used in the parallel version.

In main.cpp, NUMSORTS sorts are created, one in each iteration of the loop. The sort is then performed, and the time to execute the sort is printed. There is also a worker( ) function that is commented out but will be used in the parallel version.

In QuickSort, there are two constructors. One creates and initializes an array of the desired number of elements and the other, the zero arg constructor, creates an array of zero elements. The zero arg constructor will be used in the parallel version. The sort( ) function sorts the array, and is basically the entry point to the quick sort routine from outside of the class. quickSort and partition do the sort and partitioning of the data for the sort.

What you need to do:

1. Have the QuickSort function inherit from the Command abstract class, and implement the pure virtual functions declared in Command.

2. Write a DotProduct class that also inherits from the Command abstract class and implements its pure virtual functions. DotProduct will have two constructors, a zero arg and a constructor that takes an int that is the length of the a and b arrays whose dot product will be taken. DotProduct also needs to implement operator&lt;&lt;(…). I’ll include sample output that will make it clear what the output should be.

3. A WorkerQueue class that implements a work queue, where work items are shared_ptr&lt;Command&gt; objects. The queue should be implemented using a C++ std::vector.

In addition to any needed constructors (I used a single zero-arg constructor) you will need to implement a get() function that returns a shared_ptr&lt;Command&gt; of some entry in the queue, and removes that entry from the queue. Removing the entry from the queue should be properly synchronized using a std::mutex and a std::lock_guard.

You will also need to implement a put() function, that takes a std::shared_ptr&lt;Command&gt; as an argument and returns a void, that adds the std::shared_ptr&lt;Command&gt; to the work queue. The add of the shared pointer to the queue should be properly synchronized.

4. In the file main.cpp, the worker function should be uncommented and the write that is done with identify( ) should be called. You should hold a lock different than the lock used for WorkQueue when calling identify so that there is not a race on std::ostream.

In the main function, we will time the time it takes to

a. add eight std::shared_ptr&lt;Command&gt; objects to the work queue. Four will point to dot products and four will point to quick sorts.

b. Start four threads that run the worker function, passing your work queue as an argument.

c. Wait until all four threads have finished.

5. Print out the execution time, the number of threads, etc., as shown in the sample output.

When compiling, use the -pthread option at the end of your list of files or you will get linker errors. You will need the following include files: &lt;vector&gt; for std:vector, &lt;chrono&gt; for timing (you will also need to put “using namespace std:chrono” after the includes and any defines in your main.cpp file), &lt;memory&gt; for std::share_ptr, &lt;mutex&gt; for locks, plus the normal stuff.

What to turn in:

A directory &lt;userid&gt; containing your code. If “g++ *.cpp -pthread” will compile your program, or “g++ std=c11 *.cpp -pthread” will compile your program, no make file is needed. Otherwise include a make file which will build and run your program when “make” is executed.

Points:

Properly synchronized put() using a std::lock_guard: 2 points

Properly synchronized get() using a std::lock_guard: 2 points

Properly synchronized worker(WorkQueue) function using a std::lock_guard: 2 points

Properly starting threads: 1 point

Properly joining threads: 1 point
