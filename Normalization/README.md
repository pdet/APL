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

## System/U: A Database System Based on the Universal Relation Assumption

The paper talks about a universal table, which would be a VIEW on top of all relations.
Then it proceeds to describe the Data Description Language and the Data Management Language.
It is related to our topic, but they don't physically reorganize things.

## Constant-Time Query Processing

The paper proposes using a single denormalized relation with frequency partitioning and SIMD execution.
Updates on the denormalized relation is considered future work.
This is the original paper for Blink.
They never mention which tables to denormalize. We are interested in how to denormalize and in which tables, the compression and other techniques on top of it are important but not for now.

## Bitwise Dimensional Co-Clustering

TL;DR: space filling curve that uses attributes from different tables to improve join performance. The co-clustering improves data locality.
