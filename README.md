3. List 3 tasks that can be accomplished with native SQL that you cannot do with JPQL. Explain why you would choose to use native SQL over JPQL for these specific tasks.

 Native SQL vs JPQL
1. Complex Arithmetic in Aggregate Functions

Task: Calculating the total value of items in an order, such as SUM(price * quantity).

Why Native SQL? JPQL often struggles with arithmetic operations inside aggregate functions, sometimes requiring additional Java DTOs and manual calculation in a loop. Native SQL performs this directly in the database engine, which is much more memory-efficient (RAM) and provides better performance.

2. Utilizing Database-Specific Features

Task: Using advanced features unique to a specific database, like JSON_EXTRACT for handling JSON columns in MySQL or PostgreSQL.

Why Native SQL? JPQL is designed to be "universal," so it doesn't recognize the "superpowers" of specific databases. If you need to leverage high-performance, vendor-specific functions, Native SQL is the only way to access them.

3. Advanced Date Manipulation

Task: Calculating differences between dates or extracting specific parts of a date, like DATEDIFF() or EXTRACT().

Why Native SQL? Handling dates in Java and filtering them through JPQL can sometimes be complex and lead to type mismatches. Native SQL allows you to use the database's built-in date functions to run queries like "users registered in the last 30 days" much faster and with cleaner code.
