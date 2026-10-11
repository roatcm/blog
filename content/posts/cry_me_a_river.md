+++
date = '2026-10-1-'
draft = false
title = 'Cry Me A River'
tags = ['woke', 'sociopaths', 'sensitives']
summary = 'Stepping on toes.'
+++

Way back in the day, before there was much in the way of tooling or frameworks to support data lineage tracking, I'd built my own running directly on our Redshift instance. The basic observation that led to this stored procedure being developed is that it's possible tokenise and then "join" the elements making up an individual query to a list of schema and table names, so that there's a resonable chance that if a given query mentions my_schema.my_table, then it's referring to that table. 

Then we just need to iteratively run the lineage stored procedure on every query in the AirFlow DAG and we've got ourselves an upsteam/downstream lineage matrix. Imagine a huge 2D matrix with the names of each table along both axes and a mark indicating if one table is upstream of another in the lineage graph. Simples. 



