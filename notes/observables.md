# Observables

- introduced in ES7/2016
- Angular 2+
- Lazy collections, must be subscribed to in order to use them
- Alternatives to Promises
- Can be canceled
- Can be used with array operators through 3rd party library RxJS (Reactive JS)
  - allows manipulation of data before subscribed to it
  - .pipe()
- Can convert Observables to a Promise instead of subscribing

## .subscribe()

- takes a next and error function as args
- don't *need* to unsubscribe from http requests (but probably should anyway)

## async pipe

```
<li *ngFor='let something of service.anyFunction() | async'>{{something.data}}</li>
```

- Automatically subscribes/unsubscribes to Observable
