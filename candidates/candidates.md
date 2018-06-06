## Operators

* [some](https://stackblitz.com/edit/ts-rxjs-some-userland?file=index.ts)

    A counterpart of `every`.

    Accepts a predicate function to test for emission which will terminate the observable.

* [ofLatestFrom](https://stackblitz.com/edit/ts-rxjs-userland-oflatestfrom?file=index.ts)


    A factory method that scoops latest values from supplied observables

    More of an exercise than a real candidate.

    Sort of a workaround so to be able to use `withLatestFrom` - emits a null value, scoops latest values from observables.
    Suitable for imperative usage where it is needed to skim latest values (eg from ngrx store). More imperative than reactive.

    Use case: User clicks a button, action has to be dispatched with a payload
    which includes values from ngrx store (typically wrapped in observable selectors).
    Relevant only when the button clicks are handled in a traditional EventEmitter way,
    rather than using `fromEvent`. Which kind of sucks.
