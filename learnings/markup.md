# Markup portfolio

## 1. Structure a site using semantic HTML to aid accessibility

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

![image](https://user-images.githubusercontent.com/105356599/203396437-60cdf45e-6e99-44ac-9554-81449992b7df.png)

## 3. Design a UI without relying solely on colour, so that we don’t exclude colour-blind users

Neutral colour scheme, would function the same with or without the colour.
![image](https://user-images.githubusercontent.com/105356599/203396588-0abcbf05-cd8d-4606-9c32-b4c11c208aa9.png)

## 4. Ensure our UI has sufficient colour contrast so that everyone can perceive it comfortably

![image](https://user-images.githubusercontent.com/105356599/203398302-eed0e661-1d32-47e0-90b7-61437d2f440f.png)

## 5. Use various tools to check that a website meets accessibility criteria

https://accessibilitytest.org/results/XmRojU-MICmJ
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

The project itself is not entirely built upon mobile first ideology, however, it would best be accomplished by using
responsive responsive units and media/container queries with min-width rather than max-width.

## 9. Create an attractive and accessible colour palette for a project

While not entirely accessible, and with lessons learned, our colour palette uses the following colours: 
#fbaf00
#7fb069
#313131
#e4572e

## 10. Use CSS variables to apply repeated colours to HTML elements

This can be done using the var keyword in css:
```css
color: var(--blue);
```
