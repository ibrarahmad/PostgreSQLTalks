# PostgreSQLTalks
PostgreSQL Conference Talks and Webinar's Presentations.

### 1 - Joining Heterogeneous Databases is a reality, not a Myth, [Presentation][1], [Video][2].
PostgreSQL provides a way to communicate with external data sources. This could be another PostgreSQL instance or any other database. The other database might be a relational database such as Clickhouse, MySQL, or Oracle; or any NoSQL database such as MongoDB or Hadoop. To achieve this, PostgreSQL implements ISO Standard call SQL-MED in the form of Foreign Data Wrappers (FDW). This presentation will explain in detail how PostgreSQL FDWs work. It will include a detailed explanation of simple features and will introduce more advanced features that were added in recent versions of PostgreSQL. Examples of these would be to show how aggregate-pushdown and join-pushdown work in PostgreSQL. The talk will include working examples of these advanced features and demonstrating their use with different databases. These examples show how data from different database flavors can be used by PostgreSQL, including those from heterogeneous relational databases, and showing NoSQL joins.  

### 2 - Tune your Linux Box, not just PostgreSQL, [Presentation][3], [Video][4].
PostgreSQL is one of the leading open-source databases. Out of the box, the default PostgreSQL configuration is not tuned for any particular workload. The default configuration is designed in such a way that PostgreSQL can run on any system using minimum resources. Consequently, a default installation of PostgreSQL does not give optimum performance on the high-performance machine because it is set up to use all available resources.PostgreSQL provides mechanisms that allow you to tune your database according to your workload and machine specification. Outside of PostgreSQL, though, we can tune the Linux kernel to allow the database load to work optimally.  In this talk, we will learn how to tune some of the PostgreSQL’s parameters, and we will see the effect of that tuning, but we will focus on demonstrating how to tune Linux for better Postgres performance. As there are so many Linux kernel parameters that can be tuned to improve the performance of PostgreSQL, I will also share the results of benchmarks obtained when tuning some of the Linux parameters. 

### 3 - A Deep Dive into PostgreSQL Indexing [Presentation][5], [Video-1][6], [Video-2][6].
Indexes are a basic feature of relational databases, and  PostgreSQL offers a rich collection of options to developers and designers. To take advantage of these fully, users need to understand the basic concept of indexes, to be able to compare the different index types and how they apply to different application scenarios. Only then can you make an informed decision about your database index strategy and design. One thing is for sure: not all indexes are appropriate for all circumstances, and using a ‘wrong’ index can have the opposite effect to that you intend and problems might only surface once in production. Armed with more advanced knowledge, you can avoid this worst-case scenario! We’ll take a look at how to use pg_stat_statment to find opportunities for adding indexes to your database. We’ll take a look at when to add an index, and when adding an index is unlikely to result in a good solution. So should you add an index to every column? Come and discover why this strategy is rarely recommended as we take a deep dive into PostgreSQL indexing.

### 4 - Parallelism in PostgreSQL, [Presentation][8]. [Video][9].
PostgreSQL’s architecture is process-based instead of thread-based. PostgreSQL launches a process “postmaster” on startup and after that spans a new process whenever a new client connects to PostgreSQL. Before version 10 there was no parallelism in a single connection. It is true that multiple queries from a different client can have parallelism because of process architecture, but no, In other words, a single query runs serially and did not have parallelism. This is a huge limitation because a single query cannot utilize the multi-core. PostgreSQL introduced parallelism in version 9.6. Parallelism in a sense where a single process can have multiple threads to query the system and utilize the multicore in a system. I will discuss all the parallel scans options which are in PostgreSQL with the benchmark of these scans. 

[1]: https://github.com/ibrarahmad/PostgreSQLTalks/blob/main/PostgreSQL-FDW.pptx
[2]: https://www.youtube.com/watch?v=7wLLb2IY51A&t=903s
[3]: https://github.com/ibrarahmad/PostgreSQLTalks/blob/main/Performance-Tuning.pptx
[4]: https://www.youtube.com/watch?v=BsOYn1CWqBA&t=3241s
[5]: https://github.com/ibrarahmad/PostgreSQLTalks/blob/main/Deep-Dive-To-PostgreSQL-Indexes.pptx
[6]: https://www.youtube.com/watch?v=yWrJC2k1C8A
[7]: https://www.youtube.com/watch?v=4UjAMH6b0_4&t=1114s
[8]: https://github.com/ibrarahmad/PostgreSQLTalks/blob/main/Parallel-Queries.pptx
[9]: https://www.youtube.com/watch?v=GGGHWfDgw6A&t=752s








