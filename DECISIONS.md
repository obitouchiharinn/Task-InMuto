**Architectural Decision Record: Circular Dependency Detection**  
**Context**  

In the Task Management System, there is a possibility for one task to be dependent on another. For example, Task A has to be completed prior to the starting of Task B. The dependencies must always constitute a Directed Acyclic Graph (DAG).  

In a case of a circular dependency, such as A → B → C → A, the system comes to a halt. No task within the loop can be completed as they are all waiting for each other. This situation not only results in a dissatisfied user but also in the corruption of data.  

Thus, the system necessitated a dependable backend mechanism to detect and prevent cycles from being entered.  

**Decision**  

The backend cycle detection was decided to be done by applying a Depth-First Search (DFS) algorithm.  

Even if at the same time there are several updates going on or frontend validations are ignored, the approach still guarantees that creation of dependency that is circular will not happen.  

**Why DFS?**  

DFS is the most applicable and widely used method for finding cycles in a directed graph.  

**How the algorithm works (in our case)**  

As we go along the traversal we check three occurrences:  

- visited: tasks that have gone through the entire process of checking  
- stack (recursion stack): tasks that are presently in the active dependency chain  
- path: the exact number of tasks that are being traversed, which we use to inform the user about the cycle  

The procedure is simple:  

1. Form the dependency graph from the database.  
2. Trigger DFS from the task being updated.  
3. While traversing dependencies:  
   - If we find a task that is currently in the stack then we have a back-edge.  
   - A back-edge means the existence of a cycle.  

As soon as we detect it, we halt the process and return the cycle path.  

DFS brings along two significant advantages:  
- It consistently finds cycles.  
- It presents the opportunity to indicate the specific tasks which are involved.