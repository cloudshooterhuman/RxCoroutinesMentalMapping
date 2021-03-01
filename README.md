# RxCoroutinesTerminology
Terminology mapping between Rx and Coroutines.

| RX                         | Coroutines         |
| -------------------------- |:------------------:|
| Single/Completable/Maybe   | suspend function   |
| Observable/Flowable        | Flow               |
| Subject                    | Channel            |
| PublishSubject             | SendChannel        |
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


- StateFlow use *distinctUntilChangeed* by default

- Coroutines Disparchers = RxJava Scheduler (+ Exception Handler + parent context/job) 
