# Errors Vs Exceptions

Exceptions enforce the idea that you should [[Return successful or not at all]].

Returning errors makes it more difficult to trace the bug (exceptions use a stack trace).

Exceptions are more difficult to spot when they happen.

> If a function is returning nothing, it should never throw an exception

I’m not sure about this one!

## Case Study: Transactions

```clojure
(
	defn accept-deposit [account-id amount] { 
		:pre [
			(> amount 0.00)
			(account-open? account-id)
		]
		:post [
			(contains? (account-transactions account-id) %)
		]
	}
	
	“Accept a deposit and return a new transaction id”
	;; some other processing…
	;; return the transaction:
	(create-transaction account-id :deposit amount)
)	
```

Create-transaction may or may not throw an exception here. If the database fails to connect, it will be handled at the same level as a negative deposit being created. It could be if these details are logged then null+error returns would be better.

## Problems with Exceptions

My biggest issue with exceptions is it encourages random try-catch blocks across code, which makes it hard to know if an exception should be caught or not. Error returns encourage errors to be dealt with as soon as possible, and it is made clear a function could not return what you expect because the return type is nullable.

Exceptions encourage you to focus on the happy path and assume success. Returning Errors force you to reckon with the fact an error might occur.
