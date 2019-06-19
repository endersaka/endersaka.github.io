---
use_math: true
---

When it comes to designing my own Web Site I become very picky. I am never sutisfied with the result and this has the disrupting side effect to transform the design process in an never ending task. This is something that everyone would like to avoid. Then: I urgently need to find a practical solution.

The first step towards the solution is to understand what you are doing wrong (in my opinion).

### Creative Distractions

If you are a picky person like me, do not waste too much time reviewing design thems that are available on the Web. Even when they are released for a fee - trust me! - they are rarely well coded and the worst drawback you wouldn't like to face is to fix messy code in the attempt to implement your customizations.

And when it comes to open source themes (especially WordPress themes) things can become very weird.

At the end of your review research you will find yourself overwelmed by a bunch of almost identical themes that almost do what you want but they actually don't do it exactly and they are almost impossible to customize.

Listen to me. Don't fall in this trap!

### Lack of Tools

One of the main problems you face during your creative process is the lack of prototyping tools that are easy to use (i.e. WYSIWYG) and generate a good ouput (good prototyping code that takes in to account possible design systems, frameworks - i.e. Bootstrap, Material Design, ecc...). There are some good designing tools like Figma or Sketch but, if you are not a developer (or if you don't want to waste your time reinventing the wheel), to convert them in to working code can be a mess. Therefore, roll up your sleeves and learn some basic coding or ask some help.

### The Shopping List

The first thing you should do after you have reviewed some modern Web Site design trends (i.e. browsing [awwwards.com](https://www.awwwards.com/)) is to write down a list of requirements (of features, if you like to call them like that).

In my case, for example, the list is:

- my Web Site theme has to be minimalist to maximize readability;

- the design priority is typograpy;

- I want to use Nunito as the Site main font;

- I want to use Fluid Typograpy in place of Responsive Typography;

- I want a simple, minimalist, Navigation Bar that hides or scales down when user scrolls the page down;

- I want a sticky side menu for sharing buttons;

- the theme must use gradients and be colorful;

- the main color should be indigo;

- I want to support comments.

### Fluid Typography

Recently, during my latest job, I had the opportunity to test and implement Fluid Typography in place of Responsive Typography. I based my work on the following articles:

- [Fluid Typography](https://css-tricks.com/snippets/css/fluid-typography/) from [css-tricks.com](https://css-tricks.com);

- [Responsive And Fluid Typography With vh And vw Units](https://www.smashingmagazine.com/2016/05/fluid-typography/) from [Smashing Magazine](https://www.smashingmagazine.com);

Essentially it works like this: if we want that the font size varies automatically from a minimum of 16px, when the viewport width value is 400px, to a maximum of 24px, when the viewport width value is 800px, the formula is the following.

```css
font-size: calc(16px + ((24 - 16) * (100vw - 400px) / (800 - 400)));
```

In the form of mathematical function it can be expressed like this:

$$
s = s' + ( s'' - s' ) * ( w - w' / w'' - w' )
$$
