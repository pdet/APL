# Normalization

Here you can find the papers and a summary of each paper about the normalization part.

## WideTable: An Accelerator for Analytical Data Processing (VLDB 2014)

WideTable is a main memory technique that denormalizes a set of relations into one wide table.
WideTable uses dictionary encoding to avoid space overhead; it also uses columnar storage and SIMD scans (they call packed scan).

The main point of the paper is that denormalization transforms heavy operations, such as
joins, into simple scans. Denormalization was explored by IBM's DB2 (former Blink), where
the biggest conclusion was that while performance for read operations was better, the anomalies
inserted by the denormalization were way too big [this is my conclusion actually].

The paper mentions multiple times that future work is to automatically (re)build the
WideTables based on the workload.

TL;DR: this idea was explored before, the updates are a problem, but at least the (re)build
is not future work. Maybe normalization considering partitions instead of the whole table
could work.
