# RxCoroutinesTerminology
Terminology mapping between Rx and Coroutines.

| RxJava                     | Coroutines         |
| -------------------------- |:------------------:|
| Single/Completable/Maybe   | suspend function   |
| Observable/Flowable        | Flow               |
| Subject/BlockingQueue      | Channel            |
| PublishSubject             | SendChannel        |
| BehaviorSubject            | StateFlow          |
| Schedulers                 | Dispatchers        | 
| Disposables                | Scopes             |
| subscribe                  | collect            |
| onNext                     | offer / onEach     |
| onError                    | catch              |
| Single\<T\>                | suspend () -> T    |
| Maybe\<T\>                 | suspend () -> T?   |
| Completable                | suspend () -> unit |
| Callback*                  | StateFlow          |
| Handler                    | Actor              |
|                            | emit (flow)        |


- StateFlow use *distinctUntilChangeed* by default

- Coroutines Disparchers = RxJava Scheduler (+ Exception Handler + parent context/job) 
