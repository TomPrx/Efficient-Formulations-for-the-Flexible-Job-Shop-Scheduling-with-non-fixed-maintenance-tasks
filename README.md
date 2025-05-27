# Efficient-Formulations-for-the-Flexible-Job-Shop-Scheduling-with-non-fixed-maintenance-tasks

The set of instances is located at /FJSSPnfa_instances/
The set of original FJSSPinstances is located at /FJSSPinstances/

They are 2010 FJSSP-nfa instances in total. 
For each original FJSSP instance they are 5 FJSSP-nfa instances (nammed _0 to _4)
- Instance _0: multiple maintenance per machine
- Instance _1 to _4 : exactly one maintenance per machine


They format of instances is as follows :
- First line, 3 values : n m a
    - n number of jobs
    - m number of machines
    - a average number of machines per operation
- Line 1 to n : one line per job :
    - first number is the number of operations for the job (j)
    - for each operation 0..j : the next number is the number of machines that can process the first operation (k)
      - for k pairs of numbers 0..k : 2 values
        - machine processing_time
        - machine : the id for the machine
        - processing time : the processing time on the machine
- Line n+1 to n+m: one line per machine
    - first number is the number of maintenance tasks for the machine (l)
    - for each maintenance task 0..l : 3 values
        - duration left right
        - duration : the duration of the maintenance task
        - [left, right] : the time window for the maintenance task



Example: Fattahi1_nfa_0
```
2 2 2.0
2 2 1 25 2 37 2 1 32 2 24 
2 2 1 45 2 65 2 1 21 2 65 
2 16 5 26 14 39 54 
2 11 17 31 15 64 80
```

- First line : 2 jobs 2 machines 2 average machines per operation
- Second line is for 1st job : 2 operations 
  - Operation 1 : 2 compatible machines 
    - machine 1 : 25 processing time
    - machine 2 : 37 processing time
  - Operation 2 : 2 compatible machines 
    - machine 1 : 32 processing time
    - machine 2 : 24 processing time
- Fourth line is for maintenance tasks on machine 1 :
  - 2 maintenance tasks:
    - maintenance task 1 : duration 16, time window [5,26]
    - maintenance task 2 : duration 14, time window [39, 54]
