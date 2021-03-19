<!-- njnmdoc: title="Database papers"  -->

I think main consequence of that is that databases are going to get easier to manage. Probably at a cost of internal complexity, but even there I don't expect too much trouble. It sort of boils down to figuring out parameters that work best for specific scenarios, and switching between them, which all can (and probably should) be done through testing / fuzzing.I recommend checking out the following publications if you have further interest:

-   Immanuel Trummer, Junxiong Wang, Deepak Maram, Samuel Moseley, Saehan Jo, and Joseph Antonakakis. 2019. SkinnerDB: Regret-Bounded Query Evaluation via Reinforcement Learning. In Proceedings of the 2019 International Conference on Management of Data (SIGMOD '19). Association for Computing Machinery, New York, NY, USA, 1153--1170.
-   Dimitrije Jankov, Shangyu Luo, Binhang Yuan, Zhuhua Cai, Jia Zou, Chris Jermaine, and Zekai J. Gao. 2019. Declarative recursive computation on an RDBMS: or, why you should use a database for distributed machine learning. Proc. VLDB Endow. 12, 7 (March 2019), 822--835.
-   Ryan Marcus and Olga Papaemmanouil. Towards a Hands-Free Query Optimizer through Deep Learning.
-   A. Pavlo, M. Butrovich, A. Joshi, L. Ma, P. Menon, D. V. Aken, L. Lee, and R. Salakhutdinov, "External vs. Internal: An Essay on Machine Learning Agents for Autonomous Database Management Systems," IEEE Data Engineering Bulletin, pp. 32-46, 2019. [PDF] [BIBTEX]
-   B. Zhang, D. V. Aken, J. Wang, T. Dai, S. Jiang, J. Lao, S. Sheng, A. Pavlo, and G. J. Gordon, "A Demonstration of the OtterTune Automatic Database Management System Tuning Service," PVLDB, vol. 11, iss. 12, pp. 1910-1913, 2018.
-   D. Van Aken, A. Pavlo, G. J. Gordon, and B. Zhang, "Automatic Database Management System Tuning Through Large-scale Machine Learning," in Proceedings of the 2017 ACM International Conference on Management of Data, 2017, pp. 1009-1024. [PDF] [BIBTEX]
-   D. Van Aken, D. E. Difallah, A. Pavlo, C. Curino, and P. Cudré-Mauroux, "BenchPress: Dynamic Workload Control in the OLTP-Bench Testbed," in Proceedings of the 2015 ACM SIGMOD International Conference on Management of Data, 2015, pp. 1069-1073. [PDF] [BIBTEX]


Another awesome paper is System R: Relational Approach to Database Management. Many things have changed since then, but not enough to make any of what it says less relevant. You can't get rid of transaction/recovery management, query optimizer, etc. <https://www.seas.upenn.edu/~zives/cis650/papers/System-R.PDF> (edited) 


Even though indexing and storage is important, I still think ARIES, describing interactions of WAL and transaction processing engine is one of the most important ones: <https://people.eecs.berkeley.edu/~brewer/cs262/Aries.pdf> it really helps you to understand recovery mechanism and notion of time. I think [@Nikolay](https://datatalks-club.slack.com/team/U01QTG9137E) will like it a lot, judging form the questions about zookeeper. It unveils what really happens when two or more transactions actually collide and do override each other's effects, or what happens during recovery: which records are persisted and which are discarded.



<https://www.snowflake.com/wp-content/uploads/2019/06/Snowflake_SIGMOD.pdf>

<https://www.allthingsdistributed.com/files/p1041-verbitski.pdf>

Next one is Principles of Transaction-Oriented Database Recovery, or "ACID Paper" that "establishes adequate and precise terminology for a topic in which confusion of concepts and implementation aspects imposes a lot of problems": <https://sites.fas.harvard.edu/~cs265/papers/haerder-1983.pdf>


