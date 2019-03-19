# SQLServerDeadLocks
A procedure to list recent deadlocks on sql server. Another procedure to cause a deadlock.
* pr_DeadlockList - Lists recent deadlocks. Lists which stored procedures/line numbers caused the error.
* pr_Deadlock_Test - Causes a deadlock to happen. 
  1. Open two query windows. 
  2. Execute pr_Deadlock_Test in one of the query windows.
  3. Execute pr_Deadlock_Test in the other query window.
  4. Wait a minute or two. One of them should crash with a deadlock error.
  5. It creates two tables to make this happen, but those tables should be deleted once the test is over.
  6. You should then see a description of this deadlock if you run pr_DeadlockList.
