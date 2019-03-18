# Accessibility
## Overview
### When websites and web tools are properly designed and coded, people with disabilities can use them. However, currently many sites and tools are developed with accessibility barriers that make them difficult or impossible for some people to use.Making the web accessible benefits individuals, businesses, and society.International web standards define what is needed for accessibility.

## Semantic HTML
### Structural, semantic HTML is the key starting point toward good accessibility practices.

### When a screen reader, or any sort of assistive device scans a web page, it gets information about the Document Object Model (DOM), or the HTML structure of the page. No styles or JavaScript will be read by a screen reader.

### When we write semantically correct HTML, we’re letting the browser know what type of content it’s dealing with and how that content relates to other content. By doing this, assistive technology is more easily able to do its job because it has a structure that it can work with.

### Use Container Elements for Layout Only
### Elements like `<div>` and `<span>` are for layout only. They’re semantically meaningless, they don’t have keyboard or touch support in any browser, and they don’t communicate anything to the accessibility API. For example, never use a div or span for a button when you could use a semantically meaningful button element.

### All of the other HTML elements should be used to tell the browser what functional purpose your content serves. These other HTML elements provide meaning to the browser and assistive technology about what you’re saying on your website, so you should choose them based on what the content is - not based on how they look with graphics.

### HTML elements to structure every page:
* header
* nav
* main
* article
* aside
* footer
* Headings

### Use one H1 per page, matching the page title.
### Do not skip heading levels when increasing, but you can skip levels when decreasing (h1, h2, h3, h2, h3, h4, h2, h3, h4). The headings taken out of context should logically represent the page content for screen readers and users who choose this option as a way to scan the page.

## ARIA
### Accessible Rich Internet Applications (ARIA) is a set of attributes that define ways to make web content and web applications (especially those developed with JavaScript) more accessible to people with disabilities.

### It supplements HTML so that interactions and widgets commonly used in applications can be passed to Assistive Technologies when there is not otherwise a mechanism. For example, ARIA enables accessible navigation landmarks in HTML4, JavaScript widgets, form hints and error messages, live content updates, and more.

### ARIA Roles:
### An ARIA role is added via a `role="<ROLE TYPE>"` attribute, and does not ever change for an element once it is set. There are four categories of ARIA roles:
* landmark
* document
* widget
* abstract
* Landmark ARIA Roles

### Much like semantic HTML elements, landmark ARIA Roles are used to give users of assistive technology a better way to navigate and identify the different parts of a web page.

### For many of the roles we have listed on this page, you will notice there are HTML5 elements with the same name, such as `<main>` and the aria landmark `role='main'`. There is no consensus on this matter, but in our opinion and from our research, using something like:

  `<nav class='mobile-nav' role='navigation' aria-label='Mobile Menu'> List of Links </nav>`
