+++
date = '2025-04-14T11:53:24+03:00'
title = 'Event Delegation in JavaScript'
categories = [ "javascript" ]
+++

Sometimes we don't want to attach event listeners to every single elements.

Instead, we can attach just one listener to a parent - and use it to handle all events from its children.

This techniwue is called `event delegation`

### Why use delegation?

We can use event delegation when:

1. We have lots of similar elements (like list items or buttons)

2. We want to reduce the number of listeners in memory

3. We added elements to the page dynamically

4. We want cleaner, smarter code.

Basic example: clicking on list items


Let's say we have a list like this:


```html
<ul id="userList">
    <li>Eva</li>
    <li>Mia</li>
    <li>Anna</li>
</ul>
```

Instead of adding a click listener to every `<li>`, we can add one to the parent `<ul>`

```js
const userList = document.getElementById('userList');

userList.addEventListener('click', (event) => {
    if(event.target.tagName === 'LI') {
        console.log('Clicked on:', event.target.textContent);
    }
});
```

Now any `<li>` inside `#userList` will be handled, even if we add new ones latter.

### Dynamic content? Still works.

Delegation works beautifully with dynamically created elements:

```js
const newItem = document.createElement('li');

newItem.textContent = 'Elle';
userList.append(newItem);
//No new listener needed!
```

We don't need to reattach listeners - the parent already listens.


### How it work (under the hood)

1. Events bubble up from the clicked element

2. The parent (listener) catches the event

3. We use event.target to check which element triggered it

4. If it matches what we're looking for (like a `<li>`) we run logic

### Notes

We can use delegation for `click`, `change`, `input` and more

Use event.target to find what was clicked

Combine with `.matches()` for more precise control

Greate for performance, cleaner code and dynamic interfaces