# vue-notes
Notes for Vue 3

v-if: Do not render the element at all
v-show: Render the element but only adds display none.
v-else
v-on
v-for

Event Binding
@ is symbol for event binding
Example
@click
@mousehover

Attribute Binding
: symbol for attribute binding
Example
:href
:class
other html attributes

Dynamic classes
:class {className: expression} 
If expression is true the className will be applied. And className will come from the stylesheet of the component.

Computed Property
Manipulate data before accessing in html

3 Parts of vue file
template (HTML)
script (JS/ TS)
style (CSS)

Event Handlers
Event Modifiers
 .stop
.prevent
.self
.capture
.once
.passive
Key Modifiers
.enter
.tab
.delete
.etc...

Mouse Button Modifier
.right
.left
.middle

Reactivity
ref()
Wraps the value
Can hold all types of datatypes
reactive()
Makes an object itself
Cannot hold primitive data types

Parent and Child Communication
Property
```
in parent
<ChildView :message="Hello from parent" />

in child
defineProps({ message: { type: String, required: true, } });
<h1>{{ message }}</h1>
```

Event
syntax: payload is optional
emit(eventName, payload)

name of the event should be the same for the both parent and child
```
in parent
<ChildComponent @custom-event="customEvent" />
kebab-case

in child
<button @click=$emit('customEvent')>
camelCase
```

composition api: context.emit()
Context object has access to slots, attributes, and emit method itself.
can be called setup(props, context)

Slots
Teleport
Forms and Data Binding
Vue Router
Composition API
Async with Composition API
Routing with Composition API
