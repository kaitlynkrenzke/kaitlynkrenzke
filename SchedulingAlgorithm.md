# Python Scheduling Algorithm

## Objective

The objective of this personal project is to demonstrate python coding ability in a simple, effective algorithm. 
 
### Skills Learned


- 

## Code 
```
import schedule
import time

def job():
  print("I'm a scheduled task!")

# Schedule a task to run every minute
schedule.every(1).minutes.do(job)

while True:
  schedule.run_pending()
  time.sleep(1)
```

## Steps

Using schedule library: https://www.geeksforgeeks.org/how-to-implement-interval-scheduling-algorithm-in-python/
Custom scheduling algorithms: Stack Overflow thread with a basic implementation (https://stackoverflow.com/questions/54339470/python-scheduling-algorithm)
drag & drop screenshots here or use imgur and reference them using imgsrc

Every screenshot should have some text explaining what the screenshot is about.

Example below.

*Ref 1: Network Diagram*
