
# 2020 Plan
## May
### Week 1

- [x] Implement BitVector
- [ ] Run uniform data and workload experiments
    - Finished, 10M rows, 1% sel, 1000 queries
    - Variation: selectivity, number of rows
    
   ```
| 0.001 | 0.01 | 0.1   | 0.5   | 0.9   |
| ----- |:----:| -----:| -----:|------:|
| 100K	|      |       |       |       |
| 1M	|      |       |       |       |
| 10M	|      |       |       |       |
| 100M	|      |       |       |       |
| 1B	|      |       |       |       |
```


- [ ] Run real world experiments (Genome and Power)
    - Quasii is not working, infinite loop or just taking too long.
    - Results are strange, after some queries the selectivity drops to 0.0.
    - Still need to implement the power benchmark.
- [ ] Implement turning off parts of the Cracking KDTree when it reaches the minimum
        partition size

### Week 2

- [ ] Outline methods section
    - At least put the topics of each paragraph.
- [ ] Get workloads from Progressive Index paper
    - Figure 06 from Progressive Indexes: Indexing for Interactive Data Analysis
    - Two dimensions, and color demonstrates the query order.
- [ ] Write Methods section
    - Actually write the methods section, at least my part of it.
- [ ] Write Experiments section
    - Start writing the experiments section, by now the experiments shold all
        be running fine.

### Week 3

- [ ] Write Experiments section
    - Finish experiments section
- [ ] Write Conclusion
- [ ] Write Related Work

### Week 4

- [ ] Write Introduction
- [ ] Write Abstract

## June
### Week 1

- [ ] MDAI paper revision
Multidimensional Paper (Last year dates)
		Abstract submission due: June 8, 2019
		Submission due: June 15, 2019



- [ ] Workshop paper
    - Experimental paper with different methods to scan a table with MultD queries.
    - This comes from the problems we had on this paper trying to figure out the best
        way to do it. Is it using a bitmap with uint64's, or a char bitmap? Or even a
        candidate list? When each is better than the other. For example, on my mac
        a simple array of chars was faster than a fancy uint64 bitvector with bitmagic and
        candidate lists. However, in bricks03 the candidate list was faster than the array
        of chars.

- [ ] CIMPLO stuff

## July
	
## August

- [ ] Start working on adaptive physical layout for joins

## September
## October
- [ ] User Committee meeting
## November
## December
