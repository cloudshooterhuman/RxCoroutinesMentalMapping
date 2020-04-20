# RxCoroutinesTerminology
Terminology mapping between Rx and Coroutines.

| RX                         | Coroutines       |
| -------------------------- |:----------------:|
| Single/Completable/Maybe   | suspend function |
| Observable/Flowable        | Flow             |
| Subject                    | Channel          |
| Schedulers                 | Dispatchers      |
| Disposables                | Scopes           |
| subscribe                  | collect          |
| onNext                     | offer            |
| onError                    | catch            |
