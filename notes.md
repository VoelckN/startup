# CS 260 Notes

These are intro notes so that I learn to add a commit.

[My startup - Simon](https://simon.cs260.click)

## Helpful links

- [Course instruction](https://github.com/webprogramming260)
- [Canvas](https://byu.instructure.com)
- [MDN](https://developer.mozilla.org)

## AWS

My IP address is: 54.81.96.130
Launching my AMI I initially put it on a private subnet. Even though it had a public IP address and the security group was right, I wasn't able to connect to it.

## Caddy

No problems worked just like it said in the [instruction](https://github.com/webprogramming260/.github/blob/main/profile/webServers/https/https.md).

## HTML

This was easy. I was careful to use the correct structural elements such as header, footer, main, nav, and form. The links between the three views work great using the `a` element.

The part I didn't like was the duplication of the header and footer code. This is messy, but it will get cleaned up when I get to React.

## CSS

This took a couple hours to get it how I wanted. It was important to make it responsive and Bootstrap helped with that. It looks great on all kinds of screen sizes.

Bootstrap seems a bit like magic. It styles things nicely, but is very opinionated. You either do, or you do not. There doesn't seem to be much in between.

I did like the navbar it made it super easy to build a responsive header.

```html
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand">
            <img src="logo.svg" width="30" height="30" class="d-inline-block align-top" alt="" />
            Calmer
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" href="play.html">Play</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="about.html">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="index.html">Logout</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
```

I also used SVG to make the icon and logo for the app. This turned out to be a piece of cake.

```html
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <rect width="100" height="100" fill="#0066aa" rx="10" ry="10" />
  <text x="50%" y="50%" dominant-baseline="central" text-anchor="middle" font-size="72" font-family="Arial" fill="white">C</text>
</svg>
```

## React Part 1: Routing

Setting up Vite and React was pretty simple. I had a bit of trouble because of conflicting CSS. This isn't as straight forward as you would find with Svelte or Vue, but I made it work in the end. If there was a ton of CSS it would be a real problem. It sure was nice to have the code structured in a more usable way.

## React Part 2: Reactivity

This was a lot of fun to see it all come together. I had to keep remembering to use React state instead of just manipulating the DOM directly.

Handling the toggling of the checkboxes was particularly interesting.

```jsx
<div className="input-group sound-button-container">
  {calmSoundTypes.map((sound, index) => (
    <div key={index} className="form-check form-switch">
      <input
        className="form-check-input"
        type="checkbox"
        value={sound}
        id={sound}
        onChange={() => togglePlay(sound)}
        checked={selectedSounds.includes(sound)}
      ></input>
      <label className="form-check-label" htmlFor={sound}>
        {sound}
      </label>
    </div>
  ))}
</div>
```
# MIDTERM NOTES

### 18. How to style in JavaScript using an element's id: 
```js
document.getElementById("given-id").style.color = "green"
```
### 19. Opening HTML Tags!

Paragraph: 
```html 
<p>Lorem ipsum dolor sit amet</p>
```

Ordered list:
```html
<ol>
  <li> Ordered 1
  <li> Ordered 2
</ol>
```

Unordered list:
```html
<ul>
  <li> Item
  <li> Item
</ul>
```

Headings:
```html
<h1>First level heading</h1>
<h2>Second level heading</h2>
<h3>Third level heading</h3>
```

### 20. To declare the document type as html, use:
```html <!DOCTYPE html> ```

### 21. Syntax for JavaScript

If/else statement
```js
if (boolean_condition) {
  perform_action();
} else {
  perform_other_action();
}
```

For loop
```js
for (initialization; condition; finalExpression) {
  //initialization = declaring and starting a loop counter variable
  // condition = boolean evaluated before each iteration (often involving the counter variable)
  // finalExpression = code executed at the end of the iteration to adjust the counter variable
  execute_code();
}
```

While loop
```js
while (boolean_condition) {
  execute_code();
}
```

Switch statement
This serves as an if-else-if-else-if-else-if without being overly cluttered.
```js
switch (expression) {
  case value1: // In the case that expression === value1, do the following code underneath:
    execute_code_1();
    break; // ends the switch block entirely
  case value2:
    execute_code_2();
    break;
  default:
    backup_code_in_case_no_case_is_met();
}
```

### 22. Ok, creating an object in JavaScript can be done in many different ways. Here are some.

  1. Object initializers. Takes a name and adds key-value pairs to them, which are the object's properties and its values.
  ```js
  const obj = {
    property1: value1,
    property2: 500;
  };
  ```
  2. Constructor functions.

### 23. Yes, one can add new properties to JavaScript objects.
They can use dot notation, like:
```js
const obj = {};
obj.property = value;
```
They can also use bracket notation, like:
```js
obj["property"] = value;
```
> [!TIP]
> Properties must be of type String or Symbol
> Values can be any type however.


### 24. To include JS in an HTML page:

### 25. Using JavaScript to change text in HTML

### 26. What is JSON?

### 27. Various Console Commands
- chmod
- cd
- ls
- vim
- nano
- mkdir
- mv
- rm
- man
- ssh
- ps
- wget
- sudo

### 28. Using console to create a remote shell session

### 29. -la parameter with ls in console

### 30. Pieces of the domain name

### 31. Is a web certificate necessary to use HTTPS?

### 32. What can DNS A records point to?

### 33. Ports to their Protocols
- 443
- 80
- 22

### 34. JavaScript using Promises

