
# Cyclic Materials util-predicate API

- [`predicateObject`](#predicateObject)

- [`predicateObservable`](#predicateObservable)

- [`predicateObjectOfObservable`](#predicateObjectOfObservable)

### <a id="predicateObject"></a> `predicateObject(definitions, predicateKey)`

Returns a function that takes an object as argument. The function predicates
each property of the provided object with the matching properties
of `definitions`. If the value of a definition is a function, it will
be called as predicate taking the matching object property as argument.
If the definition value is an object, it will look for the predicate
function specified by `predicateKey` (defaults to `type`).

#### Arguments:

- `definitions :: Object` Object of properties to match.
- `predicateKey :: String` Optional name of the property specifying the predicate.

#### Return:

*(Function)* Takes the Object to predicate as argument.

- - -

### <a id="predicateObservable"></a> `predicateObservable(predicateFunc)`

Returns a function that takes an Observable as argument. The function maps
the items of the Observable and passes the item as argument
to `predicateFunc`

#### Arguments:

- `predicateFunc :: Function` Function to receive items from Observable.

#### Return:

*(Function)* Takes the Observable as argument whose items to predicate.

- - -

### <a id="predicateObjectOfObservable"></a> `predicateObjectOfObservable(definitions, predicateKey)`

Returns a function that takes an Observable that emits Objects as argument.

#### Arguments:

- `definitions :: Object` Object of properties to match.
- `predicateKey :: String` Optional name of the property specifying the predicate.

#### Return:

*(Function)* Takes the Observable as argument whose objects to predicate.

- - -

