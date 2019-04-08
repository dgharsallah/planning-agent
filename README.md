
## Introduction
Planning is an important topic in AI because intelligent agents are expected to automatically plan their own actions in uncertain domains. Planning and scheduling systems are commonly used in automation and logistics operations, robotics and self-driving cars, and for aerospace applications like the Hubble telescope and NASA Mars rovers.

This project is split between implementation and analysis. First you will combine symbolic logic and classical search to implement an agent that performs progression search to solve planning problems. Then you will experiment with different search algorithms and heuristics, and use the results to answer questions about designing planning systems.

Read all of the instructions below and the project rubric [here](https://review.udacity.com/#!/rubrics/1800/view) carefully before starting the project so that you understand the requirements for successfully completing the project. Understanding the project requirements will help you avoid repeating parts of the experiment, some of which can have long runtimes.

**NOTE:** You should read "Artificial Intelligence: A Modern Approach" 3rd edition chapter 10 *or* 2nd edition Chapter 11 on Planning, available [on the AIMA book site](http://aima.cs.berkeley.edu/2nd-ed/newchap11.pdf) before starting this project.

See the [Project Enhancements](#optional-project-enhancements) section at the end for additional notes about limitations of the code in this exercise.

![Progression air cargo search](images/Progression.PNG)


## Getting Started (Workspaces)
The easiest way to complete the project is to click "next" below to open a Workspace that has already been configured with the required files and libraries to support the project. (NOTE: Workspaces does not currently support pypy3, so your code will run slower than completing the project locally if you install pypy3.) 

If you use the Workspace, you do NOT need to perform any of the setup steps outlined below. Skip to the next section with instructions for completing the project.

**NOTE:** Workspace sessions will time out if there is no detected user activity for a period of time (about half an hour). You can lose progress if your session terminates due to timeout while an experiment is running. (Using the mouse to interact in the Workspace window periodically should keep the connection alive.)

## Getting Started (Local Environment)
If you would prefer to complete the exercise in your own local environment, then follow the steps below:

**NOTE:** You are _strongly_ encouraged to install pypy 3.5 (download [here](http://pypy.org/download.html)) for this project. Pypy is an alternative to the standard cPython runtime that tries to optimize and selectively compile your code for improved speed, and it can run 2-10x faster for this project. There are binaries available for Linux, Windows, and OS X. Simply download and run the appropriate pypy binary installer (make sure you get version 3.5) or use the package manager for your OS. When properly installed, any `python` commands can be run with `pypy` instead. (You may need to specify `pypy3` on some OSes.)

- Activate the aind environment (OS X or Unix/Linux users use the command shown; Windows users only run `activate aind`)
```
$ source activate aind
```

## Instructions

  - Run the example problem (this example implements the "have cake" problem from Fig 10.7 of AIMA 3rd edition). The script will print information about the problem domain and solve it with several different search algorithms, however these algorithms cannot solve larger, more complex problems so next you'll have to implement a few more sophisticated heuristics.
```
$ python example_have_cake.py
```

  - Run the search experiment manually (you will be prompted to select problems & search algorithms)
```
$ python run_search.py -m
```

  - You can also run specific problems & search algorithms - e.g., to run breadth first search and UCS on problems 1 and 2:
```
$ python run_search.py -p 1 2 -s 1 2
```


### Additional Search Topics

- Regression search with GraphPlan (ref. [GraphPlan](https://github.com/aimacode/aima-pseudocode/blob/master/md/GraphPlan.md) in the AIMA pseudocode). Regression search can be very fast in some problem domains, but progression search has been more popular in recent years because it is more easily extended to real-world problems, for example to support resource constraints (like planning for battery recharging in mobile robots).

- Progression search with Monte Carlo Tree Search (e.g., ["Using Monte Carlo Tree Search to Solve Planning Problems in Transportation Domains"](https://link.springer.com/chapter/10.1007%2F978-3-642-45111-9_38))
