# User Guide

## Features 
Duke is a task management system that helps users to keep track their tasks. The type of tasks that Duke can keep track are todo, event, or deadline. Duke is designed to provide users with the ability to add, delete, and mark tasks as done or not done. In addition, Duke will save a record of the tasks automatically and the tasks will be shown even when it is opened the next time. 

## Features - Accept Upper and Lower Case for commands
Duke commands ignore upper and lower case. Hence, the command will work as long as the word match. 

## ```list``` - List all the tasks out 

By entering the ```list``` command, Duke will print out the list of tasks provided previously, including both done and undone tasks.  

Example 

Command ```list``` 

```
Here are the tasks in your list: 
1. [T][ ]: visit park
2. [D][X]: Submit assignment (by: Monday) 
3. [E][ ]: Project Meeting (at: Tue 1-2pm) 
```

## ```add``` - Add a new task 

The task must be one of these type, ```Todo```, ```Event``` or ```Deadline```. 
- ```Todo```: ```todo {description}```. E.g. ```todo visit park``` will add a new ```Todo``` task with description of ```visit park``` in the list. 
- ```Event```: ```event {descrpition} /at {time}```. For example, ```event meeting /at 2023-02-24``` will add a new ```Event``` with description ```meeting``` at the date specificed as ```Feb 24 2023```; 
- ```Deadline```: ```deadline {description} /by {time}```. For example, ```deadline assignment /by 2023-02-04``` will add a new ```Deadline``` with descripition ```assignemnt``` at the date specified as ```Feb 24 2023```.  

The supported format for the deadline are as followed: 
- 

Else, the date cannot be recognised.


### ```delete``` - Delete a specific task 
By entering the delete command followed by the index, Duke will delete the task.

Example 

Command: ```delete 2``` 

```
Noted, I've removed this task: 
[T][ ]: Visit park
```

### ```Find - Search relevant task in list 

```find {argument}``` will show all the tasks with ```{arugment}``` included in the task description. 

Example 

Command: ```find visit``` 

Assuming this is the list of tasks;

``` 
1.[T][ ] visit park 
2.[T][ ] Watch TV 
3.[T][ ] Visit America 
``` 

The following command will print the following: 

``` 
Here are the tasks related to visit keyword: 
1. [T][ ] visit park 
2. [T][ ] visit america
``` 

### ```mark``` - Mark the task as done  

By inputting ```mark {index} ``` will mark the task at the position as done. 

Example: 

Assuming this is the list of tasks;

``` 
1.[T][ ] visit park 
2.[T][ ] Watch TV 
3.[T][ ] Visit America 


Command: ```mark 1```  

```Nice! I've marked this task as done: 
[T][X] visit park 

### ```unmark``` - Mark the task as not done 

By inputting ```unmark {index} ``` will unmark the task at the position as done. 

Example: 

Assuming this is the list of tasks;

``` 
1.[T][ ] visit park 
2.[T][X] Watch TV 
3.[T][ ] Visit America 


Command: ```unmark 2```  

```Nice! I've marked this task as not done yet: 
[T][ ] Watch TV 

### ```Bye``` - Terminate the program and all tasks in the list will be stored in the duke.txt file in the ```userData``` folder.  

Example 

Command: bye 
``` 
The Duke program will terminate.
```
