# Intro to Next.js & Tailwind CSS


## Tailwind CSS

Tailwind CSS – A Utility First CSS Framework, which provides several of these opinionated, single-purpose utility classes that you can use directly inside your markup to design an element.

Some of the utility classes that I frequently use these days are:

- flex: Used to apply Flexbox to a `<div>`
- items-center: to apply the CSS property `align-items: center;` to a `<div>`
- rounded-full: to make an image circular, and so on



**Example**
```
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
  </div>
</div>
```

In the example above, we’ve used:

- Tailwind’s flexbox and padding utilities `(flex, shrink-0, and p-6)` to control the overall card layout
- The max-width and margin utilities `(max-w-sm and mx-auto)` to constrain the card width and center it horizontally
- The background color, border radius, and box-shadow utilities `(bg-white, rounded-xl, and shadow-lg)` to style the card’s appearance
- The width and height utilities `(w-12 and h-12)` to size the logo image
- The space-between utilities `(space-x-4)` to handle the spacing between the logo and the text
- The font size, text color, and font-weight utilities `(text-xl, text-black, font-medium, etc.)` to style the card text


### Tailwind CSS Benefits

- **You aren’t wasting energy inventing class names**. No more adding silly class names like sidebar-inner-wrapper just to be able to style something, and no more agonizing over the perfect abstract name for something that’s really just a flex container.
- **Your CSS stops growing.** Using a traditional approach, your CSS files get bigger every time you add a new feature. With utilities, everything is reusable so you rarely need to write new CSS.
- **Making changes feels safer.** CSS is global and you never know what you’re breaking when you make a change. Classes in your HTML are local, so you can change them without worrying about something else breaking.

