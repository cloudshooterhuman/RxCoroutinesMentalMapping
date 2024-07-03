# RxCoroutinesTerminology
Mental Mapping between Rx and Coroutines.

| RxJava                     | Coroutines         |
| -------------------------- |:------------------:|
| Single/Completable/Maybe   | suspend function   |
| Observable/Flowable        | Flow               |
| Subject/BlockingQueue      | Channel            |
| PublishSubject             | SendChannel        |
| BehaviorSubject            | StateFlow          |
| Schedulers                 | Dispatchers        | 
| Disposables                | Scopes/Job         |
| subscribe                  | collect            |
| Observable.toSingle()      | Flow.collect       |
| subscribeOn                | flowOn             | 
| observeOn                  | collector’s context|  
| onNext                     | offer/onEach/emit  |
| onError                    | catch              |
| Single\<T\>                | suspend () -> T    |
| Maybe\<T\>                 | suspend () -> T?   |
| Completable                | suspend () -> unit |
| Callback*                  | StateFlow          |
| Handler                    | Actor              |
|                            | emit (flow)        |


- StateFlow use *distinctUntilChangeed* by default

- Coroutines Disparchers = RxJava Scheduler (+ Exception Handler + parent context/job) 


Ref:
- https://medium.com/@elizarov/execution-context-of-kotlin-flows-b8c151c9309b
- https://elizarov.medium.com/reactive-streams-and-kotlin-flows-bfd12772cda4
