# Day 63 – Transactions and Combining Search Results

## What I Did

- Continued the **Splunk Search Expert 103** course
- Learned how transactions group related events into a single logical activity
- Explored the `transaction` command and its use in event correlation
- Studied complete and incomplete transactions and techniques for optimizing transaction searches
- Reviewed the concept of subsearches
- Learned how to combine search results using various SPL commands

## What I Understood

Today's learning focused on correlating related events and combining data from multiple searches. I learned that transactions help reconstruct activities that span multiple events, while commands such as `append`, `appendcols`, `join`, and `union` make it possible to merge search results in different ways depending on the use case.

## Concepts Covered

### Transactions

- Understanding Transactions
- `transaction`
- Working with Transactions
- Complete and Incomplete Transactions
- Optimizing Transactions

### Combining Search Results

- Introduction to Subsearches
- `append`
- `appendcols`
- `join`
- `union`

## Key Takeaways

- Transactions help correlate multiple related events into a single activity for easier investigation.
- Optimizing transaction searches is important because they can be resource-intensive.
- Different SPL commands combine search results in different ways, and selecting the appropriate command depends on the investigation scenario.
- Understanding these commands improves the ability to build more advanced and efficient SPL queries.

## Next Step

- Continue **Splunk Search Expert 103** and explore more advanced SPL techniques and search optimization concepts.