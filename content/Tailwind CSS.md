+++
hidden = true
date = '2025-09-12T18:53:24+03:00'
title = 'Tailwind CSS Cheatsheet — 100 Classes and Setup'
draft = true
+++

## Tailwind CSS Cheatsheet ^-^

Complete guide to start with Tailwind and master 100 most important classes.  
From setup to advanced utilities — everything you need

### Setup

npm install -D tailwindcss postcss autoprefixer — install Tailwind

npx tailwindcss init -p — create config files

tailwind.config.js → add content paths: 
```js
["./index.html", "./src/**/*.{js,ts,jsx,tsx}"]
```

In index.css add:
```css
@tailwind base;

@tailwind components;

@tailwind utilities;
```

npm run dev — start dev server

### Colors & Background

text-red-500 — red text

text-blue-600 — blue text

text-gray-700 — gray text

bg-pink-500 — pink background

bg-green-400 — green background

bg-gradient-to-r from-pink-500 to-yellow-500 — gradient

border — default border

border-2 border-blue-500 — thick blue border

border-dashed — dashed border

divide-y divide-gray-300 — divide children with line

### Spacing

m-4 — margin 1rem

mt-2 — margin top

mx-auto — center horizontally

p-4 — padding 1rem

px-6 — padding left and right

py-8 — padding top and bottom

space-x-4 — horizontal space between children

space-y-6 — vertical space between children

gap-4 — gap in grid or flex

container mx-auto — centered container

### Sizing

w-1/2 — half width

w-full — full width

max-w-sm — small max width

max-w-4xl — large max width

h-12 — height 3rem

min-h-screen — min height = viewport

aspect-square — keep square ratio

aspect-video — keep video ratio

object-cover — fit image cover

object-contain — fit image contain

### Typography

font-sans — sans-serif font

font-serif — serif font

font-bold — bold text

font-light — light text

text-sm — small text

text-lg — large text

text-2xl — extra large text

tracking-wide — letter spacing

leading-relaxed — line height

truncate — ellipsis for overflow

### Layout (Flex & Grid)

flex — display flex

flex-col — flex direction column

flex-row — flex direction row

justify-center — center horizontally

justify-between — space between

items-center — center vertically

items-start — align start

grid — display grid

grid-cols-2 — 2 column grid

grid-cols-3 gap-4 — 3 columns with gap

### Effects

shadow — default shadow

shadow-lg — large shadow

rounded — small border radius

rounded-lg — large radius

rounded-full — circle

opacity-50 — 50% opacity

opacity-100 — full opacity

hover:bg-blue-500 — change bg on hover

hover:text-white — text color on hover

active:scale-95 — shrink on click

### Responsive

sm:text-sm — small screen text

md:text-lg — medium screen text

lg:text-xl — large screen text

xl:text-2xl — extra large screen

2xl:text-3xl — super large

sm:hidden — hide on small screen

md:flex — show flex on medium

lg:grid — show grid on large

sm:px-2 md:px-6 lg:px-12 — responsive padding

sm:w-full md:w-1/2 — responsive width

### Advanced Utilities

cursor-pointer — pointer cursor

cursor-not-allowed — disabled cursor

select-none — disable text select

select-all — select all text

z-10 — z-index 10

z-50 — z-index 50

absolute top-0 left-0 — absolute position

fixed bottom-0 right-0 — fixed position

sticky top-0 — sticky position

hidden — display none

### Animations & Transitions

transition — enable transition

transition-all — all properties

duration-300 — 300ms duration

ease-in — ease in

ease-out — ease out

transform — enable transforms

scale-110 — scale up

rotate-45 — rotate 45°

animate-spin — spin animation

animate-bounce — bounce animation

Key Points ^-^

- Setup first, then utilities

- 100 classes cover 90% of real work

- Think in small utilities, combine for complex design

