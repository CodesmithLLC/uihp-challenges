# Challenge: Templates and Directives
## User Interface Hard Parts

In this challenge, we'll explore how templates provide a way to make UI programming more declarative. 

### Part 1

For the first part of the challenge, you'll be working in the file `static.html` to build out a simple webpage using HTML. You'll see that a boilerplate skeleton has been set up for you, but there's nothing in the body tag yet. That's what we'll be changing!

To test your work throughout the challenge, open the `static.html` file in your browser. Before you start, you should see a blank page displayed. Time to start filling it out!

See [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) for a reference on HTML tags that are available for you to use. Note that for this challenge, you should be using *only* HTML, and no styling is necessary. You do not need to add CSS or use the HTML `style` attribute.

The content of your page can be whatever you like, but it must adhere to the following structure:

- [ ] First, add a **heading** to your page. This should be the largest element of text that will display on the page.
- [ ] Below the main heading, add a **subtitle**. This text should be smaller than the heading, but larger than anything else.
- [ ] Add a **paragraph** of text below the subtitle.
- [ ] Create a **bulleted list** and fill it with five items.
- [ ] Lastly, embed an **image** next to the page subtitle.

When you look at the HTML you just wrote, you should find that it's extremely intuitive to follow. The page is laid out exactly as your code describes - someone else should be able to easily tell what's there simply by looking at your HTML file.

In this day and age, however, the user experience of navigating a webpage is *dynamic*. The content of the page must be able to change to reflect the user's interactions - our `static.html` file will not be able to do that. Thus, in practice, frontend developers primarily use *JavaScript* to create HTML elements and update the DOM. 

### Part 2

Open up the `dynamic.html` file. You'll see that we also have an HTML skeleton that will simply render a blank page - but this time, we've included a script tag that links to a JavaScript file, `templates.js`. For this part of the challenge, *do not* modify anything in the `dynamic.html`- you'll be working strictly in the JavaScript file to *dynamically* add HTML elements to the DOM.

Your task here is to write JavaScript code that will recreate the structure and content of `static.html`, and add it to `dynamic.html`, in the same order. Again, the resulting page must contain the following:

- [ ] Heading
- [ ] Subtitle
- [ ] Paragraph
- [ ] Bulleted list
- [ ] Image next to the subtitle

Refer to [this page](https://developer.mozilla.org/en-US/docs/Web/API/Document) for a list of methods that can be used to interact with the DOM.

You can consider this part of the challenge complete once both HTML files look identical when you open them in the browser. Now, though, compare your `templates.js` file with `static.html`. You'll likely find that your JavaScript code is fairly repetitive and very *imperative* - listing out step-by-step instructions for everything that must be done to add each element to the page.

### Part 3

Next, you'll be refactoring your code in `templates.js` to make it more declarative. We'll still need to use the DOM API to create elements and append them to the page - but if we create functions to modularize that logic, which we can reuse whenever we need to add another element, we'll eliminate the need to write lots of repetitive lines of code.

- [ ] Create a function called `template`, which creates and returns HTML elements.
  - This function should take in a string that denotes the **type** of element to be created, as well as that element's **content**. 
    - Note that, in order for our template to be fully dynamic, it should be able to accept content of any type!
  - You should be able to use this `template` function to create any of the elements you created in the previous section.   
    - The bulleted list element has five children, all of which are individual `list item` elements. How can we make sure our template is able to handle this?

- [ ] Finally, use your `template` function to recreate each element and append the results to the DOM. If you've done it correctly, your `dynamic.html` file should look exactly the same as `static.html`!