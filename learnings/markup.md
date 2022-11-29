# Markup learnings

## 1. Structure a site using semantic HTML to aid accessibility

Semantic tags provide meaning to the content they enclose. This aids accessibility by making it easier for screen readers and other assistive technologies to interpret the content of a web page. 

Example:
```html
<header>
  <nav class="navbar">
    <ul>
      <li><img class="logo" src="images/logo.svg" alt="logo" /></li>
      <li><a class="home" href="index.html">home</a></li>
      <li><a class="pagelink" href="#about-us-main">who are we</a></li>
      <li><a class="pagelink" href="contact-page/contact-page.html">get in touch</a></li>
    </ul>
  </nav>
</header>


```

## 2. Make a web page more readable for screen readers

In order for a web page to be more readable for screen readers it needs to have certain accomodations such as:
- A cohesive layout with semantic HTML,
- h1 tag should be used only once,
- h2-h6 should appear in the correct order,
- Alt text for images,
- Labels for each input element.

Example:

```html
<section class="f-box__layout">
	<label class="f-lbl__layout" for="company-name">Company name<span class="required">*</span></label>
	<input class="f-inp__layout f-inp__border" id="company-name" aria-describedby="required-description" type="text" name="company-name" placeholder="Company name" required />
</section>
```

## 3. Design a UI without relying solely on colour, so that we don’t exclude colour-blind users

- Clear and concise labelling,
- Create visual distinction by using icons, shapes or patterns,

![image](https://user-images.githubusercontent.com/105356599/203396588-0abcbf05-cd8d-4606-9c32-b4c11c208aa9.png)

## 4. Ensure our UI has sufficient colour contrast so that everyone can perceive it comfortably

Our site mostly has sufficient contrast, using our color scheme, save for one oversight in the footer.<br> 
![image](https://user-images.githubusercontent.com/105356599/203400983-43c6328e-a210-49ed-8015-76fe35f658c1.png)

## 5. Use various tools to check that a website meets accessibility criteria

https://accessibilitytest.org/results/XmRojU-MICmJ <br>
![image](https://user-images.githubusercontent.com/105356599/203398534-1ece14c5-8183-42b9-8a85-0dd161b6d632.png)

## 6. Ensure a website displays well on screens of different sizes

![image](https://user-images.githubusercontent.com/105356599/203398589-5a6f5c87-6cb2-4d86-ae5c-c38704f1ece5.png)

## 7. Use CSS media queries to ensure content is always presented effectively

```js
@media only screen and (max-width: 760px) {
  #quotes-section content {
    padding: 1.875rem .625rem;
  }

  #quotes-section quote {
    font-size: 1.5rem;
    line-height: 1.4;
  }

  #quotes-section quote-citation {
    display: block;
    padding-top: 1rem;
    margin: auto;
  }
}
```

## 8. Demonstrate a mobile-first approach to designing a website with a great user experience

Mobile first approach can be demonstrated by:
- Media queries for a responsive design which adapts to different screen sizes,
- Fluid layouts that resize automatically to fit the width of a user's device,
- Responsive typography that adjusts automatically to the size of a user's device,
- Avoiding the use of fixed-width elements which don't resize automatically,
- Use touch friendly elements for smaller screen sizes,
- Simplify the design to make it easier to use on a small screen,

## 9. Create an attractive and accessible colour palette for a project

While not entirely accessible, and with lessons learned, our colour palette uses the following colours: <br>
- #fbaf00
- #7fb069
- #313131
- #e4572e

## 10. Use CSS variables to apply repeated colours to HTML elements

This can be done using the var keyword in css:
```css
:root {
--blue: rgb(0, 0, 255);
}

.arbitraryclass {
background-color: var(--blue);
}
```
