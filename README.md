# Sofware Security

## Assignments

The assignments work as a kind of small CTF challenges. Therefore go visit [scoreboard.softsec.rub.de](scoreboard.softsec.rub.de). There you can login and find the currently available "assignements"
There are different kind of assignments. Normal ones and *checkpoint tasks*. Last ones are more complex and will be used to grade the student during the semester before the exam. 

## Checkpoint Tasks

Those will need some programming (maybe revers engineering) to solve. The code for those need to be submitted. The code itself needs to be well documentated and straight forward. On the submit window is a select menu to put in the code and a text explanaiton on how the tasks got solved. Both will be used together with the correct flag to grad the student.

---

# Process

First download the demo file from the scoreboard and setup the container. Find out how to get the flag by scripting a solution. After that request a real instance and try your solution. Then submit the flag and a text on how you did it and your code.

Usefull commands:

```bash
nc 127.0.0.1 1024
```
Connect to the running docker container.

```
docker build -t quiz .
```
to build the docker container. Either ways you could also just run in it. It will build on itself.

