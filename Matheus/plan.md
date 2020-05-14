
# 2020 Plan
## May
### Week 1

- [x] Implement BitVector
- [x] Run uniform data and workload experiments
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


- [x] Run real world experiments (Genome and Power)
    - Still need to implement the power benchmark.
- [ ] Implement turning off parts of the Cracking KDTree when it reaches the minimum partition size
    - Apparently it did not bring benefits, still need to check it

### Week 2

- [ ] Get workloads from Progressive Index paper
    - Figure 06 from Progressive Indexes: Indexing for Interactive Data Analysis
    - All of them can be used, just need to implement it
    - Two dimensions, and color demonstrates the query order.
- [ ] Write Methods section
    - Write the methods section, at least my part of it.

### Week 3

- [ ] Write methods section
- [ ] Write Experiments section
    - Finish experiments section

### Week 4

- [ ] Write methods section
- [ ] Write Experiments section
    - Finish experiments section

## June
- [ ] MDAI paper revision

- [ ] Multidimensional Paper (Last year dates)
	- Abstract submission due: June 8, 2019
	- Submission due: June 15, 2019

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
- Vacation maybe?
