# My CSS Articles

1. [How To Create a User Interface Using CSS Grid](https://medium.com/geekculture/how-to-create-a-user-interface-using-css-grid-738d0b51282)

# Books
1. https://www.refactoringui.com/

# Code

```html
<div className="card-content">
    <p className="card-date">{formattedDate}</p>
    <h6 className="card-title" data-date={formattedDate}>
      {post.title}
    </h6>
</div>
```

```css
.card-content {
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  gap: 5px;
}

.card-title::after {
		content: " — " attr(data-date);
		font-size: smaller;
		color: gray;
}

.card-date {
  display: none;
} 
```

# Tools
https://cssstats.com/



# Resources
1. https://css-tricks.com/building-a-scalable-css-architecture-with-bem-and-utility-classes/
2. https://github.com/jareware/css-architecture
3. https://developer.mozilla.org/en-US/docs/Web/CSS/clamp
4. https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity
5. http://smacss.com/
6. https://frontendmasters.com/courses/css-variables/dry-fallback-strategies/
7. https://open-props.style/
8. https://nerdy.dev/
9. https://styleguide.github.com/
10. https://bradfrost.com/blog/post/atomic-web-design/
11. https://css-weekly.com/
12. https://frontendfoc.us/
13. https://www.lightningdesignsystem.com/components/overview/
14. https://www.youtube.com/watch?v=7hYOLLO2gc4&t=1357s&ab_channel=YouGottaLoveFrontend
15. https://courses.rachelnabors.com/p/web-animation-essentials-css-animations-and-transitions
