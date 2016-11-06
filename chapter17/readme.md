# chapter 17 : Modern Web Layout with Flexbox

- Flexbox Basics

On the surface, flexbox is pretty simple. There are only two components you need to make it work:

1. The Flex container

Any HTML element can be a flex container, but usually you'll use a `<div>` or some other structural HTML tag. The tag you use for the flex container will contain children and other tags that make up the second part of the flexbox model.

1. Flex items

Tags nested directly inside the flex container element are called flex items. Every direct child of the container element is automatically turned into a flex item. You can place any HTML tag inside the flex container. What's more, the child tags don't even have to be of the same type. For example, you could have one paragraph and four divs inside a flex container, and each of those will be a flex item.

Keep in the mind that only children of the flex container turn into flex items. If you had a `<div>` tag that you turned into a flex container and placed an unordered list inside it, only the `<ul>` tag would be a flex item. The `<li>` tags nested inside the `<ul>` tag would not be flex items.

In other words, as you're probably used to by now, flexbox is as easy as adding a `<div>` to a page and nesting additional divs inside it. For example, here's some simple HTML that can easily be used to create a row of items using flexbox:

```
<div class="container">
  <div>A flex item</div>
  <div>Another flex item</div>
  <div>A third flex item</div>
</div>
```
