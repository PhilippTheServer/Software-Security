# Software Security

## Assignments

The assignments work as small CTF challenges. Visit [scoreboard.softsec.rub.de](http://scoreboard.softsec.rub.de) to log in and find the currently available assignments.

There are two types of assignments:
- **Regular assignments**: Standard challenges
- **Checkpoint tasks**: More complex challenges used for grading throughout the semester before the exam

## Checkpoint Tasks

These tasks require programming and potentially reverse engineering to solve. You must submit your code along with the solution.

**Submission requirements:**
- Well-documented code
- Clear and straightforward implementation
- Text explanation of your approach
- Correct flag

All components (code, explanation, and flag) will be considered for grading.

---

## Workflow

1. Download the demo file from the scoreboard
2. Set up the Docker container
3. Analyze and script a solution to capture the flag
4. Request a real instance and test your solution
5. Submit the flag, your code, and a written explanation

## Useful Commands

**Connect to the running Docker container:**
```bash
nc 127.0.0.1 1024
```

**Build the Docker container:**
```bash
docker build -t quiz .
```

**Run the container directly:**
```bash
docker run -p 1024:1024 quiz
```
*Note: Running will automatically build the container if needed.*

---

# Use full stuff

The setup lecture mentioned a python library `pwntools`. Maybe have a look into it later.