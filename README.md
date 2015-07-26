gg
==

An ECMASCRIPT 5 compliant JavaScript utility library.

### Instance Methods
Instance methods refers to all methods on an instance of **gg**.
An instance of **gg** is returned when calling **gg(selector)**, where *selector* is a [selector string](http://www.w3.org/TR/selectors-api2/#findelements).
Almost all methods on a **gg** instance returns the instance, or a new instance, to enable chaining. The following methods are instance methods:
- **.each(func)** - call *func* for each node stored within this instance
- **.add(nodes)** - append additional *nodes* to this instance
- **.subtract(index)** - remove the node from this instance stored at *index*
- **.get(index)** - return a new instance with the node at *index* of this instance
- **.data(name, value)** - set a data attribute *name* to *value*
- **.remData(name)** - remove a data attribute *name*
- **.attr(name, value)** - set an attribute *name* to *value*
- **.remAttr(name)** - remove an attribute *name*
- **.(prop|css|style)(name, value)** - set a style property *name* to *value*
- **.rem(Prop|Css|Style)(name)** - remove a style property *name*
- **.text(string)** - set the textContent attribute to *string*
- **.remText()** - set the textContent attribute to an empty string
- **.html(string)** - set the innerHTML attribute to *string*
- **.remHtml()** - set the innerHTML attribute to an empty string
- **.classes(string)** - if *string* is defined set the className attribute, otherwise return its value
- **.addClass(string)** - add a class specified by *string*
- **.remClass(string)** - remove a class *string*
- **.togClass(string)** - toggle a class *string*
- **.hasClass(string)** - check if a class *string* exists
- **.insert(item, pos)** - call the insertAdjacentHTML method with the string *item* and the position *pos* being one of 'beforebegin', 'afterbegin', 'beforeend', or 'afterend'
- **.prepend(item)** - prepend *item* to all nodes; if *item* is a string and an html tag, create a new element and prepend it
- **.prependTo(parent)** - prepend all nodes to *parent*
- **.append(item)** - append *item* to all nodes; if *item* is a string and an html tag, create a new element and append it
- **.appendTo(parent)** - append all nodes to *parent*
- **.after(item)** - place *item* after each node; if *item* is a string and an html tag, create a new element and place it
- **.before(item)** - place *item* before each node; if *item* is a string and an html tag, create a new element and place it
- **.remove(children)** - remove *children* from all nodes; if *children* is undefined then remove all nodes
- **.parents()** - get the parents of all nodes
- **.children()** - get the children of all nodes
- **.select(selector)** - call select on all nodes and return a new instance
- **.selectAll(selector)** - call selectAll on all nodes and return a new instance
- **.clone(deep)** - clone all nodes and return a new instance
- **.hide()** - hide all nodes
- **.show()** - show all nodes
- **.on(ev, func, bub, params)** - add an event listener
- **.off(ev, func, bub)** - remove an event listener; if *func* is undefined, remove all listeners of type *ev*
- **.once(ev, func, bub, params)** - listen for event *ev* once and only once

### Non-Instance Methods
Non-instance methods refers to the utility methods on the **gg** constructor, and can be accessed by calling **gg.method()**, where **method()** is any of the following:
- **typeOf(value)** - updates the typeof operator
- **noop()** - an empty function block
- **isBoolean(boolean)** - check if *boolean* is a boolean
- **isNumber(number)** - check if *number* is a number
- **isString(string)** - check if *string* is a string
- **isArray(array)** - check if *array* is an array
- **isObject(object)** - check if *object* is an object
- **isFunction(func)** - check if *func* is a function
- **isNull(nul)** - check if *nul* is null
- **isUndefined(undef)** - check if *undef* is undefined
- **isNode(node)** - check if *node* is a DOM node
- **isEmpty(object)** - check if *object* is an empty object
- **isArrayLike(object)** - check if *object* is an array-like object
- **toArray(value)** - convert *value* to an array
- **inArray(array, value)** - check *value* is contained within *array*
- **toCamelCase(string)** - convert *string* to a camel case string
- **undoCamelCase(string)** - convert *string* to a hyphenated string
- **getCharCodes(string)** - convert *string* to a Uint8Array of character codes
- **getStringFromCodes(codes)** - convert an array of character *codes* to a string
- **getById(id)** - a shorthand for document.getElementById
- **select(selector)** - a shorthand for document.querySelector
- **selectAll(selector)** - a shorthand for document.querySelectorAll
- **uuid()** - generate a universally unique id
- **supplant(string, object)** - perform variable substitution *string* where *object*'s keys marked by braces are replaced with the corresponding values
- **inherits(ctor, super_ctor)** - have *ctor* inherit from *super_ctor*'s prototype and set *ctor.gg_super* to *super_ctor*
- **extend(object, add, overwrite)** - extend *object* with the properties of *add* and overwrite existing properties if *overwrite* is set to true
- **each(items, func, thisarg)** - call *func* for each item within *items*, and set the this argument to *thisarg* within *func*'s body
- **cloneNodeDeeper(node)** - clone *node* and its event handlers
- **keyboardHandler(options)** - listen for the 'keydown' event where *options* is an object whose keys are keyCodes and values are callbacks
- **mouseHandler(options)** - listen for the 'mousedown' event where *options* is an object whose keys are keyCodes and values are callbacks
- **xhrReq(options)** - perform an XMLHttpRequest where the following possible *options* are:
  - **data** - the data to send with the request
  - **method** _string_ - the method to perform
  - **url** _string_ - the target url
  - **async** _boolean_ - indicate whether this operation should be asynchronous
  - **username** _string_ - a username to send with the request
  - **password** _string_ - a password to send with the request
  - **mimType** _string_ - the mime type of the data being sent
  - **responseType** _string_ - the response type; either '', 'arraybuffer', 'blob', 'document', 'json', or 'text'
  - **headers** _object_ - additional headers to send with the request
  - **timeout** _number_ - the timeout in milliseconds for the request
  - **success** _function_ - the function to call if the request succeeds
  - **failure** _function_ - the function to call if the request fails
- **readFiles(options)** - read files selected by the user where the following possible *options* are:
  - **element** _node_ - the file input element to listen for the 'change' event on
  - **readAs** _string_ - read the file as either 'arraybuffer', 'binary', 'blob', 'dataurl', or 'text'
  - **mimeType** _string_ - only read files with this specified mime type
  - **success** _function_ - the function to call if the file read succeeds
  - **failure** _function_ - the function to call if the file read fails
