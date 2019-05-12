# Defer

Block of statements inside defer will be executed when execution leaves the current scope. 

Defer statements are useful when there are multiple exit points in the current scope and you wish to execute certain statements at the end, for every possible exit.

```
self.fetchOffers { [weak self] (response, error) in
guard let self = self else {
return }
defer {
self.dispatchGroup.leave()
}
//if error, handle error, exit
//if response, execute else exit
// handle response, exit
}
```

Dispatch group here is used to keep track of the count of active API fetch operations. When the API fetching and respective parsing is completed, the task is removed from the dispatchGroup.

