# Lab 7
## This is my assignment code
### 1.
```python
class stack:
    def __init__(self):
        self.__stk = []

    def push(self, val):
        self.__stk.append(val)

    def pop(self):
        val = self.__stk[-1]
        del self.__stk[-1]
        return val

class CountingStack(stack):
    def __init__(self):
        super().__init__()
        self.__counter = 0

    def get_counter(self):
        return self.__counter

    def pop(self):
        val = super().pop()
        self.__counter += 1
        return val

stk = CountingStack()
for i in range(100):
    stk.push(i)
    stk.pop()
print(stk.get_counter())
```

### 2.
### a.
```python
class QueueError(IndexError):
    pass
class Queue:
    def __init__(self):
        self.__queue = []

    def put(self, elem):
        self.__queue.insert(0, elem)

    def get(self):
        if len(self.__queue) == 0:
            raise QueueError
        return self.__queue.pop()

que = Queue()
que.put(1)
que.put("dog")
que.put(False)
try:
    for i in range(4):
        print(que.get())
except QueueError:
    print("Queue Error")
```

### b.
```python
class QueueError(IndexError):
    pass
class Queue:
    def __init__(self):
        self.__queue = []

    def put(self, elem):
        self.__queue.insert(0, elem)

    def get(self):
        if len(self.__queue) == 0:
            raise QueueError
        return self.__queue.pop(0)

class SuperQueue(Queue):
    def isempty(self):
        return len(self._Queue_queue) == 0

que = SuperQueue()
que.put(1)
que.put("dog")
que.put(False)
for i in range(4):
    if not que.isempty():
        print(que.get())
else:
    print("Queue empty")
```

### 3.
```python
class Timer:
    def __init__(self, hours=0, minutes=0, seconds=0):
        self.__hours = hours
        self.__minutes = minutes
        self.__seconds = seconds
    def __str__(self):
        return f"{self.__hours:02}:{self.__minutes:02}:{self.__seconds:02}"
    def next_second(self):
        self.__seconds += 1
        if self.__seconds == 60:
            self.__seconds = 0
            self.__minutes += 1
        if self.__minutes == 60:
            self.__minutes = 0
            self.__hours += 1
        if self.__hours == 24:
            self.__hours = 0

    def prev_second(self):
        self.__seconds -= 1
        if self.__seconds < 0:
            self.__seconds = 59
            self.__minutes -= 1
        if self.__minutes < 0:
            self.__minutes = 59
            self.__hours -= 1
        if self.__hours < 0:
            self.__hours = 23
timer = Timer(23, 59, 59)
print(timer)
timer.next_second()
print(timer)
timer.prev_second()
print(timer)
```

### 4.
```python
class WeekDayError(Exception):
    pass
class Weeker:
    __days = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
    def __init__(self, day):
        if day not in self.__days:
            raise WeekDayError
        self.__day = day
    def __str__(self):
        return self.__day
    def add__days(self, n):
        idx = self.__day.index(self.__day)
        self.__day = self.__days[(idx + n) % 7]
    def subtract_days(self, n):
        idx = self.__day.index(self.__day)
        self.__day = self.__day[(idx - n) % 7]

weekday = Weeker('Mon')
print(weekday)
weekday.add_days(15)
print(weekday)
weekday.subtract_days(23)
print(weekday)
weekday = Weeker('Monday')
except WeekDayError:
print("Sorry, I can't serve your request.")
```
 ; I was having trouble creating and executing WeekDayError and QueueError
