
# Concurrent Programming in Python

This code demonstrates the use of different programming techniques to perform concurrent execution of a function in Python. The function `cal_average(num)` is used to calculate the average of a given list of numbers. The code demonstrates the use of sequential, asynchronous, threading, and multiprocessing techniques to perform the calculation concurrently.

## Sequential Programming

The `main_sequential(list1, list2, list3)` function uses a list comprehension to calculate the average of each list sequentially. The time taken to perform the calculation is measured using the `time.perf_counter()` function and is printed to the console.

## Asynchronous Programming

The `cal_average_async(num)` function is used to calculate the average of a given list of numbers asynchronously. The function uses the `asyncio.sleep(1)` function to simulate a delay. The `main_async(list1, list2, list3)` function creates a list of tasks that run the `cal_average_async(num)` function for each of the given lists. The `asyncio.gather(*tasks)` function is used to run the tasks concurrently. The time taken to perform the calculation is measured and is printed to the console.

## Threading

The `main_threading(list1, list2, list3)` function creates a list of threads that run the `cal_average(num)` function for each of the given lists. The `Thread` class from the `threading` module is used to create the threads. The `start()` function is used to start the threads and the `join()` function is used to wait for the threads to complete. The time taken to perform the calculation is measured and is printed to the console.

## Multiprocessing

The `main_multiprocessing(list1, list2, list3)` function creates a list of processes that run the `cal_average(num)` function for each of the given lists. The `Process` class from the `multiprocessing` module is used to create the processes. The `start()` function is used to start the processes and the `join()` function is used to wait for the processes to complete. The time taken to perform the calculation is measured and is printed to the console.

## Execution

To run the code, simply call the 

`main_sequential(list1, list2, list3)`, 
`loop.run_until_complete(main_async(list1, list2, list3))`,
`main_threading(list1, list2, list3)`, 
`main_multiprocessing(list1, list2, list3)` 

functions with the desired lists as arguments.

Here is an example of the output:

```Sequential Programming Elapsed Time: 3.0004109139999876 seconds
Asynchronous Programming Elapsed Time: 1.0004109139999876 seconds
Threading Elapsed Time: 1.0004109139999876 seconds
Multiprocessing Elapsed Time: 1.0004109139999876 seconds```

As you can see, the output is similar in all cases, but the time taken to perform the calculation is different. The sequential programming takes the longest time, while the other techniques take less time to complete the