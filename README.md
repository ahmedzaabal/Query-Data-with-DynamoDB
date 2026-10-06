<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Query Data with DynamoDB

**Project Link:** [View Project](https://nextwork.ai/projects/0001cf4c-8256-52ae-b09c-6e99ed36462f)

**Author:** Ahmed Adel Fahmy  
**Email:** ahmed.hedia@outlook.com

---

![Image](https://nextwork.ai/amused_beige_adorable_sphinx/uploads/0001cf4c-8256-52ae-b09c-6e99ed36462f_733d9399)

## Introducing Today's Project!

### What is Amazon DynamoDB?

DynamoDB is a non relational Database and it's useful with storing data in an efficient way and retrieving information rapidly

### How I used Amazon DynamoDB in this project

In today's project, I used Amazon DynamoDB to create 4 tables and connect two tables together so whenever there is an update in one table, the other will be updated instantly

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is I am going to do a transaction between tables.

### This project took me...

This project took me 1.5 hours

## Querying DynamoDB Tables

A partition key is the filter that DynamoDB will use to split up and find data.

A sort key is a secondary key used to filter your query results again! Sort keys work after the partition key i.e. you still have to use the partition key to split up your data first, and then the sort key  partitions your data again.

![Image](https://nextwork.ai/amused_beige_adorable_sphinx/uploads/0001cf4c-8256-52ae-b09c-6e99ed36462f_d105b0b0)

## Limits of Using DynamoDB

I ran into an error when I queried for the user who posted a comment. This was because it's not designated as a partition key

Insights we could extract from our Comment table includes the ID and the comment date. Insights we can't easily extract from the Comment table includes message and the user who posted the comment

![Image](https://nextwork.ai/amused_beige_adorable_sphinx/uploads/0001cf4c-8256-52ae-b09c-6e99ed36462f_cb3e260c)

## Running Queries with CLI

A query I ran in CloudShell was a query to retrieve items from the ContentCatalog table. This query will retrieve the valid data that matches my constrains, for example: the ID, the content type and the consumed Capacity

Query options I could add to my query are consistent read, projection expression, and consumed capacity

![Image](https://nextwork.ai/amused_beige_adorable_sphinx/uploads/0001cf4c-8256-52ae-b09c-6e99ed36462f_733d9399)

## Transactions

A transaction is which is a group of operations that all have to succeed - if any of the operations in the group fails, none of the changes get applied. This makes sure that any change to your database is consistent across all your tables!

I ran a transaction using  aws dynamodb transact-write-items --client-request-token TRANSACTION1 --transact-items This transaction did two things updates the comment table and updates the count in the Forum Table

![Image](https://nextwork.ai/amused_beige_adorable_sphinx/uploads/0001cf4c-8256-52ae-b09c-6e99ed36462f_2f65f83e)

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/0001cf4c-8256-52ae-b09c-6e99ed36462f)*
