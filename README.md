# Series Queues with infinite capacity - Open Jackson Network
## Name: Vembarasi.A.R
## Reg no: 212224220120

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory

![image](https://user-images.githubusercontent.com/103921593/203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54.png)


## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203239789-bc870dce-6727-487b-a0e2-4fc3f5114889.png)


## Experiment:
<img width="816" height="505" alt="image" src="https://github.com/user-attachments/assets/d3fcde90-5482-4df1-9bde-598da6e2fb76" />


## Program
```
arr_time = float(input("Enter the mean interarrival time of objects from Feeder (in secs): "))

ser_time1 = float(input("Enter the mean inter service time of Lathe Machine1 (in secs): "))
ser_time2 = float(input("Enter the mean inter service time of Lathe Machine2 (in secs): "))
ser_time3 = float(input("Enter the mean inter service time of Lathe Machine3 (in secs): "))

Robot_time = float(input("Enter the Additional time taken for the Robot (in secs): "))

lam = 1/arr_time

mu1 = 1/(ser_time1+Robot_time)
mu2 = 1/(ser_time2+Robot_time)
mu3 = 1/(ser_time3+Robot_time)

print("-----------------------------------------------------------------------")
print("Series Queues with infinite capacity - Open Jackson Network")
print("-----------------------------------------------------------------------")

if(lam < mu1) and (lam < mu2) and (lam < mu3):

    Ls1 = lam/(mu1-lam)
    Ls2 = lam/(mu2-lam)
    Ls3 = lam/(mu3-lam)

    Ls = Ls1+Ls2+Ls3

    Lq1 = Ls1-lam/mu1
    Lq2 = Ls2-lam/mu2
    Lq3 = Ls3-lam/mu3

    Wq1 = Lq1/lam
    Wq2 = Lq2/lam
    Wq3 = Lq3/lam

    Ws = Ls/(3*lam)

    print("Average number of objects in the system S1: %0.2f"%Ls1)
    print("Average number of objects in the system S2: %0.2f"%Ls2)
    print("Average number of objects in the system S3: %0.2f"%Ls3)

    print("Average number of objects in the overall system : %0.2f"%Ls)

    print("Average number of objects in the conveyor S1 : %0.2f"%Lq1)
    print("Average number of objects in the conveyor S2 : %0.2f"%Lq2)
    print("Average number of objects in the conveyor S3 : %0.2f"%Lq3)

    print("Average waiting time of an object in the conveyor S1: %0.2f secs"%Wq1)
    print("Average waiting time of an object in the conveyor S2: %0.2f secs"%Wq2)
    print("Average waiting time of an object in the conveyor S3: %0.2f secs"%Wq3)

else:
    print("Warning! Objects Over flow will happen in the conveyor")

print("----------------------------------------------------------------------")
```


## Output
<img width="1147" height="526" alt="image" src="https://github.com/user-attachments/assets/93afab78-12e3-47dd-9499-d222ab7a10e1" />


## Result
Thus, the performance measures of the Series Queues with Infinite Capacity – Open Jackson Network were determined successfully using Python. The average number of material in the system and in the conveyor and waiting time are successfully found.
