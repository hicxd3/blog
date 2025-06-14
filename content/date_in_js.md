+++
date = '2025-04-29T02:53:24+03:00'
title = 'Date() in JavaScript'
categories = [ "javascript" ]
+++

The Date object in JavaScript helps us work with dates and times. It allows us to create, format, and extract information about specific moments in time.

To create a Date object with the current date and time:

```javascript
const now = new Date();
console.log(now); // current date and time
```

The Date object automatically uses the user's system time and timezone.
This means the date and time will reflect the user's local settings.

We can also create a Date object with specific values:

```javascript
const birthday = new Date(1990, 5, 15); // June 15, 1990
```

Note: The month index starts from 0 (January is 0, December is 11).

The constructor accepts the following parameters in this order:

```javascript
new Date(year, monthIndex, day, hours, minutes, seconds, milliseconds);
```

We can also create a date using a date-time string:

```javascript
const meeting = new Date("2025-04-29T10:30:00");
```

Useful methods:

```javascript
const date = new Date();

date.getFullYear();  // returns the full year
date.getMonth();     // returns the month (0-11)
date.getDate();      // returns the day of the month
date.getHours();     // returns the hour
```

There are also UTC versions of these methods:

```javascript
date.getUTCFullYear();
date.getUTCHours();
```

These methods are helpful when you need consistent time values across different timezones.