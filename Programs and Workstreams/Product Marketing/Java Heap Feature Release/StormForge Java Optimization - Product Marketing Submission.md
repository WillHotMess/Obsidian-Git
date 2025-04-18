### Feature Name:

Java Heap Optimization

---
### Feature Description:

2-3 sentence summary of the product feature or feature sets

**Problem:** Existing kubernetes right sizing tools only right size at the container level setting requests and limits which simply doesn’t work for java workloads, causing issues with excessive garbage collection or outright OOM kills.  
  
**Solution:** SF java heap optimization goes deeper pulling in java metrics for heap usage, non-heap usage, and garbage collection time so that we can right size the java heap in addition to the container requests and limits.  
  
**Features:**  
- collects java metrics  
- provides heap size recommendations

- can auto-deploy heap size recommendations in tandem with container requests/limits.
    

---
### Timelines & Availability:

Provide rough timelines for availability, noting the sequence of capabilities where applicable

Currently available

---

|     |                        |                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                           |                       |
| --- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
|     | **Feature Attribute**  | **Unique Differentiator**                                                                                                                                                                                                   | **Challenge Solved**                                                                                                                                                                                                                                                                                                                                                                                                                      | **Value to Customer** |
| 1   | Heap Size Right-sizing | In addition to container requests and limits we provide right sizing for java heaps.  <br>  <br>This is something none of our competitors can do and when they try to right size java containers they generally break them. | So many java workloads that right sizing the heap on each one is too much toil. This is the same problem as right sizing requests and limits at scale. It’s just when theres a jvm in the container it adds another dimension of configuration that also needs to be attended to which makes it even harder to manage at scale.  <br>  <br>Cannot use any existing right sizing tools on java workloads because they break the workloads. |                       |
