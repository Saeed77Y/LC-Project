# Traffic reporting system
Assume that there is a crossing and we want to know how many cars have entered or exited the crossing per minute.
I have designed a logical circuit that can store the amount of incoming and outgoing cars
in the last sixteen minutes up to two hexadecimal digits (or eight bits) and show them to the user; the user can choose
which minute and which one between incoming and outgoing is to be shown.
## Here I explained about project components:
### 60 seconds counter:
![60 seconds counter](https://github.com/Saeed77Y/LC-Project/blob/main/pics/1.png)
This counter counts to 60 (3C in hex) by 1Hz frequency and then resets.
The output which is made with "AND" gates, is 1 when 59 seconds pass in a period (for resetting).
### Incoming and outgoing counters:
![Amount counters](https://github.com/Saeed77Y/LC-Project/blob/main/pics/2.png)
These two counters have the same tasks and the number they show increments after clicking on the logic toggle and resets after 60 seconds.
### Data saver:
![Data saver](https://github.com/Saeed77Y/LC-Project/blob/main/pics/3.png)
This component gets the number of two counters every minute and stores them for up to sixteen minutes; the user can get the data he/she wants by five inputs:
* S3, S2, S1, and S0: these inputs are for determining the minute we want to show in binary form (for example if S3S2S1S0=0101, then output is what was the number of incoming or outgoing in the fifth minute before)
* In/Out: This input determines the amount of incoming or outgoing cars (1 for incoming and 0 for outgoing)
