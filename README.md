# Bootstrap4 - All Elements v2

Bootstrap 4 - All Elements v2

For version 2 I have added add a new color (purple), and included an element where relevant on the index.html to show how it works.  I've also added a couple of examples of compiled css files.  To use them change custom.css in the head of the index.html to either of the examples (muted.css or redish.css).

I've also added some code in the custom.js file to add smooth scrolling. Note in the snippet below I've added data-smooth="#anchor" - that facilitates smooth scroll.

```html
<ul class="navbar-nav mr-auto">
  <li class="nav-item">
    <a class="nav-link" data-smooth="#home" href="#home">Home <span class="sr-only">(current)</span></a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-smooth="#features" href="#features">Features</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-smooth="#news" href="#news">News</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-smooth="#gallery" href="#gallery">Gallery</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-smooth="#contact" href="#contact">Contact</a>
  </li>
</ul>
```

Utils.js is included in bootstrap.js, so to use scrollspy add the following to your "body" tag.  Adjust the data-offset to where you want the link to activate.

```html
<body id="home" data-spy="scroll" data-target="#navbarColor01" data-offset="90">
```

Note as you hover over each element you have the ability to view the code with the "<>" button that appears.  You can copy the code from that window also - a handy feature.

View the <a href="https://steveshead.github.io/bootstrap4-elements-v2/">demo</a> site <a href="https://steveshead.github.io/bootstrap4-element-v2/">here</a>.

---------------------------------------------------------

I have been searching the web for a 'kitchen sink' document of all Bootstrap 4 elements, but could never find one.  I found some UI kits out there and have borrowed the elements pages to create this.

When I create a UI kit from this, I create an SCSS folder inside the assets folder and create a file called custom.scss.  Using Atom I compile that file to the assets/css/custom.css and replace bootstrap.css in the head section of my index.html with custom.css.  Note that bootstrap.scss has to be imported at the bottom of the custom.scss file for this to work.

Here are some examples of overriding Bootstrap (using custom.scss).

```scss
// override bootstrap default theme colors
$theme-colors: (
  "primary": #375a7f,
  "secondary": #444,
  "success": #00bc8c,
  "info": #3498DB,
  "warning": #F39C12,
  "danger": #E74C3C,
);

// increase the default spacing
$spacer:1.25rem;

// adjust the default heading font weight
$headings-font-weight:300;

// adjust the default font weights
$font-weight-light:200;
$font-weight-normal:300;
$font-weight-bold:500;

// adjust the default font size
$font-size-base:1.2rem;

// add more spacers
$spacer: 1rem !default;
$spacers: (
    6: ($spacer * 4),
    7: ($spacer * 5),
    8: ($spacer * 7.50),
    9: ($spacer * 10)
  );

// set the button border radius
$btn-border-radius:2px;

// change the hyperlink color
$link-color: #00bc8c;

// remove underline from hyperlinks
$link-hover-decoration: none;


// Core bootstrap scss import - this should always be at the bottom of the custom.scss file
@import '../../bootstrap/scss/bootstrap';
```

View the <a href="https://steveshead.github.io/bootstrap4-elements-v2/">demo</a> site <a href="https://steveshead.github.io/bootstrap4-element-v2/">here</a>.
